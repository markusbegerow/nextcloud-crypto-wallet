# Crypto Wallet for Nextcloud

> Secure storage of cryptocurrency addresses and private keys - inside your own Nextcloud.

**Crypto Wallet** lets you manage multiple wallets and cryptocurrency addresses directly inside Nextcloud. Private keys are encrypted client-side with AES-256-GCM before being stored, so only you can access them. Live price data, password-strength feedback, and per-wallet locking are included out of the box.

---

## Features

- **AES-256-GCM encryption** - private keys are encrypted with your wallet password before storage; the server never sees them in plain text
- **Multiple wallets** - each independently locked with its own password
- **51 supported cryptocurrencies** - searchable combobox covering BTC, ETH, SOL, DOGE, LUNC and 46 more
- **Live price display** - current USD price and 24 h change fetched via CoinGecko
- **Amount tracking** - record how many coins you hold at each address; stored per-address in the database
- **Portfolio total** - wallet header shows the live total USD value of all addresses combined
- **Hide / Show amounts** - one-click toggle masks all balance figures with `•••••` for privacy; state persists across page refreshes
- **Coin badge** - the colored circle next to each address shows the ticker abbreviation (BTC, ETH, MATIC…)
- **Inline copy icon** - small clipboard icon sits directly next to the public address for quick one-click copying
- **Reveal private key** - password-protected reveal with a 30-second auto-close timer
- **Password strength indicator** - real-time visual feedback when creating or changing wallet passwords
- **Per-wallet lock/unlock** - unlock wallets on demand; re-lock with one click
- **Languages** - English 🇬🇧 · German 🇩🇪

---

## Requirements

| Dependency | Version |
|---|---|
| Nextcloud | 25 – 33 |
| PHP | 8.0+ |

---

## Installation

### From source (manual)

1. Clone or download this repository into your Nextcloud `custom_apps/` directory:
   ```bash
   cd /path/to/nextcloud/custom_apps
   git clone https://github.com/markusbegerow/nextcloud-crypto-wallet crypto-wallet
   ```
2. Enable the app:
   ```bash
   php occ app:enable crypto-wallet
   ```
3. Open the **Wallet** entry in the Nextcloud top navigation bar.

---

## Usage

1. Click **+ New Wallet** in the sidebar and choose a name and a strong password.
2. Select the wallet and click **+ Add Address**.
3. Type in the **cryptocurrency search box** to find and select a coin (51 available), enter the public address, and optionally enter a private key (requires the wallet password to encrypt it).
4. Optionally enter an **Amount** to track how many coins you hold at that address - the card will display the current USD value and the wallet header shows a portfolio total.
5. Use the **Reveal Key** button (password required) to view a stored private key - it disappears automatically after 30 seconds.
6. Use the **Hide Amounts** button to mask all balance figures for privacy; click **Show Amounts** to reveal them again.
7. Lock the wallet with the **Lock** button to require re-entry of the password before viewing private keys again.

---

## Security

- Private keys are encrypted with AES-256-GCM using the wallet password **before** being sent to the server. The server stores only the ciphertext.
- Wallet passwords are never stored - they are held in browser memory for the duration of the session only.
- This is a **self-hosted** app: your keys never leave your own Nextcloud instance.

> ⚠️ **Important:** If you forget your wallet password, there is no recovery option. Keep a secure backup of your private keys.

---

## License

[GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html) © [Markus Begerow](https://markus-begerow.de/linktree)

---

## 🙋‍♂️ Get Involved

If you encounter any issues or have questions:
- 🐛 [Report bugs](https://github.com/markusbegerow/nextcloud-crypto-wallet/issues)
- 💡 [Request features](https://github.com/markusbegerow/nextcloud-crypto-wallet/issues)
- ⭐ Star the repo if you find it useful!

## ☕ Support the Project

If you like this project, support further development with a repost or coffee:

<a href="https://www.linkedin.com/sharing/share-offsite/?url=https://github.com/MarkusBegerow/nextcloud-crypto-wallet" target="_blank"> <img src="https://img.shields.io/badge/💼-Share%20on%20LinkedIn-blue" /> </a>

[![Buy Me a Coffee](https://img.shields.io/badge/☕-Buy%20me%20a%20coffee-yellow)](https://paypal.me/MarkusBegerow)

## 📬 Contact

- 🧑‍💻 [Markus Begerow](https://linkedin.com/in/markusbegerow)
- 💾 [GitHub](https://github.com/markusbegerow)
- ✉️ [Twitter](https://x.com/markusbegerow)

