# Asset Inventory Summary: Orion HealthCloud Systems

## 1. Asset Inventory Purpose
This document provides a high-level inventory of Orion HealthCloud’s critical systems, their business function, data sensitivity, and operational ownership. The inventory supports incident response, impact assessment, and risk prioritization by identifying which systems are essential to healthcare service delivery and regulatory compliance.

This inventory reflects primary production assets and major supporting infrastructure.

---

## 2. Asset Classification Model

### Business Criticality Levels
Tier 1 – Mission Critical  
Service disruption directly impacts healthcare operations or patient data availability.

Tier 2 – Operationally Critical  
Service disruption significantly affects business operations but does not immediately halt clinical workflows.

Tier 3 – Supporting Infrastructure  
Indirect support systems with limited direct operational impact.

---

### Data Sensitivity Levels
High Sensitivity  
Protected Health Information (PHI), patient identifiers, clinical records.

Moderate Sensitivity  
Billing data, operational analytics, authentication credentials.

Standard Sensitivity  
System telemetry, configuration metadata, non-sensitive operational logs.

---

## 3. Critical System Inventory

### A-001: Medical Imaging Transfer Pipeline
Business Function  
Processes and stores diagnostic imaging uploads from healthcare providers.

Data Sensitivity  
High (PHI, medical imaging)

Business Criticality  
Tier 1 – Mission Critical

Primary System Owner  
Platform Operations – Imaging Services Team

Security Monitoring Coverage  
Authentication logging, infrastructure monitoring, partial data access monitoring

---

### A-002: Clinical Application Hosting Environment
Business Function  
Hosts Electronic Health Record (EHR) platforms and clinical workflow systems.

Data Sensitivity  
High (PHI, clinical treatment records)

Business Criticality  
Tier 1 – Mission Critical

Primary System Owner  
Application Platform Engineering

Security Monitoring Coverage  
Infrastructure monitoring, access control logging, limited internal service monitoring

---

### A-003: Identity and Access Management Platform
Business Function  
Authenticates workforce users, administrators, and service accounts.

Data Sensitivity  
Moderate (authentication credentials, access control data)

Business Criticality  
Tier 1 – Mission Critical

Primary System Owner  
Cloud Security Engineering

Security Monitoring Coverage  
Comprehensive authentication logging and alerting

---

### A-004: API Integration Gateway
Business Function  
Handles secure data exchange between Orion systems and external healthcare partners.

Data Sensitivity  
High (PHI, transactional healthcare data)

Business Criticality  
Tier 1 – Mission Critical

Primary System Owner  
Integration Services Engineering

Security Monitoring Coverage  
API access logging and traffic monitoring

---

### A-005: Analytics Data Warehouse
Business Function  
Aggregates operational and clinical data for reporting and analysis.

Data Sensitivity  
Moderate to High (aggregated PHI and operational metrics)

Business Criticality  
Tier 2 – Operationally Critical

Primary System Owner  
Data Engineering

Security Monitoring Coverage  
Access logging and infrastructure monitoring

---

### A-006: Backup and Disaster Recovery Environment
Business Function  
Stores replicated data and supports system restoration during outages or incidents.

Data Sensitivity  
High (replicated production data)

Business Criticality  
Tier 1 – Mission Critical

Primary System Owner  
Infrastructure Reliability Engineering

Security Monitoring Coverage  
Administrative access logging, limited restoration activity monitoring

---

### A-007: Security Monitoring Platform (SIEM)
Business Function  
Aggregates and analyzes security-relevant log data.

Data Sensitivity  
Moderate (security telemetry and investigation data)

Business Criticality  
Tier 2 – Operationally Critical

Primary System Owner  
Security Operations Team

Security Monitoring Coverage  
Full platform monitoring

---

## 4. Ownership Responsibilities
System owners are responsible for:

- Operational availability
- Configuration management
- Coordination with security during incidents
- Supporting investigation and remediation activities
- Maintaining system documentation

Security teams provide monitoring and response support but do not own business systems.

---

## 5. Asset Management Limitations
Current inventory limitations include:

- Incomplete documentation of legacy system dependencies
- Limited visibility into some third-party integrated components
- Ongoing infrastructure changes associated with platform modernization

Asset tracking is actively maintained but not fully comprehensive across all environments.
