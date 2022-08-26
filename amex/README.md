# 概要

kaggleのコンペ「American Express - Default Prediction」に参加した時のコードです。
https://www.kaggle.com/competitions/amex-default-prediction

# notebook構成
ノートブックの用途ごとに prefixを分けています。

- 1xx <= データ量が多いため inputファイルを分割するためのnotebook（bigquery使用することにしたので不使用）
- 2xx <= bigqueryを使った集約データを作成（SQLのメモ）
- 3xx <= 後続処理の時短のため、train, test, valid のrawデータ、前処理、特徴量選択したものをそれぞれH5ファイルとして保存するコード
- 4xx <= ベンチマークとなる単純な学習・予測
- 5xx <= パラメーターチューニング
- 6xx <= カスタム評価関数とカスタム目的関数
- 7xx <= 特徴量選択
- 8xx <= 各種の学習・予測
- 9xx <= アンサンブル


# ディレクトリ構成
- / <= notebook
- /input/ <= train, test, valid の元データ
- /output/submission <= submit ファイル
- /temp_data/agg/ <= train, testをbigqueryを使ってcustomer_ID毎に集約したデータ
- /temp_data/h5/ <= 後続処理の時短のため中間処理データをH5ファイルとして保存する場所


# 特記事項
- 初めてkaggleのコンペに参加しました（機械学習の学習を始めて２ヶ月時点）
- そのため改善の余地は多々あると思います。

# メモ

## inputファイルの行数
train_data.csv
5531452

test_data.csv
11363763

sample_submission.csv
924622

train_labels.csv
458914


