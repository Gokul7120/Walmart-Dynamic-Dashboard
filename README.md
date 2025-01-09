Here’s a refined version of the **Dynamic Retail Dashboard in Excel** description, formatted for clarity and readability:

---

Dynamic Retail Dashboard in Excel**  

## Overview
The **Dynamic Retail Dashboard** is an interactive Excel tool for visualizing and analyzing retail data. It integrates data hosted on GitHub, leverages **Power Query** for seamless data transformation, and delivers insights via dynamic charts and Key Performance Indicators (KPIs). This dashboard helps businesses tackle critical challenges and make informed decisions.

---

## **Datasets Used**  

### **1. Orders Table**  
Detailed customer order data, including shipping, product, and financial metrics.  

**Sample Data:**  

| Order ID      | Returned | Order Date | Ship Date | Ship Mode       | Customer Name  | Segment    | Country       | Market  | Sales   | Profit  | Discount |  
|---------------|----------|------------|-----------|-----------------|----------------|------------|---------------|---------|---------|---------|----------|  
| CA-2012-124891 | No       | 31-07-2020 | 31-07-2020 | Same Day       | Rick Hansen    | Consumer   | United States | US      | 2309.65 | 762.18  | 0        |  
| IN-2013-77878  | Yes      | 05-02-2021 | 07-02-2021 | Second Class   | Justin Ritter  | Corporate  | Australia     | APAC    | 3709.40 | -288.77 | 0.1      |  
| IN-2013-71249  | No       | 17-10-2021 | 18-10-2021 | First Class    | Craig Reiter   | Consumer   | Australia     | APAC    | 5175.17 | 919.97  | 0.1      |  

---

### **2. Returns Table**  
Tracks returned orders, including the respective markets.  

**Sample Data:**  

| Returned | Order ID       | Market    |  
|----------|----------------|-----------|  
| Yes      | MX-2013-168137 | LATAM     |  
| Yes      | US-2011-165316 | LATAM     |  
| Yes      | ES-2013-1525878| EU        |  
| Yes      | CA-2013-118311 | United States |  

---

### **3. People Table**  
Information about sales representatives and the regions they manage.  

**Sample Data:**  

| Person           | Region     |  
|------------------|------------|  
| Anna Andreadi    | Central    |  
| Chuck Magee      | South      |  
| Kelly Williams   | East       |  
| Matt Collister   | West       |  
| Deborah Brumfield| Africa     |  

---

## **Problem Statements and Solutions**  

### **1. Key Performance Indicators (KPIs)**  
**Objective:** Dynamically display critical business metrics such as **Total Sales**, **Total Profit**, **Total Quantity**, **Number of Orders**, and **Profit Margin**.  

**Steps:**  
1. Import the **Orders Table** using **Power Query**.  
2. Create calculated columns for:  
   - **Profit Margin**: `Profit / Sales`.  
   - **Total Orders**: Count of `Order ID`.  
3. Use formulas to calculate key metrics:  
   - **Total Sales**: `=SUM(Sales)`.  
   - **Total Profit**: `=SUM(Profit)`.  
   - **Total Quantity**: `=SUM(Quantity)`.  

**Dynamic KPI Table:**  

| **Metric**        | **Symbol** |  
|--------------------|------------|  
| Total Sales        | 💰         |  
| Total Profit       | 📈         |  
| Total Quantity     | 📦         |  
| Number of Orders   | 🛒         |  
| Profitability (%)  | 💹         |  

