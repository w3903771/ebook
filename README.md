# ebook —— 电子书门户

`ebook.ttzg.site` 的源码：一个纯静态单页（`index.html`），列出所有学科，每个学科链到各自的子域名站点。

## 结构

- `index.html` —— 门户单页（学科卡片网格）
- `CNAME` —— 自定义域名 `ebook.ttzg.site`

## 部署（GitHub Pages，从分支部署，无需构建）

1. 推送到 GitHub 仓库 `w3903771/ebook` 的 `main` 分支。
2. 仓库 **Settings → Pages → Build and deployment → Source** 选 **Deploy from a branch**，分支 `main`、目录 `/ (root)`。
3. **Custom domain** 填 `ebook.ttzg.site`（`CNAME` 文件已带），勾 **Enforce HTTPS**。
4. DNS 在 `ttzg.site` 加：`ebook` CNAME → `w3903771.github.io`。

## 新增一个学科

复制 `index.html` 里的 `<a class="card">` 区块，改学科名、简介与链接（指向 `<学科>.ebook.ttzg.site`）即可。各学科站的搭建见 `quant` 仓库的 `DEPLOY.md`。
