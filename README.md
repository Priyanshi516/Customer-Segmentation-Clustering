# Project Report: Data-Driven Customer Segmentation using K-Means

## Executive Summary
This project applies unsupervised machine learning to partition a retailer's customer base into 5 distinct behavioral segments. By shifting from generic marketing to tailored persona strategies, the business can maximize marketing ROI and reduce customer churn.

## 1. Methodology & Feature Engineering
- **Features Used:** Customer Age, Annual Income ($k$), and a behavioral Spending Score (1–99).
- **Preprocessing:** All features were scaled using a `StandardScaler` to normalize standard deviations and prevent high-magnitude features (Income) from dominating Euclidean distance calculations.

## 2. Choosing K (Model Validation)
Based on empirical testing from $k=2$ to $k=10$:
- **The Elbow Method** showed a distinct structural inflection ("elbow") at $k=4$ and $k=5$.
- **The Silhouette Score** peaked optimally at $k=5$ ($\approx 0.39$).
- **Decision:** $k=5$ was selected as the optimal trade-off between model simplicity and cluster distinctness.

## 3. Customer Personas & Targeted Marketing Actions

### Cluster 0: "The Careful Wealthy"
- **Metrics:** Age: 53 | Income: $88k | Spending Score: 14
- **Strategic Action:** Do not spam with generic discount codes. Target them with premium, high-tier product showcases, exclusive brand partnerships, and VIP concierge services.

### Cluster 1: "The VIP MVPs"
- **Metrics:** Age: 43 | Income: $89k | Spending Score: 78
- **Strategic Action:** These are your core revenue drivers. Enroll them automatically into premium loyalty tiers, offer early-access previews to new collections, and provide personalized holiday gifts.

### Cluster 2: "The Passionate Spenders"
- **Metrics:** Age: 46 | Income: $23k | Spending Score: 81
- **Strategic Action:** High engagement despite lower financial bandwidth. Target them with bundle offers, "Buy One Get One" promotions, and flexible payment options (BNPL).

### Cluster 3: "The Stable Traditionalists"
- **Metrics:** Age: 56 | Income: $59k | Spending Score: 51
- **Strategic Action:** Predictable, middle-of-the-road shoppers. Maintain standard cadence via email newsletters and seasonal catalog mailings.

### Cluster 4: "The Untapped Youth"
- **Metrics:** Age: 27 | Income: $67k | Spending Score: 35
- **Strategic Action:** Young professionals with disposable income who aren't fully hooked. Target heavily via social media ads, digital-first shopping experiences, and limited-time flash sales.
