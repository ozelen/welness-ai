# Welness AI Architecture

## System Overview

Welness AI is a comprehensive health tracking and personal wellness platform that leverages AI to provide personalized health recommendations and insights. The system is designed to be scalable, secure, and user-friendly while integrating with various health devices and services.

## Architecture Components

### 1. Frontend Tier
- **Technology Stack:**
  - Flutter for the main web application
 
- **Key Components:**
  - User Authorization
  - User Onboarding
  - User Dashboard
  - Diet Plan
  - Scanning Barcodes
  - Chat interface
  - Multi-language Support System (next)
  - Device Integration Interface (next)
  
### 2. Backend Tier
- **Technology Stack:**
  - Django/Python
  - PostgreSQL for primary database
  - Redis for caching and agent memory
  - MongoDB for open food facts data

- **Key Modules:**
  - Goals: User goals planning
  - Meals: Diet planning
  - Facts: Food nutrition facts data & integrations
  - Activities: User Activities
  - Bots: Messengers integrations
  - Agents: Agents configuration
  - Workouts (next): Workout planning
  - Coaches (next): Adding humans in the loop

### 3. AI/ML Layer (next)
- **Components:**
  - ML models for health recommendations
  - Food 101 for food recognition
  - Predictive analytics for health trends

### 4. Integration Layer
- **Food Marketplace Integrations:**
  - Mercadona API integration
  - Consum API integration

- **Device Integrations:**
  - Apple health integration
  - Apple watch Interface
  - Garmin watch Interface
  - Smart Watches API
  - Aura Ring API
  - Glucose Monitors API
  - Other Health Device APIs

- **Third-party Services:**
  - Open Food Facts database dump rollout
  - Open Food Facts API integration
  - Cloud Storage for documents
  - Translation Services
  - Voice-to-Text Services
  - Health Data Standards (FHIR, HL7)

- **Messaging integrations** -
  - Telegram Chatbot
  - Web UI Chat interface widget
  - Push Notifications

### 5. Data Layer
- **Data Storage:**
  - User Goals and Preferences
  - Meal plan relational data
  - Meal log data
  - Workout plan relational data
  - Workout log data

- **Data Security:**
  - End-to-end encryption
  - HIPAA compliance
  - GDPR compliance
  - Data anonymization

## System Flow

1. **User Authentication Flow:**
   - User registration/login
   - OAuth2.0 integration
   - JWT token management

2. **Onboarding Flow:**
   - AI agent interviews users, for their goals, current state, and food preferences
   - AI agent


3. **AI Processing Flow:**
   - Data aggregation
   - Pattern analysis
   - Recommendation generation
   - Health insights generation

4. **User Interaction Flow:**
   - Real-time data updates
   - Personalized recommendations
   - Multi-language support
   - Voice command processing

## Security Architecture

1. **Authentication & Authorization:**
   - Federated identity (OAuth)
   - Account-level data separation
   - Basic RBAC - User/Coach/Admin
   - Multi-factor authentication - not needed
   - Session management - not needed
   - API security - key based

2. **Data Protection:**
   - Encryption at rest
   - Encryption in transit - not needed
   - Secure key management - AWS KMS/Secret Store
   - Regular security audits - not needed

## Scalability & Performance

1. **Scalability:**
   - Modular Monolith architecture
   - Load balancing ALB
   - Database vertical scaling
   - Redis Caching

2. **Performance Optimization:**
   - CDN for static assets

## Monitoring & Analytics

1. **System Monitoring:**
   - Prometheus/Graphana
   - APM metrics

2. **Health Metrics:**
   - System health checks
   - Performance metrics
   - User engagement metrics
   - AI model performance

## Deployment Architecture

1. **Infrastructure:**
   - AWS Cloud
   - ECS/Fargate
   - Github CI
   - Infrastructure as Code

2. **Environment Strategy:**
   - Trunk based
   - Production Only
