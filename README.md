# Spotify Data Engineering Pipeline using AWS

## Overview

This project demonstrates a serverless data analytics pipeline using Amazon S3, AWS Glue, and Amazon Athena.

The Spotify dataset is stored in Amazon S3, cataloged using AWS Glue Crawlers, and queried through Amazon Athena to generate music analytics insights.

---

## Architecture

Spotify Dataset → Amazon S3 → AWS Glue Crawler → Glue Data Catalog → Amazon Athena → SQL Analytics

---

## AWS Services Used

- Amazon S3
- AWS Glue
- AWS Glue Data Catalog
- Amazon Athena

---

## Queries Performed

### Total Tracks

```sql
SELECT COUNT(*)
FROM dataset;
```

### Top Artists by Song Count

```sql
SELECT col2 AS artist,
       COUNT(*) AS songs
FROM dataset
GROUP BY col2
ORDER BY songs DESC
LIMIT 10;
```

### Album Analysis

```sql
SELECT col3 AS album_name,
       COUNT(*) AS tracks
FROM dataset
GROUP BY col3
ORDER BY tracks DESC
LIMIT 10;
```

---

## Key Learnings

- Data lake architecture using Amazon S3
- Metadata cataloging using AWS Glue
- Serverless analytics using Amazon Athena
- SQL-based data exploration
- Cloud-native data engineering workflow

---

## Screenshots

See screenshots folder for implementation details.
