# 我的技术文档网站

基于 MkDocs Material 搭建的个人技术文档网站，通过 GitHub Actions 自动部署到 GitHub Pages。

## 🌐 访问地址

**在线网站**：https://chencai170.github.io/my-docs/

## 📖 实验报告

详细的实践过程、关键截图和原理理解请查看：[个人实验报告](report/README.md)

## 🛠 技术栈

| 工具 | 用途 |
| --- | --- |
| MkDocs Material | 静态网站生成器 |
| GitHub Actions | 自动构建与部署 |
| GitHub Pages | 网站托管 |

## 📁 项目结构

```
my-docs/
├── .github/workflows/deploy.yml   # CI/CD 工作流
├── docs/                          # 文档源码
│   ├── index.md
│   ├── about.md
│   ├── guide.md
│   └── api.md
├── report/                        # 实验报告
│   ├── README.md
│   └── images/
├── mkdocs.yml                     # MkDocs 配置
├── requirements.txt               # Python 依赖
└── README.md
```

## 🚀 本地预览

```bash
# 创建虚拟环境
python -m venv .venv
source .venv/Scripts/activate   # Windows Git Bash

# 安装依赖
python -m pip install -r requirements.txt

# 启动预览服务
python -m mkdocs serve
```

访问 http://127.0.0.1:8000/ 查看效果。

## 📝 作者

chencai170
