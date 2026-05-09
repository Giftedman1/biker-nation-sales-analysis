# Biker Nation Sales Analysis

## What 15,000+ Transactions Reveal About Bikes, Brands and Profit

A data-driven look at which brands, product lines and seasons drive the most profit for a multi-channel bike retailer.

---

## Introduction

Biker Nation is a company that sells bikes across different brands and categories through both online and in-store channels. With over 15,000 transactions on record, there is a lot of useful information sitting inside that data waiting to be uncovered.

The goal of this project was to dig into those transactions and answer four key business questions that could directly influence how Biker Nation stocks its inventory, plans its calendar, and manages its sales channels.

The entire analysis was completed in Python using Pandas, Matplotlib, and Seaborn, from raw data cleaning to final dashboard.

---

## The Data

The dataset contains transaction records from Biker Nation covering sales across multiple brands and product categories.

### Column Description

| Column | Description |
|---|---|
| `Transaction ID` | A unique identifier for each transaction |
| `Transaction Date` | The date the transaction took place |
| `Sales Channel` | Indicates whether the transaction happened online or in-store |
| `Order Status` | Shows whether the transaction was approved or cancelled |
| `Brand` | The brand of the bike sold |
| `Product Line` | Represents the type of bike, which is Road, Mountain, Standard, or Touring |
| `Product Class` | Describes the quality of the product as Low, Medium, or High |
| `Product Size` | The size of the bike, either Small, Medium, or Large |
| `Selling Price` | The price at which the product was sold in US dollars |
| `Standard Cost` | The cost of producing the product in US dollars |
| `Profit` | A calculated column derived by subtracting Standard Cost from Selling Price |

---

## Objectives

This analysis set out to answer four specific business questions:

- What brands of products should Biker Nation focus on?
- What are the most profitable months and is there a seasonal trend?
- What product line should Biker Nation have in stock?
- What sales channel generates the most profit and how great is the difference?

---

## Tools Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Data Cleaning

Before the analysis could begin, the dataset needed some attention. The following issues were identified and resolved:

- The column names had inconsistent casing and spacing across the dataset and were standardized to lowercase with underscores for consistency
- The sales channel column originally contained 1s and 0s which were replaced with Online and In-Store to make the data more readable
- Cancelled transactions were removed from the dataset since they do not represent actual completed sales
- Missing values in brand, product line, product class, and product size were filled with Unknown and later filtered out of the analysis to avoid skewing the results
- The selling price column had some rows with text characters mixed into the numeric values which were cleaned and converted to a proper numeric data type
- Duplicate rows were identified and removed from the dataset

After cleaning, the dataset was ready for analysis.

---

# Insights

## 1. Solex Leads in Volume but WeareA2B Leads in Profit

Looking at purchases by brand, Solex is the most purchased brand with 4,129 transactions, significantly ahead of Giant Bicycles and WeareA2B which are closely matched in second and third place respectively.

However, when profit is considered, a different picture emerges. WeareA2B generates the highest profit despite ranking third in total purchases. This means WeareA2B bikes sell at a higher margin per transaction, making it the most financially valuable brand for Biker Nation even though Solex moves more units.

This distinction between volume and profitability is an important one. A brand that sells a lot is not always the brand that makes the most money.

---

## 2. October is the Most Profitable Month

Profit remains relatively stable across all 12 months, which means there is no extreme seasonal slump to worry about. However, October stands out as the single most profitable month, followed closely by August and July.

June and September are the two weakest months, recording the lowest profit figures of the year. On a quarterly basis, Q4 is the strongest quarter driven by October's performance, while Q2 is the weakest with June pulling it down.

For Biker Nation, this means the second half of the year is generally stronger than the first, with a clear peak in Q4.

---

## 3. Standard Bikes Drive the Business

Standard is the most purchased `product_line` with 13,796 transactions, which is a significant distance ahead of Road in second place. Mountain records the least purchases with only 415 transactions.

The profit picture tells the same story. Standard leads all `product_line` categories at $7.9M in total profit. Road and Touring are closely matched in second and third place while Mountain generates the least profit at just $40,095 across the entire dataset.

When `product_class` is considered, Medium class products generate the most profit at $8.3M, far ahead of Low at $1.2M and High at $1.1M. Medium class bikes are clearly the sweet spot for Biker Nation, selling in high volumes at a profitable margin.

On `product_size`, Medium sized bikes account for the largest share of sales at over 50%, confirming that most customers prefer a mid-sized bike over large or small options.

---

## 4. Online and In-Store Perform Almost Equally

In-Store transactions generated $5,344,969 in profit while Online generated $5,287,680. The difference between the two `sales_channel` options is less than 1%, meaning Biker Nation does not rely heavily on one channel over the other.

Both channels are performing at an almost identical level.

---

# Recommendations

### Brand Strategy

WeareA2B should receive more attention and investment despite not being the highest volume brand. Its profit margin per transaction is higher than any other brand, meaning more stock and better promotion of WeareA2B bikes could meaningfully grow overall profit without needing to increase transaction volumes significantly.

### Inventory Management

Standard bikes in Medium class and Medium size should always be well stocked. They dominate across every metric including purchases, profit, and size distribution.

Running low on this combination would directly hurt revenue.

Mountain bikes, on the other hand, contribute very little to profit and may not justify large inventory space.

### Seasonal Planning

Biker Nation should prepare for stronger demand in Q4, particularly in October. Marketing campaigns, promotions, and inventory builds should be timed ahead of this period to maximize the natural profit peak the data consistently shows.

### Sales Channels

Since Online and In-Store perform almost equally, Biker Nation should maintain investment in both rather than deprioritizing either.

The balance between the two channels is a sign of healthy diversification and should be protected.

---

## Conclusion

Over 15,000 transactions told a clear story about how Biker Nation's business actually works.

- Standard bikes in Medium class drive the overwhelming majority of revenue
- WeareA2B is the most profitable brand per transaction despite not being the most purchased
- October is consistently the strongest month and Q4 the strongest quarter
- Both sales channels contribute almost equally to the bottom line

This analysis demonstrates how transactional sales data can uncover actionable business insights that directly support inventory planning, marketing strategy, and revenue optimization.
