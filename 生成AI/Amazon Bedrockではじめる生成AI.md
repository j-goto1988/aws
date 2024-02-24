# Amazon Bedrockの基本
## Amazon Bedrockとは
基盤モデルを活用した生成AIアプリケーションを簡単に構築できる<br>
基盤モデルは事前にとトレーニングされた大規模な機械学習モデル<br>
幅広い基盤モデルがある(テキスト生成、埋め込み、画像生成)<br>
サーバーレスで、API経由で基盤モデルにアクセスする<br>

## データセキュリティ・コンプライアンス
お客様のデータが基盤モデルの学習やAWSおよびサードパーティーのモデルプロバイダーに共有されることは無い<br>
AWS PrivateLinkを使うことでAmazon VPCとAmazon Bedrock間のプライベート接続を実現<br>
全ての転送・保管されるデータは常に暗号化<br>
HIPPA コンプライアンス等標準規格に準拠<br>


# 生成AIアプリ開発をサポートするAmazon Bedrockの各種機能
## お客様独自のデータを基盤モデルに活用する方針
下記の二つがある
RAGはプロンプトの調整
Fine Tuning/Continued Pre-trainingはモデル自体の更新

### RAG
ドキュメントを格納したデータベースを準備<br>
ユーザーが質問すると、データベースの中に関連するドキュメントがあるかを検索<br>
検索にヒットした場合はそのドキュメントの内容を返す<br>
ユーザーからの問い合わせとドキュメントの内容をプロンプトに含めて基盤モデルに入力<br>

### Knowledge Bases for Amazon Bedrock
AWSでRAGを実現できる<br>
検索対象のデータをS3に保存する<br>
ドキュメントを検索可能な形で保存するベクトルDBを用意して選択する<br>
Amazon Bedrockがドキュメントを検索可能な形に変換した後、データベースに格納する<br>

### Fine Tuning/Continued Pre-training
お客様独自のデータをAmazon Bedrockの基盤モデルに追加で学習させて独自のカスタムモデルを構築するという手法で、2つの方法がある<br>
Fine Tuningはラベル付きデータを新たに学習して特定のタスクの精度を高める手法<br>
Continued Pre-trainingは大量のラベル無しデータを用いてモデルに新たなドメイン知識を習得させる手法<br>
どちらもS3にデータを追加する<br>

## データや外部 API との連携の
### Agent
ユーザーの入力を複数の小さなタスクに分割し、タスクごとに適切なAPIを呼び出すことで回答を生成する
### Agents for Amazon Bedrock
AWSでAgentを実現できる<br>
Agents for Amazon Bedrockを使わない場合はLangChain (OSS)とAWS Step Functionsで実現できる<br>

## 評価によるユースケースに適した基盤モデルの選択
### Model Evaluation on Amazon Bedrock
複数の基盤モデルをコード不要で比較・評価しユースケースに最適なモデルを選択可能<br>

### バッチ推論
S3ファイルに記載した複数のプロンプトを非同期に推論できる機能<br>
スロットリングを回避し大規模なジョブを確実に処理<br>

## 生成 AI アプリの適切な利用状況の維持と安定的稼働
### Guardrails for Amazon Bedrock
自社ポリシーに従って、ユーザーの入力や基盤モデルの出力から望ましくないコンテンツを制御するためのガードレールを定義

### Model Invocation Logging
基盤モデルの入出力結果をログとして記録

### Provisioned Throughput
スループットを確保し安定したAPI実行が可能

# Amazon Bedrockを今日からはじめよう
Amazon Bedrock サービスページ内Playgroundから基盤モデルの利用をお試しできる
