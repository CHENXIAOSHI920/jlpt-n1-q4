# 问题四完整版 · 发布用

这个文件夹是可以部署到 HTTPS 的离线 PWA 版本。

## 直接发给别人

如果只想把网页文件发给别人，请使用 `问题四_N1_词汇_离线分享版.zip` 里的单文件 HTML；它双击就能离线使用。

## 安装到手机

PWA 需要通过 HTTPS 打开一次：

1. 把本文件夹部署到静态网站。
2. 用手机浏览器打开地址。
3. Safari 选择「分享 → 添加到主屏幕」。
4. 第一次联网加载完成后，Service Worker 会缓存页面，之后断网也能打开。

## 可用的免费托管

- GitHub Pages
- Cloudflare Pages
- Netlify Drop

把本文件夹作为站点根目录上传即可。`manifest.webmanifest`、`sw.js` 和三个 PNG 图标需要保持在同一目录。

部署完成后会得到一个固定的 HTTPS 地址。第一次联网打开后，页面会缓存到本地，之后断网也能继续使用。

最简单的方式是打开 Netlify Drop，把本文件夹直接拖进去，然后按提示认领站点；认领后链接才会长期保留。想要最稳定的免费地址，可以新建一个 GitHub 仓库，把本文件夹里的文件上传到仓库根目录，再到仓库的 Settings → Pages 中选择从主分支根目录发布。

## 本地测试

在本目录运行：

```sh
python3 -m http.server 8000
```

然后打开 `http://localhost:8000`。直接双击 `index.html` 可以使用单文件功能，但浏览器不会注册 Service Worker。
