# Polygon_OZG

- [Polygon_OZG](#polygon_ozg)
  - [Example Lx/Ly Bridge](#example-lxly-bridge)
  - [Setup](#setup)
    - [Frontend](#frontend)
    - [Smart Contract](#smart-contract)
  - [Resources](#resources)

## Example ERC-20 Bridge

This application is an example of both frontend and smart contract implmentation of lx/ly bridge for ERC20 token bridging.

`Frontend`

`Claim Function Listener`

## Setup

#### Frontend

- Add the Wallet Connect project id to `src/app/providers.tsx`
- [File To Edit](./frontend/src/app/providers.tsx)

```sh
cd frontend
yarn
yarn dev
```

#### Smart Contract

```sh
cd backend
npm i
npx hardhat compile
```

**Smart Contract Addresses :**

```json
{
  "ERC20BridgeMainnet": "0x716a1CbfEff5cad0c139b31D4De59B02f855aAe2",
  "ERC20BridgezkEVM": "0x8A82c434F2701A44258173287aa0497856735386",
  "erc20MainnetToken": "0x716a1CbfEff5cad0c139b31D4De59B02f855aAe2",
  "erc20zkEVMToken": "0x716a1CbfEff5cad0c139b31D4De59B02f855aAe2",
  "deployerAddress": "0x716a1CbfEff5cad0c139b31D4De59B02f855aAe2",
  "tokenName": "customTokenName",
  "tokenSymbol": "CTN",
  "tokenInitialBalance": "1000000000000000000000000000"
}
```

All addresses are on testnet.

- Bridging from `göerliETH` to `zkEVMTestnet` can be done from the frontend.
- But we need to run a claim listener in order to process the claims when ready.

To run the claim listener :

```sh
npm run monitor:polygonZKEVMTestnet
```

ENV example :

```sh
MNEMONIC="test test test test test test test test test test test junk"
INFURA_PROJECT_ID=""
ETHERSCAN_API_KEY=""
ETHERSCAN_ZKEVM_API_KEY=""
PVTKEY=""
```

## Resources

Problem Statement Link :

[https://pushprotocol.notion.site/Polygon-557f8054f87e4dec8fe14fd55e76becd](https://pushprotocol.notion.site/Polygon-557f8054f87e4dec8fe14fd55e76becd)

More Code Examples :

[https://github.com/0xPolygonHermez/code-examples](https://github.com/0xPolygonHermez/code-examples)

How ZkEVM Bridge Works ? :

[https://wiki.polygon.technology/docs/zkevm/protocol/zkevm-bridge/](https://wiki.polygon.technology/docs/zkevm/protocol/zkevm-bridge/)
