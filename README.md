## 経歴

2017年 入社

2017年 6月 ~ 2018年 09月 

メインフレーム 運用チーム配属(スケジューラー)

オープン側で言うと、JP1で実現していることを自社開発されたシステムを使用してメインフレームで

JP1 とは
[Link]("https://e-words.jp/w/JP1.html")

#####　JCLのサンプル

ファイルのコピー
```js
//IEBGENER JOB ,,CLASS=A,MSGCLASS=A,MSGLEVEL=(1,1)
//*
//*        COPY PS DATASET
//*
//IEBGENER EXEC PGM=IEBGENER
//SYSPRINT DD SYSOUT=*
//SYSUT1   DD DISP=SHR,DSN=XXXX.PS.DATASET1
//SYSUT2   DD DISP=SHR,DSN=XXXX.PS.DATASET2
//SYSIN    DD DUMMY
```

SORT

```js
//SORT     JOB ,,CLASS=A,MSGCLASS=A,MSGLEVEL=(1,1),REGION=8192K
//*********************************************************************
//*        Sample JCL for SORT
//*        ===================
//*********************************************************************
//*********************************************************************
//*        SORT EXEC JCL FOR IBM SYSTEM
//*
//*        SYSIN CONTROL CARD
//*          SORT  FIELDS=(X,Y,FM,Z)
//*            |           | | |  |
//*            |           | | |  SORT PATTERN A;ASCEND
//*            |           | | |               D;DESCEND
//*            |           | | KEY TYPE CH;CHR
//*            |           | |          BI;BIN
//*            |           | |          ZD;ZONE
//*            |           | |          PD;PACK
//*            |           | KEY LNG(BYTE)
//*            |           KEY START POINT
//*            SORT;MERGE
//*          RECORD TYPE=F|V,LENGTH=value
//*
//*        SORTWKnn DATASET MUST BE PLACED ON 2314 DISK ONLY.
//*        OTHERWISE, IER042A - UNITS ASGN ERROR.
//*        SORT/MERGE UTILITY INSTALLED FROM OS/360 MVT SYSTEM.
//*********************************************************************
//SORT     EXEC PGM=SORT,PARM='MSG=AP'
//SORTLIB  DD DSN=SYS1.SORTLIB,DISP=SHR
//SYSOUT   DD SYSOUT=*
//SORTWK01 DD UNIT=SORT,SPACE=(CYL,10),VOL=SER=SORT01
//SORTWK02 DD UNIT=SORT,SPACE=(CYL,10),VOL=SER=SORT02
//SORTWK03 DD UNIT=SORT,SPACE=(CYL,10),VOL=SER=SORT03
//SORTWK04 DD UNIT=SORT,SPACE=(CYL,10),VOL=SER=SORT04
//SORTWK05 DD UNIT=SORT,SPACE=(CYL,10),VOL=SER=SORT05
//SORTWK06 DD UNIT=SORT,SPACE=(CYL,10),VOL=SER=SORT06
//SORTIN   DD DISP=SHR,DSN=USR1.PARMLIB(SORTDATA)
//SORTOUT  DD SYSOUT=*,DCB=(RECFM=FB,BLKSIZE=4000,LRECL=80)
//SYSIN    DD *
  SORT  FIELDS=(40,10,CH,A)
  RECORD TYPE=F,LENGTH=80
  END
//*

```


ジョブやプログラム、データセットなど本番で利用するリソースを登録・変更・削除する担当
また、ジョブのトラブル対応のため夜勤

主な使用スキル：JCL, MSP(OS)


2018年 10月 ~ 2021年 12月

メインフレーム 基盤構築・運用保守チーム配属

メインフレームに関するインフラすべての担当

ベンダーとやり取りしながら、機器のリプレイスや新たなシステムの導入の実施

トラブル対応(365日24時間)

運用をしていく中で必要な場合にCOBOLでの開発


#### 作成したプログラム

