# CS特別講義XI
- 書いていない項目は資料を読む

# 授業内容
- 課題提出は3回 later 4month, early 6month 6/22
- 最初の2,3回は試練
- パタヘネは，ヘネパタよりもソフトウェアエンジニアより

- instruction setとは，ソフトウェアから見た命令セット
- Micro-architectureとはハードウェアてきな配置のこと

## Instruction Pipeline
- ALUはレジスタファイルから2入力

## x86 Processor - Machine Code
- movは（レジスタへの）書き込み
- testはブランチの判断材料（if文などの条件分岐と組み合わせて使われる）

## Decode
- Instruction FormatがInstruction architectureそのもの

## Write back
- CPUはread-write architecture

## Pipelined Processing
- 1cycleあたり1/4命令
- 1cycleあたり1命令（4cycleで4命令てきな）
- 実際にはConditional Brunch

## Super Scalar
- レジスタに依存関係がなければ，命令を同時発行できるようにしよう
- IPC上がる
- そのためにはOut-Of-Order Instruction issueを解決する必要あり
- Hardwareの方で命令を入替えて発行されている(発行入替えはHardware,Software両方で行われる)

## HT
- プロセッサとしてのIPCは上がる

## Hyper Pipelined Technology
- より細かくして深さ増やす
- Intelの失敗談
- 電力を考慮していなかった(電圧の自乗に比例，より小さくすべきだった)

## 
- Super なんとか（3番めの絵）から，命令発行レベルでの並列性が必要
- そうするとIPCが2になる

## Hazard
- L1にInstruction Pointerが書き込まれるまで待ち

## Solution
- Before RenamingのMOVでAXに0を書き込む必要なし
- そこでRegister Renaming
