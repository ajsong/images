## 前言

- 什么是 Forestry？
  1. 免费提供静态博客管理功能，使你的博客拥有 CMS 般的体验。
  2. 你可以很轻松地编写、修改和发布博客，包括图片与文件，而不需要手动去编译上传，`Forestry` 已经为你自动处理了。
  3. 如果你需要多用户功能，则需要开通收费版。
- 为什么使用 GitHub 作为图床？
  1. 免费且无限量的 CDN

## 准备

我们约定存储方式为：使用上传当天日期作为文件夹，例如：

```
|- 20191004
    |- logo.png
    |- ...
|- 20191102
    |- logo.png
    |- ...
```

- 新建一个 GitHub 仓库，例如：`pic`
- 注册一个账号：[Forestry](https://forestry.io/)

## 配置 Forestry

新建站点

[![使用 Forestry 管理基于 GitHub 的图床-字节智造](https://oss.tqlcool.com/resources/tqlFile/webp/J7lX4PIDnKaVRgBq.webp)](https://oss.tqlcool.com/resources/tqlFile/webp/J7lX4PIDnKaVRgBq.webp)

[![使用 Forestry 管理基于 GitHub 的图床-字节智造](https://oss.tqlcool.com/resources/tqlFile/webp/ramlq8wOtgzhWkyD.webp)](https://oss.tqlcool.com/resources/tqlFile/webp/ramlq8wOtgzhWkyD.webp)

[![使用 Forestry 管理基于 GitHub 的图床-字节智造](https://oss.tqlcool.com/resources/tqlFile/webp/d01AZEIwgn6qkXxj.webp)](https://oss.tqlcool.com/resources/tqlFile/webp/d01AZEIwgn6qkXxj.webp)

- 修改时区
  `Settings` >> `General` >> `TIMEZONE`，选择 `(GMT+08:00) Beijing`，保存 `Save settings`
- 修改上传规则
  - `Settings` >> `Media` >> `UPLOAD DIRECTORY` 改为空
  - `Settings` >> `Media` >> `PUBLIC PATH` 改为空
  - `Settings` >> `Media` >> `FILE PATH` 改为 `:year::month::day:/:filename:`

## 最终结果

[![使用 Forestry 管理基于 GitHub 的图床-字节智造](https://oss.tqlcool.com/resources/tqlFile/webp/FToEnmkesNB5tH2i.webp)](https://oss.tqlcool.com/resources/tqlFile/webp/FToEnmkesNB5tH2i.webp)

CDN 规则：https://cdn.jsdelivr.net/gh/cnguu/pic@master/20191004/logo.png

- cnguu：GitHub 账号
- pic：仓库名
- master：仓库分支
