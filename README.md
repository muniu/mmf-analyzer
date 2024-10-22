# Kenyan Money Market Fund (MMF) Analysis Tool

## Overview
A Python-based command-line tool for analyzing and comparing Money Market Funds in Kenya. This tool provides comprehensive analysis of potential returns, taking into account daily interest calculations, management fees, withholding tax, and actual calendar days.

## Features
- Accurate daily interest calculations with monthly compounding
- Real calendar day handling (28/30/31 days per month)
- Management fee impact analysis
- Withholding tax calculations
- Comparative analysis across multiple funds
- Detailed monthly progression tracking
- Comprehensive fund performance comparison

## Requirements
- Python 3.6+
- No additional packages required (uses standard library only)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/mmf-analyzer.git
cd mmf-analyzer
```

2. Run the analyzer:
```bash
python mmf_analyzer.py
```

## Usage
The tool will prompt you for the following inputs:
- Initial Capital (minimum KES 100)
- Monthly Contribution (minimum KES 0)
- Investment Period in months
- Withholding Tax percentage
- Management Fee inclusion preference
- Dividend reinvestment preference

## Sample Output
```
=== Money Market Fund Analysis Tool ===

Initial Capital (KES): 100000
Monthly Contribution (KES): 50000
Investment Period (months): 12
Withholding Tax (%): 15
Include management fees in calculation? (y/n): y
Reinvest dividends? (y/n): y

================================================================================
                          Investment Analysis Results                           
================================================================================

Investment Parameters:
Initial Capital: KES 100,000.00
Monthly Contribution: KES 50,000.00
Investment Period: 12 months
Start Date: October 2024
End Date: October 2025
Withholding Tax: 15.0%
Management Fees: Included
Dividend Reinvestment: Yes

Fund Comparison:
--------------------------------------------------------------------------------------------------------------
Fund Name                               Rate        Final Balance        Interest      Net Return
--------------------------------------------------------------------------------------------------------------
Enwealth Money Market Fund            11.728%       KES 685,774.81   KES 38,696.69           5.50%
GenAfrica Money Market Fund           11.789%       KES 685,606.85   KES 38,893.57           5.48%
Lofty-Corban KSH Money Market Fund    11.712%       KES 685,532.24   KES 38,636.04           5.47%
[... other funds ...]

Monthly Balance Progression (Best Fund):
--------------------------------------------------
October 2024 (31 days): KES 100,000.00
November 2024 (30 days): KES 100,783.19
December 2024 (31 days): KES 151,939.28
[... other months ...]
```

## Key Features Demonstrated in Output
1. **Fund Comparison**: Ranks all funds by performance
2. **Monthly Progression**: Shows balance growth with actual calendar days
3. **Detailed Results**: Includes interest earned, fees paid, and net returns
4. **Comprehensive Notes**: Important considerations and assumptions

## Calculation Methodology
- Interest is calculated daily and compounded monthly
- Management fees are based on average monthly balance
- Returns are shown after applicable withholding tax
- Calculations use actual calendar days per month

## Data Source
Fund data is sourced from [Vasili Africa's August 2023 MMF analysis](https://vasiliafrica.com/top-15-money-market-funds-in-kenya-august-2023/), including:
- Fund rates
- Management fees
- Performance metrics

## Notes and Assumptions
- Interest is calculated daily and compounded monthly
- Returns are shown after withholding tax
- Management fees are deducted monthly (if enabled)
- Calculations account for actual calendar days
- Bank holidays are not considered
- Past performance does not guarantee future returns

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## Disclaimer
This tool is for informational purposes only. Always consult with a qualified financial advisor before making investment decisions.

## License
MIT License - see LICENSE file for details.

## Contact
For questions or suggestions, please open an issue in the GitHub repository.

---
Data Source: [Vasili Africa - Top 15 Money Market Funds in Kenya (August 2023)](https://vasiliafrica.com/top-15-money-market-funds-in-kenya-august-2023/)