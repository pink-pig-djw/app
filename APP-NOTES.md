## 移动端封装说明

本项目采用原生 Android WebView 封装，而不是依赖远程网页，因此没有网络时也能打开。应用通过 JavaScript Bridge 补充了浏览器版 HTML 在 WebView 中缺少的文件导出与剪贴板能力。

应用默认载入：

```text
file:///android_asset/index.html#/home
```

如果将来接入在线影视资料库或云同步，需要在 AndroidManifest.xml 中加入 INTERNET 权限，并在网页侧配置真实 API 地址。
