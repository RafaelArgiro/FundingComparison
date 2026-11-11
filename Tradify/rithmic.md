rithmic

---

https://help.tradeify.co/en/collections/19288902-rithmic

Rithmic
Platform setup guides for Rithmic

4 articles
Tradesea Setup Guide
Complete guide to connecting your Tradeify account to Tradesea, including setup, key features (charts, DOM, trading modes, risk tools, copy trading, hot keys), mobile app, and troubleshooting.
R|Trader Pro Setup Guide
Complete guide to downloading, installing, and connecting your Tradeify account to R|Trader Pro — Rithmic's native trading platform. Covers desktop (Windows), web, and mobile access, key features, and troubleshooting.
Quantower Setup Guide
Guide to installing Quantower and connecting your Tradeify account. Covers beta version setup, Rithmic connection, charting, DOM, volume profile, and troubleshooting.
Sierra Chart Setup Guide
Connect Sierra Chart with Rithmic credentials: sign CME agreement in R|Trader Pro, select Rithmic Direct - DTC, pick Tradeify server, turn off Trade Simulation Mode, fix Permission Denied and login…


---

https://help.tradeify.co/en/articles/14068317-tradesea-setup-guide

Tradesea Setup Guide
Complete guide to connecting your Tradeify account to Tradesea, including setup, key features (charts, DOM, trading modes, risk tools, copy trading, hot keys), mobile app, and troubleshooting.

Updated over 3 weeks ago
This guide covers everything you need to connect your Tradeify account to Tradesea and start trading — from initial setup to key features and troubleshooting.



⚠️ Third-Party Software Notice

Tradesea is a third-party platform not owned or operated by Tradeify. Tradeify does not provide technical support for Tradesea. For platform-specific issues (bugs, UI problems, feature questions), contact Tradesea directly at support@tradesea.ai or visit the Tradesea Help Center. For account or billing questions, contact Tradeify support.





What is Tradesea?
Tradesea is a high-performance, web-based trading platform built for serious futures traders. It combines TradingView-powered charts, an ultra-fast DOM (Depth of Market), and low-latency order execution in one unified interface — no software download required.



Key features:

TradingView charts — Advanced charting with indicators, drawing tools, multi-timeframe layouts, and trade-from-chart execution

Ultra-fast DOM — Real-time price ladder with one-click order entry and draggable order repositioning

Three trading modes — Scalp Mode, DOM Mode, and Order Mode for different trading styles

Built-in risk controls — Position brackets, daily loss/profit limits, and personal lockouts

Copy trading — Mirror trades from a lead account to multiple follower accounts

Mobile apps — Available on iOS and Android for trading on the go



How to access Tradesea:

Web: app.tradesea.ai (recommended)

iOS: App Store

Android: Google Play Store (currently in beta)








Prerequisites
Before connecting to Tradesea, make sure you have:



A Tradeify account purchased with Rithmic as your broker. Tradesea connects using Rithmic credentials. If you purchased with Tradovate or WealthCharts, you cannot use Tradesea.

Your Rithmic credentials. Find your Rithmic username and password in your Tradeify dashboard under your account details.

A Tradesea account. Sign up for free at app.tradesea.ai using your Google account or email (OTP verification).

A supported browser. Google Chrome 111+ (recommended), Microsoft Edge 111+, Firefox 128+, or Safari 16+. Other Chromium-based browsers (Brave, Opera, Vivaldi) work if the Chromium version is 111+.








Connecting Your Tradeify Account
Follow these steps to link your Tradeify trading account to Tradesea:



Step 1: Log in to Tradesea
Go to app.tradesea.ai and log in with your Google account or email OTP. This is your Tradesea account login — not your Rithmic credentials.



Step 2: Open Account Centre
Once logged in, open the Account Centre. You can access it from the top-left account selector dropdown or from the main navigation.






Step 3: Click "Connect New"
In Account Centre, click the "Connect New" button to add a new trading account.






Step 4: Select Tradeify
A list of supported prop firms will appear. Find and select Tradeify from the list, then click Connect.






Step 5: Enter Your Rithmic Credentials
Enter your Rithmic credentials from your Tradeify dashboard:



Rithmic Username — your username from the Tradeify dashboard

Rithmic Password — your password from the Tradeify dashboard

Environment — select Simulation for evaluation and sim funded accounts, or Live for live accounts

Full Name — enter your name as it appears on your Tradeify account



Click Connect to link your account.



Important: Both your Rithmic username and password are case-sensitive. Copy them exactly as shown in your Tradeify dashboard.






Step 6: Verify Connection
After successful authentication, you'll be redirected to Account Centre. Your Tradeify account should now appear as connected. Select it from the account dropdown in the top bar to start trading.








Platform Overview
Once connected, here's a quick tour of the Tradesea Station interface.



Account Panel
The Account Panel in the top bar gives you a real-time snapshot of your trading status:



Account Selector — Switch between connected trading accounts. The selected account determines which account receives your orders.

Balance (Bal) — Your current account balance including all closed trade results.

RPL (Realized P&L) — Total profit or loss from trades that have been closed today.

