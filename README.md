## Home assignment

***Model 3 - NYISO Fuel Mix Data Analysis***


**Introduction**

The goal of this assignment was to code a model that meets the Overall System Requirements and uses the following inputs:
* NYISO fuel-mix generation data for the month of August 2019 (see attached zip file) where the NYISO measures and reports (at 5 minute granularity) fuel-mix generation data for the entire ISO. This data separates electrical generation by the following fuel sources: dual fuel, natural gas, nuclear, other fossil fuels, other renewables, wind, and hydropower. In this home assignment you ought to analyze and gather insights from the NYISO fuel-mix generation data. Note that all data is reported in time-ending format. For example, data at timestamp 12/15/2020 00:10:00 is for the timespan 12/15/2020 00:05:00 to 12/15/2020 00:10:00.
* Emission factors [metric kgCO2e/kWh] by fuel source:
- Dual Fue = 0.444
- Natural Gas = 0.426
- Nuclear = 0
- Other Fossil Fuels = 0.935
- Other Renewables = 0.256
- Wind=0
- Hydro = 0

**Technologies**

* Lorem version: 12.3
* Ipsum version: 2.33

import pandas as pd
import os
import seaborn as sns
import matplotlib.pyplot as plt

**Code Examples**

To generate lorem ipsum use special shortcode: `put-your-code-here`

**Results** 

As per requested as a part the assignment, the following tables have been created: 

* One (1) line plot of total generation for NYISO for the average and typical days (x-axis: timestamp, y-axis: generation). Impose both lines on the same plot.

The Average is displayed in orange and the blue represents the typical day. Notice that the energy generation is closely dependent on the working hours of the day. I suspect that is due to both labor availability and also in the cases of renewables -  outside environmental conditions.

![Average vs Typical day](AvgVsTypical%20day.png)

* One (1) line plot of total carbon emissions for NYISO for the average and typical days (x-axis: timestamp, y-axis: total emissions). Impose both lines on the same plot.

The Average is displayed in orange and the blue represents the typical day. Notice that the average displays irregularities, especially prior and post- working hours. 

![CO2 Production](CO2production.png)

* Heatmap plot of total generation for NYISO (x-axis: date, y-axis: time of the day, z-axis: power) for the dataset (1 plot)

Due to noise in the data, some of the time stamps have been removed. This noise constituted false time recording e.g. 00:12 min. This may be a measuring or reporting error. If it were to be included, the time stamp could be corrected into turning it into the closest 5 min interval rounding up or rather replacing it with the average in between the two time stamps where it is located. For the sake of transparency of these issues I decided to leave these problematic observations out of the sample for now.

![Heat Map: Total energy generation](HeatMap.png)


**Commentary** 


**Suggestions and future improvements**




Launch
