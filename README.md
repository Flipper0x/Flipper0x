# Flipper0x 
A Decentralized ShapeShift for small-cap tokens with continuous liquidity. 

## Problem
Decentralised exchange is mission critical infrastructure for tokenized projects. The 0x Protocol is a giant leap forward enabling the long tail of tokens. However for the time being liquidity remains thin, there is no simple mechanism for incentivizing market makers, and the [radarrelay](http://radarrelay.com) UX is too complex for the average user. 

## Solution
Flipper0x is a fully decentralized ShapeShift alternative for tokens within the Aragon Network. There is no counterparty risk and Tokens listed on Flipper0x have continuous liquidity using the Bancor Protocol as an automated market maker.

All the tokens listed will have ETH and DAI pairs.

Any longterm holder of ETH, FL0X, or any token listed on Flipper0x, can use their holdings to earn fees for providing this continuous liquidity by holding the intermittent token of a relayer.

### Token relayer
Each pair is a token relayer built on Bancor. A token relayer is an automated market maker giving the tokens continuous liquidity.

### How it works
- Alice, a [BitPoint Network](http://bitpoint.network) teller wants to buy some BPT tokens 
- She sends ETH to the token relayer, which would buy an intermediate token called BPT-ETH. This BPT-ETH token would then be exchanged again for BPT.
- This intermediate step will be abstracted away in the exchange interface to improve user experience; there will be a separate interface similar to [memefactory](memefactory.io) for investing liquidity in a relayer.
- The fee for each of these conversions would be 0.1%, and since two transactions took place the total fee would be 0.2%.
- The token relayer has a stock of each of the tokens (BPT & ETH), and they are priced based on the quantity of each token in the contract. If BitPoint Network users see BPT priced slightly cheaper than market value (radarrelay), they'll have an incentive to purchase it, shifting the pricing back up to normal. If ETH is cheaper in comparison, then users may sell their BPT at a premium.

This explanation of how bancor relayers work was adapted from this great article on the [Enjin token relayer](https://blog.enjincoin.io/enjin-coin-bancor-token-relay-explainer-11313c0bab2).

### Who provides liquidity?
In the example of a BPT-ETH relayer, people that own BPT or ETH tokens can transfer them into the token relayer, and receive an 'IOU' token called BPT-ETH. Anyone can place some of their long-term holdings of BPT or ETH into the token relayer and provide liquidity while watching their holdings grow.

In the medium to long-term, we expect 0x Protocol to have massive amounts of volume. Flipper0x relayers will be connected 0x through bots arbitraging the price and connecting the liquidity pools.

This will be of great benefit to small-cap tokens by providing a market maker service as well as giving HODLers the opportunity to grow their stake in the projects they believe in.

### D0xINFRA framework 
Relayers are analogous to curation markets in that they mint and burn tokens at a price dependant on a bonding curve.

Using the d0xINFRA framework, relayers will be the equivalent of memes in [memefactory](http://memefactory.io). By depositing their token users will receive the relayer's intermediate token in exchange. This can be displayed as an upvote for curation of the relayer in the interface. 

### User experience
Bancor relayers do not require an order book which leads to a very simple and intuitive UX, similar to that of ShapeShift. The interface has three views:

1. The token-exchange interface. Here, users select the token-pair and number of tokens they want to trade (DNT-DAI, 150DNT), and the price is displayed.

2. A list of (ETH, DAI) pairs sorted by capitalization.

3. A memefactory-style interface for users providing liquidity.

Flipper0x builds on the simplicity of the ShapeShift model as well as totally eliminating counterparty risk by being fully decentralized.

Flipper0x has a mobile-first interface built for Status, Cipher, and Toshi. 

In addition to being fully decentralized, users do not need to add a send or receive addresses. Flipper0x uses the sends and receives from the wallet used for web3 injection (metamask, or mobile browser interface).


### Token Curated trading pairs 
The list of trading pairs Flipper0x supports will be curated by DNT token holders. Flipper0x will implement a carbon voting system similar to the District0x proposal system. DNT token holders will make a proposal by opening an issue on the Flipper0x trading pairs repository. 

These pairs can then be voted on using the carbon voting app. The top pairs will be added to the Flipper0x exchange.

Total deposited funds in the relay are used to curate a list view of relayers with the highest capitalized at the top.

### FL0X Token
- Total supply: 1,000,000 FL0X
- Community incentives: 400,000 FL0X
- Token sale: 400,000 FL0X
- Retained: 200,000 FL0X 
- Founders and Advisors: 0 FL0X ☺

Contract:  0xa13F7D0f7e67B1d62bAa72a8CB9C32774f19c444
Decimals: 18
Ticker: FL0X
Token Tracker:
[Click here](https://etherscan.io/token/0xa13f7d0f7e67b1d62baa72a8cb9c32774f19c444)


FL0X is a asset-backed governance token. All decisions from development bounties to funding relayers will be decided by token holders.

Fees collected from relayers and any advertising revenue will be distributed to token holders. 

1,000,000 FL0X is currently backed by ~$10,000 in tokens and Ethereum.

- 40% of the tokens will be distributed to the community for code contributions and community participation.
- After the completion of stage 1, 40% of the tokens will be sold to fund stage 2.

### Governance 
Flipper0x will be governed by token-weighted direct democracy. All the DAO's parameters are subject to change by token holders including the governance system itself.

Direct democracy is a simple and agile system. However, as the organization grows, a more scalable governance system will be needed.

All the organization's assets will be transferred to an AragonOS with the launch of the mainnet release.

### Conclusion
Achieving liquidity will be a major concern for small-scale DAOs. Flipper0x will provide a mechanism for these types of projects.

If you're a graphics designer, front/back-end dev, or just interested in the idea join the conversation and earn some tokens! 

[T.me/Flipper0x](t.me/Flipper0x)

### Milestones
Flipper0x is an open source project. Development will be incentivized for by placing bounties in ETH, DNT, SNT, ANT and Flipper0x native token FL0X for all milestone tasks on Status [Open Bounty](https://openbounty.status.im) and [Ethlance](ethlance.com).

A list of bounties can be found here in the bounties repo (issues):
https://github.com/Flipper0x/bounties

Ethlance job post can be found here:
https://ethlance.com/#/job/286

Stage 1 bounties:

- 100,000 FL0X
- 20,000 DNT
- 700 SNT
- 400 ANT
- 1 ETH

Stage 1: 
- [x] Conceptual outline
- [x] initial funding 
- [x] Mint token
- [x] Setup Bounties 
- [ ] Wireframes
- [ ] Artwork and branding  
- [ ] Clickable demo with initial pair 
- [ ] Write frontend contracts 
- [ ] Deploy relayers to Kovan testnet
- [ ] Connect Flipper0x interface and frontend contracts to relayer
- [ ] Integrate into Status
- [ ] Carbon voting

Telegram: [T.me/Flipper0x](t.me/Flipper0x)

Address: 0x4875d7B642E68F216B36737e90733eB9951D9E67
