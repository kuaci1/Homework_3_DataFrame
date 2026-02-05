# Homework 3 – DataFrame Solutions
## Data Science Batch 55

---

## Summary of Results

### Task 1: Full Name Column ✓
Created a new column "Full Name" combining First Name and Last Name in title case format.
- Position: Inserted after "Last Name" column
- Format: Title case (e.g., "Elvride Aries", "Basir Ninuk")

### Task 2: GMV Calculation ✓
Added GMV (Gross Merchandise Value) column after "Seller Discount".

**Formula:** 
```
GMV = Transaction Amount - Seller Discount + Delivery Fee
```

**Total GMV across all transactions:** Rp 2,714,593,600.00

### Task 3: Category Grouping & Pivot Table ✓

**Category Groups:**
- **Group 1:** Fashion, Babies/ Kids, Beauty/ Health
- **Group 2:** Service/ Mokado, Gadget/ Komputer

**Pivot Table - Total GMV per Month by Group:**

| Year-Month | Group 1      | Group 2        | Total          |
|------------|--------------|----------------|----------------|
| 2017-07    | 83,916,600   | 194,045,200    | 277,961,800    |
| 2017-08    | 59,189,600   | 341,657,100    | 400,846,700    |
| 2017-09    | 198,279,800  | 156,506,600    | 354,786,400    |
| 2017-10    | 92,012,400   | 135,405,000    | 227,417,400    |
| 2017-11    | 221,708,700  | 300,590,900    | 522,299,600    |
| 2017-12    | 89,257,800   | 435,267,100    | 524,524,900    |

**Key Insights:**
- November 2017 had the highest combined GMV
- Group 2 (Service/Gadget) dominated in August and December
- Group 1 (Fashion/Kids/Beauty) peaked in November

### Task 4: Seller with Highest GMV (August 2017) ✓

**ANSWER:**
- **Seller Name:** Petrus Sinda
- **Total GMV:** Rp 18,500,000.00

**Top 5 Sellers in August 2017:**
1. Petrus Sinda - Rp 18,500,000
2. Nita Musriyatul - Rp 14,006,000
3. Liany Ratih - Rp 14,006,000
4. Leony Wiwit - Rp 13,705,000
5. Wahyu Falentina - Rp 12,429,000

### Task 5: Seller with Most Transactions in Fashion (September 2017) ✓

**ANSWER:**
- **Seller Name:** A.Indraputra Wahyu
- **Transaction Count:** 1

**Note:** In the dataset for September 2017 Fashion category, multiple sellers have exactly 1 transaction each. The result shows the first seller alphabetically among those with the maximum count.

---

## Python Code Implementation

### Key Functions Used:
- `pd.read_csv()` - Load data
- `.str.title()` - Convert to title case
- `pd.to_datetime()` - Convert date strings
- `.pivot_table()` - Create summary tables
- `.groupby()` - Aggregate data by groups
- `.sort_values()` - Sort results

### Data Cleaning Steps:
1. Removed commas from numeric columns
2. Converted string numbers to float
3. Created proper datetime objects
4. Handled missing/null values appropriately

---

## Submission Instructions

1. Upload the Jupyter notebook to Google Colab
2. Upload both CSV files (Paid-Transaction.csv and Seller.csv) to Colab
3. Update file paths in the notebook if needed
4. Run all cells to verify results
5. Set sharing to "Anyone with the link can view"
6. Submit the Colab notebook link

---

**All tasks completed successfully! ✓**
