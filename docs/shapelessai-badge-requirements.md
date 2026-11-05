# Voxel3D 的 ShapelessAI 目录徽章

## 页脚

- 从原提交回执或审核邮件确认 Voxel3D 的目录 slug，并取出官方徽章 HTML。公开接口目前无法确认该记录。
- 在 voxel3d.app 的共享页脚放置 “Featured on ShapelessAI” 徽章。徽章链接指向 Voxel3D 的目录详情页，链接文字或图片替代文本包含 ShapelessAI，且链接不加 `nofollow`。
- 确保首页的服务端 HTML 包含徽章，英文和九种本地化页面使用同一页脚。

## 部署和验收

1. 部署到 voxel3d.app 后，检查首页的原始 HTML 包含正确的徽章链接。
2. 用原提交的 claim token 请求 `POST https://shapelessai.com/api/ai-tools/<slug>/verify`。通过 Authorization 请求头传递凭证。
3. 确认返回 `badge.verified: true`。随后检查公开目录页可以访问，指向 voxel3d.app 的链接没有 `nofollow`，页面没有 `noindex` 指令。

[ShapelessAI 徽章与验证规范](https://shapelessai.com/ai-tools/agents.md)
