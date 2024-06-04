# -

欲しいものリストのアプリケーションを作ります。

# GithubPages関連URL

[API定義]
(https://shiryu-go.github.io/-/redocly-openAPI)

# mockサーバーの建て方

1. dockerイメージ取得

```bash
docker pull danielgtaylor/apisprout
```

2.

```
docker run -p 8000:8000 -v {$フルパス}/openapi.yml danielgtaylor/apisprout /openapi.yml
```

TODO 多分ワンライナーで書ける

以上でモックサーバーが建てられる。

# lint/formatter
package.json参照