![image](https://github.com/user-attachments/assets/5b9e47cc-b9e9-4b1c-b8dd-5382251928c4)


### **2. Sales and Profit Analysis**  
**Objective:** Visualize trends in sales and profit over time.  

**Steps:**  
1. Create a **Pivot Table** grouping `Order Date` by **Year** and **Month**.  
2. Add **Sales** and **Profit** as values.  
3. Create a **Line Chart** to display trends.  
4. Add **Slicers** for dynamic filtering (e.g., by category, market, or region).  
![image](https://github.com/user-attachments/assets/ffebfbd2-97c8-4eab-b6c7-433f55dc87a2)

---

### **3. Category-Wise Profit**  
**Objective:** Analyze profit distribution across product categories.  

**Steps:**  
1. Create a **Pivot Table** with `Category` as rows and `Profit` as values.  
2. Sort the table in descending order of `Profit`.  
3. Create a **Bar Chart** for visualization.  
4. Add **Slicers** for filtering by region or year.  
![image](https://github.com/user-attachments/assets/1a274652-cc7c-4b24-9961-7afc5ebb6ec4)

---

### **4. Segment-Wise Sales Share (%)**  
**Objective:** Visualize sales contribution from each customer segment.  

**Steps:**  
1. Create a **Pivot Table** with `Segment` as rows and `Sales` as values.  
2. Calculate percentage share: `=Sales / Total Sales * 100`.  
3. Use a **Pie Chart** or **Donut Chart** to visualize.  
4. Add labels to dynamically display percentage values.  
![image](https://github.com/user-attachments/assets/3b13a0aa-44f4-4dab-a058-eb8d013fbd9d)

---

### **5. Sales by Country**  
**Objective:** Examine sales performance across countries.  

**Steps:**  
1. Create a **Pivot Table** with `Country` as rows and `Sales` as values.  
2. Sort by descending order of `Sales`.  
3. Apply **Conditional Formatting** or a **Heatmap** to highlight top performers.  
4. Alternatively, use a **Geographic Map Chart** to visualize data.  
![image](https://github.com/user-attachments/assets/181bd31b-3b48-4b7a-8bcd-340483800e5e)

---

### **6. Top 5 Subcategories**  
**Objective:** Identify the top-performing subcategories by sales.  

**Steps:**  
1. Create a **Pivot Table** with `Sub-Category` as rows and `Sales` as values.  
2. Sort in descending order of `Sales`.  
3. Filter to display only the top 5 subcategories.  
4. Create a **Column Chart** to visualize results.  
![image](https://github.com/user-attachments/assets/c7d5eb99-1acb-46dc-a5cb-3f2c933d1ce5)

---

### **7. Bottom 5 Subcategories**  
**Objective:** Highlight the lowest-performing subcategories by sales.  

**Steps:**  
1. Sort the **Pivot Table** in ascending order of `Sales`.  
2. Filter to show the bottom 5 subcategories.  
3. Create a **Column Chart** with contrasting colors for emphasis.  
![image](https://github.com/user-attachments/assets/5bfaa14c-6102-4d6f-a21e-4100bc4caae2)

---

### **8. Yearly Sales Trends**  
**Objective:** Analyze sales trends over the years.  

**Steps:**  
1. Group the `Order Date` by **Year** in a **Pivot Table**.  
2. Add `Sales` as values.  
3. Create a **Line Chart** to show yearly trends.  
4. Use **Slicers** for filtering by category, region, or segment.  

![image](https://github.com/user-attachments/assets/572666bf-5791-417e-ac68-d3fa33b9ee86)
![image](https://github.com/user-attachments/assets/2223a0cf-42da-48d0-baff-facc24e3ccc9)


---

## **Dynamic Features**  
- **Dynamic Charts**: Automatically update based on slicer selections.  
- **Power Query Integration**: Automates data cleaning and transformation.  
- **KPI Table**: Provides a quick summary of essential metrics.  

---

## **Next Steps for Extension**  
1. **Return Analysis**: Investigate return rates by market or category.  
2. **Customer Insights**: Identify top and bottom customers by profitability.  
3. **Market Comparison**: Evaluate performance across global markets.  
4. **Product Analysis**: Examine individual product performance.  

---

## **Significance**  
The **Dynamic Retail Dashboard** enables businesses to:  
- Monitor key metrics via KPIs.  
- Gain actionable insights into category, segment, and geographical trends.  
- Make informed, strategic decisions to enhance performance.  

--- 

This edited version refines the content and enhances structure and readability while maintaining all essential details.