UPL (Unrealized P&L) — Real-time profit or loss from currently open positions.

Account Status — Shows whether the account is active, restricted, or locked.






TradingView Charts
Tradesea uses TradingView-powered charts with full access to indicators, drawing tools, and custom studies. You can trade directly from the chart by dragging stop-loss and take-profit markers onto price levels.



Multiple chart types and timeframes

Multi-chart layouts (view multiple symbols or timeframes side by side)

Trade from chart — place and manage orders directly on the chart

Customizable chart settings, drawing tools, and saved layouts






DOM (Depth of Market)
The DOM displays a live price ladder showing the best bid and best ask, traded volume at each price, and your own working orders. No synthetic or system-generated liquidity.



Price — Tradable price levels

Bid/Ask Size — Number of buy/sell contracts waiting at each price

Volume — Contracts traded at each price level

My Bid/My Ask — Your active working orders on the ladder

Level 1 data: Rithmic accounts include Level 1 CME market data. The DOM shows the best bid and best ask along with your own working orders — it does not show full order book depth. Level 2 depth data and EUREX data are not yet available on Rithmic accounts and cannot be purchased — coming soon. See Level 2 (L2) and EUREX Data: Availability by Broker.





Click a bid column price to place a buy limit order, or an ask column price for a sell limit order. Working orders can be cancelled or repositioned directly on the ladder.






Order Types
Tradesea supports the following order types:



Market Order — Executes immediately at the best available price

Limit Order — Executes only at your specified price or better

Stop Market Order — Becomes a market order when the trigger price is reached

Stop Limit Order — Becomes a limit order after the stop price is triggered

Trailing Stop-Loss — A stop that automatically moves as the price moves in your favor

Bracket Order — Attaches a stop-loss and take-profit to a single entry order





Trading Modes
Tradesea offers three trading modes designed for different styles and speeds of execution.



Scalp Mode
Optimized for fast execution and quick trades. A movable floating Scalp Pad lets you place orders without leaving the chart. Features include:



Buy/Sell — Instant market orders

Join Bid/Join Ask — Limit orders at the current best bid or ask

Close Position — Quick exit at market

Lot Selector — Set order size for subsequent trades



Best for: Scalpers, momentum traders, and high-frequency intraday trading.






DOM Mode
Designed for order-flow and precision traders who want direct interaction with the order book. Click price levels on the DOM ladder to place limit orders, drag to reposition, and use the execution panel for quick actions (Buy, Sell, Join Bid, Join Ask, Close, Reverse, Cancel All, Flatten All).



Best for: Intraday traders, order-flow traders, and active position managers.






Order Mode
Built for planned trades where the full trade structure is defined before entry. Select your direction, order type (market, limit, stop), position size, and attach automatic stop-loss and take-profit levels before submitting.



Best for: Swing traders, positional traders, and strategy-based setups with defined risk-reward ratios.








Risk Management Features
Tradesea includes built-in risk controls to help you manage your trading discipline. These are personal risk tools you configure yourself — they are separate from Tradeify's account-level rules (Daily Loss Limit and Max Trailing Drawdown), which are enforced by Tradeify regardless of your platform settings.



Position Brackets
Position brackets manage your entire open position with a single stop-loss and take-profit. Unlike order brackets (which protect individual orders), position brackets automatically adjust when you add to or reduce your position:



Enter a trade — bracket is placed for the full position

Add contracts — average price recalculates and bracket adjusts automatically

Partially close — bracket resizes to match remaining exposure



You can also enable Auto Position Brackets to automatically attach stop-loss and take-profit to every new position.



Daily Loss & Profit Limits
Set personal daily boundaries to protect your account:



Personal Daily Loss Limit (PDLL) — Maximum daily loss before Tradesea takes action

Personal Daily Profit Target (PDPT) — Daily profit target to lock in gains



When a limit is hit, you choose the action: Liquidate (closes positions) or Liquidate and Block (closes positions and locks trading for the rest of the day).



To configure: click Settings (top right) and find the PDLL/PDPT fields.






Personal Lockouts
Personal lockouts let you temporarily block yourself from placing orders — a cooling-off tool to prevent impulsive or revenge trading after losses.



To activate: click the padlock icon in the upper right corner (above the DOM). Choose a preset trading session or enter a custom lockout duration in hours, then click Set Lockout. A countdown timer appears in the top right showing time remaining.








Copy Trading
Tradesea's built-in trade copier lets you mirror trades from one account to multiple accounts automatically. This is useful if you have several Tradeify accounts and want them to execute the same trades.



Lead Account — The account where you place trades manually. Orders are automatically copied to follower accounts.

Follower Accounts — Accounts that automatically receive and execute the same trades as the lead.



To set up: go to Settings > Copy Trading, then assign which account is the lead and which are followers.



Note: Copy trading is explicitly allowed by Tradeify. Using a trade copier across your own accounts does not violate any Tradeify rules, provided every account trades in the same direction. Do not configure the copier to reverse or invert direction on any follower account — opposing positions across your accounts are a hedging violation. See Rules: Hedging & Correlated Products.








