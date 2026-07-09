# Coinductor Paper Wallet — TRON Cold Wallet Generator (Secure & Offline)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![CodeQL](https://img.shields.io/badge/CodeQL-enabled-blue?logo=githubactions&logoColor=white)](https://github.com/vlasenkofedor/tron-paper-wallet/actions/workflows/codeql.yml)
[![Downloads](https://img.shields.io/github/downloads/vlasenkofedor/tron-paper-wallet/total?label=Downloads&color=brightgreen&logo=github)](https://github.com/vlasenkofedor/tron-paper-wallet/releases)
[![No Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen?logo=html5)](coinductor-paper.html)
[![Works Offline](https://img.shields.io/badge/works-offline-blue?logo=cloudflare)](coinductor-paper.html)
[![Single File](https://img.shields.io/badge/single-HTML%20file-orange?logo=html5)](coinductor-paper.html)
[![TRON Network](https://img.shields.io/badge/TRON-TRX%20%2F%20USDT%20TRC--20-red)](coinductor-paper.html)

**Coinductor Paper Wallet** is a professional, 100% client-side, self-contained single-page HTML application designed to generate secure, air-gapped **TRON cold wallets** offline. This generator allows users to create a physical paper backup for **TRX**, **USDT (TRC-20)**, and other TRON network assets, ensuring maximum protection against online hacks, malware, and remote attacks.

---

## 💾 Download & Use Offline

<a href="coinductor-paper.html" download="coinductor-paper.html">
  <img src="https://img.shields.io/badge/⬇ Download-coinductor--paper.html-brightgreen?style=for-the-badge" alt="Download coinductor-paper.html"/>
</a>

To use the generator offline (highly recommended):
1. Click the **Download** button above to save `coinductor-paper.html` to your device.
2. Transfer the file to a clean, offline/air-gapped computer (via USB drive).
3. Open the file in any browser to securely generate your TRON wallet key pair.

---

## 🛡️ Security Features & Audit Integrity

* **Cryptographically Secure Entropy:** Generates private keys using the browser's standard native Cryptographically Secure Pseudo-Random Number Generator (CSPRNG) via `window.crypto.getRandomValues`.
* **Zero External Dependencies:** Built entirely inside a single standalone HTML file (`coinductor-paper.html`). It does not load CDNs, external scripts, Google Fonts, tracking pixels, or execute any network calls.
* **secp256k1 Range Validation:** Explicitly validates that derived private keys fall strictly within the mathematically valid secp256k1 boundary range $[1, N-1]$, complying with SECG and NIST SP 800-56A specifications.
* **Local Session Memory Overwrite:** Includes a "Clear Session" feature that overwrites generated variables and clears HTML5 Canvas buffers to scrub keys from browser memory.
* **Printout Layout Protection (Bi-Fold):** The print sheet features a foldable layout. The top half contains the public deposit address, and the bottom half contains the private key which folds back and seals to hide the secret key.

---

## 💾 File Integrity Verification (SHA-256)

To guarantee that the file has not been altered or compromised, verify the SHA-256 hash sum before running it on an offline device.

* **File name:** `coinductor-paper.html`
* **Expected SHA-256 Hash:**
  ```text
  4edd7ce77a5bf9c8ca34e82a0aafcc9766511b3f61b9bff67b53f8b69205cd9b
  ```

### How to verify the hash sum on your operating system:

#### 🍏 macOS & iOS
Open **Terminal** (on macOS) or run a shell command in the **Shortcuts** app (on iOS) and execute:
```bash
shasum -a 256 coinductor-paper.html
```

#### 🐧 Linux
Open your terminal and run:
```bash
sha256sum coinductor-paper.html
```

#### 🪟 Windows
Open **PowerShell** and run:
```powershell
Get-FileHash coinductor-paper.html -Algorithm SHA256
```
Or open **Command Prompt (CMD)** and run:
```cmd
certutil -hashfile coinductor-paper.html SHA256
```

---

## ⚖️ License
MIT © [coinductor.io](https://coinductor.io)
