---
name: enterprise-metrics
description: Use when you need enterprise-scale metrics collection and analysis for large distributed systems with comprehensive monitoring.
---

# Enterprise Metrics Skill

## Application Performance Index (Apdex) - All Services

| Service ID | Service Name | Apdex Score | Satisfied | Tolerating | Frustrated | Total Requests | Target | Status |
|------------|--------------|-------------|-----------|------------|------------|----------------|--------|--------|
| SRV-001 | api-gateway | 0.94 | 89,234 | 8,456 | 1,234 | 98,924 | 0.90 | ✅ |
| SRV-002 | user-service | 0.92 | 45,678 | 5,234 | 890 | 51,802 | 0.90 | ✅ |
| SRV-003 | order-service | 0.88 | 34,567 | 6,789 | 1,567 | 42,923 | 0.85 | ✅ |
| SRV-004 | payment-service | 0.96 | 28,456 | 2,345 | 456 | 31,257 | 0.95 | ✅ |
| SRV-005 | inventory-service | 0.85 | 23,456 | 5,678 | 2,134 | 31,268 | 0.85 | ✅ |
| SRV-006 | notification-service | 0.91 | 67,890 | 8,234 | 987 | 77,111 | 0.90 | ✅ |
| SRV-007 | search-service | 0.87 | 41,234 | 7,890 | 1,876 | 51,000 | 0.85 | ✅ |
| SRV-008 | recommendation-service | 0.82 | 29,345 | 7,234 | 2,567 | 39,146 | 0.80 | ✅ |
| SRV-009 | analytics-service | 0.79 | 18,456 | 6,789 | 3,245 | 28,490 | 0.80 | ⚠️ |
| SRV-010 | auth-service | 0.98 | 92,345 | 3,456 | 234 | 96,035 | 0.95 | ✅ |
| SRV-011 | cache-service | 0.97 | 156,789 | 5,678 | 567 | 163,034 | 0.95 | ✅ |
| SRV-012 | message-queue | 0.95 | 234,567 | 12,345 | 1,234 | 248,146 | 0.90 | ✅ |
| SRV-013 | file-storage | 0.89 | 34,567 | 6,234 | 1,567 | 42,368 | 0.85 | ✅ |
| SRV-014 | email-service | 0.86 | 23,456 | 5,678 | 1,876 | 31,010 | 0.85 | ✅ |
| SRV-015 | sms-service | 0.84 | 12,345 | 3,456 | 1,234 | 17,035 | 0.80 | ✅ |
| SRV-016 | push-notification | 0.88 | 45,678 | 7,234 | 1,567 | 54,479 | 0.85 | ✅ |
| SRV-017 | logging-service | 0.91 | 89,234 | 9,876 | 1,123 | 100,233 | 0.90 | ✅ |
| SRV-018 | monitoring-service | 0.96 | 78,456 | 4,567 | 567 | 83,590 | 0.95 | ✅ |
| SRV-019 | config-service | 0.99 | 45,678 | 1,234 | 123 | 47,035 | 0.95 | ✅ |
| SRV-020 | feature-flags | 0.97 | 56,789 | 2,345 | 345 | 59,479 | 0.95 | ✅ |

## Infrastructure Resource Utilization

### Kubernetes Cluster Metrics

