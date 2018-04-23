<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MCBE Portal Project 仕様書</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><blockquote>
<p>プロジェクトの方針と大体の機能を纏めたり、あとは各々のロジックを図で表したりしてグループで理解と効率化を図る</p>
</blockquote>
<h1 id="mcbe-portal-project">MCBE Portal Project</h1>
<h2 id="メンバー">メンバー</h2>

<table>
<thead>
<tr>
<th>発案・バックエンド担当</th>
<th>かずえもん (@mcpe_kazuemon)</th>
</tr>
</thead>
<tbody>
<tr>
<td>アイデア担当</td>
<td>うらむんオイル (@UramnOIL)</td>
</tr>
<tr>
<td>公式サイト担当</td>
<td>そうたん (@soutan_fon)</td>
</tr>
<tr>
<td>アイコンお願い (<strong>予定</strong>)</td>
<td>うろのるさん (@URNR__)</td>
</tr>
<tr>
<td>宣伝動画お願い (<strong>予定</strong>)</td>
<td>るいるいさん (@chell_uoxou)</td>
</tr>
</tbody>
</table><h2 id="現時点で作る必要があるもの">現時点で作る必要があるもの</h2>
<ul>
<li>アプリの公式サイト</li>
<li>Webアプリ</li>
<li>スマホ用アプリ</li>
</ul>
<h2 id="環境など">環境など</h2>
<ul>
<li>
<p>主にGoogleのFirebaseを使用</p>
<ul>
<li>基本は<strong>無料</strong>で、スケールに応じて<strong>プラス課金</strong>可能</li>
</ul>
</li>
<li>
<p>バックエンド</p>
<ul>
<li>アカウント管理
<ul>
<li>Firebase Auth<br>
(<a href="https://firebase.google.com/products/auth/?hl=ja">https://firebase.google.com/products/auth/?hl=ja</a>)</li>
</ul>
</li>
<li>内部API (Nodejs)
<ul>
<li>Cloud Functions for Firebase<br>
(<a href="https://firebase.google.com/docs/functions/?hl=ja">https://firebase.google.com/docs/functions/?hl=ja</a>)</li>
</ul>
</li>
<li>データ管理
<ul>
<li>Firestore<br>
(<a href="https://firebase.google.com/products/firestore/?hl=ja">https://firebase.google.com/products/firestore/?hl=ja</a>)</li>
</ul>
</li>
</ul>
</li>
<li>
<p>Webアプリ</p>
<ul>
<li>Firebase Hosting<br>
(<a href="https://firebase.google.com/products/hosting/?hl=ja">https://firebase.google.com/products/hosting/?hl=ja</a>)</li>
</ul>
</li>
<li>
<p>スマホ用アプリ</p>
<ul>
<li>Flutter (クロスプラットフォーム開発可能)<br>
(<a href="https://flutter.io">https://flutter.io</a>)</li>
</ul>
</li>
</ul>
<h2 id="現在の課題">現在の課題</h2>
<ul>
<li>iOS向けのアプリをどのように公開するか
<ul>
<li>「プロ生ちゃんアプリ開発支援プログラム」(<a href="http://pronama.azurewebsites.net/2016/10/12/pronama-chan-developer-support-program/">http://pronama.azurewebsites.net/2016/10/12/pronama-chan-developer-support-program/</a>) を利用する。</li>
</ul>
</li>
</ul>
<h2 id="主な機能">主な機能</h2>
<p>基本的にはLobiのようなスレッドタイプの掲示板で、それぞれの用途に合わせて機能を追加する。<br>
以下3つを「メインカテゴリ(ディメンション)」とし、それぞれが「サブカテゴリ(チャンク)」とスレッドにつけられる「タグ」を持つ。</p>
<h3 id="inventory-インベントリ">Inventory (インベントリ)</h3>
<p>制作物の配布を行う場。</p>
<h4 id="サブカテゴリ">サブカテゴリ</h4>
<ul>
<li>ワールド</li>
<li>テクスチャ</li>
<li>スキン</li>
<li>Mod</li>
<li>アドオン (需要あり?)</li>
<li>PMMPプラグイン</li>
<li>Nukkitプラグイン</li>
<li>MiNETプラグイン</li>
<li>その他</li>
</ul>
<hr>
<h3 id="forum-フォーラム">Forum (フォーラム)</h3>
<p>質問、ユーザーとの交流を行う場。</p>
<h4 id="サブカテゴリ-1">サブカテゴリ</h4>
<ul>
<li>全般</li>
<li>テクスチャ</li>
<li>スキン</li>
<li>Mod</li>
<li>アドオン</li>
<li>コマンド</li>
<li>PMMPプラグイン</li>
<li>Nukkitプラグイン</li>
<li>MiNETプラグイン</li>
<li>その他</li>
</ul>
<hr>
<h3 id="invite-インバイト">Invite (インバイト)</h3>
<p>宣伝、募集を行う場。</p>
<h4 id="サブカテゴリ-2">サブカテゴリ</h4>
<ul>
<li>Xbox</li>
<li>サーバー<br>
(サーバーステータス表示サービスの提供)</li>
<li>その他</li>
</ul>
<h2 id="その他機能">その他機能</h2>
<h3 id="discord連携">Discord連携</h3>
<p>新規スレッドがあった場合、スレッドの内容をDiscordに通知する。</p>
<h3 id="経験値システム仮">経験値システム(仮)</h3>
<p>ユーザーがどれだけ活動を行っているかどうかを、マイクラの「経験値」と「レベル」で表示する。</p>
<blockquote>
<p>製作者の意欲向上と、質問に対しての回答者がどれほど信頼出来るかを示す。</p>
</blockquote>
</div>
</body>

</html>
