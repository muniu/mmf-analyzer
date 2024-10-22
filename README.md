# Kenyan Money Market Fund (MMF) Analysis Tool

## Overview
A Python-based command-line tool for analyzing and comparing Money Market Funds in Kenya. The tool provides detailed calculations of potential returns across different funds, taking into account daily interest calculations, management fees, and withholding tax.

## Features
- Daily interest calculation with monthly compounding
- Management fee considerations
- Withholding tax calculations
- Comparative analysis across multiple funds
- Monthly progression tracking
- Actual calendar day calculations
- Detailed return breakdowns

## Key Functionalities
- Calculate potential returns for multiple MMFs
- Compare fund performance
- Track monthly balance progression
- Account for management fees and taxes
- Handle daily interest calculations
- Consider actual calendar days per month

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/mmf-analyzer.git
cd mmf-analyzer
```

2. Ensure you have Python 3.6+ installed:
```bash
python --version
```

3. No additional packages required (uses standard library only)

## Usage

1. Run the analyzer:
```bash
python mmf_analyzer.py
```

2. Enter the requested information:
- Initial capital
- Monthly contribution
- Investment period
- Tax rate
- Fee inclusion preferences

3. Review the comprehensive analysis, including:
- Fund comparisons
- Monthly progression
- Best performing fund details
- Final results

## Sample Output
```
Investment Analysis Results
==========================

Investment Parameters:
Initial Capital: KES 100,000.00
Monthly Contribution: KES 30,000.00
Investment Period: 12 months
...

Fund Comparison:
Fund Name                               Rate     Final Balance          Interest     Net Return
--------------------------------------------------------------------------------------
GenAfrica Money Market Fund           11.789%    KES 514,800.00    KES 54,800.00      12.45%
...
```

## Data Attribution
The Money Market Fund data used in this tool is sourced from [Vasili Africa's August 2023 MMF analysis](https://vasiliafrica.com/top-15-money-market-funds-in-kenya-august-2023/). The data includes:
- Fund rates
- Management fees
- Minimum investment requirements
- Performance metrics

Last updated: August 2023

## Notes and Assumptions
- Interest is calculated daily and compounded monthly
- Returns are shown after applicable withholding tax
- Management fees are deducted monthly (if enabled)
- Calculations account for actual number of days in each month
- Bank holidays are not considered in the calculations
- Past performance does not guarantee future returns

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer
This tool is for informational purposes only and should not be considered as financial advice. Always consult with a qualified financial advisor before making investment decisions.

## Contact
For questions or suggestions, please open an issue in the GitHub repository.

---
Data Source: [Vasili Africa - Top 15 Money Market Funds in Kenya (August 2023)](https://vasiliafrica.com/top-15-money-market-funds-in-kenya-august-2023/#:~:text=Stepping%20into%20the%20spotlight%20for,or%20invest%20at%20any%20time.)