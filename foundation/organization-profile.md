# Organization Profile: Orion HealthCloud Systems

## 1. Organization Summary
Orion HealthCloud Systems is a healthcare SaaS and cloud infrastructure provider that hosts and manages clinical and business-critical systems for hospitals, outpatient clinics, and telehealth organizations. Orion operates a multi-tenant platform used to store, process, and transmit sensitive healthcare and billing data, including Protected Health Information (PHI). As a business associate to covered entities, Orion’s security posture directly impacts the availability, confidentiality, and integrity of client data and services.

## 2. Business Model and Services
Orion delivers subscription-based healthcare cloud services, including:
- Multi-tenant SaaS platform for clinical application hosting
- Medical imaging upload and storage services
- Data integration APIs for client systems and third-party partners
- Analytics and reporting platform for operational and clinical insights
- Disaster recovery support for client-hosted workloads

Service availability and data integrity are primary contractual requirements due to client reliance on Orion-hosted systems for patient care workflows.

## 3. Client Profile and Tenant Scope
Orion supports a diverse healthcare customer base, including:
- 48 regional hospitals
- 130 outpatient clinics
- 6 telehealth platforms

Orion’s platform design results in shared services across tenants, which increases operational complexity during security events and requires careful isolation and communication during incident response.

## 4. Data Types and Sensitivity
Orion processes and stores multiple high-sensitivity data categories, including:
- Protected Health Information (PHI)
- Patient identifiers (PII)
- Medical imaging files and metadata
- Appointment and telehealth session data
- Billing and payment-related data
- Authentication credentials and session artifacts

Data classification at Orion prioritizes PHI and associated identifiers as highest impact if exposed, altered, or made unavailable.

## 5. Locations and Operational Footprint
- Headquarters: Seattle, Washington
- Primary production environment: Oregon (cloud region and production services)
- Disaster recovery environment: Virginia (cloud region and backup workloads)

Orion’s operational footprint supports high availability and business continuity for healthcare customers across multiple states.

## 6. Workforce Overview
- Total employees: 620
- Information Technology staff: 40
- Security staff: 12

Orion maintains a lean security organization relative to client scope, requiring prioritization of critical risks, automation where feasible, and strong cross-team coordination during incidents.

## 7. Critical Business Services
Orion’s most business-critical services include:
- Medical imaging upload and transfer pipeline
- Clinical application hosting environment
- Identity and access management for customer-facing portals
- Integration APIs used by hospitals and partner platforms
- Backup and recovery services supporting service availability objectives

Disruption to these services may affect clinical operations, patient scheduling, imaging access, and revenue cycle functions for customers.

## 8. External Dependencies and Third Parties
Orion relies on third-party services and vendors for key operational capabilities, including:
- Cloud service providers for hosting and storage
- Managed monitoring and alerting services
- Identity provider and authentication services
- Healthcare software partners integrated through APIs
- Select managed service providers supporting infrastructure operations

Third-party risk is a recurring operational concern due to the interconnected nature of healthcare ecosystems.

## 9. Operating Assumptions for the Simulation
This simulation models Orion as an organization with a developing security program and realistic enterprise constraints, including:
- Continuous uptime demands from healthcare customers
- Resource constraints within security and IT teams
- Inconsistent enforcement of security controls across all systems
- Ongoing modernization efforts involving legacy and cloud-native workloads
- Compliance obligations that influence incident response decisions and timelines

This document defines the baseline organizational context for all incident scenarios documented in this repository.

## Document Control
- Owner: Security Program Office
- Last reviewed: 2026-02-22
- Version: 1.0
