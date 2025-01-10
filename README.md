# OCI Document Understanding サンプルコード

## 概要
このプロジェクトは、Oracle Cloud Infrastructure (OCI) の Document Understanding サービスを使用して、画像からテキストを抽出する同期OCRのサンプルコードです。

## 前提条件
- Python 3.x
- OCIアカウントとアクセス権限
    - Document Understanding サービスのアクセス権限が必要です。
    -  [ドキュメント理解ポリシーについて](https://docs.oracle.com/ja-jp/iaas/Content/document-understanding/using/about_document-understanding_policies.htm#about_vision_policies)を参考に権限を設定してください。
- 適切に設定されたOCI構成ファイル（~/.oci/config）

## インストール
必要なパッケージをインストールします：

```bash
pip install -r requirements.txt
```

## 環境設定
1. `.env_example`を参考に`.env`ファイルを作成
2. `.env`ファイルに以下の環境変数を設定：
   - `OCI_COMPARTMENT_ID`: OCIのコンパートメントID

## プロジェクト構成
```
.
├── .env                    # 環境変数設定ファイル
├── requirements.txt        # 依存パッケージリスト
├── images/                 # 解析対象の画像ファイル
├── output/                 # OCR結果の出力先
└── synchronously_analyze_document.ipynb  # メインのJupyterノートブック
```

## 機能
- 画像ファイルからのテキスト抽出
- 抽出されたテキストの信頼度スコア表示
- テキストの位置情報（境界ポリゴン）の取得
- 結果のJSON形式での保存

## 使用方法
1. Jupyterノートブックを開く
2. 必要なパッケージのインストールと環境変数の設定を確認
3. 解析したい画像ファイルのパスを設定
4. ノートブックのセルを順番に実行

## 注意事項
- このサンプルコードは学習目的で作成されており、エラー処理は最小限です
- 本番環境での使用には適切なエラー処理の実装が必要です
- OCIの課金が発生する可能性があるため、使用量に注意してください

## 参考ドキュメント
- [OCI Document Understanding 英語ドキュメント](https://docs.oracle.com/en-us/iaas/Content/document-understanding/using/home.htm)
- [OCI Document Understanding 日本語ドキュメント](https://docs.oracle.com/ja-jp/iaas/Content/document-understanding/using/home.htm)
- 【コンソールからの Document Understandingの利用方法】
    - [日本語ドキュメント](https://docs.oracle.com/ja-jp/iaas/Content/document-understanding/using/pretrained-doc-using.htm#custom_model_using_console)
    - [英語ドキュメント](https://docs.oracle.com/en-us/iaas/Content/document-understanding/using/pretrained-doc-using.htm#custom_model_using_console)
- 【APIからの Document Understandingの利用方法】
    - [日本語ドキュメント](https://docs.oracle.com/ja-jp/iaas/Content/document-understanding/using/api_models.htm#api_models)
    - [英語ドキュメント](https://docs.oracle.com/en-us/iaas/Content/document-understanding/using/api_models.htm#api_models)
    - [OCI Document Understanding API リファレンス](https://docs.oracle.com/en-us/iaas/api/#/en/document-understanding/20221109/)
    - [Python SDK ドキュメント](https://docs.oracle.com/en-us/iaas/tools/python/latest/api/ai_document/client/oci.ai_document.AIServiceDocumentClient.html)

## ライセンス
このプロジェクトは MIT-0 ライセンスの下で公開されています。