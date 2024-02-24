# インフラ技術への投資の必要性
## 生成AIスタック
基盤モデルを活用したアプリケーション<br>
基盤モデルを使って構築するためのツール<br>
モデルを学習、推論するためのインフラストラクチャ<br>

## 何故インフラ技術への投資を続けているのか
インフラをチップレベルから設計することで最適化<br>
幅広いインフラの選択肢を用意することで、需要の変化に柔軟に対応<br>

# 生成AIの進化を支えるインフラ技術～AWS Trainium、Inferentia2によるイノベーションと活用事例～
## AWS自社設計MLチップ搭載インスタンス
### AWS Inferentia
初代ML推論専用アクセラレータで、高性能かつ低価格
### AWS Trainium
高性能ML学習向けアクセラレータで、学習コストを最大50%削減
### AWS Inferentia2
第2世代ML推論向けアクセラレータで、大規模言語モデルに対応

## Amazon EC2 Trn1/Trn1nインスタンス
AWS自社設計高性能ML学習向けアクセラレータAWS Trainiumを搭載したインスタンス<br>
最大16個のAWS Trainiumを搭載<br>
同等のGPUインスタンスと比較し最大50%低価格を実現<br>
512GBの高速HBM2メモリ搭載<br>
最大1600GbpsのEFAネットワーク帯域に対応<br>
Trn1上で学習したモデルのデプロイ先は自由<br>
3万以上のAWS TrainiumアクセラレータをEC2 UltraClusterにデプロイ、6エクサフロップスの演算性能を提供<br>

## Amazon EC2 Inf2インスタンス
最もコスト効率の高い生成AIモデルに対応した推論向けインスタンス<br>
第2世代ML推論チップAWS Inferentia2搭載<br>
Inf1と比較して最大4倍高いスループット、10分の1の低レイテンシーを実現<br>
384GBの高速HBM2メモリ搭載<br>
大規模言語モデル（LLM）を単一サーバ上にデプロイ可能<br>
小規模モデルの学習にも対応<br>

## AWS Trainium
第2世代Neuronコアv2<br>
32GB HBMメモリスタック<br>
NeuronLink-v2→高帯域、低遅延なデバイス間接続<br>
専用Collective Computeエンジン→分散学習、推論を行う際に、演算と通信をオーバーラップ<br>

## AWS Neuron
AWS TrainiumとAWS Inferentiaアクセラレータ上のMLワークロードを最適化するSDK

# AWS Trainium、Inferentia2活用事例
Amazon SearchはInf2を活用し2倍の高速化を達成

# 今後の展望
## Anthropicとの戦略的提携を発表
## Trn1、Inf2インスタンスを東京リージョンで一般提供開始
## AWS Trainium2
生成AI基盤モデル、大規模言語モデルのトレーニング向け第2世代アクセラレータチップ<br>
第1世代AWS Trainiumと比較して、最大4倍のトレーニング性能、3倍のメモリ容量、2倍のエネルギー効率を実現<br>
基盤モデル、大規模言語モデルのトレーニング時間を大幅に短縮<br>
Amazon EC2 Trn2インスタンスには16個のAWS Trainium2チップが搭載、最大10万個のTrainium2チップからなるEC2 UltraClusterに導入することで、最大65エクサフロップスの計算性能を提供<br>
