## Description
EncryptedERC20 is introduced which is called by the Safe contract to wrap and distribute the tokens.
<br>
<br>
<img width="1121" alt="Screenshot 2024-06-25 at 19 42 12" src="https://github.com/0xprinc/confidential-gnosis/assets/82727098/c8fc3769-ca4d-46e6-ae4d-a7f1f019b5d9">

## Setup
- Install dependencies
```Shell
pnpm install
```

- compile code
```Shell
npx hardhat compile
```

- Go to test/instance.ts and update the configuration for Rivest.
``` Javascript
export const createInstance = async () => {
  const instance = await createFhevmInstance({
    networkUrl: network.config.url,
    gatewayUrl: "http://localhost:7077" //"https://gateway.rivest.inco.org", // "http://localhost:7077"
  });
  return instance;
};
``` 

- run tests
```Shell
npx hardhat test --network Inco
```