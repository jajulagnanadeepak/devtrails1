# EarnShield AI
### Smart Parametric Income Protection for Gig Workers

> **Team Alphabitrix**  
> Protecting delivery partners from income loss caused by weather and environmental disruptions.

---

## Problem Statement

Gig workers such as food delivery partners depend heavily on daily orders for income.  
Events like **heavy rain, extreme heat, severe air pollution, and city curfews** can suddenly stop them from working.

When these disruptions occur, workers lose their earnings for the day, while most platforms do not provide immediate financial protection.

---

## Our Solution

**EarnShield AI** is an AI-powered parametric insurance platform designed for gig workers.

Workers subscribe to a **small weekly protection plan**.  
When predefined disruption conditions are met, the system automatically verifies the trigger and releases payouts without requiring manual claim filing.

This creates a **fast, transparent, and reliable income safety net** for workers.

---

## Key Highlights

- AI-based risk prediction
- Dynamic weekly premium calculation
- Automatic claim trigger system
- Real-time disruption monitoring
- Instant payout through UPI
- Fraud detection and anti-spoofing support

---

## Target Users

### Initial Focus
- Swiggy delivery partners
- Zomato delivery partners
- Gig workers in Hyderabad

### Future Expansion
- Bike taxi workers
- Courier partners
- Hyperlocal service workers

---

## Parametric Trigger Model

| Event | Trigger Condition | Payout |
|-------|-------------------|--------|
| Heavy Rain | Rainfall > 50 mm | ₹300 |
| Extreme Heat | Temperature > 45°C | ₹200 |
| Severe Pollution | AQI > 400 | ₹150 |
| City Curfew | Official government alert | ₹400 |

---

## How AI Helps

### 1. Risk Prediction
AI evaluates area-based disruption probability using weather history, pollution patterns, and risk zones.

### 2. Dynamic Premium Pricing
Premiums are adjusted based on worker location and expected disruption exposure.

### 3. Fraud Detection
The system detects abnormal claims, suspicious location activity, coordinated spoofing attempts, and repeated misuse patterns.

---

## Adversarial Defense & Anti-Spoofing Strategy

To defend the platform against coordinated fraud rings and GPS spoofing attacks, EarnShield AI uses a **multi-signal fraud detection approach** instead of relying only on basic location coordinates.

### 1. The Differentiation
Our system differentiates between a genuinely stranded delivery partner and a bad actor spoofing location by combining:

- Recent route consistency and movement history
- Order activity and delivery behavior patterns
- Device behavior signals such as impossible jumps in location
- Environmental consistency checks against real disruption conditions
- Historical work behavior compared with normal worker activity

A genuine worker usually shows **natural movement, realistic disruption impact, and normal work history**, while a bad actor often shows **static spoofed coordinates, abnormal claim timing, repeated trigger-zone claims, or suspicious synchronization with other accounts**.

### 2. The Data
Beyond GPS coordinates, the system analyzes:

- Route trace history over time
- Device motion and speed consistency
- Timestamped order acceptance and delivery activity
- IP region consistency and suspicious device switching
- Claim timing clusters across nearby users
- Device fingerprint patterns
- Weather-event correlation with activity drop
- Historical claim frequency
- Zone-level anomaly spikes
- Cross-account coordination signals

This allows the platform to detect a **coordinated fraud ring**, not just an individual suspicious claim.

### 3. The UX Balance
Fraud prevention should not unfairly penalize honest workers facing real disruptions or temporary network issues.

Our workflow uses a **risk-tiered handling process**:

- **Low-risk claims** are auto-approved instantly
- **Medium-risk claims** undergo soft verification using passive signals
- **High-risk claims** are temporarily flagged for review instead of being immediately rejected

To maintain fairness:

- No worker is blocked based on one failed signal alone
- Grace windows are allowed during severe weather and network drops
- Delayed telemetry reconciliation can validate genuine claims
- Workers with positive trust history receive higher confidence scoring
- Only strong multi-signal fraud patterns trigger strict review

### Security Design Principle
> **No single data point should be powerful enough to trigger or reject a payout.**

All payout and fraud decisions are based on **multi-signal verification, anomaly detection, and risk-aware review**, making the system more resilient against adversarial attacks.

---

## Website Features

- Worker onboarding
- Weekly insurance plan display
- Risk score visibility
- Protected earnings dashboard
- Automatic claim trigger alerts
- Payout confirmation screen
- Claim and disruption history

---

## Tech Stack

**Frontend:** React.js + Tailwind CSS  
**Backend:** Node.js  
**AI Layer:** Python  
**Database:** PostgreSQL  
**APIs:** Weather API, AQI API, Government Alert Data  
**Payments:** UPI Integration

---

## System Architecture

Worker / User
     ↓
Frontend Website
     ↓
Backend API
     ↓
AI Risk Engine
     ↓
Weather API / AQI API 
     ↓
Parametric Trigger Engine
     ↓
Payment Gateway / UPI
     ↓
Instant Worker Payout
