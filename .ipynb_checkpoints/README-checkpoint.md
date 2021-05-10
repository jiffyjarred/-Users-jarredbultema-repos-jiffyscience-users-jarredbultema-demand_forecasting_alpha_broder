# Alpha Broder Demand Forecasting
May 10, 2021

### Goal:
- Generate 12-month forecasts for demand of variant-region or variant-category-region for products that we sell from Alpha Broder
- Weekly or daily granularity has benefits over monthly
- We will post-process total demand to allocate AB sales target. We don't want to include existing allocation logic or splits data to understand only historical demand fulfill by AB. Rather, we want total demand of the styles they sell
- A business goal is to partner more directly with AB, provide granular forecasts that allow for generation of JS sales targets as part of an incentive/discount program
- We will plan to scale out this type of work to our other suppliers as well, and all items we sell

### Plan of Attack:
1. Get the data
2. Basic EDA (use TS helpers)
3. Cluster series (us TS helpers and/or hierarchical clustering from roll_package)
4. Use DR to do quick segmented modeling (basic parameters)
5. Evaluate performance
6. Look at insights to determine where we might want additional data types or feature engineering

### Other comments:
1. Functionalize this work so it's easily repeatable and/or rolled into a package later
2. Use the JiffyPy package for relevant functionality
2. Quick turnaround needed (5/14) for initial results that are good enough to send to supplier
3. Focus on DR-replacement for this workflow if possible
4. Don't worry too much about cold-starts, but be on the lookout for that stuff in the data