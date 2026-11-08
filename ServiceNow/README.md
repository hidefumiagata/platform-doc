---
title: ServiceNow ナレッジベース 全体目次（README）
category: meta
domain: general
release: Australia
last_verified: 2026-11-08
summary: ServiceNow ナレッジベースの入口。ナレッジの目的と読者、基準リリース（Australia、Brazil 併記）、情報の確度ラベル、画像の著作権の扱い、各編の役割、全 126 ファイルの一覧と要約、読者別の読み順、質問カテゴリから参照ファイルを引く対応表を示す。AI はまずこのファイルを読み、質問に応じて参照先を選ぶ。
keywords: [README, 目次, index, ServiceNow, ナレッジベース, 読み順, 参照ガイド, Australia, Brazil, 確度ラベル]
sources:
  - https://www.servicenow.com/docs/r/australia/release-notes/available-versions.html
  - https://www.servicenow.com/docs/r/brazil/release-notes/available-versions.html
---

# ServiceNow ナレッジベース 全体目次（README）

## 概要

このリポジトリ（`ServiceNow/`）は、ServiceNow（ServiceNow AI Platform と、その上で動く ITSM・ITOM・ITAM・HRSD・CSM・SecOps・IRM・SPM などの製品群）について、日本語でまとめた Markdown のナレッジベースである。この README は、人間の読者と AI の両方が最初に読む入口として置いている。ナレッジの前提（基準リリース、確度ラベル、画像の扱い）、各編の役割、全ファイルの一覧、読者別の読み順、質問カテゴリ別の参照先を示す。

- 執筆規約：[_CONVENTIONS.md](_CONVENTIONS.md)
- 用語集：[glossary.md](glossary.md)（A–Z、約 380 語。付録に早見表・旧名称対応表・日本語訳の揺れ）
- ファイル数：125（README を除く。01_入門編 9、02_リファレンス 80、03_導入編 19、04_応用編 15、ルート直下 2）

## 1. ナレッジの目的と読者

### 1.1 目的

このナレッジベースの目的は次の 3 つである。

1. **AI による質問回答の根拠にする**：AI（LLM／RAG）が読み込んで、ServiceNow の仕様・導入・運用に関する質問に、出典つきで正確に答えられるようにする。各ファイルはフロントマター（`title`／`summary`／`keywords`）と見出し単位で検索しやすいように書いている。見出しの直下では主語を省略しないため、1 つのチャンクだけを読んでも意味が分かる。
2. **人間の学習と調査に使う**：入門者が基本を体系的に学び、経験者が仕様を調べるためのリファレンスとして使う。
3. **導入・運用の判断材料にする**：ライセンス、エディション、導入方法論、運用設計、失敗パターンなどを、提案・設計・意思決定の場で使えるようにする。

### 1.2 想定読者

| 読者 | 主な用途 | 主に読む編 |
|---|---|---|
| 入門者（ServiceNow を初めて扱う人） | 基本概念・用語・画面の理解 | 01_入門編 |
| IT コンサルタント／PM | 提案、ライセンス・価格、導入計画、体制、ガバナンス | 03_導入編、04_応用編 |
| アーキテクト | インスタンス構成、データモデル、CMDB/CSDM、連携、セキュリティ | 02_リファレンス（platform）、03_導入編 |
| エンジニア／開発者・管理者 | テーブル、ロール、プロパティ、スクリプト、API、デバッグ | 02_リファレンス |
| AI（LLM／RAG） | 質問への回答根拠の検索 | 全編（本 README の対応表から参照先を選ぶ） |

## 2. 基準リリース（Australia、Brazil 併記方針）

- **基準リリースは Australia** である。Australia は 2026-05-05 に GA した。本ナレッジの作成時点（2026-11-02）で GA が確定していた最新ファミリーである。本文中で特に断りがない仕様は Australia 時点のものである。
- **次期ファミリー Brazil** は 2026-09-24 に EA となった。Brazil で変更・追加・廃止されると判明した事項は、本文中に次の形で併記している。
  > **Brazil での変更:** …
- Brazil の GA 日は公式表に明記されていない。2026-11-05 に Brazil Patch 2 が「Available」になったため、この日に GA したとみられる【推定】。詳細は [07-release-cycle.md](01_入門編/07-release-cycle.md) を参照。
- それより前のリリース（Zurich、Yokohama、Xanadu など）で入った機能は、導入リリースが分かる場合は「（Xanadu で導入）」のように書いている。
- リリース名の順序：… Utah → Vancouver → Washington DC → Xanadu → Yokohama → Zurich → **Australia** → **Brazil**（Zurich までは都市名、Australia からは国名）。
- 各ファイルのフロントマター `last_verified` は、そのファイルを最後に確認した日を示す。製品名の変更（例：Now Assist → ServiceNow Otto、Service Bridge → Service Exchange、APM → Enterprise Architecture）やパッケージ体系の変更（2026-04 に Standard/Pro/Enterprise から Foundation/Advanced/Prime へ移行）は頻繁に起こるため、回答に使う前に `last_verified` と出典を確認すること。

## 3. 情報の確度ラベル

本ナレッジの事実記述には、節ごとまたは文末に `[出典](URL)` を付けている。各ファイルの末尾「## 参照元」に URL の一覧がある。情報源は次の優先順位で採用している。

1. ServiceNow 公式ドキュメント（servicenow.com/docs、docs.servicenow.com）
2. 公式サイト・公式ブログ・リリースノート・ServiceNow Community の公式記事
3. Developer サイト（developer.servicenow.com）
4. パートナー・第三者のブログ・調査会社
5. フォーラムへの投稿

ラベルのない記述は公式情報に基づいている。公式情報以外に依拠する記述には、次のラベルを付けている。

| ラベル | 意味 | 読み方・使い方 |
|---|---|---|
| `【第三者情報】` | パートナー・第三者の公開情報に基づく | 公式に確認されたものではない。重要な判断に使う場合は公式情報で裏付けを取る |
| `【推定】` | 複数の情報から推定したもの（価格の推定値など） | 確定値ではない。価格は必ず「推定値・出典・取得日」とセットで書いている |
| `【経験則】` | 実務で一般に語られる知見 | 状況によって当てはまらないことがある |

- 確認できなかった事項は推測で埋めず、「公開情報では確認できず」と書いている。
- **価格**は公式に定価が公開されていない。価格に関する記述（主に [02-pricing.md](03_導入編/02-pricing.md)、[16-competitor-comparison.md](03_導入編/16-competitor-comparison.md)）はすべて【推定】である。
- AI が回答するときは、ラベルを省かずに回答へ引き継ぎ、出典 URL を添えること。

## 4. 画像の著作権について

- 本ナレッジの画像（画面スクリーンショットなど）は、ServiceNow 公式ドキュメントなどから取得したものである。保存先は `assets/images/<ファイルの slug>/` で、各ファイルから相対パスで参照している。
- **画像の著作権は ServiceNow, Inc. などの権利者に帰属する。本リポジトリの画像は社内の参照目的に限って使用し、外部へ再配布しない。** 本リポジトリ（またはその一部）を社外に共有する場合は、画像を除くか、権利者の許諾を確認すること。
- AI は画像を読めない前提で書いている。各画像の直下には、キャプション、画面の文章による説明（メニューの位置、主要項目）、出典 URL と取得日を置いている。画像を取得できなかった箇所は、公式ページへのリンクと文章による画面説明で代えている。

## 5. 編ごとの説明

| 編 | 目的 | 主な読者 | 内容 |
|---|---|---|---|
| [01_入門編](01_入門編/) | ServiceNow を語るうえで欠かせない基本事項 | 入門者が最初に読む | 会社概要、プラットフォームの全体像、製品ポートフォリオ、基本概念、UI、ITIL/ITSM、リリースサイクル、ユーザー・ロール・ライセンスの基本、学習パス、用語集 |
| [02_リファレンス](02_リファレンス/) | 製品仕様の詳細（テーブル、ロール、設定、API、画面） | AI の回答の主な根拠。エンジニア・アーキテクト | 領域別のサブフォルダ：`platform`（40）、`itsm`（10）、`itom`（10）、`itam`（4）、`spm`（4）、`customer`（5）、`employee`（3）、`secops`（1）、`irm`（1）、`industry`（1）、`other`（1） |
| [03_導入編](03_導入編/) | ライセンス・価格・エディション、導入方法論、運用 | コンサルタント・PM | ライセンスモデル、価格（推定）、エディション比較、方法論、体制、要件定義・設計、インスタンス戦略、データ移行、連携設計、セキュリティ、テスト、運用・ガバナンス、アップグレード、サポート、日本市場、競合比較、ROI、AMS、DR |
| [04_応用編](04_応用編/) | 導入・運用の経験者による知見（失敗パターン、ベストプラクティス） | 経験者・コンサルタント（**すべて出典 URL つき**） | 失敗パターン、技術的負債、性能、アップグレードの教訓、CMDB、ライセンス最適化、スクリプト、連携、CoE、AI 導入、ITSM 設計、セキュリティ強化、定着化、コンサルティング、展開ロードマップ |

**使い分けの目安**：「何ができるか・どう設定するか」は 02_リファレンス、「どう計画・契約・運用するか」は 03_導入編、「実際にどこでつまずくか・どうすればうまくいくか」は 04_応用編で調べる。同じテーマを複数の編で扱っている場合がある（例：アップグレードは 01-07、03-13、04-04）。その場合は、仕様 → 計画 → 知見の順に読むとよい。

## 6. 全ファイル一覧

各行の書式は「`[タイトル](相対パス) — フロントマター summary`」である。

### 01_入門編（9 ファイル）

- [ServiceNowとは（会社概要・沿革・市場ポジション・日本法人）](01_入門編/01-what-is-servicenow.md) — ServiceNow, Inc. がどのような会社か（創業・沿革・業績規模・顧客層・主要買収）、Gartner Magic Quadrant 等での市場ポジション、"The AI platform for business transformation" から "AI Control Tower" / "Super Intelligence Control Tower" へ変化してきた自社の位置づけ、日本法人 ServiceNow Japan 合同会社の概要に答える入門ファイル。
- [Now Platform（ServiceNow AI Platform）の全体像](01_入門編/02-platform-overview.md) — ServiceNow の製品群が乗る共通基盤「ServiceNow AI Platform（旧称 Now Platform）」とは何かを、単一プラットフォーム・単一データモデル・単一アーキテクチャ、マルチインスタンス方式の SaaS、ワークフロー、AI／データ／自動化の位置づけ、全体アーキテクチャ図の観点から入門者向けに説明する。
- [製品ポートフォリオ一覧（Product Portfolio）](01_入門編/03-product-portfolio.md) — ServiceNow の全製品を、ワークフロー領域（Technology / Customer / Employee / Creator / Finance and Supply Chain / Industry）と 2026 年時点の公式ソリューション分類の両面から一覧化し、各製品の1〜2行説明と本ナレッジ内の詳細リファレンスへの対応を示す。ServiceNow Otto・EmployeeWorks・Autonomous Workforce・製品ティア（Foundation/Advanced/Prime）・名称変更も整理する。
- [必須の基本概念（Core Concepts）](01_入門編/04-core-concepts.md) — ServiceNow を理解するうえで最低限必要な基本概念（インスタンス、テーブル・レコード・フィールド、sys_id、テーブル拡張と Task／CMDB、参照とドットウォーク、アプリケーションスコープ、プラグイン、ユーザー・グループ・ロール、ACL、ビジネスルール）を、入門者向けに相互の関係とともに説明する。
- [UIの基本（UI Basics）](01_入門編/05-ui-basics.md) — ServiceNow の画面（UI）の種類と基本操作を入門者向けに整理する。Next Experience UI（旧称 Polaris）と Unified Navigation、Classic environment／Core UI（旧 UI16）、リスト・フォーム・フィルター、Configurable Workspace、Service Portal、Employee Center、Now Mobile／Mobile Agent の役割と使い分け、日常操作のコツを、Australia リリース基準で説明する。
- [ITILとITSMの基礎（ITIL 4 と ServiceNow ITSM の対応）](01_入門編/06-itil-itsm-basics.md) — ITIL 4 の基本構造（SVS・サービスバリューチェーン・34 プラクティス）と ServiceNow ITSM の関係を整理し、インシデント／問題／変更／リクエスト／構成／ナレッジ／サービスレベル管理の各プラクティスが ServiceNow のどのモジュール・テーブル・ロールに対応するかを入門者向けに説明する。
- [リリースサイクルとバージョン（Release Cycle and Versions）](01_入門編/07-release-cycle.md) — ServiceNow の年2回のファミリーリリース、命名規則（都市名→国名）、Early Release Program（RTP/EA）と GA、Patch/Hotfix/Security patch の種類と命名、N/N-1 サポートポリシーと EOL、Store アプリの独立リリース、歴代リリース一覧を入門者向けに解説する。
- [ユーザー・ロール・ライセンスの基本（Users, Roles and Licensing Basics）](01_入門編/08-users-roles-licensing-basics.md) — ServiceNow のユーザー種別（Fulfiller／Business Stakeholder／Approver／Requester など）が、ロール（Role）とサブスクリプション（ライセンス）とどう結びついているかを入門者向けに説明し、誤解しやすいポイントを整理する。
- [学習パスと認定資格（Learning Path & Certifications）](01_入門編/09-learning-path.md) — ServiceNow を学ぶための公式学習基盤 ServiceNow University（旧 Now Learning）、無料の Personal Developer Instance（PDI）と Developer Program、認定資格体系（CSA / CAD / CIS 各種 / CTA / CMA ほか）と受験・維持の手続き、コミュニティ、日本語の学習リソースを、入門者向けに整理する。

### 02_リファレンス（80 ファイル）

#### platform — プラットフォーム共通機能（基盤・開発・UI・連携・AI・セキュリティ）

