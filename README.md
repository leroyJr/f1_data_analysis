## F1 Fantasy Sports and Data Analysis

Investigate the F1 choose 5 drivers + 1 constructor under a budget optimization challenge

### Data

Track and pull data from a number of sites using Selenium.

### Analytics

#### Value

Who is consistently outperforming their value.  What is their actual value, and how much virtual budget is gained by choosing a driver with higher value?

##### Driver Points Price
|    | Driver               |   Points Value Price |   Current Price |   Diff |      Mean Points |   Median Points|
|---:|:---------------------|------------:|----------------:|-------------:|---------:|---------:|
|  5 | Leclerc  Ferrari     |    25.8847  |            18.7 |     7.18471  | 28.4     |       23 |
|  1 | Verstappen  Red Bull |    37.3688  |            30.4 |     6.96877  | 41       |       45 |
|  3 | Perez  Red Bull      |    24.0011  |            17.9 |     6.10108  | 26.3333  |       28 |
|  8 | Sainz  Ferrari       |    21.3883  |            17.2 |     4.18831  | 23.4667  |       27 |
|  2 | Russell  Mercedes    |    27.4645  |            23.8 |     3.66453  | 30.1333  |       30 |
| 12 | Stroll  Aston Martin |    11.0587  |             9.1 |     1.95873  | 12.1333  |       11 |
| 10 | Ocon  Alpine         |    14.1576  |            12.3 |     1.8576   | 15.5333  |       19 |
|  4 | Alonso  Alpine       |    13.2462  |            12.7 |     0.546167 | 14.5333  |       14 |
| 11 | Bottas  Alfa Romeo   |    10.0258  |             9.5 |     0.525769 | 11       |       14 |
| 13 | Albon  Williams      |     7.95985 |             7.7 |     0.259853 |  8.73333 |       10 |
| 16 | Magnussen  Haas      |     6.31927 |             6.1 |     0.219272 |  6.93333 |        6 |
| 19 | Norris  Mclaren      |    15.2513  |            15.9 |    -0.648679 | 16.7333  |       17 |
|  7 | Vettel  Aston Martin |    11.0587  |            11.8 |    -0.741273 | 12.1333  |       14 |
| 17 | Schumacher  Haas     |     5.34708 |             6.3 |    -0.952923 |  5.86667 |        5 |
| 15 | Latifi  Williams     |     4.55717 |             6.9 |    -2.34283  |  5       |        8 |
|  6 | Gasly  AlphaTauri    |     8.99281 |            13   |    -4.00719  |  9.86667 |       13 |
| 14 | Zhou  Alfa Romeo     |     4.07107 |             8.1 |    -4.02893  |  4.46667 |        6 |
|  9 | Tsunoda  AlphaTauri  |     3.15964 |             8.4 |    -5.24036  |  3.46667 |       -1 |
|  0 | Hamilton  Mercedes   |    23.8188  |            30.6 |    -6.7812   | 26.1333  |       26 |
| 18 | Ricciardo  Mclaren   |     5.4686  |            14.2 |    -8.7314   |  6       |        5 |

#### Team Points Price
|    | Team         |   Points Value Price |   Current Price |   Diff |      Mean Points |   Median Points|
|---:|:-------------|------------:|----------------:|-------------:|---------:|---------:|
|  1 | Red Bull     |    40.5023  |            32.7 |     7.80231  | 60.7333  |       63 |
|  3 | Ferrari      |    30.988   |            25.8 |     5.18804  | 46.4667  |       47 |
|  2 | Alpine       |    15.4273  |            14.1 |     1.32733  | 23.1333  |       23 |
|  5 | Aston Martin |    12.6709  |            11.8 |     0.870864 | 19       |       20 |
|  0 | Mercedes     |    33.789   |            34.2 |    -0.411029 | 50.6667  |       55 |
|  7 | Williams     |     5.64631 |             6.2 |    -0.553685 |  8.46667 |        8 |
|  8 | Haas         |     5.15726 |             6.4 |    -1.24274  |  7.73333 |        5 |
|  6 | Alfa Romeo   |     6.49104 |             8.6 |    -2.10896  |  9.73333 |        7 |
|  4 | AlphaTauri   |     5.37956 |            10.2 |    -4.82044  |  8.06667 |        6 |
|  9 | Mclaren      |    11.6483  |            17.7 |    -6.0517   | 17.4667  |       16 |


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
