# 王文莉 · 个人主页

一个手写的单文件个人主页：没有框架、没有构建工具，只有 `index.html` 里的 HTML / CSS / 原生 JS。托管在 GitHub Pages 上。

## 本地预览

双击 `index.html` 用浏览器打开即可。也可以在该目录下起一个本地服务：

```bash
python -m http.server 8000
# 然后访问 http://localhost:8000
```

## 需要改的地方

打开 `index.html`，搜索 `TODO` 就能找到所有要替换的位置：

| 位置 | 现在的内容 | 改成 |
| --- | --- | --- |
| 首屏 GitHub 按钮 | `https://github.com/` | 你的 GitHub 主页地址 |
| 联系区邮箱 | `wangwenli@example.com` | 你的真实邮箱 |
| 联系区 GitHub | `github.com/wangwenli` | 你的用户名 |
| 作品区三张卡片 | 示例项目 | 你真实的课设 / 项目 / 仓库 |

页面里的学校、时间线、技能标签也都写成了普通文字，直接改字即可。

## 发布到 GitHub Pages（一次性配置）

1. 在 GitHub 新建仓库，例如 `wangwenli-about`（不要勾选自动生成 README）。
2. 在本目录执行：

   ```bash
   git remote add origin https://github.com/<你的用户名>/wangwenli-about.git
   git push -u origin main
   ```

3. 打开仓库 → **Settings** → **Pages** →
   - Source 选 `Deploy from a branch`
   - Branch 选 `main`，目录选 `/ (root)`，点 Save
4. 等 1–3 分钟，访问 `https://<你的用户名>.github.io/wangwenli-about/`

想用更短的地址 `https://<你的用户名>.github.io/`，就把仓库命名为 `<你的用户名>.github.io`。

## 更新内容

改完 `index.html` 后：

```bash
git add -A
git commit -m "更新自我介绍"
git push
```

Pages 会自动重新构建，一两分钟后刷新页面即可。
