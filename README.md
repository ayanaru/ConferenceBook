# カンファレンス参加の楽しみ方合同誌(仮)

## 概要説明
カンファレンス参加の楽しみ方合同誌（仮）

## この本の目的
### 背景
RSGT2021の参加者の中に、本を書いてみたいという人がいたというのが一つです。また、最近オンライン開催のカンファレンスも増えてきましたので、気軽に参加できるようになった一方、ちょっとしたことをケアしておくとより楽しめたりします。そういった知識を共有することで、勉強会ライフはより快適になるでしょう。

### 対象読者
若手エンジニアむけ？
特に、勉強会/カンファレンス参加を迷っている人にこんなに楽しいぞ！こうすればもっと楽しいぞ、をお伝えしたいと思います。

文章に起こすことで整理される側面もあるでしょう。
他の人と共有しやすくなることもあるでしょう。
それを見て、行動を起こす人がいるかもしれません。

1ページからでも構いません。執筆者の仲間入りです。
5ページ書けますか？まとまった量で読み応えありますね。
10ページ書きますか？どんとこい。
そして、あなたの本を技術書典に参加する1万人（あるいはそれ以上）に届けませんか？

## 執筆・配布スケジュール
募集開始・環境構築　2021年1月10日(済)
初稿：1月末
レビュー＆追記：2月末日
最終入稿日まで追記・参加は随時OKです。
発行:　2021年4月末頃　技術書典11目標（ただしイベント予定は未公開)
詳細は、Discordにて。(アジャイルのやさしいサーバー内。)

## 著者紹介兼あとがき
Contributers.re内に、テンプレートに従って記入ください。

## 執筆にあたってのお願い
CIでコンパイルが通ることを確認してください。エラーのまま放置はなるべくやめてください。

Confrictが発生した場合は、解決お願いします。

push -f等はやめましょう。（歴史を書き換えてはいけません。

相談事：
Issue立ててください。

雑談、ざっくばらんな相談については、Slackがあります。
参加方法は、親方まで。https://twitter.com/oyakata2438

## 執筆方法

本書は、easybooks を使って発行されています。easybooks では Markdown か Re:VIEW で記述します。

* [Markdownでの書き方](https://raw.githubusercontent.com/erukiti/easybooks/master/example/about-easybooks.md)
* [Re:VIEWチートシート](https://gist.github.com/erukiti/c4e3189dda179a0f0b73299fb5787838) を作ってみたので、参考にしてみてください。

また、プレーンテキストやWordとかでの提出も可能です。編集部にてコンバートします。

## CI
https://app.wercker.com/oyakata2438/onestop-online/runs
でPDFが書きだされます。
一番上のBuildをクリックすると展開されるので、
Output Artifactをクリックして、Download artifactをクリックすると、
tarで固めたpdfがダウンロードできます。

## インストール

細かい準備(TeX入れたり)は[『技術書をかこう！』](https://github.com/TechBooster/C89-FirstStepReVIEW-v2)に準じます。

### Dockerを使う方法

Dockerを使うのが一番手軽です。とても面倒なTeXのインストールなどを全てDockerでやってくれるため、何も悩むことはありません。

```sh
$ docker run -t --rm -v $(pwd):/book vvakame/review:3.2 /bin/bash -ci "cd /book && yarn && yarn build"
```

このコマンドの実行が成功すれば、コンパイルされたPDFが、`.review/Onestop-Online.pdf` として出力されています。

Mac なら `open .review/Onestop-Online.pdf` で PDF を開くことができます。

### WindowsでReviewを使う方法

https://qiita.com/implicit_none/items/398c6e0bbedc8b160621
暗黙の型宣言さんが詳しく書いてくれてます。あるいは、技術同人誌を書こう‐アウトプットのススメ‐をご覧ください。

Windows10(Home/Pro問わず)であれば、WSL＋docker越しにRe:VIWEを扱う方法もあります。https://qiita.com/hoshimado/items/7592cee28c1bde545b78

※2019/11/04時点で、次の環境にて後述のdockerコマンドからコンパイル出来ることを確認済み。

<!-- (3.1指定は、2.x環境と共存のため) -->

* Microsoft Windows 10 Home Version 1903 
* Ubuntu 16.01
* Docker version 17.03.2-ce, build f5ec1e2
* Docker image : vvakame/review (tag:3.1)
* Docker image : vvakame/review (tag:3.2)

### Dockerを使わずにビルドする

* TeX をインストールする
* Ruby をインストールする
  * review gem をインストールする
* Node.js をインストールする

```sh
yarn && yarn build
```

### 権利

ベースには、[TechBooster/ReVIEW\-Template: TechBoosterで利用しているRe:VIEWのテンプレート（B5/A5/電子書籍）](https://github.com/TechBooster/ReVIEW-Template) を使っています。

  * 設定ファイル、テンプレートなど制作環境（techbooster-doujin.styなど）はMITライセンスです
    * 再配布などMITライセンスで定める範囲で権利者表記をおねがいします
