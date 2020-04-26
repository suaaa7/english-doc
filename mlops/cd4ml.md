# Continuous Delivery for Machine Learning

https://martinfowler.com/articles/cd4ml.html

## Summary

*CONTENTS*

- Introduction and Definition
- A Machine Learning Application for Sales Forecasting
    - Common challenges
- Technical Components of CD4ML
    - Discoverable and Accessible Data
    - Reproducible Model Training
    - Model Serving
    - Testing and Quality in Machine Learning
    - Experiments Tracking
    - Model Deployment
    - Continuous Delivery Orchestration
    - Model Monitoring and Observability
- The End-to-End CD4ML Process
- Where do We Go From Here?
    - Data Versioning
    - Data Pipelines
    - Platform Thinking
    - Evolving Intelligent Systems without Bias
- Conclusion

*SIDEBARS*

- Data Pipelines
- Machine Learning Pipelines
- Deployment Pipelines

## Note

- Cause of change
    - Data => Schema, Sampling over Time, Volume
    - Model => Algorithms, More Training, Experiments
    - Code => Business Needs, Bug Fixes, COnfiguration

Continuous Delivery for Machine Learning (CD4ML) is a software engineering approach in which a cross-functional team produces machine learning applications based on code, data, and models in small and safe increments that can be reproduced and reliably released at any time, in short adaptation cycles.

- DVC(Data Science Version Control)
    - it has multiple backend plugins to fetch and store large files on an external storage outside of the source control repository;
    - it can keep track of those files' versions, allowing us to retrain our models when the data changes;
    - it keeps track of the dependency graph and commands used to execute the ML pipeline, allowing the process to be reproduced in other environments;
    - it can integrate with Git branches to allow multiple experiments to co-exist;
    - Other tool
        - Pachyderm
        - MLflow Project

- Model Serving Patterns
    - Embedded model
        - MLeap
        - H2O
    - Model deployed as a separate service
        - MLaaS
            - Azure Machine Learning
            - AWS SageMaker
            - Google AI Platform
        - Kubeflow
        - MLflow Models
    - Model published as data
        - in this approach, the model is also treated and published independently, but the consuming application will ingest it as data at runtime.
        - We have seen this used in streaming/real-time scenarios where the application can subscribe to events that are published whenever a new model version is released, and ingest them into memory while continuing to predict using the previous version.
        - Software release patterns such as Blue Green Deployment or Canary Releases can also be applied in this scenario.

- Testing
    - Validating data
    - Validating component integration
    - Validating the model quality
    - Validating model bias and fairness

- Experiments Tracking
    - DVC
    - MLflow Tracking

- Deployment
    - Multiple models
    - Shadow models
    - Competing models
        - A/B test
        - Multi-Armed Bandits
    - Online learning models

- Continuous Delivery Orchestration
    - GoCD

- Model Monitoring and Observability
    - Model inputs
    - Model interpretability outputs
        - ELI5
        - LIME
    - Model outputs and decisions
    - User action and rewards
    - Model fairness
    - -
    - Tool
        - EFK
        - ELK
            - L: Logstash
        - Splunk

### Technical terms

- Data Pipelines
    - Pipeline is an overloaded term, especially in ML applications.
    - We want to define a "data pipeline" as the process that takes input data through a series of transformation stages, producing data as output.
    - Both the input and output data can be fetched and stored in different locations, such as a database, a stream, a file, etc.
    - The transformation stages are usually defined in code, although some ETL tools allow you to represent them in a graphical form.
    - They can be executed either as a batch job, or as a long-running streaming application.
    - -
    - For the purposes of CD4ML, we treat a data pipeline as an artifact, which can be version controlled, tested, and deployed to a target execution environment.

- Machine Learning Pipelines
    - The "machine learning pipeline", also called "model training pipeline", is the process that takes data and code as input, and produces a trained ML model as the output. 
    - This process usually involves data cleaning and pre-processing, feature engineering, model and algorithm selection, model optimization and evaluation.
    - -
    - While developing this process encompasses a major part of a Data Scientist's workflow, for the purposes of CD4ML, we treat the ML pipeline as the final automated implementation of the chosen model training process.

- Deployment Pipelines
    - In this article we have talked about data pipelines and ML pipelines, but there is another type of pipeline to understand: the Deployment Pipeline.
    - A deployment pipeline automates the process for getting software from version control into production, including all the stages, approvals, testing, and deployment to different environments.
    - -
    - In CD4ML, we can model automated and manual ML governance stages into our deployment pipeline, to help detect model bias, fairness, or to introduce explainability for humans to decide if the model should further progress towards production or not.

- holdout dataset?
    - ?

- EFK
    - Elasticsearch
    - FluentD
    - Kibana

### Important sentences

### Sentences I couldn't understand

Besides the code, changes to ML models and the data used to train them are another type of change that needs to be managed and baked into the software delivery process.

### Word etc

be subject to: 対象になる
fraction: 破片、断片、少量
comprise: 成る、含む、構成する
besides: の他にも
accordingly: それに応じて、適宜に
deterministic: 決定論的な
mature: 成熟する、満ちる
illustrate: 示す、説明する、入れる
retailer: 小売業者
combine: 結合する、結びつける
hand over: 手渡す、引き渡す
stifle: 息苦しくさせる、抑える、もみ消す
friction: 摩擦、衝突、不和
symptom: 症状、兆候、しるし
proof-of-concept: 概念実証、実証実験
stale: 新鮮でない、古臭い、つまらない
auditable: 審査可能な、監視可能な
straightforward: 正直な、複雑でない、簡単な
retrieve: 回収する、取り戻す
encourage: 元気づける、励ます、助長する
as well as: と同様に、及び
perishable: 腐敗しやすい
outlier: 外れ値
decentralize: 分散させる
flavour: あんばい、ぐあい、ほどあい
de-normalize: 非正規化
devise: 工夫する、考案する、発明する
convention: 慣習、しきたり、規則
overload: 過負荷
fetch: 取ってくる、引き出す
iterative: 反復の
formalise: 正式化する、公式化する
encompass: 取り囲む、包囲する、含む
invocation: 呼び出し、発動、実施
ingest: 搾取する、取り込む
language-agnostic: 言語に依存しない
applicable: 該当する、適用できる
suffice: 満足させる、十分である
relevant: 適切な、妥当な、関連のある
holistically: 全体的に
holdout: 抵抗、忍耐、踏ん張る
in-depth: 詳細な
centric: 中心の
deem: 思う、判断する
trunk: 幹、胴、主要部
hinder: 妨げる、邪魔する
pose: 見せかける、持ち出す
feed: 供給する、与える、養う
provision: 供給する
instrument: 取り付ける、備える
federated: 連邦化された
diverge: 分岐する、広がる、離れる
curate: 収集する、整理する
coordinate: 同等の、同格の、同格にする、整合する、調整する
feasible: 実行できる、うまくいきそうな
provenance: 起源、由来、出どころ
compatible: 互換性のある
