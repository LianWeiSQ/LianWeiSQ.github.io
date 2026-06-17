# William / LianWeiSQ GitHub Pages

这是一个可以直接发布到 GitHub Pages 的静态个人主页，参考 `qzweng.github.io` 的学术主页信息架构，但内容定位为工程型开源个人品牌：

- Agent Harness Engineering
- OpenAgent runtime
- BrainBox sandbox
- Fintech Agent
- GitOps / eval / trace / context engineering

## 本地预览

```bash
python3 -m http.server 4173
```

然后打开：

```text
http://127.0.0.1:4173
```

## 发布到 GitHub Pages

推荐创建用户主页仓库：

```bash
gh repo create LianWeiSQ.github.io --public --source=. --remote=origin --push
```

如果已经创建过仓库：

```bash
git init
git branch -M main
git remote add origin git@github.com:LianWeiSQ/LianWeiSQ.github.io.git
git add .
git commit -m "Launch personal homepage"
git push -u origin main
```

GitHub Pages 用户站点会自动发布到：

```text
https://LianWeiSQ.github.io/
```

## 设计参考

- `assets/design-concept.png`：本次生成的视觉概念图，用于后续迭代时保持设计方向一致。

## 上线前要替换

- `mailto:hello@example.com`：替换成真实邮箱，或删除 Email 链接。
- 头像区域：现在是 SVG 占位，可以后续换成真实头像或个人符号。
- Writing links：目前部分是占位 `#`，建议发布对应文章后补上真实链接。
- News 时间线：每 1-2 周更新一次，让网站看起来持续经营。