*   ログ管理システム用ID作成コマンドの自動生成
*   災害対策用コマンドの自動生成
*   災害対策対象ファイル抽出プログラム
*   災害対策コマンドの実行結果自動監視

使用スキル: COBOL, JCL, MSP(OS)

#### 主な案件

*   災害対策システム構築
*   仮想テープリプレイス作業

PTFアップ(OSのバージョンアップ時の確認作業), パラメータや監視設定の変更など

* * *

## 保有資格
社会人になってから取得した資格一覧

ITは関係ないがTOEICは675点(大学4回生で取得)

資格名: ITパスポート

認定日: 2017-02-05

* * *

資格名: LPIC-1 (5年経つため期限切れ状態)

認定日: 2017-05-29

* * *

資格名: ITIL® Foundation Certificate in IT Service Management

認定日: 2017/06/02

* * *

資格名: 基本情報技術者試験

認定日: 2018-5-16

* * *

資格名: RPA Developer Foundation Diploma

認定日: 2018-12-08

* * *

資格名: AWS Certified Solutions Architect – Associate

認定日: 2019-07-17

* * *

資格名: AWS Certified Solutions Architect - Professional

認定日: 2021-07-11


* * *

## 独学

仕事とは関係ないが、興味があったため勉強していた分野

HTML, CSS, JavaScript, TypeScript, React, Python, AWS

今後は独学で勉強していたことを仕事にしていきたい

#### 使用した教材

*   Progate
*   PyQ
*   Udemy
*   書籍


* * *

#### 過去に作成したもの

転職活動を機に過去に勉強兼遊びで作成したアプリの振り返りを行う

見出しは、アプリを作るときに決めた名前と大体の機能が完成した時の日付

#### 晩御飯決めアプリ 2019/03/31

##### どんなアプリか

料理名を入力しておいて、ボタンを押すと入力してる料理からランダムで表示


##### 作ろうと思った理由

一人暮らしをしていて、晩御飯に何を食べようかいつも迷っていたためランダムで決めてくれるものがあればいいなと思い作成


##### 使用した技術

HTML, CSS, Python(Flask)


##### 振り返ってみて

初めて作るアプリっぽいもので試行錯誤しながら作成した記憶
機能としては一応できたが、レスポンシブ対応ができなくて挫折


写真しか残っていない

<img src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/foodchoice.png" />

* * *

### SHARE PUT　2019/8/3

・どんなアプリか

勉強したことをアウトプット、他の人の投稿を見てインプットするアプリ

共有のSHAREとINPUT・OUTPUTのPUTを取って、SHARE PUT


・　作ろうと思った理由

勉強したことをまとめることは良いと思いつつも記事にするのはなかなか大変なのでSNS感覚で投稿できるものが
あればいいなと思い作成


・　使用技術

HTML, CSS, Python(Django), heroku


・　どうなったか

使い物にはならないが、ある程度の形になったことは嬉しかった。

レスポンシブ対応もできたはず

初めてどんなアプリを作ろうか、デザインをどうしようか、どうやってプログラムを組むのかなど考えて作ってて楽しかったし、できたときは嬉しかった

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/shareput.mp4"></video>

* * *

### MyBookRecord 2019/09/21

・どんなアプリか

読んだ本の登録とメモを残すことでできるアプリ

LINEを使用して対話的に登録できる


・　作ろうと思った理由

読書が好きで気に入った文章や言葉があればメモしてExcelにまとめていた。

少しずつプログラムを組めるようになってきて、自分で管理するアプリを作ってみたいと思ったのがきっかけ


・　使用技術

HTML, CSS, Python(Django), LINE API, DialogFlow, 楽天API , EC2


・　どうなったか

今まではExcelにまとめていたため、パソコンに向かって書いていたのをスマホでも気軽に書けるようにしたいと思ったが好きな文章が長くなると書くのが面倒くさくなりパソコンの方が結局楽という結論に至った

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/mybookrecord.mp4"></video>

