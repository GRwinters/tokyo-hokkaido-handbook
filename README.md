# 東京 → 北海道 · 旅行手册（2026.12.14—12.20）

一个单文件的旅行手册网页：手绘 SVG 头图、实时倒计时与双时区时钟、可交互路线地图、七天时间轴、交通票据 / 住宿 / 待办 / 贴士。

- 纯静态：`index.html` 一个文件，全部样式、脚本、插画内联，无 CDN、无外部字体、无图片请求，断网可打开。
- 浅色 / 深色两套配色，切换后记忆在本机 localStorage。
- 适配 376px 起的手机与桌面，纵向单列滚动。
- 打卡进度同样存在 localStorage。

## 在线地址

| 平台 | 地址 | 说明 |
|---|---|---|
| Cloudflare Pages | https://tokyo-hokkaido-handbook-bcn.pages.dev | 已接本仓库，推送到 `main` 自动重建 |
| GitHub Pages | https://grwinters.github.io/tokyo-hokkaido-handbook/ | 备用地址，同样自动重建 |

> Cloudflare 项目名 `tokyo-hokkaido-handbook` 对应的 `*.pages.dev` 子域已被占用，Cloudflare 自动分配了 `-bcn` 后缀。若想换成更短的地址，需要在 Cloudflare 里新建项目（项目名决定子域，创建后不可改）。

## 目录

```
index.html    # 全部内容
README.md     # 本文件
```

## 更新内容

直接编辑 `index.html` 后推送到 `main` 分支，两个平台都会自动重新部署：

- 行程数据在 `<script>` 里的 `DAYS` 数组（每天一个对象，含 items / stay）
- 景点介绍在 `PLACES`（一句话推荐、必看点、体验建议）
- 票据、住宿、待办、贴士分别是 `TICKETS` / `STAYS` / `TODOS` / `TIPS`

## 说明

本页为规划稿：航班号、车次时刻、酒店房态与订单号均未确认，标注「待补充 / 待确认」的内容需在预订后回填。耗时与气温为参考值。
