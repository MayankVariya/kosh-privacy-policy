# Privacy Policy for Kosh: Personal Financial Vault

**Effective Date:** October 3, 2026  
**Last Updated:** October 3, 2026  
**Application Name:** Kosh: Personal Financial Vault  
**Developer Contact:** support@kosh.app  

---

## 1. Introduction & Core Philosophy
Kosh ("we", "our", or "the app") is designed from the ground up as an **offline-first, sovereign personal financial vault**. We believe your financial data is strictly private and belongs solely to you. 

Unlike traditional financial management applications, **Kosh operates without centralized servers, remote databases, or mandatory user accounts.** Your financial ledger, accounts, balances, transactions, and categories reside 100% locally on your device.

---

## 2. Information We Do NOT Collect
We do not collect, harvest, sell, rent, or monetize your personal or financial data:
- **No Financial Data Collection:** We do not collect your transaction amounts, notes, bank names, account numbers, income, expenses, or investment portfolios.
- **No Personal Identity Tracking:** We do not collect your name, phone number, address, or government identifiers.
- **No Advertising or Tracking SDKs:** Kosh contains **zero third-party advertising SDKs** (e.g. Google AdMob, Meta Ads) and **zero user tracking/telemetry frameworks** (e.g. Firebase Analytics, AppsFlyer, Mixpanel).
- **No Contact Access or Location Data:** Kosh does not request or access your device location, address book, microphone, or camera.
- **No SMS or Banking Scraping:** Kosh does not read your SMS messages or banking notifications.

---

## 3. Data Stored Locally On Your Device
All financial records entered into Kosh are stored in an encrypted/private SQLite database in your device's isolated application sandbox:
- Account names, types (Bank, Cash, Investment), and current balances
- Transaction history (dates, amounts, categories, self/family tags, notes)
- Custom user-created spending categories and frozen fund commitments
- User preferences (theme settings, biometric lock toggles)

This data is never transmitted to the developer or any unauthorized third party.

---

## 4. Biometric Authentication & Security
Kosh offers an optional biometric lock (Fingerprint, Face Recognition, or Device PIN):
- Biometric verification is performed locally by your device’s operating system using the official Android Biometric API (`androidx.biometric`).
- **Kosh never has access to your raw biometric data, fingerprint scans, or facial templates.** All biometric processing stays securely inside your device's hardware security enclave (Trusted Execution Environment / TEE).
- The app only receives a cryptographic success or failure signal from the operating system to unlock the vault.

---

## 5. Optional Google Drive & Sheets Backup (User-Initiated)
Kosh provides an optional backup feature allowing users to sync their transaction ledger to a personal Google Spreadsheet:
- **Direct Device-to-Google Communication:** When enabled, Kosh uses the official Google Sign-In SDK and Google Drive/Sheets REST APIs to communicate directly from your device to your personal Google account via secure HTTPS.
- **Developer Has No Access:** The developer does not maintain intermediary proxy servers, databases, or logging mechanisms. We never see, store, or receive your Google OAuth access tokens, Google credentials, or spreadsheet data.
- **Limited Scope:** Kosh only requests access to the specific spreadsheets created by the app (`https://www.googleapis.com/auth/drive.file` and `https://www.googleapis.com/auth/spreadsheets`).
- **Complete Control:** You can disconnect Google Sign-In or revoke Kosh's permissions at any time via the in-app Settings or through your Google Account Security Settings at `https://myaccount.google.com/permissions`.

---

## 6. Device Permissions Used
Kosh requests only the minimum permissions necessary for its functionality:

| Permission | Technical Name | Purpose |
|---|---|---|
| **Internet Access** | `android.permission.INTERNET` | Used solely for the optional, user-initiated Google Sheets backup and export features. |
| **Biometric Authentication** | `android.permission.USE_BIOMETRIC`, `USE_FINGERPRINT` | Used to protect app launch with your device's fingerprint or biometric lock. |

---

## 7. Data Retention & Your Right to Complete Deletion
Because your data is stored exclusively on your device, **you retain 100% sovereignty over your data at all times**:
- **In-App Data Purge:** You can instantly erase your entire transaction ledger by navigating to **Settings → Danger Zone → Clear All Transactions**.
- **Complete App Data Wipe:** Clearing application data in Android Settings (`Settings → Apps → Kosh → Storage → Clear Storage`) or uninstalling Kosh permanently and irreversibly erases all local databases, accounts, and cryptographic keys from your device.

---

## 8. Children’s Privacy
Kosh is a personal budgeting and financial management tool intended for individuals aged 18 and older (or the age of majority in your jurisdiction). We do not knowingly collect or solicit data from children under 13.

---

## 9. Changes to This Privacy Policy
We may update our Privacy Policy periodically to reflect app updates or regulatory requirements. Any modifications will be posted within the application and published on our repository with an updated effective date.

---

## 10. Contact Us
If you have any questions or feedback regarding this Privacy Policy, please contact:
- **Application:** Kosh: Personal Financial Vault
- **Developer Support:** support@kosh.app