- [アクセス制御（Access Control List / ACL）](02_リファレンス/platform/access-control-acl.md) — ServiceNow の ACL（Access Control List）の仕組み（評価順序、テーブル/フィールド ACL、操作種別、ロール/条件/スクリプト/Security Attribute）、Deny-Unless ACL、Query ACL、Security Data Filters、Before Query Business Rule、デバッグ手段（Debug Security Rules・Access Analyzer）、High Security Settings と関連システムプロパティを網羅的に解説する。
- [アプリケーション開発（App Engine・ServiceNow Studio・ServiceNow IDE・ServiceNow SDK・Application scope・Source control・Application Repository・Store 公開）](02_リファレンス/platform/app-development.md) — ServiceNow AI Platform 上のカスタムアプリケーション開発について、App Engine / Creator Workflows の位置づけ、開発ツール（Creator Studio・App Engine Studio・ServiceNow Studio・Legacy Studio・ServiceNow IDE・ServiceNow SDK と ServiceNow Fluent・Build Agent）、Scoped / Global アプリケーションとアプリケーションアクセス設定、Delegated Development、Source control（Git）連携、Application Repository、ServiceNow Store 公開、App Engine Management Center のパイプラインを、テーブル名・ロール名・プロパティ・メニュー位置・制約まで含めて Australia リリース基準で解説する。
- [認証とSSO（Authentication and Single Sign-On）](02_リファレンス/platform/authentication-sso.md) — ServiceNow インスタンスへのログイン認証（ローカル認証・パスワードポリシー・アカウントロックアウト）、Multi-Provider SSO（SAML 2.0 / OIDC）とユーザープロビジョニング（JIT / SCIM）、Account Recovery、MFA（強制適用・MFA Context・Factor Policy・例外）、Adaptive Authentication（ポリシーコンテキスト・Filter criteria）、セッション管理、IP Address Access Control、API 認証（OAuth / Machine Identity Console、Basic 認証と Basic Auth Restriction、API Key、mTLS）の仕様・テーブル・ロール・プロパティを網羅的に解説する。
- [Automated Test Framework（ATF、自動テストフレームワーク）](02_リファレンス/platform/automated-test-framework.md) — ServiceNow 標準の自動テスト機能 Automated Test Framework（ATF）について、Test / Test suite / Test step / Step configuration のデータモデル、ロール、システムプロパティ、Client test runner、Parameterized test、Quick start tests、スケジュール実行、Cloud Runner と ATF Test Generator、Headless Browser、CI/CD API、Failure Insights・Code Coverage・Test Agent などの AI 機能、アップグレード時の活用方法をまとめる。
- [CMDB と CSDM（構成管理データベースと共通サービスデータモデル）](02_リファレンス/platform/cmdb-csdm.md) — ServiceNow の CMDB（cmdb_ci 階層、主要 CI クラス、CI Relationship、IRE、CMDB Health、CMDB Workspace、CMDB Data Manager）と CSDM 5（7 ドメイン、テーブル構成、Foundation/Crawl/Walk/Run/Fly の成熟度ステージ）の仕様を、Australia リリース基準でまとめたリファレンス。
- [コラボレーション機能（Visual Task Boards・Connect・Microsoft Teams/Slack 連携）](02_リファレンス/platform/collaboration-vtb-teams-slack.md) — ServiceNow のコラボレーション機能を横断的に整理する。Visual Task Boards（Freeform／Flexible／Guided ボード、レーン・スイムレーン・レーン制限、vtb_* テーブル、カード上限 glide.vtb.board_max）、Connect Chat／Connect Support（Core UI 専用・Next Experience 非対応・Connect Support は Utah で廃止）と後継の Sidebar、Conversational Integration（sn_va_teams／sn_va_slack による Microsoft Teams・Slack 上の Virtual Agent と ServiceNow Otto（旧 Now Assist））、ITSM／Major Incident 向けの Teams 連携（Start Microsoft Teams Chat、MIM workbench からのグループチャット、Notify connector、Meeting Extensions）と Slack 連携（Collaboration Services、/now スラッシュコマンド）、関連プラグイン・ロール・ライセンス、廃止・改称状況をまとめる。
- [Data Model and System Dictionary（データモデルとシステムディクショナリ）](02_リファレンス/platform/data-model-dictionary.md) — ServiceNow のデータモデルを、テーブル（sys_db_object）、テーブル拡張階層と 3 つの Extension model（Table per class / hierarchy / partition）、System Dictionary（sys_dictionary）の各項目、全フィールドタイプ一覧、Reference・List（glide_list）・Document ID・ドット・ウォーク、Choice list（sys_choice / sys_choice_set）、Dictionary override、Dictionary attributes、Australia で追加された Read-only option、Database views、Schema map、主要システムテーブル（sys_user, sys_user_group, task, cmdb_ci 等）の観点で網羅的に説明する。
- [デバッグ・トラブルシューティング（ログ・Script Debugger・Session Debug）](02_リファレンス/platform/debugging-troubleshooting.md) — ServiceNow でエンジニアが日常的に使う問題調査の手段（System Log／Transaction Log／Node Log、Script Debugger と Console、Session Log、Session Debug の各オプション、Script Tracer、JavaScript Log と Field Watcher、Access Analyzer、gs.info／gs.log／GSLog とスコープ別ログ、Flow 実行詳細、ECC Queue、アウトバウンド HTTP ログ、Transaction Quota によるキャンセル、Now Support への問い合わせ）を、ロール・プロパティ・メニュー位置・制約付きで横断的に整理する。
- [Domain Separation（ドメインセパレーション）](02_リファレンス/platform/domain-separation.md) — ServiceNow の Domain Separation（ドメインセパレーション）について、概念、データ・プロセス・UI の分離、ドメイン階層（TOP/Default/global）、Visibility/Contains ドメインと Domain scope、プラグインと有効化、MSP（サービスプロバイダー）向け設計、管理ツール、アプリ別サポートレベル、制約事項を網羅的にまとめる。
- [イベント（Event Registry）・Script Action・スケジュールジョブ](02_リファレンス/platform/events-script-actions-scheduled-jobs.md) — ServiceNow のサーバー側非同期処理の仕組み（sysevent キューとイベント処理、Event Registry、gs.eventQueue / eventQueueScheduled、Script Action、カスタムキューと Queue Registry、sys_trigger とスケジューラーワーカー、Scheduled Script Execution、非同期 Business Rule、Fix Script / Background Script、Flow の非同期実行との比較、監視とトラブルシューティング）を体系的にまとめる。
- [Workflow Studio / Flow Designer（ワークフロースタジオ／フローデザイナー）](02_リファレンス/platform/flow-designer-workflow-studio.md) — ServiceNow のローコード自動化環境 Workflow Studio（旧 Flow Designer・Process Automation Designer・Decision Builder を統合）の仕様を網羅する。Flow／Subflow／Action／Trigger／Data pill／Flow logic／Playbooks／Decision tables の構成要素、ロール、システムプロパティ、上限値、実行コンテキスト（execution details・状態値・reporting level）、Flow debugger、FlowAPI、レガシー Workflow Editor との違いに答える。
- [データインポート/エクスポート（Import Sets・Transform Map・Export Sets・IntegrationHub ETL）](02_リファレンス/platform/import-export-data.md) — ServiceNow へのデータ取り込み（Data Source、Import Set、Transform Map、Coalesce、Transform scripts、Scheduled import、Concurrent import、Robust Transform Engine、IntegrationHub ETL、Easy import、Import Set API）と、データ取り出し（リスト/フォーム/URL からの CSV・Excel・PDF・XML・JSON・Google Sheets エクスポート、Export limits、Export Sets、Scheduled/Delta/Parallel export）の仕様・テーブル・ロール・プロパティをまとめたリファレンス。
- [Instance Architecture（インスタンスアーキテクチャ）](02_リファレンス/platform/instance-architecture.md) — ServiceNow のマルチインスタンスアーキテクチャ、ノード構成、データセンターペアとリージョン（日本の東京・大阪を含む）、Advanced High Availability（AHA）とバックアップ／DR、インスタンス種別（本番／サブプロダクション／PDI／Developer Sandbox）、Hosting options（商用クラウド、Protected Platform、GCC/NSC、Private Stack＝Self-hosted）、RaptorDB（Standard/Professional）を説明する。
- [IntegrationHub（インテグレーションハブ）](02_リファレンス/platform/integrationhub.md) — ServiceNow IntegrationHub（Integration Hub）の構成要素（Spoke、Connection & Credential alias、REST/SOAP/PowerShell/SSH/JDBC 等の Integration step、Data Stream action、Remote tables、Retry policy）の仕様と、サブスクリプション・パッケージ（Starter/Standard/Professional/Enterprise）およびトランザクション課金の考え方をまとめたリファレンス。
- [Knowledge Management（ナレッジ管理）](02_リファレンス/platform/knowledge-management.md) — ServiceNow Knowledge Management の仕様リファレンス。Knowledge Base／Article の構造とテーブル、公開・退役ワークフロー（Workflow／Flow）、User criteria によるアクセス制御、KCS、Knowledge Blocks、Feedback、Article templates、バージョニング、Knowledge Center、検索（Zing／AI Search）、主要システムプロパティとロールを網羅する。
- [Lists and Forms（リストとフォーム）](02_リファレンス/platform/lists-forms.md) — ServiceNow の classic environment（クラシック環境）におけるリスト（List v2/v3、List Control、List editor、フィルタ・条件ビルダー・エンコードクエリ）とフォーム（Form Builder / Form Designer / Form Layout、セクション、ビュー、関連リスト、Formatter、UI Policy、Data Policy、Client Script との関係、パーソナライズ）の仕様、関連テーブル、ロール、システムプロパティをまとめる。
- [ローカライゼーション（日本語化）— Localization / Internationalization](02_リファレンス/platform/localization.md) — ServiceNow インスタンスを日本語化するための仕組み（I18N 言語プラグイン、5 つの翻訳テーブル、Localization Framework、Localization Workspace、Dynamic Translation、Now Assist の多言語対応）と、タイムゾーン・日付形式・ロケール・通貨などの System Localization 設定、日本語環境特有の注意点を、テーブル名・ロール・プロパティ単位で整理する。
- [MID Server（ミッドサーバー）](02_リファレンス/platform/mid-server.md) — ServiceNow インスタンスと顧客ネットワーク内のシステムを仲介する Java アプリケーション MID Server について、役割、ECC Queue を中心としたアーキテクチャ、インストール要件と方式、MID Server 選択（Applications / IP Ranges / Capabilities）、クラスタ、アップグレード、セキュリティ、コンテナ化、利用する機能（Discovery、Service Mapping、Event Management、Orchestration、IntegrationHub、Import Sets 等）を、テーブル名・ロール・パラメータ・プロパティのレベルまで整理する。
- [モバイル（ServiceNow Mobile Platform）](02_リファレンス/platform/mobile.md) — ServiceNow のネイティブモバイルアプリ（Now Mobile、ServiceNow Agent / Mobile Agent、旧 Onboarding アプリ）と、それを支える Mobile Platform（Mobile App Builder、Mobile Card Builder、画面階層と sys_sg_* テーブル、ディープリンク、プッシュ通知）、オフラインモード、認証・セキュリティ、共有デバイス、MDM/MAM（AppConfig、Intune、Workspace ONE、BlackBerry）、Mobile Publishing、Mobile SDK の仕様を、プラグイン・テーブル・ロール・プロパティ・メニュー位置まで含めて整理する。
- [Next Experience UI（ネクストエクスペリエンス UI）](02_リファレンス/platform/next-experience-ui.md) — ServiceNow のデスクトップ向け標準 UI である Next Experience UI（旧称 Polaris）について、Unified Navigation（All / Favorites / History / Workspaces メニュー等）の構成要素、テーマ（Coral / Polaris / Theme Builder / ダークテーマ）、ユーザー設定、Contextual side panel、Core UI（UI16）との違い、有効化・無効化のシステムプロパティと移行時の考慮事項をまとめる。
- [Notifications and Email（通知とメール）](02_リファレンス/platform/notifications-email.md) — ServiceNow の Email notifications（メール通知）、Email templates / Email layouts、Notification variables と Mail scripts、Inbound email actions、Email accounts（SMTP/POP3/IMAP/OAuth 2.0/Microsoft Graph）、Email properties、Notification preferences（購読・配信チャネル）、SMS / Push 通知、Email logs と通知のデバッグ方法を、テーブル名・フィールド・ロール・プロパティ単位で解説する。
- [Now Assist と AI Agents（ServiceNow Otto / 生成AI・エージェント型AI）](02_リファレンス/platform/now-assist-ai-agents.md) — ServiceNow の生成AI（Now Assist、2026年から ServiceNow Otto ブランド）とエージェント型AI（AI Agents、AI Agent Orchestrator、AI Agent Studio）、AI Skill Kit（旧 Now Assist Skill Kit）、AI Control Tower、LLM 選択（Now LLM／外部LLM／BYOK）、Assist 課金単位、AI Guardian・Data Privacy、主要製品別スキル、Brazil での変更を、テーブル・ロール・プロパティ・メニュー単位で整理する。
- [プラットフォームのパッケージ構成（Standard / Pro / Pro Plus / Enterprise → Foundation / Advanced / Prime）](02_リファレンス/platform/platform-licensing-packaging.md) — ServiceNow のパッケージ（旧 Standard / Pro / Pro Plus / Enterprise / Enterprise Plus と 2026-04 以降の Foundation / Advanced / Prime）ごとの Performance Analytics・Predictive Intelligence・Virtual Agent・Now Assist（ServiceNow Otto）・AI Agents・Process Mining 等の機能差を製品横断で整理する。インスタンス上で権利（Entitlement）を確認する方法（Subscription Management）も記載する。
- [プラットフォームセキュリティと暗号化（Platform Security and Encryption）](02_リファレンス/platform/platform-security-encryption.md) — ServiceNow AI Platform のインスタンスセキュリティ機能（Security Center / 旧 Instance Security Center、Hardening settings、High Security Settings、security_admin）、暗号化機能（Field Encryption / 旧 Column Level Encryption、Key Management Framework、EKMS、Cloud Encryption、Edge Encryption、Database Encryption、Password2）、データプライバシー（Data Discovery・Data Classification・Data Anonymization）、ServiceNow Vault、監査ログ（sys_audit、Log Export Service）の仕様を、テーブル名・ロール・プロパティ・プラグイン ID・制約まで含めて整理する。
- [Service Portal と Employee Center（サービスポータルと従業員センター）](02_リファレンス/platform/portals-employee-center.md) — ServiceNow のセルフサービスポータル基盤 Service Portal（Portal／Page／Container／Widget／Theme の構造、Widget 開発、API、プロパティ、アクセス制御）と、その上に構築された Employee Center／Employee Center Pro、Unified Taxonomy（統合タクソノミー）、Advanced Portal Navigation／Mega menu、Content Publishing／Content Experiences、CSM 系ポータル（Customer Service Portal／Business Portal／Consumer Portal）の仕様リファレンス。Australia を基準に Brazil での変更点、後継の EmployeeWorks（Employee Slate）の位置付けも記載する。
- [Predictive Intelligence と AI Search（予測インテリジェンスと AI 検索）](02_リファレンス/platform/predictive-intelligence-ai-search.md) — ServiceNow の機械学習機能 Predictive Intelligence（Classification / Similarity / Clustering / Regression）のソリューション定義・学習要件・ロール・プロパティ・API、製品組込み手段（Task Intelligence、非推奨の PIWB）と、検索エンジン AI Search（Indexed source / Search source / Search profile / Search application、Genius Results）の構成要素、および旧来の Zing テキスト検索との違いを整理する。
- [プロセス自動化（RPA・Process Mining・Document Intelligence）](02_リファレンス/platform/process-automation-rpa-mining.md) — ServiceNow のプロセス自動化・業務分析系製品群（RPA Hub と Attended/Unattended Robot、Process Mining、Task Mining、Document Intelligence と Now Assist in Document Intelligence、Automation Center）について、構成要素・テーブル・ロール・プロパティ・状態値・メニュー位置・制約・リリース差分（Australia 基準、Brazil 併記）をまとめたリファレンス。
- [レポートとアナリティクス（Reporting / Platform Analytics / Performance Analytics）](02_リファレンス/platform/reporting-analytics.md) — ServiceNow の分析機能（Core UI の Reports・Dashboards、Next Experience の Platform Analytics（Data visualizations・Dashboards・Library・KPI Details）、Performance Analytics（Indicators・Breakdowns・Indicator sources・Data collection・Data snapshots）、Migration Center、PA ライセンス）の仕様を、テーブル・ロール・プロパティ・メニュー・制約の単位でまとめたリファレンス。Australia 時点の Core UI 非推奨化の状況と Brazil での変更点も記載。
- [クライアントサイドスクリプト（Client-side Scripting）](02_リファレンス/platform/scripting-client-side.md) — ServiceNow のブラウザ側で動くスクリプト機構（Client Scripts の onLoad/onChange/onSubmit/onCellEdit、g_form/g_user/g_list、GlideAjax、UI Policies、UI Actions、UI Scripts、UI Pages、Jelly、GlideModal）の仕様・フィールド・API・実行順序・制約・ベストプラクティスをまとめたリファレンス。
- [サーバーサイドスクリプト（Server-side Scripting）](02_リファレンス/platform/scripting-server-side.md) — ServiceNow のサーバーサイドスクリプト実行ポイント（Business Rules、Script Includes、Scheduled Jobs、Fix Scripts、Background Scripts）と主要 API（GlideRecord、GlideAggregate、GlideSystem、GlideElement、GlideDateTime、GlideQuery）、スコープ API の差異、JavaScript モード、ベストプラクティスを網羅的にまとめる。
- [Service Catalog（サービスカタログ）](02_リファレンス/platform/service-catalog.md) — ServiceNow Service Catalog の仕様リファレンス。Catalog／Category／Catalog item、Record producer、Order guide、Variables／Variable sets（MRVS を含む）、Catalog client script／Catalog UI policy、User criteria によるアクセス制御、カート・チェックアウト、sc_request／sc_req_item／sc_task の構造と状態、Flow による Fulfillment（step-based fulfillment を含む）、Catalog Builder、API、主要システムプロパティ、Australia／Brazil の変更点を網羅する。
- [SLAとスケジュール（Service Level Management / Schedules）](02_リファレンス/platform/sla-schedules.md) — ServiceNow の SLA Definition（SLA定義）、Start/Pause/Stop/Reset/Cancel 条件、Retroactive start、Task SLA、SLA エンジン（2011）、SLA timeline、SLA repair、OLA/UC、Schedules（cmn_schedule）と Timezone の仕様を、テーブル名・フィールド・ロール・プロパティ単位でまとめたリファレンス。
- [Survey・Assessment（Survey Designer / Assessment Designer / 顧客満足度調査）](02_リファレンス/platform/surveys-assessments.md) — プラットフォーム共通のアンケート・評価エンジン「Assessments and Surveys」の仕様リファレンス。asmt_* テーブル群（Metric Type／Instance／Metric Result ほか）、Survey Designer と Assessment（Metric Type）構成、Trigger Condition、メール・ポータル・モバイル・Outlook での配信、匿名／Public Survey、One Click／Kiosk Survey、スコアリング計算式とレポート、ロール・プロパティ・API、Smart Assessment Engine（IRM／TPRM）や Enterprise Architecture スコアリングでの再利用、CSAT／NPS 設計の要点をまとめる。
- [System Administration（システム管理）](02_リファレンス/platform/system-administration.md) — ServiceNow インスタンスのシステム管理機能（System Properties、プラグイン管理、System Log／Node Log File Browser、Scheduled Jobs、Table Rotation／Archive／Table Cleaner、Data Management Console とデータ保持、Instance Observer、Slow Queries／Index Suggestion Engine／インデックス作成、Transaction Quota）について、テーブル名・プロパティ・ロール・メニュー位置・制約を Australia リリース基準で網羅的に説明する。
- [Update Sets and System Clone（アップデートセットとクローン）](02_リファレンス/platform/update-sets-cloning.md) — ServiceNow のインスタンス間で設定変更を移送する Update Set（記録対象/対象外、Retrieve・Preview・Commit、Batch、Merge、Collision、Back out）と、インスタンス全体を複製する System Clone（Clone Admin Console、Exclusion・Preserver・Cleanup script、Clone options、Rollback）の仕様と移送のベストプラクティスをまとめる。
- [ユーザー・グループ・ロール（Users, Groups, and Roles）](02_リファレンス/platform/users-groups-roles.md) — ServiceNow のユーザー（sys_user）・グループ（sys_user_group）・ロール（sys_user_role）のテーブル構造、ロール継承、昇格ロール（security_admin）、ロール委任と承認・作業の Delegation、ドメインセパレーションとの関係、LDAP 連携、主要ロール一覧（admin、itil、catalog_admin、Australia のグラニュラー管理ロール等）を網羅的に解説する。
- [Virtual Agent と会話型AI（Conversational Interfaces）](02_リファレンス/platform/virtual-agent.md) — ServiceNow の会話型インターフェース（Virtual Agent、Assistant Designer / Virtual Agent Designer、Topic、NLU と LLM による Topic discovery、ServiceNow Otto for Virtual Agent（旧 Now Assist in Virtual Agent）、Microsoft Teams / Slack 連携、Live Agent への引き継ぎ、Agent Chat）の仕様を、プラグイン・テーブル・ロール・プロパティ・メニュー位置まで含めて整理する。
- [Web Services / REST API（Webサービスと REST API）](02_リファレンス/platform/web-services-api.md) — ServiceNow AI Platform のインバウンド REST API（Table / Aggregate / Attachment / Import Set / Batch / Scripted REST）、アウトバウンド REST Message（RESTMessageV2）、SOAP、GraphQL、REST API Explorer、レート制限、認証方式（Basic / OAuth 2.0 / API Key・HMAC / mTLS）とアクセスポリシーの仕様をまとめたリファレンス。
- [Workflow Data Fabric（ワークフローデータファブリック）](02_リファレンス/platform/workflow-data-fabric.md) — ServiceNow の Workflow Data Fabric（WDF）の構成要素（WDF Home、Connect Hub、Zero Copy Connectors、データファブリックテーブル、Data Products / Data Interfaces、Data Catalog、Knowledge Graph、RaptorDB）と、Integration Hub との使い分け、ロール、プラグイン ID、制約、ライセンス（WDF Credits）を Australia 基準で整理する。
- [Workspace と UI Builder（Configurable Workspace / Service Operations Workspace / UI Builder）](02_リファレンス/platform/workspaces-ui-builder.md) — Configurable Workspace（構成可能なワークスペース）と Service Operations Workspace、ServiceNow が提供するワークスペース一覧、UI Builder の構成要素（Experience・Page・Variant・Component・Data resource・Client state・Event・UI interaction）、関連テーブル・ロール・プロパティ、および旧 Agent Workspace の廃止と移行を Australia リリース基準で解説する。

