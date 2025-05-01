# AWSポリシー変更関連アクション一覧 (Markdown版) - 更新版

**注意:** このリストは主要なアクションを網羅するよう努めていますが、AWSサービスの進化により、新しいアクションが追加されたり、変更されたりする可能性があります。完全性を保証するものではないため、定期的な見直しや公式ドキュメントの確認をお勧めします。ここでいう「ポリシー」には、リソースポリシー、信頼ポリシー、インラインポリシー、アクセスポリシー、SCPなど、広義のアクセス制御設定を含みます。

## IAM (Identity and Access Management)

* `iam:PutGroupPolicy`: グループにインラインポリシーを作成または更新します。
* `iam:PutRolePolicy`: ロールにインラインポリシーを作成または更新します。
* `iam:PutUserPolicy`: ユーザーにインラインポリシーを作成または更新します。
* `iam:DeleteGroupPolicy`: グループからインラインポリシーを削除します。
* `iam:DeleteRolePolicy`: ロールからインラインポリシーを削除します。
* `iam:DeleteUserPolicy`: ユーザーからインラインポリシーを削除します。
* `iam:UpdateAssumeRolePolicy`: ロールの信頼ポリシー（誰がロールを引き受けられるかを定義）を更新します。

## S3 (Simple Storage Service)

* `s3:PutBucketPolicy`: S3バケットにバケットポリシーを適用または置換します。
* `s3:DeleteBucketPolicy`: S3バケットからバケットポリシーを削除します。
* `s3:PutAccessPointPolicy`: S3アクセスポイントにアクセスポリシーを適用または置換します。
* `s3:DeleteAccessPointPolicy`: S3アクセスポイントからアクセスポリシーを削除します。
* `s3:PutMultiRegionAccessPointPolicy`: S3マルチリージョンアクセスポイントにポリシーを適用または置換します。
* `s3:DeleteMultiRegionAccessPointPolicy`: S3マルチリージョンアクセスポイントからポリシーを削除します。
* `s3-outposts:PutEndpointPolicy`: S3 on Outpostsのエンドポイントにポリシーを設定または置換します。
* `s3-outposts:DeleteEndpointPolicy`: S3 on Outpostsのエンドポイントからポリシーを削除します。

## Secrets Manager

* `secretsmanager:PutResourcePolicy`: シークレットにリソースベースのポリシーをアタッチまたは置換します。
* `secretsmanager:DeleteResourcePolicy`: シークレットからリソースベースのポリシーを削除します。
* `secretsmanager:ValidateResourcePolicy`: リソースポリシーが有効かどうかを検証します（変更アクションではありませんが関連性が高いです）。

## KMS (Key Management Service)

* `kms:PutKeyPolicy`: KMSキーにキーポリシーをアタッチまたは置換します（デフォルトポリシーの変更には制限があります）。

## Lambda

* `lambda:AddPermission`: Lambda関数またはレイヤーバージョンにリソースベースのポリシー（アクセス許可）を追加します。
* `lambda:RemovePermission`: Lambda関数またはレイヤーバージョンからリソースベースのポリシー（アクセス許可）を削除します。
* `lambda:AddLayerVersionPermission`: Lambdaレイヤーバージョンにリソースベースのポリシー（アクセス許可）を追加します。
* `lambda:RemoveLayerVersionPermission`: Lambdaレイヤーバージョンからリソースベースのポリシー（アクセス許可）を削除します。

## SQS (Simple Queue Service)

* `sqs:SetQueueAttributes`: キューの属性を変更します。属性名 `Policy` を指定することでキューポリシーを変更できます。
* `sqs:AddPermission`: キューにアクセス許可を追加します（キューポリシーを変更）。
* `sqs:RemovePermission`: キューからアクセス許可を削除します（キューポリシーを変更）。

## SNS (Simple Notification Service)

* `sns:SetTopicAttributes`: トピックの属性を変更します。属性名 `Policy` を指定することでトピックポリシーを変更できます。
* `sns:AddPermission`: トピックにアクセス許可を追加します（トピックポリシーを変更）。
* `sns:RemovePermission`: トピックからアクセス許可を削除します（トピックポリシーを変更）。

## ECR (Elastic Container Registry)

* `ecr:SetRepositoryPolicy`: ECRリポジトリにリポジトリポリシーを設定または置換します。
* `ecr:DeleteRepositoryPolicy`: ECRリポジトリからリポジトリポリシーを削除します。

## API Gateway (v1 - REST APIs)

* `apigateway:UpdateRestApi`: REST APIの設定を更新します。このアクションの一部としてリソースポリシー (`policy` フィールド) を更新できます。（注: このアクションはポリシー以外の設定も変更するため、拒否する際は影響範囲に注意が必要です。）

