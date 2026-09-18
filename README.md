# Social-Media-Ad-Conversion-Optimization

### Author: Aixin Gabriel V. Marcera

## Background

Digital advertising generates valuable data on audience characteristics, ad exposure, engagement, advertising spending, and purchasing behavior. However, high impressions and clicks do not necessarily translate into successful purchases. Understanding how users move through the advertising conversion funnel can help businesses identify effective campaigns, evaluate audience segments, and improve advertising efficiency.

This project analyzes social media advertising data to examine the relationship between ad engagement, customer characteristics, campaign performance, and purchase outcomes.

## Business Task

Analyze social media advertising data to identify campaign, audience, and engagement patterns associated with stronger purchase conversion performance and evaluate opportunities to improve advertising efficiency and targeting strategies.

## Business Questions

- Which campaigns generate the highest number of approved purchases?
- Which campaigns achieve stronger purchase conversion rates?
- Which campaigns generate purchases more efficiently relative to advertising spend?
- How does purchase conversion vary across age groups and gender?
- Which interest categories are associated with higher purchase conversion rates?
- How effectively do impressions and clicks translate into product inquiries and approved purchases?
- Is higher advertising spending associated with a greater number of approved purchases?
- Which campaigns demonstrate stronger overall conversion efficiency?

## Objectives

- Clean and prepare the advertising dataset for analysis.
- Create relevant digital marketing performance metrics.
- Evaluate the conversion funnel from impressions to approved purchases.
- Compare campaign performance based on volume, conversion rate, and cost efficiency.
- Identify audience segments and interest categories associated with stronger conversion outcomes.
- Develop a Tableau dashboard to communicate actionable advertising insights.
- Provide data-driven recommendations for campaign targeting and budget optimization.

## Tools

- **Microsoft Excel** — Data cleaning, issue logging, calculated fields, data transformation, pivot tables, and exploratory analysis
- **Tableau** — Data visualization, dashboard development, and performance comparison 

## Dataset 

**Source:** Anonymous social media advertising campaign dataset

**Kaggle Link:**  
https://www.kaggle.com/datasets/loveall/clicks-conversion-tracking/data

The original dataset contains **1,143 observations and 11 variables**. Each observation represents an individual advertisement and includes information about its campaign, target audience, advertising activity, spending, and conversion outcomes.

### Dataset Variables

| Variable | Description |
|---|---|
| `ad_id` | Unique identifier for each advertisement |
| `xyz_campaign_id` | Identifier associated with each campaign |
| `fb_campaign_id` | Campaign tracking identifier used by Facebook |
| `age` | Age group of the person shown the advertisement |
| `gender` | Gender of the person shown the advertisement |
| `interest` | Interest category associated with the audience member |
| `impression` | Number of times the advertisement was displayed |
| `clicks` | Number of clicks received by the advertisement |
| `spent` | Amount spent to display the advertisement |
| `total_conversion` | Number of people who inquired about the product after seeing the advertisement |
| `approved_conversion` | Number of people who purchased the product after seeing the advertisement |

### Scope

The analysis focuses on:

- Advertising reach and engagement
- Campaign-level performance
- Audience segmentation
- Interest-category performance
- Purchase conversion
- Advertising cost efficiency

The dataset does not include actual purchase revenue, profit margins, customer lifetime value, ad creative information, or detailed sales follow-up data. Therefore, the project evaluates conversion performance and advertising efficiency rather than profitability.

## Analytical Approach

The project followed a structured data analytics workflow:

1. Reviewed the dataset structure and variable definitions.
2. Inspected data quality issues and calculated-field errors.
3. Cleaned and transformed the dataset using Microsoft Excel.
4. Created marketing performance metrics for conversion and cost analysis.
5. Conducted exploratory analysis using pivot tables and summary calculations.
6. Compared campaign, demographic, and interest-category performance.
7. Examined the relationship between advertising spending and approved purchases.
8. Developed a Tableau dashboard to communicate key findings and business opportunities.

## Data Preparation

The original dataset contained **1,143 records**. Data preparation involved reviewing calculated fields, identifying formula errors, investigating outliers, and creating additional marketing performance metrics.

