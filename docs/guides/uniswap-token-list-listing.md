# Uniswap Default Token List — apxUSD & apyUSD Listing Guide

## Overview & Current Status

The Uniswap Default Token List is the curated list of tokens that appear by default in the Uniswap interface. Being on this list significantly improves token discoverability for users.

**Current Status**: Issue #2340 filed on February 22, 2026, requesting both apxUSD and apyUSD. The issue is currently **open** and awaiting review by the Uniswap team.

**CoinGecko Status Update**:
- ✅ **apxUSD**: Listed on CoinGecko (live since March 2026)
- ⏳ **apyUSD**: CoinGecko listing pending

---

## How the Uniswap Token List Works

### The Process
1. **File an issue** on the `Uniswap/default-token-list` repository — this is the ONLY public action available to external contributors
2. **Uniswap team internally reviews** the request
3. **Uniswap team creates and merges a PR** if approved — only team members can merge
4. **Tokens are published** to NPM as `@uniswap/default-token-list`

### Key Facts
- **Only these team members merge PRs**: `robert-seitz-uniswap`, `matteenm`, `0sh3`, `dgilmanuni`
- **1,300+ open issues** — no guaranteed review timeline
- **Tokens are added to**: `src/tokens/ethereum.json` in the repo
- **Repository**: https://github.com/Uniswap/default-token-list

**Important**: Filing an issue does NOT guarantee addition to the list. The Uniswap team has sole discretion over which tokens are included.

---

## Issue Details (Issue #2340)

| Field | Value |
|-------|-------|
| **Issue** | https://github.com/Uniswap/default-token-list/issues/2340 |
| **Filed by** | dead-pool-aka-wilson |
| **Date** | February 22, 2026 |
| **Status** | Open — awaiting review |

### Tokens Requested

| Field | apxUSD | apyUSD |
|-------|--------|--------|
| **Address** | `0x98A878b1Cd98131B271883B390f68D2c90674665` | `0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A` |
| **Name** | apxUSD | apyUSD |
| **Symbol** | apxUSD | apyUSD |
| **Decimals** | 18 | 18 |
| **Homepage** | https://apyx.fi | https://apyx.fi |
| **CoinGecko** | https://www.coingecko.com/en/coins/apxusd | [PENDING] |

### Token Descriptions

**apxUSD**: Apyx's synthetic dollar backed by a diversified basket of low-volatility, variable-rate, preferred shares issued by Digital Asset Treasuries (DATs).

**apyUSD**: An ERC-4626 yield-bearing vault token. Users deposit apxUSD to receive apyUSD, which accrues value from the dividend income of the underlying DAT preferred shares.

---

## What Strengthens a Listing Request

The following factors improve the likelihood of inclusion:

### ✅ Already Achieved
- **CoinGecko Listing**: apxUSD is now listed on CoinGecko
- **Smart Contract Audits**: Quantstamp audit completed, Certora formal verification done
- **DeFi Integrations**: Active liquidity on Curve Finance, lending markets on Morpho, yield trading on Pendle
- **Regulatory Compliance**: Partnership with institutional custodians (Anchorage Digital, BitGo)

### ⏳ In Progress
- **apyUSD CoinGecko Listing**: Pending submission
- **CoinMarketCap Listing**: Both tokens pending
- **Trading Volume Growth**: Organic adoption increasing

### Additional Credibility Markers
- Active community on X/Twitter and Discord
- Monthly accounting attestation reports
- Transparent collateral backing via public DAT filings

---

## Follow-Up Strategy

### Completed ✅
- [x] Initial issue filed (Feb 22, 2026)
- [x] CoinGecko link added via comment update

### Pending ⏳
- [ ] Monitor issue for Uniswap team response
- [ ] When apyUSD gets CoinGecko listing → add another comment
- [ ] If CoinMarketCap listing happens → add another comment
- [ ] Check issue status monthly (no spam)

### Do NOT ❌
- Do NOT tag Uniswap team members
- Do NOT post "when listing?" comments
- Do NOT spam or bump the issue
- Do NOT create duplicate issues

**Note**: The original issue stated "Not yet listed on CoinGecko or CoinMarketCap" — this has been updated with a comment noting that apxUSD is now listed on CoinGecko.

---

## Reference Links

| Resource | URL |
|----------|-----|
| **Issue #2340** | https://github.com/Uniswap/default-token-list/issues/2340 |
| **Uniswap Token List Repo** | https://github.com/Uniswap/default-token-list |
| **CoinGecko apxUSD** | https://www.coingecko.com/en/coins/apxusd |
| **GeckoTerminal apxUSD** | https://www.geckoterminal.com/eth/tokens/0x98A878b1Cd98131B271883B390f68D2c90674665 |
| **apxUSD Etherscan** | https://etherscan.io/token/0x98A878b1Cd98131B271883B390f68D2c90674665 |
| **apyUSD Etherscan** | https://etherscan.io/token/0x38EEb52F0771140d10c4E9A9a72349A329Fe8a6A |
| **Quantstamp Audit** | https://certificate.quantstamp.com/full/apx-usd-stablecoin/2a5be074-3d9f-49e7-aa08-46fb5f1e5bd6/index.html |
| **Curve Pool** | https://curve.finance/dex/ethereum/pools/0xe1b96555bbeca40e583bbb41a11c68ca4706a414 |
| **Apyx Website** | https://apyx.fi |
| **X/Twitter** | https://x.com/apyx_fi |
| **Documentation** | https://docs.apyx.fi |
| **Discord** | https://discord.com/invite/apyx-fi |

---

## Summary

The Uniswap default token list request for apxUSD and apyUSD has been filed and is awaiting review. With apxUSD now listed on CoinGecko and strong fundamentals (audits, integrations, institutional custody), the listing request is well-positioned. The recommended approach is patience — check monthly, add updates when new milestones are achieved (apyUSD CoinGecko, CoinMarketCap), and avoid any behavior that could be perceived as spam.
