## これってなに？

hugoを使用して作成した自分用のwebsiteです。

## 導入方法

#### 必要要件

- [HUGO](https://gohugo.io/)

#### インストール

まず適当なディレクトリに移動して `git clone https://github.com/nullnyat/nullnyat-nca10moe` します。

そしたら `cd nullnyat-nca10moe` します。

次にそのディレクトリに `config.toml` を作成します。中身は以下のようにします。

```toml
baseURL = 'https://example.com'
title = 'タイトル'
author = '名前'
HasCJKLanguage = true
DefaultContentLanguage = 'ja'
languageCode = 'ja-jp'
enableRobotsTXT = true
pluralizeListTitles = false
markup.highlight.noClasses = false

[Params]
dateformat = '2006/01/02'
description = '説明'

[taxonomies]
tag = 'tags'
category = 'categories'
archive = 'archives'

[markup.goldmark.renderer]
unsafe = true

[outputs]
 home = ['html', 'rss']
 section = ['html', 'rss']
 taxonomy = ['html']
 term = ['html']

disableKinds = ['rss']

[services]
 [services.rss]
 limit = 42
 copyright = '© 20xx name'

[params]
 [params.author]
  email = 'example@example.com'
  name = '名前'
```

exampleとかを変更してください。

そしたら `content` と `static` を作成してください。

`content` はblogの記事などを入れておくやつです。

`static` は画像とかいろいろなものを入れておくやつです。

`hugo server --watch`すれば起動できます。
