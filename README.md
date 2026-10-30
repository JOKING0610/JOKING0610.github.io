# 星梦 Ximora · 官方网站

会思考 · 会动手 · 记得住 · 能造应用 —— 住在你手机里的 AI 搭档。

**线上地址**:<https://joking0610.github.io/>(经自定义域名 <https://www.joking0610.top/> 提供)

## 仓库结构

```
/            星梦官网(React + Vite 构建产物,由本仓库直接发布)
/other/      旧版「JOKING 的个人导航站」整体迁移于此,内部链接相对路径不受影响
CNAME        自定义域名配置(www.joking0610.top),请勿删除
.nojekyll    跳过 Jekyll 处理,加快发布
.ximora-deploy.json  部署脚本用的文件清单标记,请勿删除
```

## 更新官网

官网源码在本机 `D:\.desktop\Agent\ximora-web`(React 19 + Vite + Tailwind CSS v4,双主题)。

```bash
cd D:/.desktop/Agent/ximora-web
npm run build            # 产出 dist/
node scripts/deploy.mjs  # 通过 GitHub API 远端提交并触发 Pages 重新发布
```

部署脚本不需要克隆本仓库:它直接调用 GitHub Trees API,把 `dist/` 产物写入库根并提交。

## 旧版入口

- 旧版导航站:<https://joking0610.github.io/other/>
- 旧站各页面(music / snake / plan / constellation 等)都在 `/other/` 对应子目录下。
