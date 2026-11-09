# 使用指南

本文档介绍如何在本地修改、预览并发布这份技术文档。

## 修改文档的基本流程

1. 在 `docs/` 目录中找到对应的 Markdown 文件进行编辑
2. 在本地启动预览服务，检查页面效果和链接是否正常
3. 确认无误后，提交修改并推送到 `main` 分支
4. 等待 GitHub Actions 自动完成构建和部署
5. 打开线上网站，确认内容已更新

## 常用命令

### 创建虚拟环境（首次使用）

```bash
python -m venv .venv
# Windows Git Bash
source .venv/Scripts/activate
# macOS / Linux
source .venv/bin/activate
```

### 安装依赖

```bash
python -m pip install -r requirements.txt
```

### 本地预览

```bash
python -m mkdocs serve
```

执行后访问 `http://127.0.0.1:8000/` 即可在浏览器中查看效果。修改文件后页面会自动刷新。

### 构建检查

```bash
python -m mkdocs build --strict
```

`--strict` 参数会将警告视为错误，帮助你提前发现断链等问题。

## 新增页面的方法

1. 在 `docs/` 下新建 `.md` 文件，例如 `docs/faq.md`
2. 编辑 `mkdocs.yml`，在 `nav` 中添加对应的导航项
3. 本地预览确认后提交推送

## 注意事项

- YAML 配置文件使用空格缩进，不要使用 Tab
- 导航中的路径是相对于 `docs/` 目录的，不要写成 `docs/index.md`
- `site/` 目录是自动生成的，不要手动修改，也不要提交到 Git（已在 `.gitignore` 中排除）
- 图片等资源文件建议放在 `docs/images/` 下，使用相对路径引用

[返回首页](index.md) | [关于本项目](about.md) | [API 参考](api.md)
