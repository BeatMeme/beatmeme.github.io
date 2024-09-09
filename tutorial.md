---
layout: page
title: Tutorial
description: Step-by-step guide on how to get $BEAT tokens, including wallet setup and token claiming.
permalink: /tutorial/
---

# How to Get $BEAT Tokens

Follow this simple guide to set up your wallet and get your $BEAT tokens.

## 1. Add Arthera Network to Your Wallet

First, you will need to add the Arthera network to your Web3 wallet (MetaMask, Trust Wallet, etc.)

### Automatic Method
- Click the button below to automatically add Arthera network:
<button onclick="addArtheraNetwork()" class="btn">Add Arthera Network</button>

### Chainlist Method
- Visit [Chainlist.org/chain/10242](https://chainlist.org/chain/10242)
- Connect your wallet
- Click "Add to Wallet" to add Arthera network

### Manual Method
Add these network details to your wallet:
- **Network Name**: Arthera Mainnet
- **RPC URL**: https://rpc.arthera.net
- **Chain ID**: 10242
- **Currency Symbol**: AA
- **Block Explorer**: https://explorer.arthera.net

## 2. Add $BEAT Token to Your Wallet

### Automatic Method
- Click the button below to add $BEAT token:
<button onclick="addBeatToken()" class="btn">Add $BEAT Token</button>

### Manual Method
Add these token details to your wallet:
- **Token Address**: 0xBEa7d44bb5627533a54DFD3ca131FD7E323d1f29
- **Token Symbol**: BEAT
- **Decimals**: 18

## 3. Get an Arthera Gas Pass

To receive $BEAT tokens, you need an Arthera Gas Pass:

1. Visit the [Arthera Gas Pass Faucet](https://faucet.arthera.net)
2. Enter your wallet address
3. Submit the form to receive your free Gas Pass
4. Your Gas Pass ID determines your $BEAT allocation:
   - ID 0 receives 1,000,000 $BEAT
   - ID 1 receives 999,999 $BEAT
   - Each subsequent ID receives 1 less $BEAT
   - Last ID (999,999) receives 1 $BEAT

## 4. Claim Your Tokens

Once you have an Arthera Gas Pass:

1. Your tokens will automatically appear in your wallet (no manual claiming required)
2. You can verify your balance by checking your wallet after adding the $BEAT token

## 5. Use $BEAT on Arthera

Here are the current places where you can use your $BEAT tokens:

- **Elk Finance**: Trade and farm $BEAT tokens
  - [Visit Elk Finance DEX](https://app.elk.finance)
  - Liquidity pairs available: $ELK-$BEAT
  - [Add $ELK-$BEAT liquidity](https://app.elk.finance/add/v2/0xeEeEEb57642040bE42185f49C52F7E9B38f8eeeE/0xBEa7d44bb5627533a54DFD3ca131FD7E323d1f29) to earn trading fees
  - [Farm liquidity pair](https://app.elk.finance/faas/manage/0x884832028ccbCc28bD7186057Fe23aCE0850B8d5/v2) to earn more $BEAT and $ELK
  - [Trade $BEAT](https://app.elk.finance/swap/10242/ELK/BEAT)

- **Third Trade**: Trade and farm $BEAT tokens
  - [Visit Third Trade DEX](https://third.trade)
  - Liquidity pairs available: $XPAA-$BEAT, $USDC.e-$BEAT
  - [Add $XPAA-$BEAT liquidity](https://third.trade/pool/0xab27fcb30d2aae4deb7841a07b6ba7bb4aaedf4e/new-position) to earn trading fees
  - [Add $USDC.e-$BEAT liquidity](https://third.trade/pool/0x6dbfd6b2e83dc4a30f567591b8ce173f516b3413/new-position) to earn trading fees
  - [Farm liquidity pair](#) not yet available
  - [Trade $BEAT](https://third.trade/swap/Arthera?buy=0xBEa7d44bb5627533a54DFD3ca131FD7E323d1f29)

- **Community Events**:
  - Join our [Telegram group](https://t.me/BeatTokenCommunity) to engage with our community
  - Follow us on [X](https://x.com/BeatCryptoToken) for $BEAT updates
  - Participate in community contests

## 6. Optional: Repeat for Other Wallets

Want to maximize your $BEAT holdings? You can:

1. Create additional Web3 wallets
2. Repeat steps 3-4 for each wallet
3. Each wallet can receive tokens based on its Gas Pass ID
4. It works with different wallet types:
   - MetaMask
   - Trust Wallet
   - WalletConnect compatible wallets

## Important Notes

- Arthera offers free Gas Passes for three months
- Each Gas Pass entitles you to $BEAT tokens
- Tokens are distributed on a first-come, first-served basis
- The earlier your Gas Pass ID, the more tokens you receive
- $BEAT is an experimental community token with no intrinsic value or expectation of financial return
- There is no formal team or roadmap

<script>
async function addArtheraNetwork() {
    try {
        await window.ethereum.request({
            method: 'wallet_addEthereumChain',
            params: [{
                chainId: '0x2802',
                chainName: 'Arthera Mainnet',
                nativeCurrency: {
                    name: 'AA',
                    symbol: 'AA',
                    decimals: 18
                },
                rpcUrls: ['https://rpc.arthera.net'],
                blockExplorerUrls: ['https://explorer.arthera.net']
            }]
        });
    } catch (error) {
        console.error(error);
        alert('Failed to add network. Please add manually.');
    }
}

async function addBeatToken() {
    try {
        await window.ethereum.request({
            method: 'wallet_watchAsset',
            params: {
                type: 'ERC20',
                options: {
                    address: '0xBEa7d44bb5627533a54DFD3ca131FD7E323d1f29',
                    symbol: 'BEAT',
                    decimals: 18
                },
            },
        });
    } catch (error) {
        console.error(error);
        alert('Failed to add token. Please add manually.');
    }
}
</script>