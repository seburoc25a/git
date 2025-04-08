# **主要なGitホスティングサービスの比較：Azure DevOps Basic、GitHub Enterprise Cloud、GitLab Premium**

**1\. はじめに**

現代のソフトウェア開発環境において、適切なGitホスティングサービスの選択は、チームのコラボレーション、開発速度、そしてプロジェクト全体の成功に不可欠な要素です。この選択は、ソースコードの管理方法だけでなく、継続的インテグレーションと継続的デリバリー（CI/CD）のワークフロー、プロジェクトの組織化、セキュリティ対策にも大きな影響を与えます。本レポートの目的は、主要な3つのGitホスティングサービス、すなわちAzure DevOps（Basicプラン）、GitHub Enterprise Cloud、GitLab Premiumを詳細かつ客観的に比較検討することです。この比較を通じて、組織が自社の特定のニーズと優先順位に最も適したプラットフォームを選択するための実用的な洞察を提供します。比較分析の主要な基準には、Gitホスティング機能、CI/CDの能力、プロジェクト管理ツール、パッケージ管理システム、セキュリティスキャン機能、Amazon Web Services（AWS）との統合、自己ホスト型オプションの利用可能性、そしてそれぞれの価格モデルの複雑さが含まれます。

**2\. GitLab Premiumの主な機能と利点**

GitLab Premiumは、成長する組織のニーズに対応するために設計された、豊富な機能と利点を提供します。これらの機能は、チームの生産性を向上させ、コラボレーションを強化し、ソフトウェア開発ライフサイクル全体を合理化することを目的としています。

* **より迅速なコードレビュー:** GitLab Premiumは、コードレビュープロセスを迅速化し、効率を高めるためのさまざまな機能を提供します。マージリクエストに必要な承認者の最小数を設定する機能により、コード品質が保証されます 1。'Code Owners'機能は、コードの特定のセクションを担当するチームメンバーを自動的にマージリクエストの承認者として割り当てることで、レビュープロセスを効率化し、関連する専門知識を持つ担当者がレビューに参加することを保証します 1。パイプラインページで利用可能な'Code Quality Reports'は、組織のコーディング標準に準拠していないコードベースの領域を強調表示し、潜在的な問題を早期に特定して修正することを可能にします 1。'Merged results pipelines'は、マージされたコードに対して、マスターブランチに統合される前に特別なパイプラインを実行することで、ブランチ上では問題がなくても、統合時に失敗する可能性のある変更を検出するのに役立ちます。これにより、マスターブランチの安定性が維持されます 1。さらに、'Code Review Analytics'は、オープンなマージリクエストのレビュー期間を把握することで、コードレビュープロセスにおけるボトルネックを特定し、対処するのに役立ちます 1。GitLab Premiumは、包括的なコードレビューツールを開発ワークフローに直接組み込むことで、コード品質を優先し、効率的なチームコラボレーションを促進し、より迅速なイテレーションサイクルと技術的負債の削減につながります。自動化されたコードレビューの側面と詳細な分析により、チームは開発速度を犠牲にすることなく、高いコード標準を維持できます 1。  
* **高度なCI/CD:** GitLab Premiumは、基本的な自動化を超えた洗練されたCI/CD機能を提供し、複雑なマルチプロジェクトデプロイメントの管理と、効率的で安全なデリバリーパイプラインの確保を可能にします。'Instance file templates'と'Group file templates'機能を使用すると、LICENSE、.gitignore、Dockerfile、.gitlab-ci.ymlなどの重要なプロジェクトファイルのカスタムテンプレートをインスタンスレベルとグループレベルの両方で定義できます。これにより、組織内のすべてのプロジェクト全体で高いレベルの一貫性と標準化が保証されます 1。'Operations Dashboard'は、GitLabインスタンス内のすべてのプロジェクトとグループ全体のCI/CDパイプラインの履歴と現在のステータスを一元的に視覚化し、デプロイメント状況の比類なき可視性を提供します 1。'Downstream and Multi-project pipeline graphs'は、異なるプロジェクト間のパイプラインがどのように相互接続されているかを視覚的に表現し、プロジェクト間の依存関係を明確に示します。これは、複雑なマイクロサービスアーキテクチャや、複雑な相互依存関係を持つプロジェクトを管理する上で特に価値があります 1。'Fine-grained access controls for CI/CD based Kubernetes deployments'により、Kubernetes RBACを利用してGitLab CI/CDデプロイメントジョブを正確に制限できます。これにより、クラウドネイティブ環境でのデプロイメントのセキュリティと制御が強化されます 1。'Merge Trains'は、パイプラインのキューイングと待ち時間を大幅に削減するように設計された革新的な機能です。マージトレインは、パイプラインの並列実行を可能にすることでこれを実現し、トレイン内の各パイプラインは前のパイプラインのマージ結果に基づいて構築され、コード変更のメインブランチへの統合を大幅に高速化します 1。'Environments Dashboard'は、さまざまな環境（開発、ステージング、本番など）の包括的なクロスプロジェクトの視覚化を提供します。このダッシュボードにより、チームは開発から本番までの変更の流れをシームレスに追跡できるだけでなく、パイプラインのステータスをリアルタイムで可視化し、単一の統合インターフェースから問題を診断できます 1。GitLab Premiumの高度なCI/CD機能は、複雑なソフトウェアデリバリープロセスを持つ大規模な組織が直面する課題に対処します。プロジェクト間の依存関係を視覚化および制御する能力、堅牢なKubernetes統合、および効率を高めるマージトレインにより、デプロイメントパイプラインの効率と信頼性が大幅に向上します 1。  
* **エンタープライズアジャイルデリバリー:** GitLab Premiumは、課題ボード、エピック、ロードマップなどの機能を通じて、エンタープライズグレードのアジャイル手法を包括的にサポートします 2。これにより、複数のプロジェクトにわたる大規模なイニシアチブのより良い計画と追跡が可能になり、進捗状況と依存関係の全体像を提供します。複数の担当者を単一の課題に割り当てる柔軟性により、複数のチームメンバーが同じアイテムに同時に取り組むことができ、タスクの共同所有とより効率的な解決が促進されます 7。GitLab Premiumは、チームレベルとポートフォリオレベルの両方で、アジャイルプロジェクト管理のための堅牢なツールを提供し、チームが作業を効果的に計画、追跡、管理できるようにします 1。エピックやロードマップなどの機能がPremiumティアに含まれていることは、より大規模で戦略的なイニシアチブの計画と実行をサポートすることに重点を置いていることを示しています。これらのツールは、プロジェクトの進捗状況と依存関係の可視性を向上させ、開発努力をビジネス目標と一致させる上で不可欠です。  
* **リリース制御:** GitLab Premiumは、コードレビューのための承認ルールや保護された環境の確立などの機能を通じて、ソフトウェアリリースに対するより厳格な制御を可能にします 7。これにより、承認され、レビューされたコードのみが本番環境にデプロイされることが保証されます。GitLab Premiumは、ソフトウェアデプロイメントに関連する固有のリスクを軽減するのに役立ち、より安定した安全な本番環境を保証します 1。堅牢なリリース制御の実装は、本番システムの安定性とセキュリティを維持するために不可欠です。GitLab Premiumのこの分野の機能により、組織は明確な承認ワークフローを確立し、デプロイメントを保護された環境に制限できるため、エラーや承認されていない変更の可能性が大幅に減少します。  
* **自己管理の信頼性:** GitLabを独自のインフラストラクチャにデプロイおよび管理することを選択した組織向けに、GitLab Premiumは高可用性とディザスタリカバリ機能を提供します 1。これらの機能は、システム障害や停止が発生した場合でも、事業継続性とデータ損失に対する保護を保証するために不可欠です。自己管理デプロイメントの長期的な信頼性と回復力を確保し、ダウンタイムを最小限に抑え、貴重なデータを保護するために、高可用性とディザスタリカバリは不可欠です 1。GitLab Premiumにこれらの機能が含まれていることは、独自の環境内でGitLabをホストすることを好む、または必要とするユーザーにエンタープライズグレードの信頼性を提供するという同社のコミットメントを強調しています。  
* **サポート:** GitLab Premiumサブスクリプションには、優先サポートが含まれています 1。これにより、ユーザーは専用のカスタマーサポートチャネルにアクセスでき、発生する可能性のある問題を迅速に解決し、開発サイクルの中断を最小限に抑えることができます。専用の優先カスタマーサポートへのアクセスは、ミッションクリティカルな開発業務にGitLab Premiumを利用している組織にとって大きなメリットです。安心感と、技術的な課題に対する迅速な解決策を提供します 1。優先サポートにより、Premiumユーザーは必要なときにGitLabのサポートチームからタイムリーかつ効率的な支援を受けることができ、生産性を維持し、プロジェクトのタイムラインと成果物への技術的な問題の影響を最小限に抑えることができます。  
* **コンピューティング時間:** GitLab Premiumには、月あたり10,000分のコンピューティング時間が含まれています 1。これらの時間は、GitLabのホストされたランナーでCI/CDパイプラインを実行するための消費単位であり、ビルド、テスト、およびデプロイメントプロセスを自動化するための十分な容量を提供します。このコンピューティング時間の割り当ては、通常、中程度のCI/CDワークロードを持つ組織に適しており、ソフトウェアデリバリーパイプラインの重要な側面を自動化することができます 1。含まれているコンピューティング時間は、開発チームにとって貴重なリソースであり、追加費用をすぐに発生させることなく、ソフトウェア開発ライフサイクルの主要な側面を自動化することを可能にします。この割り当ては、GitLab Premiumプランの全体的な価値提案の重要な構成要素です。

