# Project AIRI

Project AIRI 是一个面向 AI 虚拟角色 / AI waifu 的应用项目，目标是让 AI 角色以 Web、桌面端、移动端和服务端能力进入真实使用场景。

项目采用 pnpm workspace 管理，主要包含：

- `apps/stage-web`：Web 版应用。
- `apps/stage-tamagotchi`：Electron 桌面版应用。
- `apps/stage-pocket`：移动端应用。
- `apps/server`：服务端 API。
- `packages/*`：共享 UI、业务组件、SDK、运行时和工具包。
- `docs`：项目文档站。

## 环境要求

- Node.js：建议使用当前 LTS 版本。
- pnpm：项目声明版本为 `pnpm@10.33.0`。
- Git：用于版本管理和上传云端仓库。

启用 pnpm：

```powershell
corepack enable
corepack prepare pnpm@10.33.0 --activate
pnpm -v
```

## 快速开始

安装依赖：

```powershell
pnpm install
```

启动 Web 版：

```powershell
pnpm dev:web
```

启动桌面 Electron 版：

```powershell
pnpm dev:tamagotchi
```

启动文档站：

```powershell
pnpm dev:docs
```

启动 Server API：

```powershell
pnpm -F @proj-airi/server dev
```

Server API 默认读取：

```text
apps/server/.env.local
```

## 常用命令

构建 Web 版：

```powershell
pnpm build:web
```

构建桌面 Electron 版：

```powershell
pnpm build:tamagotchi
```

构建全部应用和包：

```powershell
pnpm build
```

类型检查：

```powershell
pnpm typecheck
```

Lint 检查：

```powershell
pnpm lint
```

自动修复 Lint：

```powershell
pnpm lint:fix
```

运行测试：

```powershell
pnpm test:run
```

## 重新建立 Git 仓库

如果当前目录没有 `.git`，可以重新初始化仓库：

```powershell
git init
git branch -M main
git add .
git commit -m "chore: initialize repository"
```

绑定远端并上传：

```powershell
git remote add origin https://github.com/<你的账号>/<你的仓库>.git
git push -u origin main
```

更多操作命令见 `操作文档.md`。
