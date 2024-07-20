# Minimizing-Fixed-Asset-Portfolio

The purpose of this program is to identify the lowest cost portfolio that matches the required cash flows utilizing linear programming/optimization. As one cannot precisely match the dates, one may assume that any cash paid prior to the required date can be used on that date. There is no interest paid on cash positions (if you are paid 1 month prior to needing the cash, you do not receive any interest).

The inputs should be the settlement date, a csv file of bond prices downloaded from the Treasury Direct website (https://www.treasurydirect.gov/GA-FI/FedInvest/selectSecurityPriceDateLinks) and a csv file of cash flows.

The output is a csv file with two columns of data. The first array is the CUSIPs of the bonds and the second array is the principal amounts of those bonds. The first row is the headings CUSIP, Principal.

Several sets of sample cash flows to work with and one set of bond prices have been provided.

The bond price data is downloaded from https://www.treasurydirect.gov/GA-FI/FedInvest/selectSecurityPriceDate. It is saved as a CSV file without headers. The columns are:

- CUSIP (a unique identifier for the bond)
- Security Type: We are only interested in MARKET BASED BILL, MARKET BASED NOTE and MARKET BASED BOND. Ignore other types
- Rate: The coupon rate on the bond
- Maturity Date: The maturity date for the bond
- Call Date: Always blank as Treasuries are not callable
- Buy: The price at which one buys the instrument. You are buying so you want to use this price.
- Sell: The price at which one sells the instrument. You can ignore this.

The sample cash flow files have headers. The first column is the date of the cash flow and the second is the cashflow amount.
