---
layout: project
title: End-to-End Recommender System
subtitle: AI-Powered Food Recommendation Engine for Tastet.ca
date: 2023-07-01
technologies: [Python, TensorFlow, Collaborative Filtering, Content-Based Filtering, AWS, Docker, PostgreSQL]
---

## Project Overview

Designed and implemented a comprehensive recommendation system for [Tastet.ca](http://tastet.ca/), a innovative food technology startup. The system leverages both collaborative and content-based filtering techniques to provide personalized food recommendations, enhancing user engagement and satisfaction.

<img src="/assets/tastet-project-image.png" alt="Tastet Recommender System" class="project-image">

## Key Features

### 1. Hybrid Recommendation Engine
- Combined collaborative filtering with content-based approaches
- Implemented matrix factorization using SVD and NMF
- Deep learning models for capturing complex user preferences
- Real-time preference learning and adaptation

### 2. Personalization at Scale
- Handles 100,000+ users with sub-second response times
- Dynamic user profiling based on interaction history
- Context-aware recommendations (time, location, dietary restrictions)
- A/B testing framework for continuous improvement

### 3. Food Knowledge Graph
- Built comprehensive food ontology with nutritional data
- Ingredient-level similarity computations
- Cuisine and flavor profile matching
- Allergen and dietary restriction handling

## Technical Implementation

### Architecture
- **Microservices Architecture**: Scalable, maintainable system design
- **Real-time Pipeline**: Apache Kafka for event streaming
- **Model Serving**: TensorFlow Serving with Kubernetes
- **Database**: PostgreSQL for user data, Redis for caching

### Recommendation Algorithms
1. **Collaborative Filtering**
   - User-based and item-based approaches
   - Matrix factorization with implicit feedback
   - Deep neural collaborative filtering

2. **Content-Based Filtering**
   - TF-IDF for recipe descriptions
   - Image embeddings for visual similarity
   - Nutritional profile matching

3. **Hybrid Approach**
   - Weighted ensemble of multiple models
   - Context-aware blending strategies
   - Online learning for real-time adaptation

## Performance Metrics

- **Click-Through Rate**: Increased by 45%
- **User Engagement**: 3x increase in average session duration
- **Conversion Rate**: 28% improvement
- **System Performance**: 
  - 99.9% uptime
  - < 50ms average response time
  - Handles 1000+ requests/second

## Business Impact

- **User Growth**: 60% increase in monthly active users
- **Revenue Impact**: 35% increase in order value
- **Customer Satisfaction**: NPS score improved from 42 to 71
- **Operational Efficiency**: Reduced customer support queries by 40%

## Technical Stack

- **Machine Learning**: TensorFlow, Scikit-learn, PyTorch
- **Data Processing**: Apache Spark, Pandas, NumPy
- **APIs**: FastAPI, GraphQL
- **Infrastructure**: AWS (EC2, S3, RDS), Docker, Kubernetes
- **Monitoring**: Prometheus, Grafana, ELK Stack

## Challenges & Solutions

### 1. Cold Start Problem
- Implemented content-based recommendations for new users
- Popularity-based fallback strategies
- Progressive profiling through gamification

### 2. Scalability
- Distributed computing with Apache Spark
- Efficient caching strategies
- Approximate nearest neighbor search for similarity computations

### 3. Real-time Requirements
- Pre-computed recommendations with real-time adjustments
- Edge caching for popular items
- Asynchronous model updates

## Recognition

This project was featured as a case study for successful AI implementation in the food tech industry and received positive testimonials from both users and stakeholders.