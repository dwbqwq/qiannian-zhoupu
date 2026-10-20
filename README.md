# 千年舟谱

中国船舶史三维动态海报，GitHub Pages 部署版本。

本版本从用户指定的完整单文件网页提取，保留原有页面设计、20 个船舶模型、20 段介绍视频和 7 处造船动态插图。图片、视频和模型采用相对路径，可部署在 GitHub Pages 的仓库子路径下。

## 文件说明

- `index.html`：网站首页及原有交互代码。
- `assets/`：提取的原始资源，未降低分辨率或重新编码。
- `resource-manifest.json`：原文件和资源的 SHA-256 校验值。
- `.nojekyll`：让 GitHub Pages 直接发布静态文件。

集装箱船模型超过 GitHub 的普通单文件限制，按原始字节顺序拆分为多个文件。网站查看器在打开该模型时自动加载并拼接。请完整保留所有资源及文件名。

## 本地预览

在本目录运行 `python -m http.server 8000`，然后用浏览器打开 `http://localhost:8000/`。请通过本地 HTTP 服务器预览，模型加载需要 HTTP 请求。

## 发布到 GitHub Pages

将本目录全部内容提交到目标仓库的 `main` 分支。在仓库 `Settings > Pages` 中，将发布来源设为 `Deploy from a branch`，选择 `main` 和 `/(root)`。

如果仓库是 `dwbqwq/qiannian-zhoupu`，发布完成后的地址为 `https://dwbqwq.github.io/qiannian-zhoupu/`。该地址只有在实际部署成功后才可访问。

## 更新与回退

修改资源后需同时更新对应引用及资源清单。保留 Git 提交记录，即可通过恢复此前的提交回退。原始单文件网页未被修改。