Hot Keys
Tradesea supports customizable keyboard shortcuts for fast execution. Access via Settings > Hot Keys.



Default hot keys:



B — Buy Market

S — Sell Market

J — Join Bid (limit order at current best bid)

A — Join Ask (limit order at current best ask)

R — Reverse Position (close and reopen opposite side)

F — Flatten All (close positions and cancel working orders)

C — Cancel All (cancel all working orders)

X — Close All (exit all open positions at market)



⚠️ Warning: Hot keys trigger live trading actions. Make sure you understand what each key does before activating them — especially Flatten All, Close All, and Reverse Position.








Mobile App
Tradesea is available as a mobile app on iOS and Android (Android is currently in beta). Connect your Tradeify account using the same Rithmic credentials as the web version.



Mobile features include:

TradingView charts with trade-from-chart execution

DOM trading

Order and position management

Account switching between connected accounts

Market watchlists







Troubleshooting


Dashboard or balance not updating after a holiday or half-day
Tradesea runs on Rithmic, and Rithmic does not run its end-of-day report and reconciliation on shortened (holiday or early-close) sessions. That day is combined with the next full session and posts at the next full market close — for example, a Friday half-day posts after Monday's close. So if your balance or P&L looks stuck right after a holiday or half-day, this is expected and will update at the next full market close. It is not a sync error, and you do not need to contact Tradesea support for it.



Rithmic credentials not working
Both username and password are case-sensitive — copy them exactly from your Tradeify dashboard

Make sure you are using your Rithmic credentials (not your Tradeify login or Tradesea login)

If you recently reset your password, try the new password

Verify your account is active in your Tradeify dashboard



Tradeify not listed as a prop firm
Make sure you are clicking Connect New from Account Centre (not just the account dropdown)

Try refreshing the page and checking again

If Tradeify still does not appear, contact support@tradesea.ai



Account connected but not visible in Station
Open Account Centre and verify the account shows as Connected

Refresh the platform (F5 or browser refresh)

Use the account selector dropdown in the top bar to switch to the correct account



Platform lag or slow performance
Use Google Chrome (latest version) for the best performance

Disable VPN if you are using one — VPNs add latency and can cause disconnections

Close unnecessary browser tabs to free up memory

Try clearing your browser cache or using an incognito/private window



Need more help?
Platform issues (bugs, UI problems, features): Contact Tradesea at support@tradesea.ai or visit the Tradesea Help Center

Account or billing issues (credentials, account status, payments): Contact Tradeify support through the chat widget in your dashboard

---

https://help.tradeify.co/en/articles/14068316-r-trader-pro-setup-guide


R|Trader Pro Setup Guide
Complete guide to downloading, installing, and connecting your Tradeify account to R|Trader Pro — Rithmic's native trading platform. Covers desktop (Windows), web, and mobile access, key features, and troubleshooting.

Updated over 3 weeks ago
This guide covers everything you need to connect your Tradeify account to R|Trader Pro and start trading — from downloading and installing the platform to connecting your account and navigating key features.



⚠️ Third-Party Software Notice

R|Trader Pro is developed and maintained by Rithmic, a third-party company not owned or operated by Tradeify. Tradeify does not provide technical support for R|Trader Pro. For platform-specific issues (bugs, UI problems, feature questions), contact Rithmic directly at support@rithmic.com or visit the Rithmic FAQ. For account or billing questions, contact Tradeify support.





What is R|Trader Pro?
R|Trader Pro is Rithmic's native trading platform, built for professional-grade futures trading. It provides comprehensive charting with over 100 built-in technical studies, a full-featured Depth of Market (DOM) price ladder, advanced order types, and server-side order execution — meaning your orders stay active on Rithmic's servers even if your connection drops.



Key features:

100+ technical studies — Comprehensive charting with customizable indicators, multiple chart types, drawing tools, and trade-from-chart execution

Depth of Market (DOM) — Real-time price ladder, bid/ask sizes, and one-click order entry

Advanced order types — Market, limit, stop, stop-limit, trailing stop, bracket, OCO (One Cancels Other), and group orders

Server-side orders — Orders persist on Rithmic's servers even if your internet drops, so your stop-loss and brackets stay active

Excel real-time interface — Stream live market data directly into Microsoft Excel spreadsheets (desktop version only)

Multi-platform access — Available on desktop (Windows), web browser, and mobile (iOS and Android)



How to access R|Trader Pro:

Desktop (Windows): Download the installer from rithmic.com/rtraderpro

Web: rtraderpro.rithmic.com/rtraderpro-web (Chrome, Edge, Safari, and other modern browsers)

iOS: App Store

Android: Google Play Store








Prerequisites
Before connecting to R|Trader Pro, make sure you have:



A Tradeify account purchased with Rithmic as your broker. R|Trader Pro connects using Rithmic credentials. If you purchased with Tradovate or WealthCharts, you cannot use R|Trader Pro.

Your Rithmic credentials. Find your Rithmic username and password in your Tradeify dashboard under your account details.

