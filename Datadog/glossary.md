---
title: 用語集（Glossary）
category: introduction
domain: general
last_verified: 2026-11-02
agent_version: "7.x"
summary: Datadog ナレッジ全体で使われる Datadog 固有用語・製品名（旧称を含む）・課金用語・オブザーバビリティ一般用語を、英語正式名称／日本語／定義／関連ファイルの表形式でまとめた用語集。「この用語は何か」「旧称の製品は今どれか」「どのファイルを読めばよいか」に答える。
keywords: [用語集, glossary, 用語, 定義, 略語, 旧称, 改称, rename, Datadog 用語, オブザーバビリティ用語, 課金用語, Software Catalog, Service Catalog, Cloud Security, Cloud Security Management, CSM, App and API Protection, AAP, Application Security Management, ASM, Workload Protection, Cloud Workload Security, CWS, Cloud Network Monitoring, Network Performance Monitoring, NPM, Agent Observability, LLM Observability, Work Management, Case Management, Test Optimization, Test Visibility, PR Gates, Quality Gates, Bits Investigation, Bits AI SRE, BYOC Logs, CloudPrem, Jobs Monitoring, Data Jobs Monitoring, HWMP, MHP, 99パーセンタイル, allotment, 同梱枠, オンデマンド, Logging without Limits, Metrics without Limits, Unified Service Tagging, SLO, SLI, エラーバジェット, バーンレート, RED, USE, ゴールデンシグナル]
sources:
  - https://docs.datadoghq.com/glossary/
  - https://docs.datadoghq.com/tracing/glossary/
  - https://docs.datadoghq.com/getting_started/tagging/
  - https://docs.datadoghq.com/account_management/billing/
  - https://docs.datadoghq.com/account_management/billing/pricing/
  - https://docs.datadoghq.com/data_security/data_retention_periods/
  - https://docs.datadoghq.com/service_management/service_level_objectives/
  - https://www.datadoghq.com/pricing/
  - https://www.datadoghq.com/pricing/list/
---

# 用語集（Glossary）

## 概要

本ファイルは、Datadog ナレッジ（`Datadog/` 配下の全ファイル）で使われる用語を 1 か所で引けるようにした用語集である。各用語は **英語正式名称／日本語／定義／関連ファイル** の 4 列で記載する。定義は各ファイルの記述（2026-11-02 時点の公式ドキュメント・公式料金ページに基づく）を要約したもので、詳細・出典・例外条件は「関連ファイル」のリンク先を正とする。

