# 分散システム特論1回目（つづき）
## Discussion of the Web
- Opennessは技術的に開けているという意
- 新しく参入しやすい

## Scalability
- Flash crowdsはある日急に人気が出て、アクセスが多くなること。そしてその多さに対応できなくなること。
- slashdottedも同じ意味

# 分散システム特論2回目（つづき）
## Comparison of three ...
- Ultra-largeではlogオーダーのアルゴリズム必要

## Architectural elements
- 4つのものを合わせて、様式は組み合わせを見るとわかる

## Communicating entities
- System-orientedが最下層の考え方。下に行くにしたがって、より高い階層での考え方になる。

## 
- Remote invocationはオブジェクト指向

## Communication paradigms(cont'd)
- Indirect communication
	- 解決すべき課題が2つある(space uncouplingとtime uncoupling)
	- Indirect communicationによって解決
- publish subscribe systemsはみんなで解決のメーリングリスト(group communicationとここでは同義)
- tuple spacesはmessage queuesの進化系

# Napster
- Napsterを使うことでisoイメージのダウンロードを、いままでのサーバ&クライアントの帯域だけでなく、クライアント&クライアントの帯域も使うようにできた。
# Placement
- ユーザから見たらひとつの強力なサーバに見えるが、実際にはたくさんのPCを組み合わせ、その間をやりとりするようにすれば、パフォーマンス上がる。

# Layering
- 各レイヤーのインターフェースが同じであれば、入れ替えができる
- 各レイヤーをそれぞれで開発できる

# Three-tier architecture
- スケーラビリティを上げるために、3つの機能(presentation logic, application logic, data logic)を、それぞれ異なるマシンに担当させる。
- Cons
	- レイテンシーが大きい（Web上での、お客さん逃げちゃう3秒ルールへの影響あり）


# Architectural patterns
- Brokerageはお手紙みたいに、宛先指定すれば届けておいてくれる？
- Reflectionはプログラムが動的に自身？を書き換える。

# Limitations of middleware
- 問題が起こったら、結局下のレイヤーが大事になってくる？
- harmfulはここでは、オーバーヘッドになって遅くなるという意味

# 
- 非同期分散
	- メッセージがいつまでに届くかを前提としておかないシステム

# Event ordering
- 全体のとけいを持たないかわりに、因果関係を時計として用いる。

# Failure model
- fail-stopは、一部が壊れたら全部が止まる。
- それ以外は、一部だけがうまく行かない例。
- crashより下は、プロセスは生きているが、放っておくと整合がとれなくなってくるもの。
- omissionは通信路で起きるエラー
- send-omissionとreceive-omissionも含めて、メッセージがうまく届かないエラー。
- arbitraryはいちばんやっかいで、ばらばらなメッセージが送られてくる。

## Threats
- 偽証とかデータ改ざんとか
- 対抗策のってる

# 分散システム特論3回目
## Terminology
- Communication subsystemには、ケーブルとかも含まれる。

## Performance
- transmission time
	- メッセージ長/データ転送レート
	- data ransfer rateは実際に送信されるデータ量
	- total system bandwidthは理論値？
## Performance(cont'd)
- レイテンシーの例