### Data Quality Issues Identified

An issue log was created to document errors and the corresponding solutions.

| Column | Issue | Resolution |
|---|---|---|
| `icr` | 1,143 rows contained `#DIV/0!` due to zero clicks | Used `IFERROR` to replace invalid calculations with zero |
| `icr` | One outlier recorded a 200% conversion value | Removed the outlier after investigation |
| `ipr` | 8 rows contained `#DIV/0!` due to zero product inquiries | Used `IFERROR` to replace invalid calculations with zero |

The cleaned dataset contained **1,142 observations** after the outlier was removed.

### Calculated Fields
The following calculated fields were created to support the analysis:

#### 1. Click-Through Rate (CTR)

CTR = Clicks / Impressions - measures the percentage of impressions that resulted in clicks.

#### 2. Inquiry Conversion Rate (ICR)

Inquiry Conversion Rate = Total Conversion / Clicks - measures the percentage of clicks that resulted in product inquiries.

### 3. Purchase Conversion Rate (PCR)

Purchase Conversion Rate = Approved Conversion / Clicks - measures the percentage of clicks that resulted in approved purchases.

### 4. Inquiry-to-Purchase Rate (IPR)

Inquiry-to-Purchase Rate = Approved Conversion / Total Conversion - measures the percentage of product inquiries that became approved purchases.

### 5. Cost per Click (CPC)

CPC = Spent / Clicks - measures the average advertising cost per click.

### 6. Cost per Inquiry  

Cost per Inquiry = Spent / Total Conversion - measures the average advertising cost associated with generating one product inquiry.

### 7. Cost per Approved Purchase

Cost per Approved Purchase = Spent / Approved Conversion - measures the advertising cost associated with generating one approved purchase.

IFERROR was used for calculations involving zero denominators to prevent division errors and ensure that the dataset could be analyzed consistently.

## Exploratory Data Analysis 

The exploratory analysis examined advertising performance from several perspectives:

### Overall Conversion Funnel

<img width="2152" height="356" alt="conversionfunnel" src="https://github.com/user-attachments/assets/1e7bbd59-0602-4488-8cea-766c4368b046" />

This helped identify the scale of audience exposure and the drop-off between each stage of the advertising funnel.

### Campaign-Level Performance

<img width="2152" height="1328" alt="campaign performance" src="https://github.com/user-attachments/assets/7b3b9401-b356-4b82-8563-4a4587b5af13" />

This allowed campaign performance to be assessed using approved purchases.

### Audience Performance

<img width="1834" height="1328" alt="audience performance" src="https://github.com/user-attachments/assets/85030105-3435-457d-9d1f-39e39f949eac" />

Purchase conversion rates were compared across **Age groups** and **Gender**

This helped identify audience segments associated with different levels of purchase conversion.

### Interest-Category Performance

<img width="2152" height="1328" alt="interest " src="https://github.com/user-attachments/assets/9d94738b-cdb4-4bc7-ab42-da3a56503e86" />

Interest categories were evaluated based on purchase conversion rate to identify audience interests associated with stronger conversion outcomes.

### Spending and Purchase Relationship

<img width="2152" height="1328" alt="ad spend vs approved purchases" src="https://github.com/user-attachments/assets/8a6c3b28-e992-4286-8bec-7ad1c23e8f6a" />

The relationship between advertising spending and approved purchases was examined to determine whether increased spending was associated with higher purchase volume.

### Campaign Efficiency

<img width="2152" height="1328" alt="campaign conversion efficiency matrix" src="https://github.com/user-attachments/assets/0fe0dddf-4a23-4f68-b842-031a5150bb2e" />

Campaigns were compared using a conversion efficiency matrix based on **Purchase conversion rate** and **Cost per approved purchase**

Each point in the matrix represents a campaign.

## Dashboard 

The Tableau dashboard, titled Social Media Ad Conversion Optimization Dashboard, evaluates advertising engagement, audience performance, and purchase conversion efficiency.

<img width="2350" height="1800" alt="socialmediaadv4" src="https://github.com/user-attachments/assets/1ad96683-b82b-436c-ae24-f1244340ee0a" />