## API Gateway V2 (HTTP/WebSocket APIs)

* `apigateway:PutApiPolicy`: HTTP API または WebSocket API にリソースポリシーを設定または置換します。
* `apigateway:DeleteApiPolicy`: HTTP API または WebSocket API からリソースポリシーを削除します。

## CloudWatch Logs

* `logs:PutResourcePolicy`: CloudWatch Logs のリソース（例: ロググループなど）にリソースポリシーを設定または置換します。
* `logs:DeleteResourcePolicy`: CloudWatch Logs のリソースからリソースポリシーを削除します。

## OpenSearch Service (formerly Elasticsearch Service)

* `es:UpdateDomainConfig` (または `es:UpdateElasticsearchDomainConfig`): OpenSearch/Elasticsearch ドメインの設定を更新します。アクセスポリシー (`AccessPolicies` フィールド) の変更が含まれる場合があります。
* `es:CreateDomain` (または `es:CreateElasticsearchDomain`): ドメイン作成時にアクセスポリシーを指定する場合があります。

## EventBridge (CloudWatch Events)

* `events:PutPermission`: 他のアカウントなどがイベントバスにイベントを送信することを許可します（イベントバスのポリシーに影響）。
* `events:RemovePermission`: イベントバスへのアクセス許可を削除します。
* `events:PutResourcePolicy`: イベントバスにリソースポリシーを直接設定または置換します。
* `events:DeleteResourcePolicy`: イベントバスのリソースポリシーを削除します。
* `schemas:PutResourcePolicy`: EventBridge スキーマレジストリにリソースポリシーを設定または置換します。
* `schemas:DeleteResourcePolicy`: EventBridge スキーマレジストリのリソースポリシーを削除します。

## Glacier (S3 Glacier)

* `glacier:SetVaultAccessPolicy`: Glacier ボールトにアクセスポリシーを設定または置換します。
* `glacier:DeleteVaultAccessPolicy`: Glacier ボールトからアクセスポリシーを削除します。

## CodeArtifact

* `codeartifact:PutDomainPermissionsPolicy`: CodeArtifact ドメインに権限ポリシーを設定または置換します。
* `codeartifact:PutRepositoryPermissionsPolicy`: CodeArtifact リポジトリに権限ポリシーを設定または置換します。
* `codeartifact:DeleteDomainPermissionsPolicy`: CodeArtifact ドメインから権限ポリシーを削除します。
* `codeartifact:DeleteRepositoryPermissionsPolicy`: CodeArtifact リポジトリから権限ポリシーを削除します。

## IoT (Internet of Things)

* `iot:CreatePolicy`: IoTポリシーを作成します。
* `iot:CreatePolicyVersion`: IoTポリシーの新しいバージョンを作成します（実質的な変更）。
* `iot:SetPolicyAsActiveVersion`: IoTポリシーの有効なバージョンを設定します。
* `iot:DeletePolicy`: IoTポリシーを削除します。
* `iot:DeletePolicyVersion`: IoTポリシーの特定のバージョンを削除します。
* `iot:SetDefaultAuthorizer`: デフォルトのカスタムオーソライザーを設定します（アクセス制御ポリシーに関連）。

## EFS (Elastic File System)

* `elasticfilesystem:PutFileSystemPolicy`: EFS ファイルシステムにファイルシステムポリシーを設定または置換します。
* `elasticfilesystem:DeleteFileSystemPolicy`: EFS ファイルシステムからファイルシステムポリシーを削除します。

## Backup

* `backup:PutBackupVaultAccessPolicy`: Backup ボールトにアクセスポリシーを設定または置換します。
* `backup:DeleteBackupVaultAccessPolicy`: Backup ボールトからアクセスポリシーを削除します。

## Glue

* `glue:PutResourcePolicy`: Glue データカタログにリソースポリシーを設定または置換します。
* `glue:DeleteResourcePolicy`: Glue データカタログからリソースポリシーを削除します。

## MediaStore

* `mediastore:PutContainerPolicy`: MediaStore コンテナにコンテナポリシーを設定または置換します。
* `mediastore:DeleteContainerPolicy`: MediaStore コンテナからコンテナポリシーを削除します。

## RAM (Resource Access Manager)

* *(厳密にはポリシー変更ではありませんが、クロスアカウント等のアクセス許可変更に深く関わるため記載)*
* `ram:CreateResourceShare`, `ram:UpdateResourceShare`, `ram:DeleteResourceShare`
* `ram:AssociateResourceShare`, `ram:DisassociateResourceShare`
* `ram:AcceptResourceShareInvitation`, `ram:RejectResourceShareInvitation`

