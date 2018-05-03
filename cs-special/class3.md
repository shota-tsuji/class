# 3

## What is "Snoop"
- Clockとは、CPUのClockであり、CPUから見てどれほどのサイクルかかるかを示す

## Direct Map
- 1cache-lineあたり、8byte

## Basic Protocol(A PU writes into again)
- 1,3番目のPUがどちらも、同じデータへの書き込みを行った？ので、いい感じにマージする必要がある。
- 整合性が確認できたのち、1番目をdirtyとする

## Berkeley's protocol
- Ownershipを入れた
- メモリから読み込みした最初は、Unowned Exclusive(メモリがownしているじょうたい)
- 書き込みをしたら、...
- copyとったら、copy先はUnowned Sharable

## MOESI protocol class
- 細かい内容はべつに重要でない
- メモリーを正しく管理しましょうというprotocolが複数ある、ということが大事
- 複数メモリの構成があると、このprotocol classは存在し続けるだろう

## Invalidate  vs. Udate
- 互いにデメリットがあるが、ネットワークのような機構を用いて改善を図っている(トーラスとか、リングとか)


## レポート課題
IPCを上げるためのもの
- パイプライン段数を適した値に
- キャッシュの構成は、データ取ってくる時間を縮めることができるので、よくする
