---
title: Datadog ナレッジ 全体目次（README）
category: meta
domain: general
last_verified: 2026-11-02
summary: Datadog ナレッジ全体の入口。ナレッジの目的・基準日（2026-11-02）・基準サイト（AP1）・読者別の読み方・編（入門編／リファレンス／導入編／応用編）ごとの役割と、全ファイルへの相対リンクと 1 行サマリーをまとめた目次。AI が最初に読み、質問に答えるためにどのファイルを参照すべきかを判断するために使う。
keywords: [README, 目次, index, Datadog ナレッジ, 入口, 読み方, 入門編, リファレンス, 導入編, 応用編, AP1, 基準日]
sources:
  - https://docs.datadoghq.com/
  - https://www.datadoghq.com/pricing/
---

# Datadog ナレッジ 全体目次

## 概要

本ナレッジは、SaaS 型のオブザーバビリティ＋セキュリティプラットフォーム **Datadog** について、IT コンサルタント・アーキテクト・エンジニアが読み、かつ AI が読み込んで質問に回答するための Markdown ドキュメント群である。本 README は全体目次であり、**AI が最初に読む入口**である。

| 項目 | 内容 |
|---|---|
| 基準日（`last_verified`） | **2026-11-02**（Datadog は SaaS で名前付きリリースが無いため、情報取得日を基準とする） |
| 基準サイト | **AP1（日本）**。記述は全サイト共通を前提とし、サイト差異は本文中に「> **サイト差異:** …」で明記 |
| Agent の基準 | Datadog Agent **v7 系** |
| 料金の正本 | [03_導入編/pricing-by-product.md](03_導入編/pricing-by-product.md)（公式料金ページの定価、2026-11-02 時点） |
| 執筆規約 | [_CONVENTIONS.md](_CONVENTIONS.md) |
| 収録ファイル数 | 108 ファイル（入門編 7 / リファレンス 71 / 導入編 15 / 応用編 15。README・規約を除く） |

## ナレッジの目的

本ナレッジは、次の 3 つの目的のために作成している。

1. **正確な仕様の根拠を提供する**：製品機能・設定キー・制限値・デフォルト値・API・画面を、公式ドキュメントを一次情報として出典付きで整理する。
2. **導入・提案・運用の判断材料を提供する**：料金・エディション・契約・選定比較・導入方法論・設計・運用・コンプライアンスを、コンサルタント／PM／アーキテクトがそのまま使える形でまとめる。
3. **経験知を共有する**：ベストプラクティス、失敗パターン、コスト最適化、導入事例を、出典と確度ラベル（`【第三者情報】`・`【推定】`・`【経験則】`）付きで蓄積する。

## 読み方

### 入門者向け

