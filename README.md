# 📊 Sales & Customer Insights Dashboard
### لوحة تحليل المبيعات وسلوك العملاء

> **EN:** A Power BI project analyzing sales performance, customer behavior, and regional trends using real-world structured data.
>
> **AR:** مشروع Power BI لتحليل أداء المبيعات وسلوك العملاء والاتجاهات الإقليمية باستخدام بيانات حقيقية منظمة.

---

## 🗂️ Project Overview · نظرة عامة

**EN:** This project simulates a business intelligence solution for a retail company. It covers the full data analytics pipeline — from raw data preparation in Excel to interactive dashboard design in Power BI.

**AR:** يحاكي هذا المشروع حلاً لذكاء الأعمال لشركة تجزئة، ويغطي كامل مراحل تحليل البيانات — من تجهيز البيانات في Excel وصولاً إلى تصميم لوحة تحكم تفاعلية في Power BI.

**Tools Used · الأدوات المستخدمة:** Power BI · Excel · SQL · Power Query · DAX

---

## 📁 Files · الملفات

| File | Description | الوصف |
|------|-------------|-------|
| `Sales_Dashboard_Data.xlsx` | Dataset with 200 orders across 5 sheets | بيانات 200 طلب موزعة على 5 أوراق |
| `index.html` | Interactive dashboard — open live at [aryam-mis.github.io/Sales-Dashboard-PowerBI](https://aryam-mis.github.io/Sales-Dashboard-PowerBI) | لوحة التحكم التفاعلية |

---

## 📋 Dataset Structure · هيكل البيانات

**EN:** The Excel file contains **5 sheets**:

**AR:** يحتوي ملف Excel على **5 أوراق عمل**:

| Sheet | Content | المحتوى |
|-------|---------|---------|
| `Sales_Data` | 200 orders — product, customer, region, revenue, profit | 200 طلب — المنتج، العميل، المنطقة، الإيراد، الربح |
| `Monthly_Summary` | Revenue & profit aggregated by month | الإيراد والربح مجمّعان شهرياً |
| `Category_Analysis` | Performance breakdown by product category | تحليل الأداء حسب فئة المنتج |
| `Region_Analysis` | Sales metrics by region | مؤشرات المبيعات حسب المنطقة |
| `KPI_Dashboard` | Key metrics summary | ملخص المؤشرات الرئيسية |

---

## 📈 Dashboard Features · مميزات اللوحة

- **KPI Cards · بطاقات المؤشرات** — إجمالي الإيراد، الربح، الطلبات، متوسط قيمة الطلب
- **Line Chart · الرسم الخطي** — اتجاه الإيراد والربح الشهري (يناير–ديسمبر 2024)
- **Donut Chart · الرسم الحلقي** — توزيع الإيراد حسب فئة المنتج
- **Filters · الفلاتر** — تصفية حسب المنطقة والفئة

---

## 💡 Key Insights · أبرز النتائج

- 📦 **Electronics · الإلكترونيات** is the top category at **38%** of total revenue · تمثل 38% من إجمالي الإيراد
- 🌍 **North Region · المنطقة الشمالية** leads in sales with **158K SAR** · تتصدر المبيعات بـ 158 ألف ريال
- 💻 **Laptop · اللابتوب** is the best-selling product with **98.4K SAR** · أعلى مبيعاً بـ 98.4 ألف ريال
- 📅 Revenue shows a consistent **upward trend** throughout 2024 · الإيراد في ارتفاع مستمر طوال 2024
- 💰 Overall **profit margin: 30.4%** · هامش الربح الإجمالي: 30.4%

---

## 🔧 How to Reproduce in Power BI · كيفية التطبيق

**EN:**
1. Open **Power BI Desktop**
2. Click **Get Data → Excel** and import `Sales_Dashboard_Data.xlsx`
3. Load all 5 sheets
4. Use `Sales_Data` as the main fact table
5. Build relationships on: `Month`, `Category`, `Region` columns
6. Create visuals: Card · Line Chart · Donut Chart · Bar Chart · Table
7. Add **Slicers** for Region and Category filtering

**AR:**
1. افتح **Power BI Desktop**
2. اضغط **Get Data ← Excel** واستورد ملف `Sales_Dashboard_Data.xlsx`
3. حمّل جميع الأوراق الخمس
4. استخدم `Sales_Data` كجدول الحقائق الرئيسي
5. أنشئ العلاقات على أعمدة: `Month`، `Category`، `Region`
6. أنشئ المرئيات: بطاقات · رسم خطي · رسم حلقي · رسم شريطي · جدول
7. أضف **Slicers** للتصفية حسب المنطقة والفئة

---

## 📐 DAX Measures · معادلات DAX

```dax
Total Revenue = SUM(Sales_Data[Revenue])
Total Profit = SUM(Sales_Data[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)
Avg Order Value = DIVIDE([Total Revenue], DISTINCTCOUNT(Sales_Data[Order_ID]), 0)
Revenue Growth % = 
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], PREVIOUSYEAR('Date'[Date])),
    CALCULATE([Total Revenue], PREVIOUSYEAR('Date'[Date])),
    0
)
```

---

## 👩‍💻 Author · المؤلفة

**Aryam Mohammed Almohammedi**
Management Information Systems · Taibah University
تخصص نظم المعلومات الإدارية · جامعة طيبة

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/aryam-mis)

---

> 📌 *This is a personal project built independently to apply and showcase skills in Power BI, Excel, and business intelligence.*
>
> 📌 *مشروع شخصي مستقل لتطبيق وعرض مهارات Power BI وExcel وذكاء الأعمال.*
