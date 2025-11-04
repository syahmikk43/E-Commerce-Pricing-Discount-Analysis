# E-Commerce-Pricing-Discount-Analysis
Analyzing product pricing, discounts, and RRP across multiple brands and categories.

## 📘 Project Background & Overview
This project focuses on analysing pricing structures and discount behavior in an e-commerce retail environment. The dataset contains product-level details such as brand, category, gender, color, current price, discount, and recommended retail price (RRP).
While it does not include sales or profit data, it still provides valuable insights into how pricing strategies differ across brands and product categories, and how discounts are applied to various product types and demographics.

### 🎯The analysis aims to uncover :
- How pricing compares to RRP across brands
- Which brands or colors tend to offer higher discounts
- The general price positioning and markdown practices within the dataset

Through Excel and Tableau, this project demonstrates how limited but structured data can still be transformed into meaningful insights using effective data visualization design.

### 🚀The final interactive dashboard allows viewers to explore :
- Key KPIs like average discount and price
- Discount trends across brands and gender
- Displays most common product colors across listings
- Analyze average current price by brand and categories.
- Price vs RRP comparison

This project highlights analytical storytelling — turning simple retail data into visual insights about pricing behavior, brand strategy, and discount variability.

### 🛠️ Tools & Resources :
- **Excel** — data preparation and cleaning 
- **Tableau Public** — data visualization & dashboard design
- 📁 [Dataset Source (Kaggle)](https://www.kaggle.com/datasets/imrulhasanrobi/e-commerce-big-dataset-from-multi-category/data)
- 📁 [Cleaned Data](https://github.com/syahmikk43-jpg/E-Commerce-Pricing-Discount-Analysis/tree/main/Cleaned%20data)
- 🖥️ [Tableau Dashboard (Public Link)](https://public.tableau.com/app/profile/syahmikk43/viz/E-CommercePricingDiscountAnalysisDashboard/Dashboard1)  


## 🗃️ Dataset Overview
### Data Description
This dataset contains **product-level** information (not transaction-level).  
It lacks sales quantity or profit data, so analysis focuses purely on **price and discount insights**.

The dataset containing product listings with details such as:
| Column Name | Description |
|--------------|-------------|
| `brand_name` | Product brand name |
| `title` | Product title / name |
| `current_price` | Current selling price |
| `previous_price` | Price before discount |
| `colour` | Product color |
| `rrp` | Recommended retail price |
| `Category` | Product category |
| `Gender` | Target audience |

To enhance the analysis, I add several new columns:
| New Column | Formula | Purpose |
|--------------|-------------|-------------|
| `Discount Price` | `=previous_price - current_price` | calculated discount amount |
| `Discount (%)` | `=(previous_price - current_price)/previous_price` | percentage discount |
| `RRP Gap` | `=(rrp - current_price)/rrp` | difference between RRP and current price |
| `Price Ratio` | `=current_price / rrp` | ratio of current price to RRP |

These additional columns provided more insights into pricing trends and discount behavior across brands and categories.
All fields are in a **single flat table** — no relational links.


## 🧭 Executive Summary
Despite being a limited dataset, several insights emerged:

- Average discount rates vary widely by **brand** — some apply aggressive markdowns, others stay near full price.  
- **Fashion-focused categories** tend to show higher discount behavior.  
- The **top 10 colors** (Black, Blue, White, etc.) dominate across product listings.  
- Most prices hover around **80–90% of RRP**, showing consistent markdown practices.
  
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/3d0a9d9a-3e2b-440f-80ec-f3794adcc5e5" />

