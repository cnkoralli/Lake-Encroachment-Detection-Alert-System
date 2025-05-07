# Lake Encroachment Detection & Alert System

## Overview

Lake encroachment poses a serious threat to ecosystems, biodiversity, and water security. This project presents a machine learning-based solution deployed on IBM Z and LinuxONE Community Cloud (L1CC) to detect encroachments using satellite imagery and geospatial data.

## Key Features

* Utilizes **Google Earth Engine** for real-time satellite imagery.
* Applies **K-means clustering** for land-water segmentation.
* Detects changes in water boundaries over time.
* Sends automatic alerts upon detecting potential encroachment.
* Hosted on IBM Z LinuxONE for enterprise-grade scalability, speed, and security.

## Tech Stack

* **Platform**: IBM Z, IBM LinuxONE Community Cloud (L1CC)
* **Languages**: Python, JavaScript (for GEE scripting)
* **Libraries**: NumPy, Pandas, scikit-learn, OpenCV, Matplotlib
* **Tools**: Google Earth Engine, Docker, Jupyter, REST API
* **Model**: K-Means clustering for segmentation

## High-Level Architecture

```python
# Simplified Pseudocode for High-Level Design

1. Import satellite data using Google Earth Engine
2. Preprocess imagery (normalize, resize, remove clouds)
3. Apply K-means clustering to segment land vs. water
4. Compare historical and current images to detect area differences
5. Calculate encroachment area using pixel count
6. Generate alerts if encroachment exceeds threshold
7. Deploy on IBM Z instance with REST API
```

```
[Start]
   |
   v
[Fetch Satellite Image]
   |
   v
[Preprocess & Segment Image]
   |
   v
[Compare with Previous Image]
   |
   v
[Calculate Encroachment]
   |
   v
[Trigger Alert if Needed]
   |
   v
[End]
```

## Implementation Steps

1. **Set Up Google Earth Engine**: Register for an account and access satellite data (e.g., Landsat, Sentinel).
2. **Image Preprocessing**:

   * Filter by date and location
   * Apply cloud masking and normalization
3. **Clustering Algorithm**:

   * Use K-means to classify land and water
   * Label and color regions accordingly
4. **Change Detection**:

   * Overlay past and current segmentation masks
   * Compute difference in water body area
5. **Alerting Mechanism**:

   * Define a threshold for significant change
   * Use email/SMS/REST API to notify stakeholders
6. **Deployment**:

   * Containerize the model using Docker
   * Upload to L1CC
   * Serve via a REST API

## Mentorship

This project was developed with support from IBM Z mentors as part of the IBM Z Datathon.

## Contributors

* Charushila
* Dhanya Hegde
* Akshata Pandit
* Jhansi
* Rachana N. S

