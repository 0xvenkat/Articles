# A Deep Dive into Perpetuals: Drift Protocol
#### Published Jun, 2024 for LVResearch 

![Image](https://github.com/user-attachments/assets/89083f15-5d2f-4b24-854f-65ca7f2c6d27)

## 1. Overview
The DeFi ecosystem is rapidly embracing perpetual trading protocols, positioning Drift Protocol as a prominent player. 
Built on the Solana blockchain, Drift Protocol aims to redefine decentralised perpetual trading with a focus on scalability, efficiency, and security, appealing significantly to the DeFi landscape through its innovative three liquidity mechanism - JIT (Just In Time), DLOB (Decentralised Orderbook) and Drift AMM.

## 2. Key Performance Metrics
#### 2.1 Trading Volume
Cumulative Trading Volume: As of the latest data, Drift Protocol has facilitated a cumulative trading volume of $29.19 billion.
Weekly Trading Volume Trends: Drift had a peak weekly trading volume around their airdrop announcement in April 2024. Third week of June was the highest volume week post-airdrop, without points and a live rewards program indicating real product usage.
Daily Trading Volume Analysis: Daily volumes fluctuate with significant peaks, indicative of market reactivity and trader engagement on the platform.

#### 2.2 Total Trades
Cumulative Trades: The platform has executed a total of 18,422,338 trades, indicating robust trading activity and platform reliability.

#### 2.3 Drift Users
Total Registered Users: The user base has reached a cumulative total of 192,801, highlighting the platform's expanding community.
User Growth Trends: Weekly data reveals significant spikes in user registration, particularly noticeable in early 2024, suggesting effective user acquisition strategies.
Daily User Engagement: Daily user statistics provide insights into active users, with peaks correlating to promotional events or market volatility.

#### 2.4 Total Value Locked (TVL)
Current TVL in USD: The total value locked within Drift Protocol stands at $335,063,247, underscoring the trust and liquidity that users place in the platform.
TVL Growth Over Time: The TVL has seen upward trends, particularly in the latter half of the period displayed, indicating increased asset deposits and protocol utilisation.

![Image](https://github.com/user-attachments/assets/c9267c7d-deef-46ec-b074-3b6d915dc653)

## 3. Introduction
Drift Protocol is a decentralized trading platform on Solana, designed to offer advanced DeFi instruments like perpetual futures and spot trading with leverage. 
Leveraging Solana's high-speed, low-cost infrastructure, Drift provides sophisticated risk management via cross-margined lending/borrowing, optimizing collateral efficiency.

Central to Drift V2 is it’s Deep Liquidity, Robust Security that is computationally efficient, and incentivises market maker participation, as well as liquidity provision.
Drift offers users perpetual swaps with up to 10x leverage, leveraged spot trading, and yield earning on deposits. Users can also participate in insurance fund staking for additional yield and utilize advanced tools for efficient market making. These features are designed to provide a comprehensive, high-speed, and low-cost trading experience.

#### 3.1 Why?
The Problem - On-chain exchanges face limitations due to blockchain speed and computational capacity. 
When off-chain centralized exchange infrastructure is ported onto the blockchain, it leads to inefficient blockchain use and discourages market-maker participation due to unfavorable conditions. 
Consequently, most on-chain orderbooks experience slow fills, high spreads, and low liquidity.

#### 3.2 History
Behind the scenes, Drift Protocol is led by Cindy Leow, a seasoned professional in the web3 space. Cindy began her crypto journey in 2017 by capitalizing on Bitcoin price disparities between the US and Korea. Following her success, she founded a digital asset management company and contributed to decentralized derivatives projects on Ethereum, before moving her focus to Solana, attracted by its user-friendly interface, rapid transaction speeds, and robust ecosystem.
Notable Versions:
Drift V1: Drift launched its first version in November 2021. This version introduced the DAMM, which provides liquidity and minimizes slippage. Drift V1 quickly gained traction, amassing over $10 billion in trading volume within six months.
Drift V2: Launched on December 19, 2022, this version enhanced the platform with new features such as Just-in-Time (JIT) liquidity, decentralized order books, and passive liquidity providers. Drift V2 also introduced robust security measures and expanded its offerings to include spot trading, borrowing, and lending.

#### 3.3 Getting Started
Add 1 SOL to your Solana wallet.
Visit Drift Protocol.
Connect and fund your wallet.
Begin trading or providing liquidity as desired.

#### 3.4 Core Products
##### 3.4.1 Trading Options
Perpetual Futures/Swaps: Engage in the most dynamic markets with up to 10x leverage. Drift Protocol allows for indefinite holding of positions, catering to a broad range of trading strategies.
Spot Trading: Trade a variety of assets with up to 5x leverage. This feature is designed for those who prefer trading the actual underlying assets rather than derivatives.
Token Swaps: Swap any token pair with up to 5x leverage, offering flexibility and efficiency in managing portfolio diversification.
Drift Protocol prioritizes capital efficiency while safeguarding user assets, achieved through a sophisticated cross-margined risk engine. This comprehensive system provides extensive protection against overextending risks, enhancing both the efficiency and safety of trades.

##### 3.4.2 Lending and Borrowing
Integrated Collateral Use: Users can utilize their collateral not only for perpetual futures but also to enhance their trading capacity in spot markets. This integration allows for seamless management of investments and maximized capital efficiency.
Earning through Borrowing: Deposited tokens can earn returns through lending and also serve as collateral for perpetual swaps. Borrowing is tightly regulated, ensuring it only occurs when the collateral levels are sufficiently high to maintain safety measures.

##### 3.4.3 Yield Opportunities
Lend/Borrow Mechanism: Earn competitive yields on your deposits through lending activities within the platform.
Insurance Fund Staking: Stake your assets in a dedicated vault to earn yields derived from exchange fees, providing an additional stream of income.
Market Maker Rewards: Participate in the Alpha Program exclusively for market makers to receive rewards for providing market liquidity.
Backstop AMM Liquidity (BAL): Offer liquidity with the advantage of leverage in specialized pools and earn yields. This advanced feature supports the platform's liquidity needs, particularly in volatile market conditions.

##### 3.4.4 Safety and Security Features
Cross-Margined Risk Engine: Protects traders by pooling risks across multiple positions, thus minimizing the likelihood of liquidations and enhancing overall trading stability.
Safety Protocols for Borrowing: Ensures that borrowers maintain a higher collateral level than required for their positions, providing robust protection against market downturns and reducing systemic risk.

#### 3.5 Market Positioning
Perpetual trading, a derivative market that allows traders to hold positions without an expiration date, has traditionally been dominated by centralized exchanges (CEXs). However, the emergence of Decentralized platforms like Drift are shifting the landscape from CEX-dominated futures trading by offering decentralized perpetual trading protocols and leverage spot trading. 

![Image](https://github.com/user-attachments/assets/5bc0aaeb-cc92-43c9-9725-fcaca440af60)

## 4. Operational Framework
#### 4.1 Drift Automated Market Makers (AMMs)
Drift v1 AMM:
Dynamic Automated Market Maker (DAMM): Improved upon the concept of Perpetual Protocol's virtual AMM (vAMM). It features configurable parameters including:
Peg: Acts as a price multiplier.

K: Modulates liquidity depth.

Fee Pool: Consists of accumulated taker fees, with provisions for future fee discount structures.

Fee Tranches: Allocations from the fee pool are used for operational adjustments such as peg readjustment and liquidity depth modifications.

Drift v2 AMM:
Continues using a constant product formula but incorporates enhancements like:
Backstop AMM Liquidity (BAL): Provides concentrated liquidity.

Dynamic Spread/Peg: Automatically adjusts before trade execution based on inventory levels and market volatility.
Inventory Adjusted Spreads: Different prices for buys and sells based on the current inventory, using a model that adjusts the bid/ask spread dynamically.

![Image](https://github.com/user-attachments/assets/d5ec772d-3cc0-42b4-9201-6a8487d5761f)

#### 4.2 Decentralized Orderbook (DLOB)
Functionality:
Keeper Bots: Manage the decentralized orderbook by monitoring, storing, and executing limit orders. They organize orders by price and age, prioritizing older and larger orders to enhance market efficiency.

Order Matching: Executes limit orders against each other or the AMM based on trigger conditions.

Order Construction: Keepers build an off-chain orderbook from on-chain data, optimizing computational efficiency and scalability.

![Image](https://github.com/user-attachments/assets/5abd01e2-1532-4d49-ba5a-ece0c04c4e37)

#### 4.3 Keeper Incentives:
Keepers earn fees for each transaction they facilitate, aligning their incentives with efficient market operation and user benefit.
Future Enhancements: Drift plans to track and reward consistent performance among Keepers to encourage reliability and competitive service offerings.

#### 4.4 Just-in-Time (JIT) Auctions
Mechanism:
Provides liquidity from market makers in a short, predetermined auction window, enhancing the immediacy and competitiveness of liquidity provision.
Auction Dynamics: Start at a more favourable price and progressively adjust to a predetermined end price, promoting competitive bidding among market makers.

![Image](https://github.com/user-attachments/assets/560cc405-1301-4b0c-8cbc-e3ff8bdf9be5)


#### 4.5 Liquidity Provision Strategies
##### Passive Liquidity Provision:

Backstop AMM Liquidity (BAL): Addresses on-chain limitations like transaction speed and computational capacity by offering a robust liquidity reserve.
Constant Liquidity: Ensured through the AMM, which adjusts liquidity based on a constant product formula and the current inventory levels.
Limit Orderbook Liquidity (DLOB): Complemented by Keeper-managed limit orders, providing depth and stability to the market.

##### Revenue and Insurance Fund Management:

Revenue Pool: Accumulates fees from various activities within the platform, such as borrow fees, exchange fees, and liquidations.
Insurance Fund: Part of the revenue pool is periodically directed to the insurance fund to provide additional security and stability, with mechanisms in place to cap contributions based on market conditions and insurance fund needs.



## 5. Key Highlights
#### 5.1 Advanced On-Chain Trading with Leverage
Drift Protocol enables on-chain trading of cryptocurrencies with up to 10x leverage, enhancing the potential for significant returns. Traders can engage in both perpetual swaps and spot trading, taking long and short positions on a variety of assets including SOL, BTC, ETH, USDC, XRP, and BONK. This range of options caters to diverse trading strategies and risk appetite.

#### 5.2 Automatic Yield on Deposits
By depositing assets into Drift Protocol, users automatically earn yields through the protocol’s liquidity provision mechanisms. The interest earned on these deposits vests and compounds over time, offering what is often referred to as "yield on yield." This system not only enhances the returns for liquidity providers but also strengthens the overall liquidity of the platform.

#### 5.3 Advanced Liquidity Mechanisms
Drift Protocol employs a sophisticated blend of liquidity mechanisms designed to optimize market efficiency and encourage participation:

Just-in-Time (JIT) Liquidity: Triggered by market orders, it initiates a Dutch auction where market makers bid to provide liquidity, ensuring minimal slippage for traders.

Drift Automated Market Maker (Drift AMM) Liquidity: Acts as a fallback liquidity provider when no market makers are available to fill an order. Drift’s v2 AMM enhances traditional AMM mechanics with external Backstop AMM Liquidity (BAL), dynamic spreads, and oracle-based live pricing. The AMM dynamically adjusts bid/ask prices based on inventory and live market conditions, improving price accuracy and trade efficiency.

Decentralized Orderbook (DLOB) Liquidity: Unlike traditional automated market makers, the DLOB allows for the direct matching of limit orders by Keepers. The Keeper Bots on Drift Protocol match open orders with various on-chain liquidity mechanisms once they cross or meet their trigger condition. These scenarios include taker auction against taker auction, taker/maker limit orders against taker auction, maker limit orders against taker limit orders, and taker/maker orders against Drift's AMM.

#### 5.4 Innovative Pricing and Risk Management
Drift Protocol integrates a novel oracle-based pricing system that recalibrates and adjusts spreads based on real-time market conditions such as volatility and inventory levels. This dynamic pricing mechanism is crucial for enabling effective arbitrage, which in turn helps maintain market stability and liquidity.

#### 5.5 User Growth and Volume
Protocols see a drop in their usage and momentum after airdrop but Drift Protocol saw highest volume week post-airdrop, without points and a live rewards program.

![Image](https://github.com/user-attachments/assets/9263d000-f5f1-4e65-bd22-578f3ddaec56)

## 6. Perpetuals (Perp) Trading Metrics Analysis

### 6.1 Total Value Locked (TVL) and Utilization Insights:
TVL Notional: The Total Value Locked across various perpetual markets has reached $316M. Notably, iSolOSL and SOL markets represent the most significant portions with $140M and $55.1M respectively. These figures suggest a strong investor confidence and a deep liquidity pool in these specific assets.

Utilization Trends: The utilization rate for USDC stands out at 71.8%, which might indicate a robust leveraging of assets compared to other currencies like SOL at 28.4% and ETH at 5.8%. Such a high utilization rate could reflect an aggressive use of capital, possibly driving higher returns or increased market activity.

#### 6.2 Market Performance and Risk Management:
Borrow/Lend TVL Notional: This metric highlights the scale of financial engagement and risk exposure within the perpetual markets. The maintenance of balanced notional values across different assets suggests effective risk dispersion and capital utilization.

Withdraw and Borrow Limits: The limits set for withdrawals and borrows appear prudent, ensuring the market's liquidity is not overly strained. This strategic limitation likely helps in mitigating potential liquidity crises and maintaining market stability.

#### 6.3 Spot Trading Metrics Analysis
USDC Spot Market Dynamics:

Rates Analysis: The lending rate of 18.3% alongside a borrowing rate of 25.7% for USDC signifies a lively lending market. These rates could be attracting a substantial volume of traders looking to capitalize on leveraging opportunities, thereby increasing market liquidity and activity.

Total Deposits and Borrows: With $82.63M in deposits and $59.28M in borrows, there's a clear indication of a vibrant trading environment. The considerable gap between deposits and borrows might also point to a conservative yet active borrowing behavior, maintaining healthy liquidity levels.

Asset Flow and Operational Health:

Asset Price Stability: The relatively stable asset price movements provide a foundation for steady trading conditions. This stability is crucial for maintaining trader confidence and fostering a predictable trading environment.

Liquidity Risk Management: The established withdrawal limits are indicative of a well-calibrated risk management framework. These limits are essential for preventing sudden liquidity shortages and ensuring the platform can respond effectively to market demands.

## 7. Revenue Dynamics of Drift Protocol
#### 7.1 Overview of Revenue Streams
Drift Protocol leverages diverse revenue streams to maintain a robust and financially sustainable platform. The primary sources include:
Trading Fees: Collected on each trade executed on the platform, these fees cover operational costs and contribute significantly to the ecosystem's sustainability.

Liquidation Fees: Imposed when positions are forcibly closed due to insufficient margin, these fees compensate for the risk taken on by the protocol during liquidations.

Maker and Taker Fees: Designed to incentivize liquidity on the platform, where makers, who add liquidity, typically incur lower fees than takers, who remove liquidity.

Borrow Fees: A portion of interest earned is allocated to the insurance fund to secure the protocol. 

#### 7.2 Detailed Revenue Analysis
Annualized Revenue: As shown in the latest financial snapshot, Drift Protocol has generated an annualized revenue of $20.19 million, based on the rolling 7-day revenue, highlighting strong performance and growth potential.

Monthly Revenue: The platform has seen a substantial month-on-month revenue growth of 7.13%, with a recent monthly increase of $1.82 million, signaling robust platform activity and increasing user engagement.

#### 7.3 Revenue Growth Trends
The revenue growth chart indicates a steady upward trajectory, affirming the platform's expanding financial base and successful monetization strategies.

#### 7.4 Revenue Distribution by Market
Revenue Per Market: Analysis shows that SOL-PERP is the largest revenue contributor at 39%, followed by BTC-PERP at 10%, and USDC IF at 9%. This diversity in revenue sources underscores the platform's broad appeal and ability to monetize various trading instruments effectively.

Market-specific Revenue: The platform efficiently captures profits from different markets, with the largest profits reported in SOL-PERP and BTC-PERP, indicating high trading volume and engagement in these markets.

## 8. How Trading Works on Drift Protocol
#### 8.1 Trading Process:
Opening a Position: Users begin by depositing collateral and selecting their desired leverage to establish a trade position.

Placing Orders: Trades can be executed by choosing to take long or short positions. Additional order types like stop-loss and take-profit help manage risks.

Margin Maintenance: To avoid liquidation, traders must monitor and maintain adequate margin levels based on market movements.

Earning Funding Payments: Traders either pay or receive funding payments, which are swaps between long and short positions to anchor the perceptual futures prices to the spot market.

Closing a Position: Traders can close their positions at any time to realize gains or curtail losses.

## 9. Technical Breakdown
#### 9.1 Architecture Overview
Drift Protocol's architecture integrates advanced decentralized trading features on Solana. 
It combines a low-slippage, low-fee decentralized exchange (DEX) with an Automated Market Maker (AMM) that ensures constant liquidity through dynamic bid-ask spreads. 
Additionally, a Decentralized Orderbook (DLOB) managed by Keeper Bots efficiently sorts and executes on-chain limit orders. 
Just-in-Time (JIT) Auctions further enhance liquidity by conducting short-term auctions to fill market orders optimally. This comprehensive setup delivers an efficient and seamless trading experience for users.
This architecture is designed to be inherently scalable, secure, and efficient, meeting the needs of complex DeFi applications while maintaining high-security standards.

#### 9.2 Cross-Margined Risk Engine
Drift Protocol features an advanced cross-margined risk engine that enhances asset management across various financial activities:
Efficient Asset Utilization: The engine allows users to leverage their collateral in diversified operations such as lending, borrowing, and trading in perpetual futures.
Robust Risk Management: With built-in safeguards, the engine limits excessive risk exposure, thereby protecting user assets from potential market volatilities and financial instabilities.
Versatility and Flexibility: The protocol supports multiple use cases, allowing participants to maximize yield generation opportunities while effectively managing risk.
User-Centric Design: Drift Protocol places a strong emphasis on user safety and satisfaction by providing a sophisticated risk management framework that fosters trust and stability within the ecosystem.


## 10. Drift Tokenomics
DRIFT Token Role: Facilitates governance, staking, and operational incentives within the Drift ecosystem.

DAO Structure: Includes Realms DAO, Security Council, and Futarchy DAO for comprehensive governance.

#### 10.1 Key Metrics of $DRIFT (as of June, 2024)
Circulating Supply: 150,127,785

Total Supply: 1,000,000,000

Max Supply: 1,000,000,000

Market Cap: $77,984,177

Total Value Locked (TVL): $375.85M

Cumulative Users: 191,927

Cumulative Trading Volume: $28.02 billion

Total Trades: 18,191,257

All-time High: $1.25

Yearly Increase: 381.36%

#### 10.2 Governance Token Distribution

##### Tokenomics:
A total of 1 billion DRIFT governance tokens will be distributed over a span of 5 years, with a significant portion (over 50%) being allocated to the community to foster growth and active participation.
Distribution breakdown:

Community: 53% — This encompasses a diverse range of stakeholders from stakers to algorithmic traders. This allocation is dedicated to the growth of active users on Drift, through trading rewards, future airdrops, and rewards for providing liquidity.

Ecosystem Development and Trading Rewards: 43% — This category includes funding for developers and public awareness campaigns to broaden Drift's usage.

Launch Airdrop: 10% — Reserved for the initial launch phase, distributed to existing Drift users in recognition of their contributions to the platform.

Protocol Development: 25% — Dedicated to future contributors for the development of Drift Protocol tooling, products, and infrastructure.

Strategic Participants: 22% — Represents the contributions of key partners and advisors who have supported the development of critical infrastructure.

![Image](https://github.com/user-attachments/assets/d3c5d025-5556-431e-bfd9-fcc66cb6309f)

Token Emission Schedule: DRIFT emissions follow a 5-year plan, after which all tokens will be fully circulating, with the majority allocated to ecosystem growth.

## 11. Drift DAO Foundation
The Foundation will facilitate the coordination of decisions and initiatives from the token holders and the DAO.

The DAO administrator will be Webslinger, a leading advisory firm for crypto projects. The Foundation will be led by independent Director Matt Shaw and will provide transparency reports to ensure accountability.

## 12. Drift DAO
#### 12.1 Multi-Branch Structure:
Realms DAO: Responsible for general protocol development; elects members of the Security Council via DAO votes; manages future tokenomics updates and rewards for contributing to Drift Protocol.

Security Council: Monitors and updates risk parameters including fees, maintenance margin ratios, and program upgrades; responsible for approving new markets and changes to existing conditions.

Futarchy DAO: Funds ecosystem projects and grants related to Drift, operating under a futarchy model where decisions are based on the time-weighted average prices of a conditional market.

## 13. Funding and Partnerships
#### 13.1 Strategic Collaboration and Capital Infusion
Funding Rounds: Drift Protocol has successfully secured funding from prominent venture capitalists . VCs that have invested in Drift Protocol include well-known names such as Polychain Capital, Bixin Ventures, Folius Ventures, Ethereal Ventures, Raj Gokal, Anatoly Yakovenko,Multicoin Capital, Jump Capital, Robot Ventures, QCP Capital, Jason choi and others.

Drift raised $3.80 million in its first round of funding in 2021. Afterward, they completed a second round of fundraising. In 2023, they secured $23.5 million in a Series A round from early-stage venture capitalists.

Strategic Partnerships: Drift Protocol has forged strategic partnerships with leading blockchain projects and technology providers to enhance its offerings and expand its market reach.

These partnerships may involve collaboration on product development, integration of technologies, joint marketing efforts, or other mutually beneficial activities.

Examples of strategic partners may include prominent blockchain platforms like Ethereum, Solana, or Binance Smart Chain, as well as DeFi infrastructure providers, liquidity providers, or oracle services.

## 14. Conclusion
Drift Protocol has established itself as a leader in the DeFi ecosystem by offering advanced trading features and leveraging Solana's high-speed blockchain. 
Its innovative use of perpetual swaps, dynamic liquidity mechanisms, and sophisticated risk management tools cater to both traders and developers. 

The protocol's significant growth in trading volume, user base, and total value locked highlights its strong market position.
With a focus on decentralization and community governance through the DRIFT token, Drift Protocol is well-positioned for sustainable and inclusive growth in the decentralized trading landscape.
