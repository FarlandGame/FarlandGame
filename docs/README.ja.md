# Bardiya Alizadeh · Farland_game

[English](https://github.com/FarlandGame) | [日本語](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.ja.md) | [فارسی](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.fa.md)

**Bardiya Alizadeh** です。**Kabir**、**Farland_game** という名前でも活動しています。このページでは、ソフトウェアのプロジェクトや創作活動を紹介しています。

## 作品紹介

### [Vexland_Manhunt](https://github.com/FarlandGame/Vexland_Manhunt)

**[Bardiya Alizadeh（Kabir）· Farland_game](https://github.com/FarlandGame) と [Ali · Alivexor](https://github.com/Alivexor) が共同制作した、Minecraftのランナー対ハンターを一通り楽しめるプラグインです。**

Vexland_Manhuntは、試合の準備、チームの役割、追跡の開始、トラッキング、進行状況、報酬、結果表示、管理機能を1つのPaperサーバープラグインにまとめています。ランナーはエンダードラゴンの討伐を目指し、ハンターは最後のランナーを倒そうとします。複数のランナーに対応し、死亡、リスポーン、ディメンション間の移動、再接続があっても追跡を続けられるようにしています。管理者は`/mhgui`のコントロールセンターからメニューで試合を操作でき、プレイヤー向けのメッセージやガイドブックも選択した言語で表示されます。

#### ダウンロードと互換性

| ファイル / バージョン | ダウンロード | 用途 |
|---|---|---|
| **1.13.1 — 現行版** | [VexLandManhunt-1.13.1.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/VexLandManhunt-1.13.1.jar) | Bardiya と Ali が制作した Manhunt プラグイン |
| **GrimAC 2.3.73 — 必須** | [grimac-bukkit-2.3.73.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.13.1/grimac-bukkit-2.3.73.jar) | 別途必要なサードパーティ製アンチチート |
| 1.9.11 — アーカイブ版 | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | 以前の Manhunt ビルド |
| 1.6.4 — アーカイブ版 | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | さらに古い Manhunt ビルド |

**対象環境：Paper 1.21.11、Java 21。** 1.6.4、1.9.11、1.13.1 はプラグインのリリース番号であり、対応する Minecraft のバージョン番号ではありません。1.13.1 では GrimAC が必須依存関係となり、連携ブリッジには 2.3.73 API が必要です。**現行版の JAR を両方**ダウンロードしてください。サーバープラグインのため、プレイヤーがクライアントの mods フォルダーに入れる必要はありません。

これらは個人サーバー向けのオリジナルビルドで、制作者固有の高度な管理権限を含め、提供された状態のまま保存されています。本マニュアルでは公開 Manhunt 操作を説明します。

#### Manhuntの体験

- **ランナーとハンターのチーム：** オンラインプレイヤーをどちらかのチームに割り当てます。試合には最低1人のランナーと、1人のハンターまたは役割未割り当てのオンラインプレイヤーが必要です。味方が死亡しても生存中のランナーは続行し、死亡したランナーは、その死亡で試合が終了する場合を除いてハンターになります。
- **演出付きの試合開始：** インベントリとゲームモードを準備し、チームを紹介してから、ルーレットでランナーの先行時間を決めます。そのカウントダウン中、ハンターは動けず、画面のタイトルと音で状況が通知されます。先行時間はランダムで、管理者はハンターを早めに解放することもできます。
- **追跡対象を選べるコンパス：** ハンターには専用コンパスが渡されます。右クリックで対象メニューからランナーを選び、追跡中に対象を変更できます。別のディメンションにいる場合は、直接追跡できるようになるまで関連するポータル経路を案内します。リスポーンしたハンターには追跡用コンパスが再び渡されます。
- **進行状況の表示：** ボスバーと試合情報に、ランナーの装備、ネザーの資源、ブレイズロッド、エンダーパール、エンダーアイ、要塞、ジ・エンドへの進行を反映します。新しいビルドでは、より細かな段階とドラゴンの体力を反映した進行表示が加わります。
- **ランナーのキル報酬：** 試合中にランナーがハンターを倒すと、進行度を考慮した50項目の重み付き報酬プールが使われます。アニメーション付きの抽選、ダブル／トリプル報酬、連続キルの通知、レアアイテム獲得時の演出が含まれます。
- **勝利と結果：** 最後のランナーが死亡するとハンターの勝利、エンダードラゴンを倒すとランナーの勝利です。試合終了のタイトル、祝勝演出、キル／死亡情報、一時的なアイテムの片付けも含まれます。新しいビルドでは、MVP、ダメージ、移動距離の結果も表示します。
- **チーム連絡と便利な機能：** `/teammsg`で味方だけにメッセージを送り、`/trash`で54スロットの廃棄用インベントリを開き、`/nv`で自分の暗視を切り替えられます。
- **メニューによる管理：** コントロールセンターには、役割、開始／リセット、ハンターの早期解放、フレンドリーファイア、サーバーロック、全員のテレポート、回復／食料補充、言語、防護設定、状態、ガイドブックがあります。フリーズと完全リセットは、次の試合の準備にも使えます。
- **多言語ガイド：** ランナー、ハンター、管理者向けの本で、目標、追跡用コンパスの使い方、死亡、準備、コマンドを説明します。1.9.11では、`/mhhelp`でプレイヤーの役割に応じたガイドが渡されます。
- **Paper Anti-Xrayとの連携：** メニューからPaperのワールド単位の保護を設定します。変更を反映するにはサーバーの再起動が必要です。

#### 1.13.1 の新機能

提供された 1.9.11 ビルドからの変更点：

- **ゴースト観戦者：** 管理者が割り当てる独立した役割。保護された飛行、他プレイヤーからの非表示、状態の保存と復元、ページ分けされた参加者へのテレポートメニューを備えます。
- **刷新されたコントロールセンター：** カテゴリー別メニュー、明示的な四種類の役割選択、名前付きの対象選択、再接続猶予時間の選択、Classic/Fast/Hardcore/Custom プリセット、専用の 30 秒確認画面。
- **GrimAC 連携：** 必須の GrimAC 2.3.73 が、従来有効だった VexAC の起動経路を置き換えます。GUI から全体、五つの検査グループ、通知、監視/適用モードを操作できます。Paper Anti-Xray は独立しています。
- **新しい Smart Hunter Kit プランナー：** Runner の装備とエンチャント、最寄りの Runner、チーム人数、距離、ディメンション、地形に応じて装備と補給を調整します。既存のより強い装備を保持し、道具の重複を避け、30 秒間の履歴で消耗品の補充量を制限します。固定の装備差や実測されたバランスを保証するものではありません。
- **検証付き復旧：** SHA-256 で封印したスナップショット、スキーマ/状態チェック、有効なバックアップへのフォールバックを使用します。無効または新しい形式のスナップショットは上書きせず保持します。観戦者の状態は別途永続化します。
- **メッセージの拡充：** 各同梱翻訳のキー数は 683 から 762 に増えました。ゲーム内の言語は従来と同じ十言語です。新たに二つの公開コマンド `/mspectator <player>` と `/mhspectate` が登録されています。
- **リセット時の代替動作：** オーバーワールドのスポーン地点付近に安全な地面が見つからない場合、無理にテレポートせず、その処理を省略できます。

#### `/mhgui` で始める

1. Paper 1.21.11 / Java 21 のサーバーに VexLandManhunt-1.13.1.jar と grimac-bukkit-2.3.73.jar の両方を入れ、完全に再起動します。
2. 信頼できる OP として参加し、**`/mhgui`** を実行します。
3. **Player Roles** でプレイヤーを選び、Runner、Hunter、Spectator、No Team を指定します。Runner と Hunter を少なくとも 1 人ずつ設定します。
4. **Match Settings**、**Global Language**、**GrimAC Security** を確認し、**Server Freeze** をオフにします。
5. **Match Controls → Start Match** をクリックします。解放後、Hunter はコンパスを右クリックして Runner を選びます。
6. Spectator はコンパスか `/mhspectate` を使います。管理者は Match Controls で Pause/Resume や確認付きの Reset Match を行います。

**[完全な GUI ガイドとコマンド一覧](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ja.md)**

#### Dreamへの冗談まじりの挑戦

Bardiyaから、ちょっとしたMinecraftの軽口です 😄

> 「はぁ……僕とAliのManhuntプラグインはDreamの100倍よくなったのに、Dreamは怖がって僕らのプラグインを遊んでくれないんだ！」

**説明の言語 (18):**

[English](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/README.md) · [日本語](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ja.md) · [فارسی](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.fa.md) · [Deutsch](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.de.md) · [Français](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.fr.md) · [Español](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.es.md) · [Português (Brasil)](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.pt-BR.md) · [Italiano](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.it.md) · [Nederlands](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.nl.md) · [Polski](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.pl.md) · [Українська](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.uk.md) · [Türkçe](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.tr.md) · [Русский](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ru.md) · [简体中文](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.zh-CN.md) · [繁體中文](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.zh-TW.md) · [한국어](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ko.md) · [हिन्दी](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.hi.md) · [Bahasa Indonesia](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.id.md)

### [Farland_autcliker](https://github.com/FarlandGame/Farland_autcliker)

<!-- APP_DOCUMENTATION -->
**説明の言語 (18):**

[English](https://github.com/FarlandGame/Farland_autcliker/blob/main/README.md) · [日本語](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ja.md) · [فارسی](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.fa.md) · [Deutsch](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.de.md) · [Français](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.fr.md) · [Español](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.es.md) · [Português (Brasil)](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.pt-BR.md) · [Italiano](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.it.md) · [Nederlands](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.nl.md) · [Polski](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.pl.md) · [Українська](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.uk.md) · [Türkçe](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.tr.md) · [Русский](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ru.md) · [简体中文](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.zh-CN.md) · [繁體中文](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.zh-TW.md) · [한국어](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ko.md) · [हिन्दी](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.hi.md) · [Bahasa Indonesia](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.id.md)

**[Windows 用をダウンロード](https://github.com/FarlandGame/Farland_autcliker/releases/latest/download/Farland_autcliker.zip)** · [ソースコードを見る](https://github.com/FarlandGame/Farland_autcliker) · [日本語の使い方](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ja.md)

Farland_autcliker は、**Bardiya Alizadeh（Kabir）／活動名 Farland_game** が制作した Windows 用デスクトップアプリです。主な特徴は、自動クリックの開始方法にあります。**実際にマウスをクリックするたびに、そのクリックをきっかけとして、1 秒間の追加クリック処理が始まります。** 自分のマウス操作で追加クリックの開始タイミングを決め、左右のボタンを個別に調整したい人に向けた設計です。ペルシャ語の画面、変更可能な操作キー、設定の保存、すぐに使える Windows 実行ファイルを備えています。

#### 実際のクリックから追加クリックへ

オートクリッカーを有効にしてから、左または右ボタンをクリックします。実際のクリックは通常どおり送信され、その後の 1 秒間に同じボタンの追加クリックが予定されます。たとえば左側を **20 CPS** に設定すると、実際の左クリック 1 回につき、**左の追加クリック 20 回**が予定されます。対象アプリの入力処理によりますが、実際の 1 回を含めると、要求されるクリック数は合計 21 回です。

最初の処理が終わる前に再びクリックすると、別の追加クリック処理が始まります。左を 2 回クリックした場合、それぞれの 1 秒間の処理を合わせて、追加クリック 40 回が予定されます。そのため CPS は**個々の処理の設定値**であり、重なった処理全体の上限ではありません。新しい実際のクリックがなければ、新しい処理は始まりません。すでに予定された処理は、完了するかオートクリッカーを停止するまで続きます。

#### 操作の流れの違い

よく使われる[停止するまで繰り返す方式](https://www.opautoclicker.com/)では、開始操作後にクリックを繰り返します。Farland_autcliker の特徴は、**実際のクリックごとに追加クリック処理を始めること**と、左右の設定を個別に持つことです。

| 操作 | 停止するまで繰り返す方式 | Farland_autcliker |
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
| GitHub | [FarlandGame](https://github.com/FarlandGame) |
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
