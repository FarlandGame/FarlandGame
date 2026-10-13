# Bardiya Alizadeh · Farland_game

[English](https://github.com/FarlandGame) | [日本語](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.ja.md) | [فارسی](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.fa.md)

**Bardiya Alizadeh** です。**Kabir**、**Farland_game** という名前でも活動しています。このページでは、ソフトウェアのプロジェクトや創作活動を紹介しています。

## 作品紹介

### [Farland Auto Clicker](https://github.com/FarlandGame/Farland-Auto-Clicker)

**[Windows 用をダウンロード](https://github.com/FarlandGame/Farland-Auto-Clicker/releases/latest/download/Farland-Auto-Clicker.zip)** · [ソースコードを見る](https://github.com/FarlandGame/Farland-Auto-Clicker) · [日本語の使い方](https://github.com/FarlandGame/Farland-Auto-Clicker/blob/main/docs/README.ja.md)

Farland Auto Clicker は、**Bardiya Alizadeh（Kabir）／活動名 Farland_game** が制作した Windows 用デスクトップアプリです。主な特徴は、自動クリックの開始方法にあります。**実際にマウスをクリックするたびに、そのクリックをきっかけとして、1 秒間の追加クリック処理が始まります。** 自分のマウス操作で追加クリックの開始タイミングを決め、左右のボタンを個別に調整したい人に向けた設計です。ペルシャ語の画面、変更可能な操作キー、設定の保存、すぐに使える Windows 実行ファイルを備えています。

#### 実際のクリックから追加クリックへ

オートクリッカーを有効にしてから、左または右ボタンをクリックします。実際のクリックは通常どおり送信され、その後の 1 秒間に同じボタンの追加クリックが予定されます。たとえば左側を **20 CPS** に設定すると、実際の左クリック 1 回につき、**左の追加クリック 20 回**が予定されます。対象アプリの入力処理によりますが、実際の 1 回を含めると、要求されるクリック数は合計 21 回です。

最初の処理が終わる前に再びクリックすると、別の追加クリック処理が始まります。左を 2 回クリックした場合、それぞれの 1 秒間の処理を合わせて、追加クリック 40 回が予定されます。そのため CPS は**個々の処理の設定値**であり、重なった処理全体の上限ではありません。新しい実際のクリックがなければ、新しい処理は始まりません。すでに予定された処理は、完了するかオートクリッカーを停止するまで続きます。

#### 操作の流れの違い

よく使われる[停止するまで繰り返す方式](https://www.opautoclicker.com/)では、開始操作後にクリックを繰り返します。Farland Auto Clicker の特徴は、**実際のクリックごとに追加クリック処理を始めること**と、左右の設定を個別に持つことです。

| 操作 | 停止するまで繰り返す方式 | Farland Auto Clicker |
| --- | --- | --- |
| 追加クリックの開始 | 繰り返し処理を開始 | 有効にしてから実際にクリック |
| 新しい実際のクリック | 繰り返しの継続には不要 | 新しい追加クリック処理を開始 |
| 処理の終了 | 繰り返し処理を停止 | 各処理が 1 秒間の予定を完了 |

この比較は 2 種類の操作方式を説明するものです。他のオートクリッカーが追加のモードを備えている場合もあります。ここでは、実際のコードで確認できる動作と操作を紹介しています。

#### 左右を個別に調整

左右それぞれを **1～10,000 CPS** に設定でき、各ボタンを個別に有効／無効にできます。左を 20 CPS、右を 8 CPS に設定した場合、左クリックは左の処理を、右クリックは右の処理を開始します。一方を無効にすると、そのボタンの実際のクリックは通常どおり働き、新しい追加クリックを発生させません。

#### 自分の環境に合わせた操作

メインボタン、または中央ボタン、左右のサイドボタン、F6～F9、Home、End、Insert から選んだグローバルホットキーで、有効／無効を切り替えられます。**F12** は緊急停止と終了に使います。ダーク、ライト、パープル、ブルーの 4 種類のテーマがあります。クリック速度、左右の有効状態、ホットキー、テーマは次回起動時にも復元されます。無効なクリック速度の入力は、直前の有効な値に戻ります。

#### 追加クリックを適切に処理

実際の入力と Windows が注入された入力として識別するクリックを区別し、アプリ自身が作ったクリックで新しい処理が始まることを防ぎます。スケジューラーが重なった処理を管理し、高速時はクリックを小さな単位にまとめて送信します。**10,000 CPS は設定可能な上限であり、実測速度の保証ではありません。** 実際の送信速度はパソコンの性能、Windows の入力処理、対象アプリに依存します。

#### ダウンロードとソースコード

公開 ZIP には実行ファイル、ソースコード、画面のプレビュー、英語・日本語・ペルシャ語の説明が入っています。展開後に `Farland-Auto-Clicker/dist/Farland Auto Clicker.exe` を開けば使え、実行ファイル版には Python の別途インストールは必要ありません。ソースコードの対象は Windows 10 または 11 と Python 3.10 以降で、Tkinter と Windows API を使用しています。リポジトリには、クリックを模擬して実行する 6 件のテストもあります。スケジューリング、左右の同時処理、取り消し、ホットキー、注入された入力の除外を確認します。

**使用技術：** Python · Tkinter · Windows API · PyInstaller

## リンク

### チャンネルと SNS

| プラットフォーム | チャンネル／ページ |
| --- | --- |
| YouTube | [Farland_game](https://www.youtube.com/@Farland_game) · [Farland_animation](https://www.youtube.com/@Farland_animation) |
| Rubika チャンネル | [farland_gam](https://rubika.ir/farland_gam) · [Farland_animatio](https://rubika.ir/Farland_animatio) |
| Rubika ページ | [farland_game](https://rubika.ir/farland_game) · [Farland_animations](https://rubika.ir/Farland_animations) |
| Instagram | [farland_game](https://www.instagram.com/farland_game/) |
| Telegram チャンネル | [Farland_gam](https://t.me/Farland_gam) · [Farland_animatio](https://t.me/Farland_animatio) |
| Twitch | [farlandgame](https://twitch.tv/farlandgame) |
| Kick | [farlandgame](https://kick.com/farlandgame) |
| Aparat | [Farland_Game](https://aparat.com/Farland_Game) |
| SoundCloud | [Bardiya Kabir](https://soundcloud.com/bardiya-kabir-798008614) |

### Telegram 音楽ボット

[Farland Music Bot](https://t.me/Farland_Music_bot) — 曲の動画リンクを Telegram ボットに送って、曲を探せます。

### コミュニティと家族

- **THE APEX：** [YouTube](https://www.youtube.com/@THE_APEX_MC) · [Telegram](https://t.me/+-3uY7eIZArVjZDE0)
- **Manhunt：** [Telegram グループ](https://t.me/+DAq20XrkPyZhNjVk)
- **兄弟のチャンネル：** [YouTube の ArmiyaFabix](https://www.youtube.com/@ArmiyaFabix)

### 活動を応援する

[Reymit で支援する](https://reymit.ir/farland_game) ❤️