#### itsm — IT Service Management

- [Change Management（変更管理）](02_リファレンス/itsm/change-management.md) — ServiceNow Change Management の `change_request` / `change_task` テーブル、Normal・Standard・Emergency の変更タイプと Change Model（変更モデル）、State（状態）値と遷移、Change Approval Policies（変更承認ポリシー）、CAB Workbench、Conflict detection（競合検出）とブラックアウト/メンテナンス スケジュール、Risk assessment・Risk conditions・Risk Intelligence・Calculated Risk Score、Change Success Score、DevOps Change Velocity、ロール・プラグイン・プロパティ・REST API を Australia リリース基準でまとめたリファレンス。
- [Incident Management（インシデント管理）](02_リファレンス/itsm/incident-management.md) — ServiceNow Incident Management の `incident` テーブル主要フィールド、State（状態）遷移、Impact/Urgency/Priority マトリクス、Assignment（割り当て）、Resolution（解決）とクローズ、Major Incident Management（重大インシデント管理）、On-Call Scheduling（オンコール スケジューリング）、関連ロール・プロパティ・プラグインを Australia リリース基準で網羅したリファレンス。
- [ITSM 概要とパッケージ（IT Service Management Overview and Packaging）](02_リファレンス/itsm/itsm-overview.md) — ServiceNow IT Service Management (ITSM) の全体像、旧パッケージ（Standard / Professional / Pro Plus / Enterprise / Enterprise Plus）と 2026-04 以降の新パッケージ（Foundation / Advanced / Prime）の機能差、ITSM のアプリケーション（モジュール）一覧、Service Operations Workspace (SOW) の構成・ロール・設定、Simplified ITSM、主要テーブルに答える。
- [ITSM Pro/Enterprise 固有機能（Predictive Intelligence・Performance Analytics・Virtual Agent・Process Mining・CIM・Now Assist・DPM）](02_リファレンス/itsm/itsm-pro-features.md) — ITSM の上位パッケージ（旧 ITSM Pro / Enterprise、2026-04 以降の Advanced / Prime）で提供される Predictive Intelligence for ITSM、Task Intelligence、Performance Analytics for ITSM、ITSM Virtual Agent、Process Optimization（Process Mining）、Continual Improvement Management、Now Assist（ServiceNow Otto）for ITSM、Digital Portfolio Management の仕様（プラグイン、テーブル、ロール、プロパティ、メニュー、制約）を一か所にまとめる。
- [Problem Management（問題管理）](02_リファレンス/itsm/problem-management.md) — ServiceNow Problem Management の `problem` / `problem_task` テーブル、State（状態）遷移（New / Assess / Root Cause Analysis / Fix in Progress / Resolved / Closed）と UI アクション、Resolution code、Known Error（既知のエラー）と Known Error 記事、Workaround（回避策）の連絡、Problem task（問題タスク）のライフサイクル、ロール・プロパティ・プラグイン、Problem Management models、Service Operations Workspace での操作を Australia リリース基準でまとめたリファレンス。
- [Release Management と DevOps（リリース管理と DevOps）](02_リファレンス/itsm/release-management.md) — ServiceNow のリリース管理系アプリケーション（Release Management v2 の `rm_release` 系テーブル、後継の Digital Product Release（DPR）の `sn_dpr_model_*` 系テーブル）、Agile Development 2.0 の `rm_release_scrum` との関係と CWM への移行、DevOps Change Velocity（`sn_devops`）による変更要求の自動作成・自動承認・パイプライン連携、CI/CD 連携（Jenkins／GitHub Actions／Azure DevOps／GitLab、DevOps API、CICD API `sn_cicd`）について、テーブル・ロール・プロパティ・状態値・メニュー・制約を Australia リリース基準でまとめたリファレンス。
- [Request Management（リクエスト管理）](02_リファレンス/itsm/request-management.md) — ServiceNow Request Management（リクエスト管理）について、Request（`sc_request`）・Requested Item（`sc_req_item`）・Catalog Task（`sc_task`）の3層データモデルと生成順序、承認（Approval）、Fulfillment（フルフィルメント：Workflow Studio フロー／レガシーワークフロー／Execution Plan／Service Fulfillment Steps）、Stage（ステージ）と State（状態）、Request と Incident の使い分けと相互連携、Universal Request 連携、ロール・プロパティ・ドメインセパレーション、Walk-up Experience（ウォークアップ対応）を Australia リリース基準で網羅したリファレンス。
- [ITSMにおけるサービスレベル管理とサービスポートフォリオ（Service Portfolio Management / Service Offering / SLA Commitments）](02_リファレンス/itsm/service-level-management-itsm.md) — ServiceNow ITSM におけるサービスの定義と管理（Service Portfolio Management、Business Service、Technology Management Service、Service Offering、Service Commitment、Subscription、Availability、SLA Results）、Service Builder、Digital Portfolio Management（DPM）、非推奨化された Service Owner Workspace、CSDM のデジタルプロダクトとの関係を、プラグイン・ロール・テーブル・フィールド・メニュー単位でまとめたリファレンス。
- [Vendor Manager Workspace / Service Owner Workspace とマルチソーシング（SIAM）](02_リファレンス/itsm/vendor-manager-service-owner-siam.md) — ITSM Pro に含まれてきた Vendor Management Workspace（旧 Vendor Manager Workspace、sn_itsm_vendor）のベンダー管理・ベンダースコア・KPI グループ・契約/SLA 連携・サービスクレジットの仕様、ロール、テーブル、プロパティ、Australia での非推奨化と GRC: Vendor Management Workspace（sn_vrm_ws）との違い、Service Owner Workspace の機能と非推奨化（後継 DPM）、そして ServiceNow で複数ベンダー運用（SIAM）を設計する際の論点（ベンダー別割当グループ、Underpinning contract、eBonding / Remote Instance spoke、ドメイン分離との使い分け）を整理する。
- [Workforce Optimization（WFO）for ITSM / CSM](02_リファレンス/itsm/workforce-optimization.md) — ServiceNow Workforce Optimization（WFO）for ITSM / for Customer Service の構成（Manager Workspace、Channel Management、Scheduling、Demand Forecast、Teams、Coaching、Work Scheduler、Skills）、プラグイン、ロール、テーブル、システムプロパティ、スケジュールジョブ、AWA / On-Call との関係、含まれるエディション、品質管理・ゲーミフィケーションの扱い、Brazil での非推奨準備を整理する。

#### itom — IT Operations Management

