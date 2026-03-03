# CoinGecko Listing Guide for apxUSD

This guide provides a complete, step-by-step walkthrough for submitting the **Apyx apxUSD** token for listing on CoinGecko. It includes pre-filled values for every form field, mandatory verification instructions, and post-submission monitoring steps.

## Section 1: Overview & Prerequisites

Before starting the submission, ensure you have the following ready:

- [ ] **CoinGecko Account**: Create an account at [coingecko.com](https://www.coingecko.com) and sign in.
- [ ] **Logo File**: Download the logo from [assets.apyx.fi/tokens/apxUSD.png](https://assets.apyx.fi/tokens/apxUSD.png).
    - **Action Required**: Resize the image to **200x200px** (original is 256x256). Use a transparent background.
- [ ] **Whitepaper/Docs**: Use https://docs.apyx.fi or leave blank if no dedicated whitepaper exists
- [x] **Distribution Schedule**: Not applicable — apxUSD has no distribution schedule (mint/burn stablecoin)
- [ ] **Supply Data**: Refresh the supply numbers immediately before submission (see the REFRESH box in Section 4).
- [ ] **Verification Access**: Ensure you have access to the official **@apyx_fi** X (Twitter) account.
- [ ] **Duplicate Check**: Verify on [GeckoTerminal](https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665) that apxUSD does not already have a CoinGecko page. If it does, you must submit a "Token Update" request instead.

**Listing Form URL**: [https://www.coingecko.com/request-form?locale=en](https://www.coingecko.com/request-form?locale=en)

---

## Section 2: Form Type Selection (Step 0)

On the initial screen, select the following options:

- **Listing Type**: Select **"Token"** (apxUSD is an ERC-20 token).
- **Request Type**: Select **"Active Listing"** (apxUSD is live and trading since 02/23/2026).

---

## Section 3: Step 1 — Basic Coin Information

### 1. Basic Coin/Token Information

| Field                    | Value                                                                         |
| :----------------------- | :---------------------------------------------------------------------------- |
| **Coin/Token Name**      | **Apyx apxUSD**                                                               |
| **Coin/Token Symbol**    | **apxUSD**                                                                    |
| **Website URL**          | **https://apyx.fi**                                                           |
| **Website URL (2)**      | **https://docs.apyx.fi**                                                      |
| **Website URL (3)**      | *(Leave blank)*                                                               |
| **Whitepaper Link**      | **https://docs.apyx.fi** *(or leave blank if no dedicated whitepaper exists)* |
| **Submitter's Role**     | **Product Manager**                                                           |
| **Submitter's Telegram** | **koed_the_kat**                                                              |

> **Naming Methodology Note**: CoinGecko requires stablecoins to follow the `IssuerName TokenTicker` format. "Apyx apxUSD" follows their [official methodology](https://support.coingecko.com/hc/en-us/articles/33608537461913-CoinGecko-Asset-Naming-Methodology).

### 2. Project Information

Copy and paste the following descriptions exactly. Do not paraphrase.

**"What is the project about?"**
> Apyx is a stablecoin protocol that uses preferred equity from Digital Asset Treasuries (DATs) as collateral for dollar tokens. DATs are publicly listed companies that hold digital assets on their balance sheets and issue preferred shares with monthly cash dividends. The protocol acquires those preferred shares, keeps them as collateral, and routes the dividend cash flow to onchain users as yield.
>
> The system uses two tokens. apxUSD is the base dollar token and is backed by more than 100% collateral in DAT preferred shares. It does not distribute yield by itself. apyUSD is an ERC-4626 vault token. Users deposit apxUSD to mint apyUSD, and the vault distributes dividend income over time so the apyUSD to apxUSD exchange rate rises.
>
> Risk controls include daily NAV calculations, automatic rebalancing when issuer concentration passes limits, stress tests for drawdowns and rate moves, and a protocol-owned liquidity buffer above the collateral base.
>
> *(955 characters)*

**"What makes your project unique?"**
> USDT and USDC rely on fiat reserve structures and do not distribute yield to holders. Yield-bearing designs such as Ethena's USDe usually depend on delta-neutral basis and funding-rate trades. Those trades can lose efficiency when similar capital crowds into the same setup.
>
> Apyx sources yield from monthly cash dividends paid by preferred shares issued by publicly traded companies. The collateral instruments are listed on public exchanges and priced in open markets under securities regulation. Dividend payments come from issuer obligations attached to the preferred shares. Collateral capacity can expand as additional DAT companies issue preferred equity, so growth does not depend on repeating the same derivatives trade.
>
> *(729 characters)*

**"History of your project?"**
> In August 2020, Michael Saylor started converting MicroStrategy's treasury into Bitcoin. That move set the Digital Asset Treasury (DAT) playbook. Strategy, formerly MicroStrategy, later issued preferred share series STRK, STRF, STRC, and STRD to fund more Bitcoin acquisitions. STRC pays an 11.25% annual dividend through monthly cash distributions. Saylor referred to these instruments as "digital credit." Dozens of publicly listed companies then adopted the model, and the market for DAT preferred shares grew around digital asset balance sheets.
>
> DeFi Development Corp. (DFDV) became the first Solana-focused DAT listed on Nasdaq and applied the same preferred-equity structure to SOL holdings. Dividend cash flow from DAT preferred shares remained offchain, so DeFi users could not access it directly. The team behind DFDV built Apyx to move that income onchain through a stablecoin wrapper backed by DAT preferred-share collateral. The protocol launched as a dividend-backed stablecoin system backed by Digital Credit. Development began in late 2025, and the protocol launched on Ethereum in February 2026.
>
> At launch, Apyx worked with Anchorage Digital and BitGo for custody, Gauntlet for risk modeling, and Morpho and Pendle for DeFi integrations. Anchorage Digital, which also holds STRC on its own balance sheet, acts as primary custodian for the preferred-share collateral. Quantstamp audited the smart contracts, and Certora performed formal verification.
>
> *(1467 characters)*

**"What's next for your project?"**
> Current work centers on Ethereum market depth for apxUSD and apyUSD. The team is coordinating with Morpho and Pendle to expand lending markets and yield-trading venues. Apyx has stated that it will publish monthly accounting attestation reports so collateral data remains verifiable.
>
> Collateral coverage can broaden as more DAT companies issue preferred equity. The current collateral set is still limited, but the DAT issuer base is growing. Protocol design already supports onboarding additional preferred-share issuers when they become available.
>
> A governance token called APYX is planned. Proposed governance scope includes selecting eligible preferred shares, setting yield split parameters between apxUSD and apyUSD holders, and directing general protocol policy. The team has also discussed expansion beyond Ethereum, with no public chain-by-chain launch schedule yet.
>
> *(877 characters)*

**"What can your coin/token be used for?"**
> apxUSD is the base dollar token in the Apyx system. It targets stable value using DAT preferred-share collateral and can be used in common stablecoin workflows, including trading pairs, lending collateral, liquidity provision, and settlement. The token trades against USDC on Curve Finance. apxUSD itself does not distribute yield.
>
> apyUSD is the yield-bearing token. Users deposit apxUSD into an ERC-4626 vault and receive apyUSD. The vault receives dividend income from underlying preferred shares and distributes that value linearly, so the apyUSD to apxUSD exchange rate increases over time. The mechanism follows the same exchange-rate model used by Maker's sDAI and Ethena's sUSDe. Holders can redeem apyUSD back to apxUSD at the current rate.
>
> DeFi integrations extend the utility further. apyUSD can be deposited into Pendle to separate and trade the yield component, and it can serve as collateral on platforms that accept yield-bearing assets. Both apxUSD and apyUSD are ERC-20 tokens on Ethereum.
>
> *(1007 characters)*

### 3. Exchange Trading Information

| Field | Value |
| :--- | :--- |
| **Exchange Name** | **Curve (Ethereum)** |
| **Exchange Trade URL** | **https://curve.finance/dex/ethereum/pools/0xe1b96555bbeca40e583bbb41a11c68ca4706a414** |

### 4. Block Explorer Links

| Field | Value |
| :--- | :--- |
| **Explorer Link** | **https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665** |

### 5. Contract Information

| Field | Value |
| :--- | :--- |
| **Blockchain Platform (1)** | **Ethereum** |
| **Contract Address (1)** | **0x98A878b1Cd98131B271883B390f68D2c90674665** |
| **Contract Decimal Places (1)** | **18** |

---

## Section 4: Step 2 — Supply Information

> ### ⚠️ REFRESH BEFORE SUBMISSION
> Supply values change as users mint/burn apxUSD. Before submitting, pull fresh numbers from:
> - **Total/Circulating Supply**: [Etherscan](https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665) (Check "Total Supply")
> - **Holder Count**: [Etherscan](https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665#balances)
> - **Price/Volume**: [GeckoTerminal](https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665)
>
> **Last known values (02/26/2026)**: Total Supply = 11,568,350 | Holders = 161 | Liquidity = $7.3M

### 6. Coin Holders & Distribution Schedule

| Field | Value |
| :--- | :--- |
| **Top Holder List URL** | **https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665#balances** |
| **Distribution Schedule** | *(leave blank — apxUSD is a stablecoin with no token distribution schedule; supply is created on-demand via collateral deposits)* |

### 7. Coin/Token Supply Information

| Field | Value |
| :--- | :--- |
| **Token Generation Date (TGE)** | **02/23/2026** |
| **Max Supply Amount** | *(Leave blank)* |
| **Is Infinite Supply** | **✅ Ticked** (apxUSD is a stablecoin minted on-demand) |

### 8. Total Supply

| Field | Value |
| :--- | :--- |
| **Total Supply Amount** | **11568350** (Refresh before submission) |
| **Total Supply API** | *(Leave blank — no REST endpoint currently available)* |
| **Burned Wallet** | *(Leave blank — no burn mechanism)* |

### 9. Circulating Supply

| Field | Value |
| :--- | :--- |
| **Circulating Supply Amount** | **11568350** (Same as Total Supply — all supply is circulating) |
| **Circulating Supply API** | *(Leave blank — no REST endpoint currently available)* |
| **Vested/Locked Wallet** | *(Leave blank — stablecoin has no vesting schedule)* |

### 10. Initial Token Allocation

*(Leave all allocation fields blank)* — apxUSD is a stablecoin with no initial token allocation. Supply is created on-demand when users deposit collateral.

### 11. Additional Supply Information

Enter this text:
> apxUSD is a collateral-backed stablecoin. The protocol mints tokens when users deposit collateral and burns tokens when users redeem. Supply has no fixed cap, and there is no team allocation, vesting schedule, or pre-mine. All issued supply is circulating. The largest holder, the apyUSD vault at 0x38EEb52F0771140d10c4E9a9a72349A329Fe8a6A, is a user-controlled ERC-4626 yield vault that receives voluntary apxUSD deposits.

---

## Section 5: Step 3 — Additional Information

### 12. Community Information

| Field | Value |
| :--- | :--- |
| **X/Twitter Profile Link** | **https://x.com/apyx_fi** |
| **Telegram Channel Link** | **https://t.me/apyx_announcements** |
| **Facebook Profile Link** | *(leave blank — no Facebook page)* |
| **YouTube Channel Link** | *(Leave blank)* |
| **Subreddit Link** | *(Leave blank)* |
| **Other Social Media Link** | *(Leave blank)* |
| **Discord Invitation URL** | **https://discord.com/invite/apyx-fi** |
| **Medium URL** | *(Leave blank)* |

### 13. Coin/Token Category

Select up to three categories. Provide the following reasons (each ≥250 characters):

**Category 1: Stablecoins**
> apxUSD is a US dollar stablecoin. The peg relies on over-collateralization with preferred equity issued by publicly listed Digital Asset Treasury companies. The protocol targets a stable $1.00 value and supports minting through collateral deposits plus redemption through the Apyx system on Ethereum. Collateral positions are valued as part of ongoing risk and NAV processes.
>
> *(375 characters)*

**Category 2: USD Stablecoin**
> apxUSD is denominated in US dollars and targets a 1:1 USD peg. It trades against USDC on Curve Finance. Peg support comes from protocol collateral management that holds preferred equity shares valued in USD terms. Live market data for price, volume, and liquidity is available on GeckoTerminal at https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665.
>
> *(381 characters)*

**Category 3: Decision Required**
apxUSD is backed by preferred equity (securities), not commodities. Choose the best fit from the dropdown:

- **Option A: Commodity-backed Stablecoin** (If no better fit exists)
    > apxUSD uses offchain financial collateral: preferred equity shares issued by publicly listed Digital Asset Treasury companies and traded on regulated exchanges. These instruments are securities rather than commodities, but they are externally verifiable assets with observable market pricing. The collateral portfolio spans multiple DAT issuers and is monitored with daily NAV calculations plus monthly third-party attestations.
    >
    > *(428 characters)*

- **Option B: Real World Assets (RWA)** (Recommended if available)
    > apxUSD is collateralized by real-world assets, specifically preferred equity shares issued by publicly listed Digital Asset Treasury (DAT) companies. The preferred shares trade on regulated stock exchanges, pay monthly cash dividends, and have public market pricing. Institutional custodians Anchorage Digital and BitGo hold collateral, and monthly attestation reports verify collateral status.
    >
    > *(394 characters)*

### 14. Developer Information

| Field | Value |
| :--- | :--- |
| **GitHub** | **https://github.com/apyx-labs** |
| **GitLab** | *(Leave blank)* |
| **Bitbucket** | *(Leave blank)* |

### 15. Attachments

**Token Image**: Upload the resized **200x200px** logo.

**Logo Resize Instructions**:
The original logo at [assets.apyx.fi/tokens/apxUSD.png](https://assets.apyx.fi/tokens/apxUSD.png) is 256x256px. CoinGecko requires 200x200px.
```bash
# Using ImageMagick
convert apxUSD.png -resize 200x200 apxUSD-200.png

# Using sips (macOS)
sips -z 200 200 apxUSD.png --out apxUSD-200.png
```

### 16. Additional Information — Remarks

Enter this text:
> Security: Quantstamp audited the apxUSD smart contracts (https://certificate.quantstamp.com/full/apx-usd-stablecoin/2a5be074-3d9f-49e7-aa08-46fb5f1e5bd6/index.html), and Certora completed formal verification.
>
> Team: The builders of Apyx are the team behind DeFi Development Corp. (Nasdaq: DFDV), a publicly listed Digital Asset Treasury company.
>
> Integrations: apxUSD integrates with Curve Finance for liquidity, Morpho for lending, and Pendle for yield trading. Anchorage Digital and BitGo provide custody. Gauntlet provides risk modeling.
>
> GeckoTerminal: https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665

---

## Section 6: Verification Process (MANDATORY)

CoinGecko requires public verification to prove you represent the project.

**Step 1**: Before submitting the form, post the following from the **@apyx_fi** account on X:
> Preparing to submit our @coaborator request to @coingecko for Apyx apxUSD! [TEAM CUSTOMIZES: Add any additional context if desired]
>
> 🔗 GeckoTerminal: https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665
>
> 📩 Telegram: @koed_the_kat

**Step 2**: Submit the form. You will receive a **Request ID** (e.g., CL1234567890) via email.

**Step 3**: Reply to your own verification post with the Request ID:
> 🎫 Request ID: CLxxxxxxxxxx

**Reference**: [CoinGecko Verification Guide](https://support.coingecko.com/hc/en-us/articles/23725417857817-Verification-Guide-for-Listing-Update-Requests-on-CoinGecko)

---

## Section 7: Fast Pass (Optional)

CoinGecko offers an expedited review service called **Fast Pass**.

| Feature | Standard (Free) | Fast Pass |
| :--- | :--- | :--- |
| **Cost** | $0 | $1,000 |
| **Timeline** | ~2 weeks | 24 hours |
| **Guarantee** | No | No (Faster review only, not guaranteed approval) |

- Fast Pass is offered **after** you submit the form.
- Payment is non-refundable.
- Reference: [What is Fast Pass?](https://support.coingecko.com/hc/en-us/articles/37298264234649)

---

## Section 8: Post-Submission Monitoring

- **Check Status**: Monitor your submission at [coingecko.com/request-form/submissions](https://www.coingecko.com/request-form/submissions?locale=en).
- **Action Needed**: If the status changes to "Action Needed", you have **3 CALENDAR DAYS** to respond. Failure to respond will result in auto-rejection.
- **Response**: Reply directly through the CoinGecko portal. Be detailed and accurate.
- **Rejection**: If rejected, do not resubmit immediately. Wait 2 weeks, address the issues, and submit a new request.

---

## Section 9: Reference Links

| Resource | URL |
| :--- | :--- |
| **Listing Form** | [https://www.coingecko.com/request-form?locale=en](https://www.coingecko.com/request-form?locale=en) |
| **Asset Naming Policy** | [https://support.coingecko.com/hc/en-us/articles/33608537461913](https://support.coingecko.com/hc/en-us/articles/33608537461913) |
| **Verification Guide** | [https://support.coingecko.com/hc/en-us/articles/23725417857817](https://support.coingecko.com/hc/en-us/articles/23725417857817) |
| **Fast Pass FAQ** | [https://support.coingecko.com/hc/en-us/articles/37297414892697](https://support.coingecko.com/hc/en-us/articles/37297414892697) |
| **GeckoTerminal** | [https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665](https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665) |
| **Etherscan** | [https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665](https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665) |
| **Quantstamp Audit** | [https://certificate.quantstamp.com/full/apx-usd-stablecoin/2a5be074-3d9f-49e7-aa08-46fb5f1e5bd6/index.html](https://certificate.quantstamp.com/full/apx-usd-stablecoin/2a5be074-3d9f-49e7-aa08-46fb5f1e5bd6/index.html) |

