# battery_project
Battery Arbitrage Analysis in ERCOT Real-Time Market

### Overview:
This project explores how a battery energy storage system can generate revenue in the ERCOT real-time electricity market through energy arbitrage.
Using historical 15-minute settlement point price data for the Houston Hub (HB_HOUSTON), I built a simple dispatch model to estimate how a battery could charge during low-price periods and discharge during high-price periods.

### The goal of this project is to answer:
How much revenue could a battery generate from energy arbitrage in the ERCOT real-time market?


### Data:
Source: ERCOT Market Data (https://www.ercot.com/mp/data-products/data-product-details?id=np6-785-er&utm_source=chatgpt.com)

Product: Settlement Point Prices (Real-Time Market) 

Location: Houston Hub (HB_HOUSTON)

Resolution: 15-minute data aggregated to hourly

Dates: 2025 and the beggining of 2026 



### Methodology:

#### 1.Data Processing

Combined multiple datasets (2025 and 20026)

Built timestamps from delivery date, hour, and interval

Filtered for HB_HOUSTON

#### 2.Price Aggregation

Converted 15-minute prices into hourly averages

#### 3.Battery Model

Assumed:100 MW power capacity, 400 MWh energy capacity (4-hour duration), 90% round-trip efficiency

Strategy: Charge during lowest-price hours each day, discharge during highest-price hours

#### 4.Revenue Calculation

Daily profit = discharge revenue − charging cost
 
### Results:

Battery revenue is highly variable across days

Most days generate moderate profits

A small number of high-price events drive a large share of total revenue

### Key Insights:

Battery value is strongly tied to price spikes

Revenue is not stable, it is event-driven

A small number of days contribute disproportionately to total profits
 
### Limitations:

Perfect foresight within each day (tbh, not realistic in practice)

No state-of-charge tracking

No participation in ancillary service markets

No degradation or operational constraints
 
### Next Steps (potential improvements include):

Adding state-of-charge (SOC) tracking for realistic dispatch

Incorporating ancillary service revenues

Running sensitivity analysis on battery size and efficiency

Using forecast-based dispatch instead of perfect hindsight