**4\. GitLab Premiumの料金体系**

GitLab Premiumの料金体系は、いくつかの側面で構成されており、組織は自社の特定のニーズと予算に基づいてコストを評価できます。

* **基本料金:** GitLab Premiumの標準リスト価格は、月あたり1ユーザーあたり29ドルで、年間契約で請求されます 1。この年間請求モデルは、より長期的な契約へのコミットメントを示しており、特に多数のユーザーがいる組織にとっては、かなりの財政支出となる可能性があります 1。年間請求は、月額サブスクリプションと比較して有効な月額コストが低くなる可能性がありますが、より大きな初期投資と長期的なプラットフォーム利用の確実性を必要とします。組織は、予算サイクルと予想される成長を慎重に検討する必要があります。  
* **一時的な移行価格:** 2024年4月2日まで、既存のGitLab Premiumサブスクライバーの対象となる今後の更新には、月あたり1ユーザーあたり24ドルの一時的な移行価格が自動的に適用されました 3。この一時的な値下げは、発表された価格引き上げに対する直接的な対応であり、既存顧客への財政的影響を緩和し、移行期間中の顧客離れを潜在的に軽減することを目的としていました 3。価格引き上げは、特に確立されたサービスの場合、多くの場合、ユーザーの不満と代替手段の再評価につながる可能性があります。一時的な移行価格を実施することで、GitLabは既存のPremiumユーザーベースを維持し、新しい価格体系への調整期間を提供することを目指しました。  
* **追加のCI/CD時間:** 月あたりの割り当てられた10,000分のコンピューティング時間超過した場合、追加の時間は1,000分あたり10ドルの料金で購入できます 6。この従量課金制の追加CI/CDリソースの購入モデルは、変動する、または特に要求の厳しいCI/CDワークロードを持つ組織に、潜在的に未使用の機能を持つより高価なプランにアップグレードする必要なく、使用量をスケーリングする柔軟性を提供します 6。CI/CDパイプラインの実行時間が大幅に変動する、または一貫して使用量が多い組織は、必要に応じて追加のコンピューティング時間を購入できるという利点があります。このオンデマンドのスケーラビリティは、実際に消費するリソースに対してのみ料金を支払うことで、コストを最適化するのに役立ちます。  
* **追加ストレージ:** Premiumプランに含まれる50GBのストレージを超えるストレージが必要な組織の場合、追加ストレージは年間10GBあたり60ドルの費用で利用できます 6。特に大規模なコードベースを管理している、豊富なビルド成果物を保持している、または多数のソフトウェアパッケージをホストしている組織は、この追加ストレージ費用を全体的なコスト評価の一部として考慮する必要があります 6。ソフトウェア開発プロジェクトのストレージ要件は、プロジェクトのサイズ、リポジトリの数、ビルド成果物の保持ポリシーなどの要因によって大きく異なる可能性があります。かなりのストレージニーズを予測している組織は、GitLab Premiumを検討する際にこの追加コストを慎重に評価する必要があります。  
* **割引:** GitLabは、スタートアップ、教育機関、非営利団体などの特定のカテゴリーのユーザーに割引価格を提供する場合があります 11。さらに、大規模なデプロイメントまたは長期契約の場合、ボリュームディスカウントも交渉可能かもしれません 11。利用可能な割引について積極的に問い合わせて、潜在的にそれらを確保することは、特に適格な組織や大規模なデプロイメントを検討している組織にとって、GitLab Premiumサブスクリプションの全体的なコストを大幅に削減する可能性があります 11。これらのカテゴリーに該当する組織は、GitLabの営業チームに利用可能な割引について積極的に問い合わせる必要があります。同様に、多数のユーザーまたは複数年契約を計画している組織は、潜在的なボリュームディスカウントについて問い合わせて、投資を最適化する必要があります。  
* **AWS Marketplace:** GitLab Premiumは、Amazon Web Services（AWS）Marketplaceを通じて購入することもできます 17。これにより、実際の消費量に合わせた従量課金制や従来の年間契約オプションなど、柔軟な価格モデルが組織に提供されます。AWS Marketplaceを通じて購入すると、組織のAWSプラットフォームへのコミットされた支出にも貢献する可能性があります 17。確立されたAWSアカウントを持ち、AWSサービスに依存している組織にとって、AWS Marketplaceを通じてGitLab Premiumを購入すると、ベンダー管理と請求プロセスが合理化されます。さらに、既存のAWS支出コミットメントや割引を利用して、全体的なコストを潜在的に削減できる可能性があります。

