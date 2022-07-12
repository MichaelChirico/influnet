# InfluNet

## Contents

This repository contains data extracted from the [Italian National Institute of Health (ISS)](https://www.epicentro.iss.it/influenza/influnet) bulletins starting from the [2003-2004 seasonal flu](https://w3.iss.it/site/rmi/influnet/pagine/stagioni.aspx)


## Epidemiological data schema

### National cases

| Column      | DataType | Description     |
| :---        |    :----:   |          ---: |
| flu_season      | String       | Flu season reference period  |
| year_week     |  String       | Bulletin reference week   |
| number_healthcare_workers   | Integer | Number of cases reported by the healthcare workers  |
| number_cases  | Integer | Weekly number of new confirmed cases  |
| population | Integer | Reference population |
| incidence | Double | 1000 x number_cases/pop |
| pop_0-4 | Integer | 0-4 reference population  |
| cases_0-4 | Integer | 0-4 weekly new cases  |
| inc_0-4 | Double | 1000 x cases_age_0-4/pop_age_0-4  |
| pop_5-14 | Integer | 5-14 reference population  |
| cases_5-14 | Integer | 5-14 weekly new cases  |
| inc_5-14 | Double | 1000 x cases_age_5-14/pop_age_5-14  |
| pop_15-64 | Integer | 15-64 reference population  |
| cases_15-64 | Integer | 15-64 weekly new cases  |
| inc_15-64 | Double | 1000 x cases_age_15-64/pop_age_15-64  |
| pop_65+ | Integer | ≥65 reference population  |
| cases_65+ | Integer | ≥65 weekly new cases  |
| inc_65+ | Double | 1000 x cases_age_65-plus/pop_age_65-plus  |

### Regional cases

| Column      | DataType | Description     |
| :---        |    :----:   |          ---: |
| flu_season      | String       | Flu season reference period  |
| year_week     |  String       | Bulletin reference week   |
| region     |  String       | Region reference name   |
| number_healthcare_workers   | Integer | Number of cases reported by the healthcare workers  |
| number_cases  | Integer | Weekly number of new confirmed cases  |
| population | Integer | Reference population |
| incidence | Double | 1000 x number_cases/pop |
| pop_0-4 | Integer | 0-4 reference population  |
| cases_0-4 | Integer | 0-4 weekly new cases  |
| inc_0-4 | Double | 1000 x cases_age_0-4/pop_age_0-4  |
| pop_5-14 | Integer | 5-14 reference population  |
| cases_5-14 | Integer | 5-14 weekly new cases  |
| inc_5-14 | Double | 1000 x cases_age_5-14/pop_age_5-14  |
| pop_15-64 | Integer | 15-64 reference population  |
| cases_15-64 | Integer | 15-64 weekly new cases  |
| inc_15-64 | Double | 1000 x cases_age_15-64/pop_age_15-64  |
| pop_65+ | Integer | ≥65 reference population  |
| cases_65+ | Integer | ≥65 weekly new cases  |
| inc_65+ | Double | 1000 x cases_age_65-plus/pop_age_65-plus  |

## Virological data schema






## Getting the data

**Direct download (CSV)**: https://raw.githubusercontent.com/fbranda/influnet/main/data-aggregated/epidemiological_data/national_cases.csv

**Python** (requires `pandas`):
```python
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/fbranda/influnet/main/data-aggregated/epidemiological_data/national_cases.csv")
```

**R** (requires `httr`):
```r
library(httr)
df <- read.csv(text=content(GET("https://raw.githubusercontent.com/fbranda/influnet/main/data-aggregated/epidemiological_data/national_cases.csv")))
```

## Contributions
1) Automatic report at link 


## License and attribution

This repository and data exports are published under the CC BY 4.0 license.