* * *

### ポートフォリオ 2019/12/08

・どんなアプリか

自己紹介アプリ


・　作ろうと思った理由

ポートフォリオという存在を知り、自分も欲しいなと思ったのがきっかけ


・　使用技術

HTML, CSS, JavaScript, GoogleApplicationScript(スプレッドシートをデータベースにしたため), AWS_S3(ホスティング)


・　どうなったか

とりあえずダサくて恥ずかしくなった

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/portfolio.mp4"></video>

* * *

### Troument 2020/07/10

・どんなアプリか

現在つまづいているエラーや解決したエラーを投稿できるアプリ

Trouble managementの造語

・　作ろうと思った理由

少しずつアプリっぽいものを作っているなかでエラーがよく出ていたので、エラー中やエラー解決などを投稿するSNSを作ろうと思ったため

・　使用技術

React、AWS_S3, Node.js(Express), MongoDB


・　振り返ってみて

勉強会に参加したことをきっかけにReactに興味を持ったため、Reactでの初めての開発

2月ぐらいから作成しててめっちゃ時間かかってる

今思うと、2つめに作ろうとしたSHARE PUTと似ている

SHARE PUTのときはアプリを作っていなかったためあんまりエラーってものに遭遇していなかったためテキストで勉強してる知識を共有

Troumentはアプリを作るようになってバグにいっぱい遭遇したため、エラーに特化したものを作ろうとした気がする

プラットフォーム系のアプリは個人のレベルでは

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/troument.mp4"></video>

* * *

### いいね検索アプリ 2020/08/22

・どんなアプリか

Twitterでいいねしたツイートを検索できるアプリ


・　作ろうと思った理由

Twitter APIの存在を知って使ってみたくなった ＋ 自分がいいねしてるツイートを見たくなった時にさかのぼって見るのが面倒だったので検索できたらいいなと思ったから

・　使用技術

React, AWS_APIGateWay, AWS_Lambda, Python, TwitterAPI

・　どうなったか

APIでさかのぼれる件数が決まっていて自分の理想にはならなかった

余談でTwitter APIで100日以上投稿がない人のフォローを外すプログラムを組んでいるときに、フォローを外す処理を条件外の箇所に書いて
全員のフォローを外してしまうミスを犯した


<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/iinesearch.mp4"></video>

* * *


### サブスク管理 2021/03/24

・どんなアプリか

登録しているサブスクの合計金額や更新日が近くなればメールを送信するアプリ


・　作ろうと思った理由

色々なサブスクリプションに登録しててどのぐらい月額かかっているか知りたかったのと、サブスクの解除を忘れて更新されることがあったため


・　使用技術

React, LINE Messaging API, vercel, AWS_Lambda, AWS_API_GateWay, postgreSQL 

・　どうなったか

サブスクを登録した時点でこのアプリにも自動で登録できる仕組みを実現させたかったけど、どうすればいいかわからず実用的に使えるとこまで持って行けず
サブスクの解除を後回しにする人は、サブスクの登録も後回しにするため意味がなくなる

すぐに登録したくなるようなデザイン設計ができれば良いが、そんなスキルは自分にはなかった

あと、課金日がいつかわからず正確な情報が取得できなかった。

5/31日に登録されたサブスクの次の課金日は 6/30 か 7/1 どっちになるのかがアプリによって違う気がしたため
アプリ内では月末(6/30)になるようにした

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/subscription.mp4"></video>

* * *

### メール翻訳 2021/06/21

・どんなアプリか

英語で届いたメールを翻訳して再度受信できるアプリ


・　作ろうと思った理由

英語のメールが届いた時に、何が書いているかわからず日本語で読みたくなったことがあるため

Gメールは翻訳できるっぽいけど、Yahooメールには翻訳機能が無さそう


・　使用技術

React, AWS_Lambda, Python, AWS_SES, AWS_Translate, AWS_S3

