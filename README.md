# Trussic

Trussic 官网落地页，单文件静态站点：**https://www.trussic.com**

## 结构

```
site/index.html   # 唯一页面：结构、样式、文案、交互全部在里面
```

零依赖，不引外部字体，单 HTML 文件部署。

## 本地预览

```
npx serve site
```

直接双击 `site/index.html` 也能看，但 `file://` 下剪贴板权限会被浏览器限制，「复制链接」只能走兜底方案。

## 改哪里

- **文案**：`<script>` 里的 `COPY` 对象（`en` / `zh` 两组），键名与 HTML 上的 `data-copy` 一一对应
- **配色与字号**：`<style>` 顶部的 `:root` 变量与响应式断点
- **分享链接**：常量 `SITE = 'https://trussic.com'`

## 部署

线上跑在 Cloudflare Workers（静态资源）。更新时把 `site/index.html` 重新上传部署即可，域名和证书不用动。

---

© Trussic
