---
layout: 'layouts/doc-post.njk'
title: プライバシーサンドボックスの用語集
subhead: プライバシーサンドボックスの記事とドキュメントは、プライバシー、広告、および Web 開発の概念に関する知識があることを前提としています。この用語集では、重要な用語について説明しています。
description: 重要な概念の簡単な説明。
date: 2021-05-18
updated: 2021-05-18
authors:
  - Web開発者向け
---

{% Aside %}

何か足りないと思われる場合は、[お知らせください！](https://github.com/GoogleChrome/developer.chrome.com/issues/new?assignees=&labels=feature+request&template=feature_request.md&title=)

{% endAside %}

## 広告プラットフォーム (アドテック) {:#adtech }

広告配信サービスを提供する会社。

## 広告主 {: #advertiser }

お金を使って製品を宣伝する会社。

## アトリビューション {: #attribution }

結果に寄与するユーザーアクションの識別。例：広告のクリックまたは表示と[コンバージョン](#conversion)の相関関係。

## Blink {: #blink }

Chrome で使用される[レンダリングエンジン。](https://en.wikipedia.org/wiki/Browser_engine) [Chromium](#chromium) プロジェクトの一部として開発。

## Chromium {: #chromium }

オープンソースのウェブブラウザープロジェクト。 Chrome や Microsoft Edge、Opera などのブラウザは Chromium をベースにしています。

## クリックスルー率 (CTR) {:#ctr }

広告を見たユーザーがそれをクリックする割合。([インプレッション](#impression)も参照してください。)

## クリックスルーコンバージョン (CTC) {:#ctc }

「クリックされた」広告に起因するコンバージョン。

## コンバージョン

ユーザーによるアクションに続いて起こる何らかの期待される目標の完了。広告主のサイトにリンクする広告をクリックした後に製品を購入したり、ニュースレターにサインアップしたりする場合が含まれます。

## クッキー

ウェブサイトは、ユーザーのコンピューターに Cookie と呼ばれる小さなテキストデータを保存することをウェブブラウザーに要求できます。Cookie は、ユーザーがウェブを移動するにあたり、ユーザーに関するデータ (またはウェブサイトのバックエンドサーバーに保存されているデータへの参照) を保存するためにウェブサイトで使用することができます。たとえば、オンラインストアは、ユーザーがログインしていなくてもショッピングカートの詳細を保持できます。また、サイトは、そこでのユーザーのブラウジングアクティビティを記録できます。[ファーストパーティ Cookie](#first-party-cookie) と [サードパーティ Cookie](#third-party-cookie) を参照してください。

## 差分プライバシー {: #differential-privacy }

データセットに関する情報を共有して、ユーザーの個人情報やそのユーザーがデータセットに属しているかどうかを明らかにせずに、そのユーザーの行動パターンを明らかにする手法。

## ドメイン

[トップレベルドメイン](#tld) と [eTLD](#etld) を参照してください。

## eTLD、eTLD + 1 {: #etld }

**効果的なトップレベルドメイン**は、[パブリックサフィックスリスト](https://publicsuffix.org/list/)によって以下のように定義されます。

```text
co.uk
github.io
glitch.me
```

効果的な TLD は、foo.appspot.comを bar.appspot.com とは別のサイトにすることを可能にするものです。この場合の有効なトップレベルドメイン (**eTLD**) は appspot.com であり、**サイト**の完全な名前 (foo.appspot.com、bar.appspot.com) は **eTLD+1** として知られています。

[トップレベルドメイン](#tld)も参照してください。

## エントロピー

データの項目が個人のアイデンティティを明らかにする度合の尺度。

データエントロピーはビット単位で測定されます。データによってアイデンティティが明らかになればなるほど、そのエントロピー値は高くなります。

データを組み合わせて個人を特定することはできますが、新しいデータがエントロピーを高めるかどうかを判断するのは難しい場合があります。たとえば、ある人物がカンガルー島出身であることをすでに知っている場合は、その人物がオーストラリア出身であることを知ってもエントロピーが低減することはありません。

## フェデレーション ID (別名フェデレーションログイン)

サイトに独自の ID サービスを実装しなくても、ユーザーがウェブサイトにサインインできるようにするサードパーティのプラットフォーム。

## フィンガープリンティング {: #fingerprinting }

個々のユーザーの行動を識別および追跡するための手法。フィンガープリンティングは、ユーザーが認識しておらず、制御できないメカニズムを使用します。[Panopticlick](https://panopticlick.eff.org) や [amiunique.org](https://amiunique.org/) などのサイトでは、フィンガープリントデータを組み合わせて個人を識別する方法を紹介しています。

## フィンガープリンティングサーフェス {: #fingerprinting-surface }

特定のユーザーまたはデバイスを識別するために (おそらく他のサーフェスと組み合わせて) 使用できるもの。たとえば、Javascript の `navigator.userAgent()` メソッドや `User-Agent` HTTPリクエストヘッダーは、フィンガープリントサーフェス (ユーザーエージェント文字列) へのアクセスを提供します。

## ファーストパーティ {: #first-party }

ユーザーが訪問しているサイトのリソース。たとえば、現在あなたが読んでいるページは、developer.chrome.com というサイトにあり、そこにはそのサイトからリクエストされたリソースが含まれています。そうしたファーストパーティリソースに対するリクエストは「ファーストパーティリクエスト」と呼ばれます。またこのサイトにアクセスしている間に保存される developer.chrome.com の [Cookie](#cookie) は[ファーストパーティ Cookie](#first-party-cookie) と呼ばれます。[サードパーティ](#third-party)についてもお読みください。

## ファーストパーティCookie {：#first-party-cookie }

ユーザーがサイトにアクセスしている間にウェブサイトによって保存される [Cookie](#cookie)。例: オンラインストアは、ログインしていないユーザーのショッピングカートの詳細を保管するために、Cookie を保存することをブラウザに要求する場合があります。[サードパーティ Cookie](#third-party-cookie) についてもお読みください。

## インプレッション {: #impression }

- 広告の表示。([クリックスルー率](#ctr)) も参照してください。）
- 広告スロット: 広告を表示できるウェブページ上の空の長方形。広告スロットは[インベントリ](#inventory)を構成します。

## インベントリ {: #inventory }

サイト上で利用可能な広告スロット: 広告を表示できる空の長方形。

## k-匿名性

データセット内の匿名性の尺度。 *k* 匿名性がある場合は、データセット中の他の *k-1* 人と区別がつきません。つまり、(自分を含めて) *k* 人が同じ情報を持っているということになります。

## ノンス

暗号通信で 1 回だけ使用される任意の番号。

## オリジン

リクエストの発信元で、スキームとサーバー名を含むが、パス情報は含まれない。例: `https://developer.chrome.com`

## オリジントライアル {: #origin-trial }

オリジントライアルは、新しい機能または実験的な機能へのアクセスを提供し、機能がすべての人に利用可能になる前に、ユーザーが限られた時間だけ試すことができる機能を構築できるようにします。 Chrome が機能のオリジントライアルを提供するとき、[オリジン](#origin)は、トライアルに登録すれば、そのオリジンを試しているすべてのユーザーに対して機能を有効化することができます。ユーザーは、フラグやスイッチを Chrome の代替ビルドに切り替える必要がありません (アップグレードが必要な場合はあります)。オリジントライアルを使用すると、開発者は新しい機能を使用してデモやプロトタイプを作成できます。またこのトライアルは、Chrome エンジニアが新機能の用途や他のウェブテクノロジーと対話する方法を理解するのにも役立ちます。詳細は、[Chrome のオリジントライアルを始めましょう](https://web.dev/origin-trials/)を参照してください。

## パッシブサーフェス {: #passive-surface }

ユーザーエージェント文字列や IP アドレス、accept-language ヘッダーなどのフィンガープリンティングサーフェスは、サイトが要求するかどうかを問わず、すべてのウェブサイトで利用できます。つまり、パッシブサーフェスは、サイトのプライバシーバジェットを簡単に消費する可能性があります。

プライバシーサンドボックスイニシアチブは、パッシブサーフェスを特定の情報を取得するアクティブな方法に置き換えることを提案しています。たとえば、すべてのサーバーに対するすべての応答に accept-language ヘッダーを使用するのではなく、クライアントヒントを 1 回使用してユーザーの言語を取得するなどの方法です。

## パブリッシャー

プライバシーサンドボックスのコンテキストで、広告を表示するサイト。

## リーチ

広告を見た人、または広告を表示するウェブページにアクセスした人の総数。

## リマーケティング

以前自分のサイトにアクセスしたユーザーを別のサイトでリーチする。たとえば、オンラインストアが自社のサイトでおもちゃを閲覧したユーザーに対しておもちゃのセール広告を表示する場合がこれに該当します。

## サイト

[トップレベルドメイン](#tld)および [eTLD](#etld) を参照してください。

## サーフェス

[フィンガープリンティングサーフェス](#fingerprinting-surface)および[パッシブサーフェス](#passive-surface)を参照してください。

## サードパーティ {: #third-party }

アクセスしているウェブサイトとは異なるドメインから提供されるリソース。たとえば、foo.com というウェブサイトは、google-analytics.com の分析コード (JavaScript 使用)、use.typekit.net のフォント (リンク要素を使用)、vimeo.com の動画 (iframe 内で使用)を使用する場合があります。[ファーストパーティ](#first-party)も参照してください。

## サードパーティ Cookie {: #third-party-cookie }

サードパーティのサービスによって保存された [Cookie](#cookie)。たとえば、動画ウェブサイトには、ユーザーが動画サイトに移動しなくても、動画をウィッシュリストに追加できるようにするために、埋め込みプレーヤーに**後で見る**ボタンが含まれている場合があります。[ファーストパーティ Cookie](#first-party-cookie) も参照してください。

## トップレベルドメイン (TLD) {: #tld }

.com や .org などのトップレベルドメインは、[ルートゾーンデータベース](https://www.iana.org/domains/root/db)に記載されています。

一部の「サイト」は実際には単なるサブドメインであることに注意してください。たとえば、translate.google.com や maps.google.com は、google.com ([eTLD + 1](#etld)) のサブドメインです。

## .well-known サブディレクトリー

標準化された URL からウェブサイトへのリダイレクトを追加すると便利な場合があります。 たとえば、ウェブサイトに `/.well-known/change-password` からサイト内のパスワード変更ページへのリダイレクトがセットアップされている場合は、パスワードマネージャーを使用するとユーザーは簡単にパスワードを更新できます。また、リクエストを送信する*前に*、ポリシーやホストに関する他の情報にアクセスすることが役に立つこともあります。たとえば、robots.txt は、ウェブクローラーにアクセスするページと無視するページを指示します。IETF [RFC8615](https://tools.ietf.org/html/rfc8615) には、サイト全体のメタデータを /.well-known/ サブディレクトリーの標準的な場所でアクセスできるようにするために標準化された方法について記載されています。その一欄は、[iana.org/assignments/well-known-uris/well-known-uris.xhtml](https://www.iana.org/assignments/well-known-uris/well-known-uris.xhtml) で確認できます。