| 項目 | 本ファイルでの扱い |
|---|---|
| 基準日 | 2026-11-02（`last_verified`）。Datadog は SaaS で継続的に改称・機能追加されるため、迷ったら関連ファイルと公式ドキュメントを確認する |
| 製品名 | 現名称を見出しにし、旧称は「旧称：xxx」で併記する。旧称から引く場合は [1. 改称履歴](#1-製品名の改称履歴旧称現名称) を使う |
| 料金 | 本ファイルには金額を原則記載しない。金額の正本は [製品別料金表](03_導入編/02-pricing-by-product.md)、計算方法は [課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| 確度ラベル | 関連ファイルで `【推定】`・`【第三者情報】`・`【経験則】` が付いている事項は、本ファイルでも同じラベルを付ける |
| 状態表記 | `【Preview】`（プレビュー）、`【Limited Availability】`（限定提供）。無表記は一般提供（GA） |
| 並び順 | 章ごとに関連の強い順（アルファベット順ではない）。略語は [17. 略語索引](#17-略語索引) から引く |

章立ては次のとおり。

| 章 | 内容 |
|---|---|
| [1](#1-製品名の改称履歴旧称現名称) | 製品名の改称履歴（旧称→現名称） |
| [2](#2-組織認証サイト) | 組織・認証・サイト |
| [3](#3-データ収集agent計装opentelemetryintegrations) | データ収集（Agent・計装・OpenTelemetry・Integrations） |
| [4](#4-タグメトリクス) | タグ・メトリクス |
| [5](#5-モニターダッシュボードslo分析ツール) | モニター・ダッシュボード・SLO・分析ツール |
| [6](#6-infrastructureインフラ) | Infrastructure |
| [7](#7-apmapplications) | APM |
| [8](#8-logsログ) | Logs |
| [9](#9-demdigital-experience) | DEM（RUM・Synthetic 等） |
| [10](#10-securityセキュリティ) | Security |
| [11](#11-software-delivery) | Software Delivery |
| [12](#12-service-management) | Service Management |
| [13](#13-ai) | AI |
| [14](#14-data) | Data |
| [15](#15-課金契約用語) | 課金・契約用語 |
| [16](#16-オブザーバビリティ一般用語) | オブザーバビリティ一般用語 |
| [17](#17-略語索引) | 略語索引 |

---

## 1. 製品名の改称履歴（旧称→現名称）

Datadog は製品の対象範囲拡大に合わせて製品名を変更することが多い。古いブログ・技術記事・Terraform リソース名・API パス・環境変数には旧称が残るため、旧称で質問された場合は現名称のファイルを参照する。改称時期・根拠の詳細は [製品ポートフォリオ全体像 §13](01_入門編/04-product-map.md#13-改称履歴旧称現名称の対応表) を参照。

| 旧称（英語） | 現名称（英語） | 日本語 | 補足（旧称が残る場所の例） | 関連ファイル |
|---|---|---|---|---|
| Network Performance Monitoring（NPM） | Cloud Network Monitoring（CNM） | クラウドネットワークモニタリング | ブログ URL、Monitor タイプ一覧の表記 | [Cloud Network Monitoring](02_リファレンス/infrastructure/cloud-network-monitoring.md) |
| Cloud Security Management（CSM） | Cloud Security | クラウドセキュリティ | 料金一覧の品目名（`CSM Pro` / `CSM Enterprise`）、ドキュメント URL。改称時期は 2025 年頃【第三者情報】 | [Cloud Security](02_リファレンス/security/cloud-security.md) |
| Cloud Workload Security（CWS）／CSM Threats | Workload Protection | ワークロード保護 | ドキュメント URL（`/security/cloud_workload_security/`） | [Workload Protection](02_リファレンス/security/workload-protection.md) |
| CSPM（CSM Misconfigurations） | Misconfigurations（Cloud Security の機能） | 設定不備 | 製品メニュー、旧ブログ | [Cloud Security](02_リファレンス/security/cloud-security.md) |
| CIEM | Identity Risks（Cloud Security の機能） | ID リスク | 製品メニュー | [Cloud Security](02_リファレンス/security/cloud-security.md) |
| Application Security Management（ASM）／Application Security Monitoring | App and API Protection（AAP） | アプリケーションと API の保護 | ドキュメント URL（`/security/application_security/`）、`DD_APPSEC_ENABLED`。改称時期は 2025 年【第三者情報】 | [App and API Protection](02_リファレンス/security/app-and-api-protection.md) |
| Security Monitoring | Cloud SIEM | クラウド SIEM | API 名（`security_monitoring`）、画像パス【推定】 | [Cloud SIEM](02_リファレンス/security/cloud-siem.md) |
| Risk Insights | Entity Risks（Cloud SIEM の機能） | エンティティリスク | — | [Cloud SIEM](02_リファレンス/security/cloud-siem.md) |
| Active Protection | Automated response（Workload Protection の機能） | 自動応答 | — | [Workload Protection](02_リファレンス/security/workload-protection.md) |
| event rules（AAP） | In-App WAF rules | In-App WAF ルール | — | [App and API Protection](02_リファレンス/security/app-and-api-protection.md) |
| exclusion filter（AAP） | Passlist | パスリスト | — | [App and API Protection](02_リファレンス/security/app-and-api-protection.md) |
| Code Analysis | Code Security（SAST 等の構成品目） | コードセキュリティ | — | [Code Security](02_リファレンス/security/code-security.md) |
| Service Catalog | Software Catalog（ドキュメント上は「Catalog」） | ソフトウェアカタログ | `service.datadog.yaml`、古いスクリーンショットのタブ名 | [Software Catalog](02_リファレンス/platform/software-catalog.md) |
| Infrastructure List | Host List | ホストリスト | 多くのドキュメント・画面説明 | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| Recent Changes | Resource Changes（Resource Catalog の機能） | リソース変更 | — | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| Live Containers | Containers Explorer | コンテナエクスプローラー | 旧 URL | [コンテナ・Kubernetes 監視](02_リファレンス/infrastructure/container-and-kubernetes-monitoring.md) |
| Orchestrator Explorer | Kubernetes Explorer | Kubernetes エクスプローラー | — | [コンテナ・Kubernetes 監視](02_リファレンス/infrastructure/container-and-kubernetes-monitoring.md) |
| Test Visibility（CI Test Visibility） | Test Optimization | テスト最適化 | 製品ページ URL | [Test Optimization](02_リファレンス/software-delivery/test-optimization.md) |
| Intelligent Test Runner（ITR） | Test Impact Analysis（TIA） | テスト影響分析 | `ITR:NoSkip`、`datadog_itr_unskippable`、権限名 | [Test Optimization](02_リファレンス/software-delivery/test-optimization.md) |
| Quality Gates | PR Gates | PR ゲート | `datadog-ci gate evaluate`、URL（`/quality_gates/`）。2026 年に置き換え | [DORA Metrics・PR Gates・Code Coverage](02_リファレンス/software-delivery/software-delivery-insights.md) |
| CI Visibility | CI Visibility（料金上の品目名は Pipeline Visibility / CI Pipeline Visibility） | CI 可視化 | ドキュメントでは CI Visibility のまま | [CI Visibility](02_リファレンス/software-delivery/ci-visibility.md) |
| Case Management／Case | Work Management／Work Item | ワークマネジメント／作業項目 | API エンドポイント・権限名（`cases_*`）。改称告知ブログは 2026-08-18 公開 | [Work Management](02_リファレンス/service-management/case-management.md) |
| VictorOps | Splunk On-Call | — | 通知ハンドル | [通知・コラボレーション連携](02_リファレンス/platform/collaboration-integrations.md) |
| LLM Observability | Agent Observability | エージェント オブザーバビリティ | URL（`/llm_observability/`）、SDK（`ddtrace.llmobs`）、`DD_LLMOBS_*`、権限名。改称時期 2026-06【第三者情報】 | [Agent Observability](02_リファレンス/ai/llm-observability.md) |
| Bits AI SRE | Bits Investigation | — | ブログ URL（`bits-ai-sre`）【推定】 | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Bits AI Dev Agent | Bits Code | — | ブログ URL【推定】 | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Bits Assistant（Bits AI アシスタント） | Bits Chat | — | ブログ URL【推定】 | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Bits AI Security Analyst | Bits Security Analyst | — | — | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Database Investigator | Database Investigations in Bits Chat | — | — | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Data Jobs Monitoring（DJM） | Data Observability: Jobs Monitoring | データジョブ監視 | 本ナレッジのファイル名、旧 URL【推定】 | [Data Jobs Monitoring](02_リファレンス/data/data-jobs-monitoring.md) |
| Metaplane（買収製品） | Data Observability（Quality Monitoring 等）。既存顧客には "Metaplane by Datadog" | データ品質監視 | 2025-04 買収 | [Data Observability](02_リファレンス/data/data-observability.md) |
| Eppo（買収製品） | Experiments / Feature Flags 系（"Eppo by Datadog"） | 実験 | 2025-05 買収 | [製品ポートフォリオ全体像](01_入門編/04-product-map.md) |
| CloudPrem | BYOC Logs（BYOC Log Management） | — | Helm チャート・Docker イメージ名（`datadog/cloudprem`）。2026 年改称 | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| Log Workspaces（Logs Workspaces） | Notebooks Analysis Features | ノートブックの分析機能 | ドキュメント URL | [Notebooks・DDSQL・Reference Tables](02_リファレンス/platform/notebooks-and-data-tools.md) |
| Widget Clipboard | Datadog Clipboard | — | — | [画面構成とナビゲーション](01_入門編/06-ui-navigation.md) |
| Library Injection（ライブラリインジェクション） | Local SDK Injection | ローカル SDK インジェクション | — | [APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) |
| トレーサー／トレーシングライブラリ（tracer / tracing library） | Datadog SDK | Datadog SDK | GitHub リポジトリ名 `dd-trace-*` | [APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) |
| Code Hotspots（通称） | Trace to Profiling integration | トレースとプロファイルの連携 | — | [Continuous Profiler](02_リファレンス/apm/continuous-profiler.md) |
| App Analytics | Retention Filters（APM） | リテンションフィルター | 2020-10-20 に自動変換 | [課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Synthetic Monitoring | Synthetic Testing and Monitoring（ドキュメント表題。Synthetic Monitoring も併用） | 外形監視・合成監視 | — | [Synthetic Monitoring](02_リファレンス/dem/synthetic-monitoring.md) |
| （Incident Management と On-Call の総称） | Incident Response | インシデントレスポンス | 料金上のバンドル名 | [Incident Management](02_リファレンス/service-management/incident-management.md) |
| Kinesis Data Firehose | Amazon Data Firehose | — | AWS 側の改称 | [AWS Integration](02_リファレンス/platform/aws-integration.md) |
| Azure Active Directory（Azure AD） | Microsoft Entra ID | — | Microsoft 側の改称 | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Google Cloud Platform（GCP） | Google Cloud | — | インテグレーションタイル名・API パス・Terraform リソース名に GCP が残る | [Google Cloud Integration](02_リファレンス/platform/gcp-integration.md) |
| Terraform Cloud | HCP Terraform | — | HashiCorp 側の改称 | [Terraform と IaC](02_リファレンス/platform/terraform-and-iac.md) |

> **注意:** 本ナレッジの一部ファイル名（`case-management.md`、`llm-observability.md`、`data-jobs-monitoring.md`）は旧称のままである。ファイル名で探す場合は旧称で、本文で探す場合は現名称で検索するとよい。

---

## 2. 組織・認証・サイト

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Datadog, Inc. | データドッグ社 | 統合オブザーバビリティ＋セキュリティプラットフォームを SaaS で提供する米国企業（NASDAQ: DDOG）。日本法人は Datadog Japan 合同会社 | [Datadogとは](01_入門編/01-what-is-datadog.md) |
| Organization（org） | 組織 | データ・ユーザー・設定（ロール、キー、連携設定など）の境界となる単位。組織はちょうど 1 つのサイト上に存在する | [必須概念](01_入門編/05-core-concepts.md)、[組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Multi-organization account（parent org / child org） | マルチオーガニゼーション（親組織／子組織） | 1 つの親組織が複数の子組織を管理する仕組み。既定で無効でサポートに依頼して有効化する。子組織どうしは互いのデータにアクセスできず、子組織は親のプランを継承し親の請求に合算される | [必須概念](01_入門編/05-core-concepts.md)、[大規模・マルチorg運用](04_応用編/15-large-scale-and-multi-org.md) |
| Cross-Organization Visibility | クロスオーガニゼーション可視化 | 組織をまたいでデータ（メトリクス等）を参照する機能 | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Organization Groups | 組織グループ | 複数 org のポリシーを一元管理する機能 | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Custom subdomain | カスタムサブドメイン | 組織専用のサブドメイン URL。既定で無効でサポートに依頼して有効化する | [必須概念](01_入門編/05-core-concepts.md) |
| Datadog Site | サイト（リージョン） | Datadog が世界各地で運用する、互いに完全に独立した SaaS インスタンス。サイト間でデータは共有できない。2026-11-02 時点で US1・US3・US5・EU1・AP1（日本）・AP2（オーストラリア）・UK1・US1-FED・US2-FED の 9 サイト | [Datadog Sites](02_リファレンス/platform/datadog-sites.md)、[アーキテクチャ概観](01_入門編/03-architecture-overview.md) |
| AP1 | AP1（日本サイト） | 日本に所在する Datadog サイト。URL は `https://ap1.datadoghq.com`、サイトパラメータは `ap1.datadoghq.com`。本ナレッジの基準サイト | [Datadog Sites](02_リファレンス/platform/datadog-sites.md) |
| US1-FED / US2-FED（Datadog for Government） | 米国政府向けサイト | 米国政府向けのサイト（`ddog-gov.com` 系）。FedRAMP 等に対応し、一部製品（Bits AI、MCP Server 等）は非対応。Remote Configuration は既定で無効 | [Datadog Sites](02_リファレンス/platform/datadog-sites.md)、[セキュリティとコンプライアンス](03_導入編/12-security-and-compliance.md) |
| Site parameter（`DD_SITE`） | サイトパラメータ | Agent・SDK・API クライアントに設定する送信先サイトの指定値（例：`ap1.datadoghq.com`）。誤ると正しい API キーでも別サイトの組織に届かない | [必須概念](01_入門編/05-core-concepts.md)、[Agent 設定リファレンス](02_リファレンス/platform/agent-configuration.md) |
| Intake | インテーク（取り込み口） | Datadog Site 上の、製品・データ種別ごとのデータ受付エンドポイント | [アーキテクチャ概観](01_入門編/03-architecture-overview.md)、[ネットワーク・接続要件](03_導入編/11-network-and-connectivity.md) |
| Data residency | データレジデンシー | データの保存場所の要件。Datadog ではデータは組織を作成したサイトに保存される | [Datadog Sites](02_リファレンス/platform/datadog-sites.md)、[セキュリティとコンプライアンス](03_導入編/12-security-and-compliance.md) |
| Dual Shipping（`additional_endpoints`） | デュアルシッピング（二重送信） | Agent から複数のサイト・組織へ同時にデータを送る設定。サイト移行や他製品からの移行の並行稼働に使う | [Datadog Sites](02_リファレンス/platform/datadog-sites.md)、[他製品からの移行](03_導入編/14-migration-from-other-tools.md) |
| Datadog Disaster Recovery（DDR） | Datadog ディザスタリカバリ | クラウドリージョンや Datadog サービスの障害時に、別サイトにあらかじめ作った副 org に切り替えて観測を続ける機能。商用サイトでは【Limited Availability】 | [Datadog Sites](02_リファレンス/platform/datadog-sites.md)、[大規模・マルチorg運用](04_応用編/15-large-scale-and-multi-org.md) |
| PrivateLink / Private Service Connect / Azure Private Link | 閉域接続 | AWS PrivateLink、Google Cloud Private Service Connect、Azure Private Link を使い、インターネットを経由せずに Datadog へ送信する接続方式 | [ネットワーク・接続要件](03_導入編/11-network-and-connectivity.md) |
| `ip-ranges` | IP レンジ一覧 | Datadog が公開する送信元・送信先 IP レンジの一覧。ファイアウォール許可リストの根拠に使う | [ネットワーク・接続要件](03_導入編/11-network-and-connectivity.md) |
| API key | API キー | 組織に一意の、データ送信用の認証情報。Agent はこのキーで送信先の組織を特定する。既定で組織あたり 50 個まで（Managed キーは数えない）。失効後 7 日間は UI から復元可能 | [必須概念](01_入門編/05-core-concepts.md)、[API とキー管理](02_リファレンス/platform/api-and-keys.md) |
| Managed API key | マネージド API キー | Datadog の連携やサービスが作成した API キー。上限に数えられず、値の表示や名前変更はできない | [必須概念](01_入門編/05-core-concepts.md) |
| Application key（app key） | アプリケーションキー | API キーと組み合わせてプログラムから API を操作するための、作成ユーザー（またはサービスアカウント）に紐づくキー。スコープで権限を絞れる。作成ユーザーを無効化すると失効する | [必須概念](01_入門編/05-core-concepts.md)、[API とキー管理](02_リファレンス/platform/api-and-keys.md) |
| Scoped application key | スコープ付きアプリケーションキー | 権限（authorization scopes）を限定したアプリケーションキー。未指定なら作成者の全権限を持つ | [API とキー管理](02_リファレンス/platform/api-and-keys.md) |
| One-Time Read（OTR）mode | ワンタイムリード モード | アプリケーションキーのシークレットを作成時にのみ表示し、以後取得できなくするモード。2025-08-20 以降に作成された新規親組織では恒久的に有効 | [必須概念](01_入門編/05-core-concepts.md)、[API とキー管理](02_リファレンス/platform/api-and-keys.md) |
| Client token | クライアントトークン | ブラウザ・モバイル等（RUM、ブラウザログ等）のクライアント側からデータを送るための組織に一意のトークン | [必須概念](01_入門編/05-core-concepts.md)、[RUM（ブラウザ）](02_リファレンス/dem/rum-browser.md) |
| Personal Access Token（PAT） | パーソナルアクセストークン | 開発者のスクリプト・CLI など個人に紐づく API 呼び出し用トークン（接頭辞 `ddpat_`）。スコープと有効期限（24 時間〜1 年）が必須 | [API とキー管理](02_リファレンス/platform/api-and-keys.md) |
| Service Access Token（SAT） | サービスアクセストークン | CI/CD・Terraform・自律型 AI エージェントなどの自動化向けに、サービスアカウントに紐づくトークン（接頭辞 `ddsat_`） | [API とキー管理](02_リファレンス/platform/api-and-keys.md) |
| Service Account | サービスアカウント | 人ではなく自動化処理のためのアカウント。ユーザーの退職等に影響されないキー運用に使う | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Workload Identity Federation（WIF） | ワークロード ID 連携 | クラウドの認証情報で Terraform Provider や Agent を認証し、静的キーを不要にする方式（AWS のみ GA） | [API とキー管理](02_リファレンス/platform/api-and-keys.md)、[Terraform と IaC](02_リファレンス/platform/terraform-and-iac.md) |
| RBAC（Role-Based Access Control） | ロールベースアクセス制御 | ユーザーにロールを割り当てて権限を制御する仕組み。既定ロールは Datadog Admin / Standard / Read Only の 3 つで、カスタムロールも作成できる | [必須概念](01_入門編/05-core-concepts.md)、[組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Datadog Admin / Standard / Read Only Role | 管理者／標準／読み取り専用ロール | Datadog の既定ロール。Admin は請求・キー失効・ユーザー管理等、Standard はダッシュボード・モニター等の閲覧と変更、Read Only は編集不可 | [必須概念](01_入門編/05-core-concepts.md) |
| Granular Access Control（Restriction Policy） | 細粒度アクセス制御（制限ポリシー） | 個々のリソース（特定のダッシュボード等）単位で編集者・閲覧者を制御する仕組み。Terraform では `datadog_restriction_policy` | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Restriction Query（Logs RBAC） | 制限クエリ | ログのデータアクセスをクエリ条件でロールごとに制限する仕組み | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Data Access Control（Restricted Datasets） | データアクセス制御 | タグ・属性単位でデータの閲覧を制限する仕組み | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Datadog Teams（team handle） | チーム | ユーザーのグループ。ダッシュボード・サービス・モニター・インシデント・SLO 等をチームに紐付け、`team:<team-handle>` で絞り込める | [必須概念](01_入門編/05-core-concepts.md)、[タグ戦略の実践](04_応用編/02-tagging-strategy.md) |
| SAML / SSO | SAML シングルサインオン | 外部 IdP によるログイン。子組織には継承されず、組織ごとに設定する。JIT プロビジョニング、SAML Strict、Group Mapping（AuthN Mapping）に対応 | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| SCIM | SCIM（ユーザー自動プロビジョニング） | IdP（Okta、Microsoft Entra ID 等）からユーザー・チームを自動同期する標準プロトコル | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md)、[運用設計](03_導入編/13-operations-design.md) |
| IP Allowlist | IP 許可リスト | UI・API へのアクセス元 IP を制限する組織設定。親から子組織へ継承されない | [組織・ユーザー・権限管理](02_リファレンス/platform/account-and-access-management.md) |
| Audit Trail | 監査証跡 | 誰が・いつ・どの認証手段で・何を操作したかを記録し、検索・アラート・保管・外部転送できる製品。有効時は 90 日保持（無効時 7 日） | [Audit Trail](02_リファレンス/platform/audit-trail.md) |
| Notable Events | 注目イベント | Audit Trail で重要度の高い操作として抽出されるイベント | [Audit Trail](02_リファレンス/platform/audit-trail.md) |
| Governance Console | ガバナンスコンソール | コスト配賦・アクセス制御・タグの衛生状態を 1 画面にまとめ、ポリシーチェックとガードレールを提供するコンソール（Infrastructure Enterprise に含まれる） | [Usage・Cost Visibility](02_リファレンス/platform/usage-and-cost-attribution.md)、[運用設計](03_導入編/13-operations-design.md) |
| Trust Center | トラストセンター | Datadog の認証取得状況（SOC 2、ISO 27001 等）やセキュリティ資料を公開するサイト（`trust.datadoghq.com`） | [セキュリティとコンプライアンス](03_導入編/12-security-and-compliance.md) |

---

## 3. データ収集（Agent・計装・OpenTelemetry・Integrations）

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Datadog Agent | Datadog エージェント | ホストやコンテナ上で動作し、メトリクス・ログ・トレース・プロセス・ネットワーク・セキュリティイベント等を収集して Intake へ送るオープンソースのソフトウェア。現行メジャーバージョンは v7（Python 3 のみ） | [Datadog Agent](02_リファレンス/platform/agent.md)、[Agent 設定リファレンス](02_リファレンス/platform/agent-configuration.md) |
| Collector（Agent） | コレクター | Agent のメインプロセスで、チェック（インテグレーション・カスタムチェック）を実行し、標準メトリクスを 15 秒ごとに収集するコンポーネント | [アーキテクチャ概観](01_入門編/03-architecture-overview.md) |
| Forwarder | フォワーダー | 収集したデータを HTTPS で Datadog へ送る Agent のコンポーネント。ネットワーク断に備えメモリ（設定によりディスク）にバッファリングする | [アーキテクチャ概観](01_入門編/03-architecture-overview.md)、[ネットワーク・接続要件](03_導入編/11-network-and-connectivity.md) |
| Trace Agent（`trace-agent`） | トレースエージェント（APM Agent） | Datadog SDK からトレースを受け取り（既定ポート `8126`）、サンプリング・送信する Agent の子プロセス | [Datadog Agent](02_リファレンス/platform/agent.md) |
| Process Agent（`process-agent`） | プロセスエージェント | ライブプロセス・ライブコンテナ情報を収集する Agent の子プロセス | [Datadog Agent](02_リファレンス/platform/agent.md) |
| System Probe（`system-probe`） | システムプローブ | eBPF 等でカーネルレベルの観測を行う Agent の子プロセス。Cloud Network Monitoring、Universal Service Monitoring、Workload Protection 等で使う | [Datadog Agent](02_リファレンス/platform/agent.md)、[Universal Service Monitoring](02_リファレンス/apm/universal-service-monitoring.md) |
| Security Agent（`security-agent`） | セキュリティエージェント | Workload Protection 等のセキュリティ機能を担う Agent の子プロセス | [Workload Protection](02_リファレンス/security/workload-protection.md) |
| Logs Agent | ログエージェント | ファイル・コンテナ・journald 等からログを収集して送る Agent のコンポーネント。既定で無効（`logs_enabled: true` で有効化） | [ログ収集](02_リファレンス/logs/log-collection.md) |
| `datadog.yaml` | Agent 主設定ファイル | Agent の主設定ファイル。キーは `DD_` で始まる環境変数でも設定できる | [Agent 設定リファレンス](02_リファレンス/platform/agent-configuration.md) |
| `conf.d` / Check | チェック設定ディレクトリ／チェック | インテグレーション（チェック）ごとの設定ディレクトリと、そこで定義される収集処理 | [Agent 設定リファレンス](02_リファレンス/platform/agent-configuration.md)、[Integrations](02_リファレンス/platform/integrations.md) |
| Custom check（Custom Agent Check） | カスタムチェック | 社内システム向けに自作する Agent チェック。送るメトリクスはカスタムメトリクスになる | [Integrations](02_リファレンス/platform/integrations.md) |
| Service Check | サービスチェック | チェックが報告する状態（OK / WARNING / CRITICAL / UNKNOWN 等）。例：`datadog.agent.up` | [Integrations](02_リファレンス/platform/integrations.md)、[Monitors](02_リファレンス/platform/monitors.md) |
| Agent flare | フレア | Agent のログ・設定等をまとめてサポートへ送る診断パッケージ。Fleet Automation からリモート送信もできる | [Datadog Agent](02_リファレンス/platform/agent.md)、[サポートと教育](03_導入編/15-support-and-training.md) |
| Secrets Management（`ENC[]`） | シークレット管理 | 設定ファイル中の秘密情報を `ENC[]` 記法と外部コマンド（`secret_backend_command`）で解決する Agent の仕組み | [Agent 設定リファレンス](02_リファレンス/platform/agent-configuration.md) |
| Infrastructure mode（`infrastructure_mode`） | インフラストラクチャモード | Agent がどこまでインフラ監視を行うかを決める設定（Full / Basic / End User Device / None）。Agent の動作を変えるだけで契約は変わらない | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| IoT Agent / FIPS Agent | IoT エージェント／FIPS エージェント | 組み込み・IoT 機器向けの軽量 Agent と、FIPS 準拠の暗号モジュールを使う Agent の派生パッケージ | [Datadog Agent](02_リファレンス/platform/agent.md) |
| Remote Configuration（RC） | リモート設定 | Datadog UI で行った設定変更を Agent・Datadog SDK・Observability Pipelines Worker 等に配布するプル型の仕組み。通信は顧客環境→Datadog の HTTPS。多くの組織で既定有効、US1-FED・US2-FED では既定無効 | [Fleet Automation と Remote Configuration](02_リファレンス/platform/fleet-automation.md)、[アーキテクチャ概観](01_入門編/03-architecture-overview.md) |
| Fleet Automation | フリートオートメーション | Agent と OTel Collector を Datadog 画面から一元管理する機能（一覧・構成確認、設定配布、リモートアップグレード、リモート flare） | [Fleet Automation と Remote Configuration](02_リファレンス/platform/fleet-automation.md)、[Agent 展開設計](03_導入編/10-agent-rollout-design.md) |
| Datadog Installer | Datadog インストーラー | リモートアップグレード（`remote_updates`）等で使われる Agent のインストール・更新の仕組み | [Fleet Automation と Remote Configuration](02_リファレンス/platform/fleet-automation.md) |
| Node Agent | ノード Agent | Kubernetes の各ノードに DaemonSet として 1 Pod ずつ配置される Datadog Agent | [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md) |
| Datadog Cluster Agent（DCA） | クラスターエージェント | Kubernetes API サーバーとノード Agent の間のプロキシとして、クラスターメタデータ、Kubernetes イベント、Cluster Checks の配布、Admission Controller、External Metrics（HPA 用）、Kubernetes State Metrics Core を担うコンポーネント | [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md)、[Kubernetes 監視の実践](04_応用編/07-kubernetes-monitoring-practices.md) |
| Cluster Checks / Cluster Checks Runner（CLC Runner） | クラスターチェック／クラスターチェックランナー | クラスター内で 1 回だけ実行すればよいチェックと、それだけを実行する専用 Agent 群（任意） | [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md) |
| Endpoint Checks | エンドポイントチェック | Kubernetes Service の背後にある各エンドポイント（Pod）を対象に実行するチェック | [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md) |
| Datadog Operator（`DatadogAgent` CRD） | Datadog オペレーター | `DatadogAgent` カスタムリソースから Node Agent・Cluster Agent・Cluster Checks Runner を展開・調整する Kubernetes Operator。新規導入では Datadog が推奨 | [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md) |
| Helm chart（`datadog-values.yaml`） | Helm チャート | Helm で Datadog Agent を Kubernetes に展開するためのチャート | [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md) |
| Admission Controller | アドミッションコントローラー | Cluster Agent の MutatingAdmissionWebhook。Pod 作成時に環境変数（`DD_ENV` 等）や SDK を自動注入する | [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md)、[APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) |
| Autodiscovery | オートディスカバリー | コンテナの起動・停止を検知し、アノテーション・ラベル等のテンプレートに従ってインテグレーションを自動実行する仕組み。コンテナ環境での Unified Service Tagging の前提 | [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md)、[Integrations](02_リファレンス/platform/integrations.md) |
| Kubernetes State Metrics Core（KSM Core） | Kubernetes ステートメトリクス Core | Kubernetes オブジェクトの状態メトリクス（`kubernetes_state.*`）を Agent 内で生成するチェック | [コンテナ/Kubernetes向けAgent](02_リファレンス/platform/kubernetes-and-containers-agent.md) |
| Integrations | インテグレーション | 外部システム（ミドルウェア、DB、クラウド、SaaS 等）からデータを取り込む、または外部へ連携する部品の総称。1,000 を超える組み込みインテグレーションがあり、Agent ベース・認証（クローラー）ベース・ライブラリの 3 種に大別される | [Integrations](02_リファレンス/platform/integrations.md) |
| Marketplace | マーケットプレイス | パートナーが提供する有償・無償のインテグレーションやアプリの流通基盤（Datadog 内） | [Integrations](02_リファレンス/platform/integrations.md) |
| OpenMetrics check | OpenMetrics チェック | Prometheus 形式のエンドポイントから汎用的にメトリクスを取り込むチェック。取り込んだメトリクスはカスタムメトリクスになり得る | [Integrations](02_リファレンス/platform/integrations.md)、[Custom Metrics と DogStatsD](02_リファレンス/platform/custom-metrics-and-dogstatsd.md) |
| JMXFetch（JMX check） | JMX チェック | Java アプリケーションの JMX メトリクスを取り込む仕組み | [Integrations](02_リファレンス/platform/integrations.md) |
| AWS Integration | AWS インテグレーション | Datadog の AWS アカウントから IAM ロール委任（External ID）で顧客の AWS API を呼び、Agent なしで CloudWatch メトリクス・イベント・タグ・リソース情報を収集する連携。ログは Datadog Forwarder か Amazon Data Firehose で送る | [AWS Integration](02_リファレンス/platform/aws-integration.md) |
| CloudWatch Metric Streams | CloudWatch メトリクスストリーム | API ポーリングの代わりに Firehose 経由でメトリクスを準リアルタイムに送る AWS 側の機能 | [AWS Integration](02_リファレンス/platform/aws-integration.md) |
| Datadog Forwarder（Lambda Forwarder） | Datadog フォワーダー（Lambda） | CloudWatch Logs や S3 のログを Datadog へ送る Lambda 関数 | [ログ収集](02_リファレンス/logs/log-collection.md)、[AWS Integration](02_リファレンス/platform/aws-integration.md) |
| Azure Integration（App Registration 方式 / Azure Native Integration） | Azure インテグレーション | App Registration の資格情報または Azure Native ISV Service（"Datadog - An Azure Native ISV Service"）で Azure Monitor のメトリクスとリソースメタデータを収集する連携 | [Azure Integration](02_リファレンス/platform/azure-integration.md) |
| Google Cloud Integration | Google Cloud インテグレーション | サービスアカウントの偽装（impersonation）で Google Cloud のメトリクス・リソース・ログ等を取り込む連携 | [Google Cloud Integration](02_リファレンス/platform/gcp-integration.md) |
| Resource Collection | リソース収集 | クラウド連携でリソースの構成情報を収集する機能（AWS では SecurityAudit ポリシーが必要） | [AWS Integration](02_リファレンス/platform/aws-integration.md) |
| Agentless | エージェントレス | Agent を使わず、クラウド連携・API・Agentless Scanning 等でデータを取得する経路の総称 | [アーキテクチャ概観](01_入門編/03-architecture-overview.md) |
| Datadog SDK（旧称：トレーサー／トレーシングライブラリ） | Datadog SDK | アプリケーションに組み込み、トレース・プロファイル・AAP 等のデータを生成するライブラリ（GitHub リポジトリ名 `dd-trace-*`） | [APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) |
| Instrumentation | インスツルメンテーション（計装） | トレース・メトリクス・ログを取得して送るためのコードやライブラリを組み込むこと。自動計装とカスタム（手動）計装がある | [APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) |
| Single Step Instrumentation（SSI） | シングルステップ計装 | Agent のインストール時にアプリへ Datadog SDK を自動注入し、コード変更なしで APM を有効化する方式（Single Step APM） | [APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md)、[APM 運用の実践](04_応用編/05-apm-practices.md) |
| Local SDK Injection（旧称：Library Injection） | ローカル SDK インジェクション | Kubernetes 等で Admission Controller を使い Pod 単位に SDK を注入する方式 | [APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) |
| Orchestrion | Orchestrion | Go 向けのコンパイル時自動計装ツール | [APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) |
| OpenTelemetry（OTel） | オープンテレメトリー | CNCF のベンダー中立なテレメトリ計装・収集の仕様と実装。Datadog は OTel のトレース・メトリクス・ログを受け付ける | [OpenTelemetry サポート](02_リファレンス/platform/opentelemetry.md)、[OpenTelemetry 活用戦略](04_応用編/10-opentelemetry-strategy.md) |
| OTLP（OpenTelemetry Protocol） | OTLP | OTel の送信プロトコル。Agent の OTLP 受信は既定で gRPC `4317`、HTTP `4318` | [OpenTelemetry サポート](02_リファレンス/platform/opentelemetry.md) |
| DDOT Collector（Datadog Distribution of OpenTelemetry Collector） | DDOT コレクター | Datadog Agent に組み込まれた OTel Collector。OTel の中立性と Fleet Automation 等の Datadog 固有機能を両立する推奨経路 | [OpenTelemetry サポート](02_リファレンス/platform/opentelemetry.md)、[アーキテクチャ概観](01_入門編/03-architecture-overview.md) |
| OTLP Ingest in the Agent | Agent の OTLP 取り込み | 既存の Datadog Agent に OTLP を受信させる経路（トレース・メトリクスは Agent 7.32.0 以降、ログは 7.48.0 以降。ログは既定無効） | [OpenTelemetry サポート](02_リファレンス/platform/opentelemetry.md) |
| Datadog Exporter / Datadog Connector | Datadog エクスポーター／コネクター | 顧客運用の OSS OTel Collector から Datadog へ送るためのコンポーネント（Connector は Trace Metrics 相当を算出） | [OpenTelemetry サポート](02_リファレンス/platform/opentelemetry.md) |
| Direct OTLP Ingest（Agentless OTLP） / Managed Platform OTLP | 直接 OTLP 取り込み | Agent・Collector を介さず、アプリから Datadog の OTLP Intake へ直接送る経路。Agent・Collector を置けない場合の選択肢 | [OpenTelemetry サポート](02_リファレンス/platform/opentelemetry.md) |
| Semantic conventions | セマンティック規約 | OTel の属性命名規約。`deployment.environment.name`→`env`、`service.name`→`service`、`service.version`→`version` に対応付けられる | [OpenTelemetry サポート](02_リファレンス/platform/opentelemetry.md)、[必須概念](01_入門編/05-core-concepts.md) |
| Synthetics Private Location（Worker） | プライベートロケーション | 顧客ネットワーク内で Synthetic テストを実行するワーカー | [Synthetic Monitoring](02_リファレンス/dem/synthetic-monitoring.md) |
| Datadog Terraform Provider | Datadog Terraform プロバイダー | Datadog 公式の Terraform プロバイダー（`DataDog/datadog`）。Monitor・Dashboard・SLO 等を IaC 管理する | [Terraform と IaC](02_リファレンス/platform/terraform-and-iac.md)、[Monitoring as Code](04_応用編/09-monitoring-as-code.md) |
| datadog-ci | datadog-ci | CI/CD から Datadog（Synthetic、CI Visibility、Code Coverage、Serverless 計装等）を操作する公式 CLI | [API とキー管理](02_リファレンス/platform/api-and-keys.md)、[CI Visibility](02_リファレンス/software-delivery/ci-visibility.md) |
| datadog-sync-cli | datadog-sync-cli | 組織間・サイト間でダッシュボード・モニター等の設定を複製するツール | [大規模・マルチorg運用](04_応用編/15-large-scale-and-multi-org.md) |

---

## 4. タグ・メトリクス

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Tag | タグ | テレメトリやリソースに付けるラベル。`<key>:<value>` 形式が推奨。最大 200 文字、メトリクスタグ・スパンタグは小文字に正規化される。絞り込み・グループ化・相関・所有者明確化・コスト配賦の基盤 | [Tagging](02_リファレンス/platform/tagging.md)、[必須概念](01_入門編/05-core-concepts.md) |
| Reserved tags | 予約タグ | Datadog が特別な意味を持たせたタグキー：`host`、`device`、`source`、`service`、`env`、`version`、`team` | [Tagging](02_リファレンス/platform/tagging.md) |
| Host tag | ホストタグ | ホストに付けたタグ。そのホストのメトリクス・ログ・トレースに継承される。UI での変更は反映に最大 5 分 | [必須概念](01_入門編/05-core-concepts.md) |
| Unified Service Tagging（UST） | 統合サービスタグ付け | 予約タグ `env`・`service`・`version` をすべてのテレメトリに一貫して付け、テレメトリどうしを結び付ける仕組み（`DD_ENV`・`DD_SERVICE`・`DD_VERSION` 等で設定） | [必須概念](01_入門編/05-core-concepts.md)、[Tagging](02_リファレンス/platform/tagging.md)、[タグ戦略の実践](04_応用編/02-tagging-strategy.md) |
| Cardinality | カーディナリティ | あるタグキーに紐づくタグ値の数（公式用語集の定義）。値の組み合わせが増えるほどカスタムメトリクスの時系列数と課金が増える | [Tagging](02_リファレンス/platform/tagging.md)、[よくある失敗](04_応用編/12-common-pitfalls.md) |
| Tag cardinality（`DD_CHECKS_TAG_CARDINALITY` / `DD_DOGSTATSD_TAG_CARDINALITY`） | タグカーディナリティ設定 | コンテナ環境で付与するタグの粒度を `low`（既定）・`orchestrator`・`high` から選ぶ設定 | [必須概念](01_入門編/05-core-concepts.md)、[Kubernetes 監視の実践](04_応用編/07-kubernetes-monitoring-practices.md) |
| Tag Policies（Monitor Tag Policies） | タグポリシー | モニターに必須タグを強制する組織設定 | [Tagging](02_リファレンス/platform/tagging.md)、[タグ戦略の実践](04_応用編/02-tagging-strategy.md) |
| Metric | メトリクス | 時系列で追跡する数値データ。値とタイムスタンプの組の列（timeseries）として保存され、保持期間は 15 か月 | [Metrics](02_リファレンス/platform/metrics.md)、[必須概念](01_入門編/05-core-concepts.md) |
| Metric types（COUNT / RATE / GAUGE / HISTOGRAM / DISTRIBUTION / SET） | メトリクスタイプ | 送信時のタイプ。COUNT は区間内の発生回数、RATE は毎秒の発生回数、GAUGE は区間内の最後の値、HISTOGRAM は Agent 側で統計量を計算、DISTRIBUTION は全値をサーバー側で集計、SET はユニーク値の数（DogStatsD のみ） | [Metrics](02_リファレンス/platform/metrics.md)、[必須概念](01_入門編/05-core-concepts.md) |
| Submission type / In-app type | 送信タイプ／アプリ内タイプ | メトリクスの送信時のタイプと Datadog 内で保存・表示されるタイプ。例：DogStatsD の COUNT は RATE として表示される | [必須概念](01_入門編/05-core-concepts.md) |
| DDSketch | DDSketch | DISTRIBUTION のパーセンタイルを相対誤差保証付きで集計するデータ構造 | [Metrics](02_リファレンス/platform/metrics.md) |
| Flush interval | フラッシュ間隔 | Agent が区間内の値を 1 つにまとめて送る間隔（DogStatsD は 10 秒） | [Custom Metrics と DogStatsD](02_リファレンス/platform/custom-metrics-and-dogstatsd.md) |
| Custom Metrics | カスタムメトリクス | 標準インテグレーション以外から送るメトリクス。**メトリクス名とタグ値（`host` を含む）の一意な組み合わせ（時系列 1 本）** を 1 個と数える | [Custom Metrics と DogStatsD](02_リファレンス/platform/custom-metrics-and-dogstatsd.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| DogStatsD | DogStatsD | Agent に同梱された StatsD 互換のメトリクス集約サービス。HISTOGRAM・DISTRIBUTION・タグ・Service Check・Event を拡張し、UDP（既定 `8125`）または UDS で受け付ける | [Custom Metrics と DogStatsD](02_リファレンス/platform/custom-metrics-and-dogstatsd.md) |
| Origin Detection | オリジン検出 | DogStatsD の送信元コンテナを特定し、コンテナタグを付与する仕組み | [Custom Metrics と DogStatsD](02_リファレンス/platform/custom-metrics-and-dogstatsd.md) |
| Metrics without Limits™（MwL） | Metrics without Limits | メトリクスごとにクエリ可能に残すタグを構成し、取り込み（Ingested）とインデックス（Indexed）を分けて扱う仕組み。タグ構成したメトリクスのみ Ingested が課金対象になる | [Metrics](02_リファレンス/platform/metrics.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md)、[コスト最適化](04_応用編/01-cost-optimization.md) |
| Ingested / Indexed custom metrics | 取り込み／インデックス済みカスタムメトリクス | MwL において、送信された全タグ組み合わせ数（Ingested）と、タグ構成後にクエリ可能として残る組み合わせ数（Indexed） | [課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Metric Name pricing | メトリクス名課金 | カスタムメトリクスをメトリクス名の数とデータポイント数で課金するモデル。カーディナリティ課金とは契約 SKU で相互排他 | [課金計算の仕組み](03_導入編/03-billing-mechanics.md)、[Metrics](02_リファレンス/platform/metrics.md) |
| Historical Metrics Ingestion（HMI） | 履歴メトリクス取り込み | 1 時間より古いタイムスタンプのデータ点を取り込む機能 | [Metrics](02_リファレンス/platform/metrics.md) |
| Metrics Summary / Metrics Explorer | メトリクスサマリー／メトリクスエクスプローラー | 報告中のメトリクス一覧とメタデータ・タグ構成を管理する画面／メトリクスをアドホックにグラフ化する画面 | [Metrics](02_リファレンス/platform/metrics.md) |
| Time aggregation（rollup） | 時間集約（ロールアップ） | 時間バケット内のデータ点をまとめる方法（既定 `avg`。`sum`・`min`・`max`・`count`）。常に適用される | [メトリクスクエリと関数](02_リファレンス/platform/metrics-query-and-functions.md) |
| Space aggregation | 空間集約 | ホストやタグをまたいで時系列をまとめる方法と軸（`avg by {host}` 等） | [メトリクスクエリと関数](02_リファレンス/platform/metrics-query-and-functions.md) |
| Formulas and Functions | 数式と関数 | クエリ結果に対する演算・関数（`anomalies`、`outliers`、`forecast`、`timeshift` 等） | [メトリクスクエリと関数](02_リファレンス/platform/metrics-query-and-functions.md) |
| `as_count()` / `as_rate()` | カウント表示／レート表示 | COUNT・RATE 系メトリクスの表示単位を切り替える修飾子 | [メトリクスクエリと関数](02_リファレンス/platform/metrics-query-and-functions.md) |
| Generate Metrics（log-based / span-based metrics） | メトリクス生成 | ログ・スパン・RUM イベント等からメトリクスを生成する機能。生成したメトリクスはカスタムメトリクスとして計上される | [ログ検索と分析](02_リファレンス/logs/log-search-and-analytics.md)、[APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |
| Estimated Usage Metrics（`datadog.estimated_usage.*`） | 推定使用量メトリクス | 使用量をメトリクスとして推定表示するもの。課金使用量とは平均 10〜20% 異なる | [Usage・Cost Visibility](02_リファレンス/platform/usage-and-cost-attribution.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md) |

---

## 5. モニター・ダッシュボード・SLO・分析ツール

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Monitor | モニター | Datadog に取り込まれたデータを定期評価し、条件を満たすとステータスを `ALERT` / `WARN` / `NO DATA` 等へ遷移させて通知する定義 | [Monitors](02_リファレンス/platform/monitors.md)、[必須概念](01_入門編/05-core-concepts.md) |
| Monitor types（Metric / Anomaly / Outlier / Forecast / Composite / Change / Log / APM / SLO Alerts / Watchdog ほか） | モニタータイプ | 監視対象・方式ごとのモニターの種類。Anomaly は過去パターンからの逸脱、Outlier はグループ内の外れ値、Forecast は将来のしきい値超過予測、Composite は複数モニターの論理式 | [Monitors](02_リファレンス/platform/monitors.md)、[アラート設計とノイズ削減](04_応用編/03-alert-design-and-noise-reduction.md) |
| Simple Alert / Multi Alert | 単一アラート／マルチアラート | すべての報告元を集約して 1 件通知する方式／グループ（ホスト・サービス等）ごとに通知する方式 | [必須概念](01_入門編/05-core-concepts.md)、[Monitors](02_リファレンス/platform/monitors.md) |
| Evaluation window | 評価ウィンドウ | モニターが評価するデータの期間。ローリング（5 分〜カスタム）と累積（Current hour / day / month）がある | [Monitors](02_リファレンス/platform/monitors.md) |
| Evaluation delay / New group delay | 評価遅延／新規グループ遅延 | 遅れて届くデータに備えて評価を遅らせる秒数（最大 86,400 秒）／新規グループの評価開始を遅らせる時間（既定 60 秒） | [Monitors](02_リファレンス/platform/monitors.md) |
| No Data | データなし | 評価対象のデータが届かない状態。扱い（ゼロとみなす、最後の状態を維持、NO DATA 通知など）を設定できる | [Monitors](02_リファレンス/platform/monitors.md) |
| Recovery threshold | 回復しきい値 | アラートから回復したとみなす値。フラッピング防止に使う | [Monitors](02_リファレンス/platform/monitors.md)、[アラート設計とノイズ削減](04_応用編/03-alert-design-and-noise-reduction.md) |
| Priority（P1〜P5） | 優先度 | モニターに任意で付ける優先度。P1 が最高 | [必須概念](01_入門編/05-core-concepts.md) |
| Notification handle（`@slack-…` 等） | 通知ハンドル | モニター等のメッセージ本文に書く `@<連携名>-<値>` 形式の宛先指定 | [通知・コラボレーション連携](02_リファレンス/platform/collaboration-integrations.md)、[通知と Downtime](02_リファレンス/platform/notifications-and-downtimes.md) |
| Template variables / Conditional variables（Monitor） | テンプレート変数／条件変数（通知） | 通知メッセージに値やタグを埋め込む変数（`{{value}}` 等）と、状態に応じて本文を出し分ける変数（`{{#is_alert}}` 等） | [通知と Downtime](02_リファレンス/platform/notifications-and-downtimes.md) |
| Renotify | 再通知 | 問題継続中に間隔を空けて再度通知する設定 | [通知と Downtime](02_リファレンス/platform/notifications-and-downtimes.md) |
| Monitor Notification Rules | モニター通知ルール | タグに基づいてモニター通知の宛先を一元的にルーティングするルール | [通知と Downtime](02_リファレンス/platform/notifications-and-downtimes.md)、[運用設計](03_導入編/13-operations-design.md) |
| Downtime / Mute | ダウンタイム／ミュート | メンテナンス等の期間にモニター通知を抑止する設定（スケジュール、RRULE による繰り返しに対応） | [通知と Downtime](02_リファレンス/platform/notifications-and-downtimes.md) |
| Dashboard | ダッシュボード | ウィジェットを並べ、メトリクス・ログ・トレース等を一画面で可視化する機能。グリッドレイアウトの最大幅は 12 | [Dashboards](02_リファレンス/platform/dashboards.md)、[ダッシュボード設計の実践](04_応用編/04-dashboard-design-practices.md) |
| Timeboard / Screenboard | タイムボード／スクリーンボード | 全体が 1 つの時点を表示する自動レイアウト型／オブジェクトを自由配置するフリーフォーム型の旧来のダッシュボード種別（現行形式に統合） | [Dashboards](02_リファレンス/platform/dashboards.md) |
| Widget | ウィジェット | ダッシュボードの可視化部品（Timeseries、Query Value、Top List、Table、SLO 等） | [Dashboards](02_リファレンス/platform/dashboards.md) |
| Template Variables（Dashboard） | テンプレート変数（ダッシュボード） | ダッシュボード内のウィジェットをタグで動的に絞り込む変数（例：`$env`） | [Dashboards](02_リファレンス/platform/dashboards.md) |
| Powerpack | パワーパック | 複数ウィジェットをまとめて再利用可能にしたテンプレート | [Dashboards](02_リファレンス/platform/dashboards.md) |
| Saved Views | 保存ビュー | Explorer 系画面の検索条件・表示設定を保存したもの | [画面構成とナビゲーション](01_入門編/06-ui-navigation.md)、[ログ検索と分析](02_リファレンス/logs/log-search-and-analytics.md) |
| Shared Dashboards（Public / Invite-only / Embed） | 共有ダッシュボード | Datadog 外へダッシュボードを共有する機能 | [Dashboards](02_リファレンス/platform/dashboards.md) |
| Scheduled Reports | スケジュールレポート | ダッシュボードを定期的に PDF 等で配信する機能 | [Dashboards](02_リファレンス/platform/dashboards.md) |
| Quick Nav（Cmd/Ctrl+K） | クイック検索 | 画面・リソースを横断検索するナビゲーション | [画面構成とナビゲーション](01_入門編/06-ui-navigation.md) |
| Notebooks | ノートブック | テキストとグラフを混在させた調査・ポストモーテム用ドキュメント | [Notebooks・DDSQL・Reference Tables](02_リファレンス/platform/notebooks-and-data-tools.md) |
| Notebooks Analysis Features（旧称：Log Workspaces） | ノートブック分析機能 | ノートブック上で複数データソースを結合・変換して分析する機能 | [Notebooks・DDSQL・Reference Tables](02_リファレンス/platform/notebooks-and-data-tools.md) |
| DDSQL / DDSQL Editor | DDSQL エディタ | SQL 風の構文で Datadog のデータ（インフラリソース、メトリクス等）を問い合わせる機能 | [Notebooks・DDSQL・Reference Tables](02_リファレンス/platform/notebooks-and-data-tools.md) |
| Reference Tables | リファレンステーブル | CSV やクラウドストレージから取り込む参照表。ログ等のエンリッチ（Lookup Processor）に使う | [Notebooks・DDSQL・Reference Tables](02_リファレンス/platform/notebooks-and-data-tools.md) |
| Sheets | シート | スプレッドシート形式で Datadog のデータを加工・分析する機能 | [Notebooks・DDSQL・Reference Tables](02_リファレンス/platform/notebooks-and-data-tools.md) |
| Service Level Objective（SLO） | サービスレベル目標 | 一定期間における SLI の目標割合。期間はローリング 7 / 30 / 90 日、目標値は 100% 未満 | [SLO](02_リファレンス/platform/slo.md)、[SLO 運用の実践](04_応用編/08-slo-practices.md) |
| Metric-based SLO / Monitor-based SLO / Time Slice SLO | メトリクスベース／モニターベース／タイムスライス SLO | Datadog の 3 つの SLO タイプ。件数ベース（良いイベント÷全イベント）、モニターの稼働時間ベース、メトリクスとしきい値による独自のアップタイム定義（モニター不要） | [SLO](02_リファレンス/platform/slo.md)、[オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| Status Corrections | ステータス補正 | 計画メンテナンス等の期間を SLO 計算から除外する機能 | [SLO](02_リファレンス/platform/slo.md) |
| Burn Rate Alert / Error Budget Alert | バーンレートアラート／エラーバジェットアラート | エラーバジェットの消費速度が Long window と Short window の両方でしきい値以上になったら通知するアラート／消費率が設定割合を超えたら通知するアラート（SLO Alerts モニター） | [SLO](02_リファレンス/platform/slo.md)、[オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| Watchdog | ウォッチドッグ | メトリクス・APM・ログ・RUM 等を横断分析し、ベースラインからの逸脱を自動検知する Datadog の AI エンジン。セットアップ不要 | [Watchdog](02_リファレンス/platform/watchdog.md) |
| Watchdog Alerts / Watchdog Monitor | Watchdog アラート／Watchdog モニター | Watchdog が検知した異常の通知と、それを通知に使うモニタータイプ | [Watchdog](02_リファレンス/platform/watchdog.md) |
| Watchdog Insights | Watchdog インサイト | 各 Explorer 上部のカルーセルに、検索条件に合う異常（Anomalies）と外れ値（Outliers）を表示する調査支援機能 | [Watchdog](02_リファレンス/platform/watchdog.md) |
| Watchdog RCA / Impact Analysis | 根本原因分析／影響分析 | Watchdog による根本原因候補の提示と、ユーザー影響の分析 | [Watchdog](02_リファレンス/platform/watchdog.md) |
| Faulty Deployment Detection | 不良デプロイ検知 | デプロイ後に新バージョンの性能を以前のバージョンと比較し、新しいエラー種別やエラー率増加を数分以内に検知する機能（`version` タグで有効） | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md)、[Watchdog](02_リファレンス/platform/watchdog.md) |
| Faulty Cloud & SaaS API Detection | クラウド・SaaS API 障害検知 | 外部クラウド・SaaS API の障害を検知する Watchdog の機能 | [Watchdog](02_リファレンス/platform/watchdog.md) |
| Event Management | イベント管理 | あらゆるソースのイベントを取り込み・正規化（Pipelines）・相関（Correlation）し、Work Item にまとめる機能群。イベントは 15 か月保持 | [Event Management](02_リファレンス/platform/event-management.md) |
| Event Correlation（Pattern-based / Intelligent） | イベント相関 | イベントを Alert に重複排除し、Alert を Work Item にまとめる機能 | [Event Management](02_リファレンス/platform/event-management.md) |
| Triage Inbox | トリアージ受信箱 | 相関で作られた Work Item をトリアージ・調査・エスカレーションする画面 | [Event Management](02_リファレンス/platform/event-management.md) |
| Software Catalog（旧称：Service Catalog） | ソフトウェアカタログ | テレメトリから自動検出したサービスや YAML で宣言したエンティティを一元管理し、オーナー・依存関係・運用情報をライブデータと並べて表示するインベントリ。IDP の中核 | [Software Catalog](02_リファレンス/platform/software-catalog.md) |
| Internal Developer Portal（IDP） | 社内開発者ポータル | Catalog、Scorecards、Self-Service Actions、Engineering Reports 等で構成されるプラットフォームエンジニアリング基盤 | [Software Catalog](02_リファレンス/platform/software-catalog.md) |
| Entity definition（`entity.datadog.yaml`） | エンティティ定義 | Software Catalog にサービス・システム・データストア・キュー・API 等を宣言する YAML（schema v3.0 等） | [Software Catalog](02_リファレンス/platform/software-catalog.md) |
| Scorecards / Campaigns | スコアカード／キャンペーン | エンティティがベストプラクティスを満たすかを pass / fail で評価するルール群と、改善を組織的に進める機能 | [Software Catalog](02_リファレンス/platform/software-catalog.md)、[組織への定着](04_応用編/14-organizational-adoption.md) |
| Self-Service Actions | セルフサービスアクション | App Builder と Workflow Automation で作ったアプリを開発者向けのセルフサービス操作として公開する機能 | [Software Catalog](02_リファレンス/platform/software-catalog.md) |
| Resource Catalog | リソースカタログ | クラウドリソースの一覧・属性・所有者・設定不備を横断的に確認するカタログ | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| Change Tracking | 変更追跡 | デプロイ・設定変更・フィーチャーフラグ変更などの変更イベントをサービスやダッシュボード上に重ねて表示する機能 | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |

---

## 6. Infrastructure（インフラ）

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Infrastructure Monitoring | インフラストラクチャ監視 | ホスト・コンテナ・プロセス・クラウドリソースのメトリクスを集め、可視化・監視する中核製品（Free tier / Basic / Pro / Enterprise） | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md)、[エディション・プラン](03_導入編/04-editions-and-plans.md) |
| Host | ホスト | 公式用語集では「コンピューターまたは仮想マシン」、課金上は「物理または仮想の OS インスタンス」。`host` 予約タグで識別される | [必須概念](01_入門編/05-core-concepts.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Canonical hostname / Host alias | 正規ホスト名／ホストエイリアス | Agent が候補から規則で決めるホスト名と、それ以外の候補名。エイリアスは検索・フィルターには使えない | [必須概念](01_入門編/05-core-concepts.md)、[Agent 設定リファレンス](02_リファレンス/platform/agent-configuration.md) |
| Host List（旧称：Infrastructure List） | ホストリスト | 報告中のホストを一覧する画面 | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| Host Map | ホストマップ | ホストを六角形で並べ、メトリクスで色分けする俯瞰画面 | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| Live Processes | ライブプロセス | ホスト上のプロセスをリアルタイムに一覧・検索する機能（保持 36 時間） | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| Process Check / Live Process Monitor | プロセスチェック／ライブプロセスモニター | `process.up` サービスチェックでプロセスの稼働を見るチェックと、Live Processes のデータでプロセス数を監視するモニター | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| End User Device Monitoring（EUDM） | エンドユーザーデバイス監視 | 従業員の PC の性能・接続性・アプリの問題を可視化する機能【Preview】（`infrastructure_mode: end_user_device`） | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| GPU Monitoring | GPU 監視 | GPU フリートの健全性・性能・コストをワークロードやチームと関連付けて可視化する製品 | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| Cloudcraft | Cloudcraft | クラウド環境の構成図を自動生成する機能（Datadog 内機能と単独版がある） | [Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| Container Monitoring | コンテナ監視 | Docker・Kubernetes・ECS 等のコンテナとオーケストレーターのデータを専用画面で可視化・分析する機能群 | [コンテナ・Kubernetes 監視](02_リファレンス/infrastructure/container-and-kubernetes-monitoring.md) |
| Containers Explorer（旧称：Live Containers） | コンテナエクスプローラー | 実行中コンテナを一覧・検索する画面 | [コンテナ・Kubernetes 監視](02_リファレンス/infrastructure/container-and-kubernetes-monitoring.md) |
| Kubernetes Explorer（旧称：Orchestrator Explorer） | Kubernetes エクスプローラー | Pod・Deployment 等の Kubernetes リソースの状態・YAML を確認する画面 | [コンテナ・Kubernetes 監視](02_リファレンス/infrastructure/container-and-kubernetes-monitoring.md) |
| Container Images Explorer | コンテナイメージエクスプローラー | 使用中のコンテナイメージと脆弱性を確認する画面 | [コンテナ・Kubernetes 監視](02_リファレンス/infrastructure/container-and-kubernetes-monitoring.md) |
| Kubernetes Resource Utilization | Kubernetes リソース使用率 | requests / limits と実使用量を比較してライトサイジングを支援する画面 | [コンテナ・Kubernetes 監視](02_リファレンス/infrastructure/container-and-kubernetes-monitoring.md) |
| Kubernetes Autoscaling（DKA、`DatadogPodAutoscaler`） | Kubernetes オートスケーリング | スケーリング推奨と、`DatadogPodAutoscaler`（DPA）による水平・垂直・多次元の自動スケーリング | [コンテナ・Kubernetes 監視](02_リファレンス/infrastructure/container-and-kubernetes-monitoring.md) |
| Serverless Monitoring | サーバーレス監視 | AWS Lambda / Step Functions、Azure Functions / App Service / Container Apps、Google Cloud Run 等のメトリクス・トレース・ログを関数・アプリ単位で可視化する製品群 | [Serverless Monitoring](02_リファレンス/infrastructure/serverless.md) |
| Datadog Lambda Extension / Lambda Library | Lambda 拡張機能／Lambda ライブラリ | Lambda 関数内で動き、トレース・Enhanced Metrics・カスタムメトリクスを送る拡張機能と、ランタイム別の計装ライブラリ（Layer 等） | [Serverless Monitoring](02_リファレンス/infrastructure/serverless.md) |
| `serverless-init` / Serverless Compatibility Layer | serverless-init | Azure Container Apps や Cloud Run 等のコンテナ型サーバーレスで計装・送信を担うエントリポイント（サイドカー可）と、Azure Functions 等向けの互換レイヤー | [Serverless Monitoring](02_リファレンス/infrastructure/serverless.md) |
| Enhanced Metrics | 拡張メトリクス | Datadog が算出する高粒度のサーバーレスメトリクス（例：`aws.lambda.enhanced.*`） | [Serverless Monitoring](02_リファレンス/infrastructure/serverless.md) |
| Cloud Network Monitoring（CNM、旧称：Network Performance Monitoring / NPM） | クラウドネットワークモニタリング | Agent が収集した接続単位のデータをタグで集約し、通信の依存関係と品質（通信量、TCP 再送、RTT、DNS エラー）を可視化する製品。トラフィックデータは 14 日保持 | [Cloud Network Monitoring](02_リファレンス/infrastructure/cloud-network-monitoring.md) |
| Network Analytics / Network Map | ネットワーク分析／ネットワークマップ | CNM のフロー集計画面と、通信の依存関係を地図表示する画面 | [Cloud Network Monitoring](02_リファレンス/infrastructure/cloud-network-monitoring.md) |
| DNS Monitoring | DNS 監視 | DNS サーバーへの問い合わせ・応答・エラー（NXDOMAIN、SERVFAIL 等）を可視化する CNM の機能 | [Cloud Network Monitoring](02_リファレンス/infrastructure/cloud-network-monitoring.md) |
| Network Path | ネットワークパス | traceroute で送信元から宛先までの経路をホップ単位で可視化する機能 | [Cloud Network Monitoring](02_リファレンス/infrastructure/cloud-network-monitoring.md)、[Synthetic Monitoring](02_リファレンス/dem/synthetic-monitoring.md) |
| Network Device Monitoring（NDM） | ネットワークデバイス監視 | ルーター・スイッチ・ファイアウォール等の機器を、主に SNMP ポーリングで Agent 経由で監視する製品 | [Network Device Monitoring](02_リファレンス/infrastructure/network-device-monitoring.md) |
| SNMP / SNMP Traps / Device Profiles | SNMP／SNMP トラップ／デバイスプロファイル | ネットワーク機器管理プロトコル、機器から送られる非同期通知、機種ごとの収集 OID 定義 | [Network Device Monitoring](02_リファレンス/infrastructure/network-device-monitoring.md) |
| NetFlow Monitoring | NetFlow 監視 | NetFlow v5/v9・IPFIX・sFlow のフロー情報から上位通信元や帯域使用量を分析する機能 | [Network Device Monitoring](02_リファレンス/infrastructure/network-device-monitoring.md) |
| Network Configuration Management（NCM） | ネットワーク構成管理 | ネットワーク機器の設定管理とロールバック | [Network Device Monitoring](02_リファレンス/infrastructure/network-device-monitoring.md) |
| Database Monitoring（DBM） | データベースモニタリング | Agent が読み取り専用ユーザーで DB に接続し、正規化クエリ単位の性能メトリクス、実行中クエリのサンプル、実行計画、待機イベント等を収集する製品 | [Database Monitoring](02_リファレンス/infrastructure/database-monitoring.md) |
| Query Metrics / Query Samples / Explain Plan | クエリメトリクス／クエリサンプル／実行計画 | 正規化クエリ単位の性能指標（15 か月保持）、実行中クエリのスナップショット（15 日保持）、クエリの実行計画 | [Database Monitoring](02_リファレンス/infrastructure/database-monitoring.md) |
| Normalized query | 正規化クエリ | リテラル値を除いて同型のクエリをまとめたもの。DBM の集計・課金上の単位 | [Database Monitoring](02_リファレンス/infrastructure/database-monitoring.md) |
| Cloud Cost Management（CCM） | クラウドコスト管理 | AWS・Azure・Google Cloud・Oracle、SaaS・AI サービス、Custom Costs、Datadog 自身の利用料を取り込み、コストメトリクスとして可視化・配賦・最適化・監視する FinOps 製品 | [Cloud Cost Management](02_リファレンス/infrastructure/cloud-cost-management.md) |
| FOCUS（FinOps Open Cost and Usage Specification） | FOCUS | FinOps Foundation のコストデータ共通仕様。CCM は FOCUS タグを自動付与し、複数事業者を `all.cost` 等で横断クエリできる | [Cloud Cost Management](02_リファレンス/infrastructure/cloud-cost-management.md) |
| CUR（Cost and Usage Report） | コストと使用状況レポート | AWS の請求明細データ。CCM の AWS 取り込み元 | [Cloud Cost Management](02_リファレンス/infrastructure/cloud-cost-management.md) |
| Tag Pipelines | タグパイプライン | CCM でコストデータのタグの欠落・表記揺れを補正するルール | [Cloud Cost Management](02_リファレンス/infrastructure/cloud-cost-management.md)、[タグ戦略の実践](04_応用編/02-tagging-strategy.md) |
| Custom Allocation Rules / Container Cost Allocation | カスタム配賦ルール／コンテナコスト配賦 | 共有コストを分割するルールと、ノード費用を Pod・タスクに配るコンテナ配賦 | [Cloud Cost Management](02_リファレンス/infrastructure/cloud-cost-management.md) |
| Cost Recommendations / Cost Anomalies / Cost Monitor | コスト推奨／コスト異常検知／コストモニター | 削減候補の提示、コストの異常検知、コスト変化の監視モニター | [Cloud Cost Management](02_リファレンス/infrastructure/cloud-cost-management.md) |
| Storage Management | ストレージ管理 | Amazon S3 等のオブジェクトストレージの使用状況・コストを分析する製品 | [Cloud Cost Management](02_リファレンス/infrastructure/cloud-cost-management.md) |

---

## 7. APM（Applications）

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| APM（Application Performance Monitoring） | アプリケーションパフォーマンス監視 | 計装済みアプリケーションから送られる分散トレースを収集・保存・分析する製品（APM / APM Pro / APM Enterprise） | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md)、[APM 運用の実践](04_応用編/05-apm-practices.md) |
| Trace | トレース | 1 つのリクエストの処理時間とステータスを追跡するもの。1 つ以上のスパンで構成される | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Span | スパン | 分散システム内の一定期間の論理的な作業単位 | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Trace root span | ルートスパン | トレースの最初のスパン。エントリーポイントとなるメソッドに当たる | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Service entry span | サービスエントリースパン | あるサービスへのリクエストの入口となるスパン。top-level span とほぼ同義と考えられる【推定】 | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Service | サービス | エンドポイント・クエリ・ジョブ等をまとめる単位。`service` タグで識別され、Software Catalog と Service Map に表示される | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md)、[必須概念](01_入門編/05-core-concepts.md) |
| Resource | リソース | サービス内の特定の処理（Web エンドポイント、DB クエリ、バックグラウンドジョブ）。例：`GET /productpage` | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Operation Name（Span Name） | オペレーション名 | スパンの種類を示す静的な名前（例：`web.request`）。Trace Metrics の名前空間 `trace.<SPAN_NAME>.*` に使われる | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Primary Operation | プライマリオペレーション | サービスのエントリーポイントとなるオペレーション。サービス統計はこの名前のスパンから計算される | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Primary Tag | プライマリタグ | APM の集計統計を環境・AZ 等でスコープするタグ。`env` が必須の既定 Primary Tag | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Trace context propagation / Baggage | トレースコンテキスト伝播／バゲージ | Trace ID 等をサービス間で受け渡してスパンをつなぐ仕組みと、サービス境界を越えて伝播するキー・バリュー | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md)、[APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) |
| Ingestion Controls | インジェスト制御 | Datadog に送るトレースの量を制御する仕組みと画面。送られたトレースは 15 分間の Live Search に使える | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Head-based sampling | ヘッドベースサンプリング | トレースを残すか捨てるかをルートスパンで決め、下流へ伝播する方式。トレースが不完全にならない | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Error sampler / Rare sampler | エラーサンプラー／レアサンプラー | Head-based で捨てられがちなエラートレースや低頻度トレースを Agent が追加で拾う仕組み | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Single Span Sampling | シングルスパンサンプリング | Head-based で捨てられたトレースから個別のスパンだけを拾って取り込む仕組み | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Adaptive Sampling | アダプティブサンプリング | 月間の取り込み量（GB）目標に収まるよう、`env`×`service`×`resource` 単位のサンプリングレートを Datadog が自動調整する機能 | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| `ingestion_reason` | 取り込み理由 | スパンが取り込まれた理由（`auto`、`rule`、`manual`、`single_span` 等）を示すタグ | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Ingested span / Indexed span | 取り込み済みスパン／インデックス済みスパン | Datadog に収集されたすべてのスパン／Retention Filter で保持され検索・監視できるスパン（カスタム保持フィルタは 15 日） | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Retention Filters | リテンションフィルター | どのスパンをインデックスして保持するかを決めるルール。Agent が取り込む量は制御しない | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Intelligent Retention Filter | インテリジェントリテンションフィルター | 多様性サンプリング等で代表的なトレースを自動保持する既定フィルター。保持 30 日で、Indexed Spans の課金に含まれない | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Live Search / Indexed Search | ライブ検索／インデックス検索 | 直近 15 分の全取り込みスパンの検索と、インデックス済みスパンの検索 | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |
| Trace Metrics（`trace.*`） | トレースメトリクス | トレースから自動計算されるヒット数・エラー・レイテンシのメトリクス。サンプリング前の全トラフィックから計算され、15 か月保持 | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md) |
| Span-based Metrics | スパンベースメトリクス | 取り込み済みスパンから任意に生成するメトリクス（カスタムメトリクスとして課金） | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md)、[APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |
| Service Page / Resource Page | サービスページ／リソースページ | サービス・リソースごとのスループット・レイテンシ・エラー率等を表示する画面 | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |
| Service Map | サービスマップ | サービス間の依存関係をリアルタイムで俯瞰する画面 | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |
| Inferred services | 推論サービス | 計装されていない依存先（DB、キュー、サードパーティ等）をスパンから推論して表示するサービス | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md)、[APM 運用の実践](04_応用編/05-apm-practices.md) |
| Trace Explorer / Trace View | トレースエクスプローラー／トレースビュー | スパンを検索・集計する画面と、1 トレースをフレームグラフ・ウォーターフォールで表示する画面 | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |
| Trace Queries | トレースクエリ | 複数スパンの関係（親子・上流下流）でトレースを絞り込む機能 | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |
| Deployment Tracking | デプロイ追跡 | `version` タグでデプロイ前後の性能を比較する機能 | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |
| Endpoints（Endpoint Observability） | エンドポイント一覧 | API エンドポイント単位で性能・所有者を観測する画面 | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md) |
| Flame Graph | フレームグラフ | スパンやスタックの入れ子関係と所要時間を横棒で表す可視化 | [APM 画面と分析機能](02_リファレンス/apm/apm-ui-and-analysis.md)、[Continuous Profiler](02_リファレンス/apm/continuous-profiler.md) |
| Universal Service Monitoring（USM） | ユニバーサルサービスモニタリング | アプリケーションを計装せず、system-probe の eBPF で通信を解析してサービスの RED メトリクスを得る製品 | [Universal Service Monitoring](02_リファレンス/apm/universal-service-monitoring.md) |
| Continuous Profiler | 継続的プロファイラー | 本番環境で常時動作し、CPU・メモリ・I/O・ロック待ち等のボトルネックをメソッド・行の粒度で特定する製品。プロファイルは 8 日保持 | [Continuous Profiler](02_リファレンス/apm/continuous-profiler.md) |
| Profile types（CPU Time / Wall Time / Allocations / Heap / Lock 等） | プロファイル種別 | プロファイラーが取得する資源消費の種類。言語ごとに対応が異なる | [Continuous Profiler](02_リファレンス/apm/continuous-profiler.md) |
| Trace to Profiling integration（通称：Code Hotspots） / Endpoint Profiling | トレースとプロファイルの連携／エンドポイントプロファイリング | スパンから該当コードのプロファイルへ辿る機能と、エンドポイント単位の資源消費分析 | [Continuous Profiler](02_リファレンス/apm/continuous-profiler.md) |
| Profile Comparison / Timeline | プロファイル比較／タイムライン | 期間・バージョン間のプロファイル比較と、スレッド単位の時系列表示 | [Continuous Profiler](02_リファレンス/apm/continuous-profiler.md) |
| Dynamic Instrumentation（DI） | 動的計装 | 稼働中のアプリにコード変更・再デプロイなしで動的スパン・スパンタグ・メトリクスを追加する機能（Remote Configuration で配信） | [Dynamic Instrumentation と Live Debugger](02_リファレンス/apm/dynamic-instrumentation.md) |
| Live Debugger / logpoint | ライブデバッガー／ログポイント | 自動失効する logpoint でログイベントと変数スナップショットを取得する機能 | [Dynamic Instrumentation と Live Debugger](02_リファレンス/apm/dynamic-instrumentation.md) |
| Error Tracking | エラートラッキング | APM・RUM・Logs 等のエラーを類似するもの同士で Issue に自動集約し、トリアージ・修正追跡する製品。単体（Standalone）でも利用可能 | [Error Tracking](02_リファレンス/apm/error-tracking.md) |
| Issue / fingerprint | イシュー／フィンガープリント | Error Tracking でエラーを集約した単位と、グルーピングの識別子（`error.fingerprint`）。すべての Issue は For Review 状態で始まる | [Error Tracking](02_リファレンス/apm/error-tracking.md) |
| Regression | リグレッション | 解決済み Issue の再発 | [Error Tracking](02_リファレンス/apm/error-tracking.md) |
| Suspected Causes / Suspect Commits | 推定原因／疑わしいコミット | Issue の原因カテゴリのラベルと、原因と疑われるコミットの提示 | [Error Tracking](02_リファレンス/apm/error-tracking.md) |
| Exception Replay | 例外リプレイ | 例外発生時のローカル変数等を自動取得して Issue に添付する機能 | [Error Tracking](02_リファレンス/apm/error-tracking.md) |
| Data Streams Monitoring（DSM） | データストリーム監視 | Kafka・RabbitMQ・SQS 等を使うパイプラインのプロデューサー→キュー→コンシューマーの流れを地図化し、エンドツーエンドレイテンシ・Consumer Lag・スループットを測る製品 | [Data Streams Monitoring](02_リファレンス/apm/data-streams-monitoring.md) |
| Pathway context | パスウェイコンテキスト | DSM がメッセージのヘッダーに載せて伝搬させる独自のコンテキスト | [Data Streams Monitoring](02_リファレンス/apm/data-streams-monitoring.md) |
| Consumer Lag | コンシューマーラグ | コンシューマーの処理がプロデューサーの書き込みに対して遅れている量 | [Data Streams Monitoring](02_リファレンス/apm/data-streams-monitoring.md) |

---

## 8. Logs（ログ）

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Log Management | ログ管理 | ログの収集・前処理・インデックス化・長期保管・検索を担う製品。取り込み（Ingest）と保持（Indexing / Storage）を分けて課金する | [ログ収集](02_リファレンス/logs/log-collection.md)、[ログ管理の実践](04_応用編/06-log-management-practices.md) |
| Logging without Limits™ | Logging without Limits | ログの取り込みとインデックス化（保持）を分離する Datadog の考え方。取り込んだ全ログを Live Tail・メトリクス生成・アーカイブに使い、必要なものだけインデックスする | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md)、[コスト最適化](04_応用編/01-cost-optimization.md) |
| Log Collection | ログ収集 | Agent・クラウド転送・HTTP API などでログを Logs インテークへ送る仕組みの総称 | [ログ収集](02_リファレンス/logs/log-collection.md) |
| `log_processing_rules` | ログ処理ルール | Agent 側でログの除外・マスキング・マルチライン集約を行う設定（`exclude_at_match`、`mask_sequences` 等）。送信前に取り込み量を減らせる | [ログ収集](02_リファレンス/logs/log-collection.md) |
| Log Pipelines | ログパイプライン | 取り込んだログを、Indexes 等へ渡す前に Datadog 上で解析・変換・付加情報の追加を行う仕組み。Pipeline とその中で順に実行される Processor で構成される | [Log Pipelines と処理](02_リファレンス/logs/log-pipelines-and-processing.md) |
| Processor | プロセッサー | Pipeline 内の処理部品（Grok Parser、各種 Remapper、Lookup Processor 等） | [Log Pipelines と処理](02_リファレンス/logs/log-pipelines-and-processing.md) |
| Grok Parser | Grok パーサー | 正規表現ベースの規則で非構造ログから属性を抽出するプロセッサー | [Log Pipelines と処理](02_リファレンス/logs/log-pipelines-and-processing.md) |
| Remapper（Attribute / Date / Status / Service / Trace） | リマッパー | 属性を予約属性や別名に対応付けるプロセッサー群 | [Log Pipelines と処理](02_リファレンス/logs/log-pipelines-and-processing.md) |
| Integration Pipeline | インテグレーションパイプライン | `source` に対応して Datadog が自動インストールする読み取り専用 Pipeline | [Log Pipelines と処理](02_リファレンス/logs/log-pipelines-and-processing.md) |
| Attribute / Reserved attributes | 属性／予約属性 | ログ本体の JSON から解析された構造化フィールドと、Datadog が特別に扱う属性（`host`、`source`、`status`、`service`、`trace_id`、`message`） | [必須概念](01_入門編/05-core-concepts.md)、[Log Pipelines と処理](02_リファレンス/logs/log-pipelines-and-processing.md) |
| Standard Attributes / Aliasing | 標準属性／エイリアス | 組織内の属性命名規約の基盤（例：`network.client.ip`）と、非標準の属性・ファセットを標準へ寄せる機能 | [Log Pipelines と処理](02_リファレンス/logs/log-pipelines-and-processing.md)、[ログ管理の実践](04_応用編/06-log-management-practices.md) |
| Facet / Measure | ファセット／メジャー | インデックスされたデータのタグ・属性を絞り込み・集計の軸として定義したもの。定量ファセットをメジャーと呼ぶ。推奨上限は 1,000 程度 | [必須概念](01_入門編/05-core-concepts.md)、[ログ検索と分析](02_リファレンス/logs/log-search-and-analytics.md) |
| Index（Log Indexes） | インデックス | ログを保持期間・日次クォータ・課金の単位で分け、検索・分析可能な状態で保持する入れ物。ログは最初にフィルターが一致した 1 つのインデックスにのみ入る。既定最大 100 | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md)、[必須概念](01_入門編/05-core-concepts.md) |
| Standard Indexing（Standard Tier） | 標準インデックス | 頻繁に検索・アラートするログを短〜中期保持する層。Monitors・Watchdog に対応 | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| Exclusion Filters | 除外フィルター | インデックスに入れないログをクエリとサンプリング率で指定するフィルター。インデックス課金は減るが取り込みは発生済み | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md)、[コスト最適化](04_応用編/01-cost-optimization.md) |
| Daily Quota | 日次クォータ | インデックスあたり 1 日に保存するログ数の上限。既定のリセット時刻は 14:00 UTC | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| Flex Logs（Flex Storage / Flex Compute） | Flex ログ | 保管（Storage）と検索用計算資源（Compute）を分離した長期保持層（最長 15 か月）。即時検索可能だが Monitors・Watchdog 非対応 | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| Flex Logs Starter | Flex Logs Starter | 長期保持用の Flex Logs の簡易版（保持 3 / 6 / 12 / 15 か月） | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md)、[製品別料金表](03_導入編/02-pricing-by-product.md) |
| Flex Frozen | Flex Frozen | Flex Logs の下に位置する、Datadog 内での複数年保持用ストレージ層。Archive Search で検索する | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| Log Archives | ログアーカイブ | 顧客所有のクラウドストレージ（S3 / Azure Storage / GCS）へログを保管する機能 | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| Archive Search | アーカイブ検索 | リハイドレートせずにアーカイブを直接検索し、結果をストリーミング表示する機能。現在アーカイブへのアクセス方法として推奨 | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| Rehydration（Historical Views） | リハイドレーション | アーカイブからログを再取り込みして検索可能にするバッチ処理 | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| Log Forwarding（Custom Destinations） | ログ転送 | 取り込んだログを Splunk・Elasticsearch・SIEM 等の外部宛先へ転送する機能 | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| BYOC Logs（BYOC Log Management、旧称：CloudPrem） | BYOC ログ | ログのインデックス化と保管を顧客自身のインフラで行い、Datadog の UI から検索・分析する Log Management の提供形態 | [Indexes・保持・アーカイブ](02_リファレンス/logs/log-indexes-retention-archives.md) |
| Log Explorer | ログエクスプローラー | ログを検索・絞り込み・集計・可視化する画面。Group into（Fields / Patterns / Transactions）と Visualize as で分析する | [ログ検索と分析](02_リファレンス/logs/log-search-and-analytics.md) |
| Live Tail | ライブテール | 取り込み直後のログを（インデックス有無に関係なく）リアルタイムに表示する機能 | [ログ検索と分析](02_リファレンス/logs/log-search-and-analytics.md) |
| Patterns / Transactions | パターン／トランザクション | 類似ログをまとめて表示する集約と、共通属性でログをまとめて所要時間等を見る集約 | [ログ検索と分析](02_リファレンス/logs/log-search-and-analytics.md) |
| Calculated Fields | 計算フィールド | クエリ時に式で作る一時的なフィールド | [ログ検索と分析](02_リファレンス/logs/log-search-and-analytics.md) |
| Observability Pipelines（OP） | オブザーバビリティパイプライン | ログとメトリクスを顧客自身のインフラ内で収集・加工し、任意の宛先へルーティングする製品。送信前のフィルタリング・サンプリング・マスキング・デュアルシップができる | [Observability Pipelines](02_リファレンス/logs/observability-pipelines.md) |
| Observability Pipelines Worker（OPW） | OP ワーカー | 顧客インフラで Sources・Processors・Destinations を実行する OP のデータプレーン（OSS の Vector が基盤） | [Observability Pipelines](02_リファレンス/logs/observability-pipelines.md) |
| VRL（Vector Remap Language） | VRL | Vector / OP でデータを変換する式言語 | [Observability Pipelines](02_リファレンス/logs/observability-pipelines.md) |
| Packs / Pipeline Simulation | パック／パイプラインシミュレーション | ソース別の処理設定の部品と、デプロイ前に処理結果をスナップショットで検証する機能 | [Observability Pipelines](02_リファレンス/logs/observability-pipelines.md) |

---

## 9. DEM（Digital Experience）

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Digital Experience Monitoring（DEM） | デジタル体験モニタリング | RUM・Session Replay・Product Analytics・Synthetic Monitoring 等、エンドユーザー体験を扱う製品区分 | [製品ポートフォリオ全体像](01_入門編/04-product-map.md) |
| Real User Monitoring（RUM） | リアルユーザーモニタリング | Web・モバイルアプリに SDK を組み込み、実ユーザーのページ表示・操作・通信・エラー等をイベントとして収集する製品 | [RUM（ブラウザ）](02_リファレンス/dem/rum-browser.md)、[RUM（モバイル）](02_リファレンス/dem/rum-mobile.md) |
| RUM events（Session / View / Action / Resource / Error / Long Task / Vital） | RUM イベント | RUM が収集するイベント種別。階層は Session > View > Action / Resource / Error / Long Task | [RUM（ブラウザ）](02_リファレンス/dem/rum-browser.md) |
| Session（RUM） | セッション | 1 ユーザーの一連の操作。15 分の無操作、または 4 時間の連続操作で終了し、課金の単位になる | [RUM（ブラウザ）](02_リファレンス/dem/rum-browser.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Long Task | ロングタスク | メインスレッドを長時間ブロックした処理 | [RUM（ブラウザ）](02_リファレンス/dem/rum-browser.md) |
| Core Web Vitals（LCP / INP / CLS） | コアウェブバイタル | Google が定めた Web 体験指標。LCP は表示速度、INP は応答性、CLS はレイアウトの安定性 | [RUM（ブラウザ）](02_リファレンス/dem/rum-browser.md) |
| Frustration Signals（rage click / dead click / error click） | フラストレーションシグナル | ユーザーの不満を示すクリックパターンを Action に付与する機能 | [RUM（ブラウザ）](02_リファレンス/dem/rum-browser.md) |
| Mobile Vitals / Crash Reporting（ANR / App Hang） | モバイルバイタル／クラッシュレポート | モバイルアプリの性能指標と、クラッシュ・ANR・App Hang 等の収集。シンボルファイル（mapping / dSYM）のアップロードが必要 | [RUM（モバイル）](02_リファレンス/dem/rum-mobile.md) |
| RUM without Limits | RUM without Limits | 全セッションを取り込んで `rum.measure.*` メトリクスを計算し、Retention Filters に一致したセッションのみを RUM Explorer に 30 日保持する方式 | [RUM（ブラウザ）](02_リファレンス/dem/rum-browser.md)、[コスト最適化](04_応用編/01-cost-optimization.md) |
| RUM Measure / RUM Investigate | RUM Measure／RUM Investigate | RUM の 2 つの料金品目。Measure は全トラフィック、Investigate はフィルタ後に保持したセッションが対象 | [製品別料金表](03_導入編/02-pricing-by-product.md)、[エディション・プラン](03_導入編/04-editions-and-plans.md) |
| Session Replay | セッションリプレイ | ブラウザ・モバイルのユーザー操作を記録し動画のように再生する機能（RUM のアドオン）。保持 30 日（延長オプション時 15 か月） | [Session Replay と Product Analytics](02_リファレンス/dem/session-replay-and-product-analytics.md) |
| Privacy level（`defaultPrivacyLevel`） | プライバシーレベル | Session Replay 等で入力値やテキストをマスクする度合いの設定（`mask`、`mask-user-input`、`allow`） | [Session Replay と Product Analytics](02_リファレンス/dem/session-replay-and-product-analytics.md) |
| Product Analytics | プロダクト分析 | RUM と同じ SDK のユーザー行動データで、利用状況・コンバージョン・継続利用（Pathways、Funnel、Retention 等）を分析する製品 | [Session Replay と Product Analytics](02_リファレンス/dem/session-replay-and-product-analytics.md) |
| Heatmaps | ヒートマップ | 画面上のクリック等の集中度を可視化する機能（ブラウザのみ） | [Session Replay と Product Analytics](02_リファレンス/dem/session-replay-and-product-analytics.md) |
| Experiments | 実験 | フィーチャー変更の A/B テストと統計的検定（Eppo が基盤） | [製品ポートフォリオ全体像](01_入門編/04-product-map.md) |
| Synthetic Monitoring（Synthetic Testing and Monitoring） | シンセティックモニタリング（外形監視） | Datadog 管理ロケーションまたは Private Location から模擬リクエスト・模擬操作を定期実行し、可用性と性能を監視する製品 | [Synthetic Monitoring](02_リファレンス/dem/synthetic-monitoring.md) |
| API Test / Multistep API Test / Browser Test | API テスト／マルチステップ API テスト／ブラウザテスト | HTTP・SSL・DNS・TCP・UDP・ICMP・WebSocket・gRPC の単発テスト、複数リクエストの連鎖テスト、ブラウザ操作のテスト | [Synthetic Monitoring](02_リファレンス/dem/synthetic-monitoring.md) |
| Mobile App Testing | モバイルアプリテスト | 実機の iOS / Android 端末でモバイルアプリのテストを実行する機能 | [Synthetic Monitoring](02_リファレンス/dem/synthetic-monitoring.md) |
| Managed locations / Private Locations | 管理ロケーション／プライベートロケーション | Datadog が運用する世界各地のテスト実行拠点と、顧客ネットワーク内に置くワーカー | [Synthetic Monitoring](02_リファレンス/dem/synthetic-monitoring.md) |
| Continuous Testing | 継続的テスト | Synthetic テストを CI/CD パイプラインから（並列）実行する仕組み | [Synthetic Monitoring](02_リファレンス/dem/synthetic-monitoring.md) |
| Journey Monitoring | ジャーニーモニタリング | RUM の操作や Synthetic のテストスイートをユーザージャーニーとして定義し、ジャーニー単位で監視する機能 | [Synthetic Monitoring](02_リファレンス/dem/synthetic-monitoring.md) |

---

## 10. Security（セキュリティ）

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Datadog Security | Datadog セキュリティ | Agent・Log Management・APM・Integrations 上に構築されたセキュリティ製品群の総称（Cloud SIEM、Cloud Security、Workload Protection、App and API Protection、Code Security、AI Guard、Sensitive Data Scanner） | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md) |
| Security Signal | セキュリティシグナル | 進行中の脅威を表す検知結果の共通形式 | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md) |
| Finding | ファインディング（検出結果） | 修正すべき弱点（設定不備・脆弱性等）を表す検知結果の共通形式 | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md) |
| Detection Rules（OOTB / Custom） | 検知ルール | ログ・イベント等を分析してシグナルを生成するルール。Datadog 提供（OOTB）とカスタムがある | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md)、[Cloud SIEM](02_リファレンス/security/cloud-siem.md) |
| Suppressions / Dynamic Severity | 抑制／動的重大度 | 条件に一致するシグナルの生成を抑止する設定と、文脈に応じて重大度を変える機能 | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md)、[セキュリティ運用の実践](04_応用編/11-security-operations-practices.md) |
| Security Inbox | セキュリティ受信箱 | 優先度付けされたセキュリティ課題を集約する画面 | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md)、[Cloud Security](02_リファレンス/security/cloud-security.md) |
| Automation Pipelines | 自動化パイプライン | Findings のミュート・期限設定等を自動化する仕組み | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md) |
| Threat Intelligence（BYOTI） | 脅威インテリジェンス | 既知の悪性 IP・ドメイン等の情報。独自の脅威情報を持ち込む BYOTI にも対応 | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md)、[Cloud SIEM](02_リファレンス/security/cloud-siem.md) |
| Cloud SIEM（旧称：Security Monitoring） | クラウド SIEM | ログ等のテレメトリを検知ルールで継続分析して Security Signal を生成し、調査・対応まで行うセキュリティ分析製品。Log Management が基盤 | [Cloud SIEM](02_リファレンス/security/cloud-siem.md) |
| Content Packs | コンテンツパック | ログソースごとの取り込み設定・検知ルール・ダッシュボード等をまとめたパッケージ | [Cloud SIEM](02_リファレンス/security/cloud-siem.md) |
| Historical Jobs | ヒストリカルジョブ | 過去ログに対して検知ルールを実行（バックテスト）する機能 | [Cloud SIEM](02_リファレンス/security/cloud-siem.md) |
| OCSF（Open Cybersecurity Schema Framework） | OCSF | セキュリティイベントの共通スキーマ。Cloud SIEM はログを OCSF に正規化できる | [Cloud SIEM](02_リファレンス/security/cloud-siem.md) |
| Cloud Security（旧称：Cloud Security Management / CSM） | クラウドセキュリティ | クラウド環境とホスト・コンテナ・Kubernetes を対象に、設定不備・ID リスク・脆弱性を検出し優先度付けする製品（CNAPP に相当） | [Cloud Security](02_リファレンス/security/cloud-security.md) |
| Misconfigurations（CSPM / KSPM） | 設定不備 | クラウド（CSPM）と Kubernetes（KSPM）の設定をコンプライアンスフレームワーク等に照らして評価する Cloud Security の機能 | [Cloud Security](02_リファレンス/security/cloud-security.md) |
| Identity Risks（CIEM） | ID リスク | クラウドの権限・ID の過剰付与等を検出する Cloud Security の機能 | [Cloud Security](02_リファレンス/security/cloud-security.md) |
| Vulnerabilities（Vulnerability Management） | 脆弱性管理 | ホスト・コンテナイメージ・サーバーレスの脆弱性を検出する Cloud Security の機能 | [Cloud Security](02_リファレンス/security/cloud-security.md) |
| Agentless Scanning | エージェントレススキャン | 顧客クラウドアカウント内の専用 VM でディスクスナップショットから SBOM を生成し、脆弱性を検出する仕組み | [Cloud Security](02_リファレンス/security/cloud-security.md)、[アーキテクチャ概観](01_入門編/03-architecture-overview.md) |
| SBOM（Software Bill of Materials） | ソフトウェア部品表 | ソフトウェアに含まれるコンポーネントの一覧（CycloneDX、SPDX 等） | [Cloud Security](02_リファレンス/security/cloud-security.md)、[Code Security](02_リファレンス/security/code-security.md) |
| Workload Protection（旧称：Cloud Workload Security / CWS、CSM Threats） | ワークロード保護 | ホスト・コンテナ・Fargate 上のファイル・ネットワーク・プロセスのアクティビティを Agent でリアルタイム監視し、脅威を検知するランタイムセキュリティ製品。ファイル整合性監視（FIM）を含む。イベントは 90 日保持 | [Workload Protection](02_リファレンス/security/workload-protection.md) |
| Agent Rules（SECL） | エージェントルール | Agent 上でカーネル・OS イベントを評価するルールと、その記述言語 SECL（Security Language） | [Workload Protection](02_リファレンス/security/workload-protection.md) |
| App and API Protection（AAP、旧称：ASM） | アプリケーションと API の保護 | Datadog SDK に組み込まれた In-App WAF で HTTP リクエストを検査し、Web アプリと API への攻撃を検知・ブロックし、API の存在とリスク（API Posture）を可視化する製品。スパンは 90 日保持 | [App and API Protection](02_リファレンス/security/app-and-api-protection.md) |
| In-App WAF | アプリ内 WAF | APM の SDK 内で動作する WAF | [App and API Protection](02_リファレンス/security/app-and-api-protection.md) |
| Exploit Prevention（RASP） | エクスプロイト防御 | アプリ実行時に SQLi・SSRF・LFI・コマンドインジェクション等を検知・ブロックする RASP（Runtime Application Self-Protection）機能 | [App and API Protection](02_リファレンス/security/app-and-api-protection.md) |
| Account Takeover（ATO）protection | アカウント乗っ取り対策 | クレデンシャルスタッフィング等のログイン攻撃を検知・防御する AAP の機能 | [App and API Protection](02_リファレンス/security/app-and-api-protection.md) |
| Code Security | コードセキュリティ | 自社コードと OSS ライブラリの脆弱性・設定ミス・秘密情報漏えいを IDE・PR から本番まで検出する製品群 | [Code Security](02_リファレンス/security/code-security.md) |
| SAST（Static Code Analysis） | 静的コード解析 | リポジトリのソースコードを静的解析して脆弱性・品質問題を検出する | [Code Security](02_リファレンス/security/code-security.md) |
| SCA（Software Composition Analysis：Static / Runtime） | ソフトウェア構成分析 | 依存ライブラリの既知脆弱性・ライセンスを、リポジトリ（Static）または実行中サービス（Runtime）で検出する | [Code Security](02_リファレンス/security/code-security.md) |
| IAST（Runtime Code Analysis） | 対話型アプリケーションセキュリティテスト | 実行中のアプリケーション内でコードの脆弱性を検出する（旧 ASM の Application Vulnerability Management） | [Code Security](02_リファレンス/security/code-security.md) |
| Secret Scanning / IaC Security | シークレットスキャン／IaC セキュリティ | リポジトリ内の秘密情報（API キー等）の検出と、Terraform 等の IaC ファイルの設定不備の検出 | [Code Security](02_リファレンス/security/code-security.md) |
| Supply Chain Firewall（SCFW） | サプライチェーンファイアウォール | 悪性パッケージのインストールを防ぐ Code Security の機能 | [Code Security](02_リファレンス/security/code-security.md) |
| AI Guard | AI ガード | AI アプリ・エージェントの入出力・ツール呼び出しをインラインで検査し、プロンプトインジェクション・ジェイルブレイク・機密データ流出を検出・ブロックする製品 | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md)、[App and API Protection](02_リファレンス/security/app-and-api-protection.md) |
| Sensitive Data Scanner（SDS） | センシティブデータスキャナー | クレジットカード番号・API キー・PII 等の機微データを検出・分類し、必要に応じてマスキングする製品 | [Sensitive Data Scanner](02_リファレンス/security/sensitive-data-scanner.md) |
| Scanning Group / Scanning Rule | スキャングループ／スキャンルール | SDS で対象データ（クエリ）を定める単位と、その中で適用する検出ルール（ライブラリルール約 500 本・カスタム正規表現） | [Sensitive Data Scanner](02_リファレンス/security/sensitive-data-scanner.md) |
| Redact / Partially redact / Hash / Mask | 墨消し／部分マスク／ハッシュ化／マスク | SDS のマスキング動作 | [Sensitive Data Scanner](02_リファレンス/security/sensitive-data-scanner.md) |
| MITRE ATT&CK | MITRE ATT&CK | 攻撃者の戦術・技術の体系。検知ルールの分類に使われる | [Datadog Security 概要](02_リファレンス/security/security-platform-overview.md) |
| Detection as Code | ディテクション・アズ・コード | 検知ルールを Terraform 等でコード管理・レビュー・テストする運用 | [セキュリティ運用の実践](04_応用編/11-security-operations-practices.md) |

---

## 11. Software Delivery

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| CI Visibility（CI Pipeline Visibility / Pipeline Visibility） | CI 可視化 | CI パイプラインの実行結果・所要時間・信頼性を CI プロバイダ横断で収集し、トレース／スパンとして可視化する製品 | [CI Visibility](02_リファレンス/software-delivery/ci-visibility.md) |
| CI/CD Optimization | CI/CD 最適化 | CI Visibility と Test Optimization の画面を統合した UI | [CI Visibility](02_リファレンス/software-delivery/ci-visibility.md) |
| Committer（Active Git committer） | コミッター | CI 系・Code Security 系製品の課金単位。月 3 回以上コミットした一意な Git 作成者（author email で識別） | [CI Visibility](02_リファレンス/software-delivery/ci-visibility.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Test Optimization（旧称：Test Visibility） | テスト最適化 | テストを SDK で自動計装し、テスト単位の結果・所要時間・フレーキー性を可視化・管理する製品 | [Test Optimization](02_リファレンス/software-delivery/test-optimization.md) |
| Flaky test / Flaky Test Management | フレーキーテスト／フレーキーテスト管理 | 同じコードで成功・失敗が揺れる不安定なテストと、その状態（Active / Quarantined / Disabled / Fixed）を管理する機能 | [Test Optimization](02_リファレンス/software-delivery/test-optimization.md) |
| Early Flake Detection（EFD） | 早期フレーク検出 | 新規追加テストを最大 10 回再実行してフレーキー性を早期検出する機能 | [Test Optimization](02_リファレンス/software-delivery/test-optimization.md) |
| Auto Test Retries（ATR） | 自動テスト再試行 | 失敗テストを自動再試行する機能（既定最大 5 回） | [Test Optimization](02_リファレンス/software-delivery/test-optimization.md) |
| Test Impact Analysis（TIA、旧称：Intelligent Test Runner / ITR） | テスト影響分析 | コードカバレッジと変更ファイルから、変更に無関係なテストをスキップする機能 | [Test Optimization](02_リファレンス/software-delivery/test-optimization.md) |
| Code Coverage | コードカバレッジ | テストカバレッジの追跡と PR 上の品質チェック | [DORA Metrics・PR Gates・Code Coverage](02_リファレンス/software-delivery/software-delivery-insights.md) |
| PR Gates（旧称：Quality Gates） | PR ゲート | SAST・SCA・カバレッジ・新規フレーキーテスト等のルールで、基準を満たさない PR のマージをブロックする機能 | [DORA Metrics・PR Gates・Code Coverage](02_リファレンス/software-delivery/software-delivery-insights.md) |
| Deployment Gates | デプロイゲート | モニター状態や Faulty Deployment Detection でデプロイ続行可否を判定する機能 | [DORA Metrics・PR Gates・Code Coverage](02_リファレンス/software-delivery/software-delivery-insights.md) |
| CD Visibility | CD 可視化 | デプロイメント（CD）の実行状況を可視化する機能 | [DORA Metrics・PR Gates・Code Coverage](02_リファレンス/software-delivery/software-delivery-insights.md) |
| DORA Metrics（Delivery Performance） | DORA メトリクス | デプロイ頻度・変更のリードタイム・変更失敗率・復旧時間の 4 指標を計測する機能 | [DORA Metrics・PR Gates・Code Coverage](02_リファレンス/software-delivery/software-delivery-insights.md) |
| Feature Flags | フィーチャーフラグ | テレメトリと連動した段階的ロールアウトのためのフラグ管理 | [製品ポートフォリオ全体像](01_入門編/04-product-map.md) |

---

## 12. Service Management

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Incident Response | インシデントレスポンス | Incident Management と On-Call 等からなる製品群、および料金上のバンドル名 | [Incident Management](02_リファレンス/service-management/incident-management.md)、[On-Call](02_リファレンス/service-management/on-call.md) |
| Incident Management | インシデント管理 | 障害やセキュリティ脅威を「インシデント」として宣言し、対応・調整・記録・事後分析までを Datadog 上で行う製品（シート課金） | [Incident Management](02_リファレンス/service-management/incident-management.md) |
| Severity（SEV-1 等） / Incident Commander（IC） | 重大度／インシデントコマンダー | インシデントの深刻度の区分と、対応を指揮する役割 | [Incident Management](02_リファレンス/service-management/incident-management.md) |
| Postmortem | ポストモーテム | インシデント後の振り返り文書。フォローアップ（再発防止タスク）を伴う | [Incident Management](02_リファレンス/service-management/incident-management.md)、[組織への定着](04_応用編/14-organizational-adoption.md) |
| Status Pages | ステータスページ | 社内・社外向けにシステムの稼働状況を公開するページ（Incident Management の機能） | [Incident Management](02_リファレンス/service-management/incident-management.md) |
| On-Call | オンコール | Page を Team に送り、Routing Rules と Escalation Policy に従って当番者を電話・SMS・プッシュ等で呼び出すオンコール管理製品（シート課金） | [On-Call](02_リファレンス/service-management/on-call.md) |
| Page / Routing Rules / Escalation Policy / Schedule | ページ／ルーティングルール／エスカレーションポリシー／スケジュール | On-Call の呼び出し単位、緊急度と送り先を決めるルール、未応答時に段階的に呼び出す方針、当番表 | [On-Call](02_リファレンス/service-management/on-call.md) |
| Work Management（旧称：Case Management） | ワークマネジメント | 問題・依頼・作業を Work Item（旧称：Case）として一元的にトリアージ・追跡・解決するチケット管理機能。Jira・ServiceNow 等と同期できる | [Work Management](02_リファレンス/service-management/case-management.md) |
| Workflow Automation（Datadog Workflows） | ワークフロー自動化 | アラート・シグナル・スケジュール等をトリガーに、クラウド・SaaS・Datadog への操作（Action）を連鎖実行するローコードの自動化基盤（100 実行単位の課金） | [Workflow Automation](02_リファレンス/service-management/workflow-automation.md) |
| Action Catalog / Connections | アクションカタログ／接続 | 実行可能な操作の一覧と、その接続資格情報 | [Workflow Automation](02_リファレンス/service-management/workflow-automation.md) |
| Private Action Runner（PAR） | プライベートアクションランナー | 社内ネットワーク内のサービスをインターネットに公開せずに操作するための実行エージェント | [Workflow Automation](02_リファレンス/service-management/workflow-automation.md) |
| Blueprints | ブループリント | ワークフロー・アプリのテンプレート | [Workflow Automation](02_リファレンス/service-management/workflow-automation.md)、[App Builder](02_リファレンス/service-management/app-builder.md) |
| App Builder | アプリビルダー | Datadog 内で社内向け運用ツールを作るローコード開発基盤（公開済みアプリ数で課金） | [App Builder](02_リファレンス/service-management/app-builder.md) |
| Datadog Apps | Datadog Apps | アプリをコード（React + TypeScript 等）で開発する App Builder のコードファースト版【Preview】 | [App Builder](02_リファレンス/service-management/app-builder.md) |
| Datastores / Forms | データストア／フォーム | App Builder・Workflow Automation から使う構造化データストアと、入力収集フォーム | [App Builder](02_リファレンス/service-management/app-builder.md) |
| SOAR | セキュリティ運用の自動化 | Security Orchestration, Automation and Response。Datadog では Workflow Automation で実現する | [Workflow Automation](02_リファレンス/service-management/workflow-automation.md)、[セキュリティ運用の実践](04_応用編/11-security-operations-practices.md) |

---

## 13. AI

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Bits AI | Bits AI | Datadog の生成 AI 機能群の総称。チャットで対話する使い方と、タスクを委任する自律エージェントの使い方がある。US1-FED・US2-FED では非対応 | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Bits Chat（旧称：Bits Assistant） | Bits チャット | 自然言語でオブザーバビリティデータを探索・質問するチャット | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Bits Investigation（旧称：Bits AI SRE） | Bits インベスティゲーション | アラートを起点に仮説を立ててテレメトリを収集し、根本原因を自律的に調査する AI エージェント | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Bits Code（旧称：Bits AI Dev Agent） | Bits コード | エラーや性能問題に対するコード修正を自動化する AI エージェント | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Bits Security Analyst | Bits セキュリティアナリスト | Cloud SIEM のシグナルをトリアージ・調査する AI エージェント | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Bits Detection / Bits Remediation | Bits ディテクション／Bits レメディエーション | サービス劣化を自律監視するエージェント／是正アクションを実行するエージェント（DASH 2026 で発表） | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Bits Agent Builder / Skills Library | Bits エージェントビルダー／スキルライブラリ | Action Catalog にアクセスできるカスタム AI エージェントの構築機能と、エージェントに与える手順の集合 | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| AI Credits | AI クレジット | Bits AI 各機能の共通課金単位（月次クレジットバンドルまたはオンデマンド） | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md)、[製品別料金表](03_導入編/02-pricing-by-product.md) |
| Datadog MCP Server | Datadog MCP サーバー | 外部 AI エージェント（Claude Code、Cursor 等）に Datadog のデータとツールを提供する MCP（Model Context Protocol）サーバー | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Natural Language Queries（NLQ） | 自然言語クエリ | 自然言語からクエリを生成する機能 | [Bits AI と AI 機能](02_リファレンス/ai/bits-ai.md) |
| Agent Observability（旧称：LLM Observability） | エージェント オブザーバビリティ | LLM アプリ（チャットボット、RAG、AI エージェント）の LLM 呼び出し・ツール呼び出し・検索等をスパンとして記録し、トークン・コスト・レイテンシ・評価結果を可視化する製品（LLM スパン課金） | [Agent Observability](02_リファレンス/ai/llm-observability.md) |
| `ml_app` | ML アプリ名 | Agent Observability の LLM アプリケーション名。トレースのグルーピングと Data Access Control の単位 | [Agent Observability](02_リファレンス/ai/llm-observability.md) |
| Span kind（llm / workflow / agent / tool / task / embedding / retrieval） | スパン種別 | Agent Observability のスパン分類。ルートスパンになれるのは `llm`・`workflow`・`agent` | [Agent Observability](02_リファレンス/ai/llm-observability.md) |
| Evaluations（LLM-as-a-judge） | 評価 | LLM の出力品質・安全性（ハルシネーション、プロンプトインジェクション等）を評価する機能。LLM を評価者に使う方式を含む | [Agent Observability](02_リファレンス/ai/llm-observability.md) |
| Datasets / Experiments / Playground | データセット／実験／プレイグラウンド | プロンプトやモデルをデータセットで比較評価する機能群 | [Agent Observability](02_リファレンス/ai/llm-observability.md) |
| Prompt injection | プロンプトインジェクション | 入力に命令を紛れ込ませて LLM の挙動を乗っ取る攻撃。AI Guard や Evaluations で検出する | [Agent Observability](02_リファレンス/ai/llm-observability.md)、[Datadog Security 概要](02_リファレンス/security/security-platform-overview.md) |

---

## 14. Data

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Data Observability（DO） | データオブザーバビリティ | 分析・AI 向けデータの信頼性を高め、データパイプラインの性能とコストを最適化する製品群。Quality Monitoring と Jobs Monitoring の両面から観測する | [Data Observability](02_リファレンス/data/data-observability.md) |
| Data Observability: Jobs Monitoring（旧称：Data Jobs Monitoring / DJM） | ジョブ監視 | Spark・Databricks 等のデータ処理ジョブと、Airflow・dbt 等のオーケストレーターのジョブの性能・信頼性・コスト効率を可視化する製品 | [Data Jobs Monitoring](02_リファレンス/data/data-jobs-monitoring.md) |
| Quality Monitoring（Data Quality Monitoring） | データ品質監視 | テーブルの鮮度（Freshness）・件数（Row Count）・スキーマ変更・値の異常を検知する機能（Metaplane が基盤。監視対象テーブル単位で課金） | [Data Observability](02_リファレンス/data/data-observability.md) |
| Data Catalog | データカタログ | 接続したデータ資産の一元的なインベントリ | [Data Observability](02_リファレンス/data/data-observability.md) |
| Lineage（column-level lineage） | データリネージ（カラムリネージ） | データの上流ソースと下流の利用者の依存関係を可視化する機能 | [Data Observability](02_リファレンス/data/data-observability.md) |
| Data Observability Monitor | データオブザーバビリティモニター | データウェアハウスの鮮度・行数・カラムメトリクス・カスタム SQL を監視するモニタータイプ | [Data Observability](02_リファレンス/data/data-observability.md)、[Monitors](02_リファレンス/platform/monitors.md) |
| OpenLineage | OpenLineage | データジョブのリネージ情報を交換するオープン仕様 | [Data Jobs Monitoring](02_リファレンス/data/data-jobs-monitoring.md) |
| DBU（Databricks Unit） | DBU | Databricks の処理量単位。Databricks Serverless の Jobs Monitoring の課金単位 | [Data Jobs Monitoring](02_リファレンス/data/data-jobs-monitoring.md) |

---

## 15. 課金・契約用語

金額は [製品別料金表](03_導入編/02-pricing-by-product.md)（料金の正本）を参照。

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Billing unit | 課金単位 | 製品（SKU）ごとに独立した課金の数え方（ホスト、GB、100 万イベント、1,000 セッション、シート、コミッター等） | [料金体系の全体像](03_導入編/01-pricing-overview.md) |
| SKU | SKU（料金品目） | 料金表上の品目。1 製品に複数 SKU がある場合や、複数製品を束ねたバンドルがある | [製品ポートフォリオ全体像](01_入門編/04-product-map.md)、[エディション・プラン](03_導入編/04-editions-and-plans.md) |
| Annual（billed annually） | 年契約 | 年単位でコミットする契約形態。単価が最も低い | [料金体系の全体像](03_導入編/01-pricing-overview.md)、[購入経路と契約](03_導入編/06-procurement-and-contracts.md) |
| Month-to-month | 月契約 | 月単位の契約形態 | [料金体系の全体像](03_導入編/01-pricing-overview.md) |
| On-demand | オンデマンド | コミットなしの従量単価、または同梱枠とコミットを超えた量。Usage 画面では「ON-DEMAND」と表示 | [料金体系の全体像](03_導入編/01-pricing-overview.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Commitment | コミット | 契約で購入した量。Usage 画面では「COMMITTED」と表示。使用量はコミットで止まらない | [課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Overage | 超過 | 同梱枠とコミットを超えた使用量。オンデマンド単価で課金される | [課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Allotment | 同梱枠（割当量） | ホスト課金製品に付随する無償枠（コンテナ、カスタムメトリクス、Indexed / Ingested Spans 等）。アカウント全体でプールされる。Usage 画面では「ALLOTTED」と表示 | [課金計算の仕組み](03_導入編/03-billing-mechanics.md)、[製品別料金表](03_導入編/02-pricing-by-product.md) |
| High Water Mark Plan（HWMP） / 99th percentile | ハイウォーターマーク方式／99 パーセンタイル | ホスト数を 1 時間ごとに計測し、月末に上位 1% の時間を除いた最大値で課金する方式（30 / 31 日の月は 9 番目、2 月は 8 番目に高い値） | [課金計算の仕組み](03_導入編/03-billing-mechanics.md)、[料金体系の全体像](03_導入編/01-pricing-overview.md) |
| Hybrid Monthly/Hourly Plan（MHP） | ハイブリッド月次／時間課金プラン | 月次の最低コミットを支払い、超えたホスト時間を時間単価で課金する方式 | [課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Billable host | 課金対象ホスト | 課金上のホスト（物理または仮想の OS インスタンス）。製品ごとに別々に数え、`INACTIVE` ホストは対象外。Agent 未導入でもクラウド連携が検出した EC2 は対象 | [課金計算の仕組み](03_導入編/03-billing-mechanics.md)、[Infrastructure Monitoring](02_リファレンス/infrastructure/infrastructure-monitoring.md) |
| Container hours | コンテナ時間 | コンテナ同梱枠（Infrastructure Pro 5 / Enterprise 10 per host、全体でプール）を超えたコンテナの課金単位。コンテナは 5 分ごとに計測 | [課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Ingested Logs / Indexed Logs | 取り込みログ／インデックス済みログ | ログの二段階課金の単位。取り込みは非圧縮 GB、インデックスは 100 万イベント単位・保持期間別単価 | [課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Ingested Spans / Indexed Spans | 取り込みスパン／インデックス済みスパン | APM の課金次元。取り込みは GB、インデックスは件数（APM ホストあたりの同梱枠あり） | [課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Seat | シート | On-Call・Incident Management 等のユーザー単位の課金 | [製品別料金表](03_導入編/02-pricing-by-product.md) |
| Infrastructure Free tier / Basic / Pro / Enterprise | インフラのエディション | Infrastructure Monitoring のティア。Free tier は最大 5 台の Basic ホスト・メトリクス 1 日保持、Basic は非重要ワークロード向け（Contact sales）、Pro / Enterprise はコンテナ・カスタムメトリクス同梱等を含む | [エディション・プラン](03_導入編/04-editions-and-plans.md) |
| DevSecOps Pro / Enterprise | DevSecOps バンドル | Infrastructure Pro / Enterprise と Cloud Security（料金ページ表記：CSM Pro / Enterprise）をホスト単位で一体化した SKU | [エディション・プラン](03_導入編/04-editions-and-plans.md) |
| APM / APM Pro / APM Enterprise | APM のプラン | APM の 3 段階プラン。Pro は Data Streams Monitoring、Enterprise はさらに Continuous Profiler を含む | [エディション・プラン](03_導入編/04-editions-and-plans.md)、[製品ポートフォリオ全体像](01_入門編/04-product-map.md) |
| Free Trial | 無料トライアル | 14 日間の無料試用。終了後は有償プランか Free tier を選ぶ | [エディション・プラン](03_導入編/04-editions-and-plans.md)、[はじめてのDatadog](01_入門編/07-getting-started.md) |
| Datadog for Startups（DDFS） | Datadog for Startups | 初期段階のスタートアップに 1 年間 Datadog を無償提供するプログラム | [エディション・プラン](03_導入編/04-editions-and-plans.md) |
| Plan & Usage（Usage / Bill Overview / Billing History） | プランと使用量 | 使用量・推定コスト・請求履歴を確認する管理画面 | [Usage・Cost Visibility](02_リファレンス/platform/usage-and-cost-attribution.md)、[課金計算の仕組み](03_導入編/03-billing-mechanics.md) |
| Usage Attribution | 使用量属性（タグ別利用量） | 最大 3 つのタグキーで使用量・コストを按分表示する機能（Enterprise プランの機能）。請求額自体は変わらない | [Usage・Cost Visibility](02_リファレンス/platform/usage-and-cost-attribution.md)、[タグ戦略の実践](04_応用編/02-tagging-strategy.md) |
| Cost Summary / Cost Chargebacks | コストサマリー／コストチャージバック | Datadog 利用料の推定・確定コストの表示と、組織別等の配賦表示 | [Usage・Cost Visibility](02_リファレンス/platform/usage-and-cost-attribution.md) |
| Datadog Costs | Datadog コスト | Datadog 自身の日次コストを CCM 上のコストメトリクスとして表示する機能 | [Usage・Cost Visibility](02_リファレンス/platform/usage-and-cost-attribution.md)、[Cloud Cost Management](02_リファレンス/infrastructure/cloud-cost-management.md) |
| Usage Notifications | 使用量通知 | 使用量や契約外製品の初回使用を通知する機能 | [Usage・Cost Visibility](02_リファレンス/platform/usage-and-cost-attribution.md) |
| MSA（Master Subscription Agreement） | 基本サブスクリプション契約 | Datadog の公開基本契約。実際の契約では Order（注文書）や個別条項が優先される | [購入経路と契約](03_導入編/06-procurement-and-contracts.md) |
| Order / Order Term | 注文書／契約期間 | 営業経由の契約で数量・単価・期間を定める文書 | [購入経路と契約](03_導入編/06-procurement-and-contracts.md) |
| DPA（Data Processing Addendum） | データ処理補遺 | 個人データの処理条件を定める契約補遺 | [購入経路と契約](03_導入編/06-procurement-and-contracts.md)、[セキュリティとコンプライアンス](03_導入編/12-security-and-compliance.md) |
| AWS / Azure / Google Cloud Marketplace（Private Offer） | クラウドマーケットプレイス（プライベートオファー） | クラウド事業者のマーケットプレイス経由の購入経路。個別条件の Private Offer やクラウド側コミット（EDP / PPA / MACC）の消化に使える | [購入経路と契約](03_導入編/06-procurement-and-contracts.md) |
| CPPO（Channel Partner Private Offers） | チャネルパートナー・プライベートオファー | 販売パートナーが AWS Marketplace 上で提示するプライベートオファー | [購入経路と契約](03_導入編/06-procurement-and-contracts.md) |
| Datadog Partner Network（DPN） | Datadog パートナーネットワーク | リセラー・サービスパートナー等のパートナー制度 | [購入経路と契約](03_導入編/06-procurement-and-contracts.md) |
| Support Plan（Free / Standard / Premier） | サポートプラン | サポートの段階。Standard は有償エディション契約に含まれ、Premier は有償アドオン（月額支出の 8%、最低 $2,000/月） | [サポートと教育](03_導入編/15-support-and-training.md) |
| TAM（Technical Account Manager） | テクニカルアカウントマネージャー | 技術的な継続支援を行う有償サービスの担当者 | [サポートと教育](03_導入編/15-support-and-training.md) |
| Learning Center / Datadog Certification | ラーニングセンター／認定資格 | 公式の学習コンテンツと認定資格（Datadog Fundamentals 等） | [サポートと教育](03_導入編/15-support-and-training.md)、[はじめてのDatadog](01_入門編/07-getting-started.md) |
| Cardinality explosion | カーディナリティ爆発 | 高カーディナリティタグ（ユーザー ID 等）の付与でカスタムメトリクスの時系列数が急増し、請求が急増する現象 | [よくある失敗](04_応用編/12-common-pitfalls.md)、[コスト最適化](04_応用編/01-cost-optimization.md) |
| Bill shock | 請求急増 | 想定外の使用量増加による請求額の急増 | [よくある失敗](04_応用編/12-common-pitfalls.md) |
| Chargeback / Showback | チャージバック／ショーバック | コストを利用部門に請求すること／請求せず配賦結果を見せること | [タグ戦略の実践](04_応用編/02-tagging-strategy.md)、[Usage・Cost Visibility](02_リファレンス/platform/usage-and-cost-attribution.md) |

---

## 16. オブザーバビリティ一般用語

Datadog 固有ではない一般用語。定義の出典（CNCF、Google SRE Book 等）と確度ラベルは [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) を参照。

| 英語正式名称 | 日本語 | 定義 | 関連ファイル |
|---|---|---|---|
| Observability | オブザーバビリティ（可観測性） | システムの外部出力の知識から内部状態をどの程度推測できるかの尺度（CNCF の定義）【第三者情報】 | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| Monitoring | 監視 | システムに関するリアルタイムの定量データを収集・処理・集計・表示すること（Google SRE Book の定義）【第三者情報】 | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| White-box / Black-box monitoring | ホワイトボックス監視／ブラックボックス監視 | システム内部が公開するメトリクスに基づく監視／ユーザーから見える外部挙動をテストする監視（Synthetic Monitoring が該当） | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| Telemetry | テレメトリ | システムが外部に出力する観測データの総称 | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| Telemetry signals（Metrics / Logs / Traces / Events / Profiles） | テレメトリシグナル | 本ナレッジで整理する 5 つのデータ種別。メトリクス・ログ・トレースが主要シグナル、プロファイル等が新しいシグナル【経験則】 | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| Event | イベント | デプロイ・設定変更・アラート等の頻度の低い離散的な出来事 | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md)、[Event Management](02_リファレンス/platform/event-management.md) |
| Profile | プロファイル | コード（関数・行）単位の CPU・メモリ・ロック等の資源消費の記録 | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md)、[Continuous Profiler](02_リファレンス/apm/continuous-profiler.md) |
| Distributed tracing | 分散トレーシング | 1 リクエストが複数サービスを通過する経路と各処理の時間を、トレース ID でつないで記録する手法 | [APM の概念とインジェスト制御](02_リファレンス/apm/apm-concepts-and-ingestion.md)、[APM 運用の実践](04_応用編/05-apm-practices.md) |
| W3C Trace Context | W3C トレースコンテキスト | トレース ID 等を HTTP ヘッダー（`traceparent`）で伝播する W3C 標準 | [OpenTelemetry サポート](02_リファレンス/platform/opentelemetry.md)、[APM インスツルメンテーション](02_リファレンス/apm/apm-instrumentation.md) |
| Head-based / Tail-based sampling | ヘッドベース／テイルベースサンプリング | トレース開始時に保持可否を決める方式／トレース完了後に内容（エラー・遅延等）を見て決める方式（OTel Collector の tail sampling 等） | [APM 運用の実践](04_応用編/05-apm-practices.md)、[OpenTelemetry 活用戦略](04_応用編/10-opentelemetry-strategy.md) |
| Four Golden Signals | 4 つのゴールデンシグナル | Latency・Traffic・Errors・Saturation（Google SRE Book） | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| RED Method | RED メソッド | サービス向けの Rate・Errors・Duration（Tom Wilkie 氏）。Datadog APM の Trace Metrics と USM で自動的に揃う | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| USE Method | USE メソッド | リソース向けの Utilization・Saturation・Errors（Brendan Gregg 氏） | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| Work metrics / Resource metrics | ワークメトリクス／リソースメトリクス | Datadog「Monitoring 101」の分類。システムが有用な出力を出しているか（Throughput、Success、Error、Performance）と、依存するコンポーネントの状態（Utilization、Saturation、Errors、Availability） | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| SLI（Service Level Indicator） | サービスレベル指標 | サービスの性能・信頼性の定量的な測定値。Datadog ではメトリクスまたは 1 つ以上のモニターの集計 | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md)、[SLO](02_リファレンス/platform/slo.md) |
| SLA（Service Level Agreement） | サービスレベル合意 | 顧客とサービス提供者の間の信頼性に関する合意。通常 SLO より緩く設定する【経験則】 | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| Error Budget | エラーバジェット | 100% − SLO 目標値。許容される非信頼性の量 | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md)、[SLO 運用の実践](04_応用編/08-slo-practices.md) |
| Burn Rate | バーンレート | SLO に対してエラーバジェットを消費する速さ。1 を維持すると期間末にちょうど使い切る | [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md)、[SLO](02_リファレンス/platform/slo.md) |
| Multiwindow, multi-burn-rate alerts | マルチウィンドウ・マルチバーンレートアラート | 長短 2 つのウィンドウと複数のバーンレートしきい値を組み合わせるアラート設計（Google SRE Workbook） | [SLO 運用の実践](04_応用編/08-slo-practices.md) |
| CUJ（Critical User Journey） | クリティカルユーザージャーニー | ユーザーにとって重要な一連の操作。SLI の選定単位に使う | [SLO 運用の実践](04_応用編/08-slo-practices.md) |
| MTTD / MTTR | 平均検知時間／平均復旧時間 | 障害発生から検知まで、検知から復旧までの平均時間。導入効果の指標に使われる | [導入事例](04_応用編/13-case-studies.md)、[Incident Management](02_リファレンス/service-management/incident-management.md) |
| SRE（Site Reliability Engineering） | サイト信頼性エンジニアリング | ソフトウェア工学の手法で運用・信頼性を扱う考え方（SLO、エラーバジェット、ポストモーテム等） | [組織への定着](04_応用編/14-organizational-adoption.md)、[SLO 運用の実践](04_応用編/08-slo-practices.md) |
| Alert fatigue / Flapping | アラート疲れ／フラッピング | 過剰な通知で重要なアラートが見落とされる状態／状態がしきい値付近で頻繁に切り替わること | [アラート設計とノイズ削減](04_応用編/03-alert-design-and-noise-reduction.md) |
| Symptom-based alerting | 症状ベースアラート | ユーザー影響（症状）でアラートし、原因は調査に使う設計原則 | [アラート設計とノイズ削減](04_応用編/03-alert-design-and-noise-reduction.md)、[オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md) |
| eBPF | eBPF | Linux カーネル内で安全にプログラムを実行する技術。Datadog では system-probe が CNM・USM・Workload Protection に使う | [Universal Service Monitoring](02_リファレンス/apm/universal-service-monitoring.md)、[Cloud Network Monitoring](02_リファレンス/infrastructure/cloud-network-monitoring.md) |
| IaC（Infrastructure as Code） / Monitoring as Code | IaC／モニタリング・アズ・コード | インフラや監視設定をコードで宣言・レビュー・適用する手法 | [Terraform と IaC](02_リファレンス/platform/terraform-and-iac.md)、[Monitoring as Code](04_応用編/09-monitoring-as-code.md) |
| Drift | ドリフト | コードで管理する設定と実環境（UI 変更等）の差分 | [Monitoring as Code](04_応用編/09-monitoring-as-code.md) |
| FinOps | FinOps | クラウド費用を可視化・最適化する組織的な実践 | [Cloud Cost Management](02_リファレンス/infrastructure/cloud-cost-management.md)、[コスト最適化](04_応用編/01-cost-optimization.md) |
| SIEM | SIEM | Security Information and Event Management。ログ等を相関分析して脅威を検知する仕組み | [Cloud SIEM](02_リファレンス/security/cloud-siem.md) |
| CNAPP / CSPM / KSPM / CIEM | CNAPP 等 | クラウドネイティブアプリ保護基盤／クラウド・Kubernetes の設定監査／クラウド権限管理を指す業界用語。Datadog Cloud Security が相当する | [Cloud Security](02_リファレンス/security/cloud-security.md) |
| CoE（Center of Excellence） / Platform team | CoE／プラットフォームチーム | 監視基盤の標準化・展開・教育を担う中央チーム | [組織への定着](04_応用編/14-organizational-adoption.md)、[運用設計](03_導入編/13-operations-design.md) |
| Vendor lock-in | ベンダーロックイン | 特定ベンダーの仕様に依存して移行が難しくなる状態。OTel 採用の判断軸 | [OpenTelemetry 活用戦略](04_応用編/10-opentelemetry-strategy.md) |
| PoC（Proof of Concept） | 概念実証 | 本導入前に限定範囲で有効性を検証すること。Datadog では無料トライアルを使うことが多い【経験則】 | [導入方法論](03_導入編/08-implementation-methodology.md) |

---

## 17. 略語索引

| 略語 | 正式名称 | 本ファイルの章 |
|---|---|---|
| AAP | App and API Protection（旧 ASM） | [10](#10-securityセキュリティ) |
| APM | Application Performance Monitoring | [7](#7-apmapplications) |
| ASM | Application Security Management（現 AAP） | [1](#1-製品名の改称履歴旧称現名称) |
| ATO | Account Takeover | [10](#10-securityセキュリティ) |
| ATR | Auto Test Retries | [11](#11-software-delivery) |
| CCM | Cloud Cost Management | [6](#6-infrastructureインフラ) |
| CIEM | Cloud Infrastructure Entitlement Management（現 Identity Risks） | [10](#10-securityセキュリティ) |
| CLC Runner | Cluster Checks Runner | [3](#3-データ収集agent計装opentelemetryintegrations) |
| CNM | Cloud Network Monitoring（旧 NPM） | [6](#6-infrastructureインフラ) |
| CPPO | Channel Partner Private Offers | [15](#15-課金契約用語) |
| CSM | Cloud Security Management（現 Cloud Security） | [1](#1-製品名の改称履歴旧称現名称) |
| CSPM / KSPM | Cloud / Kubernetes Security Posture Management | [10](#10-securityセキュリティ) |
| CUR | Cost and Usage Report | [6](#6-infrastructureインフラ) |
| CWS | Cloud Workload Security（現 Workload Protection） | [1](#1-製品名の改称履歴旧称現名称) |
| DBM | Database Monitoring | [6](#6-infrastructureインフラ) |
| DCA | Datadog Cluster Agent | [3](#3-データ収集agent計装opentelemetryintegrations) |
| DDOT | Datadog Distribution of OpenTelemetry Collector | [3](#3-データ収集agent計装opentelemetryintegrations) |
| DDR | Datadog Disaster Recovery | [2](#2-組織認証サイト) |
| DEM | Digital Experience Monitoring | [9](#9-demdigital-experience) |
| DI | Dynamic Instrumentation | [7](#7-apmapplications) |
| DJM | Data Jobs Monitoring（現 Jobs Monitoring） | [14](#14-data) |
| DKA / DPA | Datadog Kubernetes Autoscaling / DatadogPodAutoscaler | [6](#6-infrastructureインフラ) |
| DSM | Data Streams Monitoring | [7](#7-apmapplications) |
| EFD | Early Flake Detection | [11](#11-software-delivery) |
| EUDM | End User Device Monitoring | [6](#6-infrastructureインフラ) |
| FOCUS | FinOps Open Cost and Usage Specification | [6](#6-infrastructureインフラ) |
| HMI | Historical Metrics Ingestion | [4](#4-タグメトリクス) |
| HWMP | High Water Mark Plan | [15](#15-課金契約用語) |
| IAST | Interactive Application Security Testing（Runtime Code Analysis） | [10](#10-securityセキュリティ) |
| IC | Incident Commander | [12](#12-service-management) |
| IDP | Internal Developer Portal | [5](#5-モニターダッシュボードslo分析ツール) |
| ITR | Intelligent Test Runner（現 TIA） | [1](#1-製品名の改称履歴旧称現名称) |
| KSM | Kubernetes State Metrics | [3](#3-データ収集agent計装opentelemetryintegrations) |
| MCP | Model Context Protocol | [13](#13-ai) |
| MHP | Hybrid Monthly/Hourly Plan | [15](#15-課金契約用語) |
| MSA | Master Subscription Agreement | [15](#15-課金契約用語) |
| MwL | Metrics without Limits | [4](#4-タグメトリクス) |
| NCM | Network Configuration Management | [6](#6-infrastructureインフラ) |
| NDM | Network Device Monitoring | [6](#6-infrastructureインフラ) |
| NLQ | Natural Language Queries | [13](#13-ai) |
| NPM | Network Performance Monitoring（現 CNM） | [1](#1-製品名の改称履歴旧称現名称) |
| OCSF | Open Cybersecurity Schema Framework | [10](#10-securityセキュリティ) |
| OP / OPW | Observability Pipelines / Observability Pipelines Worker | [8](#8-logsログ) |
| OTel / OTLP | OpenTelemetry / OpenTelemetry Protocol | [3](#3-データ収集agent計装opentelemetryintegrations) |
| OTR | One-Time Read | [2](#2-組織認証サイト) |
| PAR | Private Action Runner | [12](#12-service-management) |
| PAT / SAT | Personal Access Token / Service Access Token | [2](#2-組織認証サイト) |
| RASP | Runtime Application Self-Protection | [10](#10-securityセキュリティ) |
| RBAC | Role-Based Access Control | [2](#2-組織認証サイト) |
| RC | Remote Configuration | [3](#3-データ収集agent計装opentelemetryintegrations) |
| RUM | Real User Monitoring | [9](#9-demdigital-experience) |
| SAST / SCA | Static Application Security Testing / Software Composition Analysis | [10](#10-securityセキュリティ) |
| SBOM | Software Bill of Materials | [10](#10-securityセキュリティ) |
| SCFW | Supply Chain Firewall | [10](#10-securityセキュリティ) |
| SDS | Sensitive Data Scanner | [10](#10-securityセキュリティ) |
| SECL | Security Language（Workload Protection の Agent Rules） | [10](#10-securityセキュリティ) |
| SIEM | Security Information and Event Management | [10](#10-securityセキュリティ) |
| SLI / SLO / SLA | Service Level Indicator / Objective / Agreement | [16](#16-オブザーバビリティ一般用語) |
| SOAR | Security Orchestration, Automation and Response | [12](#12-service-management) |
| SSI | Single Step Instrumentation | [3](#3-データ収集agent計装opentelemetryintegrations) |
| TAM | Technical Account Manager | [15](#15-課金契約用語) |
| TIA | Test Impact Analysis（旧 ITR） | [11](#11-software-delivery) |
| USM | Universal Service Monitoring | [7](#7-apmapplications) |
| UST | Unified Service Tagging | [4](#4-タグメトリクス) |
| VRL | Vector Remap Language | [8](#8-logsログ) |
| WIF | Workload Identity Federation | [2](#2-組織認証サイト) |

---

## 参照元

本ファイルの定義は、下記リンク先の各ファイル（およびそれらが引用する出典）を要約したものである。個々の事実の出典は各ファイルの「参照元」を参照すること。

### 本ナレッジ内の主な参照ファイル

- [製品ポートフォリオ全体像](01_入門編/04-product-map.md)（製品一覧・改称履歴）
- [必須概念](01_入門編/05-core-concepts.md)（組織・キー・タグ・ホスト・サービス・メトリクス・ファセット・インデックス・モニター・ダッシュボード・SLO）
- [オブザーバビリティの基礎](01_入門編/02-observability-fundamentals.md)（一般用語・方法論・SLI/SLO）
- [アーキテクチャ概観](01_入門編/03-architecture-overview.md)（Agent 構成・データ経路・保持期間）
- [課金計算の仕組み](03_導入編/03-billing-mechanics.md)、[料金体系の全体像](03_導入編/01-pricing-overview.md)、[製品別料金表](03_導入編/02-pricing-by-product.md)、[エディション・プラン](03_導入編/04-editions-and-plans.md)（課金・契約用語）
- `02_リファレンス/` 配下の各リファレンス（製品別の用語定義）

### Datadog 公式（2026-11-02 取得）

- Datadog Glossary: https://docs.datadoghq.com/glossary/
- APM Terms and Concepts: https://docs.datadoghq.com/tracing/glossary/
- Getting Started with Tags: https://docs.datadoghq.com/getting_started/tagging/
- Billing: https://docs.datadoghq.com/account_management/billing/
- Billing pricing: https://docs.datadoghq.com/account_management/billing/pricing/
- Data Retention Periods: https://docs.datadoghq.com/data_security/data_retention_periods/
- Service Level Objectives: https://docs.datadoghq.com/service_management/service_level_objectives/
- Pricing: https://www.datadoghq.com/pricing/
- Pricing list: https://www.datadoghq.com/pricing/list/
