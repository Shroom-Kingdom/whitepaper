# Token Economics

The native Fungible Token for Shroom Kingdom is called Shroom and has the symbol SHRM.
Fungible Tokens do not differ from each other and are a common way to develop "money-like" tokens.

Since SHRM is commonly minted by playing on Shroom Kingdom, there is no upper limit.
Instead, a constant minting and burning mechanism should make sure, that the token's value
won't suffer from inflation or deflation.

Also keep in mind, that this document often talks about minting, but in fact the tokens
do not yet exist on-chain.
Instead they will be stored in an off-chain database first.
The user can then decide to mint its SHRM tokens by calling a Smart Contract.
This mechanism is explained more in depth in the [Smart Contract details](#smart-contract-details)

## Minting and burning

SHRM tokens will be minted by one of the following tasks:

- finishing a level (max 5 x 1 SHRM / day)
- voting/rating a level (max 1 x 3 SHRM / day)
- daily challenges (5 SHRM / day)
- passive generation while others play own levels (max 8 SHRM / day).

SHRM tokens will be burned by one of the following tasks:

- unlocking new building blocks and entities that can be placed in levels (token amount varies)
- minting of levels (100 SHRM)
- challenge passes (tbd)
- virtual land acquisition and NFTs involved (tbd)

Since Shroom Kingdom will launch with relatively few game mechanics as a Minimum Viable Product,
there won't be many ways for burning SHRM tokens.
Once more game mechanics will be implemented, there will also be more ways to burn tokens.
To prevent inflation in the early days after launch, a multiplier will be applied to all previously
mentioned minting mechanisms.

To make sure that every kind of player enjoys playing on Shroom Kingdom, the SHRM token minting
will be capped at 13 SHRM per day (8 SHRM for playing/building + 5 SHRM for daily).
Players can either decide whether they want to earn their tokens by playing or by building levels
or by a combination of both.

## Initial SHRM token launch & funding

- initial SHRM token generation of 10mm
  - 15% founder (=1.5mm)
  - 40% DAO (=4mm)
  - 20% IDO (=2mm)
  - 20% Liquidity (=2mm)
  - 5% Airdrops (=0.5mm)

- IDO sale for NEAR token. Distribution:
  - 25% founder
  - 75% DAO

## Smart Contract details
