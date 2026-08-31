# Meridian Privacy Policy

*Last updated: August 31, 2026*

Meridian is a local-first household finance app. This policy describes, honestly and
completely, what data Meridian touches and where it goes — which, for almost everything
the app does, is nowhere but your own devices.

## What Meridian does not do

Meridian has no servers of its own, collects no analytics, and sends no telemetry. There
is no Meridian-run backend that ever sees your holdings, balances, transactions, or any
other financial data. The company behind Meridian cannot see your data, because it never
reaches us — there is nothing to see it *with*.

## Where your data lives

- Your financial data (holdings, cash, expenses, liabilities, and everything else you
  enter) is encrypted on your device with a key derived from your own vault password
  (Argon2id) and stored in a local, encrypted vault file.
- If you sync with another household member, that sync happens either directly between
  your devices (a peer-to-peer connection) or through a cloud folder *you* choose and
  control (e.g. iCloud Drive, Dropbox) — never through a server Meridian operates. Each
  member's file is encrypted with a shared household key derived from a 24-word recovery
  phrase; Meridian never has access to that key or that phrase.
- On iOS (Quasar), unlocking with Face ID uses Apple's on-device biometric APIs. Your
  vault password is stored in the iOS Keychain, protected by Face ID at the OS level —
  it is never transmitted anywhere, including to Meridian.

## Optional third-party services you can connect

These are entirely opt-in, and each uses **your own account and API key**, not one
Meridian provides or has access to:

- **Market data** — Coinbase's public WebSocket (crypto), Alpaca or Yahoo (equities), for
  live price quotes. No account data is sent, only the symbols you hold, to fetch prices.
- **Wallet balances** — CoinStats, only if you add your own free API key, to look up
  public on-chain wallet addresses you've added. Meridian never accepts, stores, or
  transmits a private key or seed phrase for any wallet.
- **The Advisor tab** — if you choose a "bring your own key" AI backend (Anthropic,
  OpenAI, Google, Grok, or a custom endpoint), a summary of your finances (net worth,
  holdings, cash, spending) is sent to that provider's API, billed to your own account,
  to generate a response to your question. If you instead choose a local backend
  (Ollama on desktop, or Apple's on-device Apple Intelligence on Quasar), nothing leaves
  your device at all.

## Software updates

The direct-download build of Meridian checks a public endpoint for new versions and
verifies every update is cryptographically signed before installing it. This check
contains no personal or financial data — only a version number. The Mac App Store and
TestFlight builds use Apple's own update mechanism instead.

## Data you export

Meridian lets you export your own data (CSV, JSON, an encrypted vault backup, or an
estate "Go Bag") to a location you choose. Once exported, that file is yours — Meridian
has no visibility into what happens to it after that point.

## Questions

Meridian is open about how it works — the source is available, and the household sync
protocol, encryption scheme, and threat model are documented in the project's own
`SECURITY.md`. If you have questions about this policy, open an issue at
[github.com/ThinkEnigmatic/Meridian-releases](https://github.com/ThinkEnigmatic/Meridian-releases/issues).