- [Agent Client Collector（ACC）](02_リファレンス/itom/agent-client-collector.md) — ServiceNow のエージェント型収集基盤 Agent Client Collector（ACC）の仕様リファレンス。ACC-F / ACC-V（ACC-VC）/ ACC-M / ACC-L の違い、MID Server の ACC Listener（MID Web Server・Websocket Endpoint）を中心としたアーキテクチャ、MID-less 構成、Windows MSI・Linux・macOS のインストールと配布、acc.yml、チェック定義・ポリシー・プラグイン、エージェント経由の Discovery / Visibility、Health Log Analytics・Metric Intelligence 連携、SU 消費、テーブル・ロール・プロパティ・REST API、トラブルシューティングを整理する。
- [Certificate Inventory and Management と Firewall Audits and Reporting（証明書インベントリ管理・ファイアウォール監査）](02_リファレンス/itom/certificate-inventory-firewall-audits.md) — ITOM Visibility に含まれる2つの Store アプリ、Certificate Inventory and Management（TLS 証明書の検出・インベントリ・期限通知・申請／更新／失効の自動化・ACME・Kubernetes cert-manager 連携・更新 AI エージェント）と Firewall Audits and Reporting（Palo Alto Panorama / Fortinet FortiManager のポリシー検出・監査・ルール申請・生成 AI によるルール申請）の仕様を、プラグイン、テーブル、ロール、プロパティ、メニュー、ワークスペース、バージョン履歴、ライセンス上の位置付けのレベルで整理する。
- [Cloud Management（クラウド管理：Cloud Provisioning and Governance / Cloud Services Catalog / Cloud Account Management / Cloud Cost Management）](02_リファレンス/itom/cloud-management.md) — ServiceNow のクラウド管理製品群の仕様リファレンス。ITOM Cloud Accelerate 配下の Cloud Provisioning and Governance（CPG、旧 Cloud Management）と後継の Cloud Services Catalog（CSC）について、Cloud Admin Portal / Cloud User Portal、カタログアイテム（Cloud template・Terraform・Blueprint）、Cloud account / Service account / Logical datacenter、Governance（Quotas・Policies・Pools・Permissions・Tags・Lease）、ロールとテーブルを整理する。あわせて Cloud Account Management（CAM）と、ITAM 製品群に属する Cloud Cost Management（CCM、旧 Cloud Insights）の機能・ロール・テーブル・プロパティ・ライセンス単位、Brazil での非推奨化・変更点をまとめる。
- [Digital End-user Experience（DEX）](02_リファレンス/itom/digital-end-user-experience.md) — ServiceNow の端末パフォーマンス・従業員体験可視化製品 Digital End-user Experience（DEX）の仕様リファレンス。目的と構成要素、Agent Client Collector（ACC-VC、MID-less）によるデータ収集アーキテクチャ、Digital Experience Score（DEX Score）の算出方法、Service Operations Workspace 上の DEX 画面と DEX Administration、Metric rules と Proactive Engagement によるプロアクティブ解決・セルフヒーリング、Incident の Investigation タブと AI エージェント、Employee Center / Desktop Assistant / DEX Self-service、Microsoft 365・Zoom・Jamf・Intune・Tanium 等の外部連携、パッケージと SU ライセンス、ロール・テーブル・プロパティを整理する。
- [Discovery（ディスカバリー）](02_リファレンス/itom/discovery.md) — ServiceNow Discovery の仕様リファレンス。Horizontal discovery の4フェーズ（Scanning / Classification / Identification / Exploration）、Probes・Sensors・Patterns、Discovery schedule（フォーム項目・MID Server 選択・IP 範囲）、Credentials（種類・順序・Credential affinity・Credential alias・外部保管）、Cloud discovery（AWS / Azure / GCP ほか、Service Graph Connectors との使い分け）、Agent Client Collector（ACC）、Discovery Admin Workspace と監視、トラブルシューティング（Error Framework の refined code、エラーメッセージ）、主要プロパティを、テーブル名・ロール・プロパティ・メニュー位置のレベルで整理する。
- [Event Management と AIOps（イベント管理と AIOps）](02_リファレンス/itom/event-management-aiops.md) — ServiceNow ITOM AIOps の中核である Event Management（em_event / em_alert、Event rules、Alert management rules、Alert grouping、Alert priority、Impact calculation）と、Health Log Analytics・Metric Intelligence・Service Operations Workspace（旧 Operator Workspace）・Connectors の仕様を、テーブル・ロール・プロパティ・ジョブ単位で整理したリファレンス。
- [ITOM 概要とパッケージ（IT Operations Management）](02_リファレンス/itom/itom-overview.md) — ITOM の製品構成と、旧（Standard/Pro/Enterprise）・新（Advanced/Prime）パッケージ、Subscription Unit（SU）による課金の仕様（CI カテゴリ・比率・90日平均・バンドル/アラカルト）を説明する。ITOM/OT SU Licensing アプリのメニュー・テーブル・ロール・ジョブにも答える。
- [Operational Technology（OT）Management（OT Discovery / OT Service Management / OT Vulnerability Response）](02_リファレンス/itom/operational-technology-management.md) — ServiceNow Operational Technology Management（OTM）の製品構成（OT Manager、Industrial Process Manager、OT Discovery、OT Incident/Change/Knowledge/Request Management、OT Vulnerability Response、Industrial Workspace）、OT 用 CMDB クラス（cmdb_ci_ot、cmdb_ot_entity、ISA-95 Equipment Model）と Purdue モデル、Claroty・Nozomi・Armis・Microsoft Defender for IoT 等の OT 向け Service Graph Connector、OTM の SU ライセンス、ロール・テーブル・プロパティ、ITOM / SecOps との関係、製造業での導入時の留意点をまとめたリファレンス。
- [Service Graph Connectors（サービスグラフコネクタ）](02_リファレンス/itom/service-graph-connectors.md) — Service Graph Connectors（SGC）の仕組み（IntegrationHub ETL・RTE・IRE によるデータパイプライン）、SGC Central による導入・監視、ロール・テーブル・ジョブ、主要コネクタ（SCCM / Intune / Jamf / AWS / Azure 等）の仕様、IRE との関係、ライセンス上の扱いと Brazil での変更点をまとめたリファレンス。
- [Service Mapping（サービスマッピング）](02_リファレンス/itom/service-mapping.md) — ServiceNow Service Mapping の仕様リファレンス。Top-down（パターンベース）、Tag-based、機械学習（Automated Service Suggestions）、Traffic-based の各マッピング方式、Application service（Service instance）の種類とテーブル、Entry points、Patterns、ロール、プロパティ、Service Mapping Plus / AI Agents、Brazil での変更点を網羅する。

#### itam — IT Asset Management / Enterprise Asset Management

- [Enterprise Asset Management（EAM、エンタープライズ資産管理）](02_リファレンス/itam/enterprise-asset-management.md) — ServiceNow Enterprise Asset Management（EAM、com.sn_eam）で IT 以外の物理資産（設備・機器・車両・医療機器・施設設備等）を管理するための仕様を網羅する。データモデル（sn_ent_model / sn_ent_asset と Model category）、調達から廃棄までのライフサイクル、保守計画（Maintenance plan）と Field Service Management の計画保守との連携、在庫・Stockroom、リース・契約、Enterprise Asset Workspace、ロール、HAM との違い、ライセンス（Subscription unit ratio）、業界別アプリ（Healthcare・Facilities・OT・DCNAM・Providers）と適用例を扱う。
- [Hardware Asset Management（ハードウェア資産管理）](02_リファレンス/itam/hardware-asset-management.md) — ServiceNow Hardware Asset Management（HAM, sn_hamp）の機能、Hardware Asset Workspace の各ビュー、資産の状態/サブ状態、在庫・Stockroom・Stock rule・Transfer order、Refresh / Zero Touch Refresh、Reclamation、Disposal（廃棄・転売）、Procurement（購買・受入）および Sourcing and Procurement Operations 連携、ライセンス（Resource category）、ロール・テーブル・プロパティを網羅的に整理する。
- [ITAM 概要（IT Asset Management Overview）](02_リファレンス/itam/itam-overview.md) — ServiceNow IT Asset Management (ITAM) の製品構成、Asset（資産）と CI（構成アイテム）の関係と同期の仕組み、alm_asset / alm_hardware 等の資産テーブル、Product Model（製品モデル）と Model category（モデルカテゴリ）、資産の State/Substate と CSDM ライフサイクル、Contract Management（契約管理）のテーブル・状態・ロールに答える。
- [Software Asset Management（ソフトウェア資産管理）](02_リファレンス/itam/software-asset-management.md) — ServiceNow Software Asset Management（SAM Foundation / SAM Professional / SAM Enterprise）の構成プラグイン、ロール、主要テーブル、Software model（ソフトウェアモデル）と Software entitlement（ソフトウェアエンタイトルメント）のフィールド、License metric（ライセンスメトリック）、正規化、Reconciliation（調整）と結果、Reclamation（回収）、Publisher pack（パブリッシャーパック）、SaaS License Management、Cloud Cost Management、Australia/Brazil での変更点に答える。

#### spm — Strategic Portfolio Management・ITFM・アジャイル・テスト管理

- [Agile Development・APM・EAM（アジャイル開発・アプリケーションポートフォリオ管理・エンタープライズアーキテクチャ）](02_リファレンス/spm/agile-apm-eam.md) — ServiceNow のアジャイル開発系アプリ（Agile Development 2.0 / Scrum Programs / SAFe / Enterprise Agile Planning / Collaborative Work Management）、Enterprise Architecture（旧 Application Portfolio Management、EA Workspace）、Digital Product Release / Digital Portfolio Management の仕様（テーブル、ロール、プラグイン、プロパティ、状態値、画面、廃止予定）を Australia 基準でまとめたリファレンス。
- [IT Financial Management（ITFM/TBM）とコスト配賦・ショーバック](02_リファレンス/spm/it-financial-management-cost-allocation.md) — ServiceNow における IT コストの透明化（TBM 型コストモデル）、コストプール（Bucket）・配賦ルール（Rollup / Allocation metric / Expense allocation rule）、サービス・アプリ単位のコスト算出、ショーバック/チャージバック（Financial Charging）、CMDB・SAM・Cloud Cost Management・Enterprise Architecture（Application TCO）とのデータ連携、各テーブル・ロール・プラグインと、Australia 時点での提供形態（Financial Modeling は 2021-03 以降新規有効化不可、ドキュメントは Xanadu 版が最終、Cost Management / Expense Line / CCM は Australia で現行）を網羅したリファレンス。SPM の Financial Planning（プロジェクト財務）は対象外。
- [Strategic Portfolio Management（PPM）](02_リファレンス/spm/strategic-portfolio-management.md) — ServiceNow Strategic Portfolio Management（SPM、旧 ITBM）のうち PPM 系機能（Demand、Project、Program、Portfolio、Resource Management、Investment Funding、Financial Planning、Goal Framework、Strategic/Portfolio Planning Workspace）について、テーブル、ロール、状態値、フィールド、プラグイン/アプリケーション ID、プロパティ、ワークスペース、Australia での新機能と非推奨、Brazil での変更点を網羅したリファレンス。
- [Test Management 2.0（テスト管理 2.0）](02_リファレンス/spm/test-management.md) — ServiceNow の手動テスト管理アプリ Test Management 2.0（および旧 Test Management 1.0）について、テスト・テストバージョン・テストセット・テスト計画・テストサイクル・テスト実行スイート・テスト実行（Run/Result）のデータモデルとテーブル名、ロール、プラグイン、状態値、メニュー、Test Board、Agile Development 2.0／SAFe／PPM との連携、欠陥（Defect）の扱い、ダッシュボード、ATF との使い分け、1.0 から 2.0 への移行、廃止・Brazil の状況を Australia 基準でまとめたリファレンス。

#### secops — Security Operations

- [Security Operations (SecOps)（セキュリティ運用）](02_リファレンス/secops/security-operations.md) — ServiceNow Security Operations（SecOps）を構成する Security Incident Response、Vulnerability Response / Unified Security Exposure Management、Configuration Compliance、Threat Intelligence / TISC、Security Posture Control、プレイブック（SOAR 的機能）、Now Assist（ServiceNow Otto）for SecOps、主要連携について、テーブル・ロール・状態値・プロパティ・ストア配布の仕様を Australia 基準でまとめる。

#### irm — Integrated Risk Management（GRC）

- [Integrated Risk Management（GRC：統合リスク管理）](02_リファレンス/irm/integrated-risk-management.md) — ServiceNow Integrated Risk Management（IRM／GRC）を構成する Policy and Compliance、Risk Management（Advanced Risk）、Audit Management、Third-party Risk Management、Business Continuity Management、Operational Resilience、Privacy Management、Regulatory Change Management、ESG（Operational Sustainability Management）の仕様を、テーブル・ロール・状態遷移・プロパティ・ワークスペース・ライセンス階層の観点で Australia 基準にまとめ、Brazil での変更点を併記する。

#### employee — HR・人材・ワークプレイス・リーガル（Employee Workflows）

- [HR Service Delivery（HRサービスデリバリー）](02_リファレンス/employee/hr-service-delivery.md) — ServiceNow HR Service Delivery（HRSD）の構成要素である HR Case / HR Profile、COE（Center of Excellence）、HR Service、Lifecycle Events（オンボーディング/オフボーディング）、Employee Journey Management（Journey designer / Journey Accelerator）、Employee Document Management、Agent Workspace for HR Case Management、HR データ保護のセキュリティモデル（スコープロール、COE Security Policy、Client roles）を Australia リリース基準で網羅したリファレンス。
- [Talent Development・Employee Growth・Hiring Experiences（人材育成と採用体験）](02_リファレンス/employee/talent-development-hiring.md) — HR Service Delivery 周辺の人材系アプリ群、すなわち Growth Experiences（旧 Talent Development / Employee Growth and Development。Talent Development Core、Career hub、Aspirations、Growth plans、Career Conversations、Learning / Learning Core、Mentoring、Employee Goals、Talent Feedback、Opportunity Marketplace、Leader Hub）、Skills Foundation（旧 Skills Intelligence）のスキル/ジョブアーキテクチャのデータモデル、Hiring Experiences（Hiring tab、Recruitment workspace、Interview management、Applicant Center、Talent Profile、Hiring Core、Hiring Connector）の構成・テーブル・ロール・状態値・プロパティ・AI エージェント・パッケージを Australia リリース基準でまとめたリファレンス。
- [Workplace Service Delivery・Legal Service Delivery 等（ワークプレイス／リーガル／ESM 全般）](02_リファレンス/employee/workplace-legal-other.md) — ServiceNow の Workplace Service Delivery（WSD：予約・スペース管理・来訪者・ワークプレイスケース・移転）と Legal Service Delivery（LSD：法務リクエスト・法務案件・Contract Management Pro）のアプリ構成、テーブル、ロール、プロパティ、設定項目、状態値と、Enterprise Service Management（ESM）全体での位置付けをまとめたリファレンス。

#### customer — CSM・FSM・Sales CRM・インスタンス間連携（Customer Workflows）

