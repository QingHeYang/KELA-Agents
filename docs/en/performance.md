# Performance

## Test Environment

| Item | Specification |
|------|---------------|
| Test Data | 600,000 rows × 85 columns |
| Data Scale | ~51 million cells |

## Memory Usage

| Phase | Memory Usage |
|-------|--------------|
| Normal Usage | 300 ~ 500 MB |
| Data Import Phase | ~3.6 GB |
| Peak Memory | ~6 GB |

## Recommended Configuration

| Data Scale | Recommended RAM |
|------------|-----------------|
| Small (< 100K rows) | 4 GB |
| Medium (100K ~ 500K rows) | 8 GB |
| Large (500K+ rows) | 16 GB |

## Performance Characteristics

### Advantages

- **Fast Query Speed** - Based on SQLite database, efficient even with large datasets
- **Timely Memory Release** - Memory returns to normal levels after import completes
- **Incremental Processing** - Data imported in batches to avoid excessive resource usage

### Notes

- Data import phase is the peak memory usage, ensure sufficient available memory
- Close other memory-intensive applications when importing large files
- Row count is unlimited, but constrained by computer memory

## Capacity Limits

| Limit | Value | Description |
|-------|-------|-------------|
| Excel Files | Max 3 | Per workspace |
| Total Columns | Max 100 | Combined across all tables |
| Row Count | Unlimited | Depends on computer memory |

> Limits are applied on a first-come basis. For example: 3 files with 30, 40, and 50 columns respectively - only the first two can be imported (70 columns total), the third exceeds the 100-column limit.
