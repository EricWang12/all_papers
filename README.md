# all_papers · Zhaoning Paper Pile

我的 paper library。每篇 paper 归档到它服务的 project 下，旁边放一页 explainer：

```
<Project>/<YYYY-MM-DD>-<Short>.pdf            ← 只在本地，不进 git
<Project>/artifact/<YYYY-MM-DD>-<Short>.html   ← explainer，浏览器直接打开
<Project>/artifact/<YYYY-MM-DD>-<Short>/       ← 页面里用到的作者原图
```

- 在线版：artifact "Zhaoning Paper Pile"，https://claude.ai/artifact/GGxYmvE3MgSAJUQDSi9EHb
- `index.html`：首页，每加一篇 paper 自动重建
- PDF 不进 git（`.gitignore`）：git 会永远保留历史里的文件，PDF 会让 repo 越来越大。每个页面都记录了带版本号的 PDF 链接（`paper:pdf`），任何机器都能重新下载同一份
- `preferences.md`：页面怎么写（reader profile、projects）。改它，以后所有页面都跟着变

由 [zw-claude-skills](https://github.com/EricWang12/zw-claude-skills) 里的 `paper-explain` skill 维护：每次先 pull，加一篇 paper，再 commit + push。
