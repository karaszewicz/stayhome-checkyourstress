# Stay Home, Check Your Stress
- Call for Code Challenge 2020
- ソリューション紹介 https://youtu.be/UXoX6_Whm_U
- Apache License 2.0

## 開発メンバー
- [@kolinz](https://twitter.com/kolinz)
- [@mihoicchi](https://twitter.com/mihoicchi)
- [@miki_hiroshi_77](https://twitter.com/miki_hiroshi_77)

# 実装手順書
- こちらの[wiki](https://github.com/kolinz/stayhome-checkyourstress/wiki/Deployment)をご確認ください。

# システム概要
![system-overview](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/system-overview.png)

IBMクラウドの5つのサービスを使用しています。
| カタログ区分 | カテゴリ | サービス名 | 利用数　|
|:---|:---|:---|:---|
| サービス | AI | Watson Assistant | 1 |
| サービス | AI | Watson Discovery | 1 |
| サービス | データベース | Db2 | 1 |
| サービス | ストレージ | Object Storage | 1 |
| ソフトウェア | Webとアプリケーション | Node-RED App | 2 |

チャットボットに表示されるWatson Assistantから届く10個のテレワークに関するストレスチェックに関する質問に回答すると、Watson Discoveryから最適なアドバイスを取り出し、チャットボットに表示します。
エンドユーザーがチャットボットに回答した内容は、Db2上のテーブル「WORKATHOME」に格納され、Webブラウザ上で使用できるDb2のコンソールから、CSV形式でダウンロードすることが可能です。
ダウンロードしたデータを、人事担当者や医師などが確認し、長期の在宅勤務を行う従業員をサポートしてくために役立てることができるでしょう。

無料で始めたい場合は、Node-REDが２つ必要ですので、無料で使えるIBM Cloud ライト・アカウントの契約を2つ用意する必要があります。

# エンドユーザー側の概要
![enduser-interface](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/enduser-interface.png)

## ポータルサイト
![portal site](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/portal-site.png)

ポータルサイトに表示されたQRコードをスキャンすることで、チャットボットを利用することができます。
また、地図機能は今後開発する機能の１つで、在宅勤務をサポートする企業などの情報を共有することを想定し、拡張可能なサンプルデータを利用することができます。

## チャットボット概要
![line-bot](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/line-chatbot.png)

### 対応プラットフォーム
| アプリ名 | 対応状況 | URL |
|:---|:---|:---|
|LINE | 確認済み。 | https://line.me/en/download |
|Slack | 今後対応予定 |  |
|Mattermost | 今後対応予定 |  |

上記以外にリクエストがありましたら、Node-REDで可能な範囲でカスタマイズして対応させることができます。

テレワークに関して、運動、食事、睡眠、生活リズム、仕事の効率化、家族、感染症への不安など、10個の質問をします。
各質問には、"Strongly Disagree(強く同意しない)" から "Strongly Agree(強く同意する)" まで、1～6の範囲で回答してください。スコア集計を行い、スコアにあったアドバイスを表示します。
アドバイスは、孤独感やアルコールの過剰な摂取などテレワークにより生じるであろう要素を含みます。

# Recorded Db2
![recorded-db2](https://github.com/kolinz/stayhome-checkyourstress/blob/master/docs/insertdata-db2.png)
これらのチャットボット利用者の回答データはDb2に記録されています。企業や組織の衛生管理者は、Db2のコンソールを通じて従業員の回答データをダウンロードし、テレワークにおける健康管理サポートに役立てることができるでしょう。
