# Hayden Best Skills

> 公共 Claude Skills 仓库，供多个项目共享复用。

## 概述

这是一个集中管理和共享 AI 技能（Skills）的仓库，通过 Git Submodule 的方式集成到各个项目中。技能定义了 AI 助手在特定场景下的行为模式和工作流程。

## 使用方式

### 作为 Git Submodule 添加到项目

```bash
# 在项目根目录执行
git submodule add git@github.com:HaydWang/hayden-best-skills.git skills/@common

# 提交
git add .gitmodules skills/@common
git commit -m "feat: add common skills submodule"
git push
```

### 克隆包含 Submodule 的项目

```bash
# 方法 1：克隆时自动拉取子模块
git clone --recurse-submodules git@github.com:HaydWang/your-project.git

# 方法 2：如果已经克隆，单独拉取子模块
cd your-project
git submodule update --init --recursive
```

### 更新子模块到最新版本

```bash
# 在项目中拉取子模块最新代码
git submodule update --remote --merge

# 或进入子模块目录直接 pull
cd skills/@common
git pull
```

## 技能列表

| 技能文件 | 触发词 | 说明 |
|---------|-------|-----|
| `git-sync.md` | sync, 同步, 推送, 提交 | Git 多设备同步技能 |

## 目录结构

```
hayden-best-skills/
├── skills/
│   └── git-sync.md
└── README.md
```

## 在项目中加载

智子启动时会扫描 `skills/@common/skills/` 中的所有 `.md` 文件并自动注册为可用技能。

## 修改技能

### 修改公共技能

```bash
# 1. 在子模块目录中修改
cd skills/@common
vim skills/git-sync.md

# 2. 提交修改
git add .
git commit -m "fix: improve xxx skill"
git push

# 3. 在主项目中记录新版本
cd ../..
git add skills/@common
git commit -m "chore: update @common to latest"
git push
```

## 技能开发规范

### 技能文件格式

每个技能是一个 Markdown 文件，包含：

```markdown
---
name: 技能名称
description: 触发词说明
---

# 技能标题

## 目的
简要说明技能的作用

## 触发词
- "触发词1" / "触发词2"

## 执行流程
步骤说明...
```

## 其他项目集成

要在其他项目中使用这些公共技能：

```bash
cd ~/path/to/another-project
git submodule add git@github.com:HaydWang/hayden-best-skills.git skills/@common
git add .gitmodules skills/@common
git commit -m "feat: add common skills submodule"
```

## License

MIT
