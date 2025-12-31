==========================================================================
COTSWOLD FURNITURE: DATA QUALITY ASSESSMENT REPORT
==========================================================================
Report Generated: 2025-12-04 11:34:50
==========================================================================

==========================================================================
0. DATA PREPARATION
==========================================================================

⚠️  Found 8 temporary columns (will exclude from quality checks):
  • Revenue_Calculated
  • Profit_Calculated
  • Profit_Margin_%
  • Revenue_Difference
  • Profit_Difference
  • ... and 3 more

✓ Assessment will run on 13 original columns only

==========================================================================
1. DATASET OVERVIEW
==========================================================================
Total Records: 6,000
Total Columns: 13
Memory Usage: 1.73 MB

Column Names: Order Date, Product ID, Product, Quantity, Price, Cost, Discount, Revenue, Profit, Delivery Time (Days), Returned, Customer Name, Region

Data Types:
Order Date              datetime64[ns]
Product ID                      object
Product                         object
Quantity                         int64
Price                            int64
Cost                             int64
Discount                       float64
Revenue                        float64
Profit                         float64
Delivery Time (Days)             int64
Returned                         int64
Customer Name                   object
Region                          object
dtype: object

==========================================================================
2. COMPLETENESS ANALYSIS (Missing Values)
==========================================================================

✓ NO MISSING VALUES DETECTED
Overall Completeness: 100.00%

==========================================================================
3. DUPLICATE ANALYSIS
==========================================================================
Duplicate Rows: 0 (0.00%)
✓ No duplicate rows detected

Duplicate Product IDs: 5,990
  (Note: This is normal if Product ID refers to product type, not order ID)

==========================================================================
4. DATA CONSISTENCY CHECKS
==========================================================================
✓ Revenue calculations are consistent
  Formula validated: Revenue = (Price × Quantity) × (1 - Discount%)
✓ Profit calculations are consistent
  Formula validated: Profit = Revenue × (1 - Cost/Price)
✓ No negative prices
✓ No negative quantities
✓ All discount values are valid (0-1 range)

==========================================================================
5. OUTLIER DETECTION
==========================================================================
✓ No statistical outliers detected
  All values fall within Q1 - 3×IQR to Q3 + 3×IQR range

==========================================================================
6. DATA RANGE VALIDATION
==========================================================================

Quantity:
  Min: 1.00
  Max: 5.00
  Mean: 3.00
  Median: 3.00
  Std Dev: 1.42

Price:
  Min: 200.00
  Max: 1,500.00
  Mean: 728.71
  Median: 600.00
  Std Dev: 396.77

Cost:
  Min: 40.00
  Max: 300.00
  Mean: 132.59
  Median: 100.00
  Std Dev: 82.33

Discount:
  Min: 0.00
  Max: 0.25
  Mean: 0.13
  Median: 0.13
  Std Dev: 0.07

Revenue:
  Min: 150.00
  Max: 7,500.00
  Mean: 1,905.40
  Median: 1,440.00
  Std Dev: 1,458.90

Profit:
  Min: 120.00
  Max: 6,250.00
  Mean: 1,558.67
  Median: 1,200.00
  Std Dev: 1,183.71

Delivery Time (Days):
  Min: 2.00
  Max: 14.00
  Mean: 8.02
  Median: 8.00
  Std Dev: 3.74

==========================================================================
7. CATEGORICAL DATA QUALITY
==========================================================================

Product ID:
  Unique Values: 10
  Most Common: P1001 (647 occurrences, 10.8%)

Product:
  Unique Values: 10
  Most Common: Dining Table (647 occurrences, 10.8%)

Customer Name:
  Unique Values: 20
  Most Common: Ella Robinson (326 occurrences, 5.4%)

Region:
  Unique Values: 8
  Most Common: Wales (783 occurrences, 13.1%)

==========================================================================
8. DATE QUALITY ANALYSIS
==========================================================================

Order Date Range:
  Earliest: 2023-01-01 00:00:00
  Latest: 2025-10-31 00:00:00
  Span: 1034 days
  ✓ No future dates

==========================================================================
9. BUSINESS LOGIC VALIDATION
==========================================================================

Profit Margin Analysis:
  Negative Margins: 0 rows (0.00%)
  Extreme Margins (>95%): 0 rows (0.00%)
  Average Margin: 82.1%

Delivery Time Analysis:
  Min Delivery: 2 days
  Max Delivery: 14 days
  Average: 8.0 days

==========================================================================
10. OVERALL DATA QUALITY SCORE
==========================================================================

DATA QUALITY SCORE: 100.0/100
Grade: A (Excellent) ⭐⭐⭐⭐⭐

Outstanding data quality. Dataset is production-ready.

🎉 PERFECT SCORE - NO DEDUCTIONS!

==========================================================================
11. RECOMMENDATIONS
==========================================================================

ACTION ITEMS:
• Clean up 8 temporary calculation columns to reduce confusion

==========================================================================
DATA QUALITY ASSESSMENT COMPLETE
==========================================================================

==========================================================================
OPTIONAL: CLEAN UP TEMPORARY COLUMNS
==========================================================================

To permanently remove temporary columns, run:

  df = df[['Order Date', 'Product ID', 'Product', 'Quantity', 'Price', 'Cost', 'Discount', 'Revenue', 'Profit', 'Delivery Time (Days)', 'Returned', 'Customer Name', 'Region']]