## Lake Formation

* *(データアクセス権限の変更に関連)*
* `lakeformation:GrantPermissions`, `lakeformation:RevokePermissions`
* `lakeformation:BatchGrantPermissions`, `lakeformation:BatchRevokePermissions`
* `lakeformation:PutDataLakeSettings` (権限モデルの変更を含む)

## CodeBuild

* `codebuild:PutResourcePolicy`: CodeBuild プロジェクトにリソースポリシーを設定または置換します。
* `codebuild:DeleteResourcePolicy`: CodeBuild プロジェクトのリソースポリシーを削除します。

## CloudFormation

* `cloudformation:SetStackPolicy`: スタックポリシーを設定または更新します（リソースの更新/削除からの保護に関連）。

## ACM PCA (AWS Certificate Manager Private Certificate Authority)

* `acm-pca:PutPolicy`: プライベートCAにポリシー（アクセス許可）をアタッチします。
* `acm-pca:DeletePolicy`: プライベートCAからポリシーを削除します。

## VPC Lattice

* `vpc-lattice:PutAuthPolicy`: サービスネットワークまたはサービスに認証ポリシーを設定します。
* `vpc-lattice:DeleteAuthPolicy`: 認証ポリシーを削除します。

## Entity Resolution (NEW)

* `entityresolution:PutPolicy`: SchemaMapping または MatchingWorkflow にポリシーを設定または更新します。
* `entityresolution:DeletePolicy`: SchemaMapping または MatchingWorkflow からポリシーを削除します。

## Migration Hub Refactor Spaces (NEW)

* `refactorspaces:PutResourcePolicy`: 環境またはサービスにリソースポリシーを設定または更新します。
* `refactorspaces:DeleteResourcePolicy`: 環境またはサービスからリソースポリシーを削除します。

## Organizations (NEW - SCPs etc.)

* `organizations:CreatePolicy`: 組織ポリシー（SCPなど）を作成します。
* `organizations:UpdatePolicy`: 組織ポリシーを更新します。
* `organizations:DeletePolicy`: 組織ポリシーを削除します。
* `organizations:AttachPolicy`: 組織ポリシーをOUやアカウントにアタッチします。
* `organizations:DetachPolicy`: 組織ポリシーをOUやアカウントからデタッチします。

## Serverless Application Repository (SAR) (NEW)

* `serverlessrepo:PutApplicationPolicy`: SAR アプリケーションにポリシーを設定または更新します。
* `serverlessrepo:DeleteApplicationPolicy`: SAR アプリケーションからポリシーを削除します。

## Signer (NEW)

* `signer:PutSigningProfilePolicy`: 署名プロファイルにポリシーを設定または更新します。
* `signer:DeleteSigningProfilePolicy`: 署名プロファイルからポリシーを削除します。

## Systems Manager Incident Manager (NEW)

* `ssm-incidents:PutResourcePolicy`: レスポンスプランにリソースポリシーを設定または更新します。
* `ssm-incidents:DeleteResourcePolicy`: レスポンスプランからリソースポリシーを削除します。

## Kinesis Data Streams (NEW)

* `kinesis:PutResourcePolicy`: Kinesis データストリームにポリシーを設定または更新します。
* `kinesis:DeleteResourcePolicy`: Kinesis データストリームからポリシーを削除します。

## Redshift Serverless (NEW)

* `redshift-serverless:PutResourcePolicy`: Redshift Serverless 名前空間にポリシーを設定または更新します。
* `redshift-serverless:DeleteResourcePolicy`: Redshift Serverless 名前空間からポリシーを削除します。

## SES V2 (Simple Email Service) (NEW)

* `ses:PutEmailIdentityPolicy`: Eメールアイデンティティにポリシーを設定または更新します。
* `ses:DeleteEmailIdentityPolicy`: Eメールアイデンティティからポリシーを削除します。
* `ses:PutDomainIdentityPolicy`: ドメインアイデンティティにポリシーを設定または更新します。
* `ses:DeleteDomainIdentityPolicy`: ドメインアイデンティティからポリシーを削除します。

## Lex V2 (NEW - Covered in original list, added header for clarity)

* `lex:CreateResourcePolicy`: ボットまたはボットエイリアスにリソースポリシーを作成します。
* `lex:UpdateResourcePolicy`: ボットまたはボットエイリアスのリソースポリシーを更新します。
* `lex:DeleteResourcePolicy`: ボットまたはボットエイリアスのリソースポリシーを削除します。
