# このレポジトリの存在意義
普段、ブログを書くときには、このレポジトリは直接いじらない

このレポジトリは別の環境にブログ執筆環境を移行するときや、環境が壊れてしまって再度作り直さないといけないときに使うもの。

# 使い方
clone するときは

> git clone --recursive

# 全体の構成についてのメモ
このレポジトリは配下に4つのサブモジュールを持つ。

**origin（大元のレポジトリ）**：大元の記事データと、記事を管理するためのjsonファイル（DB代わり）、記事を変換して下記のレポジトリに再配置するためのpythonスクリプトを持つ

**zenn**:変換後のzennの記事データと、remoteにpushするためのshellスクリプトを持つ

**qiita**:変換後のqiitaの記事データと、remoteにpushするためのshellスクリプトを持つ（デプロイ関数もactions内に持つ）

**hugo**:変換後の個人ブログ用の記事データと、remoteにpushするためのshellスクリプトを持つ（デプロイ関数もactions内に持つ）