# LinkedIn (English)

아래 평문을 해당 입력란에 복사합니다. 2026-10-02 이력서 기준입니다.
글자 수는 작성 문구의 길이이며 플랫폼 제한을 확인한 값은 아닙니다.

## Headline

```
Data Engineer | On-premises MLOps & Data Platforms | Kubernetes, Airflow, Iceberg, DuckDB | From Researcher Interviews to Implementation
```

## About

```
I turn research workflows into shared data platforms, from requirements discovery to implementation and operations.

At HUINNO, I independently learned a new medical domain and on-premises MLOps, interviewed researchers, and designed and built an in-house platform from scratch. Data was scattered across nodes, generation code was unversioned, and knowledge of data production and storage depended on a few people. Datasets moved through SSH copies; models and performance were shared in Notion without linked records of data, code and environments.

I translated those problems into requirements for shared storage, automated pipelines, versioning and lineage. I assigned clear roles to Airflow, dbt, Apache Iceberg and DataHub, and built ingestion, Bronze/Silver/Gold transformations and SQL access. SeaweedFS provides S3-compatible storage and an Iceberg REST Catalog. For dimension-table generation, I resolve the latest metadata location from the catalog and pass it to DuckDB rather than infer versions from filenames.

On a two-person platform team, I was the sole owner of cluster construction: 10 on-premises nodes managed through 12 Pulumi stacks (September 2026). I also led hands-on hardware work, reclaiming RAM and NVMe drives from idle machines, selecting and replacing network equipment, and adjusting memory and disk configurations to fit workloads.

I built manifest freeze/restore tools, MLflow tracking and a model registry with SeaweedFS artifact storage. Research-code integration and end-to-end data-to-model reproducibility validation are in progress. I work with researchers to define ownership: they own domain ETL; the platform owns execution, lineage, validation and retries.

Previously, I led a data engineering team and built AWS EMR/PySpark art-market pipelines, with earlier experience in backend, frontend and iOS development.

Core stack: Python, SQL, Airflow, dbt, Iceberg, SeaweedFS, DuckDB, PostgreSQL, DataHub, MLflow, Kubernetes, Pulumi, AWS, PySpark.
```

## Experience — HUINNO, Data Engineer (Dec 2025 – Present)

```
Led requirements discovery, design and implementation of an in-house MLOps platform in a new medical domain.

· Interviewed researchers and analyzed existing workflows. Identified scattered datasets, unversioned generation code, producer-dependent knowledge and SSH-based transfers; translated these into shared-storage, automation, versioning and lineage requirements.

· Sole owner of cluster construction on a two-person platform team: 10 on-premises bare-metal nodes and 12 Pulumi stacks (September 2026). Led RAM/NVMe reclamation from idle machines, network-equipment selection and replacement, and NUMA, memory and disk adjustments.

· Built Airflow/dbt Bronze/Silver/Gold pipelines with DataHub lineage, including the shared framework, research-data pipelines, MIMIC-IV and operational ETL. Defined researcher ownership of domain ETL and platform ownership of execution, validation and retries.

· Built SeaweedFS S3 storage and Iceberg REST Catalog integration with NVMe/HDD tiers and PostgreSQL + pg_duckdb query access. Resolved the latest catalog metadata location for DuckDB dimension-table generation instead of guessing versions from filenames.

· Built manifest freeze/restore tools and MLflow tracking/model registry with SeaweedFS artifact storage to connect data versions, code and environments. Research-code integration and end-to-end reproducibility validation remain in progress.

· Implemented missing-data recovery and integrity checks, environment-specific services and buckets, and Dex/OIDC-to-Kubernetes RBAC access control. Built a shared KubeRay training environment to support research-code migration.
```

## Certifications & Languages

```
Engineer Information Processing — HRD Korea, November 2017
English — OPIc Advanced Low (AL)
```

## 줄일 때

Experience의 마지막 운영·접근 제어 항목을 먼저 축약합니다. About에서는 이전 경력과 기술 목록을 줄일 수 있습니다. 인터뷰 기반 문제 정의, 본인 역할, 데이터 설계와 재현 검증의 진행 상태는 유지합니다.
