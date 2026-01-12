# Background: Recommended Reading List

> Systematically learning quantitative trading requires spanning multiple fields: finance, statistics, machine learning, and programming. This book list is arranged by learning sequence and difficulty.

---

## About This Book

**"AI Quantitative Trading: From Zero to One"** was written specifically to lower this learning barrier.

I've extracted the most core and practical content from the classic works listed below, combined it with the modern perspective of multi-agent architecture, and reorganized it in a story-driven, code-optional way. Whether you want a quick introduction or a systematic understanding of the full landscape of quantitative trading, this book can serve as your first stop—after reading it, you can dive deeper into the specialized works below based on your interests.

Of course, in today's fast-paced society, personal time and energy may not allow for reading all these materials. My book approaches from the essence and key points, driven by new technology frameworks of AI and agents, which essentially simplifies some traditional old concepts and steps that can be revolutionized. Of course, this is subjective.

---

## 1. Essential Beginner Reading

### 1.1 Quantitative Trading Introduction

**"Quantitative Trading" - Ernest P. Chan**
- Difficulty: Beginner
- Content: Building quantitative strategies from scratch
- Characteristics: Highly practical, complete code
- Suitable for: Beginners with programming background

**"Algorithmic Trading" - Ernest P. Chan**
- Difficulty: Beginner-Intermediate
- Content: Strategy development, backtesting, live trading
- Characteristics: Second book in Chan's trilogy
- Suitable for: Developers with some experience

### 1.2 Financial Markets Fundamentals

**"A Random Walk Down Wall Street" - Burton Malkiel**
- Difficulty: Beginner
- Content: Market efficiency, investment philosophy
- Characteristics: Classic work, easy to read
- Suitable for: Everyone

**"The Intelligent Investor" - Benjamin Graham**
- Difficulty: Beginner
- Content: Value investing principles
- Characteristics: Recommended by Buffett
- Suitable for: Understanding investment fundamentals

---

## 2. Core Advanced Reading

### 2.1 Marcos López de Prado Trilogy

**"Advances in Financial Machine Learning"**
- Difficulty: Advanced
- Content: Correct application of ML in finance
- Key Chapters:
  - Financial data structures
  - Label design (Triple Barrier)
  - Meta-Labeling
  - Cross-validation pitfalls
  - Feature importance
- Characteristics: Industry's most recognized quantitative ML book
- Must-read index: ⭐⭐⭐⭐⭐

**"Machine Learning for Asset Managers"**
- Difficulty: Intermediate-Advanced
- Content: ML in asset allocation
- Characteristics: More asset management perspective
- Suitable for: Portfolio managers

**"Machine Learning for Factor Investing"**
- Difficulty: Advanced
- Content: Factor investing + ML
- Characteristics: Deep theory
- Suitable for: Factor researchers

### 2.2 Statistics and Time Series

**"Analysis of Financial Time Series" - Ruey S. Tsay**
- Difficulty: Advanced
- Content: Financial time series analysis
- Core: ARIMA, GARCH, volatility modeling
- Characteristics: Statistical perspective, math-heavy
- Suitable for: Those with statistics background

**"Elements of Statistical Learning" - Hastie, Tibshirani, Friedman**
- Difficulty: Advanced
- Content: Statistical learning methods
- Characteristics: ML bible
- Suitable for: Building theoretical foundations

---

## 3. Strategy Topics

### 3.1 Momentum and Trend

**"Following the Trend" - Andreas Clenow**
- Difficulty: Intermediate
- Content: Trend following strategies
- Characteristics: Practical code, futures perspective
- Suitable for: Trend strategy developers

**"Stocks on the Move" - Andreas Clenow**
- Difficulty: Intermediate
- Content: Momentum strategies for stocks
- Characteristics: Complete strategy implementation
- Suitable for: Stock strategy developers

### 3.2 Mean Reversion and Arbitrage

**"Statistical Arbitrage" - Andrew Pole**
- Difficulty: Advanced
- Content: Statistical arbitrage strategies
- Characteristics: Deep theory
- Suitable for: Arbitrage strategy research

**"Pairs Trading" - Ganapathy Vidyamurthy**
- Difficulty: Intermediate
- Content: Pairs trading strategies
- Characteristics: Cointegration analysis detailed
- Suitable for: Pairs trading development

### 3.3 Options and Volatility

**"Option Volatility and Pricing" - Sheldon Natenberg**
- Difficulty: Intermediate
- Content: Option pricing and volatility
- Characteristics: Must-read for options traders
- Suitable for: Options strategy development

**"Volatility Trading" - Euan Sinclair**
- Difficulty: Intermediate-Advanced
- Content: Volatility trading strategies
- Characteristics: Practice-oriented
- Suitable for: Volatility traders

---

## 4. Execution and Market Microstructure

**"Algorithmic and High-Frequency Trading" - Cartea, Jaimungal, Penalva**
- Difficulty: Advanced
- Content: Algorithmic trading theory
- Characteristics: Mathematically rigorous
- Suitable for: Execution algorithm research

**"Trading and Exchanges" - Larry Harris**
- Difficulty: Intermediate
- Content: Market microstructure
- Characteristics: Exchange operations detailed
- Suitable for: Understanding market mechanisms

**"Market Microstructure Theory" - Maureen O'Hara**
- Difficulty: Advanced
- Content: Microstructure theory
- Characteristics: Academic classic
- Suitable for: Theoretical research

---

## 5. Reinforcement Learning

**"Reinforcement Learning: An Introduction" - Sutton & Barto**
- Difficulty: Intermediate-Advanced
- Content: RL fundamentals
- Characteristics: RL bible, free online
- Suitable for: All RL learners
- Link: http://incompleteideas.net/book/the-book.html

