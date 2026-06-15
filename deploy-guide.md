# 上线指南 · GitHub + Vercel（拿到在线链接）

目标：把这个文件夹变成一个 https://你的名字.vercel.app 的在线链接，之后每次更新自动重新部署。
代码和网站永远属于你的 GitHub 账号，跟任何 AI 订阅无关，停订也不会消失。

---

## 方式 A · 零代码（推荐先用这个，最快）
1. 注册 GitHub 账号（github.com）。
2. 新建仓库 New repository → 命名如 `kero-portfolio` → Create。
3. 在仓库页点 “uploading an existing file”，把这个文件夹里的 **index.html、assets/ 整个文件夹、README.md** 全部拖进去上传 → Commit。
   （注意：要保持 assets 文件夹结构，直接拖文件夹进去即可。）
4. 注册 vercel.com，用 GitHub 账号登录 → Add New → Project → 选 `kero-portfolio` → Deploy。
5. 几十秒后得到在线链接。以后想改：在 GitHub 仓库里替换 assets 里的图片或编辑 index.html，Vercel 会自动更新。

## 方式 B · 用 Claude Code（适合以后频繁迭代、想省事）
把下面这段逐字发给 Claude Code（在终端或桌面端，用你的 Pro 账号）：

> 我有一个静态网站文件夹（index.html + assets/ + README.md），请帮我：
> 1）初始化 git 仓库并提交；
> 2）连接到我的 GitHub，新建一个名为 kero-portfolio 的仓库并推送；
> 3）告诉我接下来在 Vercel 导入并部署的步骤。
> 我没有代码基础，请每一步给出具体命令和说明。我的网站根目录是当前文件夹。

之后改内容时：

> 只更新 OneStory 项目页：把 assets/onestory/ 下的占位换成我新加的图片 hero.jpg / flow.jpg / system.jpg，并把那两页的占位框改成实际 <img>。其它项目和页面不要改动。改完帮我提交并推送。

> 这样只动一个项目，不会牵动全站，省 token 也不易出错。

## 自定义域名（可选）
Vercel → 项目 Settings → Domains，绑定你买的域名即可（如 kero.design）。