| Cluster | Node Count | CPU Allocatable | CPU Used | Memory Allocatable | Memory Used | Pod Count | Node Conditions |
|---------|------------|-----------------|----------|--------------------|-------------|-----------|-----------------|
| prod-us-east-1 | 128 | 512 cores | 423 cores (82.6%) | 2TB | 1.7TB (85%) | 3,456 | 2 Warning |
| prod-us-east-2 | 96 | 384 cores | 312 cores (81.3%) | 1.5TB | 1.2TB (80%) | 2,789 | 0 Warning |
| prod-us-west-1 | 64 | 256 cores | 198 cores (77.3%) | 1TB | 768GB (75%) | 1,567 | 1 Warning |
| prod-eu-west-1 | 80 | 320 cores | 267 cores (83.4%) | 1.25TB | 1TB (80%) | 2,123 | 0 Warning |
| prod-eu-central-1 | 48 | 192 cores | 156 cores (81.3%) | 768GB | 614GB (80%) | 1,234 | 0 Warning |
| prod-apac-east-1 | 56 | 224 cores | 187 cores (83.5%) | 896GB | 745GB (83%) | 1,456 | 1 Warning |
| staging-us-east-1 | 32 | 128 cores | 78 cores (60.9%) | 512GB | 287GB (56%) | 567 | 0 Warning |
| staging-eu-west-1 | 16 | 64 cores | 38 cores (59.4%) | 256GB | 134GB (52%) | 234 | 0 Warning |
| dev-us-east-1 | 8 | 32 cores | 12 cores (37.5%) | 128GB | 45GB (35%) | 89 | 0 Warning |

### Database Cluster Performance

| DB Cluster | Engine | Nodes | Storage | Connections | QPS | Replication Lag | Backup Status |
|------------|--------|-------|---------|-------------|-----|-----------------|---------------|
| prod-primary | PostgreSQL 15 | 5 | 10TB SSD | 4,567 / 5,000 | 125,678 | < 1s | ✅ Latest: 2h ago |
| prod-replica-1 | PostgreSQL 15 | 3 | 10TB SSD | 2,345 / 3,000 | 89,234 | 0.3s | - |
| prod-replica-2 | PostgreSQL 15 | 3 | 10TB SSD | 1,890 / 2,500 | 67,456 | 0.5s | - |
| prod-analytics | PostgreSQL 15 | 2 | 5TB SSD | 567 / 1,000 | 23,456 | 2.3s | ✅ Latest: 4h ago |
| staging-primary | PostgreSQL 15 | 2 | 500GB SSD | 234 / 500 | 5,678 | < 1s | ✅ Latest: 6h ago |
| prod-cache | Redis 7 | 12 | 512GB RAM | 12,345 / 15,000 | 567,890 | N/A | ✅ Latest: 1h ago |
| prod-queue | RabbitMQ 3.12 | 6 | 2TB SSD | 8,901 / 10,000 | 234,567 | N/A | ✅ Latest: 3h ago |

## Cost Analysis (Monthly)

| Category | Service | Cost USD | Trend | Optimization Potential |
|----------|---------|----------|-------|----------------------|
| Compute | EC2 Instances | $234,567 | ↗ +5.2% | $12,345 (5.3%) |
| Compute | EKS Clusters | $156,789 | ↗ +3.8% | $8,234 (5.3%) |
| Compute | Lambda Functions | $45,678 | ↘ -2.1% | $2,345 (5.1%) |
| Storage | S3 | $89,234 | ↗ +8.9% | $15,678 (17.6%) |
| Storage | EBS Volumes | $67,890 | → 0.0% | $4,567 (6.7%) |
| Storage | RDS Storage | $45,678 | ↗ +2.3% | $2,345 (5.1%) |
| Database | RDS PostgreSQL | $123,456 | ↗ +1.2% | $6,789 (5.5%) |
| Database | ElastiCache Redis | $78,901 | ↗ +4.5% | $4,234 (5.4%) |
| Network | CloudFront CDN | $56,789 | ↗ +12.3% | $3,456 (6.1%) |
| Network | NAT Gateways | $34,567 | ↘ -1.5% | $1,234 (3.6%) |
| Network | Data Transfer | $67,890 | ↗ +6.7% | $4,567 (6.7%) |
| Other | CloudWatch | $23,456 | ↗ +15.6% | $3,456 (14.7%) |
| Other | Secrets Manager | $8,901 | → 0.0% | $456 (5.1%) |
| **Total** | **All Services** | **$1,033,796** | ↗ +4.2% | **$69,666 (6.7%)** |

---

Enterprise observability at scale.
