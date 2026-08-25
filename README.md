# Unlocking Customer Insights: An Analysis of Customer Database


This project analyzes a customer database of *1,000 unique customer records* to uncover patterns in customer demographics, geographic distribution, contact-data quality, and loyalty-program participation.

The analysis was conducted using *Python and Pandas*, with the findings presented through a business-focused data storytelling presentation.

The objective was not only to understand the customer database, but also to identify *data-quality gaps and opportunities that can support better customer engagement, marketing, and retention strategies.*


##Table of Contents

- [1. Project Overview](#1-project-overview)
- [2. Data Analysis & Key Insights](#2-data-analysis--key-insights)
- [3. Business Recommendations](#3-business-recommendations)
- [4. Tools & Presentation](#4-tools--presentation)



# 1. Project Overview

## Business Objective

The goal of this project was to examine the existing customer database and answer key business questions around:

- Customer volume and database integrity
- Missing customer contact information
- Geographic market distribution
- Loyalty-card participation
- Opportunities for customer engagement and retention

## 📁 Dataset

The dataset contains *1,000 unique customer records* with *zero duplicate Customer IDs*.

### Customer attributes include:

| Attribute | Description |
|---|---|
| Customer ID | Unique identifier for each customer |
| Customer Name | Customer's name |
| Email | Customer email address |
| Phone Number | Customer contact number |
| Address Line 1 | Customer address |
| City | Customer city |
| Country | Customer country |
| Postcode | Customer postal code |
| Loyalty Card | Loyalty-program participation status |



## 🧹 Data Quality Assessment

The dataset was already cleaned, so the analysis focused primarily on *data inspection, quality assessment, and exploratory analysis*.

### Database Health

- *1,000* unique customer records
- *0* duplicate Customer IDs
- *0 missing values* across:
  - Customer Name
  - Address Line 1
  - City
  - Country
  - Postcode

However, gaps were identified in the digital contact fields:

| Field | Missing Records | Missing % |
|---|---:|---:|
| Email | 204 | 20.4% |
| Phone Number | 130 | 13.0% |

These gaps may reduce the organization's ability to effectively communicate with and engage customers through digital channels.


# 2. Data Analysis & Key Insights

## 👥 Customer Base

The analysis identified:

*1,000 unique customers*

with no duplicate customer IDs.

This provides a reliable foundation for customer segmentation and further analysis.



## 🌍 Geographic Distribution

The customer base is concentrated across three countries:

| Country | Customers | Share |
|---|---:|---:|
| 🇺🇸 United States | 782 | 78.2% |
| 🇮🇪 Ireland | 150 | 15.0% |
| 🇬🇧 United Kingdom | 68 | 6.8% |
| *Total* | *1,000* | *100%* |

### Key Insight

The *United States is the dominant market*, representing *78.2% of the total customer base*.

This concentration presents an opportunity to prioritize marketing and customer-engagement strategies in the US market.


## 📧 Digital Contact Data

One of the most important data-quality findings was the presence of missing digital contact information.

### Email

- *796 customers* have email addresses
- *204 customers* are missing email addresses
- *20.4%* of the database has no email address

### Phone

- *870 customers* have phone numbers
- *130 customers* are missing phone numbers
- *13.0%* of the database has no phone number
- *Out of the 204 and 130, 25 persons have missing records both in email and phone number*
### Business Impact

Incomplete contact information can limit:

- Email marketing
- Customer communication
- Promotional campaigns
- Customer retention activities
- Personalized engagement



## 💳 Loyalty Program

The customer database also tracks participation in the loyalty-card program.

The loyalty-card field is *100% complete*, with customers categorized into two groups:

- *Yes* — Active loyalty-card holders
- *No* — Customers without a loyalty card

This creates a useful foundation for customer segmentation, retention campaigns, and targeted loyalty-program enrollment.



# 3. Business Recommendations
Based on the findings, the following actions are recommended.

1. Improve Email Data Capture
There are *204 customers without email addresses*.

The business should introduce email-capture initiatives such as:

- In-store prompts
- Customer profile updates
- Physical mailers
- Data-capture incentives

The objective should be to progressively reduce the *20.4% email-data gap*.


2. Prioritize the US Market

With *782 customers*, the United States represents the largest customer market.

Marketing and logistical resources can therefore be strategically prioritized toward the US market while continuing to develop the Ireland and UK customer bases.



3. Strengthen Phone Data Collection

*130 customer records* are missing phone numbers.

Improving phone-number collection would create additional opportunities for customer communication and multi-channel engagement.

4. Increase Loyalty Program Enrollment
Customers in the *"No" loyalty-card category* can be targeted with personalized enrollment campaigns and incentives.

This could support:
- Customer retention
- Repeat purchases
- Reward campaigns
- Customer segmentation
- Long-term customer engagement



## 📌 Key Takeaways

The analysis revealed four major opportunities:

> *1,000* unique customer records provide a strong customer-data foundation.

> *20.4%* of customers are missing email addresses.

> *78.2%* of customers are located in the United States.

> Loyalty-card data provides an opportunity for targeted customer retention and enrollment campaigns.



# 4. Tools & Presentation

## 🛠️ Tools Used

### Python
Used for data inspection, analysis, and exploratory data analysis.

### Pandas
Used for data manipulation, missing-value analysis, and customer-level analysis.

### Google Colab
Used as the primary environment for conducting the analysis.

### Google Slides
Used to communicate the findings through a business-focused presentation.


## 🔎 Example Analysis

The following Python/Pandas code was used to assess missing values:

```python
null_summary = pd.DataFrame({
    'Missing Values': df.isnull().sum(),
    'Missing %': (df.isnull().sum() / len(df) * 100).round(2)
})

null_summary
```