Datadog を初めて学ぶ場合は、[01_入門編](#01_入門編) を次の順で読む。

1. [Datadogとは](01_入門編/what-is-datadog.md) → 2. [オブザーバビリティの基礎](01_入門編/observability-fundamentals.md) → 3. [製品ポートフォリオ全体像](01_入門編/product-map.md) → 4. [Datadogのアーキテクチャ概観](01_入門編/architecture-overview.md) → 5. [必須概念](01_入門編/core-concepts.md) → 6. [画面構成とナビゲーション](01_入門編/ui-navigation.md) → 7. [はじめてのDatadog](01_入門編/getting-started.md)

その後、関心のある製品を [02_リファレンス](#02_リファレンス) で確認する。

### コンサルタント・PM 向け

提案・選定・見積り・契約・導入計画では [03_導入編](#03_導入編) を中心に読む。

- 製品の全体像：[製品ポートフォリオ全体像](01_入門編/product-map.md)
- 料金：[料金体系の全体像](03_導入編/pricing-overview.md) → [製品別料金表（料金の正本）](03_導入編/pricing-by-product.md) → [課金計算の仕組み](03_導入編/billing-mechanics.md) → [コスト見積り手法](03_導入編/cost-estimation.md)
- 選定・契約：[製品選定と競合比較](03_導入編/selection-and-competitive-comparison.md)、[エディション・プラン](03_導入編/editions-and-plans.md)、[購入経路と契約](03_導入編/procurement-and-contracts.md)
- 導入計画：[導入方法論](03_導入編/implementation-methodology.md)、[セキュリティとコンプライアンス](03_導入編/security-and-compliance.md)
- 提案材料：[導入事例](04_応用編/case-studies.md)、[コスト最適化](04_応用編/cost-optimization.md)、[よくある失敗とアンチパターン](04_応用編/common-pitfalls.md)

### エンジニア・アーキテクト向け

設計・構築・運用では次の順で読む。

- 基本設計：[要件定義とアーキテクチャ設計](03_導入編/requirements-and-architecture-design.md)、[ネットワーク・接続要件](03_導入編/network-and-connectivity.md)、[Agent 展開設計](03_導入編/agent-rollout-design.md)、[運用設計](03_導入編/operations-design.md)
- 製品仕様（設定キー・制限値・デフォルト値）：[02_リファレンス](#02_リファレンス) の該当領域。共通基盤は `02_リファレンス/platform/` に集約している
- 実践知見：[04_応用編](#04_応用編)（タグ戦略、アラート設計、Monitoring as Code、Kubernetes 監視、APM・ログ・SLO・セキュリティ運用など）

### AI 向け

AI が本ナレッジを使って質問に回答する際は、次の手順と規則に従う。

1. **ファイルの選択**：まず本 README の各表の「サマリー」で該当ファイルを特定する。製品名から探す場合は [製品ポートフォリオ全体像](01_入門編/product-map.md)（旧称・改称履歴と詳細リファレンスへのリンクあり）を参照する。各ファイルのフロントマターの `summary` と `keywords`（旧称を含む）も検索に使える。
2. **根拠の優先順位**：仕様（制限値・設定キー・製品名）は **02_リファレンス** を、料金は **[pricing-by-product.md](03_導入編/pricing-by-product.md)** を正とする。ファイル間で記述が食い違う場合はこの 2 つを優先する。
3. **基準日を明示する**：回答には「2026-11-02 時点の情報」であることを示す。Datadog は継続的に変更されるため、最新情報は公式ドキュメント（https://docs.datadoghq.com/ ）での確認を促す。
4. **サイトを意識する**：基準は AP1（日本）。US1/EU1 等で機能提供・エンドポイント・価格が異なる箇所は本文の「サイト差異」を確認して回答する。サイト一覧は [Datadog Sites](02_リファレンス/platform/datadog-sites.md) を参照する。
5. **確度ラベルを引き継ぐ**：`【Preview】`・`【Limited Availability】`・`【第三者情報】`・`【推定】`・`【経験則】` が付いた記述を引用する場合は、ラベルを回答に残す。「公開情報では確認できず」と書かれた事項を推測で補わない。
6. **旧称に注意する**：質問が旧称（例：ASM、CSM、CWS、NPM、Service Catalog、LLM Observability、Case Management、Test Visibility、Quality Gates）で来た場合は、現名称のファイルを参照する。
7. **出典を示す**：各ファイルの本文中の `[出典](URL)` と末尾「## 参照元」の URL を回答の根拠として示す。

## 編の構成と役割

| 編 | 目的 | 主な読者 | ファイル数 |
|---|---|---|---|
| [01_入門編](#01_入門編) | Datadog を語るうえで必須の基本事項 | 入門者が最初に読む | 7 |
| [02_リファレンス](#02_リファレンス) | 製品仕様の詳細（機能、設定、制限値、API、画面）。各ファイルに「制限値・クォータ・デフォルト値」節、料金に関わる機能は「課金への影響」節を持つ | AI 回答の主たる根拠、エンジニア・アーキテクト | 71 |
| [03_導入編](#03_導入編) | 料金・エディション・契約、選定・比較、導入方法論、設計、運用、コンプライアンス | コンサルタント・PM・アーキテクト | 15 |
| [04_応用編](#04_応用編) | 導入・運用経験者の知見（ベストプラクティス、失敗パターン、コスト最適化、事例）。出典 URL 必須 | 経験者・コンサルタント | 15 |

共通ファイル：

| ファイル | 内容 |
|---|---|
| [_CONVENTIONS.md](_CONVENTIONS.md) | 執筆規約（基準日、サイト表記、フロントマター、本文の書き方、出典と確度ラベル、料金・画像の扱い、編ごとの役割、ファイル間の整合） |
画像は `assets/images/<ファイルのslug>/` に格納され、各ファイルから相対パスで参照されている。

## 全ファイル目次

### 01_入門編

Datadog の会社・製品思想、オブザーバビリティの基礎、製品全体像、アーキテクチャ、必須概念、画面操作、最初の導入手順を扱う。上から順に読むことを推奨する。

| ファイル | サマリー |
|---|---|
| [Datadogとは](01_入門編/what-is-datadog.md) | Datadog, Inc. の会社概要（創業者・創業年・上場・本社・日本法人）、統合オブザーバビリティ＋セキュリティプラットフォームという製品思想、SaaS 提供形態、主要ユースケース、Gartner Magic Quadrant 等による市場での位置づけを 2026-11-02 時点でまとめた入門ファイル。 |
| [オブザーバビリティの基礎](01_入門編/observability-fundamentals.md) | 監視（Monitoring）とオブザーバビリティ（Observability）の違い、メトリクス・ログ・トレース・イベント・プロファイルの5つのテレメトリシグナル、ゴールデンシグナル/RED/USE の各方法論、SLI/SLO/エラーバジェット/バーンレートの考え方を整理し、それぞれが Datadog のどの機能に対応するかを示す入門ファイル。 |
| [製品ポートフォリオ全体像](01_入門編/product-map.md) | Datadog の全製品（2026-11-02 時点）を Platform / Infrastructure / APM / Logs / DEM / Security / Software Delivery / Service Management / AI / Data の 10 区分で一覧化し、各製品の 1 行説明・課金単位・提供状況・旧称（改称履歴）・詳細リファレンスへのリンクをまとめた入門ファイル。「この機能は何という製品か」「旧名称の製品は今どれか」「どのファイルを読めばよいか」に答える。 |
| [Datadogのアーキテクチャ概観](01_入門編/architecture-overview.md) | Datadog がどのような構成（顧客環境側の Agent・SDK・クラウド連携、Intake、SaaS バックエンド、サイト）でテレメトリを収集→処理→保存→可視化→アラートしているかを、データの流れに沿って説明する。Agent 経路、Agentless（クラウド連携・API・Agentless Scanning）経路、OpenTelemetry 経路の違いと、通信方向・ポート・エンドポイント・既定の保持期間をまとめる。 |
| [必須概念](01_入門編/core-concepts.md) | Datadog を使ううえで最初に押さえるべき共通概念（組織、APIキー/アプリケーションキー、タグ、Unified Service Tagging、ホスト、サービス、メトリクス種別、ファセット、ログのインデックス、モニター、ダッシュボード、SLO）の定義・相互関係・主要なデフォルト値と制限値を、公式ドキュメントに基づいてまとめた入門ファイル。 |
| [画面構成とナビゲーション](01_入門編/ui-navigation.md) | Datadog の Web UI（左サイドバーのナビゲーションメニュー、主要画面、Cmd/Ctrl+K のクイック検索、時間セレクタ、Saved Views、テンプレート変数、Datadog Clipboard、個人設定）とモバイルアプリの画面構成・操作方法をまとめ、「どこで何ができるか」「どう操作するか」に答える。 |
| [はじめてのDatadog](01_入門編/getting-started.md) | Datadog を初めて使う人が、無料トライアル登録 → サイト（リージョン）選択 → Agent インストール → インテグレーション追加 → 最初のダッシュボードとモニター作成 → 学習リソース（Learning Center・ドキュメント・認定資格）の活用までを、2026-11-02 時点の公式情報に基づいて順に進めるための入門ガイド。 |

### 02_リファレンス

Datadog の製品仕様を領域（`domain`）別に整理したリファレンス。AI が回答する際の主たる根拠であり、機能・設定キー・制限値・デフォルト値・API・権限・サイト差異・課金への影響を記載する。領域区分は [製品ポートフォリオ全体像](01_入門編/product-map.md) の 10 区分に対応する。

#### Platform（共通基盤：Agent・インテグレーション・メトリクス・可視化・アラート・権限・API）

`02_リファレンス/platform/`（28 ファイル）

| ファイル | サマリー |
|---|---|
| [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) | Datadog の Organization（組織）、マルチオーガニゼーション（親子org・Organization Groups・Cross-Organization Visibility）、ユーザー／サービスアカウント管理、ログイン方式（パスワード・Google・SAML・MFA）、SAML/SSO と SCIM、RBAC（標準ロール・カスタムロール・権限一覧）、Teams、Granular Access Control（Restriction Policies）、ログのデータアクセス制御（Restriction Query）と Data Access Control（Restricted Datasets）、IP Allowlist 等の仕様・設定手順・制限値をまとめたリファレンス。 |
| [Agent 設定リファレンス](02_リファレンス/platform/agent-configuration.md) | Datadog Agent v7 の設定（datadog.yaml の主要キーとデフォルト値、環境変数への変換規則、conf.d のチェック設定、Secrets Management、プロキシ、ログレベル、ホスト名解決、設定の優先順位と実行時変更）を網羅したリファレンス。「この設定キーの既定値は？」「環境変数名は？」「設定ファイルはどこ？」に答える。 |
| [Datadog Agent](02_リファレンス/platform/agent.md) | Datadog Agent（v7 系）のアーキテクチャ（Collector、Forwarder、DogStatsD、Logs Agent、Trace Agent、Process Agent、System Probe、Security Agent、DDOT Collector）、対応 OS とバージョン上限、インストール方法（Linux / Windows / macOS / IoT / FIPS）、バージョン体系とアップグレード、Agent コマンド、status / flare / debug、IoT Agent、Agent v5 / v6 との差分、ポート・ファイルパス・既定値・制限値をまとめたリファレンス。 |
| [API とキー管理](02_リファレンス/platform/api-and-keys.md) | Datadog の認証情報（API キー、アプリケーションキー、クライアントトークン、Personal Access Token、Service Access Token、Workload Identity Federation）の仕様・権限・上限値と、REST API（v1/v2）の使い方、レート制限、公式クライアントライブラリ、CLI（Pup CLI・datadog-ci・Dogshell）をまとめたリファレンス。 |
| [Audit Trail（監査証跡）](02_リファレンス/platform/audit-trail.md) | Datadog Audit Trail の仕様リファレンス。監査対象イベント（全カテゴリ・クエリ）、有効化と権限、保持期間（3/7/15/30/90 日）、Audit Trail Explorer での検索・Notable Events・差分表示、AI エージェント/MCP 操作の追跡、アーカイブ、Custom Destinations への転送、Audit Trail Monitor によるアラート、API、サイト差異、制限値、課金（支出に対する %）をまとめる。 |
| [AWS Integration（AWS インテグレーション）](02_リファレンス/platform/aws-integration.md) | Datadog の AWS Integration（Amazon Web Services インテグレーション）について、接続方式（CloudFormation、Terraform、AWS Organizations StackSet、Control Tower、手動のロール委任／アクセスキー）、IAM ロールと External ID、サイト別の Datadog AWS アカウント ID、メトリクス収集（API ポーリングと CloudWatch Metric Streams）、ログ収集（Datadog Forwarder Lambda と Amazon Data Firehose）、リソース収集（SecurityAudit）、アラーム／イベント／タグ、Agent の自動インストール、API・Terraform の設定項目、制限値・デフォルト値、Datadog 側と AWS 側の課金への影響をまとめたリファレンス。 |
| [Azure Integration（Microsoft Azure インテグレーション）](02_リファレンス/platform/azure-integration.md) | Datadog の Azure Integration について、2 つの接続方式（App Registration 方式と Azure Native Integration）、認証方式（Secretless Auth と Client Secret）、必要な Azure / Datadog 権限、メトリクス収集（Azure Monitor のポーリング、フィルター、Application Insights のカスタムメトリクス）、ログ収集（自動ログ転送、Container App、Event Hub、Blob、Entra ID / Activity Log）、リソース収集、Agent 拡張機能、対応サービス、Terraform / API、制限値・デフォルト値、Datadog 側と Azure 側の課金への影響をまとめたリファレンス。 |
| [通知・コラボレーション連携](02_リファレンス/platform/collaboration-integrations.md) | Datadog のモニター通知・インシデント・Work Management（旧称 Case Management）と外部ツール（Slack、Microsoft Teams、Google Chat、Email、PagerDuty、Opsgenie / Jira Service Management Ops、Splunk On-Call（VictorOps）、ServiceNow、Jira、Linear、Webhooks、Atlassian Statuspage、Zoom、Amazon EventBridge）との連携方法・通知ハンドル構文・権限・サイト差異・制約と、Oracle Cloud Infrastructure（OCI）・Alibaba Cloud 等の AWS/Azure/Google Cloud 以外のクラウド連携の仕様をまとめたリファレンス。 |
| [Custom Metrics と DogStatsD](02_リファレンス/platform/custom-metrics-and-dogstatsd.md) | Datadog のカスタムメトリクスの定義と課金カウント方法（メトリクス名×タグ値の組み合わせ、メトリクス種別ごとの倍数、Metrics without Limits の ingested/indexed、Metric Name Pricing）、DogStatsD のプロトコル（データグラム形式 v1.1〜v1.6）・UDP/UDS 設定・クライアントライブラリ・Origin Detection・サンプリング・高スループット設定、HTTP API による送信、ログ／スパン／RUM からのメトリクス生成について答える。 |
| [Dashboards（ダッシュボード）](02_リファレンス/platform/dashboards.md) | Datadog Dashboards の種類（Dashboards / Timeboards / Screenboards）とレイアウト（12 列グリッド、高密度モード、グループ、タブ）、ウィジェット全一覧と共通設定、テンプレート変数と Saved Views、Powerpacks、共有（Public / Invite-only / Embed〔Basic・Secure〕、Shared Graphs、Widget Share URLs）、Scheduled Reports、バージョン履歴、権限、API/Terraform、制限値・デフォルト値をまとめたリファレンス。 |
| [Datadog Sites（サイト）](02_リファレンス/platform/datadog-sites.md) | Datadog の各サイト（US1/US3/US5/EU1/AP1/AP2/UK1/US1-FED/US2-FED）の URL・サイトパラメータ・ホスティング先クラウドと地域・主要エンドポイント・サイト別の機能提供差異・価格差・サイト移行の可否をまとめたリファレンス。 |
| [Event Management（イベント管理）](02_リファレンス/platform/event-management.md) | Datadog Event Management の仕様リファレンス。Events Explorer（検索・Facet・Analytics・Saved Views）、イベント送信方法（Events API v2/v1、Email、Custom Agent Check、DogStatsD、インテグレーション、Amazon SNS/EventBridge）、Event Pipelines と各 Processor、Event Correlation（Pattern-based / Intelligent）、Triage Inbox と Work Item、Maintenance Windows、イベント保持期間、Event Monitor、権限、制限値、課金単位をまとめる。 |
| [Fleet Automation と Remote Configuration](02_リファレンス/platform/fleet-automation.md) | Datadog Fleet Automation（Agent・OTel Collector の一覧と構成確認、Agent 設定・インテグレーション・カスタムログのリモート配布、リモートアップグレードとスケジュール、リモート flare、API/Terraform）と、その基盤である Remote Configuration（仕組み、対象製品、有効化の 3 階層、ステータス、ネットワーク、セキュリティ、権限、オプトアウト）の仕様・前提バージョン・制限値をまとめたリファレンス。「リモートアップグレードの前提は？」「Remote Configuration は安全か？」「どの設定を UI から変更できるか？」に答える。 |
| [Google Cloud Integration（Google Cloud インテグレーション）](02_リファレンス/platform/gcp-integration.md) | Datadog の Google Cloud Integration（旧称・通称：GCP Integration / Google Cloud Platform インテグレーション）について、認証方式（サービスアカウントの偽装（impersonation）と Datadog principal、Workload Identity Federation との関係）、組織／フォルダー／プロジェクト単位の設定手順と必要な API・IAM ロール、メトリクス収集とフィルター（名前空間・リージョン・ホスト／Cloud Run）、リソース収集とリソース変更収集（Cloud Asset Inventory + Pub/Sub）、Security Command Center、ログ収集（Pub/Sub + Dataflow テンプレート、Quick Start / Terraform / 手動、Pub/Sub Push は非推奨）、Private Service Connect、対応サービス一覧、API・Terraform、制限値・デフォルト値、Datadog 側と Google Cloud 側の課金への影響をまとめたリファレンス。 |
| [Integrations（インテグレーション）](02_リファレンス/platform/integrations.md) | Datadog の Integrations（インテグレーション）の種類（Agent ベース、認証（クローラー）ベース、ライブラリ）、Integrations 画面（カタログ）とステータス、Marketplace、Agent インテグレーションの設定・配布・パッケージ管理、カスタムチェックの作成、JMX（JMXFetch）、OpenMetrics / Prometheus、主要ミドルウェア（NGINX、Apache、MySQL、PostgreSQL、Redis、Kafka、Tomcat、RabbitMQ、MongoDB、Elasticsearch、HAProxy、IIS、SQL Server、Oracle など）の連携方法、制限値・デフォルト値、課金への影響（カスタムメトリクス扱いになるもの）をまとめたリファレンス。 |
| [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md) | コンテナ環境（Kubernetes、Docker、Amazon ECS / Fargate）に Datadog Agent を展開するための仕様リファレンス。Datadog Operator と Helm chart、Cluster Agent、Cluster Checks / Endpoint Checks / Cluster Checks Runner、Admission Controller、Autodiscovery（アノテーション、テンプレート変数、DatadogInstrumentation CRD）、Kubernetes State Metrics Core、EKS / AKS / GKE / OpenShift などディストリビューション別の設定、対応バージョン、ポート、既定値、課金単位をまとめる。 |
| [メトリクスクエリと関数](02_リファレンス/platform/metrics-query-and-functions.md) | Datadog のメトリクスクエリ構文（メトリクス名・スコープ・時間集約・空間集約）、rollup・補間・as_count/as_rate、Formulas（数式）と関数一覧（arithmetic, rollup, rate, smoothing, timeshift, rank, anomalies, outliers, forecast など）、ネストクエリ、各種制約・デフォルト値に答える。 |
| [Metrics（メトリクス）](02_リファレンス/platform/metrics.md) | Datadog の Metrics の仕様リファレンス。メトリクス種別（count / rate / gauge / histogram / distribution / set）、送信方法、保持期間と解像度、ロールアップ、Metrics Summary、Metrics without Limits、メトリクス単位、Historical Metrics Ingestion、および課金単位（カスタムメトリクス／Metric Name Pricing）について答える。 |
| [Monitors（モニター）](02_リファレンス/platform/monitors.md) | Datadog Monitors の全モニタータイプ（Metric / Anomaly / Outlier / Forecast / Host / Process / Log / APM / Composite / SLO / Change / Event / Watchdog ほか）、評価ウィンドウ・評価頻度・閾値・No Data・Recovery・Auto Resolve・Group Retention などの評価設定、Monitor Status 画面、Manage Monitors、Monitors API の主要オプション、タイプ別の制限値とデフォルト値をまとめたリファレンス。 |
| [Notebooks・DDSQL・Reference Tables](02_リファレンス/platform/notebooks-and-data-tools.md) | Datadog の分析系ツール群（Notebooks とその Analysis Features、DDSQL Editor / DDSQL、Reference Tables、Sheets、各種データエクスポート手段）の機能、設定項目、権限、制限値、サイト差異、課金への影響と、旧 Log Workspaces との関係をまとめたリファレンス。 |
| [通知と Downtime](02_リファレンス/platform/notifications-and-downtimes.md) | Datadog Monitor（モニター）の通知メッセージ（テンプレート変数・条件分岐・@メンション・eval 関数）、Priority、Renotify（再通知）、Monitor Notification Rules（通知ルール）によるタグベースのルーティング、Mute と Downtime（対象選択・グループスコープ構文・スケジュール・RRULE・終了時通知・権限）、クラウド VM の自動ミュート、Synthetic Monitoring の Downtime との違い、関連 API・制限値をまとめたリファレンス。 |
| [OpenTelemetry サポート](02_リファレンス/platform/opentelemetry.md) | Datadog が OpenTelemetry（OTel）データを受け取る4つの経路（DDOT Collector、OTLP Ingest in the Agent、アップストリームの OTel Collector（OTLP HTTP Exporter または Datadog Exporter/Connector）、Direct OTLP Ingest）の仕様、設定キー、制限値、機能互換性、セマンティック規約のマッピング、Datadog SDK と OTel API/SDK の互換、課金上の扱いをまとめたリファレンス。 |
| [Service Level Objectives（SLO）](02_リファレンス/platform/slo.md) | Datadog の Service Level Objectives（SLO）について、3 つの SLO タイプ（Metric-based / Monitor-based / Time Slice）の仕様と計算方法、エラーバジェット、Status Corrections、Error Budget アラートと Burn Rate アラート、SLO ウィジェット・SLO データソース・レポート、権限、API/Terraform、制限値・デフォルト値をまとめたリファレンス。 |
| [Software Catalog（旧 Service Catalog）](02_リファレンス/platform/software-catalog.md) | Datadog の Software Catalog（旧称 Service Catalog、現在のドキュメント上の表記は「Catalog」）と、それを中核とする Internal Developer Portal（IDP）の仕様をまとめる。エンティティモデル、エンティティ定義 YAML（schema v2/v2.1/v2.2/v3.0）、Scorecards・Campaigns、Self-Service Actions、Engineering Reports・Homepage 等の Developer Portal 機能、Datadog Teams との連携、API・権限・制限値・サイト差異に答える。 |
| [Tagging（タグ）](02_リファレンス/platform/tagging.md) | Datadog のタグについて、構文と文字・長さの制約、予約タグ（host / device / source / service / env / version / team）、Agent・コンテナ・インテグレーション・UI・API・DogStatsD による付与方法、Unified Service Tagging、タグ継承と優先順位、Monitor の Tag Policies、Cloud Cost Management の Tag Pipelines、タグに関する制限値と課金への影響をまとめたリファレンス。 |
| [Terraform と IaC（Infrastructure as Code）](02_リファレンス/platform/terraform-and-iac.md) | Datadog を IaC で管理する手段（Datadog Terraform Provider、Pulumi、AWS CloudFormation の Datadog リソース、Datadog Operator の CRD）を網羅するリファレンス。Provider の引数・環境変数・認証方式（API/アプリケーションキー、PAT/SAT、Workload Identity Federation、HCP Terraform Dynamic Provider Credentials）、主要リソース、v3→v4 の破壊的変更、既存リソースの取り込み（terraform import、UI の Export to Terraform、Terraformer）、運用上の注意、制限値・デフォルト値をまとめる。 |
| [Usage・Usage Attribution・Cost Visibility（利用量とコストの可視化）](02_リファレンス/platform/usage-and-cost-attribution.md) | Datadog 自身の利用量・コストを把握する機能群のリファレンス。Plan & Usage 画面（Usage、Bill Overview、Plan、Billing History、Usage Notifications）、月次集計方式、Estimated Usage Metrics（datadog.estimated_usage.*）の全メトリクス、Usage Attribution（タグ別利用量・Cost Attribution）、Cost Summary／Cost Chargebacks、Datadog Costs（CCM 上の日次コスト）、利用量アラートの作り方、Usage Metering API、権限、サイト差異、制限値をまとめる。 |
| [Watchdog](02_リファレンス/platform/watchdog.md) | Datadog の AI エンジン Watchdog（Watchdog Alerts、Root Cause Analysis、Impact Analysis、Watchdog Insights、Faulty Deployment Detection、Faulty Cloud & SaaS API Detection、Watchdog Explains、Watchdog Monitor）について、検知対象データ、必要な履歴期間、検知条件、画面、設定・無効化方法、権限、サイト差異、制限値、課金上の扱いをまとめたリファレンス。 |

#### Infrastructure（ホスト・コンテナ・サーバーレス・ネットワーク・DB・クラウドコスト）

`02_リファレンス/infrastructure/`（7 ファイル）

| ファイル | サマリー |
|---|---|
| [Cloud Cost Management（クラウドコスト管理）](02_リファレンス/infrastructure/cloud-cost-management.md) | Datadog Cloud Cost Management（CCM）の仕様リファレンス。AWS（CUR）・Azure（Cost Exports）・Google Cloud（BigQuery 詳細エクスポート）・Oracle（OCI FOCUS）・SaaS/AI・Custom Costs（FOCUS 形式）の取り込み要件と遅延・履歴、コストメトリクス名、FOCUS タグと Multisource Querying、タグの取得元と優先順位、Tag Pipelines、Custom Allocation Rules、コンテナコスト配賦、Cost Recommendations、Anomalies、Cost Monitor、Budgets・Forecasting、Commitment Programs、Real-Time Costs、Reports、Datadog Costs、権限、制限値、課金単位をまとめる。 |
| [Cloud Network Monitoring（旧称：Network Performance Monitoring / NPM）](02_リファレンス/infrastructure/cloud-network-monitoring.md) | Datadog Cloud Network Monitoring（CNM、旧称 NPM）について、eBPF / Windows ドライバーによるフロー収集の仕組みと OS・カーネル・Agent バージョン要件、Linux / Windows / Helm / Operator / Docker / ECS / Fargate での有効化手順、Network Analytics・Network Map・Network Health・DNS Monitoring・Network Path（Scheduled / Dynamic / Basic Dynamic Tests、AS View）の画面と設定キー、メトリクスとタグ、モニター、制限値・既定値、課金単位（ネットワークホスト、フロー、Network Path テスト）をまとめたリファレンス。 |
| [コンテナ・Kubernetes 監視](02_リファレンス/infrastructure/container-and-kubernetes-monitoring.md) | Datadog のコンテナ監視画面（Containers Explorer（旧称 Live Containers）、Container Images Explorer、Kubernetes Explorer（旧称 Orchestrator Explorer）、ECS Explorer、Kubernetes Resource Utilization、Kubernetes Autoscaling（DatadogPodAutoscaler）、Kubernetes Remediation）の機能・設定キー・検索構文・必要バージョン・データ保持期間・制限値と、コンテナ課金・Kubernetes Autoscaling 課金の単位をまとめたリファレンス。 |
| [Database Monitoring（データベースモニタリング）](02_リファレンス/infrastructure/database-monitoring.md) | Datadog Database Monitoring（DBM）について、対応データベース（PostgreSQL、MySQL、MariaDB、SQL Server、Oracle、MongoDB、Amazon DocumentDB、ClickHouse）とデプロイ形態ごとの対応バージョン・Agent 最低バージョン、セットアップ手順（DB 側パラメーター、監視ユーザー権限、Agent 設定、Kubernetes / ECS / Autodiscovery / IAM 認証）、Query Metrics・Query Samples・Explain Plan・Databases ページ・Schemas・Recommendations・Deadlock の画面と設定キー・既定値、APM 連携（DD_DBM_PROPAGATION_MODE）、DBM モニター、Bits AI 関連機能、制限値（ホストあたり 200 正規化クエリ、保持期間など）、課金単位（データベースホスト / 月）をまとめたリファレンス。 |
| [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) | Datadog Infrastructure Monitoring の中核機能（Host List（旧称：Infrastructure List）、Host Map、Live Processes、Resource Catalog）、課金上のホストの定義とホスト名決定ロジック、Agent の Infrastructure モード（Full / Basic / End User Device / None）、システムメトリクス、Agent なし（クラウドインテグレーションのみ）のホスト監視、Process Check / Live Process Monitor によるプロセス監視を、設定キー・既定値・制限値・課金単位とともにまとめたリファレンス。 |
| [Network Device Monitoring（ネットワークデバイス監視）](02_リファレンス/infrastructure/network-device-monitoring.md) | Datadog Network Device Monitoring（NDM）について、SNMP ポーリング（個別デバイス / Autodiscovery）、SNMP Traps、Syslog、Ping、VPN Monitoring、デバイスプロファイルと SNMP Profile Manager、NetFlow Monitoring（NetFlow v5/v9・IPFIX・sFlow）、Device Topology Map・Device Geomap、Summary Page・Device Health、Network Configuration Management（NCM）とロールバック、High Availability、API、設定キーと既定値、制限値、課金単位（デバイス数・Wireless AP・NetFlow レコード数）をまとめたリファレンス。 |
| [Serverless Monitoring（サーバーレス監視）](02_リファレンス/infrastructure/serverless.md) | Datadog Serverless Monitoring の対応範囲（AWS Lambda / AWS Step Functions / Azure App Service・Azure Functions・Azure Container Apps / Google Cloud Run）と、Lambda Extension・Lambda Library（Layer）・serverless-init・Serverless Compatibility Layer による計装方式、設定環境変数、Enhanced Metrics、トレース、ログ、制限値、課金単位（アクティブ関数・アクティブアプリインスタンス・トレース対象呼び出し数）をまとめたリファレンス。 |

#### APM（アプリケーション性能監視・プロファイリング・エラー追跡）

`02_リファレンス/apm/`（8 ファイル）

| ファイル | サマリー |
|---|---|
| [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) | Datadog APM の基本概念（Trace / Span / Service / Resource / Operation、Service Entry Span、Primary Tag）と、トレースデータのライフサイクル（インジェスト＝サンプリング、Retention Filters によるインデックス、Intelligent Retention、Trace Metrics、Span-based Metrics）および各段階の設定キー・デフォルト値・保持期間・制限値・課金単位を網羅したリファレンス。 |
| [APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) | Datadog APM でアプリケーションを計装（インスツルメンテーション）する方法をまとめたリファレンス。Single Step Instrumentation（SSI）の対応環境、導入手順、設定キー、言語別 Datadog SDK（旧称：トレーサー／トレーシングライブラリ。Java、Python、Node.js、Go、.NET、Ruby、PHP、C++、Rust）の対応バージョンと導入方法、自動計装と手動（カスタム）計装、ログとトレースの相関、主なライブラリ設定とデフォルト値、トレースコンテキスト伝播、OpenTelemetry API による計装を扱う。 |
| [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) | Datadog APM の分析画面（Software Catalog の Service Page・Resource Page、Service Map、Trace Explorer と Trace View、Trace Queries、Deployment Tracking と Faulty Deployment Detection、Endpoints リストによるエンドポイント観測、Span-based Metrics）について、画面構成、検索構文、可視化の種類、設定項目、デフォルト値、制限値、権限、課金への影響をまとめたリファレンス。 |
| [Continuous Profiler（継続的プロファイラー）](02_リファレンス/apm/continuous-profiler.md) | Datadog Continuous Profiler の仕組み、対応言語ごとのプロファイル種別と要件・設定キー、オーバーヘッドとその抑制策、Profile Comparison、Trace to Profiling 連携（旧称・通称 Code Hotspots）と Endpoint Profiling、Timeline、Automated Analysis、データ保持期間、課金単位（APM Enterprise／単体 Profiler／Profiled Container／Fargate）を網羅したリファレンス。 |
| [Data Streams Monitoring](02_リファレンス/apm/data-streams-monitoring.md) | Datadog Data Streams Monitoring（DSM）の仕組み、対応キュー（Kafka・RabbitMQ・SQS・SNS・Kinesis・Google Pub/Sub・IBM MQ・Azure Service Bus・BullMQ）と言語別のトレーサー最低バージョン、エンドツーエンドレイテンシ、Consumer Lag、スループット、Schema 追跡、Dead Letter Queue、Kafka Console、メトリクス、制限値、課金単位をまとめたリファレンス。 |
| [Dynamic Instrumentation と Live Debugger](02_リファレンス/apm/dynamic-instrumentation.md) | Datadog の Dynamic Instrumentation（動的スパン・スパンタグ・メトリクスの追加）と Live Debugger（自動失効する logpoint によるログ・変数スナップショット取得、Debug Session、Bits Live Debugger）について、対応言語と SDK／Agent の最低バージョン、有効化手順と環境変数、Expression Language、Sensitive Data のマスキング（識別子・型・Strict／Targeted モード・Sensitive Data Scanner）、RBAC 権限、レート制限・キャプチャ制限・サイト差異、課金への影響をまとめたリファレンス。 |
| [Error Tracking](02_リファレンス/apm/error-tracking.md) | Datadog Error Tracking が APM・RUM・Logs（および Standalone の Backend/Frontend SDK、Sentry SDK）から収集したエラーを Issue に集約する仕組み（取り込み条件、グルーピング／fingerprint、Issue 状態と自動解決・Regression、Suspected Causes、Suspect Commits、チーム所有、Exception Replay、Bits AI 調査、Monitor、チケット連携、API、RBAC）と、Rules・Rate Limit・Dynamic Sampling によるデータ量制御、保持期間・制限値、Error Tracking 単体利用の構成と課金単位をまとめたリファレンス。 |
| [Universal Service Monitoring（USM）](02_リファレンス/apm/universal-service-monitoring.md) | Datadog Universal Service Monitoring（USM）が eBPF でコード変更なしにサービスの RED メトリクスを得る仕組み、対応プラットフォーム・プロトコル（GA / Preview）、Agent・カーネル要件、デプロイ方式別の有効化設定、universal.http.* メトリクス、APM との違い、課金（USM ホスト単価と APM ホストへの同梱）を答える。 |

#### Logs（ログ収集・処理・検索・保持・パイプライン）

`02_リファレンス/logs/`（5 ファイル）

| ファイル | サマリー |
|---|---|
| [ログ収集（Log Collection）](02_リファレンス/logs/log-collection.md) | Datadog Log Management へのログ収集方法（Agent によるファイル/journald/コンテナ/Windows Event/TCP・UDP 収集、AWS・Azure・Google Cloud からの転送、HTTP API）と、マルチライン集約、Agent 側フィルタ・スクラビング、送信トランスポート、サイズ・属性数・タイムスタンプなどの制限値をまとめたリファレンス。 |
| [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) | Datadog Log Management の Indexes（インデックス）、Exclusion Filters、Daily Quota、Standard / Flex Logs（Flex Starter・Flex Frozen を含む）の保持期間、Log Archives、Archive Search、Rehydration、Log Forwarding、BYOC Logs（旧称：CloudPrem）の仕様・制限値・権限・課金への影響をまとめたリファレンス。 |
| [Log Pipelines と処理](02_リファレンス/logs/log-pipelines-and-processing.md) | Datadog Log Management の取り込み時処理（JSON Preprocessing、Pipeline、Nested Pipeline、Integration Pipeline、21 種の Processor、Grok 構文、予約属性、Standard Attributes と Aliasing、Auto-Processing、Pipeline Scanner）について、設定項目、API ペイロード、書き込み優先順位、制限値、権限、課金上の扱いを網羅したリファレンス。 |
| [ログ検索と分析](02_リファレンス/logs/log-search-and-analytics.md) | Datadog Log Management の Log Explorer における検索構文、時間範囲、Facets / Measures、Calculated Fields、Advanced Search、Log Analytics（Fields / Patterns / Transactions と各可視化）、Live Tail、Watchdog Insights、Notebooks Analysis Features（旧称：Log Workspaces）、Export、Saved Views、Generate Metrics（ログベースメトリクス）、Log Monitor、検索 API について、仕様・設定項目・制限値・権限・課金への影響をまとめたリファレンス。 |
| [Observability Pipelines](02_リファレンス/logs/observability-pipelines.md) | Datadog Observability Pipelines（OP）の Worker アーキテクチャ、Sources / Processors / Destinations の一覧と主要設定、テンプレート（ログボリューム制御・分割・アーカイブ・機微データ除去など）、Packs・Live Capture・Pipeline Simulation、デプロイ方式（Docker / Kubernetes / Linux / CloudFormation / ECS Fargate）、バッファリング、サイジング、制限値、課金単位をまとめたリファレンス。 |

#### DEM（Digital Experience Monitoring：RUM・Session Replay・Synthetic）

`02_リファレンス/dem/`（4 ファイル）

| ファイル | サマリー |
|---|---|
| [RUM（ブラウザ）](02_リファレンス/dem/rum-browser.md) | Datadog Real User Monitoring（RUM）の Browser SDK について、導入方法（npm / CDN 非同期・同期 / サーバーサイド自動インスツルメンテーション）、初期化パラメータとデフォルト値、収集イベント（Session・View・Action・Resource・Error・Long Task・Vital）と主要属性、Core Web Vitals、サンプリング、RUM without Limits（Retention Filters・Retention Quotas・rum.measure.* メトリクス）、APM 連携（allowedTracingUrls・traceContextInjection）、プライバシー設定（defaultPrivacyLevel・IP/位置情報・同意管理・プロキシ）、保持期間、技術的制限値、課金（RUM Measure / RUM Investigate / Session Replay）をまとめたリファレンス。 |
| [RUM（モバイル）](02_リファレンス/dem/rum-mobile.md) | Datadog Real User Monitoring（RUM）のモバイル SDK（Android / iOS・Apple 各 OS / React Native / Flutter / Unity / Kotlin Multiplatform）について、対応 OS・バージョン、導入手順、初期化パラメータとデフォルト値、収集イベントと主要属性、クラッシュレポート（ANR・App Hang・Watchdog Termination・NDK）とシンボルファイル（mapping / dSYM / ソースマップ）のアップロード、Mobile Vitals とアプリ起動計測（TTID / TTFD）、オフライン時のバッファリングと送信制御、トラッキング同意、WebView 連携、制限値、課金（RUM Measure / RUM Investigate / Session Replay / Error Tracking）をまとめたリファレンス。 |
| [Session Replay と Product Analytics](02_リファレンス/dem/session-replay-and-product-analytics.md) | Datadog Session Replay（ブラウザ／モバイルの録画再生）と Product Analytics（Pathways・Funnel・Retention・Analytics Explorer・Segments・Heatmaps）について、仕組み、設定パラメータとデフォルト値、プライバシーマスキング、保持期間と Extended Retention、Heatmaps、各チャートの仕様、RUM との関係、サイト差異、制限値、課金単位をまとめたリファレンス。 |
| [Synthetic Monitoring（外形監視・合成監視）](02_リファレンス/dem/synthetic-monitoring.md) | Datadog Synthetic Monitoring の API テスト（HTTP/SSL/DNS/TCP/UDP/ICMP/WebSocket/gRPC）、Multistep API テスト、Browser テスト、Mobile App Testing、Private Locations、マネージドロケーション一覧、Continuous Testing の仕様・設定項目・制限値・課金単位をまとめたリファレンス。 |

#### Security（SIEM・クラウド/ワークロード/アプリ/コードセキュリティ）

`02_リファレンス/security/`（7 ファイル）

| ファイル | サマリー |
|---|---|
| [App and API Protection（旧 ASM）](02_リファレンス/security/app-and-api-protection.md) | Datadog App and API Protection（AAP、旧称 Application Security Management / ASM）の仕組み（APM トレーサー内蔵の In-App WAF）、脅威検知（Security Signals・検知ルール・Trace Qualification・Threat Intelligence）、防御（In-App WAF ポリシー・Exploit Prevention（RASP）・IP／ユーザーのブロック・Denylist／Passlist・エッジ WAF 連携）、Account Takeover 対策、API Posture（API Inventory・API Findings・Sensitive Data・Endpoint Scanning・OWASP API Top 10 Compliance）、対応言語・プロキシ・サーバーレスとバージョン要件、設定用環境変数、API・Terraform・権限、制限値・既定値、サイト差異、課金単位をまとめたリファレンス。 |
| [Cloud Security（旧 CSM）](02_リファレンス/security/cloud-security.md) | Datadog Cloud Security（旧称 Cloud Security Management / CSM）のリファレンス。Misconfigurations（CSPM・KSPM）、Identity Risks（CIEM）、Vulnerabilities（ホスト・コンテナイメージ・サーバーレス）、Agentless Scanning、コンプライアンスフレームワーク、重大度スコアと Runtime Prioritization Engine、Security Inbox との関係、セットアップ方法（クラウド連携・Agent・Agentless・CI/CD）、API、制限値、課金単位（CSM Pro / CSM Enterprise）をまとめる。 |
| [Cloud SIEM](02_リファレンス/security/cloud-siem.md) | Datadog Cloud SIEM の製品形態（Standalone 12か月/15か月・Add-on with Flex Logs・Legacy）、ログソースと Content Packs / Entity Packs、OCSF 正規化、Security Filters とインデックスフィルタ、脅威インテリジェンス（BYOTI・IOC Explorer）、検知ルール（OOTB / カスタム、7 種の検知方式、リアルタイム / スケジュール / Historical Job、SQL・Datasets）、Suppressions・Dynamic Severity、Security Signals のトリアージ、Investigator、Entity Risks（旧称 Risk Insights）、Bits Security Analyst、SOAR（Workflow Automation）連携、API・Terraform・権限、制限値・既定値、課金単位をまとめたリファレンス。 |
| [Code Security](02_リファレンス/security/code-security.md) | Datadog Code Security（SAST・SCA・IAST・Secret Scanning・IaC Security・Supply Chain Firewall・MCP Server）の機能、対応言語・対応ファイル、セットアップ方式（Datadog ホスト型スキャン / CI / IDE / Git hook）、設定ファイル code-security.datadog.yaml、PR コメントと PR Gates、制限値・デフォルト値、課金単位をまとめたリファレンス。 |
| [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md) | Datadog Security（セキュリティ製品群）の全体像を扱うリファレンス。Cloud SIEM・Cloud Security・Workload Protection・App and API Protection・Code Security・AI Guard・Sensitive Data Scanner の役割と関係、共通データモデル（Security Signals と Findings）、Detection Rules の共通概念（ルール種別・検知方式・オプション値・管理・廃止）、Suppressions・Dynamic Severity・Automation Pipelines・Security Inbox・通知・Threat Intelligence・権限、改称履歴、保持期間と制限値、課金単位をまとめる。 |
| [Sensitive Data Scanner](02_リファレンス/security/sensitive-data-scanner.md) | Datadog Sensitive Data Scanner（SDS）の対象データ（Logs・APM スパン・RUM イベント・Event Management のイベント・Agent Observability・Cloud Storage・コードリポジトリ）、Scanning Group と Scanning Rule（ライブラリルール約 500 本・カスタム正規表現ルール）、キーワード・抑制・対象属性、マスキング動作（Redact / Partially redact / Hash / Mask）、Findings・アラート・ダッシュボード、Amazon S3 の Agentless スキャン、権限、API/Terraform、制限値、課金単位（スキャン GB、Detect プラン）をまとめたリファレンス。 |
| [Workload Protection（旧 CWS）](02_リファレンス/security/workload-protection.md) | Datadog Workload Protection（旧称 Cloud Workload Security / CWS、CSM Threats）のリファレンス。eBPF・ptrace・Windows ドライバによるランタイム検知の仕組み、Agent Rules（SECL）・Policies・Detection Rules・Finding Rules・Content Packs・Threat Intelligence、自動応答（Automated response、旧 Active Protection）と手動応答、対応 OS・カーネル・クラウド環境、Agent 設定キー、Coverage、API・Terraform、制限値・保持期間、課金単位（ホスト・コンテナ・Fargate タスク）をまとめる。 |

#### Software Delivery（CI・テスト・DORA・PR Gates）

`02_リファレンス/software-delivery/`（3 ファイル）

| ファイル | サマリー |
|---|---|
| [CI Visibility（CI Pipeline Visibility）](02_リファレンス/software-delivery/ci-visibility.md) | Datadog CI Visibility（CI Pipeline Visibility）の対応 CI プロバイダと機能対応表、プロバイダ別セットアップ手順、パイプラインのトレース（データモデル・実行タイプ・カスタムコマンド・カスタムタグ/メジャー）、画面（Pipelines / Executions / CI/CD Optimization）、メトリクスとモニター、Logs Analysis・自動ジョブリトライ・クリティカルパス、インジェスト制御、権限、制限値・デフォルト値、課金単位（コミッター・スパン）をまとめたリファレンス。 |
| [DORA Metrics・PR Gates（旧称：Quality Gates）・Code Coverage](02_リファレンス/software-delivery/software-delivery-insights.md) | Datadog Software Delivery のうち、DORA Metrics（Delivery Performance）、PR Gates（旧称：Quality Gates）、Code Coverage、CD Visibility、Deployment Gates の仕様（データソース、計算方法、設定項目、CLI/API、権限、制限値、課金単位）をまとめたリファレンス。 |
| [Test Optimization（旧 Test Visibility）](02_リファレンス/software-delivery/test-optimization.md) | Datadog Test Optimization（旧称 Test Visibility）の仕様リファレンス。テスト実行の可視化（Explorer・Test Health）、Flaky Test Management（Quarantine/Disable/Attempt to Fix）、Early Flake Detection、Auto Test Retries、Test Impact Analysis（旧称 Intelligent Test Runner）、対応言語・フレームワーク・最低バージョン、環境変数、権限、制限値、課金単位に答える。 |

#### Service Management（インシデント・オンコール・自動化）

`02_リファレンス/service-management/`（5 ファイル）

| ファイル | サマリー |
|---|---|
| [App Builder](02_リファレンス/service-management/app-builder.md) | Datadog App Builder（ローコードの社内向け運用アプリ作成ツール）の仕様をまとめる。アプリの作り方、コンポーネント、クエリ、JavaScript 式、イベント、入力パラメーター、ダッシュボードへの埋め込み、権限と実行 ID、Datastores・Forms・Datadog Apps（アプリをコードで作る版）、API・Terraform、制限値、課金単位（公開済みアプリ数）に答える。 |
| [Case Management（現名称：Work Management）](02_リファレンス/service-management/case-management.md) | Datadog Work Management（旧称：Case Management）の作業項目（Work Item／Case）の作成方法（手動・自動）、プロジェクト、ステータス・優先度・属性、カスタマイズ、権限、Automation Rules、承認、通知、On-Call/Incident 連携、Jira/ServiceNow/Linear 同期、API・MCP、制限値と課金への影響をまとめたリファレンス。 |
| [Incident Management（インシデント管理）](02_リファレンス/service-management/incident-management.md) | Datadog Incident Management の宣言方法、属性（Severity・Status・Property Fields・Responder Roles）、タイムライン、通知ルール、オートメーション、ポストモーテムとフォローアップ、Slack/Microsoft Teams 等の連携、Status Pages、分析、権限、制限値、シート課金を網羅したリファレンス。 |
| [On-Call（オンコール）](02_リファレンス/service-management/on-call.md) | Datadog On-Call の構成要素（Team・Routing Rules・Escalation Policy・Schedule・Page）、ページング手段（電話・SMS・モバイルプッシュ・メール・Live Call Routing）、通知設定、Handover Automation、外部ツール連携・移行、API/Terraform、権限、制限値、シート課金を網羅したリファレンス。 |
| [Workflow Automation（ワークフロー自動化）](02_リファレンス/service-management/workflow-automation.md) | Datadog Workflow Automation のトリガー、アクションカタログ、ロジック/データ変換アクション、接続（Connections）、Private Action Runner と Execution Policies、Blueprints、権限・実行 ID、監視、API/MCP、制限値、課金単位（100 実行単位）を網羅したリファレンス。 |

#### AI（Bits AI・Agent Observability）

`02_リファレンス/ai/`（2 ファイル）

| ファイル | サマリー |
|---|---|
| [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) | Datadog の生成 AI 機能群 Bits AI（Bits Chat、Bits Investigation（旧 Bits AI SRE）、Bits Code（旧 Bits AI Dev Agent）、Bits Security Analyst、Bits Detection、Bits Remediation、Bits Data Analysis、Skills Library、Bits Agent Builder）と Datadog MCP Server、自然言語クエリ（NLQ）の機能・設定・権限・制限値・データの取り扱い・AI Credits による課金を網羅したリファレンス。 |
| [LLM Observability（現名称：Agent Observability）](02_リファレンス/ai/llm-observability.md) | Datadog の LLM/AI エージェント向け可観測性製品 Agent Observability（旧称 LLM Observability）について、SDK と自動計装、span kind によるトレース構造、Evaluations（評価）、Datasets/Experiments/Playground、プロンプトインジェクション等のセキュリティ評価、コスト追跡、データ保持、課金（LLM span 課金）を網羅的に整理する。 |

#### Data（データオブザーバビリティ・データジョブ監視）

`02_リファレンス/data/`（2 ファイル）

| ファイル | サマリー |
|---|---|
| [Data Jobs Monitoring（現名称：Data Observability: Jobs Monitoring）](02_リファレンス/data/data-jobs-monitoring.md) | Datadog の Data Jobs Monitoring（現名称 Data Observability: Jobs Monitoring）の対応範囲、Databricks・Amazon EMR・Dataproc・Kubernetes 上の Spark・Airflow・dbt・AWS Glue・Azure Data Factory のセットアップ設定、画面と分析機能、制限値、課金単位を網羅するリファレンス。 |
| [Data Observability（データオブザーバビリティ）](02_リファレンス/data/data-observability.md) | Datadog Data Observability（Quality Monitoring・Data Catalog・Lineage・CI/CD・Data Observability Monitor）の機能、対応データソース（Snowflake / Databricks / BigQuery / Redshift ほか）、セットアップ要件、制限値、ウェアハウス側コスト、課金単位（Monitored Table）を網羅するリファレンス。 |

### 03_導入編

Datadog の料金・エディション・契約、製品選定と競合比較、導入方法論、要件定義・設計、ネットワーク、運用、セキュリティとコンプライアンス、サポートと教育を扱う。料金の数値は [製品別料金表（料金の正本）](03_導入編/pricing-by-product.md) を正とする。

| ファイル | サマリー |
|---|---|
| [Agent 展開設計](03_導入編/agent-rollout-design.md) | Datadog Agent を数十〜数万台規模に展開するための設計指針。展開方式（インストールスクリプト／MSI、Ansible・Chef・Puppet・SaltStack、Helm・Datadog Operator、Single Step Instrumentation）の選定、バージョン固定と更新方針、構成管理ツールと Fleet Automation の責任分界、段階展開（リング展開）とロールバックの設計に答える。 |
| [課金計算の仕組み](03_導入編/billing-mechanics.md) | Datadog の請求額がどのように計算されるか（ホスト数の 99 パーセンタイル / ハイウォーターマーク、コンテナとカスタムメトリクスの同梱枠のプール計算、ログの Ingest / Index の二段階課金、APM の Ingested / Indexed Span、コミットと超過のオンデマンド単価、請求画面と請求書の読み方、よくある誤解）を数値例付きで説明する。 |
| [コスト見積り手法](03_導入編/cost-estimation.md) | Datadog の月額費用を導入前に見積もる手順を、必要な入力情報（ホスト数、コンテナ数、ログ量、スパン量、カスタムメトリクス数、RUM セッション、Synthetic 実行数など）の洗い出し、製品別の計算式、トライアルでの実測方法（datadog.estimated_usage.* メトリクス）、小・中・大規模の試算例（【推定】）、見積りの落とし穴の順に解説する。単価は pricing-by-product.md（料金の正本）の AP1 / US 定価を使用。 |
| [エディション・プラン](03_導入編/editions-and-plans.md) | Datadog の「エディション（プラン/ティア）」の考え方と、Infrastructure の Free tier / Basic / Pro / Enterprise、DevSecOps Pro / Enterprise バンドル、APM・Cloud Security・Code Security・Cloud Cost Management・Agent Observability・RUM・Incident Response など製品別ティアの機能差、無料トライアル、Datadog for Startups、Student Developer Program、政府機関向け（Datadog for Government / US1-FED）をまとめ、エディション別の機能比較表を提供する。 |
| [導入方法論](03_導入編/implementation-methodology.md) | Datadog 導入プロジェクトをどのフェーズ（計画・要件定義・設計・PoC・構築・展開・定着）で進め、どの体制・WBS・成果物で管理し、PoC を何の観点で評価するかを、公式 Administrator's Guide（Plan / Build / Run）と実務事例を基に整理する。 |
| [他製品からの移行](03_導入編/migration-from-other-tools.md) | Zabbix・Nagios・Prometheus/Grafana・New Relic・Amazon CloudWatch・Splunk などから Datadog へ移行する際の進め方（棚卸し→データ収集の置き換え→ダッシュボード/アラート変換→並行稼働→切替）、製品別の対応表、並行稼働に使える公式機能（Agent の Dual Shipping、Observability Pipelines、各種インテグレーション）、移行ツール（Crest Data の Marketplace アプリ、pySigma、Terraformer 等）とその制約を整理する。 |
| [ネットワーク・接続要件](03_導入編/network-and-connectivity.md) | Datadog Agent・SDK・Synthetics Private Location などが Datadog SaaS へ通信するための送信先エンドポイント、ポート、IP レンジ（ip-ranges）、プロキシ構成、AWS PrivateLink / Azure Private Link / GCP Private Service Connect による閉域接続、ネットワーク断時のバッファリング、帯域見積りの方法をまとめる。ファイアウォール申請・閉域設計の根拠資料として使う。 |
| [運用設計](03_導入編/operations-design.md) | Datadog を本番運用するための運用設計をまとめる。運用体制（プラットフォームチームの責務・役割・RACI・社内申請窓口）、アラート運用フロー（Monitor → Notification Rules → On-Call → Incident → 振り返り）、ユーザー・権限・キーの運用（入退社・異動、ロール保守、ローテーション周期）、Agent／インテグレーションの保守（更新方針、ヘルス監視、クラウド連携の権限更新）、利用量とコストの監視、ガバナンス（Governance Console・Safety Center・Tag Policies・Audit Trail）、定期レビューのカレンダーとチェックリストに答える。 |
| [製品別料金表（料金の正本）](03_導入編/pricing-by-product.md) | datadoghq.com/pricing および /pricing/list/ に掲載された全製品の定価（年契約・月契約・オンデマンド、各エディション）、課金単位、同梱の無料枠（コンテナ、カスタムメトリクス、スパン等の allotment）を、US/EU1 と AP1（日本）の両価格で網羅した料金の正本。サイト別価格係数と US1-FED の非提供製品も記載。 |
| [料金体系の全体像](03_導入編/pricing-overview.md) | Datadog の料金がどの単位（ホスト・量・イベント・シート・コミッター等）で課金されるか、年契約・月契約・オンデマンドの違い、無料枠と試用、主要製品の課金単位の早見表をまとめ、詳細な料金・計算方法・見積りの各ファイルへ案内する。 |
| [購入経路と契約](03_導入編/procurement-and-contracts.md) | Datadog を購入する経路（直販、AWS / Azure / Google Cloud Marketplace、国内販売パートナー・CPPO）と、契約形態（年契約・月契約・オンデマンド・従量）、コミットと超過、自動更新と値上げ上限、支払い条件、サポートプラン、解約時のデータの扱いを、MSA・Support Terms・DPA 等の公式文書に基づいて整理する。 |
| [要件定義とアーキテクチャ設計](03_導入編/requirements-and-architecture-design.md) | Datadog 導入時の要件定義と基本設計で決める事項（サイト選択、単一 org / マルチ org の組織構成、タグ設計、データフロー設計、保持期間設計、RBAC 設計、命名規則）について、判断基準・公式推奨・制約値と、そのまま使える設計書テンプレートをまとめた導入ガイド。 |
| [セキュリティとコンプライアンス](03_導入編/security-and-compliance.md) | Datadog 導入時のセキュリティ審査・コンプライアンス確認に必要な事項（取得認証 SOC 2 / ISO 27001・27017・27018・27701・42001 / PCI DSS / HIPAA / FedRAMP / ISMAP の状況、データ保存場所、通信・保存時の暗号化、PII 対策、データ削除と契約終了後の削除、サブプロセッサ、DPA、日本の個人情報保護法・電気通信事業法などの観点）を、一次情報の出典付きでまとめた導入ガイド。 |
| [製品選定と競合比較](03_導入編/selection-and-competitive-comparison.md) | オブザーバビリティ製品の選定基準と、Datadog を New Relic・Dynatrace・Grafana Cloud（LGTM）・Elastic Observability・Splunk Observability Cloud・AWS CloudWatch・Azure Monitor・Google Cloud Observability・Sumo Logic と比較（機能・価格モデル・公開定価・日本リージョン・強み弱み）し、Datadog が向くケース／向かないケースを整理する。 |
| [サポートと教育](03_導入編/support-and-training.md) | Datadog のサポートプラン（Free / Standard / Premier）の応答時間・チャネル・料金、問い合わせ方法（チケット・チャット・Agent flare）、日本語サポートの提供時間、TAM・Technical Enablement 等の有償サービス、Learning Center・認定資格（Datadog Fundamentals 等）・コミュニティをまとめ、導入プロジェクトでのサポート・教育計画の根拠を提供する。 |

### 04_応用編

Datadog の導入・運用経験に基づく実践知見（設計のベストプラクティス、失敗パターン、コスト最適化、大規模運用、組織定着、導入事例）を扱う。公式情報以外に依拠する記述には確度ラベルと出典の公開日を付けている。

| ファイル | サマリー |
|---|---|
| [アラート設計とノイズ削減](04_応用編/alert-design-and-noise-reduction.md) | Datadog Monitors でアラート疲れを防ぐための設計原則（症状ベース、緊急度の3段階）、評価ウィンドウ・回復しきい値・通知グルーピング等のノイズ削減設定、Composite / Anomaly / Outlier / Forecast / Watchdog の使い分け、Notification Rules・条件付き変数・On-Call による通知ルーティング、棚卸し運用と失敗例をまとめる。 |
| [APM 運用の実践](04_応用編/apm-practices.md) | Datadog APM を本番運用する際の実践知見として、計装の段階的な進め方、サンプリングとリテンションの戦略、サービス命名（Integration override 削除・Inferred Services・Service Remapping Rules）、トレースとログの相関、コストと可視性のバランスの取り方を、公式情報と公開事例に基づいて整理する。 |
| [導入事例](04_応用編/case-studies.md) | Datadog の国内外の公開導入事例（企業名・業種・規模・課題・構成・利用製品・定量効果）を出典付きで整理し、業種別・目的別の傾向、選定理由、効果指標、コスト最適化の第三者事例をまとめる。提案・選定・社内説明で「どの企業が何のために Datadog をどう使い、どんな効果を出したか」に答えるためのファイル。 |
| [よくある失敗とアンチパターン](04_応用編/common-pitfalls.md) | Datadog の導入・運用で繰り返し起きる失敗パターン（コスト急増、タグ不統一、アラート過多、権限設計ミス、Agent バージョン放置、IaC・ダッシュボード・サイト選定などの運用プロセスの失敗）を、症状・原因・仕組み・検知方法・対策・課金への影響の形で整理したカタログ。各パターンの公式根拠と、検知に使う推定使用量メトリクス、予防のためのガードレールとチェックリストをまとめる。 |
| [コスト最適化](04_応用編/cost-optimization.md) | Datadog の請求額を可視性を落とさずに下げるための実践知。ログ（Agent 側フィルタ、Observability Pipelines、除外フィルタ、Daily quota、Flex Logs、アーカイブ / Archive Search）、カスタムメトリクス（タグ設計、Distribution のパーセンタイル、Metrics without Limits、Metric Name pricing）、APM（取り込みサンプリング、保持フィルタ、Single Span）、ホスト / コンテナ（99 パーセンタイル課金、クラウド連携フィルタ、Container Discovery Management、プリペイド）、RUM（RUM without Limits、保持フィルタ、保持クォータ）、Synthetic、コミット（契約）最適化、使用量の可視化と FinOps 運用を、試算例と出典付きで整理する。 |
| [ダッシュボード設計の実践](04_応用編/dashboard-design-practices.md) | Datadog の Dashboards（ダッシュボード）を「経営向け・サービス運用向け・調査向け」の用途別にどう設計し、階層化・テンプレート変数・Powerpack・権限制御・棚卸しでどう運用し続けるかを、公式ドキュメントと実務知見に基づいてまとめる。 |
| [Kubernetes 監視の実践](04_応用編/kubernetes-monitoring-practices.md) | Datadog で Kubernetes を本番監視する際の実践知見として、Agent 構成（Node Agent・Cluster Agent・Cluster Checks Runner・KSM Core の分散）、Agent のリソース設計、Autodiscovery の設計と責任分界、メトリクス量とログ量の制御（タグカーディナリティ、labels as tags、コンテナ除外、OpenMetrics、containerCollectAll）、マルチクラスタ運用（命名、GitOps、Fleet Automation、バージョン管理）、よくあるトラブルと対処を、公式情報と公開事例に基づいて整理する。 |
| [大規模・マルチorg運用](04_応用編/large-scale-and-multi-org.md) | Datadog を大規模組織・複数 Organization（マルチorg）で運用する際の設計判断（単一org か マルチorg か）、Cross-Organization Visibility、Organization Groups、ID・権限・キー管理のスケール、大規模環境の制限値、グローバル展開（サイト・データレジデンシー・Dual Shipping・Disaster Recovery）、M&A 時の org 統合手順をまとめる。 |
| [ログ管理の実践](04_応用編/log-management-practices.md) | Datadog Log Management を本番で運用するための実践知見。ログの構造化設計（JSON・予約属性・Standard Attributes・トレース相関）、Log Pipelines の設計、Index の分割と順序・Exclusion Filters・Daily Quota の戦略、Standard / Flex / Flex Frozen / Archive による保持期間の階層化、Cloud SIEM などセキュリティ用途のログとの共存（アクセス制御・機微データ・監査）を、公式ガイドと第三者の知見を出典付きでまとめる。 |
| [Monitoring as Code](04_応用編/monitoring-as-code.md) | Datadog の Monitor・Dashboard・SLO などの監視設定を Terraform でコード管理する実践知見（既存設定の取り込み、モジュール化、レビュー体制と CI/CD、ドリフト検知と防止、UI 変更との共存ルール、Provider v4 移行の注意点）をまとめる。 |
| [OpenTelemetry 活用戦略](04_応用編/opentelemetry-strategy.md) | Datadog で OpenTelemetry（OTel）をどう使うかを判断するためのガイド。Datadog トレーサー（Datadog SDK）と OTel SDK のどちらを選ぶか、送信経路（DDOT Collector / Agent の OTLP 受信 / 自前 Collector / Direct OTLP）の戦略的な意味、ハイブリッド構成のパターン、ベンダーロックインを避ける方法とその限界、課金と運用の落とし穴、段階的な移行手順をまとめる。 |
| [組織への定着](04_応用編/organizational-adoption.md) | Datadog を「導入した」状態から「全社で使われ続ける」状態にするための実践知見として、推進役のプラットフォームチーム（中央オブザーバビリティチーム）の責務と体制、SRE 文化の醸成、役割別の教育、社内チャンピオン制度の設計、Governance Console・Audit Trail・Dashboard Usage API・Scorecards・Campaigns を使った利用状況の可視化と定着 KPI を、公式情報と公開事例に基づいて整理する。 |
| [セキュリティ運用の実践](04_応用編/security-operations-practices.md) | Datadog の Cloud SIEM・Cloud Security（旧称 CSM）・Workload Protection（旧称 CWS）・App and API Protection（旧称 ASM）・Code Security を使う日常のセキュリティ運用の実践をまとめる。分析対象ログの選び方、検知ルールのチューニング（Suppressions・Dynamic Severity・Historical Jobs）、Detection as Code、SOC のトリアージ、ケース・チケット連携、Bits Security Analyst、SOAR、運用メトリクス（TTD/TTA/TTI/TTR）、Findings の自動化（Automation Pipelines・Security Inbox・期限 SLA）、DevSecOps（PR Gates）について、公式情報と実務知見を出典付きで扱う。 |
| [SLO 運用の実践](04_応用編/slo-practices.md) | Datadog で SLO を実運用するための実践知見をまとめたファイル。SLI の選び方と Datadog 上での実装パターン、目標値と期間の決め方、エラーバジェットポリシーの作り方と Datadog 機能への対応付け、マルチウィンドウ・マルチバーンレートアラートの設計値とルーティング、組織への定着（タグ・命名・IaC・Scorecards・レポート）、国内事例とアンチパターンを扱う。 |
| [タグ戦略の実践](04_応用編/tagging-strategy.md) | Datadog のタグを「どう設計し、どう付け、どう守らせるか」を実務観点でまとめる。タグ設計の原則、標準タグ辞書、カーディナリティ管理（カスタムメトリクス課金との関係）、チーム/所有権タグ、コスト配賦タグ（Usage Attribution・Cloud Cost Tag Pipelines）、Monitor Tag Policies・Resource Policies・Tag Rules による組織的な強制、典型的な失敗例に答える。 |

## 参照元

- Datadog 公式ドキュメント：https://docs.datadoghq.com/
- Datadog 公式料金ページ：https://www.datadoghq.com/pricing/
- 各ファイルの出典は、それぞれのフロントマター `sources` と末尾「## 参照元」を参照。
