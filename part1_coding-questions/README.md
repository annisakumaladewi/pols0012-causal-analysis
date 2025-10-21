# POLS0012 — Causal Analysis Part 1

Part 1 of the Causal Analysis summative assessment focuses on the development of quantitative and coding skills.  
The project is divided into two sections:

- **Section 1:** Replicates and extends key results from Nathan Nunn (2008), *“The Long-Term Effects of Africa’s Slave Trades”* (*Quarterly Journal of Economics*, 123(1): 139–176), using instrumental variable estimation. Two additional variables were included in the dataset by the course instructor specifically for this task.

- **Section 2:** Implements a simulated experimental dataset containing 100 units and six variables, used to demonstrate causal identification and estimation under controlled conditions.

I have included **metadata for each question** to help viewers understand the datasets, variable definitions, and structure used in my analysis.

## Metadata

### Section 1 — Nunn (2008) replication dataset

| Variable name       | Variable description                                                                 |
|---------------------|---------------------------------------------------------------------------------------|
| `country`           | Country name                                                                          |
| `ln_realgdp2000`    | Log real per capita GDP in 2000, also called “ln y” in the paper                      |
| `ln_export_area`    | Log total number of slaves exported, divided by land area                             |
| `atlantic_dist`     | Sailing distance to nearest destination of Atlantic slave trade                       |
| `indian_dist`       | Sailing distance to nearest destination of Indian slave trade                         |
| `saharan_dist`      | Overland distance to nearest port of export for Saharan slave trade                   |
| `redsea_dist`       | Overland distance to nearest port of export for Red Sea slave trade                   |
| `colonial_power`    | Name of colonizer, if any, prior to independence                                      |
| `equator_dist`      | Distance from equator                                                                 |
| `longitude`         | Longitude                                                                             |
| `rain_min`          | Minimum monthly rainfall                                                              |
| `humid_max`         | Average maximum humidity                                                              |
| `low_temp`          | Average minimum temperature                                                           |
| `ln_coastline_area` | Log coastline divided by land area                                                    |
| `low_distance`      | =1 if situated at a low distance from a major slave destination                       |
| `high_slavery`      | =1 if country had a high level of slave exports                                       |

> Note: `low_distance` and `high_slavery` were created for this question and are not in Nunn (2008).  
> You’ll also need the **AER** package for this part.

---

### Section 2 — Simulated experiment

| Variable name | Variable description                                                                 |
|---------------|---------------------------------------------------------------------------------------|
| `y1`          | Potential outcome under treatment                                                     |
| `y0`          | Potential outcome under control                                                       |
| `R`           | Reporting status under treatment and control (=1 if reports data, 0 otherwise)        |
| `x`           | A baseline covariate                                                                  |
| `d`           | Treatment assignment (=1 if in treatment group, 0 if in control group)                |
| `outcome`     | Observed outcome (assuming no attrition occurred)                                     |

