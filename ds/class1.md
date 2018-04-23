# 分散システム特論1回目

## 小テストとレポートがある．（manabaで提出）
## ひとつの教科書（改訂前）は，無料で手に入るらしい

## Characteristics derived from the definition
- Concurrency(平行性)
- No global clock
	- componentsがそれぞれ時計を持っているため，時間がずれてくる．
- Independent failures
	- 障害が起きた場合にもmessage passingで行う必要あり
	- ただ，壊れたcomponentsの特定は難しい
	- 対処法として，データのpriority（元データ）の置き場を決めたりしておくこともある．

## Examples of distributed systems
- distribution scale
	- もともとNFSが想定していたのはLAN内なので，今と比べると小さい

## MMOGs
- Eve online
- ゲームにはフィールドがある（フィールドは，状態で表される）
- その状態に対する多数のアクセスがあり，状態変更があり，それをたくさんのプレイヤーへ反映させる必要あり

## Financial trading
- FIX GatewayとReuters Gatewayがmessage passingしている

## Trends in distributed systems
- Pervasive networking and ... はいわゆるIoT

## pervasive networking and the modern internet
- IoTてきな要求
	- バストラッキング
	- 今までは人がwebにアクセスするための大きな回線がメインだった
	- IoTでは，細かなデータが多数回uploadされるようになってきたため，これまでと異なる

## Portable and handheld devices in a distributed system
- spontaneout interoperation
	- ある空間に入った際に，ネットワークサービスにアクセスできるか示してくれる(Wireless LANのInternet接続以外の使い道)
	- mdns

## 
- Paasは中間で，プラットフォームが提供されているので，自分でなにか作りたいときに使える
- Saasは，すでにアプリケーションとして提供されているもの
- Iaasは，低レイヤーで仮想マシンにアクセスできる

## Focuson resourc sharing
- benefitsは見過ごされがちだけど，どれだけすごいか説明

## Client-server computing
- よくある勘違い
	- × serverとclientが固定的である
	- あるリクエストが起きた際に，相対的にserverとclientが決まる
## More on client-server computing
- JavaではRemote Method Invocation(RMI)

## Securtity
- Integrity(改ざんされない)
- Availability(ランサムウェアはこれを対象とした悪い行為)

## Challenges for designing scalable distributed systems
- Contolling the performance loss
	- 配列でとっているか木構造でとっているかなどで，変更の際にかかるコストも低い方がよいというはなし
	
## Failure Handling
- 分散システムでは，Failureがあるときパフォーマンスを削り，機能は100%を保つようにする
	- Tolerateの意は耐える
	- Redundancyの意は冗長性（ファイルの複製をもっておくなど）
		- ただし，ファイルのバージョン管理という面でさらに厄介な話になる

## Transparency
- concealmentの意は隠す
- Access transparency
	- LocalとRemoteの区別なく，同じようにアクセスできるとよい
- Location trans
	- ユーザが自分でファイルの場所を調べてアクセスする手間が省けるとよい
