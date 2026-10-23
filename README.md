# 王喆楷的个人简历主页

一个纯静态的个人简历页面：无构建、无框架、无后端，部署在 GitHub Pages 上。除手写的介绍内容外，「GitHub Projects」区块会在页面加载时实时调用 GitHub API 拉取公开仓库列表，自动展示项目名称、描述、主语言、Star 数、Fork 数与更新时间。

**在线访问：<https://wzk-12138.github.io/resume/>**

## 页面结构

| 区块 | 内容 |
| --- | --- |
| 头部 | 头像、姓名、学校与专业、GitHub 链接、一句自我介绍 |
| About | 专业、学校、兴趣 |
| Interests | 运动 / 魔方 / 编程 / 计算机科学标签 |
| Works | 精选作品：每次打开页面时从 GitHub 仓库自动评选 3 个代表性项目 |
| GitHub Projects | 实时同步的 GitHub 公开仓库列表 |
| Contact | GitHub 与邮箱 |

## 功能特性

- **精选作品自动评选**：「Works」区块每次打开页面时，从全部公开仓库中自动挑出 3 个代表性项目——按「有介绍 / 有主语言 / 最近更新 / Star 数」评分，并保证入选项目语言不重复；上传新仓库后无需改代码，刷新页面即重新评选。
- **实时同步 GitHub 项目**：请求 `api.github.com/users/wzk-12138/repos`，按更新时间排序取最近 50 个仓库，自动过滤 fork 与简历仓库自身；每个仓库展示主语言（带语言色点）、★ Star 数、⑂ Fork 数与更新日期，同步说明中显示项目总数与刷新时间。
- **失败兜底**：实时拉取失败时显示空状态提示并说明原因，页面其余内容不受影响（「Works」区块此时自动隐藏）。
- **纯静态单文件**：`index.html` 一个文件包含全部样式与脚本，克隆后双击即可打开，也可托管到任意静态平台。
- **响应式布局**：桌面端为 760px 窄栏单列排版；视口小于 560px 时头像与资料改为纵向排列。
- **排版细节**：Noto Sans SC 字体、细分割线、大写英文小区标签、链接 hover 下划线反馈。

## 本地运行

无需安装任何依赖，任选其一：

```bash
# 方式一：直接用浏览器打开
open index.html

# 方式二：起一个静态服务器（推荐）
python -m http.server 8000
# 访问 http://localhost:8000
```

## 部署

推送到 GitHub 后，在仓库 **Settings → Pages → Build and deployment** 中选择 `main` 分支根目录，Pages 会自动发布到 `https://wzk-12138.github.io/resume/`。

## 文件结构

```
.
├── index.html          # 页面全部内容（结构 + 样式 + 脚本）
├── assets/
│   └── photo.jpg       # 头像
└── README.md
```

## 技术栈

HTML + CSS + 原生 JavaScript，无框架、无构建步骤；字体使用 Google Fonts 的 Noto Sans SC。
