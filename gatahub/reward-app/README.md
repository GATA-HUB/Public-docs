# Reward App

## Product Specification & FAQ (Community Reference)

_A reference for docs, help centers, and community moderators. Written to be accurate to how the product actually works. Some economic values (per-chain weights, the monthly PHOTON pool, sats-boost percentages, claim minimums) are **team-tunable** and may change without a code release — always treat the in-app numbers as the source of truth._

***

### 1. What GATA REWARD HUB is

GATA HUB is a **yield hub and engagement dashboard** for the GATA community across three Cosmos SDK chains — **Cosmos Hub (ATOM)**, **AtomOne (ATONE)**, and **Akash (AKT)** — plus the GATA NFT collections. It brings four things into one place:

1. **A unified view** of your delegations, NFT holdings, and Tier Score across all chains.
2. **Two live rewards** you can self-claim: an **NFT Holder Reward** (PHOTON) and a **Loyalty Bonus** (Bitcoin/sats for delegators).
3. **A Tier Score engagement system** (the "Atonement ladder") that ranks wallets and unlocks perks.
4. **Provably-fair raffles** and community seasons.

You connect with **Keplr**. The app is **non-custodial** — it never holds your funds; every on-chain action is a transaction _you_ sign in your own wallet.

***

### 2. One wallet, all chains

Cosmos Hub, AtomOne, Akash (and Stargaze) all use coin type 118, so a single Keplr account has the **same underlying address** under each chain's prefix. Connect once and GATA HUB derives your `cosmos1…`, `atone1…`, and `akash1…` addresses automatically — no separate sign-ups per chain.

***

### 3. Tier Score & the Atonement ladder

**Tier Score** is a single number that measures how much you back GATA. It is **derived** — recomputed from your live on-chain state every time you sync — from three parts:

```
Tier Score = Delegation Score + Permanent Points + NFT Hold Score
```

* **Delegation Score** — earned by staking to the GATA validators. It counts **whole tokens bonded × a per-chain weight** (set by the team). It is **price-independent**: a market dip never lowers your score; only unbonding does.
* **Permanent Points** — one-time, never-reversing points from burns, referrals, milestones, badges, the welcome bonus, ticket/points purchases, and community seasons.
* **NFT Hold Score** — a fixed score per GATA NFT you hold, varying by collection and rarity. It's **live** (drops if you sell). Genesis cats (Colonial/Voyager) only count while staked.

#### Tiers

| Tier    | Min Tier Score |
| ------- | -------------- |
| Fallen  | 0              |
| Ember   | 1,000          |
| Seeker  | 2,500          |
| Devout  | 10,000         |
| Radiant | 25,000         |
| Star    | 50,000         |

Higher tiers unlock a bigger **Loyalty Bonus boost**, **raffle standing tickets**, and status.

***

### 4. The two rewards

Both rewards **accrue continuously** and are **claimed by you** with a wallet signature. There is **no expiry** — unclaimed rewards keep accruing.

#### 4a. NFT Holder Reward (PHOTON)

* A **monthly PHOTON pool** (PHOTON is AtomOne's token), split across the GATA collections by collection share × rarity.
* Accrues per token you hold; **Genesis cats (Colonial/Voyager) must be staked** to earn.
* Selling or unstaking a token **seals** what it accrued up to that point as a credit, so you never lose earned value by moving on.
* Paid in **PHOTON on AtomOne**. A small minimum-claim threshold prevents dust claims.

#### 4b. Loyalty Bonus (Bitcoin / sats)

* For **delegators** to the GATA validators. Accrues from your bonded time × the live staking APR × the validator commission share, then **boosted by your tier**.
* Ratchets up hourly into locked sats, so a later price move **can't shrink** your accrued balance.
* Paid in **Bitcoin (allBTC) on Osmosis** — the payout is sent to your `osmo1…` address.
* A small minimum-claim threshold (in USD) applies.

**Tier boost (current):** Fallen +1% · Ember +2% · Seeker +3% · Devout +5% · Radiant +10% · Star +20%. _(Team-tunable.)_

***

### 5. NFT collections

| Collection     | Notes                                                 |
| -------------- | ----------------------------------------------------- |
| Colonial Cats  | Genesis (2022) — scores & earns **only while staked** |
| Voyager Cats   | Genesis (2022) — scores & earns **only while staked** |
| Yield Walkers  | Yield collection                                      |
| GATA Pixels    | Redeem collection                                     |
| PengOnes       | Yield collection                                      |
| Yield Gorillas | Yield collection                                      |
| Yield Paws     | Yield collection                                      |
| Yield Crocs    | Yield collection                                      |

Rarity affects both **hold score** and **PHOTON reward share**. External (non-GATA) collections can also be registered by the team for holding score and burning.

***

### 6. Badges, milestones, referrals, seasons

* **Badges** — permanent, each worth Tier Score: the six **tier badges** (one per tier), **Tri-chain Staker**, **First Flame** / **Pyromancer** (burning), **Recruiter** (referrals), and **Old Guard** (stake a 2022 Genesis cat).
* **Milestones** — First delegation, First reward claim, Claim rewards 10 times.
* **Referrals** — invite others; when a referral qualifies (delegates a threshold, or burns, or boosts) **you** earn +500 Tier Score, up to 5 referrals.
* **Welcome bonus** — a one-time Tier Score bonus for new members.
* **Seasons / Community Goal** — a collective delegation target; when the community hits it, every qualifying participant earns a Tier Score reward.

***

### 7. Raffles (provably fair)

GATA HUB runs recurring raffles in five cadences:

* **Weekly / Monthly / Surprise** — entered by **activity** (delegating, burning) or by buying tickets during the draw.
* **Quarterly / Yearly** — **tier-standing** draws: your tier auto-enters you (higher tiers get more standing tickets). These are not earned by activity.

Draws are **trustless**: each raffle commits to a future **drand** randomness round (unknowable when the raffle is created), and a public **/verify** page re-runs the exact draw in your browser so anyone can confirm the winners. Prizes are paid token-exact (PHOTON, BTC, USDC, or an NFT).

***

### 8. Burning NFTs for score

You can **burn** GATA (and registered external) NFTs to earn permanent Tier Score, valued at the collection's **live floor price** at burn time × a multiplier. **Burning is irreversible.** Genesis cats (Colonial/Voyager) are excluded from burning.
