# ETH-AVAX-MOD-4
# DegenGamingToken (DGT) Contract

The DegenGamingToken (DGT) contract is an ERC20 token smart contract deployed on the Avalanche network. It's designed to facilitate various operations for Degen Gaming, including minting, transferring, redeeming prizes, checking token balance, and burning tokens. The contract owner has special privileges to manage the token supply and add prize items.

## Features

The DGT contract provides the following features:

1. **Minting New Tokens**: The owner can mint new tokens and distribute them to players, allowing rewards to be given out.

2. **Transferring Tokens**: Players can transfer their tokens to other addresses.

3. **Redeeming Prizes**: Players can redeem their tokens for items in the in-game store. The cost of the prize is deducted from the player's balance.

4. **Checking Token Balance**: Players can check their token balance at any time.

5. **Burning Tokens**: Any token holder can burn tokens they no longer need.

## Prizes

The contract supports an in-game store where players can redeem prizes using their tokens. The initial contract deployment includes four predefined prizes, each with its associated cost:

1. Prize ID 1: Cost 1000 tokens
2. Prize ID 2: Cost 500 tokens
3. Prize ID 3: Cost 200 tokens
4. Prize ID 4: Cost 100 tokens

The contract owner can add new prize items with their respective costs using the `addPrizeCost` function.

## Usage

To interact with the DGT contract, you can use a tool like the Avalanche Web Wallet or a custom web application that interacts with the contract's functions.

Here are some key functions:

- `redeemPrize(uint256 prizeId)`: Allows players to redeem a prize item based on its prize ID. The cost of the prize is deducted from the player's balance.

- `getTokenBalance(address account)`: Returns the token balance of a given player's address.

- `burnTokens(uint256 amount)`: Allows any token holder to burn a specified amount of their tokens.

- `mint(address account, uint256 amount)`: Only the contract owner can mint new tokens and distribute them to player addresses.

- `transferTokens(address to, uint256 amount)`: Allows players to transfer tokens to other addresses.

## Important Considerations

- **Security**: Ensure that the contract is thoroughly tested and audited before deploying it in a production environment. Be aware of potential security risks when interacting with smart contracts.

- **In-Game Logic**: The contract provides the foundation for redeeming prizes, but the specific logic for providing in-game items as prizes is not implemented in this contract. This functionality should be integrated with an off-chain system.

- **Token Economics**: Consider the overall tokenomics, distribution mechanisms, and potential impacts on the gaming ecosystem.

## Deployment

To deploy this contract, you'll need access to the Avalanche network and a compatible smart contract development environment. Ensure that you've properly configured the deployment parameters, such as the network URL and the contract owner's address.

## License

This contract is licensed under the MIT License, which allows you to freely use, modify, and distribute the code. See the [LICENSE](LICENSE) file for more details.