- [CSM 顧客接点：Customer Service Portal・Engagement Messenger・Partner（B2B2C）](02_リファレンス/customer/csm-portal-engagement-messenger-partner.md) — ServiceNow CSM の外部顧客チャネル（Business Portal / Customer Service Portal / Consumer Portal / Consumer Service Portal）、Web サイト埋め込み型ウィジェット Engagement Messenger（モジュール構成・埋め込みコード・OIDC/SAML 認証・CORS・テーブル・ロール・プロパティ）、パートナーモデル（Partner Account、Account Relationship、Contact Relationship、B2B2C、Partner Relationship Management）、外部ユーザーのロールとライセンス、Contact 制限と Account Hierarchy によるデータアクセス制御を Australia 基準でまとめ、Brazil の変更点を併記する。
- [Customer Service Management（顧客サービス管理、CSM）](02_リファレンス/customer/customer-service-management.md) — ServiceNow Customer Service Management（CSM）の仕様リファレンス。顧客データモデル（Account/Contact/Consumer/Household）、Case（テーブル・フィールド・状態・メジャーケース・エスカレーション）、Entitlement、Omnichannel（AWA・Email・Voice/CCaaS・Messaging）、CSM Configurable Workspace（CRM Workspace）、顧客向けポータル、Proactive Customer Service Operations のテーブル名・ロール・プラグイン・プロパティを Australia 基準でまとめ、Brazil の変更点を併記する。
- [Field Service Management（フィールドサービス管理）](02_リファレンス/customer/field-service-management.md) — ServiceNow Field Service Management (FSM) の仕様リファレンス。Work order / Work order task のテーブル・状態・フィールド、ロール、Dispatch（Dispatcher Workspace）、Scheduling（Dynamic Scheduling・Schedule Optimization 等）、Mobile（ServiceNow Agent アプリ・オフライン）、Parts management（部品要求・転送オーダー・Advanced Parts Sourcing）、Planned maintenance（Planned Work Management）を Australia 基準で整理し、Brazil での変更点を併記する。
- [Sales and Order Management（CRM）／Sales Customer Relationship Management（Sales CRM）](02_リファレンス/customer/sales-order-management-crm.md) — ServiceNow の販売・受注領域（旧称 Sales and Order Management、Australia で Sales Customer Relationship Management に改称）について、構成アプリケーション、Lead/Opportunity/Quote/Order のテーブル・ロール・状態値、CPQ（旧 Logik.ai）、Pricing/Product Catalog、AI 機能、API、ServiceNow の CRM 戦略をまとめたリファレンス。
- [Service Bridge と eBonding（インスタンス間連携）](02_リファレンス/customer/service-bridge-ebonding.md) — ServiceNow インスタンス同士（プロバイダーと顧客、MSP とテナント、委託元と委託先）でケース・インシデント・リクエストを連携させる仕組みの仕様リファレンス。Australia で Service Exchange に改称された Service Bridge の Provider/Consumer アーキテクチャ、Remote Catalog（Remote Record Producer）、Provider Task、Remote Task・Remote Task Definition、Transform、Journal Field Framework、Foundation Data Sync、接続登録と OAuth 認証、テーブル・ロール・プロパティ、クローン・ドメインセパレーション・障害対応を説明する。あわせて、eBonding spoke、Remote Instance spoke、Remote Process Sync の位置付けとライセンスを比較する。

#### industry — 業界向けソリューション

- [業界向けソリューション（Industry Solutions）](02_リファレンス/industry/industry-solutions.md) — ServiceNow の業界向けソリューションを製品ごとにまとめる。対象は Telecommunications/Technology Provider（TMT）、Financial Services Operations（銀行・保険）、Healthcare and Life Sciences、Public Sector Digital Services、Manufacturing Commercial Operations、Retail。各製品のアプリ構成、主要テーブル、ロール、プラグイン、標準 API、Australia での新機能と Brazil での変更点を扱う。

#### other — Finance and Supply Chain・ESG ほか

- [Finance・Supply Chain・その他ワークフロー（Source-to-Pay / AP / Supplier / Procurement / Operational Sustainability (ESG) / Impact）](02_リファレンス/other/finance-supply-chain-esg.md) — ServiceNow の Finance and Supply Chain（FSC）領域（Source-to-Pay Operations：Sourcing and Procurement Operations、Supplier Lifecycle Operations、Accounts Payable Operations、Purchase Order Management）と、Operational Sustainability Management（旧 ESG Management）、ServiceNow Impact 等の周辺製品について、構成アプリ・プラグイン・テーブル・ロール・状態値・プロパティ・Australia/Brazil の新機能をまとめたリファレンス。

### 03_導入編（19 ファイル）

- [ライセンスモデル（Licensing Model）](03_導入編/01-licensing-model.md) — ServiceNow のサブスクリプション型ライセンスの仕組みを整理する。ユーザー課金（Fulfiller / Business Stakeholder / Requester / Unrestricted）、容量課金（ITOM/ITAM の Subscription Unit）、消費型課金（Integration Hub トランザクション、Now Assist の Assist、Workflow Data Fabric トークン）、インスタンス数、契約期間、True-up、Subscription Management と Usage Analytics によるライセンス監視をまとめる。
- [価格情報（Pricing：推定価格・価格交渉・TCO）](03_導入編/02-pricing.md) — ServiceNow の価格は公式に非公開である前提で、公開情報から集めた製品・パッケージ別の推定単価（ユーザー単価、Subscription Unit 単価等）、2026年4月の Foundation/Advanced/Prime 移行が価格に与える影響、価格交渉の事例と論点、総所有コスト（TCO）の内訳と試算方法を、すべて【推定】・出典・取得日付きでまとめる。
- [エディション比較（Edition Comparison：Standard / Pro / Pro Plus / Enterprise と Foundation / Advanced / Prime）](03_導入編/03-edition-comparison.md) — ServiceNow 主要製品（ITSM, ITOM, ITAM, HRSD, CSM, SecOps, IRM, SPM, App Engine）のエディションごとの機能差を比較する。2026-04 に旧体系（Standard / Pro / Pro Plus / Enterprise / Enterprise Plus）が新体系（Foundation / Advanced / Prime）へ切り替わったため、両方の体系と対応関係、選定時の実務上の注意点をまとめる。
- [導入方法論（Implementation Methodology / Now Create・Best Practices）](03_導入編/04-implementation-methodology.md) — ServiceNow 公式の導入方法論 Now Create（2025-12 以降は My Now の Best Practices サイトに統合）のフェーズ構成・7 ワークストリーム・Exit Gate・Success Pack、アジャイル（スプリント）との組み合わせ方、Fit to Standard（標準適合）の進め方、Quick start 型の短期導入手段（Simplified ITSM、Otto for Setup、Impact Accelerator、パートナーのパッケージ）、および期間・工数の目安をまとめる。
- [プロジェクト体制とパートナー（Project Organization & Partners）](03_導入編/05-project-organization.md) — ServiceNow 導入・運用における顧客側体制（Executive Sponsor、Platform Owner、Process Owner、Product Owner、Platform Architect 等）の役割定義、導入モデル（自社/Expert Services/パートナー/協業）の選び方、ServiceNow Partner Program の区分（Registered〜Elite / Global Elite、ルート別ティア、PLA・Validated Practice）、ServiceNow Expert Services、成功支援プログラム Impact（Guided / Total / Integrated Success、Accelerator、Impact ロール）、日本の主要パートナーをまとめる。
- [要件定義と設計（Requirements & Design）](03_導入編/06-requirements-design.md) — ServiceNow 導入の要件定義・設計フェーズで、OOTB（標準機能）優先の判断基準、Fit-Gap 分析の進め方と一覧表の列定義、プロセス設計（状態・割り当て・自動化手段の選定）、データ設計（テーブル拡張・命名・カスタムテーブルのライセンス・選択肢）、ロール設計（グループ付与・ロール包含・ライセンスへの影響・Australia の細粒度管理ロール）、通知設計（通知マトリクス・Weight・カテゴリ）、設計書テンプレートの観点と設計品質ゲート（Instance Scan）を、実務でそのまま使える粒度でまとめる。
- [インスタンス戦略と環境（Instance Strategy and Environments）](03_導入編/07-instance-strategy.md) — ServiceNow 導入時の環境設計（本番 Production とサブプロダクション Dev/Test/Staging の構成パターン）、非本番インスタンスの追加購入・改名・廃止の手続き、Instance Clone によるリフレッシュ戦略（頻度・方向・Clone chaining・Exclude/Preserve・データマスキング）、移送パイプライン（Update Set／App Engine Management Center／ReleaseOps／Developer Sandboxes）、Instance Data Replication（IDR）の使いどころと制約、複数本番インスタンスの是非と判断基準を、実務で使える粒度でまとめる。
- [データ移行（Data Migration）](03_導入編/08-data-migration.md) — ServiceNow 導入時のデータ移行について、移行対象（ユーザー、CMDB、チケット履歴、ナレッジ）の判断基準、移行手法（Import Set、IntegrationHub ETL、Import Set API / REST API）の使い分けと具体的な設定項目、データクレンジング、移行リハーサルとカットオーバーの進め方をまとめる。
- [連携設計（Integration Design）](03_導入編/09-integration-design.md) — ServiceNow 導入時の外部システム連携の設計方法をまとめる。対象は AD/Entra ID、SSO、メール、監視ツール、Jira、SAP、Teams/Slack の代表的な連携パターン、MID Server の要否の判断、IntegrationHub（Spoke）とスクリプト（RESTMessageV2 / Scripted REST）の使い分けで、方式・前提プラグイン・ロール・制約を具体的に示す。
- [セキュリティとコンプライアンス（Security and Compliance）](03_導入編/10-security-compliance.md) — ServiceNow 導入時のセキュリティ・コンプライアンス検討事項をまとめる。対象は、データセンターとデータレジデンシー（日本の Tokyo/Osaka ペア）、ISMAP 登録状況（AI Platform 2022年3月、Now Assist/AI Agents 2026年6月）、SOC 1/SOC 2、ISO 27001 系、FedRAMP/DoD IL、GDPR と DPA、責任共有モデル、Security Center によるインスタンスのハードニング（スコア計算、Accept Risk、主要プロパティ、MFA 強制、Explicit Roles、IP 制限）で、セキュリティ審査・調達・設計で使える具体的な確認ポイントを示す。
- [テストと本番稼働（Testing and Go-Live）](03_導入編/11-testing-golive.md) — ServiceNow 導入プロジェクトのテスト計画（単体・システム/結合・UAT・性能・回帰）、Automated Test Framework（ATF）の導入プロジェクトでの使い方、Test Management 2.0 による手動テスト管理、Instance Scan による品質ゲート、Go-Live 判定チェックリスト、カットオーバー（本番移送・データ投入・メール有効化）手順、Hypercare と運用移管を実務で使える粒度でまとめる。
- [運用とガバナンス（Operations and Governance）](03_導入編/12-operations-governance.md) — ServiceNow 本番稼働後のプラットフォーム運用体制（Platform Owner を中心とする Platform team、CoE）、3 つのガバナンスボード（Executive steering board・Demand board・Technical governance board）、Demand Management による改善要望の受付と優先順位付け、ReleaseOps / Pipelines and Deployments / Update Set によるリリース管理、Blackout schedule による変更凍結、Subscription Management によるライセンス管理運用、運用 KPI（Benchmark KPI・Change KPI・Platform Health）を、実務で使える粒度でまとめる。
- [アップグレード管理（Upgrade Management）](03_導入編/13-upgrade-management.md) — ServiceNow インスタンスのファミリーアップグレードとパッチ適用を実務で計画・実行するための手引き。年2回のアップグレードサイクルとパッチプログラム、公式7フェーズ／51ステップのアップグレード計画チェックリスト、Now Support でのスケジュール手順、Upgrade Center（Upgrade Preview・Upgrade Monitor・Upgrade History・Upgrade Plan・Skipped Record Rules）と Upgrade Console（Guided upgrade）の使い方、Skipped records（スキップされたレコード）の解消方法、Patch/Hotfix/ロールバック、ATF を使った回帰テストをまとめる。
- [サポートと監視（Support and Monitoring）](03_導入編/14-support-monitoring.md) — ServiceNow 社が提供するサポート（Now Support／旧 HI ポータル、ケース優先度 P1〜P4 と応答目標、Availability SLA）、成功支援プログラム（ServiceNow Impact の Guided／Total／Integrated Success、Impact Squad、Accelerator、アドオン）、インスタンスの健全性評価（Instance Scan、Impact の Scan Engine／HealthScan）、パフォーマンス監視（Instance Observer、Transaction log、Slow patterns、stats.do、Quota rules）、CSM の Customer Service Portal、ServiceNow Store（アプリ調達・Application Manager・認定）を、導入・運用の実務で使える粒度でまとめる。
- [日本市場における導入（ServiceNow in the Japanese Market）](03_導入編/15-japan-market.md) — 日本企業で ServiceNow を導入する際に固有に検討すべき事項をまとめる。ServiceNow Japan（日本法人）の動向と投資、日本データセンター（東京・大阪）とデータレジデンシー、ISMAP 登録、日本語化（I18N: Japanese Translations プラグイン）の範囲と品質上の注意、稟議・承認、帳票（PDF・日本語フォント）、和暦・日付書式・祝日カレンダー、Excel 文化への対応、日本企業の導入事例を、実務で使えるレベルで整理する。
- [競合比較（Competitor Comparison：Jira Service Management・BMC Helix・Ivanti・Freshservice・Salesforce・Zendesk・TOPdesk・Microsoft）](03_導入編/16-competitor-comparison.md) — ServiceNow を主要競合 8 社（Atlassian Jira Service Management、BMC Helix、Ivanti Neurons for ITSM、Freshworks Freshservice、Salesforce Agentforce IT Service、Zendesk、TOPdesk、Microsoft）と、機能範囲・公開価格帯・強み弱み・アナリスト評価の観点で比較し、製品選定・提案・競合対策で使える判断基準と質問リストを示す。価格はすべて出典・取得日付きの公開価格または【推定】。
- [ビジネスケース作成・ROI 算出・価値実現（Business Case / ROI / Value Realization）](03_導入編/17-business-case-roi-value-realization.md) — ServiceNow 導入前のビジネスケースの組み立て方（現状コスト分析、効果 KPI、ROI・NPV・TCO・回収期間の算定式、ServiceNow Benchmarks や Forrester TEI の使い方と注意点）と、導入後の価値実現（Value Realization）の測定方法（ベースライン設定、Performance Analytics の Indicator/Target/Threshold による KPI 追跡、ITSM Success Dashboard、AI Admin Center Business Value dashboard、ServiceNow Impact の Value management／Value report）を、経営層向け説明テンプレートとともに実務で使える粒度でまとめる。
- [導入後の運用保守委託（AMS/マネージドサービス）の設計](03_導入編/18-managed-services-ams.md) — ServiceNow の Go-Live 後に運用保守を外部委託（AMS: Application Management Services／マネージドサービス）するときの設計を、実務で使える粒度でまとめる。L1〜L4 のサポートレベルとスコープ（拡張開発、パッチ・アップグレード対応、ライセンス運用を含む）、ServiceNow 社のサポート（Customer Support Addendum、Impact、Developer Support）との責任分界、運用移行（Hypercare→Stabilization→移管）、AMS 契約の SLA/KPI、料金モデル（固定・時間/ポイント・チケット・専任チーム・キャパシティ型）、内製化との比較とハイブリッド型、日本市場の AMS 提供事業者の傾向、RFP・契約チェックリストを扱う。
- [ServiceNow 停止時の事業継続と災害復旧（DR）計画](03_導入編/19-service-continuity-dr.md) — ServiceNow を利用する企業側から見た BCP（事業継続計画）／DR（災害復旧）計画を実務の粒度でまとめる。ServiceNow 社が提供する AHA（データセンターペア・Transfer／Failover）、RTO 2 時間・RPO 1 時間、99.8% Availability SLA、バックアップ仕様と、顧客側の責任範囲を切り分けたうえで、インスタンス停止・劣化時の代替手順（オフライン運用、緊急連絡手段、メール受付の退避、SSO 障害時のログイン）、バックアップ一覧の取得と復元依頼（Now Support の Automation Store・サポートケース・fix-forward 方針・Deleted Records／Rollback）、外部へのデータ退避（エクスポート、Export Sets、Table API、Instance Data Replication、第三者製品）、DR 訓練の進め方を扱う。

