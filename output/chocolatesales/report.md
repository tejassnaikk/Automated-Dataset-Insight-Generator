# EDA Report — chocolatesales
_Generated: 2026-02-04T18:58:46_

## Dataset Overview
- Rows: **3282**
- Columns: **6**

### Column Roles (inferred)
| column        | role        |
|:--------------|:------------|
| Sales Person  | categorical |
| Country       | categorical |
| Product       | categorical |
| Date          | categorical |
| Amount        | text        |
| Boxes Shipped | numeric     |

## Data Quality Checks
- Duplicate rows: **0**
- Constant (single-value) columns: **None**
- High-missing columns (≥40%): **None**
- Possible identifier-like columns: **None**

### Missingness Summary (count and %)
_Missingness summary unavailable._

## Descriptive Statistics
### Categorical Column Frequency (counts + %)
Selected column: **Country**
| value       |   count |   percent |
|:------------|--------:|----------:|
| Australia   |     615 |     18.74 |
| India       |     552 |     16.82 |
| USA         |     537 |     16.36 |
| UK          |     534 |     16.27 |
| Canada      |     525 |     16    |
| New Zealand |     519 |     15.81 |

### Numeric Column Statistics (min/max/mean/median/mode/std/IQR/outliers)
| col           |   count_nonnull |   min |   max |    mean |   median |   mode |     std |   q1 |   q3 |   iqr |   outliers_1p5iqr | outlier_bounds   |
|:--------------|----------------:|------:|------:|--------:|---------:|-------:|--------:|-----:|-----:|------:|------------------:|:-----------------|
| Boxes Shipped |            3282 |     1 |   778 | 164.667 |      137 |     24 | 124.025 |   71 |  232 |   161 |                78 | (-170.5, 473.5)  |

## Visualizations
Plots saved to `plots/`:

- bar_Country.png
- box_Boxes Shipped.png
- hist_Boxes Shipped.png
- mean_Boxes Shipped_by_Country.png
- missingness.png
- missingness_profile.png

## Insights (computed + narrative)
- Dataset has 3282 rows and 6 columns.
- No missing values detected across columns (0% missingness).
- No columns exceed the high-missing threshold (40%).
- No duplicate rows detected.
- No constant (single-value) columns detected.
- No strong identifier-like columns detected by uniqueness/name heuristics (still review for privacy).
- In 'Country', the most common value is 'Australia' with 615 rows (18.74%).
- Numeric 'Boxes Shipped': mean=164.667, median=137.000, std=124.025, IQR=161.000, outliers(1.5×IQR)=78.

## Limitations / Potential Biases
- Outliers in 'Boxes Shipped' beyond [-170.500, 473.500] may skew mean; consider robust stats or winsorization.
- Not enough numeric columns to compute correlations/heatmap.
- This EDA reflects only the provided dataset; sampling method, population coverage, and time window may limit generalization.