**"Deep Reinforcement Learning Hands-On" - Maxim Lapan**
- Difficulty: Intermediate
- Content: Deep RL practice
- Characteristics: Code-oriented
- Suitable for: Practitioners

---

## 6. Programming and Engineering

**"Python for Finance" - Yves Hilpisch**
- Difficulty: Intermediate
- Content: Python finance programming
- Characteristics: Comprehensive and practical
- Suitable for: Python developers

**"Hands-On Machine Learning" - Aurélien Géron**
- Difficulty: Intermediate
- Content: ML practice guide
- Characteristics: Scikit-learn + TensorFlow
- Suitable for: ML engineers

---

## 7. Risk Management and Capital Management

### 7.1 Capital Management (Top Priority)

> **Van K. Tharp's view**: Capital management accounts for at least 50% in real trading. No matter how good the strategy, improper position management will blow up the account.

**"Trade Your Way to Financial Freedom" - Van K. Tharp**
- Difficulty: Intermediate
- Content: Complete trading system design
- Key Chapters:
  - Position Sizing: Deciding how much to invest per trade
  - Expectancy: The true meaning of win rate × risk-reward ratio
  - R-Multiple: Measuring returns in risk units
  - System development process
- Characteristics: **Extremely practical, transforms trading thinking**
- Must-read index: ⭐⭐⭐⭐⭐
- Suitable for: All traders (more important than strategy books)

**"The Definitive Guide to Position Sizing" - Van K. Tharp**
- Difficulty: Intermediate-Advanced
- Content: In-depth guide to position management
- Core:
  - Fixed Fractional method
  - Fixed Ratio method
  - Kelly formula and its limitations
  - Risk Parity
- Characteristics: Position management monograph, rich details
- Suitable for: Advanced readers who finished the previous book

**Van K. Tharp's Core Formulas**:

```
Expectancy = (Win Rate × Average Win) - (Loss Rate × Average Loss)

R-Multiple = Actual Profit/Loss / Initial Risk (stop-loss distance)

Position Size = Account Risk Percentage / Single Trade Risk
             = (Total Capital × 2%) / (Entry Price - Stop Loss Price)
```

**Why Capital Management is Most Important**:
- Strategy win rate 60%, but poor position management → Losses
- Strategy win rate 40%, but proper position management → Profits
- The key is not "how many times you're right," but "how much you make when right, how little you lose when wrong"

### 7.2 Portfolio Management

**"Active Portfolio Management" - Grinold & Kahn**
- Difficulty: Advanced
- Content: Active portfolio management
- Core: Information ratio, Alpha decomposition
- Characteristics: Must-read for institutional investors

**"Quantitative Risk Management" - McNeil, Frey, Embrechts**
- Difficulty: Advanced
- Content: Risk measurement and management
- Characteristics: Rigorous theory
- Suitable for: Risk managers

### 7.3 Trading Psychology

**"Trading in the Zone" - Mark Douglas**
- Difficulty: Beginner-Intermediate
- Content: Trading psychology
- Core: Probabilistic thinking, emotion control
- Characteristics: Must-read for mindset building
- Suitable for: All traders

**"Market Wizards" series - Jack Schwager**
- Difficulty: Beginner
- Content: Top trader interviews
- Characteristics: Understanding the real trading world
- Suitable for: Finding your own style

---

## 8. Recommended Reading Order

### Beginner Path (6-12 months)

```
Phase 1 (Fundamentals)
├── Random Walk Down Wall Street
├── Quantitative Trading (Chan)
└── Python for Finance

Phase 2 (Capital Management - Most Important!)
├── Trade Your Way to Financial Freedom ⭐ (Van K. Tharp)
└── Trading in the Zone (Mark Douglas)

Phase 3 (Strategy)
├── Following the Trend
├── Stocks on the Move
└── Algorithmic Trading (Chan)

Phase 4 (Advanced)
├── Advances in Financial Machine Learning ⭐
└── Analysis of Financial Time Series
```

> **Important**: Many people skip Phase 2 and go straight to strategy research—this is the most common mistake. Capital management determines survival; strategy is just icing on the cake.

### Machine Learning Path (3-6 months)

```
├── Elements of Statistical Learning
├── Hands-On Machine Learning
├── Advances in Financial Machine Learning ⭐
└── Reinforcement Learning (Sutton)
```

### High-Frequency/Execution Path (6-12 months)

```
├── Trading and Exchanges
├── Market Microstructure Theory
└── Algorithmic and High-Frequency Trading
```

---

## 9. Online Resources

### 9.1 Papers

- **SSRN**: https://www.ssrn.com (Financial research papers)
- **arXiv q-fin**: https://arxiv.org/list/q-fin/recent
- **Journal of Portfolio Management**

### 9.2 Blogs

- **Quantocracy**: Quantitative blog aggregator
- **QuantStart**: Strategy tutorials
- **Ernie Chan's Blog**: Author's blog

### 9.3 Courses

- **Coursera - Machine Learning (Andrew Ng)**
- **Coursera - Financial Engineering and Risk Management**
- **DataCamp - Finance with Python**

---

## 10. Reading Recommendations

1. **Don't skip fundamentals**: Read beginner books before advanced ones
2. **Practice while reading**: After each chapter, implement in code
3. **Re-read classics**: López de Prado's books are worth reading multiple times
4. **Stay skeptical**: Any strategy may become obsolete
5. **Theory + Practice**: Alternate between theoretical and practical books

---

> **Core principle**: Books are just the starting point; real learning comes from practice. After finishing a book, whether you can implement its contents in code is the true test of learning effectiveness.
