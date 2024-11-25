---
layout: default
title: Rohan Deshpande(rohankd2)
---

# Homework6

This page contains the visualizations created using Python, Altair, and Vegalite for the homework assignment. Each visualization includes a description, design choices, data transformations, and interactivity details.

---

## Visualization 1: Average Building Square Footage by Usage Type

<iframe src="visualizations/visualization1.html" width="100%" height="500px" frameborder="0"></iframe>

### Description

This visualization depicts the average building square footage for each usage type. The x-axis represents the average square footage, while the y-axis lists the usage types. This chart helps identify how the size of buildings varies based on their primary function.

### Design Choices

- **Encoding**:
  - Horizontal bar chart: Enables easy comparison of average square footage across categories.
  - Tooltip: Displays the specific values for `Square Footage` and `Usage Description` on hover.
- **Color Scheme**:
  - Used light green for bars to ensure visual clarity and alignment with accessibility standards.
- **Sorting**:
  - Sorted the bars in descending order of square footage to highlight the largest usage types prominently.

### Data Transformations

- Handled missing values in the `Square Footage` column by filling them with `0`.
- Grouped the data by `Usage Description` and calculated the average `Square Footage` for each category.

### Interactivity

- Added a **slider** to filter the data by `Year Constructed`. This allows users to dynamically explore the average square footage for buildings constructed in different years. The interactivity enhances clarity by focusing on specific subsets of data.

### Different Component than Homework5

The interactive element of sliding bar for the year was added.

---

## Visualization 2: Total Square Footage by Year

<iframe src="visualizations/visualization2.html" width="100%" height="500px" frameborder="0"></iframe>

### Description

This visualization shows the total building square footage aggregated by year. It allows users to identify trends in square footage growth over time. The chart is filtered to exclude invalid years (e.g., `0`).

### Design Choices

- **Encoding**:
  - Line chart: Highlights trends in square footage over time.
  - Tooltip: Displays the `Year Constructed`, total `Square Footage`, and the selected `County`.
- **Color Scheme**:
  - A consistent blue color was used for simplicity, as the chart focuses on a single selected county at a time.

### Data Transformations

- Filtered out rows with invalid `Year Constructed` values (`0`).
- Aggregated the data by `Year Constructed` and `County` to compute the total square footage for each year and county.

### Interactivity

- A **dropdown** was added to filter the data by `County`. This interactivity ensures the chart displays only data relevant to the selected county, making it easier to analyze specific regions.

### Different Component than Homework5

The entire visualization and the dataset for it is different than the 2nd visualization in Homework5.

---

## Notes

These visualizations were created as part of a Python and Altair assignment to explore data visualization techniques and interactivity. All files, including the dataset and notebook, are linked below:

- [View the Dataset (CSV)](https://github.com/rohan20399/dataViz/blob/main/building_inventory.csv)
- [View the Analysis (ipynb)](https://github.com/rohan20399/dataViz/blob/main/HW_6.ipynb)