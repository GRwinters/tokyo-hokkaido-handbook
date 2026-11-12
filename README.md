# 東京 → 北海道 · 旅行手册（2026.12.14—12.20）

一个单文件的旅行手册网页：手绘 SVG 头图、实时倒计时与双时区时钟、可交互路线地图、七天时间轴、交通票据 / 住宿 / 待办 / 贴士。

- 纯静态：`index.html` 一个文件，全部样式、脚本、插画内联，无 CDN、无外部字体、无图片请求，断网可打开。
- 浅色 / 深色两套配色，切换后记忆在本机 localStorage。
- 适配 376px 起的手机与桌面，纵向单列滚动。
- 打卡进度同样存在 localStorage。

## 目录

```
index.html    # 全部内容
.nojekyll     # 让 GitHub Pages 直接按静态文件发布（不做 Jekyll 处理）
```

## 部署

### Cloudflare Pages（推荐，免费、公开可读）

方式一 · 连接本仓库（推送到 GitHub 后自动构建）

1. Cloudflare 控制台 → Workers & Pages → Create → Pages → Connect to Git
2. 选择本仓库 → 框架预设 `None`，构建命令留空，输出目录 `/`
3. 保存并部署，得到 `https://<项目名>.pages.dev`

方式二 · 本地直传（不依赖 Git）

```bash
npx wrangler pages deploy . --project-name=tokyo-hokkaido
```

### GitHub Pages（可选）

仓库 Settings → Pages → Source 选 `Deploy from a branch` → 分支 `main`、目录 `/`。
地址为 `https://<用户名>.github.io/<仓库名>/`。

## 更新内容

直接编辑 `index.html`：

- 行程数据在 `<script>` 里的 `DAYS` 数组（每天一个对象，含 items / stay）
- 景点介绍在 `PLACES`（一句话推荐、必看点、体验建议）
- 票据、住宿、待办、贴士分别是 `TICKETS` / `STAYS` / `TODOS` / `TIPS`

改完提交推送，Cloudflare Pages 会自动重新部署。

## 说明

本页为规划稿：航班号、车次时刻、酒店房态与订单号均未确认，标注「待补充 / 待确认」的内容需在预订后回填。耗时与气温为参考值。
