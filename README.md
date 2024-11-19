# Portfolio Risk Analysis Framework - PUBLIC VERSION
A sophisticated quantitative framework combining Monte Carlo simulation, machine learning, and advanced risk metrics, developed as part of a project for the class "Data Science & Advanced Programming, Year 1, MscF HEC Lausanne".

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-Commercial-red.svg)](LICENSE)

## 🚀 Overview

This framework provides a comprehensive solution for portfolio risk analysis by combining state-of-the-art quantitative methods:

- **🤖 Machine Learning Integration**: 
  - Advanced regime detection using Gaussian Mixture Models
  - Pattern recognition for market states
  - Dynamic feature engineering

- **⚡ High-Performance Monte Carlo**: 
  - GPU-accelerated simulations
  - Parallel processing capabilities
  - Efficient memory management

- **📊 Dynamic Risk Management**:
  - Real-time portfolio optimization
  - Continuous risk monitoring
  - Adaptive risk thresholds

- **🔄 Market Microstructure**: 
  - Transaction cost modeling
  - Market impact analysis
  - Liquidity considerations

## 🏗️ Architecture

```mermaid
graph TD
    A[Market Data] --> B[Data Pipeline]
    B --> C[Feature Engineering]
    C --> D[Risk Engine]
    D --> E[Portfolio Optimizer]
    E --> F[Risk Analytics]
    F --> G[Reporting Layer]
    
    B --> H[Market Regime Detection]
    H --> D
    
    I[Alternative Data] --> B
    J[Real-time Feeds] --> B
```

## 🔧 Core Components

### 1. Market Analysis Engine
- GMM-based regime detection
- GARCH volatility forecasting
- Dynamic feature extraction
- Real-time market state analysis

### 2. Advanced Risk Metrics
- Conditional Value at Risk (CVaR)
- Expected Shortfall (ES)
- Maximum Drawdown (MDD)
- Conditional Drawdown at Risk (CDaR)
- Omega Ratio
- Modified Sharpe Ratio

### 3. Monte Carlo Engine
- Parallel simulation processing
- GPU acceleration support
- Regime-aware scenario generation
- Efficient path calculations

## 📦 Installation

### Prerequisites
- Python 3.8+
- CUDA toolkit (optional, for GPU support)
- Virtual environment (recommended)

```bash
# Create virtual environment
python -m venv venv

# Activate environment
source venv/bin/activate  # Unix/macOS
.\venv\Scripts\activate  # Windows

# Install dependencies
pip install -r requirements.txt
```

### Dependencies
```python
# Core Libraries
numpy>=1.21.0
pandas>=1.3.0
scipy>=1.7.0
scikit-learn>=0.24.2

# Machine Learning
torch>=1.9.0
pymc3>=3.11.0
arch>=4.19

# Visualization
matplotlib>=3.4.0
seaborn>=0.11.0
plotly>=5.1.0
dash>=2.0.0

# Development
pytest>=6.2.5
black>=21.7b0
flake8>=3.9.0
mypy>=0.910
```

## 📚 Mathematical Foundation

### Return Calculation
$$R_t = \frac{P_t - P_{t-1}}{P_{t-1}}$$

### Portfolio Value Evolution
$$V_t = V_{t-1}(1 + R_t - c|\Delta w_t|)$$

where:
- $V_t$ is portfolio value at time t
- $R_t$ is return at time t
- $c$ is transaction cost
- $\Delta w_t$ is change in position

### Key Risk Metrics
- VaR: $P(R_p \leq VaR_\alpha) = \alpha$
- Sharpe: $SR = \frac{E[R_p] - R_f}{\sigma_p}$
- Maximum Drawdown: $MDD = \min_t{\frac{V_t - \max_{s\leq t}V_s}{\max_{s\leq t}V_s}}$

## 🔬 Implementation Details

### Advanced Features
- Regime-switching models
- Dynamic volatility forecasting
- Transaction cost optimization
- Machine learning-based signal generation
- Real-time portfolio rebalancing

### Performance Optimizations
- Vectorized operations
- GPU acceleration
- Parallel processing
- Memory efficient algorithms

## 🤝 Contributing

### Development Workflow
1. Fork the repository
2. Create a feature branch
3. Install development dependencies
4. Run tests and linting
5. Submit pull request

### Code Standards
- Follow PEP 8 guidelines
- Include comprehensive docstrings
- Add unit tests for new features
- Use type hints consistently

## 📖 References

### Academic Literature
1. Bollerslev, T. (1986). "Generalized Autoregressive Conditional Heteroskedasticity"
2. McNeil, A.J., Frey, R. (2000). "Estimation of Tail-Related Risk Measures"
3. Hamilton, J.D. (1989). "A New Approach to the Economic Analysis of Time Series"
4. Ang, A., Bekaert, G. (2002). "Regime Switches in Interest Rates"

### Key Resources
1. "Advances in Financial Machine Learning" by Marcos López de Prado
2. "Machine Learning for Asset Managers" by Marcos López de Prado
3. "Active Portfolio Management" by Grinold and Kahn

## 📄 License

Commercial Software License

Copyright (c) 2024 Lucas Kemper

**All Rights Reserved**

### Usage Terms:
- **Commercial Use**: Requires paid license
- **Academic/Personal Use**: 
  - Permitted for non-commercial research
  - Must credit original work
  - Cannot be used in production

### Contact
For licensing and commercial use:
- Email: contact@lucaskemper.com
- Website: [www.lucaskemper.com](http://www.lucaskemper.com)

---
**Note**: This project is under active development. Features and documentation may be updated frequently.
