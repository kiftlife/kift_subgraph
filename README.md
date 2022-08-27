## The Graph API

We use the graph to index transaction events on the blockchain to a query-able api which helps do more powerful operations than the methods available on the contract itself. An example would be:

- find the nfts owned by a wallet address
- check if nft has been revealed
- check if nft has perks redeemed

### Setup

1. Download The Graph CLI

`yarn global add @graphprotocol/graph-cli`

2. Install dependencies

`yarn install`

3. Ensure you have auth'd using the graph access token (request for access).

`graph auth --product hosted-service <ACCESS_TOKEN>`

4. Upon making changes to the schema run the command

`graph codegen && graph build`

5. Deploy changes to the graph

`graph deploy --studio <SUBGRAPH_SLUG>`
