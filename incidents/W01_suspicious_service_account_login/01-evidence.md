# Week 01 – Evidence Log

## 1. Detection Event – Authentication Alert

### SIEM Alert Metadata
- Alert Name: Unusual Service Account Authentication
- Alert ID: SIEM-ATH-44721
- Detection Time (UTC): 2026-02-22T07:43:18Z
- Environment: Production
- Account: svc-image-transfer-prod
- Associated Asset: A-001 Medical Imaging Transfer Pipeline

### Authentication Log Snippet

```json
{
  "event_id": "evt-99384721",
  "timestamp": "2026-02-22T07:42:51Z",
  "event_type": "authentication_attempt",
  "account_name": "svc-image-transfer-prod",
  "source_ip": "185.212.44.73",
  "source_region": "Eastern Europe",
  "auth_method": "access_key",
  "result": "failure"
}
{
  "event_id": "evt-99384722",
  "timestamp": "2026-02-22T07:42:58Z",
  "event_type": "authentication_attempt",
  "account_name": "svc-image-transfer-prod",
  "source_ip": "185.212.44.73",
  "source_region": "Eastern Europe",
  "auth_method": "access_key",
  "result": "failure"
}
{
  "event_id": "evt-99384723",
  "timestamp": "2026-02-22T07:43:12Z",
  "event_type": "authentication_success",
  "account_name": "svc-image-transfer-prod",
  "source_ip": "185.212.44.73",
  "source_region": "Eastern Europe",
  "auth_method": "access_key",
  "session_id": "sess-8839201"
}

{
  "account_name": "svc-image-transfer-prod",
  "attached_policies": [
    "ImagingPipelineFullAccess",
    "S3MedicalImageWriteAccess",
    "CloudWatchLoggingAccess"
  ],
  "access_keys": [
    {
      "key_id": "AKIA-8837XK2",
      "status": "Active",
      "created_date": "2025-11-18T03:12:44Z",
      "last_used": "2026-02-22T07:43:12Z",
      "last_used_region": "eu-central-1"
    }
  ],
  "mfa_enabled": false
}

[
  {
    "timestamp": "2026-02-22T07:43:15Z",
    "event_name": "GetCallerIdentity",
    "service": "sts.amazonaws.com",
    "source_ip": "185.212.44.73",
    "region": "eu-central-1"
  },
  {
    "timestamp": "2026-02-22T07:43:18Z",
    "event_name": "ListBuckets",
    "service": "s3.amazonaws.com",
    "source_ip": "185.212.44.73"
  },
  {
    "timestamp": "2026-02-22T07:43:34Z",
    "event_name": "GetObject",
    "bucket": "ohc-medical-imaging-prod",
    "object_key": "tenant-data/hospital-17/imaging/2026-02-21-MRI-4421.dcm",
    "bytes_transferred": 5242880
  },
  {
    "timestamp": "2026-02-22T07:43:42Z",
    "event_name": "GetObject",
    "bucket": "ohc-medical-imaging-prod",
    "object_key": "tenant-data/hospital-23/imaging/2026-02-21-CT-1198.dcm",
    "bytes_transferred": 7340032
  },
  {
    "timestamp": "2026-02-22T07:44:01Z",
    "event_name": "PutObject",
    "bucket": "ohc-medical-imaging-prod",
    "object_key": "tenant-logs/test-upload.tmp",
    "bytes_transferred": 2048
  },
  {
    "timestamp": "2026-02-22T07:44:10Z",
    "event_name": "DeleteObject",
    "bucket": "ohc-medical-imaging-prod",
    "object_key": "tenant-logs/test-upload.tmp"
  }
]