・　どうなったか

あんまり英語のメール届かない ＆ 定型的なメールなのでなんとなく意味がわかる

とは言え、使いどころはありそうだがSESの設定が消えていた

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/mailtranslate.mp4"></video>

* * *

### ラズパイ 2021/07/15

作ったものではないが、興味があるため記述

組み込み系に興味を持ち、初心者キットを買って一時期やっていたが難しくて辞めた。

〇 作ってみたいもの

①　生活用品や調味料の重さを図り、指定した重さを下回ればラインで通知を送る

買い忘れが減る

②　ベランダのシャッターを自動で閉じる

外出中に雨が降ってきてもスマホ1つでシャッターを閉じ、洗濯物が濡れるものを防ぐ

シャッターを取り付けるところから始める必要あり

* * *

### バーコードスキャナ 2021/11/23

・どんなアプリか

読んだ本のバーコードをスキャンして取得した情報をNotionに登録できるアプリ


・　作ろうと思った理由

読んだ本をNotionにまとめようとしたが入力するのも面倒なため、バーコードから取得できる情報一括で登録できたら楽だと思ったため


・　使用技術

React, AWS_Lambda(Python), NotionAPI, 楽天API


・　どうなったか

他の人も使えるように変更を加えてる途中で次に作りたいものができたため、途中で止まっている状態。
自分だけなら使える

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/barcode.mp4"></video>

* * *

### ガチャガチャアプリ 2021/12/24

・どんなアプリか

自分達の思い出の写真をガチャガチャの中身にできるアプリ


・　作ろうと思った理由

単純に楽しそうと思ったから
友達同士でグループを作成して、お互いがどんな写真をアップロードしたかわからない状態で引くと楽しそう


・　使用技術

React, TypeScript, AWS_S3, AWS_Lambda, Next.js, GraphQL, faunaDB, vercel

・　どうなったか

ちゃんと使えるレベルまでは程遠いが遊びレベルでは使える状態
動きがもっさりしている

勢いで作り始めたためもう少し設計をしっかりして作り直したい

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/gachagacha.mp4"></video>

* * *

### レシピ管理アプリ 2022/03/24

・どんなアプリか

複数のアプリでお気に入りにしたレシピを一つに統合できるアプリ
また、そのレシピに対してメモを残せる


・　作ろうと思った理由

複数のレシピアプリを使用したいるが、どのアプリでどのレシピを登録したか忘れたり、作った料理が美味しかったか。次作るとしたらもうちょっとこうしたいなどのメモを残せるようにしたかった


・　使用技術

React, TypeScript, AWS_Lambda(Python), faunaDB, GraphQL, LINEAPI


・　どうなったか

マナーに反するので使うのはやめておいた

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/recipemanagement.mp4"></video>

* * *

### GPSアプリ 2022/04/16

・どんなアプリか

謎解きしつつ、目的地を目指すアプリ

・　作ろうと思った理由

接触確認アプリ(COCOA)をスマホに入れた時、どういう仕組みか気になって
GPSの技術を使ってみたくなったから

最初はすれ違い機能みたいなことしたかったが、あまり仕組みがわからなかったためとりあえず出来そうな範囲でやってみることにした

・　使用技術

React

・　どうなったか

謎解きやストーリー性を重視する必要がありプログラミング以外の比重が大きい。
あと、GPSの精度を上手いこと取れないことがあった。

* * *

### 図書館アプリ 現在作成中

・どんなアプリか

書籍貸し出しアプリ(知り合い限定)

・　作ろうと思った理由

家に色々本はあるがずっと読んでいる訳ではないので誰か読みたい人がいれば貸し出せたらいいかなと思ったため。
知り合いなので口頭や他の手段でやり取りすればいいが作ってみたくなったため

・　使用技術

React, TypeScript, Lambda, PostgreSQL, 楽天API

・　どうなったか

作成途中


* * *