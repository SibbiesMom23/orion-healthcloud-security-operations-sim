# Week 01 – Suspicious Service Account Authentication

## Case ID
OHC-W01-2026-001

## Date Opened
2026-02-22

## Environment
Production

## Initial Severity
High

## Status
Investigating

---

## Executive Summary

On 2026-02-22, the Security Operations team detected unusual authentication
activity involving the production service account `svc-image-transfer-prod`.

The account, which normally authenticates only from internal infrastructure
in the primary production region, successfully authenticated from an external
IP address geolocated to Eastern Europe following multiple failed attempts.

The account was observed using access key authentication outside of its
expected job execution window. Controlled containment measures were initiated,
including temporary key deactivation and preservation of IAM state for
forensic review.

Preliminary log analysis confirms interactive activity including bucket
enumeration and object access within the medical imaging storage environment.
Further investigation is underway to determine scope, data exposure, and
regulatory impact.
