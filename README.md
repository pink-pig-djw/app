# Afterglow Android App

这是由 `Afterglow-Standalone(2).html` 封装而成的独立 Android 应用项目，应用名称为 **Afterglow**，并使用用户提供的日落倒影图作为应用图标。

## 已完成

- 应用启动后直接进入 Afterglow 首页，不显示网站落地页
- 完整离线运行，HTML、CSS、JavaScript 和模拟数据均内置在 APK 中
- WebView 的 `localStorage` 用于保存私人影视档案
- 支持手机端底部导航、触摸操作和横竖屏
- 支持从系统相册/文件管理器上传封面与私人图片
- 支持将 JSON、Markdown、PDF 等导出文件保存到 `Downloads/Afterglow`
- 支持 Android 返回键、外部链接跳转和系统剪贴板
- 不申请相机、通讯录、定位等敏感权限

## 在 Android Studio 中生成 APK

1. 使用 Android Studio 打开本文件夹。
2. 等待 Gradle 同步完成；推荐 **JDK 17、Gradle 8.9、Android SDK 35**。
3. 选择 `Build > Build Bundle(s) / APK(s) > Build APK(s)`。
4. 生成文件位于：

```text
app/build/outputs/apk/debug/app-debug.apk
```

## 使用 GitHub Actions 自动生成 APK

项目已包含 `.github/workflows/build-apk.yml`。将整个文件夹上传到 GitHub 后，在 **Actions → Build Afterglow APK → Run workflow** 中运行，即可下载构建好的 APK。

## 本地数据说明

应用数据默认保存在 Android WebView 的本地存储中。卸载应用或清除应用数据会删除本地档案，因此建议定期使用 Afterglow 的导出功能备份。

## 修改网页内容

替换以下文件后重新构建即可：

```text
app/src/main/assets/index.html
```

## 应用标识

```text
应用名称：Afterglow
包名：com.afterglow.app
版本：1.0.0
最低系统：Android 8.0（API 26）
```
