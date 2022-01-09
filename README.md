# Financial Planners Repository
for emergencies and retirement

---

This application consists of two financial analysis tools: a financial planner to compare current savings in stocks, bonds and cryptocurrencies against an emergency reserve of 3 months monthly salary

```if total_portfolio > emergency_fund_value:
    print('Congratulations! You have enough money saved to set aside an emergency fund.'),
elif total_portfolio == emergency_fund_value:
    print('Congratulations! You have reached an important financial goal.'),
else:
    print(f"You are ${emergency_fund_value - total_portfolio} from reaching this important financial goal.")```

and a financial planner for retirement to forecast performance of a portfolio over 30 years using Monte Carlo simulations.

```MC_thirtyyear = MCSimulation(
  portfolio_data = portfolio_split_df,
  weights = [.40,.60],
  num_simulation = 500,
  num_trading_days = 252*30
)```

## *Technologies*
This application is written using Python 3.9.7 and uses historical data for 2 ETFs tracking the S&P 500 in stocks and a US aggregate bond portfolio. Datasets are collected using Python Requests and the Alpaca API in Pandas DataFrames. Monte Carlos simulations are performed using the MCForecast Tools library for 30 and 10 year projections using different weightings between stock and bond ETFs. 

Cryptocurrency prices are returned using:
```btc_url = "https://api.alternative.me/v2/ticker/Bitcoin/?convert=USD"
   eth_url = "https://api.alternative.me/v2/ticker/Ethereum/?convert=USD"```
   
![Pie chart showing distribution of investments between crypto, stocks and bonds](../financial_planners/portfolio_allocations.pg)

![500 simulations of cumulative portfolio return trajectories over 30 years](../financial_planners/

## *Installation Guide*
Install the pandas, os, requests libraries, the Alpaca Trade API, and Path from the pathlib library, load_dotenv from the dotenv library and MCSimulation from the MCForecastTools library 

## *Usage*
Run the program from the command line as 'financial_planning.py'.

## *Contributors*
This program was written by David Hockenbery with the assistance of the UW FinTech class of 2021 and instructors. Contact David at dhockenb@gmail.com.

## *License*
opyright (c) [2021] [David Hockenbery]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.