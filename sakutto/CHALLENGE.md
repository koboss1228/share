# 課題

## 前提条件

- このリポジトリは好きにつかっていただいて構いません
- 下記の課題は 1,2 をつかいますので、その他のものはすべて達成する必要はありません
- 課題内容や仕様などのなかでわからないところがあれば、お気軽にご質問ください

## 1. 掲示板アプリをつくってください

下記の制約と仕様を満たした掲示板アプリを作成してください。

下記の制約と仕様を満たしていれば、その他のことは自由に設計や細かな仕様は決めてもらって構いません。

- 制約
    - プログラミング言語 Scala をつかって作成してください
        - バージョンの指定はありませんが、安定しているバージョン 2.13 系を推奨します
    - ライブラリやフレームワークは好きなものをつかっていただいて構いません
    - データ永続化のためのミドルウェアが必要であれば好きなものをつかっていただいて構いません
    - ローカルマシン上で動作するまでで構いません(どこかにデプロイ等は不要)
- 仕様
    - アプリケーションに好きな名前をつけてください
    - HTTP をつかった WebAPI でやりとりできるアプリケーションにしてください
        - 形式は JSON など、自由で構いません
        - WebAPI のインターフェースは自由に設計してもらって構いません
    - 機能
        - スレッド作成の API エンドポイントで、スレッドを作成できる
            - スレッドにはスレッドタイトルを入力できる
        - スレッド一覧取得の API エンドポイントで、スレッドの一覧を取得できる
            - スレッド情報は「スレッド識別子(ID)」「スレッドタイトル」「いつ作られたかの日時(日本時間)」が含まれる
        - 書き込み投稿の API エンドポイントで、スレッドに書き込みできる
            - 書き込みは「書き込み先スレッド識別子(ID)」「本文」「任意の投稿者名」を入力できる
            - 「任意の投稿者名」の入力がなければ "名無しさん" として扱う
        - 書き込み取得の API エンドポイントで、指定したスレッドに書き込まれた書き込み一覧を取得できる
            - スレッド識別子(ID)を指定してリクエストできる
            - そのスレッドに書き込まれた書き込みの一覧が、投稿された順に取得できる
            - 書き込みは「書き込み識別子」「本文」「投稿者名」「書き込まれた日時(日本時間)」が含まれる
    - アプリケーションを他の人が試す際の手順ドキュメントを作ってください
        - テキストでもスライドでも、形式はなんでも OK です
        - Git にコミットしてください

以上です。
その他の機能や仕様は、もともとの制約や仕様を満たしている限り、好きに追加してもらって構いません。


## 2. 発表準備してください

掲示板アプリの開発に関する発表準備をお願いします。

内容としては、下記を想定しています。内容については相談の上変更してもらっても構いません。

- 作成したアプリの紹介、アピールポイント
- デモンストレーション
- 採用したライブラリやフレームワークの紹介と選定理由
- 工夫した点
- 苦労した点
- その他なんでも(なくても OK)

発表時間は 20 分以内程度を予定しています。


## extra. 掲示板アプリをブラウザ画面で操作できるようにしてください

※こちらは追加課題になります。時間があって試してみたいときに取り組んでみてください。\
※extra. はどちらをやってもよいですし、どっちもやってもよいですし、やらなくてもよいです。

掲示板アプリの画面を作成してください。
機能は 1. のときのままで構いません。

- 1 で作成した WebAPI を利用して SPA (SinglePageApplication) としてつくる
- 1 で作成したロジックを再利用して 動的 HTML 生成アプリケーションとしてつくる

など、形式は問いません。細かな動きの仕様も問いません。\
利用する技術も問いません。画面部分(フロントエンド)は TypeScript + ライブラリ などの構成でも構いません。


## extra. 掲示板アプリに機能追加してください

※こちらは追加課題になります。時間があって試してみたいときに取り組んでみてください。\
※extra. はどちらをやってもよいですし、どっちもやってもよいですし、やらなくてもよいです。

掲示板アプリに、以下の新機能を追加してください。

- アカウント登録
    - 「名前」「パスワード」を入力し、アカウントを登録できる
    - 利用できる文字種や文字長制限等は自由に決めてください
- ログイン
    - 「名前」「パスワード」を入力し、一致したらログインできる
- ログインしたアカウントでスレッドを作った場合、スレッド情報取得時のそのスレッドのデータに「認証マーク付きの作成者名」が含まれる
    - 画面がある場合、表示される
    - 認証マークは自由に決めてもらって構いません
- ログインしたアカウントで書き込みをおこなった場合、書き込み一覧取得時のその書き込みデータに「認証マーク付きの作成者名」が含まれる
    - 画面がある場合、表示される
    - 認証マークは自由に決めてもらって構いません
