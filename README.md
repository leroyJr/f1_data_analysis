## F1 Fantasy Sports and Data Analysis

Investigate the F1 choose 5 drivers + 1 constructor under a budget optimization challenge

### Data

Track and pull data from a number of sites using Selenium.

### Analytics

#### Value

Who is consistently outperforming their value.  What is their actual value, and how much virtual budget is gained by choosing a driver with higher value?

#### Calculate insights:

* What has been the optimal combination of drivers + team to select (and not change) over while constrained to a budget:

  * The entire season
  * The previous 4 races
  * The previous 8 races

#### Looking at optimal combinations, who shows up the most.

As of Netherlands completion (9/5/2022)

| last_name   |   top_25 |   top_50 |   top_100 |   top_200 |   pct_top_25 |   pct_top_50 |   pct_top_100 |   pct_top_200 |
|:------------|---------:|---------:|----------:|----------:|-------------:|-------------:|--------------:|--------------:|
| Leclerc     |       22 |       38 |        72 |       126 |         0.88 |         0.76 |          0.72 |         0.63  |
| Perez       |       15 |       33 |        57 |       105 |         0.6  |         0.66 |          0.57 |         0.525 |
| Verstappen  |       15 |       31 |        63 |       132 |         0.6  |         0.62 |          0.63 |         0.66  |
| Sainz       |       13 |       28 |        48 |        97 |         0.52 |         0.56 |          0.48 |         0.485 |
| Stroll      |       10 |       20 |        34 |        57 |         0.4  |         0.4  |          0.34 |         0.285 |
| Russell     |        8 |       15 |        34 |        68 |         0.32 |         0.3  |          0.34 |         0.34  |
| Ocon        |        8 |       14 |        33 |        66 |         0.32 |         0.28 |          0.33 |         0.33  |
| Magnussen   |        8 |       14 |        24 |        48 |         0.32 |         0.28 |          0.24 |         0.24  |
| Bottas      |        6 |       13 |        25 |        42 |         0.24 |         0.26 |          0.25 |         0.21  |
| Albon       |        7 |       11 |        25 |        44 |         0.28 |         0.22 |          0.25 |         0.22  |
| Alonso      |        4 |       10 |        25 |        49 |         0.16 |         0.2  |          0.25 |         0.245 |
| Schumacher  |        5 |        8 |        17 |        34 |         0.2  |         0.16 |          0.17 |         0.17  |
| Latifi      |        1 |        6 |        12 |        25 |         0.04 |         0.12 |          0.12 |         0.125 |
| Norris      |        1 |        4 |        10 |        31 |         0.04 |         0.08 |          0.1  |         0.155 |
| Vettel      |        2 |        4 |        14 |        39 |         0.08 |         0.08 |          0.14 |         0.195 |
| Zhou        |        0 |        1 |         5 |        17 |         0    |         0.02 |          0.05 |         0.085 |
| Ricciardo   |        0 |        0 |         0 |         0 |         0    |         0    |          0    |         0     |
| Hamilton    |        0 |        0 |         0 |         0 |         0    |         0    |          0    |         0     |
| Tsunoda     |        0 |        0 |         2 |         8 |         0    |         0    |          0.02 |         0.04  |
| Gasly       |        0 |        0 |         0 |        12 |         0    |         0    |          0    |         0.06  |


#### 20/20 Vision
* Hindsight: if you could see the future, what was the optimal selections (best path) for any given race?
* How does a static selection differ from best path?

### Predict

Simulate and predict potential outcomes.

Is past performance, and efficiency any indicator of future performance.  Use a time series split and train models, to predict against races that "haven't happened yet."
