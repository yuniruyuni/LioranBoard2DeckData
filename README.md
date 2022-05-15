# IPS - ICB Point System for LioranBoard2
LB2でTwitchの視聴者に対してポイントを付与するための仕組みです

## 導入手順
### LB2の導入
割愛します
LB2をインストールしたうえで、Twitchとの連携、OBSとの連携を実施してください

### 設定ファイルの配置
LB2のインストール先に `IPS` という名前のディレクトリを作成し、本レポジトリの `ips.ini` を配置してください。

LB2を `D:\LioranBoard\` にインストールしているとした場合、 `D:\LioranBoard\IPS\ips.ini` というパスになっていればOKです。

### Deckの作成
任意の名称でDeckを作成してください

### 各種ボタンのインポート
本レポジトリの `deck` ディレクトリ配下の各種jsonファイルの中身をクリップボードにコピーし、LB2にてインポートしてボタンを作成します

## 設定ファイルの設定値の解説
### basic
本システムの基本的な項目を設定します

#### channel
本システムを導入する先、つまりあなたのチャンネル名を指定します。

私の場合は `icb_games` となります。

#### point_name
本システムを利用して付与するポイントの名称を指定することができます。

#### point_unit
本システムを利用して付与するポイントの単位を指定することができます。


### chat
チャットでコメントしてくれた人に対して付与するポイントに関する設定です。

#### expire_min
最終発言から何分間ポイントを付与し続けるかを設定します。

#### points_per_min
1分間に付与するポイントを設定します。

#### subscriber_additional_tier1
Tier1サブスクしてくれている視聴者に対して、先述の `points_per_min` に加えて追加で付与するポイントを設定します。

#### subscriber_additional_tier2
Tier2サブスクしてくれている視聴者に対して、先述の `points_per_min` に加えて追加で付与するポイントを設定します。

#### subscriber_additional_tier3
Tier3サブスクしてくれている視聴者に対して、先述の `points_per_min` に加えて追加で付与するポイントを設定します。

### bits
ビッツを投げてくれた視聴者に対して付与するポイントに関する設定です。

#### points_per_100bits
投げてくれたビッツ100bitsあたりに付与するポイントを設定します。

小数以下は切り捨てのため、例えば設定値として `100` を設定した場合に250ビッツを投げてくれた人に対しては、200ポイントが付与されます。

### raid
レイドしてくれた視聴者に対して付与するポイントに関する設定です。

#### points_for_raid
レイドしてくれた視聴者に対して付与するポイントを設定します。

#### points_per_raiders
レイドの人数に応じて追加で付与するポイントを設定します。レイダー1人につき、ここで設定したポイントが追加で付与されます。