**5\. 機能の比較分析**

以下の表は、Azure DevOps Basic、GitHub Enterprise Cloud、GitLab Premiumの主要な機能を、指定されたカテゴリにわたって比較したものです。

**表1：機能比較**

| 機能 | Azure DevOps Basic | GitHub Enterprise Cloud | GitLab Premium |
| :---- | :---- | :---- | :---- |
| Gitホスティング | 無制限のプライベートGitリポジトリ | 無制限のプライベートGitリポジトリ 17 | 無制限のプライベートGitリポジトリ 8 |
| CI/CD | Azure Pipelines（無料枠を含む：Microsoftホスト型ジョブ1つ、月あたり1,800分。セルフホスト型ジョブ1つ、無制限） 31 | GitHub Actions（プライベートリポジトリ向けに、標準GitHubホスト型ランナーで月あたり50,000分の無料時間を含む） 27 | 高度なCI/CD（月あたり10,000分のコンピューティング時間を含む） 1 |
| プロジェクト管理 | Azure Boards（かんばん、スクラム、カスタマイズ可能なダッシュボード） 51 | GitHub Projects（タスク追跡、ボード、自動化） 54 | エンタープライズアジャイルデリバリー（課題ボード、エピック、ロードマップ、複数担当者） 1 |
| パッケージ管理 | Azure Artifacts（NuGet、npm、Maven、Pythonをサポート；組織あたり2GBまで無料） 31 | GitHub Packages（Docker、npm、Maven、NuGet、RubyGems、Swiftをサポート；プライベートリポジトリ向けに50GBまで無料） 27 | 組み込みパッケージレジストリ（複数の形式をサポート） 1 |
| セキュリティスキャン | 基本機能を含む（例：脆弱性スキャン、監査ログ） 52 | GitHub Advanced Security（シークレットスキャン、コードスキャン、依存関係スキャンを含むアドオン） 51 | 依存関係スキャン、コンテナスキャン、コード品質レポート 1 |
| AWS統合 | AWS Toolkit for Azure DevOps（AWSサービス管理用の拡張機能） 75 | AWS Connector for GitHub（リポジトリイベントに関するAWS通知を有効化） 78 | デプロイメントの直接統合、AWS Marketplaceでの利用可能性 17 |
| 自己ホスト型オプション | Azure DevOps Server（オンプレミスソリューション） 51 | GitHub Enterprise Server（GitHubの自己ホスト型バージョン） 28 | 自己管理オプションあり 1 |

この機能比較は、3つのプラットフォームすべてが包括的であり、ソフトウェア開発ライフサイクル全体にわたる堅牢なツールセットを提供していることを明確に示しています。違いは、各カテゴリ内の特定の機能とその機能の深さにあります。基本的な機能（GitホスティングやCI/CDなど）は3つすべてに存在しますが、追加の機能（プロジェクト管理ツールの洗練度や組み込みのセキュリティ機能の範囲など）の特定の実装と機能は大きく異なる可能性があります。たとえば、特定のアジャイル手法を強く希望する組織はAzure Boardsが特に適していると感じるかもしれませんが、統合されたDevSecOpsプラットフォームを優先する組織はGitLab Premiumに傾倒するかもしれません。同様に、外部サービスとの統合レベルやアクセス制御の粒度は、組織の既存のインフラストラクチャとコンプライアンス要件に応じて決定的な要因となる可能性があります。

**6\. 価格モデルの比較分析**

以下の表は、3つのサービスの価格モデルを比較したものです。

**表2：価格モデルの比較**

| 価格要素 | Azure DevOps Basic | GitHub Enterprise Cloud | GitLab Premium |
| :---- | :---- | :---- | :---- |
| 基本料金（ユーザーあたり/月） | 6ドル（最初の5ユーザーは無料） 51 | 21ドル（初年度）、その後は営業にお問い合わせください 28 | 29ドル（年間請求） 1 |
| CI/CD追加費用 | 40ドル/月（Microsoftホスト型並列ジョブ）、15ドル/月（セルフホスト型並列ジョブ）（無料枠を超過後） 51 | ランナーの種類に応じた分単位の料金（50,000分の無料時間超過後） 47 | 1,000分あたり10ドル（10,000分の無料時間超過後） 6 |
| ストレージ追加費用 | 2ドル/GB/月～（2GB無料超過後） 51 | 0.25ドル/GB/月（50GB無料超過後） 56 | 10GBあたり年間60ドル（50GB無料超過後） 6 |
| 高度なセキュリティ費用 | 49ドル/コミッター/月（アドオン：GitHub Advanced Security for Azure DevOps） 51 | シークレット保護：19ドル/コミッター/月、コードセキュリティ：30ドル/コミッター/月（アドオン：GitHub Advanced Security） 28 | より上位のティア（Ultimate）に含まれる 6 |

