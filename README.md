
# 📘 README –  Data for Packaging Lines

This repository contains anonymized datasets for analyzing and optimizing the sequencing of products in industrial packaging lines. All data has been structured for use in optimization models such as the Traveling Salesman Problem (TSP), metaheuristics (Ant System), or MILP approaches.

---

## 📂 File Structure

There are two types of datasets:

### 🔹 **By family**
These files represent homogeneous groups of products (technical families) within a packaging line. Filenames follow the format:

```
LineX_FamilyY.csv
```

Examples:
- `Line1_Family2.csv` refers to Family 2 of Line 1.
- `Line3_Family1.csv` refers to Family 1 of Line 3.

### 🔹 **By complete line**
These files contain all products processed on a given line. Filenames follow the format:

```
LineX_complete.csv
```

Examples:
- `Line2_complete.csv` represents the full data for Line 2.
- `Line4_complete.csv` represents the full data for Line 4.

---

## 🏷️ Column Definitions

| Column        | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| `Product_ID` | Unique product identifier (`P0001`, `P0002`, etc.)                |
| `FOR_INF`     | Code for lower packaging format                                               |
| `FOR_SUP`     | Code for upper packaging format                                               |
| `SELL_INF`    | Code for lower sealing cell used                                              |
| `SELL_SUP`    | Code for upper sealing cell used                                              |
| `GUIAS`       | Guide code used in the line                                                   |
| `GUIASC`, `GUIASL` | Specific guide codes (used in some lines only)                          |
| `Family`     | (Only in family files) Technical grouping ID (`F1`, `F2`, etc.)              |
| `Line`       | (Only in complete line files) Line identifier (`L1`, `L2`, etc.)             |

---

## ✅ Recommended Usage

These files are ready for:
- Building setup time (changeover) cost matrices between products
- Modeling sequencing problems using TSP or its variants
- Applying heuristic or metaheuristic algorithms
- Comparing optimized vs current sequencing strategies

---