### Dashboard Components 
- Overall advertising KPIs
- Conversion funnel
- Approved purchases by campaign
- Purchase conversion rate by age and gender
- Purchase conversion rate by interest category
- Advertising spend versus approved purchases
- Campaign conversion efficiency matrix

### Overall Dataset Metrics
- Total Impressions: 213.4 million
- Total Clicks: 38,164
- Overall CTR: 0.018%
- Product Inquiries: 3,262
- Approved Purchases: 1,077
- Inquiry-to-Purchase Rate: 33.02%
- Ad-level Cost per Purchase: approximately $54.51

## Key Findings

- The dataset recorded 213.4 million impressions, which generated 38,164 clicks, 3,262 product inquiries, and 1,077 approved purchases.
- The overall click-through rate was approximately 0.018%, indicating that only a small proportion of ad impressions resulted in clicks.
- Approximately 33.02% of product inquiries resulted in approved purchases, showing a substantial drop-off between inquiry and completed purchase.
- Campaign C generated the highest purchase volume with 872 approved purchases, but its aggregate cost per approved purchase was also higher than the other campaigns.
- Campaign A recorded the highest aggregate purchase conversion rate at approximately 21.24% and the lowest aggregate cost per approved purchase at approximately $6.24, although it generated a smaller number of purchases overall.
- Campaign B produced an intermediate level of purchase volume and conversion efficiency compared with Campaigns A and C.
- Purchase conversion varied across age and gender groups, with the highest observed segment being males aged 30–34, recording a purchase conversion rate of approximately 6.82%.
- Among the analyzed audience segments, females aged 45–49 recorded the lowest purchase conversion rate at approximately 1.19%.
- Interest categories also showed differences in purchase conversion performance, with Interest 31 recording the highest aggregate purchase conversion rate among the displayed categories at approximately 8.21%.
- Advertising spend was positively associated with approved purchase volume, although higher spending did not necessarily correspond to stronger conversion efficiency.

## Business Recommendations

- Evaluate campaigns using both purchase volume and cost per approved purchase rather than relying solely on impressions or clicks.
- Review high-volume campaigns for opportunities to improve conversion efficiency and reduce the cost associated with generating purchases.
- Consider using audience-level conversion patterns to guide future targeting and campaign segmentation.
- Explore interest categories with stronger purchase conversion rates for more focused advertising strategies.
- Monitor the full conversion funnel to identify potential gaps between ad engagement, product inquiries, and completed purchases.
- Avoid evaluating campaign success based only on reach or engagement; include approved purchases and cost-efficiency metrics in performance reviews.
- Continue comparing campaign-level conversion rates with spending to identify opportunities for more efficient budget allocation.

## Key Takeaway 

> Advertising performance should not be evaluated through impressions and clicks alone. The analysis shows that campaigns can generate
different outcomes in terms of purchase volume, conversion rate, and cost efficiency. Combining funnel analysis, audience segmentation, and campaign-level efficiency metrics provides a more complete basis for improving digital advertising decisions.

## Limitations

- The dataset does not include actual purchase revenue or profit margins.
- Approved purchases indicate conversion volume but do not reveal the monetary value of each purchase.
- The analysis identifies relationships and patterns but does not establish causation.
- Factors such as ad creative, messaging, pricing, product quality, seasonality, and sales follow-up processes are not included.
- Interest codes are provided as numerical categories without detailed descriptions of the actual interests.
- Campaign IDs provide identifiers but limited contextual information about campaign objectives or creative strategy.
- Cost-per-purchase metrics may be unstable for ads or campaigns with very few approved purchases.
- The dataset may not fully represent current advertising behavior or broader market conditions.

## Conclusion 

This project demonstrates how social media advertising data can be transformed into actionable business insights by examining the relationship between ad exposure, engagement, audience characteristics, spending, and purchase outcomes.

Through data cleaning, calculated-field creation, exploratory analysis, and Tableau visualization, the project evaluates campaign performance beyond basic engagement metrics. The findings highlight the importance of combining conversion volume, conversion rates, and advertising efficiency when making decisions about audience targeting, campaign evaluation, and budget allocation.

## Author
Aixin Gabriel V. Marcera
