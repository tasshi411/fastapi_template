# fastapi_template
個人開発用のFastAPIのテンプレート

# 概要
```markdown
.
├── api
│   ├── dips.py
│   └── endpoints
├── cores
├── main.py
├── models
├── repositories
├── schemas
└── services
```
- api
    - routerやrouterで使う依存性注入をまとめたdips.pyを定義
- api/endpoints
    - 各routerをまとめる
    - 各routerは基本的にはdipsで注入する依存性注入用関数やserviceを呼び出す
- api/dips.py
    - 依存性注入用の関数をまとめたスクリプト
    - 認証など
- cores
    - utils的な便利関数をまとめたファイルを置く（auth.pyなど）
- models
    - ORMの各モデルを置く
- repositories
    - modelsを操作するcrud用のスクリプトを置く
- schemas
    - routerの各リクエストやレスポンスの形式を定義したschemaスクリプトを置く
- services
    - 実際にAPIがやる処理をラップした関数群を置く
    - 基本的にapiから呼ばれる