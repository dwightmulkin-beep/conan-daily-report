# Conan日报 - GitHub Pages 部署指南

## 📁 文件夹结构

```
conan-daily-report/
├── index.html          # 密码验证页
├── dashboard.html      # 日报总览页
├── README.md           # 本文件
└── 日报/
    └── 2026-03-24.html # 日报详情页
```

## 🚀 部署步骤

### 1. 创建GitHub仓库

1. 登录 GitHub
2. 点击右上角 `+` → `New repository`
3. 仓库名称：`conan-daily-report`（私有仓库）
4. 不要勾选 Initialize with README
5. 点击 `Create repository`

### 2. 本地初始化并推送

在 `D:\OpenClaw_Files\日报-网站` 目录下执行：

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/你的用户名/conan-daily-report.git
git push -u origin main
```

### 3. 开启GitHub Pages

1. 进入仓库 `Settings`
2. 左侧菜单找到 `Pages`
3. Source 选择 `main` 分支，`/ (root)` 文件夹
4. 点击 `Save`
5. 等待1-2分钟，网站地址：`https://你的用户名.github.io/conan-daily-report/`

## 🔐 修改密码

编辑 `index.html`，找到这行：

```javascript
const CORRECT_PASSWORD = 'conan2026';
```

把 `conan2026` 改成你自己的密码。

## 📝 每日更新

每天运行 `push-daily-report.bat` 或手动推送新HTML文件到 `日报/` 文件夹。

## ❓ 常见问题

**Q: 忘记密码怎么办？**
A: 联系Conan获取密码，或修改index.html中的CORRECT_PASSWORD变量。

**Q: 能改成其他仓库名吗？**
A: 可以，但记得同步修改所有HTML文件中的链接引用。