価格モデルの比較分析は、明確なアプローチの違いを示しています。Azure DevOps Basicは、特に小規模なチームやDevOpsプラクティスの導入初期段階にあるチームにとって、その寛大な無料枠により、非常に魅力的な参入地点を提供します。対照的に、GitHub Enterprise CloudとGitLab Premiumは、より高い開始価格であるものの、より包括的な機能セットを基本プランに含んでおり、より洗練された要件を持つ組織にとって、より大きな固有の価値を提供する可能性があります。CI/CD時間とストレージの含まれるクォータを超過した場合の追加費用、および高度なセキュリティ機能の価格体系は、3つのプラットフォーム間で異なっており、予想される使用パターンとセキュリティの優先順位に基づいて慎重な評価が必要となります。

**7\. 包括的な比較表**

以下の表は、前述の2つの表を統合し、より詳細な比較を可能にするものです。

| 機能/価格要素 | Azure DevOps Basic | GitHub Enterprise Cloud | GitLab Premium |
| :---- | :---- | :---- | :---- |
| Gitホスティング | 無制限のプライベートGitリポジトリ | 無制限のプライベートGitリポジトリ | 無制限のプライベートGitリポジトリ |
| CI/CD | Azure Pipelines（無料枠あり） | GitHub Actions（無料枠あり） | 高度なCI/CD（月あたり10,000分のコンピューティング時間を含む） |
| プロジェクト管理 | Azure Boards | GitHub Projects | エンタープライズアジャイルデリバリー |
| パッケージ管理 | Azure Artifacts（2GB無料） | GitHub Packages（50GB無料） | 組み込みパッケージレジストリ |
| セキュリティスキャン | 基本機能を含む | GitHub Advanced Security（アドオン） | 依存関係/コンテナスキャン、コード品質レポート |
| AWS統合 | AWS Toolkit for Azure DevOps | AWS Connector for GitHub | 直接統合、AWS Marketplace |
| 自己ホスト型オプション | Azure DevOps Server | GitHub Enterprise Server | 自己管理オプションあり |
| 基本料金（ユーザーあたり/月） | 6ドル（最初の5ユーザーは無料） | 21ドル（初年度）、その後は営業にお問い合わせ | 29ドル（年間請求） |
| CI/CD追加費用 | 40ドル/月（Microsoftホスト型）、15ドル/月（セルフホスト型） | ランナーの種類に応じた分単位の料金 | 1,000分あたり10ドル |
| ストレージ追加費用 | 2ドル/GB/月～ | 0.25ドル/GB/月 | 10GBあたり年間60ドル |
| 高度なセキュリティ費用 | 49ドル/コミッター/月（アドオン） | シークレット保護：19ドル/コミッター/月、コードセキュリティ：30ドル/コミッター/月（アドオン） | より上位のティア（Ultimate）に含まれる |

この統合された表は、包括的で理解しやすい比較のための強力なツールとして機能します。機能とその関連コストを並べて提示することで、ユーザーは3つのGitホスティングサービスが提供する全体的な価値提案を効率的に評価できます。この形式は、ユーザーのspreadsheet互換の比較表の要求に直接応えるものです。

**8\. 結論**

本レポートでは、Azure DevOps Basic、GitHub Enterprise Cloud、GitLab Premiumという3つの主要なGitホスティングサービスを詳細に比較検討しました。3つのプラットフォームはそれぞれ、ソフトウェア開発ライフサイクルをサポートするための包括的な機能セットを提供していますが、機能の深さ、価格モデル、および特定の組織のニーズへの適合性には重要な違いが見られました。

Azure DevOps Basicは、特に小規模なチームやDevOpsの導入初期段階にある組織にとって、無料枠が充実しているため、コスト効率の高い選択肢となります。ただし、高度なセキュリティ機能や大規模なエンタープライズ向けの機能は、より上位のプランやアドオンに限定されます。

GitHub Enterprise Cloudは、大規模な組織や、高度なセキュリティ、コンプライアンス、および管理機能を必要とする企業に適しています。初年度の割引価格は魅力的ですが、その後の価格については営業担当者への問い合わせが必要であり、長期的なコストを予測するには注意が必要です。

GitLab Premiumは、バランスの取れた機能と価格設定を提供し、成長する組織や、高度なCI/CD機能、エンタープライズアジャイルプランニング、リリース制御を必要とするチームに適しています。年間請求モデルは長期的なコミットメントを必要としますが、追加リソースの柔軟な購入オプションも用意されています。

最終的な選択を行う際には、各組織は自社の具体的なチームのニーズ、プロジェクトの要件、長期的な戦略目標、そして予算制約を慎重に考慮する必要があります。このレポートで提供された詳細な比較と分析が、情報に基づいた意思決定を行うための一助となれば幸いです。

#### **引用文献**

