# EDA Report — data2
_Generated: 2026-02-04T18:58:43_

## Dataset Overview
- Rows: **4424**
- Columns: **37**

### Column Roles (inferred)
| column                                         | role        |
|:-----------------------------------------------|:------------|
| Marital status                                 | numeric     |
| Application mode                               | numeric     |
| Application order                              | numeric     |
| Course                                         | numeric     |
| Daytime/evening attendance                     | numeric     |
| Previous qualification                         | numeric     |
| Previous qualification (grade)                 | numeric     |
| Nacionality                                    | numeric     |
| Mother's qualification                         | numeric     |
| Father's qualification                         | numeric     |
| Mother's occupation                            | numeric     |
| Father's occupation                            | numeric     |
| Admission grade                                | numeric     |
| Displaced                                      | numeric     |
| Educational special needs                      | numeric     |
| Debtor                                         | numeric     |
| Tuition fees up to date                        | numeric     |
| Gender                                         | numeric     |
| Scholarship holder                             | numeric     |
| Age at enrollment                              | numeric     |
| International                                  | numeric     |
| Curricular units 1st sem (credited)            | numeric     |
| Curricular units 1st sem (enrolled)            | numeric     |
| Curricular units 1st sem (evaluations)         | numeric     |
| Curricular units 1st sem (approved)            | numeric     |
| Curricular units 1st sem (grade)               | numeric     |
| Curricular units 1st sem (without evaluations) | numeric     |
| Curricular units 2nd sem (credited)            | numeric     |
| Curricular units 2nd sem (enrolled)            | numeric     |
| Curricular units 2nd sem (evaluations)         | numeric     |
| Curricular units 2nd sem (approved)            | numeric     |
| Curricular units 2nd sem (grade)               | numeric     |
| Curricular units 2nd sem (without evaluations) | numeric     |
| Unemployment rate                              | numeric     |
| Inflation rate                                 | numeric     |
| GDP                                            | numeric     |
| Target                                         | categorical |

## Data Quality Checks
- Duplicate rows: **0**
- Constant (single-value) columns: **None**
- High-missing columns (≥40%): **None**
- Possible identifier-like columns: **None**

### Missingness Summary (count and %)
_Missingness summary unavailable._

## Descriptive Statistics
### Categorical Column Frequency (counts + %)
Selected column: **Target**
| value    |   count |   percent |
|:---------|--------:|----------:|
| Graduate |    2209 |     49.93 |
| Dropout  |    1421 |     32.12 |
| Enrolled |     794 |     17.95 |

### Numeric Column Statistics (min/max/mean/median/mode/std/IQR/outliers)
| col              |   count_nonnull |   min |   max |     mean |   median |   mode |       std |   q1 |   q3 |   iqr |   outliers_1p5iqr | outlier_bounds   |
|:-----------------|----------------:|------:|------:|---------:|---------:|-------:|----------:|-----:|-----:|------:|------------------:|:-----------------|
| Marital status   |            4424 |     1 |     6 |  1.17857 |        1 |      1 |  0.605747 |    1 |    1 |     0 |               505 | (1.0, 1.0)       |
| Application mode |            4424 |     1 |    57 | 18.6691  |       17 |      1 | 17.4847   |    1 |   39 |    38 |                 0 | (-56.0, 96.0)    |

## Visualizations
Plots saved to `plots/`:

- bar_Target.png
- box_Marital status.png
- hist_Marital status.png
- mean_Marital status_by_Target.png
- missingness.png
- missingness_profile.png
- scatter_Curricular units 1st sem (credited)_vs_Curricular units 2nd sem (credited).png

## Insights (computed + narrative)
- Dataset has 4424 rows and 37 columns.
- No missing values detected across columns (0% missingness).
- No columns exceed the high-missing threshold (40%).
- No duplicate rows detected.
- No constant (single-value) columns detected.
- No strong identifier-like columns detected by uniqueness/name heuristics (still review for privacy).
- In 'Target', the most common value is 'Graduate' with 2209 rows (49.93%).
- Numeric 'Marital status': mean=1.179, median=1.000, std=0.606, IQR=0.000, outliers(1.5×IQR)=505.
- Numeric 'Application mode': mean=18.669, median=17.000, std=17.485, IQR=38.000, outliers(1.5×IQR)=0.
- Strongest numeric correlation observed: corr(Curricular units 1st sem (credited), Curricular units 2nd sem (credited)) = 0.945.

## Limitations / Potential Biases
- Outliers in 'Marital status' beyond [1.000, 1.000] may skew mean; consider robust stats or winsorization.
- Correlation does not imply causation; observed relationships may be confounded.
- This EDA reflects only the provided dataset; sampling method, population coverage, and time window may limit generalization.
