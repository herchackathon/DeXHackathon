# DeXHackathon
## Instructions for India Decentralized Exchange Track 
# Overview
Currently, decentralized exchanges are inefficient and difficult to operate for the average user. As a result, they generally have reduced liquidity. Cryptocurrency is evolving at a rapid rate and we must ensure that blockchain technology is able to keep up.

This is an all-hands-on-deck initiative, combining the state-of-the-art technological excellence in our industry and the best of you students to once again push the envelope in technology.

In addition to having internal teams working on dex implementation, we are arranging this hackathon to work closely with bright young minds as yourselves and build the next generation blockchain.

To help facilitate this innovation, Hercules is hosting this coding competition with the clear intent of merging the best implementation(s) and/or team(s) into the (H)ERC Protocol. On top of this, we will also offer a total prize pool equivalent of $20,000 USD, paid in HERC. How does winning HERCs, then joining the Hercules team sound to you?
This paper outlines the high level requirements of what we are looking for, as well as our initial design philosophies for Hercules.

# Goal
The objective of this project is to solicit prototypes of a decentralized exchange with a focus on speed and capacity, or more precisely, a dex blockchain that is low-latency and high-throughput.
The dex prototype should have the following features:
> - Sending and receiving of the native coin
> - New token creation
> - Sending, receiving, freezing, and burning of tokens
> - Ability to trade one token with another token (all within the same chain)
 
# Bonus feature:
Native on-chain ICO


For performance, we recommend the following design considerations:
> - All features mentioned above built-in natively to the blockchain
> - No support for smart contracts, virtual machines or turing complete languages
If a trade-off is required, always choose speed and simplicity over fancy features.

# Mining & Consensus
A blockchain where all native tokens are pre-mined, there will be no mining (all HERC tokens will be converted from (H)ERC777 tokens that already exist today). You are free to use any consensus algorithm you like; performance is key.
 
# Basics
Basic features such as block generation and sending/receiving of the native coin should obviously be included. You are also free to use graphs instead of chains, assuming you can make it work reliably.

# Token Creation
Native support for new token generation is required. That is, users should be able to create new tokens simply by specifying token parameters, such as symbol, total supply, decimals, etc, without having to write smart contracts. New token generation will cost a fee, payable in the native coin of the blockchain.

Tokens can follow a simple structure; fixed supply, all pre-mined, etc. Again, if there is a need for a trade-off between advanced features vs speed and simplicity, the latter wins.
 
 
# Orders & Trades
Users should be able to place orders and trade one token for another directly on the blockchain. These orders should be natively supported by the blockchain and not via smart contracts. Limit GTC orders must be supported, and bonus points may be awarded for limit FOK and IOC, market, and other advanced order types, but keep in mind that speed is of higher priority.
## An order should contain:
> - Symbol (trading pair)
> - Side
> - Price
> - Amount
> - Expiry time (in blocks)
> - Owner

` Trading is done via sending orders to the network. As network resources are required to process each order, a fee will apply. The order fee will be dynamically adjust based on how busy the network is, similar to other network fees. Order fees are charged when the orders are submitted to the network.`

`Orders can be cancelled before they are traded. Each cancellation is also a new message to the network, thus incurring another network fee.`
`If an order matches against another order, a trade event happens. A trade is simply one atomic event involving two token transfers on the network. Again, network transfer fees will apply.`
`A trade should also trigger an execution report. We recommend an execution report structure similar to standard FIX 4.4 or higher protocol.`

# Matching Engine
You are free to use on-chain or off-chain matching engines in your design. The main consideration factor should be performance.

# Nodes
Nodes on the blockchain will handle:
> - Sending of the native coin
> - Issuing of tokens
> - Sending/receiving of tokens
> - Placing orders and handling trades

Nodes on the network will be compensated by transfer, order, trading, and other fees. Other fees include token creation, and potentially ICOs at a later date.

For this competition, nodes running in one OS will suffice, ideally Linux.

# Wallet
The wallet is the user’s interface to the blockchain. For the purpose of this dexathon, GUI wallets are not required and a command line interface (CLI) will suffice.

# ICO
While not required, a natively supported ICO implementation will definitely earn bonus points.

# Implementation
We generally like to see new implementations built from scratch, but you may choose to fork existing blockchain implementations and improve upon them. We Recommend https://github.com/0xproject 

You must ensure you do not violate any copyright or license restrictions.

Considering each trade may involve many orders, you will probably want to avoid (or change) blockchains that only allow you to have one input and one output address. Bitcoin’s many-to-many model may be a better fit here.
 
# Prize
As previously mentioned, we will offer a prize pool equivalent to $5,000 USD, paid in HERC. In addition, winning team(s) may also be considered for employment.

# Schedule
All entries must be submitted by oct 10th, 2018 23:59 UTC. Any entries submitted after this deadline will be ineligible.
You may submit your application now and continually update it until the deadline. After the submission deadline, Hercules will take a reasonable amount time to review the submissions.

# To Apply
You must register to participate in this competition. Please send the information below to social@herc.one:
Name(s)
CV(s) or LinkedIn link(s)
Team size / Team Name 
Github repo location (can be private during the competition)

# Questions
If you have any questions, please feel free to contact us at social@herc.one. You must have already submitted your application before asking detailed questions about the competition.

Lastly, Hercules reserves all rights to adjust the rules of this competition, with or without further notice.

