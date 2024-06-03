# eCommerce Purchase Funnel Analysis with Google Analytics 4 and BigQuery

This project encompasses a series of tasks designed to analyze user behavior and conversion metrics on an eCommerce platform using Google Analytics 4 (GA4) data within BigQuery. The goal is to prepare data for BI reporting, calculate conversion rates through the purchase funnel, compare conversion rates across different landing pages, and test the correlation between user engagement and purchases.

## Solution Links
- [Task 1 Solution](https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1scellular-virtue-423105-p5!2sus-central1!3se1a4fc19-def1-4a53-9f93-256c8d3d038a!2e1)
- [Task 2 Solution](https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1scellular-virtue-423105-p5!2sus-central1!3s31a563c0-6873-48bb-b88a-0b80f4076893!2e1)
- [Task 3 Solution](https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1scellular-virtue-423105-p5!2sus-central1!3s7c5e9caf-3fcb-40bc-8574-c824532bddc2!2e1)
- [Task 4 Solution](https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1scellular-virtue-423105-p5!2sus-central1!3sb08ad21c-2b19-4ec8-af43-ba2a550c80ed!2e1)

## Tasks Overview

### Task 1: Data Preparation for BI Reporting
**Objective:** Create a query to extract a table with event, user, and session information from GA4 for the year 2021, focusing on key events related to the purchase funnel.

**Query Requirements:**
- **Fields to Include:**
  - `event_timestamp` (as `timestamp`)
  - `user_pseudo_id`
  - `session_id`
  - `event_name`
  - `country`
  - `device_category`
  - `source`
  - `medium`
  - `campaign`
- **Events to Filter:**
  - Session start
  - Product view
  - Add to cart
  - Begin checkout
  - Add shipping info
  - Add payment info
  - Purchase

[View the query solution](https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1scellular-virtue-423105-p5!2sus-central1!3se1a4fc19-def1-4a53-9f93-256c8d3d038a!2e1)

### Task 2: Conversion Calculations by Date and Traffic Channels
**Objective:** Create a query to calculate conversion metrics from session start to purchase for different traffic sources, mediums, and campaigns.

**Query Requirements:**
- **Fields to Include:**
  - `event_date` (from `event_timestamp`)
  - `source`
  - `medium`
  - `campaign`
  - `user_sessions_count` (unique sessions per user)
  - `visit_to_cart` (conversions from session start to add to cart)
  - `visit_to_checkout` (conversions from session start to begin checkout)
  - `visit_to_purchase` (conversions from session start to purchase)

[View the query solution](https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1scellular-virtue-423105-p5!2sus-central1!3s31a563c0-6873-48bb-b88a-0b80f4076893!2e1)

### Task 3: Conversion Rate Comparison Across Landing Pages
**Objective:** Analyze the conversion rates for different landing pages by extracting the page path from the session start event.

**Query Requirements:**
- **Metrics to Calculate:**
  - Unique sessions per unique user
  - Number of purchases
  - Conversion rate from session start to purchase

[View the query solution](https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1scellular-virtue-423105-p5!2sus-central1!3s7c5e9caf-3fcb-40bc-8574-c824532bddc2!2e1)

### Task 4: Correlation Between User Engagement and Purchases
**Objective:** Test the correlation between user engagement and purchase behavior.

**Query Requirements:**
- **Metrics to Calculate for Each Session:**
  - Engagement status (`session_engaged = '1'`)
  - Total engagement time (sum of `engagement_time_msec`)
  - Purchase status (whether a purchase was made)

**Correlation Analysis:**
- Between engagement status and purchase status
- Between total engagement time and purchase status

[View the query solution](https://console.cloud.google.com/bigquery?ws=!1m7!1m6!12m5!1m3!1scellular-virtue-423105-p5!2sus-central1!3sb08ad21c-2b19-4ec8-af43-ba2a550c80ed!2e1)

## Conclusion
This project provides a comprehensive analysis of the eCommerce purchase funnel using GA4 data in BigQuery. The queries developed in these tasks enable detailed insights into user behavior, conversion metrics, and the impact of different traffic channels and landing pages on purchase rates.