For desktop: A Windows computer. R|Trader Pro desktop requires Windows 10 or later (not Windows S mode), a dual-core CPU, 4 GB+ RAM, and a high-speed internet connection. Mac and Linux users should use the web version instead.

For web: A modern browser. Google Chrome (recommended), Microsoft Edge, Safari, or other modern browser.








Connecting Your Tradeify Account
The login process is the same whether you are using the desktop, web, or mobile version of R|Trader Pro. Follow these steps to connect your Tradeify trading account.



Step 1: Open R|Trader Pro
Launch R|Trader Pro using whichever version you prefer:



Desktop: Download the installer from rithmic.com/rtraderpro, run the .msi file, and follow the installation prompts. Once installed, launch R|Trader Pro from your Start menu or desktop shortcut.

Web: Go to rtraderpro.rithmic.com/rtraderpro-web in your browser.

Mobile: Download "Rithmic Trader Pro" from the App Store (iOS) or Google Play Store (Android) and open the app.






Step 2: Enter Your Credentials
On the login screen, enter your Rithmic credentials from your Tradeify dashboard:



Username — your Rithmic username from the Tradeify dashboard

Password — your Rithmic password from the Tradeify dashboard



Important: Both your username and password are case-sensitive. Copy them exactly as shown in your Tradeify dashboard.



Step 3: Select System Name
In the System Name dropdown, select "Tradeify". This tells R|Trader Pro which prop firm's server to connect to.



If you do not see "Tradeify" in the list, make sure you have the latest version of R|Trader Pro installed. See the Troubleshooting section below for more help.






Step 4: Select Gateway
Select the Gateway server closest to your physical location for the best connection speed:



Chicago Area — recommended for most US-based traders

Select a different gateway if you are located outside the US — choose the one closest to your region






Step 5: Log In and Verify
Click Login. Once authenticated, your Tradeify trading account should appear and market data should begin streaming. Verify that you can see your account balance and live price data.








Platform Overview
Once connected, here is a quick tour of R|Trader Pro's main features.



Charting
R|Trader Pro includes a full charting package with over 100 built-in technical studies. You can customize chart types (candlestick, bar, line, and more), timeframes, drawing tools, and annotations. Charts support trade-from-chart execution — place and manage orders directly on the chart by clicking at your desired price level.






DOM (Depth of Market)
The DOM displays a real-time price ladder showing the best bid and best ask sizes at each price level. You can place orders directly from the DOM with a single click, view your working orders on the ladder, and modify or cancel orders by dragging them to a new price level.



Level 1 data: Rithmic accounts include Level 1 CME market data. The DOM shows the best bid and best ask along with your own working orders — it does not show full order book depth. Level 2 depth data and EUREX data are not yet available on Rithmic accounts and cannot be purchased — coming soon. See Level 2 (L2) and EUREX Data: Availability by Broker.






Order Types
R|Trader Pro supports a comprehensive set of order types for managing your trades:



Market Order — executes immediately at the best available price

Limit Order — executes only at your specified price or better

Stop Market Order — becomes a market order when the trigger price is reached

Stop Limit Order — becomes a limit order when the stop price is triggered

Trailing Stop — a stop that automatically adjusts as price moves in your favor

Bracket Order — attaches a stop-loss and take-profit to a single entry order

OCO (One Cancels Other) — two linked orders where filling one automatically cancels the other

Group Orders — link multiple orders together for coordinated execution





Key Features


Server-Side Orders
One of R|Trader Pro's standout features is server-side order management. When you place trailing stops, brackets, or OCO orders, they are stored and managed on Rithmic's servers — not on your local computer. This means if your internet connection drops or your computer crashes, your protective orders (including stop-losses) remain active and will execute as configured.



This is particularly important for risk management. Your stop-loss will execute even if you lose connectivity, helping protect your account from unexpected losses.



Excel Real-Time Interface
The desktop version of R|Trader Pro includes a two-way real-time interface with Microsoft Excel. You can stream live market data (quotes, trades, market depth) directly into Excel spreadsheets and view over 100 studies in real-time. With the power of Excel, you can build custom analysis tools and even send orders back into R|Trader Pro from your spreadsheets.



Note: The Excel interface is available on the desktop version only and requires Microsoft Excel installed on your Windows computer.







Desktop Installation


System Requirements
Operating System: Windows 10 or later (not Windows S mode)

Processor: Dual-core CPU or better

Memory: 4 GB RAM minimum

Internet: High-speed broadband connection

Not supported: macOS, Linux — use the web version instead



Note: Actual requirements may vary based on the number of instruments you are monitoring, the number of active windows, and other software running concurrently.



Download and Install
Go to rithmic.com/rtraderpro

Download the Windows installer (.msi file)

Run the installer and follow the on-screen prompts

Once installed, launch R|Trader Pro from your Start menu (All Programs > Rithmic > Launch > Rithmic Trader Pro) or from the desktop shortcut



Updating R|Trader Pro
R|Trader Pro may prompt you to update when a new version is available. You can also manually update by downloading the latest installer from rithmic.com/rtraderpro and running it — the new version will replace the existing installation.





Web and Mobile Access


