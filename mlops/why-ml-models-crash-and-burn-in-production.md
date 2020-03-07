# Why Machine Learning Models Crash And Burn In Production

https://www.forbes.com/sites/forbestechcouncil/2019/04/03/why-machine-learning-models-crash-and-burn-in-production/#7c1db76c2f43

## Summary

Most importantly, keep your best data scientists and engineers on the project after it's in production.
In contrast to classic software projects where, after deployment, your operations team handles it and engineers move on to build the next big thing, a lot of the technical challenge in ML and AI systems is keeping them accurate.
Automating retrain pipelines, online measurement, and A/B testing is hard to get right.
Your strongest technologists will enjoy this combination of intellectual challenge and business impact.

最も重要なことは、最高のデータサイエンティストとエンジニアが本番稼働後もプロジェクトに参加することです。
展開後、運用チームがそれを処理し、エンジニアが次の大きなものを構築する従来のソフトウェアプロジェクトとは対照的に、MLおよびAIシステムの技術的な課題の多くはそれらを正確に保つことです。
再トレーニングパイプライン、オンライン測定、A / Bテストを自動化するのは困難です。
あなたの最強の技術者は、知的挑戦とビジネスへの影響のこの組み合わせを楽しむでしょう。

## Note

### Technical terms

- concept drift
    - アウトプットデータとインプットデータの関係が、時間や外部影響によって変化すること
    - 対策
        - Forgetting
            - 定期的に再学習する
        - Detectors
            - 発生したタイミングを検知して、再学習を行う
        - Dynamic Ensemble
            - 利用するモデル構造自体は複数モデルのensembleから作られ、時間とともに、各モデルを評価し、重み付けする
            - アウトプットが正しく予測されるモデルはリワードとして重みを増やす
            - 一方、間違って予測されたモデルはペナルティとして、重みを減らす
        - Contextual
            - いくつかの隠れた因果関係のパターンに対する複数モデルを作成する
            - 予測するデータがインプットされた場合に、どのモデルを利用するかを判断する
            - 基本的に、各隠れ因果関係のパターンは様々な統計情報で表す
    - https://recruit.gmo.jp/engineer/jisedai/blog/concept-drift-detection-and-handling/

### Important sentences

### Sentences I couldn't understand

### Word etc

marginal: あまり重要でない、限界の
bedrock: 根底、根本
faulty: 欠点のある、誤った
assumption: 仮定、仮説
the moment: 途端に
deteriorate: 悪化させる、悪化する
intuitive: 直観の
malicious: 悪意のある、意地の悪い
interact: 相互に作用する、互いに影響し合う
grocery: 食品雑貨店
confident: 確信して
specifically: 明確に、特に、具体的に言うと
readmission: 再入院
insurance: 保険、保険料
prior distribution: 事前分布
debacle: 崩壊、失敗
heuristic: 発見を助ける、発見的な(手法)、必ず正しい答えを導けるわけではないが、ある程度のレベルで正解に近い解を得ることができる方法
opportunity: 機会

---
