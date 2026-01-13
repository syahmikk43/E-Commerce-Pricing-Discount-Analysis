# E-Commerce Pricing Discount Analysis
## Project Background
This project focuses on analysing pricing structures and discount behaviour in an e-commerce retail environment. The datasets contain ~60k data that already been cleaned to 144 records of product-level details such as brand, category, gender, colour, current price, previous price, and recommended retail price (RRP).
While it does not include sales or profit data, it still provides valuable insights into how pricing strategies differ across brands and product categories, and how discounts are applied to various product types and demographics.

#### The analysis aims to uncover :
- How pricing compares to RRP across brands.
- Which brands or colours tend to offer higher discounts.
- The general price positioning and markdown practices.

#### Resources :
- The original dataset is available [here](https://www.kaggle.com/datasets/imrulhasanrobi/e-commerce-big-dataset-from-multi-category/data).
- The cleaned data can be downloaded [here](https://github.com/syahmikk43-jpg/E-Commerce-Pricing-Discount-Analysis/tree/main/Cleaned%20data).
- An interactive Tableau dashboard can be viewed [here](https://public.tableau.com/app/profile/syahmikk43/viz/E-CommercePricingDiscountAnalysisDashboard/Dashboard1).

---

## Dataset Overview
This dataset contains **product-level** information (not transaction-level). It lacks sales quantity or profit data, so analysis focuses purely on **price and discount insights**.

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

These additional columns provided more insights into pricing trends and discount behaviour across brands and categories.
All fields are in a **single flat table** with no relational relationships.

<img width="1920" height="767" alt="Image" src="https://github.com/user-attachments/assets/195e4f87-29a3-4421-b1a6-4b58d852f1e4" />

---

## Executive Summary
Despite being a limited dataset, several insights emerged:

- Average discount rates vary widely by **brand**, with some applying aggressive markdowns, others staying near full price.  
- **Fashion-focused categories** tend to show higher discount behaviour.  
- The **top 10 colours** (Black, White, Grey, etc.) dominate across product listings.  
- Most products are sold below their RRP, indicating strong and consistent markdown practices across brands.
  
<img width="1584" height="1038" alt="Image" src="https://github.com/user-attachments/assets/18bad6ec-bff6-4ada-ad6f-4bc2fecd52e8" />

---

## Insights Deep Dive
#### 1️) Average Discount by Brand
The chart shows significant variation in discount levels across brands. Some brands, such as **Adidas** and **ASOS DESIGN** apply aggressive markdowns, while others like **Bench** or **Oskia** maintain lower discounts closer to retail. This suggests **diverse pricing strategies** for larger fashion brands rely on discounts to attract volume, whereas smaller or premium brands protect perceived value by discounting less.
In addition, men’s products tend to have slightly higher average discounts compared to women’s. This may indicate slower inventory turnover or stronger price competition within men’s categories, leading retailers to use deeper markdowns to boost conversions.

#### 2️) Top 10 Colours
The **colour distribution** shows that **neutral tones make up the majority of the collection**, with **Black**, **White**, and **Grey** being the most common. This suggests a **consumer preference toward versatile and classic colours**, which are common in fashion retail. A limited range of colour mixes could also mean that the company is more focused on its core inventory than on launching new colors based on trends or seasons.

#### 3️) Brand & Category Analysis
Across categories, pricing varies particularly between brands. **ASOS DESIGN** and **Adidas Originals** show broader price ranges, implying diverse product selection from budget to premium. Meanwhile, **smaller focus brands** cluster within tighter price ranges, indicating stable pricing or limited Stock Keeping Units (SKUs). This visualisation highlights how **brand strategy directly influences pricing diversity** within categories.

#### 4️) Price vs RRP Comparison
The scatter plot shows a **strong positive relationship** between current price and RRP, confirming that most price reductions are proportional to original retail values. Most data points fall **below the line**, indicating that the majority of products are **discounted below RRP**. A few products appear near or above the line, these likely represent new or premium releases sold closer to full price. Overall, this suggests **consistent markdown practices** across brands.

---

## Recommendations
- **Optimise markdown depth:** Several brands rely heavily on deep discounts, which may attract short-term sales but reduce perceived brand value and margin. The pricing or merchandising team should consider setting controlled discount thresholds and reserving heavy markdowns for seasonal clearance periods.

- **Balance men’s vs women’s discounting:** The analysis shows men’s products receive higher average discounts. This may suggest lower demand or slower inventory turnover. Adjusting promotional frequency for men’s items and improving marketing visibility could help maintain sales without deep price cuts.

- **Diversify product colour mix:** Neutral tones dominate the catalogue, which limits variety for trend-driven shoppers. The design or product planning team could introduce more vibrant seasonal colours to increase appeal and differentiate new collections.

- **Review RRP setting strategy:** The current RRP often sits significantly above the selling price, making discounts appear large but unrealistic. Recalibrating RRP values to better reflect actual market expectations will improve transparency and trust among customers.

- **Enhance pricing consistency across brands:** Some brands show wide pricing gaps within the same category, which may confuse buyers or suggest inconsistent quality. Setting clearer pricing tiers or subcategories can help position products more effectively and improve buyer confidence.

