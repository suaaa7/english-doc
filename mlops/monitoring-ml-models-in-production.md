# Monitoring Machine Learning Models in Production

https://christophergs.com/machine%20learning/2020/03/14/how-to-monitor-machine-learning-models/

## Summary

- Contents
    - 1. The ML System Lifecycle
    - 2. What makes ML System Monitoring Hard
    - 3. Why You Need Monitoring
    - 4. Key Principles For Monitoring Your ML System
    - 5. Understanding the Spectrum of ML Risk Management
    - 6. Data Science Monitoring Concerns
        - Model Input Monitoring
        - Model Prediction Monitoring
        - Model Versions
    - 7. Operations Monitoring Concerns
    - 8. Bringing Ops & DS Together - Metrics with Prometheus & Grafana
        - Metrics for Machine Learning
        - Practical Implementation
    - 9. Bringing Ops & DS Together - Logs
    - 10. The Changing Landscape

- Aim
    - This comprehensive guide aims to at the very least make you aware of where the complexity in monitoring machine learning models in production comes from, why it matters, 
    - and furthermore will provide a practical starting point for implementing your own ML monitoring solutions.

## Note

- six distinct phases in the lifecycle of an ML model
    - Model Building
    - Model Evaluation and Experimentation
    - Productionize Model
    - Testing
    - Deployment
    - Monitoring and Observability
    - -
    - Reference
        - Continuous Delivery for Machine Learning

- ML System 3 components
    - Code (and Config)
    - Model (ML System specific requirement)
    - Data (ML System specific requirement)
- Without a way to understand and track these data (and hence model) changes you cannot understand your system.

- monitoring
    - DS: the focus here is on statistical tests on model inputs and outputs
    - DevOps: system health, latency, memory/CPU/disk utilization
    - -
    - The whole team needs to work together on monitoring and speak each other’s language in order for the system to be effective.
    - That it’s important to define our terms to avoid confusion.

- what to monitor
    - Data Skews
        - reasons why this can happen
            - We designed the training data incorrectly
            - A feature is not available in production
            - Research/Live Data mismatch
            - Data Dependencies
    - Model Staleness
        - reasons why this can happen
            - Shifts in the environment
            - Changes in consumer behavior
            - Adversarial scenarios
    - Negative Feedback Loops

- published papers in MLOps
    - The ML Test Score: A Rubric for ML Production Readiness and Technical Debt Reduction (2017) Breck et al. (Google)
    - Software Engineering for Machine Learning: A Case Study (2019) Amershi et al. (Microsoft)

- monitoring
    - Data Science issues
        - data monitoring
        - prediction monitoring
    - Operations issues
        - system monitoring

- proxy values to model accuracy
    - model prediction distribution (regression algorithms) or frequencies (classification algorithms),
    - model input distribution (numerical features) or frequencies (categorical features), as well as missing value checks
    - model versions

- three pillars of observability
    - Metrics
        - Prometheus & Grafana
    - Logs
        - EFK
            - elasticsearch
            - fluentd
            - kibana
    - Distributed Traces

### Technical terms

### Important sentences

### Sentences I couldn't understand

### Word etc

compound: 混ぜ合わせる、調合する、いっそうひどくする、複利にする
cross-disciplinary: 学際的な
endeavor: 努力する、努力、試み
unsure: 不確かな、信頼できない、不安な
come into play: 活動し始める
realm: 領域、範囲、部門
entail: 必然的に伴う、必要とする
amid: の真ん中に、の真っ最中に
tweak: 微調整
entanglement: もつれさせること、もつれ、絡み合い
subtly: 微妙に
hopefully: うまくいけば、たぶん
sheer: まったくの、本当の、非常に
connotation: 言外の意味、含意、意味を含んでいる
isolation: 隔離、分離、孤立、単独
alongside: 並んで、一緒に、ともに
myriad: 無数
fabricate: 組み立てて製造する、作り上げる、偽造する
sway: ゆすぶる、ゆさぶる、振り動かす
rubric: 説明、注釈、規定、題名、題目
gauge: 測定用計器、ゲージ、測定する
invariant: 不変
swath: 帯
spectrum: 残像、連続体、範囲
grim: 厳格な、厳しい
enact: 制定する、規定する
mitigation: 緩和、軽減
disposal: 処分、処置、廃棄、思い通りにできる権利
upcoming: やがてやってくる、今後の
boil down to: 要約される、帰着する
full-blown: 本格的な、十分成熟した
uptime: 稼働時間
pillar: 柱、支柱、中心勢力
occasional: たまに、予備の
superset: 上位集合
noteworthy: 注目すべき、顕著な
liberally: 気前よく、寛大に、大量に
retention: 保有、保持、維持
if applicable: 該当する場合、妥当な場合
discrete: 分離した、別々の、不連続の、離散の
excel: 勝る、優れる
whilst: = while
