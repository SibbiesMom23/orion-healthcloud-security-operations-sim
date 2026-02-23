# Baseline Risk Register: Orion HealthCloud Systems

## 1. Risk Register Purpose
This register documents known security, operational, and compliance risks present in the Orion HealthCloud environment at the start of the simulation. These risks represent accepted or partially mitigated conditions that may increase the likelihood or impact of future security incidents.

Each risk includes a description, potential impact, and current mitigation status.

---

## 2. Risk Severity Model

Impact Levels:
- High: Significant regulatory, operational, or data exposure risk
- Medium: Noticeable operational or security risk requiring monitoring
- Low: Limited impact or early-stage risk condition

Status Definitions:
- Accepted: Known risk without active remediation
- Mitigating: Remediation effort in progress
- Monitoring: Tracked but not currently prioritized

---

## 3. Active Risk Register

### R-001: Over-Privileged Service Accounts
**Category:** Identity and Access Management  
**Description:** Several service accounts have broader permissions than required for operational tasks. Periodic access reviews are inconsistent.  
**Potential Impact:** Unauthorized access to sensitive systems if credentials are compromised.  
**Severity:** High  
**Status:** Monitoring  

---

### R-002: Incomplete Asset Inventory
**Category:** Asset Management  
**Description:** Not all cloud resources and legacy system dependencies are fully documented or tracked.  
**Potential Impact:** Undetected exposure or delayed response during incidents.  
**Severity:** Medium  
**Status:** Mitigating  

---

### R-003: Limited Monitoring of Internal Service Communications
**Category:** Detection and Monitoring  
**Description:** Logging coverage for some service-to-service interactions is incomplete.  
**Potential Impact:** Lateral movement or unauthorized internal activity may go undetected.  
**Severity:** High  
**Status:** Monitoring  

---

### R-004: Vendor Integration Visibility Gaps
**Category:** Third-Party Risk  
**Description:** Monitoring and security validation of some external integrations is limited.  
**Potential Impact:** External compromise could propagate into hosted environment.  
**Severity:** High  
**Status:** Monitoring  

---

### R-005: Backup Restoration Not Recently Tested
**Category:** Resilience and Recovery  
**Description:** Full system restoration procedures have not been exercised at scale.  
**Potential Impact:** Delayed recovery during major service disruption or ransomware event.  
**Severity:** High  
**Status:** Accepted  

---

### R-006: Container Image Vulnerability Backlog
**Category:** Vulnerability Management  
**Description:** Known vulnerabilities remain in some container images awaiting remediation.  
**Potential Impact:** Exploitable software components in production workloads.  
**Severity:** Medium  
**Status:** Mitigating  

---

### R-007: Inconsistent Vendor Security Assessments
**Category:** Governance and Compliance  
**Description:** Not all third-party providers undergo formal security review prior to integration.  
**Potential Impact:** Increased supply-chain attack exposure.  
**Severity:** Medium  
**Status:** Monitoring  

---

### R-008: Irregular Incident Response Exercises
**Category:** Incident Preparedness  
**Description:** Full operational incident response exercises are not conducted regularly.  
**Potential Impact:** Reduced response coordination efficiency during real incidents.  
**Severity:** Medium  
**Status:** Monitoring  

---

### R-009: Phishing Awareness Training Compliance Gaps
**Category:** Workforce Security  
**Description:** Security awareness participation varies across departments.  
**Potential Impact:** Increased credential compromise risk.  
**Severity:** Medium  
**Status:** Mitigating  

---

### R-010: Configuration Drift in Cloud Environments
**Category:** Cloud Security  
**Description:** Limited automated enforcement of configuration standards across all workloads.  
**Potential Impact:** Misconfigurations leading to exposure or control bypass.  
**Severity:** High  
**Status:** Monitoring  

---

## 4. Risk Governance Notes
Risks documented in this register are reviewed periodically by the Governance, Risk, and Compliance team. Risk prioritization is influenced by operational impact, regulatory exposure, and resource availability.

Future incident investigations may reference this register to determine whether observed events align with known risk conditions.
