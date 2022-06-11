## AWSのSSOのSAML2で実現するAWSのシングルサインオン

AWSのSSOでSAML2のIdPを構築できます｡このSAMLのIdPを利用して､AWSのコンソールログインのシングルサインオンを実装できたので､その時のメモです｡

まずはSAMLで出てくる用語の整理です｡

|用語|説明|
| --- | --- |
|IdP |Identity Providerの略で､認証情報を保持管理するサービスです｡|
|SP |Service Provideの略で､IdPで認証を受けるサービスのことです｡|
|メタデータ |IdPからSPに連携される情報で､IdPの設定情報やIdPとのやり取りを行う証明書が含まれます｡|
|アトリビュート|認証されたときに､IdPからSPに渡される情報｡この情報をもとにSP側で利用するアプリの判定を行う|

WAS SSOを利用するためには､AWS Organazationが必要となります｡

AWS SSO saml機能を用いて､追加するためには下記の手順となります｡

1. AWS Organazationを有効化する
3. AWS SSOでsamlのIdPを作成する
4. saml認証するユーザを作成する
5. AWS SSOでアプリケーションを作成する
6. SSO アプリケーションで作成したメタデータを取得する
7. メタデータをもとにAWS IAMでIdentity Providerを作成する
8. Identify Providerに紐づくロールを作成する
9. AIMで作成したIdentify Provider情報､ロール情報を登録する


