# Social Media Performance & Marketing Analytics

An interactive three-page Power BI dashboard designed to analyze social media performance, content engagement, platform trends, and audience insights.

## Project Overview

Social media platforms generate large amounts of data through likes, comments, shares, views, and other engagement activities.

However, understanding which platforms perform best, what type of content attracts more engagement, and when audiences are most active can be challenging.

This project uses Microsoft Power BI to transform social media data into meaningful business insights through interactive dashboards and data visualizations.

The dashboard helps analyze platform performance, content effectiveness, audience engagement patterns, and influencer performance.

## Problem Statement

The objective of this project is to analyze social media performance and identify patterns that can help improve content strategy and audience engagement.

The analysis focuses on the following questions:

- Which social media platform generates the highest engagement?
- Which content types receive the most engagement?
- How does engagement change over time?
- Which categories perform better?
- Does content sentiment influence engagement?
- Does content length or hashtag count relate to engagement?
- What are the most effective posting hours and days?
- How do different influencer tiers perform?
- Do verified accounts generate different engagement levels?

##  Dataset

**Dataset Source:** Kaggle

**Dataset Link:** https://www.kaggle.com/datasets/aviral342/social-media-engagement-dataset

**Dataset Name:** Social Media Engagement Dataset

The dataset contains social media post information, engagement metrics, account information, and content characteristics.

### Dataset Features

| Feature | Description |
|---|---|
| Post_ID | Unique identifier for each post |
| Timestamp | Date and time of publication |
| Platform | Social media platform |
| Content_Type | Type of published content |
| Category | Content category |
| Likes | Number of likes |
| Comments | Number of comments |
| Shares | Number of shares |
| Views | Number of views |
| Saves | Number of saves |
| Engagement_Rate | Engagement rate of the post |
| Follower_Count | Number of account followers |
| Influencer_Tier | Influencer classification |
| Verified | Account verification status |
| Content_Length | Length of the content |
| Hashtag_Count | Number of hashtags |
| Sentiment | Positive, Neutral, or Negative |
| Hour_of_Day | Hour at which the post was published |
| Day_of_Week | Day on which the post was published |



##  Tools & Technologies

- **Microsoft Power BI** – Dashboard development and data visualization
- **Power Query** – Data cleaning and transformation
- **DAX** – Measures and analytical calculations
- **Data Modelling** – Relationships and date table creation
- **Kaggle** – Dataset source

## Dashboard Pages

### 1. Social Media Overview

Provides an overall summary of social media performance.

**Key Visualizations:**
- Total Posts
- Total Likes
- Total Engagement
- Total Views
- Total Comments
- Average Engagement Rate
- Engagement by Platform
- Posts by Platform
- Engagement Trend Over Time
- Posts by Content Type
- Engagement by Category

**Purpose:** Understand overall platform performance and identify engagement patterns.

### 2. Content Performance Analysis

Analyzes the relationship between content characteristics and audience engagement.

**Key Visualizations:**
- Total Shares
- Total Comments
- Total Saves
- Average Likes per Post
- Engagement by Content Type
- Average Engagement Rate by Content Type
- Sentiment Distribution
- Engagement by Sentiment
- Engagement vs Content Length
- Hashtag Count vs Engagement

**Purpose:** Identify content characteristics and formats associated with stronger engagement.

### 3. Audience & Posting Insights

Explores audience engagement patterns and account performance.

**Key Visualizations:**
- Average Followers
- Average Engagement per Post
- Verified Posts
- Engagement by Hour of Day
- Engagement by Day of Week
- Engagement by Influencer Tier
- Platform and Influencer Tier Performance

**Purpose:** Understand audience activity patterns and compare influencer and account performance.


## Data Modelling

A separate DateTable was created to support time-based analysis.

The DateTable includes:

- Date
- Year
- Month
- Month Number
- Quarter
- Day
- Day Name
- Year-Month

A one-to-many relationship was established between:

`DateTable[Date]` → `SocialMedia[Post Date]`

This relationship supports time-based filtering and trend analysis.

## DAX Measures

Some of the key DAX measures used in the project include:

**Total Posts**
```dax
Total Posts =
DISTINCTCOUNT(SocialMedia[Post_ID])
```

**Total Likes**
```dax
Total Likes =
SUM(SocialMedia[Likes])
```

**Total Engagement**
```dax
Total Engagement =
[Total Likes] +
[Total Comments] +
[Total Shares]
```

**Average Engagement Rate**
```dax
Average Engagement Rate =
AVERAGE(SocialMedia[Engagement_Rate])
```

**Average Likes per Post**
```dax
Average Likes per Post =
DIVIDE(
    [Total Likes],
    [Total Posts],
    0
)
```

Additional measures were created for views, comments, shares, saves, followers, and other engagement metrics.

## Key Business Findings

The following findings should be completed using the actual dashboard results.

1. **Platform Performance:** TikTok generated the highest engagement at approximately 22.2 million.

2. **Content Performance:** Video content generated the highest total engagement at approximately 9.8 million.

3. **Category Analysis:** [Mention the best-performing content category.]

4. **Posting Time Analysis:** Posting time and day of the week may influence engagement performance.

5. **Influencer Analysis:** Macro influencers contributed the largest share of total engagement.

6. **Sentiment Analysis:** Positive sentiment dominated the dataset and generated the highest engagement.


