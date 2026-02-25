# Hayden Best Skills - 创建指南

## 步骤 1：在 GitHub 创建仓库

1. 访问 https://github.com/new
2. 仓库名：`hayden-best-skills`
3. 设为 Public 或 Private（根据你的偏好）
4. **不要**勾选 "Add a README file"（我们已经创建好了）
5. 点击 "Create repository"

## 步骤 2：推送本地仓库到 GitHub

```bash
cd /Users/hayden/hayden-best-skills

# 初始化 Git
git init

# 添加文件
git add .

# 首次提交
git commit -m "feat: add git-sync skill"

# 添加远端（替换 YOUR_USERNAME 为你的 GitHub 用户名）
git remote add origin git@github.com:hayden/hayden-best-skills.git

# 推送
git push -u origin main
```

## 步骤 3：在 writingsystem 中添加 Submodule

```bash
cd /Users/hayden/WeChatProjects/writingsystem

# 添加 submodule
git submodule add git@github.com:hayden/hayden-best-skills.git skills/@common

# 提交
git add .gitmodules skills/@common
git commit -m "feat: add common skills submodule"
git push
```

## 步骤 4：验证

```bash
# 检查子模块目录
ls -la skills/@common/skills/
# 应该看到 git-sync.md
```

## 当前状态

本地文件已创建在 `/Users/hayden/hayden-best-skills/`

- ✅ `skills/git-sync.md` — 同步技能
- ✅ `README.md` — 使用说明

**下一步**：请在 GitHub 创建仓库后告诉我，我将继续执行。
