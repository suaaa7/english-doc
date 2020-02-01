# Stateful and Stateless Applications Best Practices and Advantages

https://www.xenonstack.com/insights/stateful-and-stateless-applications/

## Summary

While browsing the internet, the state generated and stored somewhere. Although the state generated in both types when the state stored on the server, it generates a session. This is called a Stateful application.

When the state stored by the client, it generates some data used for further requests while technically “Stateful” as it references a state, but the state stored by the client, so call it Stateless.

## Note

### Technical terms

REST: Representational State Transfer
sticky-mode: 
HA: High Availability、高可用性
FTP: File Transfer Protocol

### Important sentences

### Sentences I couldn't understand

Statelessness is a fundamental aspect of modern applications – every day; it uses a variety of stateless services and applications. It uses HTTP to connect in a stateless way, utilizing messages which are rendered and worked within the isolation of each other and client state.

---

Stateless Architecture is entirely different and better than Stateful. Stateless applications scale very poorly.

---

The server-side logic coded in such a way that it does not depend on the ‘previously-stored state’ of the client.
The state information sent along with each request, to the server through which the server proceeds with servicing the request.
Load-balancer doesn’t need to worry about routing requests to the same server, and truly uniform load balancing achieved.
The load balancer sends traffic to any server & request serviced well since client sending token or other needful info with each request.
JSON Web Token (JWT) widely used to create Stateless applications.

---

Storage attached to Stateless is ephemeral. Organizations must begin with Stateless Containers as they are more easily adapted to this type of architecture and separated from Monolithic applications and independently scaled.

### Word etc

drawback: 欠点、不利益、障害
horizontally: 水平に、横に
persistent: 永続の
grant: 承諾する、認める
crucial: 重要な
monolith: 一枚岩
omnipresent: 遍在する、どこにもいる、ある
consideration: 考慮
verify: 確認する、検証する
dumb: 物の言えない、無口な
distinct: 明確な、他と全く別な
self-contained: 自己完結型
matter: 問題、物事、問題となる、重要である
merely: 単に、わずかに
fundamental: 基本的な、根本的な
issue: 問題、発行する
relationship: 関係、繋がり
mainstream: 主流
present: 現在の、存在している
evenly: 均等に
concurrent: 同時、並行
purpose: 目的、動機
uniform: 一定、同質
wickedly: ひどい
consistency: 一貫性
maintainable: 維持できる、保持できる
eliminate: 除く、除去する
suffer from: わずらう、悩まされる
daunt: ひるませる、鋭気をくじく
paradigm: 模範、典型、パラダイム、一時代の支配的考え方を規定している科学的認識体系または方法論
mindset: 考え方
containerization: コンテナ化
consider: 考える
ephemeral: 一時的、はかない
monolithic: モノリシック、一枚岩の、一体となっている
philosophy: 哲学
slightly: わずかな
reproduce: 再現する
load: 負荷
exponentially: 指数関数的に
sophisticate: 洗練される、複雑化する
error-prone: エラーを起こしやすい
