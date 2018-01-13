# Flipper0x 
A Decentralized shapeshift for Aragon DAOs with continuous liquidity. 

## Problem
Decentralised exchange is mission critical infrastructure for tokenized projects. 0x Protocol is a giant leap forward enabling the long tail of tokens. However for the time being liquidity remains thin, there is no simple mechanism for incentivizing market makers, and the [radarrelay](radarrelay.com) UX is too complex for the average user. 

## Solution
Flipper0x is a fully decentralized shapeshift alternative for tokens within the Aragon Network. There is no counterparty risk and Tokens listed on Flipper0x have continuous liquidity using the Bancor Protocol.

All the tokens listed will have ANT, ETH, and DAI pairs

Any longterm holder of ETH ANT or any token within the Aragon Network can use their holdings to earn fees for providing this continuous liquidity by holding the intermittent token of a relayer.
 

### Token Relayer
Each pair is a token relayer built on bancor. You can think of a Token Relay as a vending machine for two token types.


### How it works 
- Alice, a [BitPoint Network](www.BitPoint.Network) teller wants to buy some BPT tokens 
- She sends ETH to the Token Relay, which would buy an intermediate token called BPN-ETH. This BPT-ETH token would then be exchanged again for BPT.
- this intermediate step will be abstracted away in the exchange interface to improve user experience, there will be a separate interface similar to [memefactory](memefactory.io) for investing liquidity in a relayer 
- The conversion fee for each of these conversions would be 0.1%, and since two transactions took place the total fee would be 0.2%.
- The Token Relay has a stock of each of the tokens (BPT & ETH), and they are priced based on the quantity of each token in the contract. If BitPoint Network users see BPT priced slightly cheaper than market value (radarrelay), they'll have an incentive to purchase it, shifting the pricing back up to normal. If ETH is cheaper in comparison, then users may sell their BPT at a premium.


This explanation of how bancor relayers work was adapted from this article great article on the [Enjin token relayer](https://blog.enjincoin.io/enjin-coin-bancor-token-relay-explainer-11313c0bab2)

### Who provides liquidity?
In the example of a BPT-ETH relayer, people that own BPT or ETH tokens can transfer them into the Token Relay, and receive an 'IOU' token called BPT-ETH. Anyone can place some of their long-term holdings of BPT or ETH into the Token Relay and provide liquidity while watching their holdings grow.

### d0xINFRA framework 
Relayers are analogous to curation markets in that they mint and burn tokens at a price dependant on a bonding curve.

Using the d0xINFRA framework, relayers will be the equivalent of memes in [memefactory](memefactory.io). By depositing their token they will receive the relayers intermediate token in exchange. This can be displayed as an upvote for curation of the relayer in the interface. 

### User experience 
Bancor relayers do not require an order book and thus lends itself to a very simple intuitive UX, the interface has three views

1. design is based on shapeshift. Users select the token they want (DNT-ANT), the amount of tokens they want to buy or sell, and the price is displayed.

2. A list of (ANT, ETH, DAI) pairs curated by the most capitalized

3. Memefactory style interface for users providing liquidity

Flipper0x builds on the simplicity of the shapeshift model as well as totally eliminating counterparty risk by being fully decentralized.

Flipper0x has a mobile-first interface built for, status, cipher, and toshi. 

In addition to being fully decentralized, users do not need to add a send or receive addresses. Flipper0x uses the sends and receives from the wallet used for web3 injection (metamask, or mobile browser interface)

### liquidity 
In the medium to long-term, we expect 0x Protocol to have massive amounts of volume. Flipper0x relayers will be connected 0x through bots arbitraging the price and connecting the liquidity pools.

This will be of great benefit to small-cap tokens by providing a market maker service as well as giving HODLers the opportunity to grow their stake in the projects they believe in.

### Token Curated trading pairs 
The list of trading pairs Flipper0x supports will be curated by DNT token holders. Flipper0x will implement a carbon voting system similar to the District0x proposal system. DNT token holders will make a proposal by opening an issue on the Flipper0x trading pairs repository. 

These pairs can then be voted on in using the carbon voting app, the top pairs will be added to the Flipper0x exchange.

Total deposited funds in the relay are used to curate a list view of relayers with the highest capitalized at the top.

   

### Milestones
Flipper0x is an open source project. Development will be incentivized for by placing bounties in ETH and DNT for all milestone tasks on Status [Open Bounty](https://openbounty.status.im) and [Ethlance](ethlance.com)



Stage 1: 
- [ ] Conceptual outline
- [ ] Wireframes
- [ ] Artwork and branding  
- [ ] Clickable demo with initial pair 
- [ ] write frontend contracts 
- [ ] Deploy relayers to kovan testnet
- [ ] connect Flipper0x interface and frontend contracts to relayer
- [ ] Integrate into status
- [ ] modify districts carbon voting
