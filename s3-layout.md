

sh# mc ls minio/warehouse/tripdata/tripdata/data
[2025-10-19 06:45:22 UTC]  52MiB STANDARD 00000-1-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:22 UTC]  53MiB STANDARD 00001-2-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:21 UTC]  44MiB STANDARD 00002-3-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:22 UTC]  47MiB STANDARD 00003-4-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:22 UTC]  50MiB STANDARD 00004-5-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:22 UTC]  51MiB STANDARD 00005-6-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:22 UTC]  44MiB STANDARD 00006-7-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:21 UTC]  41MiB STANDARD 00007-8-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:21 UTC]  42MiB STANDARD 00008-9-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:21 UTC]  42MiB STANDARD 00009-10-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:21 UTC]  37MiB STANDARD 00010-11-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:21 UTC]  36MiB STANDARD 00011-12-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet
[2025-10-19 06:45:21 UTC]  32MiB STANDARD 00012-13-5ad11515-c3b9-4f6e-a9b7-5fc731b78cc7-0-00001.parquet

sh# mc ls minio/warehouse/tripdata/tripdata/metadata
[2025-10-19 06:45:23 UTC] 2.8KiB STANDARD 00000-05d89834-6f51-4b8c-aca9-419859874bdd.metadata.json
[2025-10-19 06:45:22 UTC]  11KiB STANDARD 6e69660a-ef62-4af6-a5bd-2e782926a8c3-m0.avro
[2025-10-19 06:45:22 UTC] 4.3KiB STANDARD snap-8368504387769468041-1-6e69660a-ef62-4af6-a5bd-2e782926a8c3.avro

sh# mc cat minio/warehouse/tripdata/tripdata/metadata/00000-05d89834-6f51-4b8c-aca9-419859874bdd.metadata.json
```json
{
  "format-version": 2,
  "table-uuid": "db398dbb-85e0-464b-b212-7eb763ab793a",
  "location": "s3://warehouse/tripdata/tripdata",
  "last-sequence-number": 1,
  "last-updated-ms": 1760856322888,
  "last-column-id": 19,
  "current-schema-id": 0,
  "schemas": [
    {
      "type": "struct",
      "schema-id": 0,
      "fields": [
        {
          "id": 1,
          "name": "VendorID",
          "required": false,
          "type": "long"
        },
        {
          "id": 2,
          "name": "tpep_pickup_datetime",
          "required": false,
          "type": "timestamp"
        },
        {
          "id": 3,
          "name": "tpep_dropoff_datetime",
          "required": false,
          "type": "timestamp"
        },
        {
          "id": 4,
          "name": "passenger_count",
          "required": false,
          "type": "double"
        },
        {
          "id": 5,
          "name": "trip_distance",
          "required": false,
          "type": "double"
        },
        {
          "id": 6,
          "name": "RatecodeID",
          "required": false,
          "type": "double"
        },
        {
          "id": 7,
          "name": "store_and_fwd_flag",
          "required": false,
          "type": "string"
        },
        {
          "id": 8,
          "name": "PULocationID",
          "required": false,
          "type": "long"
        },
        {
          "id": 9,
          "name": "DOLocationID",
          "required": false,
          "type": "long"
        },
        {
          "id": 10,
          "name": "payment_type",
          "required": false,
          "type": "long"
        },
        {
          "id": 11,
          "name": "fare_amount",
          "required": false,
          "type": "double"
        },
        {
          "id": 12,
          "name": "extra",
          "required": false,
          "type": "double"
        },
        {
          "id": 13,
          "name": "mta_tax",
          "required": false,
          "type": "double"
        },
        {
          "id": 14,
          "name": "tip_amount",
          "required": false,
          "type": "double"
        },
        {
          "id": 15,
          "name": "tolls_amount",
          "required": false,
          "type": "double"
        },
        {
          "id": 16,
          "name": "improvement_surcharge",
          "required": false,
          "type": "double"
        },
        {
          "id": 17,
          "name": "total_amount",
          "required": false,
          "type": "double"
        },
        {
          "id": 18,
          "name": "congestion_surcharge",
          "required": false,
          "type": "double"
        },
        {
          "id": 19,
          "name": "airport_fee",
          "required": false,
          "type": "double"
        }
      ]
    }
  ],
  "default-spec-id": 0,
  "partition-specs": [
    {
      "spec-id": 0,
      "fields": []
    }
  ],
  "last-partition-id": 999,
  "default-sort-order-id": 0,
  "sort-orders": [
    {
      "order-id": 0,
      "fields": []
    }
  ],
  "properties": {
    "owner": "root",
    "created-at": "2025-10-19T06:45:15.726278395Z",
    "write.format.default": "parquet",
    "write.parquet.compression-codec": "zstd"
  },
  "current-snapshot-id": 8368504387769468000,
  "refs": {
    "main": {
      "snapshot-id": 8368504387769468000,
      "type": "branch"
    }
  },
  "snapshots": [
    {
      "sequence-number": 1,
      "snapshot-id": 8368504387769468000,
      "timestamp-ms": 1760856322888,
      "summary": {
        "operation": "append",
        "spark.app.id": "local-1760856235276",
        "added-data-files": "13",
        "added-records": "38908842",
        "added-files-size": "599767374",
        "changed-partition-count": "1",
        "total-records": "38908842",
        "total-files-size": "599767374",
        "total-data-files": "13",
        "total-delete-files": "0",
        "total-position-deletes": "0",
        "total-equality-deletes": "0",
        "engine-version": "3.5.6",
        "app-id": "local-1760856235276",
        "engine-name": "spark",
        "iceberg-version": "Apache Iceberg unspecified (commit 7dbafb438ee1e68d0047bebcb587265d7d87d8a1)"
      },
      "manifest-list": "s3://warehouse/tripdata/tripdata/metadata/snap-8368504387769468041-1-6e69660a-ef62-4af6-a5bd-2e782926a8c3.avro",
      "schema-id": 0
    }
  ],
  "statistics": [],
  "partition-statistics": [],
  "snapshot-log": [
    {
      "timestamp-ms": 1760856322888,
      "snapshot-id": 8368504387769468000
    }
  ],
  "metadata-log": []
}
```

```

```