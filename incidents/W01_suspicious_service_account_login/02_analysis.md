
Paste this:

---

```markdown
# Week 01 – Investigation Analysis

## 1. Initial Assessment

Authentication originated from external IP 185.212.44.73
geolocated to Eastern Europe. This deviates from expected
internal AWS subnet behavior in us-west-2.

Access method used: access key (not federated SSO).

Multiple failed attempts preceded successful authentication.

---

## 2. Behavioral Analysis

Observed actions indicate interactive exploration:

- GetCallerIdentity
- Bucket enumeration
- Object listing
- Direct retrieval of medical imaging files
- Write test followed by deletion

User agent indicates AWS CLI usage.

This behavior does not align with automated imaging pipeline job activity.

---

## 3. Impact Assessment

- Two medical imaging objects retrieved
- Multi-tenant production bucket accessed
- Cross-region authentication observed
- Service account possesses elevated permissions

Confirmed unauthorized external access to production data.

---

## 4. Severity Reassessment

Based on confirmed object retrieval from production
medical imaging storage, severity is escalated to:

CRITICAL

---

## 5. Escalation Decision

Immediate escalation to:
- Incident Response Coordinator
- Cloud Security Engineering
- GRC Team
- CISO

Regulatory exposure assessment required.
