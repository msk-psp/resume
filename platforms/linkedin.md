# LinkedIn (English)

리크루터가 **키워드로 검색**하는 곳이라 기술명을 문장 안에 자연스럽게 깐다.
평문 입력란이므로 마크다운이 안 먹는다 — 아래 블록을 **그대로** 복사한다.

알려진 제한: Headline 220자 · About 2,600자 · 직무 설명 2,000자.
(플랫폼이 바꾸기도 한다. 잘리면 각 절의 「줄일 때」를 따른다.)

---

## Headline

```
MLOps / Platform Engineer — built an on-prem Kubernetes ML platform end to end (Pulumi, Airflow, Ray, Iceberg, MLflow)
```

<!-- 118자. 여유가 있으니 목표 직무에 맞춰 앞 라벨만 바꾸면 된다. -->

**줄일 때:** 괄호 안 스택을 3개로 줄인다 → `(Pulumi, Ray, Iceberg)`

---

## About

```
I build the machinery that lets ML research actually ship.

Over the past six months I designed, built and now operate my company's entire MLOps pipeline on bare-metal Kubernetes — ingestion, lakehouse, transformation, lineage, distributed training, and the experiment and model registry. On a two-person platform team I owned cluster construction end to end: I authored the majority of all 12 Pulumi stacks (93% of stack-code changes) and shipped 678 merged pull requests across 10 nodes, 235 running pods and 23 internal services.

What I care about is removing the human bottleneck rather than adding tools. Dataset preparation used to route through one person running hard-coded scripts over SSH for hours; it now runs on a schedule with Airflow, dbt and Apache Iceberg, with table-level lineage recorded automatically in DataHub. When asked to evaluate a GPU purchase, I measured ten days of DCGM telemetry, found 5.3% utilization with zero queued jobs, and showed the bottleneck was 1,112 GPU-hours held idle by dormant sessions — the money stayed unspent.

I work fast because I run AI coding agents continuously, and I keep that speed honest with verification gates: 719 unit tests in the platform SDK, CI checks that block tag/version drift and private-key commits, and 23 written incident post-mortems that turn each failure into a procedure.

Previously: AWS EMR/PySpark art-market pipelines and iOS engineering. Comfortable anywhere between the kernel and the notebook.

Stack: Kubernetes · Pulumi · Cilium · Airflow · dbt · Apache Iceberg · SeaweedFS · Ray/KubeRay · MLflow · DataHub · PostgreSQL · ClickHouse · Prometheus/Grafana · Dex/OIDC · Python
```

<!-- 약 1,650자. 2,600 한도 안. -->

**줄일 때:** 4문단(AI + 검증)을 먼저 살리고 5문단(이전 경력)을 줄인다 — 이전 경력은
Experience 에서 다시 보인다.

---

## Experience — HUINNO, Data Engineer (Dec 2025 – Present)

```
Designed, built and operate the company's entire MLOps pipeline on bare-metal Kubernetes — ingestion through distributed training and the model registry.

· Sole owner of cluster construction on a two-person platform team. Authored the majority of all 12 Pulumi stacks (93% of stack-code changes) across 10 nodes / 235 pods / 23 services — 678 merged PRs, 1,204 commits (92% mine).

· Designed and implemented every branch of the ETL pipeline (83% of 1,599 commits): 93% of the shared framework, 100% of three product pipelines. Researchers own domain ETL; the platform owns execution, lineage, verification and retries.

· Removed the single-person dependency in dataset preparation — work stalled whenever one data scientist was away. Airflow 3.x + dbt + Apache Iceberg now run Bronze/Silver/Gold on a schedule, lineage auto-recorded in DataHub.

· Cut training-data delivery 25x: an 8 TB transfer from 8.4 days to 7.8 hours. Opened Iceberg to ad-hoc SQL via PostgreSQL + pg_duckdb.

· Built the distributed-training foundation: 10 mixed-SKU GPUs in one KubeRay pool behind a pinned worker image and an SDK submission API. Consolidated 23 services onto one identity (Dex OIDC + oauth2-proxy) carried into Kubernetes RBAC.

· Quantified the research workflow and designed a reproducibility architecture from it — 51 branches, 67-88% of notebook cells carrying stored outputs. The cause was not missing tooling but results having no coordinates; built a contract stamping version, content hash, commit and seed onto a dataset at execution time.

· Reversed a GPU procurement decision with measurement: 10 days of DCGM/Prometheus showed 5.3% utilization and zero queued jobs, with 1,112 GPU-hours held idle by dormant sessions. Redirected from purchase to reclamation.

· Ran AI coding agents continuously to lift one person's throughput to team scale, backed by verification gates: 719 SDK unit tests, CI gates blocking tag/version drift and private-key commits, 23 incident write-ups and 30 PRDs.
```

<!-- 1,997자 — 2,000 한도 안 ✓ -->

**더 줄일 때:** 아래 순서로 뺀다.

1. 5번(distributed training) — 아직 도입 단계라 성과로는 약하다
2. 7번(Access) — About 과 겹친다
3. 2번(ETL)의 제품명 나열을 `93% of the shared framework` 까지만 남긴다

⚠ **8번(GPU 구매 결정)과 9번(AI + 검증)은 마지막까지 남긴다.** 다른 지원자와 갈리는 자리다.
