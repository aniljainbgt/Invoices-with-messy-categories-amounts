# Invoices with messy categories amounts

### About this

This is a small data cleaning task for practice available on [Foresight BI](https://foresightbi.com.ng/microsoft-power-bi/dirty-data-samples-to-practice-on/)

### About the dataset

The dataset is a messy invoice data containing almost 100 rows. A single transaction (identified with an order id ) has multiple items purchased, means a single row for each order, so merging different items purchased and the amounts together into 2 fields respectively.

in the cleaned data as shown in the following image (downloaded from [Foresight BI](https://foresightbi.com.ng/microsoft-power-bi/dirty-data-samples-to-practice-on/)):

<img src="Images/messy invoice.jpg">

### Data Source

Data is available to download here on [Foresight BI](https://foresightbi.com.ng/wp-content/uploads/2020/05/1.-Badly-Structured-Sales-Data-1.xlsx)
Thank to [Ahmed Oyelowo](https://foresightbi.com.ng/author/4eyes/) who made this available.

### Steps to Clean

1. **Data -> From Table/Range** Open the range in power query, select any cell in the range then 
2. **Home -> Manage -> Duplicate**, Make a duplicate copy of the loaded data table, select the table then, 
3. In the first table, remove Amount column, to select the column left click on the Amount column header, right click to open context menu, then click on remove
4. Similarly, remove the Category Column from the second table
5. **Home -> Split Column -> By Delimiter**, In first table, Split the Category column with custom delimiter, In Advance option select Row to split in rows
6. In second table follow step 5 to split Amount column in rows
7. **Add Column -> Index Column -> From 1**, Now add Index column (From 1) in both the tables, this Index Column is used to join both the tables
8. **Home -> Merge Queries -> Merge Queries**, select first table, to join both the tables, In Merge query window add second table and select Index column for joining and click ok
9. The second table is added as a new column at the end of the first table. 
10. Expand the second table and only select the Amount column.
11. Now remove the Index column from the first query. 
12. Rename the Amount column, finally the data is clean and ready to use
13. Close and load the table in a new worksheet

### Skills Used in Excel-Powr Query
- Power Query
  - Transpose
  - Fill Down
  - Promoting First Line as Header
  - Pivot/Unpivot Columns

### Connect with Me

- [**LinkedIn**](https://www.linkedin.com/in/anil-jain-bgt/)