### 04_応用編（15 ファイル）

- [導入失敗パターンと対策（Implementation Failure Patterns）](04_応用編/01-implementation-failure-patterns.md) — ServiceNow 導入プロジェクトで繰り返し起きる失敗パターン（過度なカスタマイズと OOTB からの逸脱、As-Is 要件の移植（Lift and Shift）、現状分析の省略、100% 網羅とスコープクリープ、履歴データの全件移行、CMDB の失敗、ガバナンス／CoE の不在、定着不足と OCM の削減、社内スキル不足、UAT 軽視、戦略不在、過剰標準化）を「症状・原因・対策」の形で整理し、公式ドキュメントと ServiceNow Community の出典を付けてまとめる。
- [カスタマイズと技術的負債（Customization and Technical Debt）](04_応用編/02-customization-technical-debt.md) — ServiceNow における Configuration（構成）と Customization（カスタマイズ）の公式定義と判断基準、カスタマイズが Skipped records（スキップされたレコード）と技術的負債を生む仕組み、Instance Scan・Impact Platform Health（Scan Engine）による負債の可視化、カスタマイズのスコアカード（KPI）の作り方、Skipped records の削減策、OOTB（標準）への回帰の進め方を、出典付きの実務知見としてまとめる。
- [パフォーマンスチューニング（Performance Tuning）](04_応用編/03-performance-tuning.md) — ServiceNow インスタンスで「遅い」と言われたときの調査手順（Transaction log、Session Debug、Slow Queries、Explain Plan）と、遅いリスト・フォーム、Business Rule、インデックス（Index Suggestion Engine）、GlideRecord、大量データ（テーブルローテーション、アーカイブ、Table Cleaner、インポート）の改善策を、ServiceNow 公式ドキュメントと ServiceNow Technical Support Performance チーム（GTSPerformance）の公開知見に基づいてまとめる。
- [アップグレードの教訓（Upgrade Lessons Learned）](04_応用編/04-upgrade-lessons.md) — ServiceNow のファミリーアップグレード／パッチ適用で実際に起きる問題事例（Skipped records の放置、クローンしたウィジェット、DOM 操作、廃止機能、MID Server、クローン事故、性能劣化、連携障害）を症状・原因・対策で整理し、事前対策、リスクベースのテスト戦略、Skipped records の Retain/Merge/Revert 判断とファミリーを飛ばすかどうかの判断基準を、出典付きの知見としてまとめる。
- [CMDB成功の要因（CMDB Success Factors）](04_応用編/05-cmdb-success-factors.md) — ServiceNow の CMDB が「使われないデータの墓場」にならずに成功するための要因を、目的・ユースケースの設定、CSDM 準拠、データ所有者（Managed by group 等）の明確化、Discovery の範囲設計、品質維持（CMDB Health・Data Manager・Attestation・CMDB success advisor）、段階導入（Foundation→Crawl→Walk→Run→Fly）の 6 観点で、出典付きの知見と具体的な設定項目（テーブル・フィールド・ロール・プロパティ・ジョブ）として整理する。
- [ライセンスコスト最適化（License Cost Optimization）](04_応用編/06-license-cost-optimization.md) — ServiceNow のサブスクリプション費用を最適化するための実務知見をまとめる。計測の仕組み（Subscription Management、measured roles、active user の定義）、ロール付与の棚卸し手順、Fulfiller 削減（Approver のみ・休眠・退職者・連携アカウント）、シェルフウェアの回避（未使用モジュール、Now Assist の Assist 枠、カスタムテーブル）、契約交渉のレバー、更新時の注意を、出典付きで整理する。
- [スクリプトのベストプラクティスとアンチパターン（Scripting Best Practices and Anti-patterns）](04_応用編/07-scripting-best-practices.md) — ServiceNow のサーバー／クライアントスクリプトでよく起きるアンチパターン（Business Rule 内の current.update()、クライアント側の同期 GlideRecord／getXMLWait、sys_id のハードコード、gs.log の残置、無秩序なグローバルスコープ開発）と、その代替手段（Before/After/Async の使い分け、setWorkflow(false) の限定利用、GlideAjax と g_scratchpad、System Property／Decision Table、スコープ付きロギング、Private scope と Runtime Access Tracking）、Instance Scan を使ったコードレビューの自動化とレビュー観点をまとめる。
- [連携の落とし穴（Integration Pitfalls）](04_応用編/08-integration-pitfalls.md) — ServiceNow と外部システムの連携で本番障害につながりやすい落とし穴を、API 制限（Rate Limit Rules、セマフォ、Transaction Quota、アウトバウンド接続プール・タイムアウト）、エラーハンドリング（Retry policy、ログ、部分失敗）、冪等性（coalesce、Correlation ID、エコーループ、順序）、MID Server 運用（ECC Queue、クラスター、サイジング、自動アップグレード、クローン後の資格情報）、認証情報管理（連携ユーザー、Connection & Credential alias、OAuth リフレッシュトークン、外部 Vault）、大量データ連携（ページング、Data Stream、Concurrent imports、Import Set のクリーンアップ）の観点で、出典付きで整理する。
- [ガバナンスとCoEの実践（Governance and CoE in Practice）](04_応用編/09-governance-coe-practice.md) — ServiceNow の Platform Owner の役割と権限、デマンド受付（Intake）の実践、アーキテクチャレビュー委員会（Technical Governance Board / ARB）の運営、標準化（Configure → Integrate → Customize、命名規約、ポリシー体系）、開発ガイドライン（スコープ方針、委任開発、Instance Scan による自動ガードレール、Definition of Ready / Done）を、公式ドキュメントと ServiceNow Community の実務知見から出典付きでまとめる。
- [Now Assist / AI Agents 導入の知見（AI Adoption Lessons）](04_応用編/10-ai-adoption-lessons.md) — Now Assist（生成AIスキル）と AI Agents（エージェント型AI）を導入・拡大するときの実務知見をまとめる。ユースケース選定（Workflow / スキル / AI エージェントの使い分け）、ナレッジ・データ品質、Assist 消費の見積り・監視・抑制、ガバナンス（Now Assist Guardian、Data Privacy、AI Control Tower、エージェントの実行ID）、効果測定（Now Assist Analytics、Value タブ、評価指標）、公開導入事例を出典付きで整理する。
- [ITSMプロセス設計の実践知（ITSM Process Design Tips）](04_応用編/11-itsm-process-design-tips.md) — ServiceNow ITSM のプロセス設計で議論になりやすい6つのテーマ（優先度設計、割り当てルール、SLA設計、カテゴリ設計、Major Incident、変更承認の簡素化）について、標準機能の仕様（テーブル、ロール、プロパティ、実行順序）と、ServiceNow 社員・実務者の知見を出典付きで整理する。「何を標準のまま使い、どこを設計で決めるべきか」に答える。
- [セキュリティ強化の実践（Security Hardening in Practice）](04_応用編/12-security-hardening-practice.md) — ServiceNow インスタンスのセキュリティ強化を「実際に回す」ための知見をまとめる。Security Center（旧 Instance Security Center）の運用サイクルと Auditor チェック・Access Findings の活用、ACL 設計で事故につながる落とし穴（空 ACL、データ条件のみの ACL による件数推測、GlideRecord、Client callable Script Include）、外部公開ポータルのリスク（Public ウィジェット、ナレッジ User Criteria、Guest、AI エージェント経路）、権限昇格の経路（security_admin、admin 付与、なりすまし、Run as System）、監査（sys_audit、sys_audit_role、Identity and Access Audit、なりすまし監査、LES による SIEM 連携）を、過去の公開事例と公式ドキュメントの出典付きで解説する。
- [定着化と組織変革（Adoption and Organizational Change Management）](04_応用編/13-adoption-change-management.md) — ServiceNow の導入効果を「使われる」状態に変えるための実務知見をまとめる。OCM（組織変革管理）の体制・計画・チャンピオン、トレーニング（役割別・タスク型、Adoption Services の Guided Tours / Embedded Help / Help Center / Dynamic Guidance）、ポータル利用促進（Employee Center、Campaign、Content Analytics、Usage Insights）、シフトレフト（ナレッジ・Virtual Agent・自動化によるデフレクション計測）、KPI による効果測定（ITSM Success Dashboard の Self-solved % / Call deflection の公式計算式、Assistant analytics の Deflection Rate）を出典付きで整理する。
- [コンサルティング実践プレイブック（Consulting Playbook）](04_応用編/14-consulting-playbook.md) — ServiceNow のコンサルティング（現状診断、新規導入・再構築の提案、ロードマップ策定）を実務で進めるための手引き。アセスメント観点（プロセス・データ・プラットフォーム健全性・ガバナンス・定着・AI）、ヒアリング質問集、成熟度評価（ServiceNow Impact の ITSM / ITOM Maturity Assessment、Health Assessment と Instance Health スコア、CSDM の Crawl/Walk/Run/Fly、Benchmarks）、ロードマップ策定、提案時の論点、よくある顧客質問と回答を、公式ドキュメントと ServiceNow Community の知見から出典付きでまとめる。
- [ITSM から ESM・全社プラットフォームへの展開ロードマップ（Platform Expansion Roadmap）](04_応用編/15-platform-expansion-roadmap.md) — 初期導入（多くは ITSM）の後に ITOM・ITAM・HRSD・CSM・SPM・IRM・SecOps・AI へ横展開する順序と判断基準（データ基盤の依存関係、CMDB/CSDM 成熟度、ライセンスの組み合わせ、組織の準備度）を、公式の段階モデル（CSDM implementation stages、Service Operations Recommended Implementation Sequence）と出典付きの実務知見で整理し、典型的な 3 か年ロードマップ例、展開時のアンチパターン、プラットフォームオーナー向け意思決定チェックリストを示す。

### ルート直下

- [ServiceNow 用語集（Glossary・A–Z）](glossary.md) — 本ナレッジ全体（01_入門編〜04_応用編）から抽出した ServiceNow の重要用語・略語約 380 語を、英語名のアルファベット順に「用語（英語）／日本語訳／説明／関連ファイル」の表で示す用語集。付録に表記ルール、主要テーブル名・ロール名の早見表、紛らわしい略語、旧名称・新名称の対応表、リリース名、認定資格、ITIL 用語対応、日本語訳の揺れを収める。AI が用語の意味と、詳しく書かれたファイルを引くための入口として使う。
- [ServiceNow ナレッジ 執筆規約](_CONVENTIONS.md) — （フロントマターに summary なし）本ナレッジの執筆規約。基準リリース、ファイル構成、フロントマター項目、本文の書き方、出典と確度ラベル、画像の扱い、編ごとの役割を定める。

## 7. 目的別の読み順

### 7.1 入門者（ServiceNow を初めて扱う人）

1. [01-what-is-servicenow.md](01_入門編/01-what-is-servicenow.md)：会社と市場での位置づけ
2. [02-platform-overview.md](01_入門編/02-platform-overview.md)：単一プラットフォームの考え方
3. [03-product-portfolio.md](01_入門編/03-product-portfolio.md)：製品の全体地図
4. [04-core-concepts.md](01_入門編/04-core-concepts.md)：インスタンス、テーブル、sys_id、スコープ、ロール、ACL
5. [05-ui-basics.md](01_入門編/05-ui-basics.md)：画面と基本操作
6. [06-itil-itsm-basics.md](01_入門編/06-itil-itsm-basics.md)：ITIL 4 と ITSM の対応
7. [07-release-cycle.md](01_入門編/07-release-cycle.md)：リリースの仕組み
8. [08-users-roles-licensing-basics.md](01_入門編/08-users-roles-licensing-basics.md)：ユーザー・ロール・ライセンスの関係
9. [09-learning-path.md](01_入門編/09-learning-path.md)：PDI と認定資格（CSA から）
10. 次の段階：[itsm-overview.md](02_リファレンス/itsm/itsm-overview.md) → [incident-management.md](02_リファレンス/itsm/incident-management.md) → [service-catalog.md](02_リファレンス/platform/service-catalog.md) → [cmdb-csdm.md](02_リファレンス/platform/cmdb-csdm.md)
- 分からない用語は随時 [glossary.md](glossary.md) で引く。

### 7.2 IT コンサルタント／PM

1. 入門編のうち 01・03・08 を読む
2. 契約と費用：[01-licensing-model.md](03_導入編/01-licensing-model.md) → [03-edition-comparison.md](03_導入編/03-edition-comparison.md) → [platform-licensing-packaging.md](02_リファレンス/platform/platform-licensing-packaging.md) → [02-pricing.md](03_導入編/02-pricing.md)（【推定】に注意）
3. 提案と比較：[16-competitor-comparison.md](03_導入編/16-competitor-comparison.md) → [17-business-case-roi-value-realization.md](03_導入編/17-business-case-roi-value-realization.md) → [15-japan-market.md](03_導入編/15-japan-market.md)
4. 導入計画：[04-implementation-methodology.md](03_導入編/04-implementation-methodology.md) → [05-project-organization.md](03_導入編/05-project-organization.md) → [06-requirements-design.md](03_導入編/06-requirements-design.md) → [11-testing-golive.md](03_導入編/11-testing-golive.md)
5. 運用：[12-operations-governance.md](03_導入編/12-operations-governance.md) → [18-managed-services-ams.md](03_導入編/18-managed-services-ams.md)
6. 知見：[14-consulting-playbook.md](04_応用編/14-consulting-playbook.md) → [01-implementation-failure-patterns.md](04_応用編/01-implementation-failure-patterns.md) → [13-adoption-change-management.md](04_応用編/13-adoption-change-management.md) → [06-license-cost-optimization.md](04_応用編/06-license-cost-optimization.md) → [15-platform-expansion-roadmap.md](04_応用編/15-platform-expansion-roadmap.md)
7. 担当領域の概要：[itsm-overview.md](02_リファレンス/itsm/itsm-overview.md)、[itom-overview.md](02_リファレンス/itom/itom-overview.md)、[itam-overview.md](02_リファレンス/itam/itam-overview.md) など

### 7.3 アーキテクト

