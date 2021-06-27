# Fuse

[Fuse](app.rari.capital/fuse) is an open interest rate protocol that allows DeFi users to lend and borrow ERC20 tokens. Each Fuse pool is a fork of the [Compound Finance protocol](Compound.Finance). The Fuse protocol enables anyone to instantly create and deploy their own lending and borrowing pool. This protocol allows users to choose all of their custom parameters and isolate risk, rater than using a large lending and borrowing pool on other platforms. Pools can be made public or private depending on the creator's preference. 

Fuse launched in April 2021 and as of June 2021, the protocol is continuing its guarded launch. Once further audits are complete, the RSS is redesigned, adn the user interface is updated, we will then allow governance to decide when permissionless pool creation is available for all users. For right now, all pool changes and new pool deployments can be pitched to governance using the pre-set templates. 

Thank you to [Compound Finance](Compound.Finance) for the detailed descriptions. Since each Fuse pool is its own version of the Compound Finance protocol, some of the descriptions below are copied directly from the [Compound Finance Docs](https://compound.finance/docs). 

*The following parameters and customization preferences can be chosen by the pool creator when creating a Fuse pool:* 

- **Custom assets**

As long as there is an oracle (shown below), a Fuse pool can support it. 

- **Custom oracles (Chainlink, Uniswap/SushiSwap TWAPs, Keep3r)**

If there is an oracle feed supported by the protocol that reports price information for the asset, then the token can be used on Fuse. 

- **Platform fee**

10% fee of all intrerest accrued is dsitributed to the [$RGT community owned treasury](https://etherscan.io/address/0x10dB6Bce3F2AE1589ec91A872213DAE59697967a).

- **Admin fee**

Fuse pool creators can choose to add a fee on top of the protocol fee. 

- **Liquidation incentive (Description from [Compound Finance](Compound.Finance))**

The additional collateral given to liquidiators as an incentive to perform liquidation of underwater accounts. For example, if the liquidation incentive is 1.1, liquidatores recevie an extra 10% of the bottrowers collateral for every unit they close. 

- **Whitelist**

Fuse pool creators can choose for a pool to be permissioned for select Ethereum addresses if they choose. This could be for KYC purposes down the road once we partner with a partner to help us build out the infastructure. 

- **Close factor** **(Description from [Compound Finance](Compound.Finance))**

The percent, ranging from 0% to 100%, of a liquidatable account's borrow that can be repaid in a single liquidate transaction. If a user has multiple borrowed assets, the closeFactor applies to any single borrowed asset, not the aggregated value of a user’s outstanding borrowing.

- **Upgradability**

When the upgradability function is turned ON, the underlying Fuse pool Smart Contracts can be modified, as well as any pool parameters that were set during the pool creation stage. 

- **Collateral Factor (Description altered from [Compound Finance](Compound.Finance))**

A fToken's (Fuse liquidity proof token) collateral factor can range from 0-90%, and represents the proportionate increase in liquidity (borrow limit) that an account receives by minting the fToken.

Generally, large or liquid assets have high collateral factors, while small or illiquid assets have low collateral factors. If an asset has a 0% collateral factor, it can't be used as collateral (or seized in liquidation), though it can still be borrowed.

- **Reserve Factor (Description altered from [Compound Finance](Compound.Finance))**

The reserve factor defines the portion of borrower interest that is converted into reserves.

Reserves are an accounting entry in each fToken contract that represents a portion of historical interest set aside as liquid cash which can be withdrawn or transferred through the protocol's governance. A small portion of borrower interest accrues into the protocol, determined by the reserve factor

- **Pool Admin**

Deployer and owner of the pool. This can be a singular Ethereum address, a multi-sig, DAO contract, etc. The address that owns and manages the pool is responsbile for parameter upkeep. 

## Supported Price Oracles

*Is there an oracle missing? Ping @DavidLucid in the #Fuse [Discord]([http://discord.gg/mtb6W57Ap6](https://t.co/nGY7gkihfQ?amp=1)) channel to have it added!*

- AlphaHomora V1
- AlphaHomora V2
- Badger Price
- Balancer LP
- Base Price 
- Chainlink 
- Curve Liquidity Gauge
- Curve LP Token
- Fixed ETH Price
- Fixed EUR Price
- Fixed Price
- Fixed Token
- Fixed USD
- Keep3r Price
- Keep3r V2 Price
- Master Price
- mStable Price
- Opeth Price
- Preferred Price
- Synthetix Price
- Recursive Price
- Uniswap LP Token
- Uniswap TWAP Price
- Uniswap V3 TWAP Price
- WSTETH Price 
- YVault V1 Price
- YVault V2 Price

## How to Earn Interest 

**Step 1: Connect a wallet**

The Rari Capital ecosystem currently supports [MetaMask](metamask.io), [WalletConnect](walletconnect.org), [Portis](portis.io), [Torus](https://tor.us/), [Formatic](https://fortmatic.com/), and [Authereum](https://authereum.com/). If you do not have a wallet, we recommend you refer to [this guide ](https://metamask.zendesk.com/hc/en-us/articles/360015489531-Getting-Started-With-MetaMask-Part-1)for [MetaMask](Metamask.io). Users can connect their wallets by selecting the "Connect Wallet" button on the [Rari Capital Fuse Portal](https://app.rari.capital/Fuse).

**Step 2: Become friendly with the Fuse dashboard**

Once connected, users will see *Supply Balance* and *Borrow Balance.* Don't worry! It's okay for these to both be $0 when you connect for the first time. Now that you are looking at the main dashboard, It's time to start getting comfortable with the user experience. Normally when you enter an open interest rate protocol portal like [Compound Finance](compound.finance), [Aave](aave.com), or [CREAM](Cream.Finance), you will immedaitely see supply and borrow tabs. This is different for Fuse, as you have to select the pool you want to lend or borrow to first! Once you select the pool that fits your choice of assets and parameters, you will now be looking at a screen with two sides: Supply and Borrow. The Supply side shows assets that you can supply to this specific Fuse pool to earn interest, while the Borrow side shows assets that you can borrow from this specific Fuse pool. Remember, everything you do in one Fuse pool is kept isolated from the rest of the pools on the platform.

**Step 3: Supply Assets to Fuse**

1. Select the asset that you would like to supply

2. Enable permissions for the Fuse protocol to interact with your asset by confirming the Ethereum transaction. 

   *Note: this will cost gas.*

3. A new window will pop up on your screen displaying the current supply APY and it will adjust based on the amount you type in

4. Now that the token has been enabled and you have typed in your desired amount to lend, click Supply and you are all done! 

   *Note: this is a transaction that will cost gas.* 

You have now supplied your first asset to a Fuse pool! On your main dashboard, you see wil see *Supply Balance* populate with the equivalanet amount (in dollars) to your newly supplied asset. 

*Note: This asset will no longer appear in your wallet as it is now in the Fuse Protocol. You will immediately receieve an fToken that represents your share in the pool. You will not have to worry about this token, but when you withdraw, your fToken will be used to redeem the underlying supply balance.*

*You will only earn interest when the pool is being utilized by borrowers*

## How to Borrow

**Step 4: Borrow against your supplied collateral**

Now that you have supplied assets, you have the opportunity to borrow assets in the same Fuse pool! Why might you do this? Users are constantly seen borrowing against their assets to gain leverage (borrowing stablecoins to buy more tokens) or borrowing to short an asset (selling an asset and buying it back at a later date), or even a chance to take out money against an appreciating asset that you do not wish to sell. 

*Note: There is a signficant amount of risk when borrowing assets, and you should do your own research and education before using this functionality*

1. Select the asset that you would like to borrow 

2. A new window will pop up on your screen displaying the current borrow APY and it will adjust based on the amount you type in

3. Now that the token has been selected and you have typed in your desired amount to borrow, click borrow and you are all done! 

   *Note: this is a transaction that will cost gas.* 

**Step 5: Understanding liquidation health**

Ethereum based assets can be extremely volatile in price action, meaning your supplied amount can change rapidly which could cause the amount you can borrow to change abruptly based on price moments. 

A *Liquidation* occures when your *Borrow Limit* reaches its full capacity. Once this health bar (at the top of your dashboard) reaches 100%, your balances will be liquidated. This can come from collateral (supplied amount) dropping in value, or borrowed assets surging in value. When you get liquidated, a computer within the community will repay a percentage of your outstanding borrowed amount, as well as keeping a reward  from your collateral based on the *liquidation incentive* percentage found on each Fuse pool's dashboard. 

*Note: You should always do your own research regarding liquidations and find the safe haven for your health limit. When borrowing assets, you should consistently be checking the monitor to avoid unforeseen liquidations*

## How to Withdraw

**Step 6: Re-paying loans**

When you are ready to return back the borrowed asset, you will follow the same steps above in reverse. 

1. Select the asset that you are currently borrowing and press the re-pay tab. 

   *Note: You will have an option to re-pay the max amount or type in your desired amount*

**Step 6: Removing collateral/supplied asset**

If you would like to stop earning interest on your supplied asset and retain ownership of it in your Ethereum wallet, it is time to remove the token from the Fuse pool.

*Note: In the background, you have now redeemed your fToken for the underlying amount that we discussed earlier. This is an example of a decentralied system as the protocol never took custody of your funds.*

1. Select the asset that you are currently supply and press the withdraw tab

   *Note: You will have an option to withdraw the max amount or type in your desired amount*

We understand this process can be very tedious for your first time, but be proud of yourself for making it this far! You are on your way to becoming a strong DeFi user who takes advantage of the protocols aimed at removing the need to trust an insitution for your finances. 

------

If you would like an interactive version of this step-by-step process, we have pubished a [Fuse YouTube Tutorial](https://www.youtube.com/watch?v=V-JLIqZGWYo) to help guide you even more.

If you noticed anything throughout your experience that was not described in this tutorial, we encourage you to reach out in our [Discord](Discord.xjfjfjdf) for assistance and a community member will always be wiling to help!

## 
