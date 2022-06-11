## AWSのSSOのSAML2で実現するAWSのシングルサインオン

AWSのSSOでSAML2のIdPを構築できます｡このSAMLのIdPを利用して､AWSのコンソールログインのシングルサインオンを実装できたので､その時のメモです｡

まずはSAMLで出てくる用語の整理です｡

IdP Identity Providerの略で､認証情報を保持管理するサービスです｡
SP Service Provideの略で､IdPで認証を受けるサービスのことです｡
メタデータ IdPからSPに連携される情報で､IdPの設定情報やIdPとのやり取りを行う証明書が含まれます｡

