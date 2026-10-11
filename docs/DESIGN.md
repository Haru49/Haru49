# Haru49 Profile — Design & Evidence

制作日: 2026-10-11（Asia/Tokyo）

## デザインコンセプト

**Engineering Intelligence, Designing Experiences.**

ヒューマノイド制作を入口に、競技ロボットの制御とインタラクティブアートへつなげる。Creative Technologist × Research Engineer はデザインの方向性として扱い、本人の現職・肩書としては使用しない。プロフィールでは学生であることを明示する。

ヒーローは黒い画面、白い二段組の名前、紫の磁力線で構成。磁力線は正負の点源から数値積分した流線を回転・配置したオリジナルの抽象表現で、実機の計測や物理的性能を示す図ではない。発光フィルター、バッジ、絵文字、実績カウンターは使わない。

| Token | Value | 用途 |
| :--- | :--- | :--- |
| Background | `#0D0D12` | SVGの背景 |
| Primary | `#A78BFA` | 流線・接続線 |
| Secondary | `#C4B5FD` | 補助見出し |
| Text | `#F5F5F7` | 名前・主見出し |
| Muted | `#9CA3AF` | 補足情報 |

SVGの外側はGitHubのテーマに従う。本文を画像に閉じ込めず、自己紹介・プロジェクトの説明・技術・リンクはテキストで提供する。

## 情報設計

Hero → About → Selected work → Experience → Tools → Currently exploring → Connect。

最初の文を「I’m building a humanoid robot and creating interactive art.」とする。本人が何を作っているかを先に示し、学校・競技経験・研究開発への関心を続ける。ヒーローの Physical AI は関心領域であり、実装済みの学習制御・研究成果を意味しない。

プロジェクトは一列で配置し、小さい画面でも二列のカードが潰れない構成とした。名前・説明・使用技術・リンクの順序を統一する。Kinetic Canvasだけは既存の作品写真を使い、ロボット2件は「ABSTRACT DIAGRAM」と明記したソフトウェア構成の図にする。

## 参考プロフィールの調査

以下の4件を実際に閲覧した。GitHub上のテキスト構成とリンクは確認済み。外部ポートフォリオの全ページやGitHubに表示されない画像の視覚効果まで評価したものではない。

