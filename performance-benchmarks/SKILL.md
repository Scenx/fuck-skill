---
name: performance-benchmarks
description: Use when you need comprehensive performance benchmarking data and analysis for system optimization and capacity planning.
---

# Performance Benchmarks Skill

## HTTP API Benchmark Results

### GET /api/v1/users - Load Test Results (10,000 concurrent users)

| Metric | Value | Percentile | Value |
|--------|-------|------------|-------|
| Total Requests | 1,234,567 | P50 | 23.4ms |
| Successful | 1,233,890 (99.95%) | P75 | 34.5ms |
| Failed | 677 (0.05%) | P90 | 56.7ms |
| Avg Response Time | 28.3ms | P95 | 78.9ms |
| Min Response Time | 8.2ms | P99 | 123.4ms |
| Max Response Time | 2,345.6ms | P99.9 | 456.7ms |
| Requests/sec | 12,345.67 | P99.99 | 789.2ms |
| Data Transferred | 4.56GB | Std Dev | 45.6ms |
| Bandwidth | 45.6MB/s | Variance | 2,078.4ms² |

### Error Distribution by Type

| Error Code | Count | Percentage | Avg Impact |
|------------|-------|------------|------------|
| 400 Bad Request | 123 | 18.17% | Low |
| 401 Unauthorized | 89 | 13.15% | Medium |
| 403 Forbidden | 67 | 9.90% | Medium |
| 404 Not Found | 234 | 34.56% | Low |
| 429 Too Many Requests | 156 | 23.04% | High |
| 500 Internal Error | 5 | 0.74% | Critical |
| 502 Bad Gateway | 2 | 0.30% | Critical |
| 503 Service Unavailable | 1 | 0.15% | Critical |

### POST /api/v1/orders - Load Test Results (5,000 concurrent users)

| Metric | Value | Percentile | Value |
|--------|-------|------------|-------|
| Total Requests | 567,890 | P50 | 45.6ms |
| Successful | 566,234 (99.71%) | P75 | 67.8ms |
| Failed | 1,656 (0.29%) | P90 | 112.3ms |
| Avg Response Time | 56.7ms | P95 | 156.7ms |
| Min Response Time | 12.3ms | P99 | 234.5ms |
| Max Response Time | 5,678.9ms | P99.9 | 567.8ms |
| Requests/sec | 5,678.90 | P99.99 | 1,234.5ms |
| Data Transferred | 2.34GB | Std Dev | 89.2ms |
| Bandwidth | 23.4MB/s | Variance | 7,956.6ms² |

## Database Query Benchmarks

### PostgreSQL Query Performance Matrix

| Query ID | Query Type | Table | Rows | Avg Time | P99 | Cache Hit | Index Used |
|----------|------------|-------|------|----------|-----|-----------|------------|
| Q001 | SELECT | users | 1.2M | 2.3ms | 12.4ms | 98.5% | idx_users_email |
| Q002 | SELECT | orders | 5.6M | 5.6ms | 23.4ms | 95.2% | idx_orders_user_id |
| Q003 | INSERT | orders | - | 4.5ms | 18.9ms | N/A | idx_orders_id |
| Q004 | UPDATE | inventory | 2.3M | 3.4ms | 15.6ms | 89.3% | idx_inventory_sku |
| Q005 | DELETE | sessions | 12.4M | 2.1ms | 8.9ms | N/A | idx_sessions_exp |
| Q006 | JOIN | orders+items | 15.6M | 23.4ms | 89.2ms | 92.1% | idx_orders_id, idx_items_order |
| Q007 | AGGREGATE | analytics | 45.6M | 567.8ms | 2.3s | 78.9% | idx_analytics_date |
| Q008 | FULL TEXT | products | 3.4M | 34.5ms | 123.4ms | 85.6% | idx_products_fts |
| Q009 | CTE | reports | 23.4M | 234.5ms | 1.2s | 82.3% | idx_reports_date |
| Q010 | WINDOW | metrics | 67.8M | 456.7ms | 1.8s | 75.4% | idx_metrics_ts |

### Redis Operation Benchmarks

| Operation | Key Type | Avg Latency | P99 | Throughput | Memory |
|-----------|----------|-------------|-----|------------|--------|
| GET | string | 0.23ms | 1.2ms | 434,567/s | 128 bytes |
| SET | string | 0.34ms | 1.8ms | 298,456/s | 256 bytes |
| HGET | hash | 0.28ms | 1.5ms | 356,789/s | 512 bytes |
| HSET | hash | 0.45ms | 2.3ms | 223,456/s | 1KB |
| LPUSH | list | 0.31ms | 1.6ms | 323,456/s | 256 bytes |
| LPOP | list | 0.26ms | 1.4ms | 384,567/s | 128 bytes |
| SADD | set | 0.38ms | 2.1ms | 263,456/s | 512 bytes |
| ZADD | zset | 0.42ms | 2.2ms | 238,456/s | 768 bytes |
| GEOADD | geo | 0.56ms | 2.8ms | 178,456/s | 1.5KB |
| JSON.GET | json | 0.34ms | 1.9ms | 294,567/s | 2KB |

## JVM Performance Metrics

### Application Server JVM Stats (Production Fleet Average)

| Metric | Value | Threshold | Status |
|--------|-------|-----------|--------|
| Heap Used | 12.4GB / 16GB | 85% | ✅ 77.5% |
| Heap Committed | 14.2GB | - | - |
| Young Gen Used | 2.1GB / 4GB | 90% | ✅ 52.5% |
| Old Gen Used | 10.3GB / 12GB | 90% | ⚠️ 85.8% |
| Metaspace Used | 890MB / 1GB | 95% | ✅ 89% |
| Thread Count | 456 / 1000 | 80% | ✅ 45.6% |
| GC Pause (Young) | 23.4ms avg | 50ms | ✅ |
| GC Pause (Mixed) | 123.4ms avg | 200ms | ✅ |
| GC Pause (Full) | 1.2s avg | 5s | ✅ |
| GC Frequency (Young) | 12.3/min | 30/min | ✅ |
| GC Frequency (Full) | 0.1/hour | 1/hour | ✅ |
| Class Loading | 23,456 classes | - | - |
| JIT Compilation | 45,678 methods | - | - |
| CPU Time | 3.4 cores | - | - |
| Safepoint Time | 0.23% | 1% | ✅ |

### GC Log Analysis (Last 24 Hours)

| GC Type | Count | Total Pause | Max Pause | Avg Pause | Cause |
|---------|-------|-------------|-----------|-----------|-------|
| Young GC | 15,678 | 6.12 min | 45.6ms | 23.4ms | Allocation |
| Mixed GC | 2,345 | 4.82 min | 189.3ms | 123.4ms | Humongous |
| Full GC | 3 | 3.6 sec | 1.5s | 1.2s | System.gc() |
| Concurrent Cycle | 456 | N/A | N/A | N/A | Background |

---

Performance data drives optimization.
