# 王喆楷 · 个人简历中心

> 上海杉达学院 · 计算机科学与技术 · 个人主页 / 简历站点

🌐 **线上访问（根域名）**：[https://wzk-12138.github.io/](https://wzk-12138.github.io/)

## 项目简介

这是一个基于纯静态 HTML 搭建的个人简历主页，托管于 GitHub Pages。页面包含个人简介、兴趣标签、作品展示，以及会自动同步的 GitHub 项目列表，整体采用简洁、克制的视觉风格，并适配移动端。

## 功能特性

- **简洁单页布局**：纯白底 + 单一蓝色主色 + 细分割线，自适应手机与桌面
- **核心信息一览**：个人照片、专业、学校、兴趣标签、联系方式
- **Works 作品区**：精选独立项目（AI 聊天助手、网站自动部署全览、游戏攻略站）
- **GitHub 项目自动同步**：页面加载时调用 GitHub API 实时拉取账号下的公开仓库，**新建仓库后刷新页面即自动出现**（本仓库 `wzk-12138.github.io` 自身已自动排除，不重复展示）

## 目录结构

```
wzk-12138.github.io/
├── index.html        # 简历主页面（GitHub Pages 入口）
├── assets/
│   └── photo.jpg      # 个人照片
├── .gitignore         # 忽略本地工作目录 .workbuddy
└── README.md
```

## 技术栈

- 原生 **HTML / CSS**（无框架、无构建步骤）
- **GitHub Pages** 静态托管
- **GitHub REST API** 实现项目列表实时同步

## 本地预览

1. 克隆仓库：

   ```bash
   git clone https://github.com/wzk-12138/wzk-12138.github.io.git
   cd resume
   ```

2. 用浏览器直接打开 `index.html` 即可（联网时 GitHub 项目区会实时同步）。

## 更新内容

- **修改页面**：编辑 `index.html` 后提交并 `git push`，GitHub Pages 会自动重新部署（通常 1 分钟内生效）。
- **新增作品 / 项目**：在 GitHub 新建仓库后，刷新简历页面即可自动出现在「GitHub Projects」区，无需改代码。

## 联系方式

- GitHub：[@wzk-12138](https://github.com/wzk-12138)
- 邮箱：[168463192@qq.com](mailto:168463192@qq.com)