Web Version
The web version of R|Trader Pro runs in your browser with no download required. Access it at rtraderpro.rithmic.com/rtraderpro-web. It works with Chrome, Edge, Safari, and other modern browsers.



The web version is a good alternative for Mac and Linux users who cannot run the desktop version. The login process is the same — enter your Rithmic credentials, select "Tradeify" as the System Name, and choose your closest Gateway.



Note: The web version may have limited availability for simulation accounts. If you cannot access the web version, use the desktop version instead.



Mobile App
R|Trader Pro is available on mobile devices for trading on the go:



iOS: Download from the App Store

Android: Download from Google Play Store



The mobile app uses the same login credentials and System Name/Gateway selection as the desktop and web versions. It includes charting, order entry, and position management for managing trades from your phone or tablet.



Note: The mobile version may have limited availability for simulation accounts. If you cannot access the mobile app, use the desktop or web version instead.







Troubleshooting


Rithmic credentials not working
Both your username and password are case-sensitive — copy them exactly as shown in your Tradeify dashboard

Make sure you are using your Rithmic credentials (not your Tradeify website login — these are different)

If you recently reset your password, try the new password

Verify your account is active in your Tradeify dashboard



"Tradeify" not appearing in System Name dropdown
Make sure you have the latest version of R|Trader Pro installed

If using the desktop version, re-download the installer from rithmic.com/rtraderpro and reinstall

If using the web version, try clearing your browser cache and refreshing the page

Contact Tradeify support if "Tradeify" still does not appear after updating



Connection failed or gateway timeout
Try selecting a different Gateway server (e.g., switch from one region to another)

Chicago Area is recommended for most US-based traders

Disable VPN if you are using one — VPNs add latency and can cause connection failures

Check your internet connection and firewall settings — R|Trader Pro may need to pass through your firewall



Desktop installer won't run
Verify you are running Windows 10 or later (not Windows S mode)

Right-click the .msi file and select "Run as administrator"

Check that your antivirus software is not blocking the installer

If you are on Mac or Linux, the desktop version is not supported — use the web version instead



Platform lag or slow performance
Desktop: Close unnecessary applications to free up RAM and CPU

Web: Use Google Chrome (latest version) for the best performance and close unnecessary browser tabs

All versions: Disable VPN if you are using one — VPNs add latency

Desktop: Verify your system meets the minimum requirements (dual-core CPU, 4 GB RAM, high-speed internet)



Need more help?
Platform issues (bugs, UI problems, features): Contact Rithmic at support@rithmic.com or visit rithmic.com/faq

Account or billing issues (credentials, account status, payments): Contact Tradeify support through the chat widget in your dashboard

---

https://help.tradeify.co/en/articles/12294317-quantower-setup-guide

Quantower Setup Guide
Guide to installing Quantower and connecting your Tradeify account. Covers beta version setup, Rithmic connection, charting, DOM, volume profile, and troubleshooting.

Updated over 3 weeks ago
This guide covers everything you need to download, install, and connect your Tradeify account to Quantower — from setting up the beta version to navigating the platform's advanced charting and order flow tools.



⚠️ Third-Party Software Notice

Quantower is a third-party platform not owned or operated by Tradeify. Tradeify does not provide technical support for Quantower. For platform-specific issues (bugs, UI problems, feature questions), visit the Quantower Help Center or contact Quantower support. For account or billing questions, contact Tradeify support.





What is Quantower?
Quantower is a professional-grade desktop trading platform built for serious futures traders who want deep market analysis. It combines advanced charting with over 150 technical indicators, a powerful DOM (Depth of Market) with heatmap visualization, volume profile analysis, and footprint (cluster) charts — giving you a complete picture of order flow and market structure.



Key features:

150+ technical indicators — Comprehensive charting with customizable indicators, multiple chart types, drawing tools, and multi-timeframe analysis

DOM and DOM Surface — Real-time price ladder, one-click order entry, and a heatmap visualization showing where large orders are resting

Volume Profile — Overlay volume distribution at each price level to identify high-volume nodes, points of control, and value areas

Footprint (Cluster) Charts — Break down traded volume at each price level, showing buyer vs. seller activity, delta, and imbalances

Order flow analysis — Power Trades detection, Time & Sales, and cumulative delta to track institutional activity

Custom indicators — Build your own indicators and automated strategies using C#

Multi-monitor support — Detach and arrange panels across multiple screens for a fully customizable workspace



How to access Quantower:

Desktop (Windows): Download for free from quantower.com/download



Quantower is a Windows-only desktop application. Mac users can run Quantower using virtual machine software such as Parallels, VMware Fusion, or VirtualBox.








Prerequisites
Before connecting to Quantower, make sure you have:



A Tradeify account purchased with Rithmic as your broker. Quantower connects using Rithmic credentials. If you purchased with Tradovate or WealthCharts, you cannot use Quantower.

Your Rithmic credentials. Find your Rithmic username and password in your Tradeify dashboard under your account details.

A Windows computer. Quantower requires Windows 10 or later, a 4-core CPU (recommended), 16 GB RAM (recommended), an SSD, and a high-speed internet connection. Mac users can run Quantower using virtual machine software (Parallels, VMware Fusion, or VirtualBox).

