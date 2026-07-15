# Data dictionary

| Field | Type | Meaning |
|---|---|---|
| `Channel` | Categorical code | `1` = Horeca (hotel, restaurant, or café); `2` = Retail |
| `Region` | Categorical code | `1` = Lisbon; `2` = Oporto; `3` = Other region |
| `Fresh` | Integer | Annual spending on fresh products, in monetary units |
| `Milk` | Integer | Annual spending on milk products, in monetary units |
| `Grocery` | Integer | Annual spending on grocery products, in monetary units |
| `Frozen` | Integer | Annual spending on frozen products, in monetary units |
| `Detergents_Paper` | Integer | Annual spending on detergents and paper products, in monetary units |
| `Delicassen` | Integer | Annual spending on delicatessen products, in monetary units; field name follows the source file |

## Workbook-derived fields

| Field | Formula or rule |
|---|---|
| `Customer ID` | Sequential workbook label from `CUST-001` to `CUST-440`; not present in the source |
| `Channel` | Code mapped through the visible lookup table with `VLOOKUP` |
| `Region` | Code mapped through the visible lookup table with `VLOOKUP` |
| `Total Spend` | Sum of the six product-category spending fields |
| `Grocery Share` | Grocery spend divided by total spend, protected by `IFERROR` |
| `Value Band` | `High Value` when total spend is at or above the dataset median; otherwise `Standard` |

Source definitions: https://archive.ics.uci.edu/dataset/292/wholesale%2Bcustomers

