# DeBank Listing Guide for Apyx Protocol

This guide provides a comprehensive workflow for requesting the listing of the **Apyx protocol** and its associated tokens (**apxUSD** and **apyUSD**) on DeBank. Unlike other platforms, DeBank does not have a public submission form; instead, it relies on direct email outreach and internal protocol adapter development.

## Section 1: Overview & Purpose

The goal of this outreach is to ensure that:
1. **apxUSD** and **apyUSD** tokens are correctly identified and priced in user portfolios.
2. The **Apyx protocol** is tracked as a distinct entity, showing Total Value Locked (TVL) and user positions.
3. The protocol's yield-bearing mechanism (apyUSD vault) is accurately represented.

DeBank is a critical infrastructure provider for DeFi users, and having a native protocol adapter ensures that Apyx users can track their positions, yield, and collateral status directly within the DeBank interface.

---

## Section 2: Prerequisites & Pre-Send Checklist

Before sending the outreach email, ensure all protocol information is up-to-date and verifiable.

> ### ⚠️ REFRESH BEFORE SUBMISSION
> DeBank's internal review team will verify live onchain data. Ensure the following values are accurate at the time of sending:
> - **apxUSD Total Supply**: [Etherscan](https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665)
> - **apyUSD Vault Balance**: [Etherscan](https://etherscan.io/token/0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A)
> - **Current TVL**: [TEAM FILLS IN: Total USD value of collateral]
> - **Liquidity (Curve)**: [Curve Pool](https://curve.finance/dex/ethereum/pools/0xe1b96555bbeca40e583bbb41a11c68ca4706a414)

### Pre-Send Checklist
- [ ] **Token Metadata**: Verify that `info.json` for both tokens is correctly merged into the Trust Wallet Assets repository.
- [ ] **Logo Availability**: Confirm that high-resolution logos are accessible at the provided URLs.
- [ ] **Documentation**: Ensure the protocol documentation (https://docs.apyx.fi) clearly explains the relationship between apxUSD and apyUSD.
- [ ] **Audit Reports**: Have the Quantstamp audit link ready for inclusion.
- [ ] **Social Verification**: Ensure the official @apyx_fi X account is active and has posted about the protocol launch.

---

## Section 3: Token Metadata

Provide DeBank with the following metadata for both tokens to ensure they are correctly indexed.

### apxUSD (Base Dollar Token)

| Field | Value |
| :--- | :--- |
| **Token Name** | **Apyx apxUSD** |
| **Token Symbol** | **apxUSD** |
| **Contract Address** | **0x98A878b1Cd98131B271883B390f68D2c90674665** |
| **Blockchain** | **Ethereum** |
| **Decimals** | **18** |
| **Token Type** | **ERC-20** |
| **Logo URL** | **https://assets.apyx.fi/tokens/apxUSD.png** |
| **Explorer Link** | **https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665** |

### apyUSD (Yield-Bearing Vault Token)

| Field | Value |
| :--- | :--- |
| **Token Name** | **Apyx apyUSD** |
| **Token Symbol** | **apyUSD** |
| **Contract Address** | **0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A** |
| **Blockchain** | **Ethereum** |
| **Decimals** | **18** |
| **Token Type** | **ERC-20 (ERC-4626 Vault)** |
| **Logo URL** | **https://assets.apyx.fi/tokens/apyUSD.png** |
| **Explorer Link** | **https://etherscan.io/token/0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A** |

---

## Section 4: Protocol Architecture & TVL

DeBank needs to understand the protocol's structure to build an accurate adapter.

### Core Contracts Table

| Contract Name | Address | Role | Relevance to TVL |
| :--- | :--- | :--- | :--- |
| **apxUSD Token** | `0x98A878b1Cd98131B271883B390f68D2c90674665` | Base stablecoin | Represents circulating supply |
| **apyUSD Vault** | `0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A` | ERC-4626 Yield Vault | Holds apxUSD deposits |
| **[TEAM FILLS IN]** | `[TEAM FILLS IN]` | Collateral Manager | Manages DAT preferred shares |
| **[TEAM FILLS IN]** | `[TEAM FILLS IN]` | Oracle/NAV Provider | Provides collateral valuation |

### TVL Methodology Options

DeBank typically writes their own adapters. We recommend presenting the following three options for their team to choose from:

**Option (a): Total apxUSD Supply (Simplified)**
- **Formula**: `Total apxUSD Supply × $1.00`
- **Approach**: Assumes every apxUSD in circulation is backed by at least $1.00 of collateral. This is the simplest to implement but may undercount the total value if the protocol is over-collateralized.

**Option (b): Vault-Only Deposits (Conservative)**
- **Formula**: `apxUSD Balance of apyUSD Vault × $1.00`
- **Approach**: Only counts the apxUSD currently deposited in the yield-bearing vault. This represents the "active" yield-generating TVL but ignores apxUSD held in wallets or other DeFi protocols.

**Option (c): Total Collateral Value (Preferred)**
- **Formula**: `[TEAM FILLS IN: Sum of (DAT Preferred Share Balance × Market Price)]`
- **Approach**: Directly tracks the value of the underlying collateral (preferred shares) held by the protocol. This is the most accurate representation of the protocol's backing and total value.
- **Implementation Note**: Requires DeBank to track offchain/regulated exchange pricing for DAT preferred shares or use the protocol's onchain NAV oracle.

**Recommended Approach**: [TEAM FILLS IN: e.g., Option (c) is preferred for accuracy, with Option (a) as a fallback.]

---

## Section 5: Email Template

Use the following template for the initial outreach.

**To**: hello.cloud@debank.com
**Subject**: Protocol Integration Request: Apyx (apxUSD & apyUSD) — Ethereum

**Body**:

> Hello DeBank Team,
>
> We are writing to request the integration of the **Apyx protocol** and its associated tokens (**apxUSD** and **apyUSD**) on Ethereum.
>
> **About Apyx**
> Apyx is a stablecoin protocol that uses preferred equity from Digital Asset Treasuries (DATs) as collateral for dollar tokens. DATs are publicly listed companies that hold digital assets on their balance sheets and issue preferred shares with monthly cash dividends. The protocol acquires those preferred shares, keeps them as collateral, and routes the dividend cash flow to onchain users as yield.
>
> The system uses two tokens:
> 1. **apxUSD** (0x98A878b1Cd98131B271883B390f68D2c90674665): The base dollar token, backed by more than 100% collateral in DAT preferred shares.
> 2. **apyUSD** (0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A): An ERC-4626 vault token. Users deposit apxUSD to mint apyUSD, and the vault distributes dividend income over time so the apyUSD to apxUSD exchange rate rises.
>
> *(806 characters)*
>
> **Institutional Credibility & Security**
> - **Team**: Built by the team behind DeFi Development Corp. (Nasdaq: DFDV).
> - **Custody**: Anchorage Digital and BitGo act as primary custodians for the preferred-share collateral.
> - **Audit**: Quantstamp audited the smart contracts, and Certora performed formal verification.
> - **Integrations**: Live integrations with Curve, Morpho, and Pendle.
>
> *(336 characters)*
>
> **Integration Details**
> - **Blockchain**: Ethereum
> - **apxUSD Contract**: 0x98A878b1Cd98131B271883B390f68D2c90674665
> - **apyUSD Contract**: 0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A
> - **TVL Methodology**: We recommend tracking the total collateral value (preferred share NAV) or the total apxUSD supply.
>
> *(288 characters)*
>
> **Resources**
> - **Website**: https://apyx.fi
> - **Documentation**: https://docs.apyx.fi
> - **GitHub**: https://github.com/apyx-labs
> - **Audit Report**: [TEAM FILLS IN: Link to Quantstamp audit]
>
> We are available to provide any additional technical information or documentation required to build the protocol adapter.
>
> Best regards,
>
> [TEAM FILLS IN: Name]
> [TEAM FILLS IN: Role]
> Apyx Finance

---

## Section 6: Attachments & Supporting Materials

When sending the email, attach or link to the following materials to expedite the review process.

### Mandatory Attachments
- **Token Logos**: Attach `apxUSD.png` and `apyUSD.png` (256x256px or higher, transparent background).
- **Audit Report**: Attach the full PDF of the Quantstamp audit report.

### Supporting Links
- **CoinGecko Page**: [TEAM ACTION: Add link once apxUSD is listed on CoinGecko]
- **GeckoTerminal**: https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665
- **Etherscan (apxUSD)**: https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665
- **Etherscan (apyUSD)**: https://etherscan.io/token/0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A

---

## Section 7: Sending & Contact Details

Ensure the email is sent from an official `@apyx.fi` or `@dfdv.com` email address to establish authority.

| Channel | Contact Info | Purpose |
| :--- | :--- | :--- |
| **Primary Email** | **hello.cloud@debank.com** | Initial submission and technical details |
| **Secondary Email** | **business@debank.com** | Business development and partnership inquiries |
| **Telegram (Backup)** | **@chuck_2140** | Urgent follow-ups or technical clarification |
| **Twitter (DM)** | **@DeBankDeFi** | General inquiries (low response rate) |

---

## Section 8: Follow-Up Timeline & Escalation

DeBank receives a high volume of requests. Follow this timeline to ensure the request remains active.

### Follow-Up Timeline

| Milestone | Action | Channel |
| :--- | :--- | :--- |
| **Day 0** | Send initial outreach email | Email (hello.cloud@debank.com) |
| **Day 7** | First follow-up (reply to original thread) | Email |
| **Day 14** | Second follow-up + Telegram outreach | Email + Telegram (@chuck_2140) |
| **Day 21** | Public mention/tag on Twitter | Twitter (@DeBankDeFi) |

### Common Questions DeBank Might Ask (FAQ)

**Q: How is the yield for apyUSD generated?**
> A: Yield is sourced from monthly cash dividends paid by preferred shares issued by publicly traded Digital Asset Treasury (DAT) companies. The protocol acquires these shares and routes the dividend income to the apyUSD vault.

**Q: Is the collateral verifiable onchain?**
> A: The collateral (preferred shares) is held offchain by institutional custodians (Anchorage/BitGo). However, the protocol publishes monthly accounting attestation reports and uses an onchain NAV oracle to reflect the collateral value.

**Q: What happens if the collateral value drops?**
> A: The protocol maintains over-collateralization and includes risk controls such as daily NAV calculations and automatic rebalancing. Gauntlet provides ongoing risk modeling for the system.

**Q: Are there any other tokens in the ecosystem?**
> A: Currently, only apxUSD and apyUSD are live. A governance token (APYX) is planned for the future but is not yet active.

---

## Section 9: Reference Links

| Resource | URL |
| :--- | :--- |
| **Official Website** | **https://apyx.fi** |
| **Protocol Documentation** | **https://docs.apyx.fi** |
| **apxUSD Etherscan** | **https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665** |
| **apyUSD Etherscan** | **https://etherscan.io/token/0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A** |
| **Curve Finance Pool** | **https://curve.finance/dex/ethereum/pools/0xe1b96555bbeca40e583bbb41a11c68ca4706a414** |
| **GeckoTerminal (apxUSD)** | **https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665** |
| **Quantstamp Audit** | **https://certificate.quantstamp.com/full/apx-usd-stablecoin/2a5be074-3d9f-49e7-aa08-46fb5f1e5bd6/index.html** |
| **GitHub Repository** | **https://github.com/apyx-labs** |
| **Official X (Twitter)** | **https://x.com/apyx_fi** |
| **Telegram Announcements** | **https://t.me/apyx_announcements** |
| **Discord Community** | **https://discord.com/invite/apyx-fi** |
| **DeBank Official Twitter** | **https://twitter.com/DeBankDeFi** |
