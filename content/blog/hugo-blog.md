+++
date = "2016-03-13T03:29:53+09:00"
draft = false
title = "Hugoでブログ生成"

+++

[Hugo](https://gohugo.io/)とテーマ[cocoa](https://github.com/nishanths/cocoa-hugo-theme)を用いてブログ生成を行う。

## Hugoのインストール

Hugoは`go get`でインストール可能。かなり簡単。

{{< highlight bash >}}
$ go get -u -v github.com/spf13/hugo
$ hugo version
Hugo Static Site Generator v0.16-DEV BuildDate: 2016-01-04T02:08:16+09:00
{{</highlight>}}

## Blogの生成

{{< highlight bash >}}
$ pwd
/Users/junk/blog/hugo
$ hugo new site mysite
Congratulations! Your new Hugo site is created in "/Users/junk/blog/hugo/mysite".
$ ls mysite
archetypes  config.toml content     data        layouts     static      themes
{{</highlight>}}

## テーマのインストール

Hugoのテーマは http://themes.gohugo.io/ 上にまとまっており、この中で気に入ったものを選択する。

テーマのセットアップは、作成したプロジェクト内のthemesディレクトリ内にthemeディレクトリを配置することで利用する。

今回、[cocoa](https://github.com/nishanths/cocoa-hugo-theme)を利用した。

{{< highlight bash >}}
$ git clone https://github.com/nishanths/cocoa-hugo-theme.git themes/cocoa
{{</highlight>}}

## 設定ファイル

今回はcocoaを利用しているため、cocoaの[設定ファイル例](https://github.com/nishanths/cocoa-hugo-theme/blob/master/exampleSite/config.toml)をベースにすすめる。

ブログのタイトル・説明、SNS系・GAのリンクなどは設定ファイル上で編集する。
以下、設定例。

{{< highlight bash >}}
baseurl = "https://you.github.io/" # TODO
builddrafts = false
canonifyurls = true
contentdir = "content"
languageCode = "en-US"
layoutdir = "layouts"
publishdir = "public"
author = "Arthur Dent"
title = "Arthur Dent"
pygmentsuseclasses = true
disqusShortname = "cocoaexamplesite" # TODO: optional, comment out to disable Disqus
pluralizelisttitles = false

[permalinks]
fixed = ":title/"
blog = "blog/:slug/"

[params]
Author = "Arthur Dent"
CacheBuster = true
DateForm = "Jan 2, 2006"
DateFormFull = "Mon Jan 2 2006 15:04:05 MST"
Description = "Don't panic"
Email = "you@example.space" # TODO:
FaviconFile = "img/leaf.ico"
GATracker = "XYZ" # TODO:
GitHub = "//github.com/you" # TODO:
Initials = "ad" # displayed on single post page; DEPRECATED in v0.3.0
Lang = "en"
LinkedIn = "//linkedin.com/in/you" # TODO:
Twitter = "//twitter.com/you" # TODO:
ExtraCssFiles = [ "/css/override.css" ] # relative to public directory

{{</highlight>}}

## 記事の作成

{{< highlight bash >}}
$ hugo new blog/example.md
/Users/junk/blog/hugo/mysite/content/blog/example.md created

# 編集
$ vim blog/example.md
+++
date = "2016-03-13T12:56:34+09:00"
draft = true
title = "example"

+++

こんにちは
{{</highlight>}}

## プレビュー

プレビューは`hugo server`コマンドで行う。
記事の作成と編集をしただけだとdraft状態となっているため、`hugo undraft content/blog/example.md` を行う必要がある。
しかし、`--buildDrafts`オプションを付与すると、draft状態の記事も表示可能となる。

{{< highlight bash >}}
$ hugo server --buildDrafts
{{</highlight>}}

## 公開

`public/`以下だけを公開対象にすればOK。