1. Why GitLab Premium?, 4月 8, 2025にアクセス、 [https://about.gitlab.com/pricing/premium/](https://about.gitlab.com/pricing/premium/)  
2. 5 GitLab Premium features to help your team scale, 4月 8, 2025にアクセス、 [https://about.gitlab.com/blog/2024/12/18/5-gitlab-premium-features-to-help-your-team-scale/](https://about.gitlab.com/blog/2024/12/18/5-gitlab-premium-features-to-help-your-team-scale/)  
3. Why upgrade to GitLab Premium?, 4月 8, 2025にアクセス、 [https://about.gitlab.com/pricing/premium/why-upgrade/](https://about.gitlab.com/pricing/premium/why-upgrade/)  
4. Self-Managed Feature Comparison \- GitLab, 4月 8, 2025にアクセス、 [https://about.gitlab.com/pricing/feature-comparison/](https://about.gitlab.com/pricing/feature-comparison/)  
5. Why GitLab Ultimate?, 4月 8, 2025にアクセス、 [https://about.gitlab.com/pricing/ultimate/](https://about.gitlab.com/pricing/ultimate/)  
6. What is GitLab? GitLab Pricing – Actual Prices for All Plans | Admina blog, 4月 8, 2025にアクセス、 [https://admina.moneyforward.com/us/blog/what-is-gitlab-gitlab-pricing-actual-prices-for-all-plans](https://admina.moneyforward.com/us/blog/what-is-gitlab-gitlab-pricing-actual-prices-for-all-plans)  
7. Features by Tier \- GitLab, 4月 8, 2025にアクセス、 [https://about.gitlab.com/features/by-paid-tier/](https://about.gitlab.com/features/by-paid-tier/)  
8. Pricing \- GitLab, 4月 8, 2025にアクセス、 [https://about.gitlab.com/pricing/](https://about.gitlab.com/pricing/)  
9. GitLab Pricing – Actual Prices for All Plans, Including Enterprise \- RevPilots, 4月 8, 2025にアクセス、 [https://revpilots.com/pricing/gitlab-pricing/](https://revpilots.com/pricing/gitlab-pricing/)  
10. GitLab Software Pricing & Plans 2025 \- Vendr, 4月 8, 2025にアクセス、 [https://www.vendr.com/marketplace/gitlab](https://www.vendr.com/marketplace/gitlab)  
11. GitLab Pricing: Plans, Features, and Savings Tips \- Spendflo, 4月 8, 2025にアクセス、 [https://www.spendflo.com/blog/gitlab-pricing-guide](https://www.spendflo.com/blog/gitlab-pricing-guide)  
12. GitLab Premium Update, 4月 8, 2025にアクセス、 [https://about.gitlab.com/pricing/faq-premium-update/](https://about.gitlab.com/pricing/faq-premium-update/)  
13. New pricing for GitLab Premium, 4月 8, 2025にアクセス、 [https://about.gitlab.com/blog/2023/03/02/gitlab-premium-update/](https://about.gitlab.com/blog/2023/03/02/gitlab-premium-update/)  
14. Is GitLab Premium worth it at its new price? : r/devops \- Reddit, 4月 8, 2025にアクセス、 [https://www.reddit.com/r/devops/comments/11gadwc/is\_gitlab\_premium\_worth\_it\_at\_its\_new\_price/](https://www.reddit.com/r/devops/comments/11gadwc/is_gitlab_premium_worth_it_at_its_new_price/)  
15. Tell HN: Gitlab Premium pricing increases incoming $19 to $29 | Hacker News, 4月 8, 2025にアクセス、 [https://news.ycombinator.com/item?id=34998255](https://news.ycombinator.com/item?id=34998255)  
16. GitLab Premium \- subscription license (1 year) \- 1 user \- Insight, 4月 8, 2025にアクセス、 [https://www.insight.com/en\_US/shop/product/PREM-SM-1/gitlab%20bv/PREM-SM-1/GitLab-Premium-subscription-license-1-year-1-user/](https://www.insight.com/en_US/shop/product/PREM-SM-1/gitlab%20bv/PREM-SM-1/GitLab-Premium-subscription-license-1-year-1-user/)  
17. AWS Marketplace: GitLab Premium Self-Managed, 4月 8, 2025にアクセス、 [https://aws.amazon.com/marketplace/pp/prodview-vehcu2drxakic](https://aws.amazon.com/marketplace/pp/prodview-vehcu2drxakic)  
18. Purchase additional compute minutes \- GitLab Docs, 4月 8, 2025にアクセス、 [https://docs.gitlab.com/subscriptions/gitlab\_com/compute\_minutes/](https://docs.gitlab.com/subscriptions/gitlab_com/compute_minutes/)  
19. The Rising Cost of GitLab: What You Need to Know About Their Billing Practices \- Medium, 4月 8, 2025にアクセス、 [https://medium.com/@focusfaithfirst/the-rising-cost-of-gitlab-what-you-need-to-know-about-their-billing-practices-cb6bbc3549eb](https://medium.com/@focusfaithfirst/the-rising-cost-of-gitlab-what-you-need-to-know-about-their-billing-practices-cb6bbc3549eb)  
20. Compute minutes \- GitLab Docs, 4月 8, 2025にアクセス、 [https://docs.gitlab.com/ci/pipelines/compute\_minutes/](https://docs.gitlab.com/ci/pipelines/compute_minutes/)  
21. Gitlab CI Capacity/Cost Analysis \- Reddit, 4月 8, 2025にアクセス、 [https://www.reddit.com/r/gitlab/comments/17nv9li/gitlab\_ci\_capacitycost\_analysis/](https://www.reddit.com/r/gitlab/comments/17nv9li/gitlab_ci_capacitycost_analysis/)  
22. GitLab Paid storage update psa : r/devops \- Reddit, 4月 8, 2025にアクセス、 [https://www.reddit.com/r/devops/comments/yw1pw3/gitlab\_paid\_storage\_update\_psa/](https://www.reddit.com/r/devops/comments/yw1pw3/gitlab_paid_storage_update_psa/)  
23. Self-Hosted GitLab CE vs. GitLab Premium: What to Choose? \- Mad Devs, 4月 8, 2025にアクセス、 [https://maddevs.io/blog/how-do-we-save-about-10000-a-year-using-self-hosted-gitlab/](https://maddevs.io/blog/how-do-we-save-about-10000-a-year-using-self-hosted-gitlab/)  
24. GitLab Premium \- AWS Marketplace, 4月 8, 2025にアクセス、 [https://aws.amazon.com/marketplace/pp/prodview-amk6tacbois2k](https://aws.amazon.com/marketplace/pp/prodview-amk6tacbois2k)  
25. Purchase GitLab through Cloud Marketplaces seamlessly, 4月 8, 2025にアクセス、 [https://page.gitlab.com/cloud-partner-marketplaces.html](https://page.gitlab.com/cloud-partner-marketplaces.html)  
26. How Much Do Azure DevOps Services Cost – Your 2025 Guide \- Anodot, 4月 8, 2025にアクセス、 [https://www.anodot.com/blog/azure-devops-pricing/](https://www.anodot.com/blog/azure-devops-pricing/)  
27. GitHub's plans \- GitHub Enterprise Cloud Docs, 4月 8, 2025にアクセス、 [https://docs.github.com/enterprise-cloud@latest/get-started/learning-about-github/githubs-plans](https://docs.github.com/enterprise-cloud@latest/get-started/learning-about-github/githubs-plans)  
28. Pricing · Plans for every developer \- GitHub, 4月 8, 2025にアクセス、 [https://github.com/pricing](https://github.com/pricing)  
29. FAQ about changes to GitHub's plans \- GitHub Enterprise Cloud Docs, 4月 8, 2025にアクセス、 [https://docs.github.com/enterprise-cloud@latest/get-started/learning-about-github/faq-about-changes-to-githubs-plans](https://docs.github.com/enterprise-cloud@latest/get-started/learning-about-github/faq-about-changes-to-githubs-plans)  
30. GitHub's plans, 4月 8, 2025にアクセス、 [https://docs.github.com/get-started/learning-about-github/githubs-products](https://docs.github.com/get-started/learning-about-github/githubs-products)  
31. What are the Benefits of Azure DevOps? | A Quick Guide \- Veritis, 4月 8, 2025にアクセス、 [https://www.veritis.com/blog/what-are-the-benefits-of-azure-devops/](https://www.veritis.com/blog/what-are-the-benefits-of-azure-devops/)  
32. What is Azure DevOps? \- Azure DevOps | Microsoft Learn, 4月 8, 2025にアクセス、 [https://learn.microsoft.com/en-us/azure/devops/user-guide/what-is-azure-devops?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/user-guide/what-is-azure-devops?view=azure-devops)  
33. Overview of services \- Azure DevOps | Microsoft Learn, 4月 8, 2025にアクセス、 [https://learn.microsoft.com/en-us/azure/devops/user-guide/services?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/user-guide/services?view=azure-devops)  
34. Exploring Azure DevOps: Features and Capabilities for Modern Software Development | by Ravi Sharma | Medium, 4月 8, 2025にアクセス、 [https://medium.com/@ravisharma23523/exploring-azure-devops-features-and-capabilities-for-modern-software-development-42c03ccfede7](https://medium.com/@ravisharma23523/exploring-azure-devops-features-and-capabilities-for-modern-software-development-42c03ccfede7)  
35. 5 Azure DevOps Features That Will Boost Your Team's Productivity, 4月 8, 2025にアクセス、 [https://www.homerun.cloud/post/5-azure-devops-features-that-will-boost-your-team-s-productivity](https://www.homerun.cloud/post/5-azure-devops-features-that-will-boost-your-team-s-productivity)  
36. A Complete Guide to Components and Features of Microsoft Azure DevOps Services, 4月 8, 2025にアクセス、 [https://www.xavor.com/blog/a-beginners-guide-to-components-and-features-of-azure-devops-services/](https://www.xavor.com/blog/a-beginners-guide-to-components-and-features-of-azure-devops-services/)  
37. 8 Important features on Azure DevOps | TO THE NEW Blog, 4月 8, 2025にアクセス、 [https://www.tothenew.com/blog/8-important-features-on-azure-devops/](https://www.tothenew.com/blog/8-important-features-on-azure-devops/)  
38. Azure DevOps Pricing Explained: Tips for Cost Optimization \- Azure FinOps Essentials, 4月 8, 2025にアクセス、 [https://azure-finops-essentials.mindbyte.nl/p/azure-devops-pricing-cost-optimization](https://azure-finops-essentials.mindbyte.nl/p/azure-devops-pricing-cost-optimization)  
39. What does Azure DevOps Services cost?, 4月 8, 2025にアクセス、 [https://veegens.wordpress.com/2022/03/12/what-does-azure-devops-services-cost/](https://veegens.wordpress.com/2022/03/12/what-does-azure-devops-services-cost/)  
40. Newbie asking about Azure DevOps pricing and how to minimise it : r/azuredevops \- Reddit, 4月 8, 2025にアクセス、 [https://www.reddit.com/r/azuredevops/comments/1dgfpr2/newbie\_asking\_about\_azure\_devops\_pricing\_and\_how/](https://www.reddit.com/r/azuredevops/comments/1dgfpr2/newbie_asking_about_azure_devops_pricing_and_how/)  
41. About GitHub Enterprise Cloud with data residency, 4月 8, 2025にアクセス、 [https://docs.github.com/enterprise-cloud@latest/admin/data-residency/about-github-enterprise-cloud-with-data-residency](https://docs.github.com/enterprise-cloud@latest/admin/data-residency/about-github-enterprise-cloud-with-data-residency)  
42. What is Azure DevOps? Features, Benefits, and Use Cases, 4月 8, 2025にアクセス、 [https://www.scholarhat.com/tutorial/devops/what-is-azure-devops](https://www.scholarhat.com/tutorial/devops/what-is-azure-devops)  
43. What is Azure Devops? Components & Benefits | Devtron, 4月 8, 2025にアクセス、 [https://devtron.ai/blog/what-is-azure-devops/](https://devtron.ai/blog/what-is-azure-devops/)  
44. Setting up a GitHub Enterprise Server instance, 4月 8, 2025にアクセス、 [https://docs.github.com/en/enterprise-server@3.12/admin/installing-your-enterprise-server/setting-up-a-github-enterprise-server-instance](https://docs.github.com/en/enterprise-server@3.12/admin/installing-your-enterprise-server/setting-up-a-github-enterprise-server-instance)  
45. Azure DevOps Services, 4月 8, 2025にアクセス、 [https://azure.microsoft.com/en-us/products/devops](https://azure.microsoft.com/en-us/products/devops)  
46. Azure DevOps Services Pricing 2025 \- TrustRadius, 4月 8, 2025にアクセス、 [https://www.trustradius.com/products/azure-devops-services/pricing](https://www.trustradius.com/products/azure-devops-services/pricing)  
47. About billing for GitHub Actions, 4月 8, 2025にアクセス、 [https://docs.github.com/en/billing/managing-billing-for-your-products/managing-billing-for-github-actions/about-billing-for-github-actions](https://docs.github.com/en/billing/managing-billing-for-your-products/managing-billing-for-github-actions/about-billing-for-github-actions)  
48. Connect Azure DevOps Pipeline to AWS Cloud \- YouTube, 4月 8, 2025にアクセス、 [https://www.youtube.com/watch?v=Vywmy5FFzoM](https://www.youtube.com/watch?v=Vywmy5FFzoM)  
49. How Can Azure DevOps Benefit Your Business? | Emergent Software, 4月 8, 2025にアクセス、 [https://www.emergentsoftware.net/blog/how-can-azure-devops-benefit-your-business/](https://www.emergentsoftware.net/blog/how-can-azure-devops-benefit-your-business/)  
50. About billing for GitHub Actions \- GitHub Enterprise Cloud Docs, 4月 8, 2025にアクセス、 [https://docs.github.com/enterprise-cloud@latest/billing/managing-billing-for-github-actions/about-billing-for-github-actions](https://docs.github.com/enterprise-cloud@latest/billing/managing-billing-for-github-actions/about-billing-for-github-actions)  
51. Azure DevOps Services Pricing, 4月 8, 2025にアクセス、 [https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/](https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/)  
52. What is the purpose of Feature in Azure DevOps Agile workflow? \- Stack Overflow, 4月 8, 2025にアクセス、 [https://stackoverflow.com/questions/53896960/what-is-the-purpose-of-feature-in-azure-devops-agile-workflow](https://stackoverflow.com/questions/53896960/what-is-the-purpose-of-feature-in-azure-devops-agile-workflow)  
53. Azure devops billing question : r/azuredevops \- Reddit, 4月 8, 2025にアクセス、 [https://www.reddit.com/r/azuredevops/comments/z87tvp/azure\_devops\_billing\_question/](https://www.reddit.com/r/azuredevops/comments/z87tvp/azure_devops_billing_question/)  
54. Top 5 Reasons to Use GitHub Enterprise \- GitKraken, 4月 8, 2025にアクセス、 [https://www.gitkraken.com/blog/top-5-reasons-to-use-github-enterprise](https://www.gitkraken.com/blog/top-5-reasons-to-use-github-enterprise)  
55. The AI Powered Developer Platform. · GitHub, 4月 8, 2025にアクセス、 [https://github.com/enterprise](https://github.com/enterprise)  
56. GitHub Enterprise \- Pricing \- Microsoft Azure, 4月 8, 2025にアクセス、 [https://azure.microsoft.com/en-us/pricing/details/githubenterprise/](https://azure.microsoft.com/en-us/pricing/details/githubenterprise/)  
57. Enabling GitHub Packages with AWS \- GitHub Enterprise Server 3.13 Docs, 4月 8, 2025にアクセス、 [https://docs.github.com/en/enterprise-server@3.13/admin/configuring-packages/enabling-github-packages-with-aws](https://docs.github.com/en/enterprise-server@3.13/admin/configuring-packages/enabling-github-packages-with-aws)  
58. GitLab Features, 4月 8, 2025にアクセス、 [https://about.gitlab.com/features/](https://about.gitlab.com/features/)  
59. About security overview \- GitHub Enterprise Cloud Docs, 4月 8, 2025にアクセス、 [https://docs.github.com/enterprise-cloud@latest/code-security/security-overview/about-security-overview](https://docs.github.com/enterprise-cloud@latest/code-security/security-overview/about-security-overview)  
60. About enabling security features at scale \- GitHub Enterprise Cloud Docs, 4月 8, 2025にアクセス、 [https://docs.github.com/enterprise-cloud@latest/code-security/securing-your-organization/introduction-to-securing-your-organization-at-scale/about-enabling-security-features-at-scale](https://docs.github.com/enterprise-cloud@latest/code-security/securing-your-organization/introduction-to-securing-your-organization-at-scale/about-enabling-security-features-at-scale)  
61. GitHub · Enterprise Application Security, 4月 8, 2025にアクセス、 [https://github.com/enterprise/advanced-security](https://github.com/enterprise/advanced-security)  
62. GitHub Advanced Security · Built-in protection for every repository, 4月 8, 2025にアクセス、 [https://github.com/security/advanced-security](https://github.com/security/advanced-security)  
63. GitHub security features, 4月 8, 2025にアクセス、 [https://docs.github.com/code-security/getting-started/github-security-features](https://docs.github.com/code-security/getting-started/github-security-features)  
64. Secure your Azure DevOps \- Learn Microsoft, 4月 8, 2025にアクセス、 [https://learn.microsoft.com/en-us/azure/devops/organizations/security/security-overview?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/organizations/security/security-overview?view=azure-devops)  
65. Azure DevOps Security and Compliance Best Practices \- KTL Solutions, 4月 8, 2025にアクセス、 [https://www.ktlsolutions.com/azure-devops-security-and-compliance-best-practices/](https://www.ktlsolutions.com/azure-devops-security-and-compliance-best-practices/)  
66. Data protection overview \- Azure DevOps Services | Microsoft Learn, 4月 8, 2025にアクセス、 [https://learn.microsoft.com/en-us/azure/devops/organizations/security/data-protection?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/organizations/security/data-protection?view=azure-devops)  
67. GitHub Compliance \- All You Need To Know \- Blog \- GitProtect.io, 4月 8, 2025にアクセス、 [https://gitprotect.io/blog/github-compliance-all-you-need-to-know/](https://gitprotect.io/blog/github-compliance-all-you-need-to-know/)  
68. About security, authentication, authorization, and security policies \- Azure DevOps, 4月 8, 2025にアクセス、 [https://learn.microsoft.com/en-us/azure/devops/organizations/security/about-security-identity?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/organizations/security/about-security-identity?view=azure-devops)  
69. About GitHub Enterprise Server, 4月 8, 2025にアクセス、 [https://docs.github.com/en/enterprise-server@3.14/admin/overview/about-github-enterprise-server](https://docs.github.com/en/enterprise-server@3.14/admin/overview/about-github-enterprise-server)  
70. The Pros and Cons of Using GitHub for Repository Management, 4月 8, 2025にアクセス、 [https://www.codeclouds.com/blog/advantages-disadvantages-using-github/](https://www.codeclouds.com/blog/advantages-disadvantages-using-github/)  
71. Azure DevOps Security Best Practices \- Blog \- GitProtect.io, 4月 8, 2025にアクセス、 [https://gitprotect.io/blog/azure-devops-security-best-practices/](https://gitprotect.io/blog/azure-devops-security-best-practices/)  
72. Security best practices \- Azure DevOps | Microsoft Learn, 4月 8, 2025にアクセス、 [https://learn.microsoft.com/en-us/azure/devops/organizations/security/security-best-practices?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/organizations/security/security-best-practices?view=azure-devops)  
73. Azure DevOps Best Practices \- Part 1 \- CloudThat, 4月 8, 2025にアクセス、 [https://www.cloudthat.com/resources/blog/azure-devops-best-practices-part-1](https://www.cloudthat.com/resources/blog/azure-devops-best-practices-part-1)  
74. What are the Differences Between GitLab Premium and GitLab Ultimate? \- ALM-Toolbox, 4月 8, 2025にアクセス、 [https://www.almtoolbox.com/blog/gitlab-premium-vs-ultimate/](https://www.almtoolbox.com/blog/gitlab-premium-vs-ultimate/)  
75. AWS Toolkit for Azure DevOps, 4月 8, 2025にアクセス、 [https://aws.amazon.com/azure-devops/](https://aws.amazon.com/azure-devops/)  
76. Getting started \- AWS Toolkit for Microsoft Azure DevOps, 4月 8, 2025にアクセス、 [https://docs.aws.amazon.com/vsts/latest/userguide/getting-started.html](https://docs.aws.amazon.com/vsts/latest/userguide/getting-started.html)  
77. Seamless Integration with Azure DevOps \- Developing and ..., 4月 8, 2025にアクセス、 [https://docs.aws.amazon.com/whitepapers/latest/develop-deploy-dotnet-apps-on-aws/seamless-integration-with-azure-devops.html](https://docs.aws.amazon.com/whitepapers/latest/develop-deploy-dotnet-apps-on-aws/seamless-integration-with-azure-devops.html)  
78. AWS Connector for GitHub · GitHub Marketplace · GitHub, 4月 8, 2025にアクセス、 [https://github.com/marketplace/aws-connector-for-github](https://github.com/marketplace/aws-connector-for-github)  
79. Set up CI/CD pipelines with Microsoft Azure DevOps \- AWS App2Container, 4月 8, 2025にアクセス、 [https://docs.aws.amazon.com/app2container/latest/UserGuide/a2c-integrations-azure-devops.html](https://docs.aws.amazon.com/app2container/latest/UserGuide/a2c-integrations-azure-devops.html)  
80. Deploy to AWS from GitLab CI/CD, 4月 8, 2025にアクセス、 [https://docs.gitlab.com/ci/cloud\_deployment/](https://docs.gitlab.com/ci/cloud_deployment/)  
81. Installing a GitLab POC on Amazon Web Services (AWS), 4月 8, 2025にアクセス、 [https://docs.gitlab.com/install/aws/](https://docs.gitlab.com/install/aws/)  
82. Integrate with AWS solutions \- GitLab Docs, 4月 8, 2025にアクセス、 [https://docs.gitlab.com/solutions/cloud/aws/gitlab\_aws\_integration/](https://docs.gitlab.com/solutions/cloud/aws/gitlab_aws_integration/)  
83. Provision GitLab on a single EC2 instance in AWS solutions, 4月 8, 2025にアクセス、 [https://docs.gitlab.com/solutions/cloud/aws/gitlab\_single\_box\_on\_aws/](https://docs.gitlab.com/solutions/cloud/aws/gitlab_single_box_on_aws/)  
84. GitLab and AWS, 4月 8, 2025にアクセス、 [https://about.gitlab.com/partners/technology-partners/aws/](https://about.gitlab.com/partners/technology-partners/aws/)  
85. Integrating GitLab with AWS \- Why and How \- YouTube, 4月 8, 2025にアクセス、 [https://www.youtube.com/watch?v=Pr9gl2XYI7s](https://www.youtube.com/watch?v=Pr9gl2XYI7s)  
86. Provision GitLab on a single EC2 instance in AWS, 4月 8, 2025にアクセス、 [https://docs.gitlab.com/ee/solutions/cloud/aws/gitlab\_single\_box\_on\_aws.html](https://docs.gitlab.com/ee/solutions/cloud/aws/gitlab_single_box_on_aws.html)  
87. Compare Azure DevOps Services with Azure DevOps Server \- Learn Microsoft, 4月 8, 2025にアクセス、 [https://learn.microsoft.com/en-us/azure/devops/user-guide/about-azure-devops-services-tfs?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/user-guide/about-azure-devops-services-tfs?view=azure-devops)  
88. Azure DevOps Server Pricing, 4月 8, 2025にアクセス、 [https://azure.microsoft.com/en-us/pricing/details/devops/server/](https://azure.microsoft.com/en-us/pricing/details/devops/server/)  
89. Billing overview \- Azure DevOps | Microsoft Learn, 4月 8, 2025にアクセス、 [https://learn.microsoft.com/en-us/azure/devops/organizations/billing/overview?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/organizations/billing/overview?view=azure-devops)  
90. Installing GitHub Enterprise Server on AWS \- GitHub Docs, 4月 8, 2025にアクセス、 [https://docs.github.com/en/enterprise-server@3.12/admin/installing-your-enterprise-server/setting-up-a-github-enterprise-server-instance/installing-github-enterprise-server-on-aws](https://docs.github.com/en/enterprise-server@3.12/admin/installing-your-enterprise-server/setting-up-a-github-enterprise-server-instance/installing-github-enterprise-server-on-aws)  
91. Installing GitHub Enterprise Server on AWS, 4月 8, 2025にアクセス、 [https://docs.github.com/en/enterprise-server@3.15/admin/installing-your-enterprise-server/setting-up-a-github-enterprise-server-instance/installing-github-enterprise-server-on-aws](https://docs.github.com/en/enterprise-server@3.15/admin/installing-your-enterprise-server/setting-up-a-github-enterprise-server-instance/installing-github-enterprise-server-on-aws)  
92. Managed DevOps Pools pricing \- Learn Microsoft, 4月 8, 2025にアクセス、 [https://learn.microsoft.com/en-us/azure/devops/managed-devops-pools/pricing?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/managed-devops-pools/pricing?view=azure-devops)  
93. GitHub Administration \- GitHub Certifications, 4月 8, 2025にアクセス、 [https://examregistration.github.com/certification/ADMIN](https://examregistration.github.com/certification/ADMIN)