| 参考 | 第一印象・構成 | Haru49への応用 |
| :--- | :--- | :--- |
| [anuraghazra](https://github.com/anuraghazra) | 短い自己紹介、箇条書きの経歴、代表リポジトリへの導線。技術領域が早く伝わる。 | 冒頭を短くし、作品から技術が伝わる説明にする。Statsの形式は採用しない。 |
| [sindresorhus](https://github.com/sindresorhus) | 短い個性的なREADMEとアプリ・ブログのリンク。詳細はPinned repositoriesへ委ねる。 | 情報量を抑え、外部ポートフォリオに詳細を任せる。 |
| [bchiang7](https://github.com/bchiang7) | 極めて短いREADME。Pinnedには個人サイトの複数世代と制作物が並ぶ。 | Web作品との導線を簡潔にする。Haru49ではロボット制作の説明を補う。 |
| [craftzdog](https://github.com/craftzdog) | 独特なプロフィール文とホームページへのリンク、用途が異なるPinned作品。 | 技術だけでなく個性を表し、作品を一つのトーンで紹介する。 |

4件とも、GitHub標準のプロフィール情報・Pinnedと外部サイトを組み合わせている。Haru49ではHeroだけに独自の視覚表現を集め、本文の階層と技術表記を統一する。レイアウトやグラフィックはコピーしていない。

## リポジトリ調査と選定理由

GitHubの公開APIからREADMEと再帰的なファイル一覧を取得し、下記の実ファイルを読んだ。リポジトリ一覧の言語集計だけでは判断していない。

| Repository | 確認した内容・段階 | 掲載判断 |
| :--- | :--- | :--- |
| [humanoid-project](https://github.com/Haru49/humanoid-project) | ESP32、六軸下半身、サーボ制御、支持された動作、NEXUSのローカル収集・制御UI。C++の現行mainとTypeScript collectorを確認。写真・歩行映像は公開ツリーに見つからない。 | **先頭に掲載。** 本人の現在のヒューマノイド制作を具体的に伝えられる。 |
| [Team9494_TurretSwerve](https://github.com/Haru49/Team9494_TurretSwerve) | Javaのfield-oriented drive、heading reset、module lock、pose telemetryを実装。公開版の自律コマンドはnull。写真・デモなし。 | **掲載。** 実際の競技ロボット制御を説明できる。リポジトリ名にTurretがあるが、公開コードで確認できないタレット機能は紹介しない。 |
| [Learning_FRC](https://github.com/Haru49/Learning_FRC) | READMEなし。RobotContainerにはWPILibのExampleSubsystemとExampleCommandを使う学習用構成。画像・デモなし。 | 学習記録として有用だが、代表作ではMini Swerveを優先。 |
| [haruta.github.io](https://github.com/Haru49/haruta.github.io) | READMEなし。index.htmlは短い初期HTML。画像・デモなし。Haru49の正規ユーザーサイト名とも異なる。 | ポートフォリオの主導線には使わない。 |
| [portfolio](https://github.com/Haru49/portfolio) | React/Vite、フィルター、作品詳細、レスポンシブUI。App.jsxにKinetic Canvasの説明・写真指定がある。公開サイトも表示確認できた。 | **Kinetic Canvasの紹介元として掲載。** ハードウェア制作と体験設計をつなぐ作品。サイト全体はConnectからリンク。 |
| [ai-security-camera](https://github.com/Haru49/ai-security-camera) | READMEとarchitecture等の設計文書のみ。Kotlin/CameraX、Python/FastAPI、MediaPipeは予定する構成。実装コード・画像・デモは公開ツリーにない。 | 完成したコンピュータビジョン製品として紹介しない。今後コード・デモが公開されたら再検討。 |
| [hamster](https://github.com/Haru49/hamster) | READMEはFlutterの初期文。lib/main.dartは風景画像をランダム表示するSceneryGacha。Dart/Flutter。独自UIのスクリーンショットなし。 | ロボット制作・アートを主軸にするため今回は省略。C++の言語集計を本人の実装言語と誤認しない。 |

## 掲載内容の根拠

### 本人提供の情報

制作依頼文の Haruta Suzuki、学校名、日本在住、デザイン・エンジニアリング・起業の学習、FRCのロボット開発経験、FGC 2025 Team Japan、ロボティクスの研究開発を目指すことを使用した。これらは本人申告であり、参加者名簿や学校による独立した照合は行っていない。受賞・論文・研究職・職務年数は追加していない。

GitHub APIの表示名は`hall`だったが、READMEでは本人が指定したHaruta Suzukiを使用する。

### 公開ソースで確認したこと

- ヒューマノイド: [README](https://github.com/Haru49/humanoid-project/blob/main/README.md)、[supported-squat README](https://github.com/Haru49/humanoid-project/blob/main/firmware/supported-squat/README.md)、[現行main.cpp](https://github.com/Haru49/humanoid-project/blob/main/firmware/supported-squat/src/main.cpp)。BNO08x/SCServo、WALKコマンド、heartbeat処理を確認。公開READMEはv34をソース段階、最後の実機書き込みをv33と記す。今回は実機を操作・ビルド・試験していない。
- NEXUS: [README](https://github.com/Haru49/humanoid-project/blob/main/nexus/README.md)、[collector.ts](https://github.com/Haru49/humanoid-project/blob/main/nexus/server/collector.ts)、[package.json](https://github.com/Haru49/humanoid-project/blob/main/nexus/package.json)。SerialPort、保存層、ローカルUIの構成を確認。READMEは旧React UIを過去のコードと明記しているので、旧UIを現行画面として紹介しない。
- Mini Swerve: [SwerveSubsystem.java](https://github.com/Haru49/Team9494_TurretSwerve/blob/main/src/main/java/frc/robot/subsystems/SwerveSubsystem.java)、[RobotContainer.java](https://github.com/Haru49/Team9494_TurretSwerve/blob/main/src/main/java/frc/robot/RobotContainer.java)。自律走行・タレット機能は掲載しない。PathPlannerは依存ファイルがあるだけなのでスキル表には載せない。
- Kinetic Canvas: [portfolio/src/App.jsx](https://github.com/Haru49/portfolio/blob/main/src/App.jsx)と[公開プロジェクトページ](https://haru49.github.io/portfolio/?project=project-kinetic-canvas)。2025の制作、TouchDesigner、2026制作中は本人ポートフォリオの記述。説明文にはAIによる初稿・本人確認待ちの注記があるため、受賞や規模などの新しい主張は追加しない。
- Web技術: [portfolio/package.json](https://github.com/Haru49/portfolio/blob/main/package.json)、App.jsx、NEXUSのpackage.jsonとcollectorを確認してReact・Vite・TypeScript・JavaScriptを掲載。

### 未確認のこと・掲載しなかったこと

- 自立歩行、閉ループの平衡制御、v34の実機検証。公開READMEに示される限界を越える説明はしない。
- ヒューマノイドREADMEが参照するINFORMATION_INDEX、handoff、telemetry-analysis文書等の一部は公開ツリーにない。非公開の詳細実験記録を閲覧したことにはしない。
- AI防犯カメラのローカル実装の有無。公開リポジトリにコードがないことと、本人が別の場所で未実装であることは同義ではない。
- FGCの受賞、FRCの順位、研究成果、未確認の所属・役職。
- 公開連絡先。GitHub APIのemailはnull。ポートフォリオの`000000@kamiyama.ac.jp`と電話番号はREADMEでも仮連絡先と明記されるため転記しない。
- Python、GLSL、Arduino、Figma等の習熟度。プロフィールのスキル表は今回直接確認した実装・制作ツールに絞った。

## アセットと保守

| File | 内容 |
| :--- | :--- |
| `assets/hero.svg` | 1200×560のデスクトップ用ヒーロー |
| `assets/hero-mobile.svg` | 680×766。600px以下の画面幅で使用 |
| `assets/projects/humanoid.svg` | 六軸・ESP32・NEXUSの抽象構成図 |
| `assets/projects/swerve.svg` | ゲームパッド・YAGSL・四輪の抽象制御図 |
| `assets/projects/kinetic-canvas.webp` | 公開portfolioの2025年作品写真。元画像を加工せずコピー |

写真の元: [kinetic-2025-main.webp](https://github.com/Haru49/portfolio/blob/main/public/photo/kinetic-2025-main.webp)。既存の本人ポートフォリオ内で使われている写真として採用。写真の権利・人物の公開許可を独立に確認したものではない。

SVGはテキスト・path・基本図形・clipPathだけで構成。外部フォント・外部画像・スクリプト・foreignObject・アニメーションは使わない。名前や文章はSVG内で直接編集できる。READMEの説明・技術・リンクはMarkdownで更新する。

今後実機写真を追加する場合は、同じパスを差し替え、READMEのaltと「抽象図」の文言も実際の写真に合わせて編集する。作品写真は現在のように比率を保持する。

## GitHubの制約と検証方法

- GitHubのページ背景は変更できない。独自配色はSVG内に限定する。
- 標準Markdown、表、画像、picture/sourceを使う。任意CSSやJavaScriptをREADMEに入れない。
- [GitHub公式の画像ガイド](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github)のpictureパターンを踏まえ、実際のGitHub Markdown APIでもsourceのmedia/srcsetが保持されることを確認する。
- Heroの画像が読めない場合もaltと直後の本人名・学校情報が意味を伝える。写真と構成図には具体的なaltをつける。
- GitHub Markdown APIでGFMをレンダリングし、画像属性・見出し・表が保持されることを確認する。公開APIへの送信はレンダリングのみで、リポジトリへの変更・公開は行わない。
- ライト・ダークのローカルプレビューはGitHub Markdown風のCSSを用いた近似。GitHubプロフィールの外枠・Camo画像プロキシでの実表示まで保証するものではない。
- Stats、Top Languages、外部動的SVGサービスは使わない。本人と作品を主役にし、外部画像サービスへの運用依存を減らす。
- プロフィール表示の要件は[GitHub公式](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme)を確認。既存のHaru49/Haru49リポジトリを使用し、新しいリポジトリは作らない。

## 次の改善

1. ヒューマノイドの全体写真と、支持条件・操作内容が伝わる短い実機動画を追加する。
2. Mini Swerveの実機写真と走行デモを追加する。
3. Kinetic Canvas 2026の完成記録ができたら2025の写真と区別して更新する。
4. 公開用メールアドレスを決めた後にConnectへ追加する。
5. GitHubへ反映した後、実際のプロフィールでCamo経由のSVGとモバイル表示を確認する。

検証結果とファイルの変更記録は`REPORT.md`に記載。
