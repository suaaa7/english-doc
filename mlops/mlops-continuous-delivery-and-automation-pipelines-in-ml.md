# MLOps: Continuous delivery and automation pipelines in machine learning

https://cloud.google.com/solutions/machine-learning/mlops-continuous-delivery-and-automation-pipelines-in-machine-learning

## Summary

The following topics are discussed:
    - DevOps versus MLOps
    - Steps for developing ML models
    - MLOps maturity levels
        - MLOps level 0: Manual process
        - MLOps level 1: ML pipeline automation
        - MLOps level 2: CI/CD pipeline automation

## Note

### Technical terms

- Training-Serving Skew
    - Training-serving skew is a difference between performance during training and performance during serving. This skew can be caused by:
        - A discrepancy between how you handle data in the training and serving pipelines.
        - A change in the data between when you train and when you serve.
        - A feedback loop between your model and your algorithm.
    - https://developers.google.com/machine-learning/guides/rules-of-ml/#training-serving_skew

- offline holdout dataset
    - テストデータセットのことっぽい
    - データの分割
        - トレーニングデータセット
        - バリデーションデータセット
        - テストデータセット、ホールドアウトデータセット

- custom code runtime

### Important sentences

This document is for data scientists and ML engineers who want to apply DevOps principles to ML systems (MLOps).
MLOps is an ML engineering culture and practice that aims at unifying ML system development (Dev) and ML system operation (Ops).
Practicing MLOps means that you advocate for automation and monitoring at all steps of ML system construction, including integration, testing, releasing, deployment and infrastructure management.

このドキュメントは、DevOpsの原則をMLシステム（MLOps）に適用したいデータサイエンティストとMLエンジニアを対象としています。 
MLOpsは、MLシステム開発（Dev）とMLシステム操作（Ops）を統合することを目的としたMLエンジニアリングの文化と実践です。 
MLOpsの実践とは、統合、テスト、リリース、展開、インフラストラクチャ管理など、MLシステム構築のすべてのステップで自動化と監視を提唱することを意味します。

---

### Sentences I couldn't understand

Deployment: 
In ML systems, deployment isn't as simple as deploying an offline-trained ML model as a prediction service.
ML systems can require you to deploy a multi-step pipeline to automatically retrain and deploy model.
This pipeline adds complexity and requires you to automate steps that are manually done before deployment by data scientists to train and validate new models.

---

CD is no longer about a single software package or a service, but a system (an ML training pipeline) that should automatically deploy another service (model prediction service).

---

Feature store

---

### Word etc

continuous integration    (CI)
continuous delivery       (CD)
continuous training       (CT)
exploratory data analysis (EDA) 

---

ingredient: 成分、材料
principle: 原理、原則、主義
pitfall: 落とし穴
diagram: 図、図式、図表
reliably: 確実に
exploratory: 探索的
criteria: 基準
implement: 実装する
assess: 評価する
adequate: 適切、十分、妥当
state-of-the-art: 最先端
highlight: 強調する
characteristic: 特徴、特性
transition: 遷移、移行
artifact: 人工物
handoff: 手渡すこと
degradation: 低下、劣化
address: 対処する
in practice: 実際には
staleness: 古さ
act as: として機能する
harness: 活用する、利用する
readiness: 覚悟、準備ができていること
aspect: 側面
ideally: 理想的には
decouple: 分離する
reproducible: 再現可能
isolate: 分離する
ensure: 確実にする、保証する
behavior: ふるまい、行動、習性
downstream: 下流
anomaly: 例外、異例
comply: 応じる、従う
consistent: 一貫している、矛盾のない
variance: 不一致、分散
compatibility: 適合性、互換性
undergo: 受ける、経験する
up-to-date: 最新の
demographic: 人口統計学の
reproducibility: 再現性
comparison: 比較、対象
lineage: 血統、系統
each time: するたびに
resume: 再開する
noticeable: 顕著な、目立つ
reliable: 信頼できる、確かな
iteratively: 反復的に、繰り返し
converge: 収束する
in turn: 順に、同様に
verify: 確認する、実証する
cope with: 対処する

---
