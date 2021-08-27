## :pancakes: Pancake Swap Exchange (Rinkeby)

# Prepare your smartcontract
- Router address
- Factory address
- WETH address

# Instructions
- mod .env to rinkeby configuration
- mod `ROUTER_ADDRESS` in `/src/constants/index.ts`
- mod `FACTORY_ADDRESS` and `INIT_CODE_HASH` in `/src/sdk/constants.ts`
- mod `MULTICALL_ADDRESS` in `/src/constants/multicall/index.ts`

# Custom WETH
- replace WETH (address) in `/src/sdk/entities/token.ts`
- replace WETH abi in `/src/constants/abis/weth.json`

# Get multicall address from https://github.com/makerdao/multicall
- replace MULTICALL abi in `/src/constants/multicall/abi.json`

# Supported ChainIds
- mod supportedChainIds to `[1,4]` in `/src/connectors/index.ts`
- mod `enum ChainId` `MAINNET = 1, BSCTESTNET = 4` in `/src/sdk/constants.ts`
- mod `BSCSCAN_PREFIXES` in `/src/utils/index.ts`
`{
  1: '',
  4: 'rinkeby.'
}`

# Tokenlist
- Add your `ERC20Token` to tokenlist in `pancakeswap.json`
- Make sure your chainId in tokenlist is all `4` (rinkeby)