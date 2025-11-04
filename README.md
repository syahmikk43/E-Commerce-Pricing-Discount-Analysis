# E-Commerce-Pricing-Discount-Analysis
Analyzing product pricing, discounts, and RRP across multiple brands and categories.

## 📘 Project Background & Overview
This project focuses on analysing pricing structures and discount behavior in an e-commerce retail environment. The dataset contains product-level details such as brand, category, gender, color, current price, previous price, and recommended retail price (RRP).
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

This project focuses on analytical storytelling, which involves transforming simple retail data into visual insights regarding price behavior, brand strategy, and discount variability.

### 🛠️ Tools & Resources :
- **Excel** — data preparation and cleaning 
- **Tableau Public** — data visualization & dashboard design
- 📁 [Dataset Source (Kaggle)](https://www.kaggle.com/datasets/imrulhasanrobi/e-commerce-big-dataset-from-multi-category/data)
- 📁 [Cleaned Data](https://github.com/syahmikk43-jpg/E-Commerce-Pricing-Discount-Analysis/tree/main/Cleaned%20data)
- 🖥️ [Tableau Dashboard (Public Link)](https://public.tableau.com/app/profile/syahmikk43/viz/E-CommercePricingDiscountAnalysisDashboard/Dashboard1)  

---

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
All fields are in a **single flat table** with no relational relationships.

---

## 🧭 Executive Summary
Despite being a limited dataset, several insights emerged:

- Average discount rates vary widely by **brand** with some apply aggressive markdowns, others stay near full price.  
- **Fashion-focused categories** tend to show higher discount behavior.  
- The **top 10 colors** (Black, White, Grey, etc.) dominate across product listings.  
- Most products are sold below their RRP, indicating strong and consistent markdown practices across brands.
  
<img width="1584" height="1038" alt="Image" src="https://github.com/user-attachments/assets/18bad6ec-bff6-4ada-ad6f-4bc2fecd52e8" />

---

## 🔍 Insights Deep Dive
### 1️⃣ Average Discount by Brand
The chart shows significant variation in discount levels across brands. Some brands such as **Adidas** and **ASOS DESIGN** apply aggressive markdowns, while others like **Bench** or **Oskia** maintain lower discounts closer to retail. This suggests **diverse pricing strategies** for larger fashion brands rely on discounts to attract volume, whereas smaller or premium brands protect perceived value by discounting less.
In addition, men’s products tend to have slightly higher average discounts compared to women’s. This may indicate slower inventory turnover or stronger price competition within men’s categories, leading retailers to use deeper markdowns to boost conversions.

### 2️⃣ Top 10 Colors
The **color distribution** shows that **neutral tones make up majority of the collection**, with **Black**, **White**, and **Grey** being the most common. This suggests a **consumer preference toward versatile and classic colors**, which are common in fashion retail. A limited range of color mixes could also mean that the company is more focused on its core inventory than on launching new colors based on trends or seasons.

### 3️⃣ Brand & Category Analysis
Across categories, pricing varies particularly between brands. **ASOS DESIGN** and **Adidas Originals** show broader price ranges, implying diverse product selection from budget to premium. Meanwhile, **smaller focus brands** cluster within tighter price ranges, indicating stable pricing or limited Stock Keeping Units (SKUs). This visualisation highlights how **brand strategy directly influences pricing diversity** within categories.

### 4️⃣ Price vs RRP Comparison
The scatter plot shows a **strong positive relationship** between current price and RRP, confirming that most price reductions are proportional to original retail values. Most data points fall **below the line**, indicating that the majority of products are **discounted below RRP**. A few products appear near or above the line, these likely represent new or premium releases sold closer to full price. Overall, this suggests **consistent markdown practices** across brands.

---

## 💡 Recommendations
| Area | Action | Rationale |
|-------|--------|-----------|
| **Pricing Consistency** | Review brands with high discount volatility | To maintain fair pricing perception |
| **Product Planning** | Focus on top color trends | Align product offering with consumer demand |
| **Data Enhancement** | Add sales, cost, and profit columns | Enables more meaningful KPI and margin analysis |
| **Modeling** | Build product–sales relational structure | Support advanced trend and profit analysis |

---

## ⚠️ Limitations
- No transaction data (e.g., sales, profit, quantity, or date).  
- Single flat dataset — limited analytical relationships.  
- Insights are **descriptive only**, not performance-based.  
- Currency fixed in USD — no regional or temporal context.
