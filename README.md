# OurAILab 课题组主页

深圳职业技术大学人工智能学院 · 模式分析与机器智能课题组（OurAILab）官网源码。

- 线上地址：<https://ourailab.github.io>
- 技术栈：Jekyll + [Academic Pages](https://academicpages.github.io/) 主题，由 GitHub Pages 自动构建
- 正常使用时**不需要**在本地装 Ruby，改完推送即可，GitHub 会在 1~2 分钟内重新构建

## 目录结构（只需要关心这几个）

| 路径 | 放什么 |
| --- | --- |
| `_config.yml` | 站点标题、作者信息、社交链接、站点地址 |
| `_data/navigation.yml` | 顶部导航栏的栏目与顺序 |
| `_pages/about.md` | 首页 |
| `_pages/research.md` | 研究方向 |
| `_pages/members.md` | 成员（头像卡片） |
| `_pages/publications.md` | 成果发表（论文/项目/专利/获奖/开源） |
| `_pages/teaching.md` | 教学 |
| `_pages/join.md` | 加入我们 |
| `_pages/cv.md` | 个人简历 |
| `_posts/` | 团队活动与新闻，一篇一个文件 |
| `resources/` | 首页/研究方向配图、成员照片（大图放这里） |
| `images/` | 站点图标、logo 等主题素材 |
| `files/` | 论文 PDF、简历 PDF 等可下载文件 |

## 怎么加一篇团队活动/新闻

在 `_posts/` 下新建 `YYYY-MM-DD-英文短名.md`，文件名里的日期就是发布日期：

```markdown
---
title: '课题组参加 XXX 会议'
date: 2026-11-20
permalink: /posts/2026/11-20/blog/
tags:
  - 学术交流
---

正文第一段。

<div class="archive__image">
  <img src='/resources/图片文件名.jpg' alt="现场照片" style="max-width:100%;height:auto;" />
</div>

正文继续。
```

要点：

- `permalink` 里的年月日要和文件名日期一致，格式为 `/posts/YYYY/MM-DD/blog/`
- 图片先放进 `resources/`，再用 `/resources/文件名` 引用
- 图片文件名**尽量不要用空格和括号**，中文名可以用，但更推荐英文

## 怎么改成员

编辑 `_pages/members.md`。成员卡片是一个 HTML 网格，每人一块：

```html
<div style="text-align:center;">
<img src="/resources/张三.jpg" alt="张三" style="width:110px;height:110px;object-fit:cover;border-radius:50%;" />
<div style="font-weight:600;margin-top:8px;">张三</div>
<div style="font-size:0.8em;color:#8a8a8a;">2026 届</div>
</div>
```

没有照片的人，用首字母圆形占位（同文件里已有示例），不要留空 `img` 标签，否则会显示破图。

照片建议：正方形、边长 400~600px、正面半身、背景干净，总体积控制在 200KB 以内（可用 <https://squoosh.app> 压缩）。

## 怎么改研究方向 / 成果

- 研究方向：`_pages/research.md`，每个方向是「二级标题 + 一段说明 + 一张配图」，照抄格式加一节即可
- 成果：`_pages/publications.md`，按「期刊论文 / 会议论文 / 在投 / 项目 / 专利 / 获奖 / 开源项目」分组，条目用 `*` 列表

## 本地预览（可选）

需要 Ruby 3.x：

```bash
bundle install
bundle exec jekyll serve
```

打开 <http://127.0.0.1:4000>。本仓库当前维护者习惯直接推送后看线上效果。

## 发布

推送到 `master` 分支即触发 GitHub Pages 构建。首次部署需在仓库 Settings → Pages 里把 Source 设为 `Deploy from a branch` → `master` / `root`。

## 常见坑

- 中文路径的图片在 GitHub Pages 上可用，但 URL 会被转义成 `%E4%B8%AD...`，分享链接时注意
- 文件名大小写敏感：Linux 上 `Resources/x.png` ≠ `resources/x.png`，本地 Windows 能跑、线上 404，引用时统一用小写目录名
- front matter 的 `date` 必须写成 `2026-11-20`（月日补零），`2026-11-2` 会导致构建失败