1. 入門編のうち 02・04・07 を読む
2. 基盤：[instance-architecture.md](02_リファレンス/platform/instance-architecture.md) → [data-model-dictionary.md](02_リファレンス/platform/data-model-dictionary.md) → [cmdb-csdm.md](02_リファレンス/platform/cmdb-csdm.md) → [domain-separation.md](02_リファレンス/platform/domain-separation.md)
3. セキュリティ：[users-groups-roles.md](02_リファレンス/platform/users-groups-roles.md) → [access-control-acl.md](02_リファレンス/platform/access-control-acl.md) → [authentication-sso.md](02_リファレンス/platform/authentication-sso.md) → [platform-security-encryption.md](02_リファレンス/platform/platform-security-encryption.md)
4. 連携とデータ：[integrationhub.md](02_リファレンス/platform/integrationhub.md) → [web-services-api.md](02_リファレンス/platform/web-services-api.md) → [mid-server.md](02_リファレンス/platform/mid-server.md) → [import-export-data.md](02_リファレンス/platform/import-export-data.md) → [workflow-data-fabric.md](02_リファレンス/platform/workflow-data-fabric.md) → [service-bridge-ebonding.md](02_リファレンス/customer/service-bridge-ebonding.md)
5. 設計：[07-instance-strategy.md](03_導入編/07-instance-strategy.md) → [09-integration-design.md](03_導入編/09-integration-design.md) → [10-security-compliance.md](03_導入編/10-security-compliance.md) → [19-service-continuity-dr.md](03_導入編/19-service-continuity-dr.md)
6. AI：[now-assist-ai-agents.md](02_リファレンス/platform/now-assist-ai-agents.md) → [predictive-intelligence-ai-search.md](02_リファレンス/platform/predictive-intelligence-ai-search.md)
7. 知見：[02-customization-technical-debt.md](04_応用編/02-customization-technical-debt.md) → [05-cmdb-success-factors.md](04_応用編/05-cmdb-success-factors.md) → [08-integration-pitfalls.md](04_応用編/08-integration-pitfalls.md) → [09-governance-coe-practice.md](04_応用編/09-governance-coe-practice.md) → [12-security-hardening-practice.md](04_応用編/12-security-hardening-practice.md)

### 7.4 エンジニア（開発者・管理者）

1. 入門編のうち 04・05 を読む
2. データと画面：[data-model-dictionary.md](02_リファレンス/platform/data-model-dictionary.md) → [lists-forms.md](02_リファレンス/platform/lists-forms.md) → [next-experience-ui.md](02_リファレンス/platform/next-experience-ui.md) → [workspaces-ui-builder.md](02_リファレンス/platform/workspaces-ui-builder.md) → [portals-employee-center.md](02_リファレンス/platform/portals-employee-center.md)
3. スクリプトと自動化：[scripting-server-side.md](02_リファレンス/platform/scripting-server-side.md) → [scripting-client-side.md](02_リファレンス/platform/scripting-client-side.md) → [events-script-actions-scheduled-jobs.md](02_リファレンス/platform/events-script-actions-scheduled-jobs.md) → [flow-designer-workflow-studio.md](02_リファレンス/platform/flow-designer-workflow-studio.md) → [notifications-email.md](02_リファレンス/platform/notifications-email.md)
4. 開発と移送：[app-development.md](02_リファレンス/platform/app-development.md) → [update-sets-cloning.md](02_リファレンス/platform/update-sets-cloning.md) → [automated-test-framework.md](02_リファレンス/platform/automated-test-framework.md)
5. 運用と調査：[system-administration.md](02_リファレンス/platform/system-administration.md) → [debugging-troubleshooting.md](02_リファレンス/platform/debugging-troubleshooting.md) → [access-control-acl.md](02_リファレンス/platform/access-control-acl.md)
6. 知見：[07-scripting-best-practices.md](04_応用編/07-scripting-best-practices.md) → [03-performance-tuning.md](04_応用編/03-performance-tuning.md) → [04-upgrade-lessons.md](04_応用編/04-upgrade-lessons.md) → [08-integration-pitfalls.md](04_応用編/08-integration-pitfalls.md)
7. 担当製品のリファレンス（02_リファレンスの領域別フォルダ）

### 7.5 AI（LLM／RAG）向けの利用手順

