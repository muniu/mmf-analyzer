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
git clone git@github.com:muniu/mmf-analyzer.git
cd mmf-analyzer
```

2. Prepare fund data file (funds_data.json):
```json
{
    "funds": [
        {
            "name": "Fund Name",
            "rate": "16.91",
            "mgt_fee": "0.85",
            "minimum_investment": "1000"
        }
    ]
}
```

3. Run the analyzer:
```bash
python mmf_analyzer.py funds_data.json
```

## Data File Requirements
The tool requires a JSON file containing fund information with the following structure:
- `name`: Fund name (string)
- `rate`: Annual interest rate (decimal)
- `mgt_fee`: Management fee percentage (decimal)
- `minimum_investment`: Minimum investment amount in KES (decimal)

## Usage
1. Provide a valid fund data JSON file when running the tool
2. The tool will prompt you for:
   - Initial Capital (must meet minimum investment requirements)
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

## Assumptions

### Interest Rate Assumptions
- Interest rates remain constant throughout the investment period
- Current advertised rates are used for the entire duration
- No market fluctuations or rate changes are considered
- Interest is earned on every calendar day

### Timing and Transaction Assumptions
- Monthly contributions are made at the start of each month
- No delays in contribution processing
- No missed contributions
- No partial withdrawals are allowed
- All dividends are automatically reinvested

### Fee Structure Assumptions
- Management fees are constant percentages
- Fees are calculated and charged monthly based on average balance
- No additional transaction fees or charges are considered
- No fee structure changes during the investment period
- No account opening, statement, or service charges

### Calendar and Processing Assumptions
- Interest is earned on all calendar days
- No distinction between business days and weekends
- Bank holidays are not considered in calculations
- No settlement or processing delays
- No deposit processing delays

### Tax Treatment Assumptions
- Withholding tax rate remains constant
- Tax is applied uniformly to all interest earned
- No tax exemptions or special cases are considered
- No changes in tax policy during the investment period

### Risk Considerations
- No credit risk factors included
- No default risk considerations
- No market risk adjustments
- All funds are assumed to be equally secure
- Past performance patterns continue into the future

### Operational Assumptions
- No minimum balance requirements enforced
- No early withdrawal penalties
- No administrative fees
- No account opening fees
- No statement or service charges

### Investment Behavior Assumptions
- All contributions are made as scheduled
- No emergency withdrawals
- Consistent investment behavior throughout the period
- All earnings are reinvested


## Important Note
These assumptions are made for calculation purposes and may not reflect actual market conditions or specific fund policies. Always consult with financial advisors and read fund documentation for actual terms and conditions.


## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.


## License
MIT License - see LICENSE file for details.

## Contact
For questions or suggestions, please open an issue in the GitHub repository.

---
Data Source: [Vasili Africa - Top 15 Money Market Funds in Kenya (August 2023)](https://vasiliafrica.com/top-15-money-market-funds-in-kenya-august-2023/)