.NET 8 installed. Quantower requires .NET 8. The installer will prompt you to download it from Microsoft if it is not already installed.








Download and Install


Step 1: Download Quantower
Go to quantower.com/download and download the installer. Run the installer and follow the on-screen prompts to complete the installation.






Step 2: Enable Beta Version
⚠️ Important: You must enable the beta version of Quantower to connect to Tradeify. The stable release does not yet support the Tradeify connection.



Open Quantower and click the General Settings icon (top right of the platform)

Find and enable the option "Use beta version"

Close the General Settings window

Click the "Refresh platform" button (top right) to download the beta update

Once the update finishes, restart Quantower











Connecting Your Tradeify Account
After restarting Quantower with the beta version enabled, follow these steps to connect your Tradeify account.



Step 3: Open the Connection Manager
In the Quantower main panel, click Connections to open the Connection Manager. Select Rithmic from the list of available connections.





Step 4: Select Tradeify Server
In the connection settings, select "Tradeify" from the server dropdown menu.





Step 5: Enter Your Credentials
Enter your Rithmic credentials from your Tradeify dashboard:



Username — your Rithmic username from the Tradeify dashboard

Password — your Rithmic password from the Tradeify dashboard



Important: Both your username and password are case-sensitive. Copy them exactly as shown in your Tradeify dashboard.



Step 6: Connect
Click Connect. Once authenticated, your Tradeify trading account should appear in the account panel and market data should begin streaming. Verify that you can see your account balance and live price data.







Platform Overview
Once connected, here is a quick tour of Quantower's main features.



Charting
Quantower's charting engine supports over 150 built-in technical indicators with customizable parameters, multiple chart types (candlestick, bar, line, Heikin Ashi, Renko, Range, and more), drawing tools, and multi-timeframe analysis. You can link chart panels together so switching instruments updates all connected panels simultaneously.





DOM (Depth of Market)
The DOM displays a real-time price ladder showing the best bid and best ask sizes and traded volume at each price level. You can place orders with a single click, drag working orders to new price levels, and view your position and P&L in real-time.



Quantower also offers DOM Surface — a heatmap visualization that plots price and traded activity over time. Note that its full order book depth view requires Level 2 data, which is not yet available on Rithmic accounts.

Level 1 data: Rithmic accounts include Level 1 CME market data. The DOM shows the best bid and best ask along with your own working orders — it does not show full order book depth. Level 2 depth data and EUREX data are not yet available on Rithmic accounts and cannot be purchased — coming soon. See Level 2 (L2) and EUREX Data: Availability by Broker.







Volume Profile
Volume Profile overlays show how much volume was traded at each price level over a given period. Use them to identify:



Point of Control (POC) — the price level with the highest traded volume

Value Area — the range where approximately 70% of trading volume occurred

High Volume Nodes — price levels that attracted heavy trading activity

Low Volume Nodes — price levels that may act as support or resistance





Footprint (Cluster) Charts
Footprint charts (also called cluster charts) break down the traded volume at each price level within each candle, showing you exactly how much was bought vs. sold. This includes:



Buy/Sell Volume — see the split between aggressive buyers and sellers at each price

Delta — the difference between buy and sell volume, revealing directional pressure

Cumulative Delta — running total of delta to track the overall buyer/seller balance

Imbalances — highlighted price levels where one side heavily dominated





Order Types
Quantower supports a full set of order types:



Market Order — executes immediately at the best available price

Limit Order — executes only at your specified price or better

Stop Order — becomes a market order when the trigger price is reached

Stop Limit Order — becomes a limit order when the stop price is triggered

Trailing Stop — a stop that automatically adjusts as price moves in your favor

OCO (One Cancels Other) — two linked orders where filling one automatically cancels the other





Troubleshooting


"Tradeify" not appearing in server list
Make sure you have enabled the beta version in General Settings and restarted Quantower

Click the Refresh platform button to ensure you have the latest beta update

If you are running an older version of Quantower, download the latest version from quantower.com/download and reinstall



Rithmic credentials not working
Both your username and password are case-sensitive — copy them exactly as shown in your Tradeify dashboard

Make sure you are using your Rithmic credentials (not your Tradeify website login — these are different)

Verify that "Tradeify" is selected as the server in the connection settings

If you recently reset your password, try the new password

Verify your account is active in your Tradeify dashboard



Connection drops or data freezes
Disable VPN if you are using one — VPNs add latency and can cause disconnections

Check your internet connection and ensure you have stable broadband

Try disconnecting and reconnecting from the Connection Manager

If the issue persists, restart Quantower



Platform lag or slow performance
Close unnecessary panels and reduce the number of active charts to free up memory

Make sure your system meets the recommended requirements (4-core CPU, 16 GB RAM, SSD)

Disable unnecessary indicators or volume analysis tools on charts you are not actively using

Close other resource-heavy applications running alongside Quantower



.NET 8 errors on startup
If Quantower displays an error about .NET 8 on startup, download and install the latest version of .NET 8 from the Microsoft .NET download page, then restart Quantower.