1. **最初にこの README を読む**。質問を「8. 質問カテゴリ → 参照ファイル対応表」に当てはめ、参照するファイルの候補を決める。
2. 候補が決まらない場合は、「6. 全ファイル一覧」の `summary` と、各ファイルのフロントマター `keywords` で照合する。用語や略語の意味は [glossary.md](glossary.md) で調べる（「関連ファイル」列から詳細ファイルへ進める）。
3. **仕様の質問は 02_リファレンスを主な根拠にする**。計画・契約の質問は 03_導入編、実務上の勘所の質問は 04_応用編を併用する。01_入門編は概要と用語の確認に使う。
4. 回答は **Australia 基準**で書く。ファイル内に「> **Brazil での変更:**」がある場合は、その内容も併記する。旧リリースや旧名称で聞かれた場合は、名称の対応（[glossary.md 付録 E](glossary.md#付録-e-旧名称新名称の対応表) の旧名・新名の対応表）を確認する。
5. **確度ラベル（【第三者情報】【推定】【経験則】）は回答から省かない**。出典 URL を添える。ナレッジにない事項や「公開情報では確認できず」と書かれた事項は、推測で補わず、その旨を答える。
6. 価格は推定値・出典・取得日をセットで答え、公式価格ではないことを明示する。
7. ファイルの `last_verified` が古い場合や、製品名・パッケージの変更に関わる質問の場合は、情報が更新されている可能性に触れる。

## 8. 質問カテゴリ → 参照ファイル対応表

「主な参照先」を最初に読み、必要に応じて「補助」を読む。パスはこの README からの相対パスである。

### 8.1 全般・概要

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| ServiceNow はどんな会社か、業績、日本法人 | [01-what-is-servicenow.md](01_入門編/01-what-is-servicenow.md) | [15-japan-market.md](03_導入編/15-japan-market.md) |
| 製品の一覧、どの製品が何をするか、製品名の変更 | [03-product-portfolio.md](01_入門編/03-product-portfolio.md) | [glossary.md 付録 E（旧名称・新名称の対応表）](glossary.md#付録-e-旧名称新名称の対応表) |
| プラットフォームの全体像・アーキテクチャ | [02-platform-overview.md](01_入門編/02-platform-overview.md) | [instance-architecture.md](02_リファレンス/platform/instance-architecture.md) |
| 用語・略語の意味 | [glossary.md](glossary.md) | [glossary.md 付録 D（紛らわしい略語）](glossary.md#付録-d-同じ略語似た名前で意味が違うもの要注意) |
| リリース名、EA/GA 日、パッチ、サポート期間（N-1） | [07-release-cycle.md](01_入門編/07-release-cycle.md) | [13-upgrade-management.md](03_導入編/13-upgrade-management.md) |
| 学習方法、PDI、認定資格（CSA/CAD/CIS） | [09-learning-path.md](01_入門編/09-learning-path.md) | — |
| ITIL との対応 | [06-itil-itsm-basics.md](01_入門編/06-itil-itsm-basics.md) | [itsm-overview.md](02_リファレンス/itsm/itsm-overview.md) |

### 8.2 ライセンス・価格・契約

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| ライセンスの種類（Fulfiller/Requester 等）、課金の仕組み | [01-licensing-model.md](03_導入編/01-licensing-model.md) | [08-users-roles-licensing-basics.md](01_入門編/08-users-roles-licensing-basics.md) |
| エディション差（Standard/Pro/Enterprise、Foundation/Advanced/Prime） | [03-edition-comparison.md](03_導入編/03-edition-comparison.md) | [platform-licensing-packaging.md](02_リファレンス/platform/platform-licensing-packaging.md)、[itsm-overview.md](02_リファレンス/itsm/itsm-overview.md) |
| 価格・単価・TCO（すべて【推定】） | [02-pricing.md](03_導入編/02-pricing.md) | [16-competitor-comparison.md](03_導入編/16-competitor-comparison.md) |
| ITOM/ITAM の Subscription Unit（SU） | [itom-overview.md](02_リファレンス/itom/itom-overview.md) | [01-licensing-model.md](03_導入編/01-licensing-model.md) |
| Now Assist の Assist 課金、IntegrationHub トランザクション、WDF | [now-assist-ai-agents.md](02_リファレンス/platform/now-assist-ai-agents.md)、[integrationhub.md](02_リファレンス/platform/integrationhub.md) | [workflow-data-fabric.md](02_リファレンス/platform/workflow-data-fabric.md) |
| ライセンス費用の削減、棚卸し | [06-license-cost-optimization.md](04_応用編/06-license-cost-optimization.md) | [12-operations-governance.md](03_導入編/12-operations-governance.md) |
| 競合との比較（JSM、BMC、Ivanti 等） | [16-competitor-comparison.md](03_導入編/16-competitor-comparison.md) | — |
| ROI、ビジネスケース、価値の測定 | [17-business-case-roi-value-realization.md](03_導入編/17-business-case-roi-value-realization.md) | [13-adoption-change-management.md](04_応用編/13-adoption-change-management.md) |

### 8.3 導入プロジェクト・運用

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| 導入方法論、期間・工数の目安 | [04-implementation-methodology.md](03_導入編/04-implementation-methodology.md) | [01-implementation-failure-patterns.md](04_応用編/01-implementation-failure-patterns.md) |
| 体制、パートナー、Impact、Expert Services | [05-project-organization.md](03_導入編/05-project-organization.md) | [14-support-monitoring.md](03_導入編/14-support-monitoring.md) |
| 要件定義、Fit-Gap、OOTB 優先 | [06-requirements-design.md](03_導入編/06-requirements-design.md) | [02-customization-technical-debt.md](04_応用編/02-customization-technical-debt.md) |
| 環境構成（Dev/Test/Prod）、クローン戦略 | [07-instance-strategy.md](03_導入編/07-instance-strategy.md) | [update-sets-cloning.md](02_リファレンス/platform/update-sets-cloning.md) |
| データ移行 | [08-data-migration.md](03_導入編/08-data-migration.md) | [import-export-data.md](02_リファレンス/platform/import-export-data.md) |
| テスト計画、Go-Live、Hypercare | [11-testing-golive.md](03_導入編/11-testing-golive.md) | [automated-test-framework.md](02_リファレンス/platform/automated-test-framework.md)、[test-management.md](02_リファレンス/spm/test-management.md) |
| 運用体制、ガバナンス、CoE、Platform Owner | [12-operations-governance.md](03_導入編/12-operations-governance.md) | [09-governance-coe-practice.md](04_応用編/09-governance-coe-practice.md) |
| アップグレード計画、Skipped records | [13-upgrade-management.md](03_導入編/13-upgrade-management.md) | [04-upgrade-lessons.md](04_応用編/04-upgrade-lessons.md) |
| Now Support、サポート、インスタンス監視 | [14-support-monitoring.md](03_導入編/14-support-monitoring.md) | [system-administration.md](02_リファレンス/platform/system-administration.md) |
| 運用保守の委託（AMS） | [18-managed-services-ams.md](03_導入編/18-managed-services-ams.md) | — |
| BCP/DR、障害時の代替手段、バックアップ | [19-service-continuity-dr.md](03_導入編/19-service-continuity-dr.md) | [instance-architecture.md](02_リファレンス/platform/instance-architecture.md) |
| 日本固有（データセンター、ISMAP、日本語化、和暦） | [15-japan-market.md](03_導入編/15-japan-market.md) | [localization.md](02_リファレンス/platform/localization.md)、[10-security-compliance.md](03_導入編/10-security-compliance.md) |
| 定着化、OCM、トレーニング、シフトレフト | [13-adoption-change-management.md](04_応用編/13-adoption-change-management.md) | — |
| アセスメント、ロードマップ、提案の論点 | [14-consulting-playbook.md](04_応用編/14-consulting-playbook.md) | [15-platform-expansion-roadmap.md](04_応用編/15-platform-expansion-roadmap.md) |

### 8.4 プラットフォーム（基盤・データ・セキュリティ）

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| インスタンス構成、データセンター、AHA、RaptorDB | [instance-architecture.md](02_リファレンス/platform/instance-architecture.md) | [19-service-continuity-dr.md](03_導入編/19-service-continuity-dr.md) |
| テーブル、フィールドタイプ、Dictionary、テーブル拡張 | [data-model-dictionary.md](02_リファレンス/platform/data-model-dictionary.md) | [04-core-concepts.md](01_入門編/04-core-concepts.md) |
| CMDB、CI クラス、IRE、CSDM | [cmdb-csdm.md](02_リファレンス/platform/cmdb-csdm.md) | [05-cmdb-success-factors.md](04_応用編/05-cmdb-success-factors.md) |
| ユーザー・グループ・ロール、主要ロール一覧 | [users-groups-roles.md](02_リファレンス/platform/users-groups-roles.md) | [08-users-roles-licensing-basics.md](01_入門編/08-users-roles-licensing-basics.md) |
| ACL、アクセス制御の評価順序 | [access-control-acl.md](02_リファレンス/platform/access-control-acl.md) | [12-security-hardening-practice.md](04_応用編/12-security-hardening-practice.md) |
| ログイン、SSO（SAML/OIDC）、MFA、OAuth | [authentication-sso.md](02_リファレンス/platform/authentication-sso.md) | [09-integration-design.md](03_導入編/09-integration-design.md) |
| 暗号化、Security Center、監査ログ、データプライバシー | [platform-security-encryption.md](02_リファレンス/platform/platform-security-encryption.md) | [10-security-compliance.md](03_導入編/10-security-compliance.md)、[12-security-hardening-practice.md](04_応用編/12-security-hardening-practice.md) |
| ドメインセパレーション、MSP | [domain-separation.md](02_リファレンス/platform/domain-separation.md) | [vendor-manager-service-owner-siam.md](02_リファレンス/itsm/vendor-manager-service-owner-siam.md) |
| システムプロパティ、プラグイン、テーブルのクリーンアップ・アーカイブ | [system-administration.md](02_リファレンス/platform/system-administration.md) | [03-performance-tuning.md](04_応用編/03-performance-tuning.md) |
| 日本語化、タイムゾーン、翻訳 | [localization.md](02_リファレンス/platform/localization.md) | [15-japan-market.md](03_導入編/15-japan-market.md) |
| 性能が遅い、インデックス、Slow Queries | [03-performance-tuning.md](04_応用編/03-performance-tuning.md) | [system-administration.md](02_リファレンス/platform/system-administration.md)、[debugging-troubleshooting.md](02_リファレンス/platform/debugging-troubleshooting.md) |

### 8.5 UI・ポータル・コラボレーション

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| 画面の種類、基本操作 | [05-ui-basics.md](01_入門編/05-ui-basics.md) | [next-experience-ui.md](02_リファレンス/platform/next-experience-ui.md) |
| リスト、フォーム、UI Policy、Data Policy | [lists-forms.md](02_リファレンス/platform/lists-forms.md) | [scripting-client-side.md](02_リファレンス/platform/scripting-client-side.md) |
| Next Experience、Unified Navigation、テーマ | [next-experience-ui.md](02_リファレンス/platform/next-experience-ui.md) | — |
| Workspace、Service Operations Workspace、UI Builder | [workspaces-ui-builder.md](02_リファレンス/platform/workspaces-ui-builder.md) | [itsm-overview.md](02_リファレンス/itsm/itsm-overview.md) |
| Service Portal、Employee Center、ウィジェット | [portals-employee-center.md](02_リファレンス/platform/portals-employee-center.md) | [csm-portal-engagement-messenger-partner.md](02_リファレンス/customer/csm-portal-engagement-messenger-partner.md) |
| モバイルアプリ（Now Mobile、Mobile Agent）、オフライン | [mobile.md](02_リファレンス/platform/mobile.md) | [field-service-management.md](02_リファレンス/customer/field-service-management.md) |
| Teams/Slack 連携、Visual Task Boards | [collaboration-vtb-teams-slack.md](02_リファレンス/platform/collaboration-vtb-teams-slack.md) | [virtual-agent.md](02_リファレンス/platform/virtual-agent.md) |
| 通知、メール送受信、Inbound email action | [notifications-email.md](02_リファレンス/platform/notifications-email.md) | — |
| アンケート、満足度調査（CSAT/NPS） | [surveys-assessments.md](02_リファレンス/platform/surveys-assessments.md) | — |
| レポート、ダッシュボード、Performance Analytics | [reporting-analytics.md](02_リファレンス/platform/reporting-analytics.md) | [itsm-pro-features.md](02_リファレンス/itsm/itsm-pro-features.md) |

### 8.6 開発・自動化・連携

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| Business Rule、Script Include、GlideRecord | [scripting-server-side.md](02_リファレンス/platform/scripting-server-side.md) | [07-scripting-best-practices.md](04_応用編/07-scripting-best-practices.md) |
| Client Script、g_form、GlideAjax、UI Action | [scripting-client-side.md](02_リファレンス/platform/scripting-client-side.md) | [07-scripting-best-practices.md](04_応用編/07-scripting-best-practices.md) |
| イベント、Script Action、スケジュールジョブ | [events-script-actions-scheduled-jobs.md](02_リファレンス/platform/events-script-actions-scheduled-jobs.md) | — |
| Flow Designer / Workflow Studio、サブフロー、Decision table | [flow-designer-workflow-studio.md](02_リファレンス/platform/flow-designer-workflow-studio.md) | — |
| カスタムアプリ開発、スコープ、Studio/IDE/SDK、Store 公開 | [app-development.md](02_リファレンス/platform/app-development.md) | [09-governance-coe-practice.md](04_応用編/09-governance-coe-practice.md) |
| Update Set、移送、クローン | [update-sets-cloning.md](02_リファレンス/platform/update-sets-cloning.md) | [07-instance-strategy.md](03_導入編/07-instance-strategy.md) |
| 自動テスト（ATF） | [automated-test-framework.md](02_リファレンス/platform/automated-test-framework.md) | [11-testing-golive.md](03_導入編/11-testing-golive.md) |
| デバッグ、ログ、Session Debug | [debugging-troubleshooting.md](02_リファレンス/platform/debugging-troubleshooting.md) | — |
| REST/SOAP API、Scripted REST、認証方式、レート制限 | [web-services-api.md](02_リファレンス/platform/web-services-api.md) | [08-integration-pitfalls.md](04_応用編/08-integration-pitfalls.md) |
| IntegrationHub、Spoke | [integrationhub.md](02_リファレンス/platform/integrationhub.md) | [09-integration-design.md](03_導入編/09-integration-design.md) |
| MID Server | [mid-server.md](02_リファレンス/platform/mid-server.md) | [08-integration-pitfalls.md](04_応用編/08-integration-pitfalls.md) |
| インポート、Transform Map、エクスポート | [import-export-data.md](02_リファレンス/platform/import-export-data.md) | [08-data-migration.md](03_導入編/08-data-migration.md) |
| Workflow Data Fabric、Zero Copy | [workflow-data-fabric.md](02_リファレンス/platform/workflow-data-fabric.md) | — |
| インスタンス間連携、eBonding、Service Bridge/Service Exchange | [service-bridge-ebonding.md](02_リファレンス/customer/service-bridge-ebonding.md) | [vendor-manager-service-owner-siam.md](02_リファレンス/itsm/vendor-manager-service-owner-siam.md) |
| 外部システム連携の設計（AD、Jira、SAP、監視ツール） | [09-integration-design.md](03_導入編/09-integration-design.md) | [08-integration-pitfalls.md](04_応用編/08-integration-pitfalls.md) |
| RPA、Process Mining、Document Intelligence | [process-automation-rpa-mining.md](02_リファレンス/platform/process-automation-rpa-mining.md) | — |

### 8.7 AI

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| Now Assist / ServiceNow Otto、AI Agents、AI Control Tower、LLM | [now-assist-ai-agents.md](02_リファレンス/platform/now-assist-ai-agents.md) | [10-ai-adoption-lessons.md](04_応用編/10-ai-adoption-lessons.md) |
| Predictive Intelligence、AI Search | [predictive-intelligence-ai-search.md](02_リファレンス/platform/predictive-intelligence-ai-search.md) | [itsm-pro-features.md](02_リファレンス/itsm/itsm-pro-features.md) |
| Virtual Agent、会話型 AI | [virtual-agent.md](02_リファレンス/platform/virtual-agent.md) | [collaboration-vtb-teams-slack.md](02_リファレンス/platform/collaboration-vtb-teams-slack.md) |
| AI 導入の進め方、Assist 消費の管理、効果測定 | [10-ai-adoption-lessons.md](04_応用編/10-ai-adoption-lessons.md) | [17-business-case-roi-value-realization.md](03_導入編/17-business-case-roi-value-realization.md) |

### 8.8 ITSM

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| ITSM の全体像、パッケージ、SOW | [itsm-overview.md](02_リファレンス/itsm/itsm-overview.md) | [03-edition-comparison.md](03_導入編/03-edition-comparison.md) |
| インシデント、優先度、Major Incident、On-Call | [incident-management.md](02_リファレンス/itsm/incident-management.md) | [11-itsm-process-design-tips.md](04_応用編/11-itsm-process-design-tips.md) |
| 問題管理、Known Error | [problem-management.md](02_リファレンス/itsm/problem-management.md) | — |
| 変更管理、CAB、承認ポリシー、リスク評価 | [change-management.md](02_リファレンス/itsm/change-management.md) | [11-itsm-process-design-tips.md](04_応用編/11-itsm-process-design-tips.md) |
| リクエスト、RITM、Catalog Task | [request-management.md](02_リファレンス/itsm/request-management.md) | [service-catalog.md](02_リファレンス/platform/service-catalog.md) |
| サービスカタログ、変数、Record producer、Order guide | [service-catalog.md](02_リファレンス/platform/service-catalog.md) | [request-management.md](02_リファレンス/itsm/request-management.md) |
| SLA 定義、スケジュール、OLA/UC | [sla-schedules.md](02_リファレンス/platform/sla-schedules.md) | [11-itsm-process-design-tips.md](04_応用編/11-itsm-process-design-tips.md) |
| サービスポートフォリオ、Service Offering、DPM | [service-level-management-itsm.md](02_リファレンス/itsm/service-level-management-itsm.md) | [cmdb-csdm.md](02_リファレンス/platform/cmdb-csdm.md) |
| リリース管理、DevOps Change Velocity、CI/CD | [release-management.md](02_リファレンス/itsm/release-management.md) | [agile-apm-eam.md](02_リファレンス/spm/agile-apm-eam.md) |
| ナレッジ管理、KCS | [knowledge-management.md](02_リファレンス/platform/knowledge-management.md) | — |
| ITSM Pro/Enterprise 固有機能（PA、PI、VA、Process Mining） | [itsm-pro-features.md](02_リファレンス/itsm/itsm-pro-features.md) | [platform-licensing-packaging.md](02_リファレンス/platform/platform-licensing-packaging.md) |
| ベンダー管理、マルチソーシング（SIAM） | [vendor-manager-service-owner-siam.md](02_リファレンス/itsm/vendor-manager-service-owner-siam.md) | [service-bridge-ebonding.md](02_リファレンス/customer/service-bridge-ebonding.md) |
| Workforce Optimization、シフト管理 | [workforce-optimization.md](02_リファレンス/itsm/workforce-optimization.md) | — |
| ITSM プロセス設計の勘所（カテゴリ、割り当て） | [11-itsm-process-design-tips.md](04_応用編/11-itsm-process-design-tips.md) | [06-requirements-design.md](03_導入編/06-requirements-design.md) |

### 8.9 ITOM・ITAM

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| ITOM の全体像、パッケージ、SU | [itom-overview.md](02_リファレンス/itom/itom-overview.md) | — |
| Discovery、資格情報、パターン | [discovery.md](02_リファレンス/itom/discovery.md) | [mid-server.md](02_リファレンス/platform/mid-server.md) |
| Service Mapping | [service-mapping.md](02_リファレンス/itom/service-mapping.md) | [cmdb-csdm.md](02_リファレンス/platform/cmdb-csdm.md) |
| Service Graph Connectors（SCCM、Intune、AWS 等） | [service-graph-connectors.md](02_リファレンス/itom/service-graph-connectors.md) | [cmdb-csdm.md](02_リファレンス/platform/cmdb-csdm.md) |
| Event Management、AIOps、アラート | [event-management-aiops.md](02_リファレンス/itom/event-management-aiops.md) | — |
| Agent Client Collector（ACC） | [agent-client-collector.md](02_リファレンス/itom/agent-client-collector.md) | [digital-end-user-experience.md](02_リファレンス/itom/digital-end-user-experience.md) |
| クラウド管理、Cloud Cost Management | [cloud-management.md](02_リファレンス/itom/cloud-management.md) | [software-asset-management.md](02_リファレンス/itam/software-asset-management.md) |
| 証明書管理、ファイアウォール監査 | [certificate-inventory-firewall-audits.md](02_リファレンス/itom/certificate-inventory-firewall-audits.md) | — |
| DEX（端末の体験可視化） | [digital-end-user-experience.md](02_リファレンス/itom/digital-end-user-experience.md) | — |
| OT（制御系・工場） | [operational-technology-management.md](02_リファレンス/itom/operational-technology-management.md) | [security-operations.md](02_リファレンス/secops/security-operations.md) |
| ITAM の全体像、Asset と CI、契約管理 | [itam-overview.md](02_リファレンス/itam/itam-overview.md) | — |
| ハードウェア資産管理（HAM） | [hardware-asset-management.md](02_リファレンス/itam/hardware-asset-management.md) | — |
| ソフトウェア資産管理（SAM）、SaaS ライセンス管理 | [software-asset-management.md](02_リファレンス/itam/software-asset-management.md) | — |
| IT 以外の物理資産（EAM） | [enterprise-asset-management.md](02_リファレンス/itam/enterprise-asset-management.md) | [field-service-management.md](02_リファレンス/customer/field-service-management.md) |

### 8.10 その他の製品領域

| 質問カテゴリ（例） | 主な参照先 | 補助 |
|---|---|---|
| PPM（Demand、Project、Portfolio、Resource） | [strategic-portfolio-management.md](02_リファレンス/spm/strategic-portfolio-management.md) | — |
| アジャイル、SAFe、Enterprise Architecture（旧 APM） | [agile-apm-eam.md](02_リファレンス/spm/agile-apm-eam.md) | — |
| IT 財務管理、TBM、コスト配賦、ショーバック | [it-financial-management-cost-allocation.md](02_リファレンス/spm/it-financial-management-cost-allocation.md) | — |
| 手動テスト管理（Test Management 2.0） | [test-management.md](02_リファレンス/spm/test-management.md) | [automated-test-framework.md](02_リファレンス/platform/automated-test-framework.md) |
| SecOps（SIR、脆弱性対応） | [security-operations.md](02_リファレンス/secops/security-operations.md) | — |
| GRC/IRM、リスク、監査、TPRM、BCM、プライバシー | [integrated-risk-management.md](02_リファレンス/irm/integrated-risk-management.md) | — |
| HR Service Delivery、HR ケース、ライフサイクルイベント | [hr-service-delivery.md](02_リファレンス/employee/hr-service-delivery.md) | [portals-employee-center.md](02_リファレンス/platform/portals-employee-center.md) |
| 人材育成、スキル、採用 | [talent-development-hiring.md](02_リファレンス/employee/talent-development-hiring.md) | — |
| ワークプレイス（座席予約・来訪者）、リーガル、ESM | [workplace-legal-other.md](02_リファレンス/employee/workplace-legal-other.md) | — |
| CSM、ケース、Omnichannel、AWA | [customer-service-management.md](02_リファレンス/customer/customer-service-management.md) | — |
| 顧客ポータル、Engagement Messenger、パートナー（B2B2C） | [csm-portal-engagement-messenger-partner.md](02_リファレンス/customer/csm-portal-engagement-messenger-partner.md) | [portals-employee-center.md](02_リファレンス/platform/portals-employee-center.md) |
| Field Service Management | [field-service-management.md](02_リファレンス/customer/field-service-management.md) | [mobile.md](02_リファレンス/platform/mobile.md) |
| 販売・受注、Sales CRM、CPQ | [sales-order-management-crm.md](02_リファレンス/customer/sales-order-management-crm.md) | — |
| 業界向け（通信、金融、医療、公共、製造、小売） | [industry-solutions.md](02_リファレンス/industry/industry-solutions.md) | — |
| 調達、買掛金、サプライヤー、ESG（Operational Sustainability） | [finance-supply-chain-esg.md](02_リファレンス/other/finance-supply-chain-esg.md) | [integrated-risk-management.md](02_リファレンス/irm/integrated-risk-management.md) |
| ITSM の後にどの製品へ広げるか | [15-platform-expansion-roadmap.md](04_応用編/15-platform-expansion-roadmap.md) | [03-product-portfolio.md](01_入門編/03-product-portfolio.md) |

## 参照元

- 本 README は、本ナレッジ内の各ファイルのフロントマター（`title`／`summary`）と [_CONVENTIONS.md](_CONVENTIONS.md) を元に作成した。個々の事実の出典は、各ファイルの「## 参照元」を参照のこと。
- Australia の公開済みバージョン一覧：https://www.servicenow.com/docs/r/australia/release-notes/available-versions.html
- Brazil の公開済みバージョン一覧：https://www.servicenow.com/docs/r/brazil/release-notes/available-versions.html
