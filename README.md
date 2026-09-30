# GCD Comic Dashboard

<img width="600" height="415" alt="demo" src="https://github.com/user-attachments/assets/830b2833-54c9-4fcc-87ef-2845f98e8024" />

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

The dataset used for this dashboard was initially a vertical key value table with over a gigabyte of information. the [tsv_csv_converter notebook](https://github.com/ElectricKelp/comics_dashboard/blob/main/tsv_csv_converter.ipynb) documents the steps taken to pivot and reduce this dataset to a more manageable 40mb.

Further processing was done in PowerQuery to clean pricing and key date values. Excel is unable to handle dates pre 1900 so information prior had to be cut for this analysis.

<img width="1305" height="805" alt="power_query" src="https://github.com/user-attachments/assets/0731d5c9-c811-43e4-9651-7f56883d0642" />

Calculations can be found in the hidden data_validation sheet including pivot tables and functions to update the currently selected comic details.

<img width="600" height="350" alt="data_validation" src="https://github.com/user-attachments/assets/f4991736-1add-4bb8-9c97-24e895c0ae07" />

Another table was added to the data model, publisher_name_sorted, to keep the most prolific publishers at the top of the main slicer in the dashboard.

<img width="1043" height="678" alt="publisher_data_sorted" src="https://github.com/user-attachments/assets/08276a13-180d-43f3-be39-ec73ec58b4e6" />

### Interesting Trends

The two largest median increases in the pricing of comics occured during 2008 and 2020, after the financial crisis and the covid pandemic.

<img width="701" height="411" alt="retail_price" src="https://github.com/user-attachments/assets/335f15a6-32bb-4905-a17f-f13e556e0e83" />

While number of issues published yearly trends up, the most notable dip occured also during 2020 likely due to work constraints.

<img width="701" height="398" alt="published_per_year" src="https://github.com/user-attachments/assets/66bc9a08-5164-4626-8906-975eeb878935" />
