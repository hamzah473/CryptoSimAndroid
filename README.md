# CryptoSim — Android crypto trading simulator

A small Android app project (Kotlin + Jetpack Compose) for **paper trading only**:
- Virtual starting balance: **US$10,000,000,000,000**
- Live public Binance Spot prices (no API key)
- Spot buy/sell with simulated balances
- Futures long/short simulator with leverage and estimated liquidation
- Local in-memory state (reset when app process/data is cleared; no real orders)

## Build an APK from an Android phone using GitHub Actions

1. Create/sign in to a GitHub account in your phone browser.
2. Create a **public or private** repository named `CryptoSimAndroid`.
3. Upload all files/folders from this ZIP into the repository (keep folder structure).
4. Open the repository's **Actions** tab and enable Actions if asked.
5. Select workflow **Build CryptoSim Android APK**, then tap **Run workflow**.
6. Wait for the run to finish with a green check.
7. Open that run, scroll to **Artifacts**, download `CryptoSim-debug-apk`.
8. Extract the downloaded artifact ZIP, then tap `app-debug.apk` to install.
9. If Android blocks installation, allow “Install unknown apps” for the browser/file manager you used. Only install APKs you built/trust.

## Important notes
- This is a starter project, not a financial exchange. It never sends orders to Binance.
- Live prices need internet and may be delayed or unavailable due to API/network limits.
- Spot simulation uses current Binance price as the fill reference, without realistic order-book slippage/fees.
- Futures liquidation is a simplified educational estimate, not Binance's exact margin engine.
- Positions and trades are held in app memory only. A later version should add persistence and tests.
- Build output is created by GitHub Actions; this chat does not claim an APK has already been built.
