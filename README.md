## 目的
2021年12月末に4年9ヶ月勤めた会社を退職したため、転職先を探しています。

そこで、経歴と独学で勉強していることを簡易的ではあるが書いていくので話を聞いてあげてもいいよという会社があれば、
連絡して頂けるとありがたいです。

基本プロフィール

年齢：28歳

住所：大阪

性別：男

##### 希望条件

勤務地：大阪(リモートと出社を選べる)

休日：土日祝

希望年収： 430万以上

求めている職種：Webエンジニア

フロント・バックエンド・インフラの希望は特になし

どの言語・どのツールを使うより、何を作るか重視したい


<br /> 

## 経歴

2017年 4月入社

2017年 4月 - 2017年 5月：自社施設により研修

#### 2017年 6月 - 2018年 09月：客先にてメインフレーム 運用チームに配属(スケジューラー)

##### 主な仕事内容
*   ジョブ(JCL)やプログラム、データセットなど本番で利用するリソースを登録・変更・削除
*   ジョブ(JCL)のトラブル対応

アプリ担当の人から依頼があると作業が発生

上流工程や開発をする機会はほとんどなく、依頼に対して既存の自社開発のシステムを使って作業を行うのみ

オープン側の場合、[JP1](/https://e-words.jp/w/JP1.html)というシステムを利用していて

主な使用スキル：JCL, MSP(OS)

##### JCLのサンプル
JCL(Job Control Language)はメインフレームで使用されるスクリプト言語みたいなもの

メインフレームを触る上では必須の知識

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

<br />

#### 2018年 10月 ~ 2021年 12月：客先にてメインフレーム 基盤構築・運用保守チームに異動

メインフレームに関する運用面すべての担当

##### 主な仕事内容

*   ベンダー・お客様とやり取りしながら、機器のリプレイスや新たなシステムの導入の実施
*   OSのパラメータ変更
*   トラブル対応(365日24時間)
*   運用をしていく中で必要な場合にCOBOLでの開発

プログラムは運用で必要になったときに、作成する 又は 過去のプログラムがトラブルを起こした時の改修作業の時に
勉強したのみで常に開発していた訳ではない


使用スキル: COBOL, JCL, MSP(OS)

<br />

##### 主に担当した案件

*   災害対策システム構築
*   仮想テープリプレイス作業

その他、PTFアップ(OSのバージョンアップ時の確認作業), パラメータや監視設定の変更、トラブル対応など大きな案件ではなく
運用していくうえで必要な作業が都度発生


<br/>

## 保有資格

資格名(取得日)
*   TOEIC 675点(2016)
*   ITパスポート(2017-02-05)
*   LPIC-1(2017-05-29) → 5年経つため期限が切れている可能性
*   ITIL® Foundation Certificate in IT Service Management(2017/06/02)
*   基本情報技術者試験(2018-5-16)
*   RPA Developer Foundation Diploma(2018-12-08)
*   AWS Certified Solutions Architect – Associate(2019-07-17)
*   AWS Certified Solutions Architect - Professional(2021-07-11)

<br/>

## 独学

仕事中にExcelのVBAに触れる機会があり、プログラミングにハマる。

そこから、興味があったため勉強していた分野

2018年の年末あたりから独学で勉強を開始

今後は独学で勉強していたことを仕事にしていきたい

##### 主に触れているもの

HTML, CSS, JavaScript, TypeScript, React, Python, AWS


<br/>

### 使用した教材

*   Progate
*   PyQ
*   Udemy
*   書籍

<br/><br/>

### 過去に作成したもの(計：13個)

転職活動を機に過去に勉強兼遊びで作成したアプリの振り返りを行う

ポートフォリオになるかわからないが、現状のスキル状況を知ったもらうための1つの手段になればいいかなと思う

作成した当時に撮った動画を載せておく

<br/>

見出しは、アプリを作るときに決めた名前と大体の機能が完成した時の日付
#### 晩御飯決めアプリ 2019/03/31

##### どんなアプリか

料理名を入力しておいて、ボタンを押すと入力してる料理からランダムで表示


##### 作ろうと思った理由

一人暮らしをしていて、晩御飯に何を食べようかいつも迷っていたためランダムで決めてくれるものがあればいいなと思い作成


##### 使用した技術

HTML, CSS, Python(Flask)


##### 振り返ってみて

初めて作るアプリっぽいもので訳わからずとりあえず手を動かしていたはず

機能としては一応できたが、レスポンシブ対応ができなくて挫折

Pythonはできたら色々と幅が広がりそうだと言う理由で採用

Web系では、PHPとかRubyがよく使われてることを知らなかった

動画がなかったので写真のみ
<br/><br/>

<img src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/foodchoice.png" />

<br/><br/>

#### SHARE PUT　2019/8/3

##### どんなアプリか

勉強したことをアウトプットするために投稿、他の人の投稿を見てインプットするアプリ

共有のSHAREとINPUT・OUTPUTのPUTを取って、SHARE PUT


##### 作ろうと思った理由

勉強したことをまとめることは良いと思いつつも記事にするのはなかなか大変なのでSNS感覚で投稿できるものが
あればいいなと思い作成


##### 使用した技術

HTML, CSS, Python(Django), heroku


##### 振り返ってみて

使い物にはならないが、ある程度の形になったことは嬉しかった。

レスポンシブ対応もある程度できて1つ目と比べて成長を感じられた

デザインをどうしようか、どんな機能があればいいかなとかをちゃんと考えたアプリ

やっぱり自分で書いたコードが動いた瞬間は楽しいね

<br/>

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/shareput.mp4"></video>

<br/>

#### MyBookRecord 2019/09/21

##### どんなアプリか

読んだ本の登録とメモを残すことでできるアプリ

LINEを使用して対話的に登録できる


##### 作ろうと思った理由

読書が好きで気に入った文章や言葉があればメモしてExcelにまとめていた。

少しずつプログラムを組めるようになってきて、自分で管理するアプリを作ってみたいと思ったのがきっかけ


##### 使用した技術

HTML, CSS, Python(Django), LINE API, DialogFlow, 楽天API , EC2, Route53


##### 振り返ってみて

作ってるときは割と便利なんじゃないかと思ってワクワクしていた。

けど、好きな文章が長くなるとスマホで打つのは面倒だったり、LINEで対話的に登録するメリットもないし使う側の目線が完全に抜けていたなと反省

多分当時はLINE APIの存在を知って使いたくなったからLINEでやり取りしてみようってなったはず

なぜかこのアプリだけ構成図を書いていたので載せておく
<br/><br/>

<img src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/mybookrecord_chart.jpg" />

<br/><br/>

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/mybookrecord.mp4"></video>

<br/><br/>

#### ポートフォリオ 2019/12/08

##### どんなアプリか

自己紹介アプリ


##### 作ろうと思った理由

ポートフォリオという存在を知り、自分も欲しいなと思ったのがきっかけ


##### 使用した技術

HTML, CSS, JavaScript, GoogleApplicationScript(スプレッドシートをデータベースに使用), AWS_S3(ホスティング)


##### 振り返ってみて

とりあえずダサくて恥ずかしくなった

<br/><br/>

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/portfolio.mp4"></video>

<br/><br/>

#### Troument 2020/07/10

##### どんなアプリか

現在つまづいているエラーや解決したエラーを投稿できるアプリ

アプリ名は、Trouble managementを略した言葉

##### 作ろうと思った理由

アプリっぽいものを作っていると絶対にエラーが出るので、エラー中の報告やエラー解決などの投稿ができるSNSを作ろうと思ったため

##### 使用した技術

React、AWS_S3, Node.js(Express), MongoDB


##### 振り返ってみて

勉強会に参加したことをきっかけにReactに興味を持ったため、Reactでの初めての開発

2月ぐらいから作成しててめっちゃ時間かかっててびっくり

Adobe製品を使ってデザインをちゃんと考えてみようと思ったりしたこともあって時間かかったのかも

自分のプログラミングスキルが全然足りていないという理由はもちろんあるが、個人レベルでユーザー数を必要とするアプリを作るのは無理があるなと思った。

ユーザーを集める努力も必要になるし、デザイン考えて、コーディングして、インフラも意識するって難易度高すぎる。。。

他の人が使わなくても自分だけが使えるアプリを目指すのが現状の目標


<br/><br/>

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/troument.mp4"></video>

<br/><br/>

#### いいね検索アプリ 2020/08/22

##### どんなアプリか

Twitterでいいねしたツイートを検索できるアプリ


##### 作ろうと思った理由

Twitter APIの存在を知って使ってみたくなった ＋ 自分がいいねしてるツイートを見たくなった時にさかのぼって見るのが面倒だったので検索できたらいいなと思ったから

##### 使用した技術

React, AWS_APIGateWay, AWS_Lambda, Python, TwitterAPI

##### 振り返ってみて

APIでさかのぼれる件数(確か 200件)が決まっていて自分の理想にはならなかった

LINE APIの時と同じでAPIを使ってみたかっただけな気する

Twitter APIで100日以上投稿がない人のフォローを外すプログラムを組んでいるときに、フォローを外す処理を条件外に書いて
全員のフォローを外してしまうミスを犯してしまった。

もし仕事やったらめっちゃ怒られてそう

<br/>

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/TwitterAPI.mp4"></video>

<br/><br/>

#### サブスク管理 2021/01/22

##### どんなアプリか

登録しているサブスクの合計金額や更新日が近くなればLINEに通知するアプリ

##### 作ろうと思った理由

色々なサブスクリプションに登録しててどのぐらい月額かかっているか把握ことと、サブスクの解除を忘れて更新されることがあったため


##### 使用した技術

React, TypeScript, LINE Messaging API, vercel, AWS_Lambda(Python), AWS_EventBridge
, AWS_API_GateWay, postgreSQL 

##### 振り返ってみて

サブスクを登録した時点でこのアプリにも自動で登録できる仕組みを実現させたかったけど、どうすればいいかわからず実用的に使えるとこまで持って行けず

サブスクの解除を忘れるパターンの大半は、気づいても後で解除しておこうと問題を後回しにしてしまうこと(自分の場合)

解除を後回しにする人は、サブスクの登録も後回しにして結局このアプリ自体にも登録されていなくて気づかないパターンが発生する可能性大

すぐに登録したくなるようなデザイン設計ができれば良いが、そんなスキルは自分にはなかった

あと、課金日がいつかわからず正確な情報が取得できなかった。

例えば、5/31日に登録されたサブスクの次の課金日は 6/30 か 7/1 どっちになるのかがアプリによって違う気がしたため

アプリ内では月末(6/30)になるようにした

<br/><br/>

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/subscription.mp4"></video>

<br/><br/>

#### メール翻訳 2021/06/21

##### どんなアプリか

英語で届いたメールを指定されたアドレスに転送することで翻訳して再度受信できるアプリ


##### 作ろうと思った理由

英語のメールが届いた時に、何が書いているかわからず日本語で読みたくなったことがあるため

Gメールは翻訳できるっぽいけど、Yahooメールには翻訳機能が無さそう


##### 使用した技術

React, AWS_Lambda, Python, AWS_SES, AWS_Translate, AWS_S3, AWS_Route53

##### 振り返ってみて

AWSのサービスがお金かかるため、設定を破棄して今は使えない

英語に触れるせっかくの機会なんでできるだけすぐに翻訳を頼らず読解する力を身に着けるためにも不要

けど役立つ時はありそう

<br/><br/>

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/mailtranslate.mp4"></video>

<br/><br/>

#### ラズパイ 2021/07/15

作ったものではないが、興味があるため記述

組み込み系に興味を持ち、初心者キットを買って一時期やっていたが難しくて辞めた。

〇 作ってみたいもの

①　生活用品や調味料の重さを図り、指定した重さを下回ればラインで通知を送る

買い忘れが減る

②　ベランダのシャッターを自動で閉じる

外出中に雨が降ってきてもスマホ1つでシャッターを閉じ、洗濯物が濡れるものを防ぐ

シャッターを取り付けるところから始める必要あり

<br/><br/>

#### バーコードスキャナ 2021/11/23

##### どんなアプリか

読んだ本のバーコードをスキャンして取得した情報をNotionに登録できるアプリ


##### 作ろうと思った理由

読んだ本をNotionにまとめようとしたが入力するのも面倒なため、バーコードから取得できる情報一括で登録できたら楽だと思ったため


##### 使用した技術

React, AWS_APIGateWay, AWS_Lambda(Python), NotionAPI, 楽天API


##### 振り返ってみて

他の人も使えるように変更を加えてる途中で次に作りたいものができたため、途中で止まっている状態。

時間ができたら続きをしたい

自分だけなら使える

バーコードをスキャンするぐらいならすぐ出来るため手軽

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/barcode.mp4"></video>

<br/><br/>

#### ガチャガチャアプリ 2021/12/24

##### どんなアプリか

自分達の思い出の写真をガチャガチャの中身にできるアプリ

タイトルをつけたガチャガチャを作成し、そのガチャに対して写真をアップロードすることができる

ガチャガチャ作成時にパスワードをつけておき、タイトルとパスワードを知ることでガチャガチャを登録して引くことができる


##### 作ろうと思った理由

単純に楽しそうと思ったから

友達同士でグループを作成して、お互いがどんな写真をアップロードしたかわからない状態で引くと楽しそう


##### 使用した技術

React, TypeScript, AWS_S3, AWS_Lambda, Next.js, GraphQL, faunaDB, vercel, Adobe_Animate

##### 振り返ってみて

ちゃんと使えるレベルまでは程遠いが遊びレベルでは使える状態

Next.jsやGraphQLを初めて使ったアプリ

動きがもっさりしている

勢いで作り始めたためもう少し設計をしっかりして作り直したい

アイデアは割と好き

ガチャの演出考えるの楽しかったけどAnimate使うの難しかった

<br/><br/>

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/gachagacha.mp4"></video>

<br/><br/>

#### レシピ管理アプリ 2022/03/24

##### どんなアプリか

複数のアプリでお気に入りにしたレシピを一つに統合できるアプリ

また、そのレシピに対してメモを残せたり、買う必要のある材料をまとめて確認できる

現状、クックパッド・デリッシュキッチン・クラシルのレシピが乗っているURLを保存できる

##### 作ろうと思った理由

複数のレシピアプリを使用しているが、どのアプリでどのレシピを登録したか忘れたり、作った料理が美味しかったか。次作るとしたらもうちょっとこうしたいなどのメモを残せるようにしたかった

##### 使用した技術

React, TypeScript, AWS_Lambda(Python), faunaDB, GraphQL, LINEAPI


##### 振り返ってみて

各アプリでは課金をすることでレシピのお気に入り数を無制限にすることができる。

しかし作成したアプリを使うと、課金せずに無制限でレシピのURLを保存できるため何かしらの規則にに反してそうで使うのはやめておいた。

<br/><br/>

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/recipemanagement.mp4"></video>

<br/><br/>

#### GPSアプリ 2022/04/16

##### どんなアプリか

謎解きしつつ、目的地を目指すアプリ

##### 作ろうと思った理由

最初はすれ違い機能がついてるアプリを開発してみたかったが、あまり仕組みがわからなかったためとりあえず出来そうな範囲でやってみることにした

##### 使用した技術

React

##### 振り返ってみて

謎解きやストーリー性を重視する必要がありプログラミング以外の比重が大きい。

簡単すぎず難しすぎない かつ 答えが導けたときに納得できる 謎解きを作成するの難易度高い

あと、GPSの精度が曖昧で正確に取得できないときがあった。取得するまで時間かかったりするときも

<video controls width="400" height="500" src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/GPS.mp4"></video>



<br/><br/>
大阪駅付近で使用している前提
<br/><br/>
謎解き1
<br/><br/>
<img src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/mystery1.png" />
<br/><br/>
謎解き2
<br/><br/>
<img src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/mystery2.png" />
<br/><br/>
謎解き3
<br/><br/>
<img src="https://nozomi-portfolio-video.s3.ap-northeast-1.amazonaws.com/mystery3.png" />
<br/><br/>


<br/><br/>

#### 図書館アプリ 現在作成中

##### どんなアプリか

書籍貸し出しアプリ(知り合い限定)

##### 作ろうと思った理由

家に色々本はあるがずっと読んでいる訳ではないので誰か読みたい人がいれば貸し出せたらいいかなと思ったため。
知り合いなので口頭や他の手段でやり取りすればいいが作ってみたくなったため

##### 使用した技術

React, TypeScript, Lambda, PostgreSQL, 楽天API

##### 振り返ってみて

作成途中

出来次第、更新予定

<br/><br/>


### 作成したものを振り返ってみて

レベルは低いとはいえ、案外アプリを作っていたなという印象

初めの頃と比べると確実に出来るようになってきているけど、まだまだ未熟

こんなアプリがあればいいなと考えて、作ったりしている時間は楽しいので今後は仕事でこんなことができたらいいなと思っています。


## 終わりに

少し長くなってしまいましたが、最後まで目を通して頂きありがとうございます。

前職でしていたメインフレーム運用関連の仕事とは離れて今後はWeb系の仕事をしたいと考えています。

すこしでも興味をもっていただけたら連絡してくださるとありがたいです。
