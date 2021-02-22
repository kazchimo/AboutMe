# AboutMe

## 森山 和樹
- [Github](https://github.com/kazchimo)
- [Twitter](https://twitter.com/Kazuki_Moriyama)
- [Zenn](https://zenn.dev/kazchimo)
- [Qiita](https://qiita.com/KtheS)
- [slides](https://slides.com/kazukimoriyama)


## 略歴
一橋大学商学部在学中に株式会社KOSKAを共同創業。
CPOとしてラズパイなどを使用したIoTシステム基盤・データ集計/計算基盤・ビジネスインサイトWebアプリケーションの開発全般と、開発計画のロードマップ作成、エンジニアリング組織マネジメント/教育などを担当。

## 職務経歴（概要）
### ソフトウェア開発
- IoTシステムの開発
    - 技術選定/実装/運用: 2年
- Webアプリケーションの開発
    - Scala, TypeScript/JavaScript, Ruby、Goあわせて3年
    
### 教育/チームビルディング
#### 教育
- 自社・他社で働くことができるようなエンジニア教育実績が何度もある

#### チームビルディング
- 0から組織を立ち上げるにあたってのエンジニアマネジメント
- スクラム・アジャイルでの開発体制の構築

### 業務外活動
#### 趣味のプログラミング
- [pfds-dotty](https://github.com/kazchimo/pfds-dotty)
    - [純粋関数型データ構造](https://www.amazon.co.jp/%E7%B4%94%E7%B2%8B%E9%96%A2%E6%95%B0%E5%9E%8B%E3%83%87%E3%83%BC%E3%82%BF%E6%A7%8B%E9%80%A0-Chris-Okasaki/dp/4048930567) という本の内容をScala3(dotty)を用いて実装してみた(途中まで)
- [agora](https://github.com/kazchimo/agora)
    - Scala × ZIOを用いて作成した仮想通貨の自動取引システム
    - 鋭意作成中
- [tats](https://github.com/kazchimo/tats)
    - Python3.9でScala likeな関数型プログラミングのパーツ
    
#### 記事
- [0からScalaを本番導入して感じたこと・考えたこと](https://qiita.com/KtheS/items/c91df9f641dcbf1a2d22)
- [Goにproperty based testingを布教したい](https://zenn.dev/kazchimo/articles/07c5636f2dbced)

世に出ていない知見を提供することで大きな影響を与えることができるという経験を何度かした。
これがモチベーションになり普段から世に足りていない知見というものを積極的にアウトプットしようとしている。

#### プレゼンテーション
- [Scalaの導入と学び](https://slides.com/kazukimoriyama/scala)
    - プレScalaMatsuri2020で招待枠で発表
    - 自社でScalaを導入した経験を共有した
    
#### OSSコミット
勉強のためや軽微な修正のためにたまにOSSにコミットします。

- [ZIO](https://github.com/zio/zio/pulls?q=+is%3Apr+author%3Akazchimo+sort%3Aupdated-desc+)
- [cats](https://github.com/typelevel/cats/pulls?q=is%3Apr+author%3Akazchimo+sort%3Aupdated-desc+)
- [shapeless](https://github.com/milessabin/shapeless/pulls?q=is%3Apr+author%3Akazchimo+sort%3Aupdated-desc+)
- [fast-check](https://github.com/dubzzz/fast-check/pulls?q=is%3Apr+author%3Akazchimo+sort%3Aupdated-desc+)

...etc
    
### プログラミングスキル
#### Scala(2.12/2.13 dotty)
- 2019年の６月頃から業務での使用を開始
- 知識が0の状態からプロダクション運用可能な状態まで持っていった経験あり
- PlayFramework/cats...etcなど有名なライブラリは一通り業務での経験あり

#### TypeScript(3.x/4.x)/JavaScript(ES6)
- 共に2018年の９月頃から業務での使用を開始
- バックエンドで使用したことはなく、Reactでの使用がメイン
- viewの一歩手前ほどまでのアーキテクチャ構成・データモデリングなどをメインに行ってた

#### Go(1.1x)
- 2019年の６月から業務での使用を開始
- 知識が0の状態からプロダクション運用可能な状態まで持っていった経験あり
- AWS LambdaでのスクリプトやラズパイでのIoTシステム開発などに使用

#### Python(3.5~3.9)
- 2018年から使用を開始
- AWS Lambdaでのスクリプトやバックエンド、ハードウェアでのIoTシステム開発などに使用
- 業務上でクラスタリングなどのPythonが得意とするアルゴリズムを作成した経験あり

#### Ruby(2.x)
- 2018年から使用を開始
- Rails5.x系を業務で使用した経験あり

### その他の技術
#### AWS
Lambda、ESC/Fargate、DynamoDB、Glue、Amplify、AppSync、ES2、S3、API Gateway...etc

#### クリーンアーキテクチャ
Scala、Go、Pythonで実装経験あり

#### CI/CD
circleci、GitHub Actions

#### その他
Terraform、Datadog、Docker/docker-compose、RaspberryPi3/4

## 職務経歴
### 株式会社KOSKA(2018/10 ~)
#### IoTデータのエクスポートサービスの開発
- 収集したIoTデータを顧客ごとの要望に応じたデータ形式に変換、統計量を計算して出力するサービス
- ユーザのリクエストを待ち受けて計算処理を走らせるGateway的な部分と実際の計算処理を担う部分に分かれる
  
##### 課題と技術選定
- 計算実行基盤がスクリプト的なものからバッチまで考えられ柔軟に対応する必要があった
    - 計算をキックする部分をScalaで書き、計算処理のハンドリングを非同期に安全に実装した
- 計算部分はScala以外の計算が得意な言語で実装したかった
    - 計算基盤は別サービスとしてPythonに切り出して計算ロジックをPythonしかかけないメンバーが実装できるようにした
    
#### Raspberry PiとRFIDセンサーを用いたIoTデータ取得システムの開発
- RFIDセンサーを用いて工程内の稼働状況を取得し、データ送信するシステムをラズパイ上に構築
- 作業者にセンサーが読み取っていることを通知するため、付属ディスプレイでのフロント表示も必要

##### 課題と技術選定
- 今までの経験からハードウェアこそ固い開発をする必要があることがわかっていた
    - PythonからGoに乗り換えて型の恩恵を教授
    - クリーンアーキテクチャで実装し実際のハードウェアを抽象化したテストを書くことができた
- ハードウェアへのデプロイは非常に手間がかかる
    - Pythonとは違いGoでシングルバイナリに丸め込むことでデプロイを簡易化
- 一つのプロセスでセンシング・付属ディスプレイの管理・リモートとのデータシンクなどの複数の要件をこなす必要があった
    - go routineとchannelを用いたeventベースの設計をし、各ユースケースの疎結合な実装・実行を達成
- 使用しているライブラリの関係でC linkが必要なコンパイルを実行する必要があり、その環境構築が大変だった
    - コンパイラサービスとしてdockerに丸めどの環境でも即時に同一なコンパイルを実施できるようにした
    
#### Raspberrypi管理システムの開発
- 工場に設置するラズパイのアルゴリズム・出荷工場などを管理する社内アプリケーション

##### 課題と技術選定
- 今後のIoTシステム運用で中枢となるアプリケーションで間違いが許されないアプリケーションで固さが必要
    - Scalaを採用することでビジネスロジックを安全に表現した
- 社内初のScalaアプリケーションだったため品質の担保が必要だった
    - クリーンアーキテクチャで実装し、各レイヤーの手本を作成してなれていないメンバーでも実装しやすいようにした
    - DDDを採用し各メンバーがビジネスロジックを十分に把握した上で認識の齟齬がないアプリケーション開発を行った
    - 規定人数のapproveが必要なコードレビューを実施しお互いにコードへの知見を深めていった
    
#### ラズパイ上で稼働するブートシステムの開発
- IoTシステムのラズパイが起動してはじめに実行されるプログラム
- サーバー上の設定値の取得・ネットワーク/ハードウェアマネージ・センシングを担当する別プログラムの取得/実行がメインの役割

##### 課題と技術選定
- ラズパイのハードウェア部分と密に連携するコードを書く必要があった
    - 豊富な実績とライブラリが存在するPythonを採用
- Pythonとはいえ一つのバグが致命的なのでなるべく固いアプリケーションを書く必要があった
    - Type Hintとpyrightというライブラリを使用して他の型あり言語と遜色のない型による恩恵を享受
- ハードウェアと絡むためテストが非常にしにくいコードになっていた
    - クリーンアーキテクチャで実装し直すことで各レイヤごとのロジックを単体でテストしやすいような設計にした
