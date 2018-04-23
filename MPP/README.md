
>プロジェクトの方針と大体の機能を纏めたり、あとは各々のロジックを図で表したりしてグループで理解と効率化を図る

# MCBE Portal Project

## メンバー

| 発案・バックエンド担当 | かずえもん (@mcpe_kazuemon) |
| --- | --- |
| アイデア担当 | うらむんオイル (@UramnOIL) |
| 公式サイト担当 | そうたん (@soutan_fon) |
| アイコンお願い (**予定**) | うろのるさん (@URNR__) |
| 宣伝動画お願い (**予定**) | るいるいさん (@chell_uoxou) |

## 現時点で作る必要があるもの

- アプリの公式サイト
- Webアプリ
- スマホ用アプリ

## 環境など

- 主にGoogleのFirebaseを使用
	- 基本は**無料**で、スケールに応じて**プラス課金**可能

- バックエンド
	- アカウント管理
		- Firebase Auth
			(https://firebase.google.com/products/auth/?hl=ja)
	- 内部API (Nodejs)
		- Cloud Functions for Firebase
			(https://firebase.google.com/docs/functions/?hl=ja) 
	- データ管理
		- Firestore
			(https://firebase.google.com/products/firestore/?hl=ja)

- Webアプリ
	- Firebase Hosting
		(https://firebase.google.com/products/hosting/?hl=ja)

- スマホ用アプリ
	- Flutter (クロスプラットフォーム開発可能)
		(https://flutter.io)

##  現在の課題

- iOS向けのアプリをどのように公開するか
	- 「プロ生ちゃんアプリ開発支援プログラム」(http://pronama.azurewebsites.net/2016/10/12/pronama-chan-developer-support-program/) を利用する。

## 主な機能

基本的にはLobiのようなスレッドタイプの掲示板で、それぞれの用途に合わせて機能を追加する。
以下3つを「メインカテゴリ(ディメンション)」とし、それぞれが「サブカテゴリ(チャンク)」とスレッドにつけられる「タグ」を持つ。

### Inventory (インベントリ)
制作物の配布を行う場。

#### サブカテゴリ 
- ワールド
- テクスチャ
- スキン
- Mod
- アドオン (需要あり?)
- PMMPプラグイン
- Nukkitプラグイン
- MiNETプラグイン
- その他

---

### Forum (フォーラム)
質問、ユーザーとの交流を行う場。

#### サブカテゴリ
- 全般
- テクスチャ
- スキン
- Mod
- アドオン
- コマンド
- PMMPプラグイン
- Nukkitプラグイン
- MiNETプラグイン
- その他

---

### Invite (インバイト)
宣伝、募集を行う場。

#### サブカテゴリ
- Xbox
- サーバー
	(サーバーステータス表示サービスの提供)
- その他

## その他機能

### Discord連携

新規スレッドがあった場合、スレッドの内容をDiscordに通知する。

### 経験値システム(仮)

ユーザーがどれだけ活動を行っているかどうかを、マイクラの「経験値」と「レベル」で表示する。

> 製作者の意欲向上と、質問に対しての回答者がどれほど信頼出来るかを示す。
