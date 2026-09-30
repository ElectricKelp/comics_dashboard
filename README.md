# GCD Comic Dashboard

insert demo gif here

## Abstract

A neat lil' board to capture some insights from the Grand Comics Database, a public volunteer effort to consolidate comic publishing data.

An archived copy of the database files [can be found here](https://www.loc.gov/item/2018487926/). The current python notebook uses the tsv file titled '2026-01-10_issues.tsv' from the 2026 archive.

### Excel Skills Used

- PowerQuery
- DataModel & DAX
- Pivot Tables/Charts
- Functions & Formulas

### Python Skills Used

- Pandas
- Jupyter Notebook
- input/output

## Construction

The dataset used for this dashboard was initially a vertical key value table with over a gigabyte of information. the tsv_csv_converter notebook documents the steps taken to pivot and reduce this dataset to a more manageable 40mb.

Further processing was done in PowerQuery to clean pricing and key date values. Excel is unable to handle dates pre 1900 so information prior had to be cut for this analysis.

need picty of powerquery worm

Calculations can be found in the hidden data_validation sheet including pivot tables and functions to update the currently selected comic details.

screen cap of updating table

Another table was added to the data model, publisher_name_sorted, to keep the most prolific publishers at the top of the main slicer in the dashboard.

data model pic

### Interesting Trends

The two largest median increases in the pricing of comics occured during 2008 and 2020, after the financial crisis and the covid pandemic.

pic of median price graph

While number of issues published yearly trends up, the most notable dip occured also during 2020 likely due to work constraints.

pic of yearly issue count