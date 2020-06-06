# MLOps with a Feature Store

https://towardsdatascience.com/mlops-with-a-feature-store-816cfa5966e9

## Summary

- What is MLOps?
- DevOps vs MLOps
- MLOps: versioned Code and Data
    - Data Versioning, Git-Style
    - Data Versioning with Time-Travel Queries and Incremental Pulling
- Hopsworks Feature Store
- End-to-End ML Pipelines with the Hopsworks Feature Store
- ML Pipelines are Stateful
- Feature Pipelines feed the Hopsworks Feature Store
- Model Training Pipelines start at the Feature Store
- Monitoring Online Models
- Summary

## Note

- Data Versioning, Git-Style
    - DVC
    - Pachyderm
- Data Versioning with Time-Travel Queries and Incremental Pulling
    - Delta Lake
    - Apache Hudi
    - Apache Iceberg
- Feature Store for ML
    - Hopsworks Feature Store
    - Feast
- ML workflow
    - DataOps workflow
    - Feature Store
    - MLOps workflow
- end-to-end ML pipelines
    - TensorFlow Extended (TFX)
    - MLFlow
- popular frameworks for data validation
    - TFX data validation
    - AWS Deequ 
- Feature Pipeline
    - Spark, PySpark, Pandas
    - TFX data validation, AWS Deequ 
- Model Training Pipeline
    - Apache Hudi -> Airflow
- validate model
    - Google’s What-If Tool
- Monitoring Online Models
    - Kafka -> Spark Streaming or Flink application
    - the error signals
        - Concept drift
        - Data drift
        - Feature pipeline changes


### Technical terms

### Important sentences

Here users can perform time-travel queries that return the data at a given point-in-time (commit-id), or the data for a given time-interval, or the changes to the data since a given point in time. 

### Sentences I couldn't understand

### Word etc

enterprise: 企て、事業、企業、冒険心
re-align: 再調整する
prerequisite: 前提条件、必要条件
fashion: 仕方、流儀、流行
suitable: 適切な、適当な、適した
ablation: 除去、切除、アブレーション
transparent: 透明な、明白な
enrich: 豊富にする、強化する、高める
decompose: 分解する、腐敗させる
cadence: リズム、抑揚、歩調
idempotent: 冪等である
obtrusive: 押し付けがましい、出すぎた、目立ちすぎる
well-defined: はっきり定義された、明確な
inobtrusive: 控えめな
backfill: 埋め戻す、穴埋めをする
impute: 帰する、負わせる、せいにする
descriptive: 記述的な、説明的な
sink: 沈没する、くぼむ、掃き溜め
periodically: 定期的に、周期的に
counterfactual: 事実関係、事実に逆らうこと
identify: 確認する、識別する、同一視する
property: 財産、資産、所有物、特質、特性、性質
