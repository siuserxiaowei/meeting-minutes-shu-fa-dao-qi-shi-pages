# 道法术器势会议拆解站（公开发布版）

这是公开 GitHub Pages 发布仓库，只包含已脱敏的静态站点产物。站点把会议纪要整理成“道、法、术、器、势”五维拆解，方便按主题、维度和文章链接检索。

## 在线入口

- GitHub Pages 首页：https://siuserxiaowei.github.io/meeting-minutes-shu-fa-dao-qi-shi-pages/
- GitHub Pages 在线配置页：https://siuserxiaowei.github.io/meeting-minutes-shu-fa-dao-qi-shi-pages/config/
- 全部文章链接清单：https://siuserxiaowei.github.io/meeting-minutes-shu-fa-dao-qi-shi-pages/links/
- 源码仓库：https://github.com/siuserxiaowei/meeting-minutes-shu-fa-dao-qi-shi

## 仓库说明

本仓库是 `meeting-minutes-shu-fa-dao-qi-shi` 的公开发布产物仓库。源仓库负责抓取、解析、拆解、脱敏校验和构建；本仓库负责托管 GitHub Pages。

当前 Pages 配置：

- 发布分支：`main`
- 发布目录：仓库根目录 `/`
- Pages 地址：https://siuserxiaowei.github.io/meeting-minutes-shu-fa-dao-qi-shi-pages/
- 发布状态可通过 GitHub 仓库的 Settings -> Pages 查看。

## 内容结构

- `index.html`：站点首页，包含文章检索、标签筛选、维度入口和最近文章。
- `articles/`：逐篇会议拆解页面。
- `dimensions/dao/`：按“道”聚合的战略和价值判断。
- `dimensions/fa/`：按“法”聚合的方法论和原则。
- `dimensions/shu/`：按“术”聚合的执行步骤和打法。
- `dimensions/qi/`：按“器”聚合的工具、系统和资源配置。
- `dimensions/shi/`：按“势”聚合的趋势、时机和外部环境。
- `links/`：全量在线链接清单。
- `config/`：GitHub Pages 在线配置页。
- `data/`：公开 JSON 数据端点，供页面和外部脚本读取。

## 公开边界

本仓库不包含原始逐字稿、`docx`、完整会议原文、飞书原始正文、临时鉴权链接或本机源文件路径。

公开站只展示：

- 会议摘要
- 标签和学习重点
- 章节标题和短句级证据
- 行动项
- 来源文件名索引
- “道、法、术、器、势”五维拆解
- 在线链接清单

## 更新方式

不要直接手写修改大量静态页面。常规更新应在私有源码仓库中完成：

```bash
cd ../meeting-minutes-shu-fa-dao-qi-shi
npm run all
rsync -a docs/ ../meeting-minutes-shu-fa-dao-qi-shi-pages/
```

然后在本仓库提交并推送：

```bash
git add -A
git commit -m "Publish meeting breakdown site"
git push origin main
```

发布后检查以下页面是否返回 `200`：

- https://siuserxiaowei.github.io/meeting-minutes-shu-fa-dao-qi-shi-pages/
- https://siuserxiaowei.github.io/meeting-minutes-shu-fa-dao-qi-shi-pages/config/
- https://siuserxiaowei.github.io/meeting-minutes-shu-fa-dao-qi-shi-pages/links/

## 独立拆分仓库

2026-05-10 的 3 篇飞书 AI 产品纪要已经拆到独立仓库，不再放在本大站顶部入口：

```text
https://github.com/siuserxiaowei/ai-product-feishu-breakdowns-20260510
https://siuserxiaowei.github.io/ai-product-feishu-breakdowns-20260510/config/
```
