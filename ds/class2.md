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