Need more help?
Platform issues (bugs, UI problems, features): Visit the Quantower Help Center or contact Quantower support

Account or billing issues (credentials, account status, payments): Contact Tradeify support through the chat widget in your dashboard


---

https://help.tradeify.co/en/articles/14477114-sierra-chart-setup-guide


Sierra Chart Setup Guide
Connect Sierra Chart with Rithmic credentials: sign CME agreement in R|Trader Pro, select Rithmic Direct - DTC, pick Tradeify server, turn off Trade Simulation Mode, fix Permission Denied and login errors.

Updated over 3 weeks ago
This guide covers everything you need to connect your Tradeify account to Sierra Chart and start trading — from subscription requirements and CME market data agreements to configuring the Rithmic data service and troubleshooting common issues.



⚠️ Third-Party Software Notice

Sierra Chart is a third-party platform not owned or operated by Tradeify. Tradeify does not provide technical support for Sierra Chart. For platform-specific issues (bugs, UI problems, feature questions), visit the Sierra Chart Support Board or email Sierra Chart support. For account or billing questions, contact Tradeify support.





What is Sierra Chart?
Sierra Chart is a professional-grade charting and trading platform for Windows, known for its speed, reliability, and deep customization. It connects to Rithmic for real-time market data and order execution, and is popular among futures traders who want institutional-level charting and analysis tools.



Key features:

Advanced charting — Hundreds of built-in technical studies, multiple chart types, real-time streaming, and minimal latency

Spreadsheet-based customization — Build custom studies and calculations using built-in spreadsheet formulas, no coding required

DOM (Depth of Market) — Real-time price ladder trading with configurable columns (Level 1 data on Tradeify accounts)

Order flow and volume analysis — Volume-at-price, footprint charts, market depth historical graph, and Numbers Bars

Chart replay — Replay historical market data tick-by-tick for practice and strategy backtesting

Automated trading (ACSIL) — Build custom automated trading systems using C++ via the Advanced Custom Study Interface and Language

Multi-monitor support — Detach and arrange chartbooks across multiple screens



Level 1 data: Rithmic accounts include Level 1 CME market data. The DOM shows the best bid and best ask along with your own working orders — it does not show full order book depth. Level 2 depth data and EUREX data are not yet available on Rithmic accounts and cannot be purchased — coming soon. See Level 2 (L2) and EUREX Data: Availability by Broker.



How to access Sierra Chart:

Desktop (Windows): Download from sierrachart.com (Windows only — no native Mac or Linux versions)







Prerequisites
Before connecting to Sierra Chart, make sure you have:



A Tradeify account purchased with Rithmic as your broker. Sierra Chart connects using Rithmic credentials. If you purchased with Tradovate or WealthCharts, you cannot use Sierra Chart.

Your Rithmic credentials. Find your Rithmic username and password in your Tradeify dashboard under your account details.

A Sierra Chart subscription (Package 10 or higher). Sierra Chart requires a paid "Integrated" subscription to connect to Rithmic. Package 10 ("Integrated Standard") is the minimum at $36/month ($23.40/month with prepaid annual). Packages 3 and 5 do NOT support external data feeds like Rithmic. Subscribe at sierrachart.com.

A Windows computer. Sierra Chart is a Windows desktop application. Mac and Linux users can run it via a virtual machine or compatibility layer (e.g., Parallels, Wine), but this is not officially supported by Sierra Chart.

CME market data agreements signed. You must log in to R|Trader Pro at least once and accept the CME Non-Professional Market Data Agreement before Sierra Chart can receive market data. See Step 1 below.







Connecting Your Tradeify Account
Follow these steps to configure Sierra Chart to connect to your Tradeify trading account using Rithmic. For a visual reference of the settings windows, see Sierra Chart's official Rithmic setup documentation.



Step 1: Sign CME Market Data Agreements
Before connecting Sierra Chart, you must sign the CME Non-Professional Market Data Agreement through R|Trader Pro. If you have already done this (e.g., when setting up another Rithmic platform), you can skip to Step 2.



Go to rtraderpro.rithmic.com/rtraderpro-web (the R|Trader Pro web version)

Log in with your Rithmic credentials from your Tradeify dashboard

Select System Name: "Tradeify"

Accept any CME Non-Professional Market Data Agreements that appear

Once signed, you can close R|Trader Pro — you only need to do this once



Important: If you skip this step, Sierra Chart will show "Permission Denied" errors when trying to load market data.





Step 2: Open Data/Trade Service Settings
Open Sierra Chart and go to Global Settings → Data/Trade Service Settings from the menu bar at the top of the window.





Step 3: Select Rithmic Data Feed
In the Data/Trade Service Settings window, find the "Current Selected Service (List)" dropdown and select "Rithmic Direct - DTC [Trading]". Then click OK to save.



Important: After clicking OK, Sierra Chart needs a moment to load the available server list from Rithmic. Wait about 5–10 seconds, then reopen Global Settings → Data/Trade Service Settings before proceeding to the next step.





Step 4: Select Your Server
After reopening Data/Trade Service Settings, the Server (List) dropdown will now be populated with available Rithmic servers. Select the correct server for your account type:



Evaluation and Sim Funded accounts: Select "Tradeify" (you may see variations like "Tradeify-Chicago Area-Non-Aggregated" — any "Tradeify" option will work)

Live Funded accounts: Select "Rithmic 01" (you may see "Rithmic 01 - US" or similar)



Important: Using the wrong server will prevent you from connecting. Evaluation and Sim Funded accounts must use a "Tradeify" server. If the Server dropdown is empty, close and reopen the settings window — the list loads asynchronously after selecting the Rithmic service.





Step 5: Enter Your Rithmic Credentials
Enter your Rithmic credentials from your Tradeify dashboard in the following fields. All three credential pairs use the same Rithmic username and password:



Trading Username — your Rithmic username

Trading Password — your Rithmic password

Market Data Username — same Rithmic username

Market Data Password — same Rithmic password

Historical Data Username — same Rithmic username

Historical Data Password — same Rithmic password



Click OK to save the settings.



Important: Credentials are case-sensitive. Copy them from your Tradeify dashboard, then check that no extra spaces were added at the start or end. If your username or password is longer than 31 characters, contact Tradeify support to have it shortened.





Step 6: Connect and Verify
Go to File → Connect to Data Feed (or press F11). Sierra Chart will connect to Rithmic and begin streaming market data.



To verify the connection is working:



The connection status bar at the top of the window should turn green

Open a chart (File → New Chart or Chart → Open) and select a futures symbol (e.g., ES) to confirm data is flowing

Check Trade → Trade Activity Log for connection status messages





Step 7: Disable Trade Simulation Mode
Sierra Chart may start in Trade Simulation Mode by default. When this mode is enabled, your orders are simulated locally and not sent to the exchange through Rithmic.



To disable it, go to Trade → Trade Simulation Mode On/Off and make sure it is unchecked (off). When Trade Simulation Mode is off, your orders will be sent through Rithmic to the exchange.



⚠️ Warning: If Trade Simulation Mode is on, you will see simulated fills but no actual orders will be placed. Your Tradeify account balance will not change. Always verify this setting before placing trades.







Optional: Denali Exchange Data Feed
Sierra Chart offers an optional alternative market data source called the Denali Exchange Data Feed, which is Sierra Chart's own exchange data service. If you configured the Rithmic data feed using the steps above, you do not need Denali — your market data is already provided through Rithmic.



Denali is a separate paid add-on ($6–$40.50/month depending on the exchanges you subscribe to) and has its own CME non-professional rate requirements. It is primarily designed for traders with personal live funded brokerage accounts.



For most Tradeify users, the Rithmic data feed configured above is the recommended approach. If you want to learn more about Denali, visit the Sierra Chart Denali Exchange Data Feed page.





Troubleshooting


"Permission Denied" or no market data
This usually means you have not signed the CME Non-Professional Market Data Agreements

Log in to R|Trader Pro (web) with your Rithmic credentials and System Name "Tradeify"

Accept any market data agreements that appear, then try Sierra Chart again

If you already signed, wait 15–30 minutes and try reconnecting — agreement propagation can be delayed



Login failed or connection refused
Make sure you are using your Rithmic credentials (not your Tradeify website login or your Sierra Chart subscription login — these are all different)

Verify all six credential fields (Trading, Market Data, Historical Data) have the same username and password

Credentials are case-sensitive — copy them from your Tradeify dashboard and check for extra spaces at the start or end

If you recently reset your password, try the new password

Verify your account is active in your Tradeify dashboard



Wrong server or cannot find account
Evaluation and Sim Funded accounts must use a "Tradeify" server (for example "Tradeify-Chicago Area-Non-Aggregated")

Live Funded accounts must use "Rithmic 01"

If the Server dropdown is empty, close the Data/Trade Service Settings window, wait a few seconds, and reopen it — the server list loads asynchronously after selecting the Rithmic service



Session already in use (platform conflict)
Rithmic credentials can only maintain one active session per connection type at a time

If you are logged into another Rithmic platform (R|Trader Pro, Tradesea, or Quantower), close it before connecting Sierra Chart

If Sierra Chart says the session is already in use, log out of all other Rithmic-connected platforms and try again



Orders not appearing in Tradeify dashboard
Check that Trade Simulation Mode is off (Trade → Trade Simulation Mode On/Off should be unchecked)

When simulation mode is on, Sierra Chart processes orders locally without sending them to Rithmic

Verify by checking the Trade Activity Log — simulated orders will show "Sim" indicators



Platform lag or slow performance
Close unnecessary chartbooks and studies to reduce CPU and memory usage

Disable VPN if you are using one — VPNs add latency and can cause disconnections

Sierra Chart is designed for Windows — if running through a virtual machine or compatibility layer, performance may be reduced

Make sure Sierra Chart is up to date (File → Fast Update)



Need more help?
Platform issues (bugs, UI problems, features): Visit the Sierra Chart Support Board or email Sierra Chart support

Account or billing issues (credentials, account status, payments): Contact Tradeify support through the chat widget in your dashboard

---
