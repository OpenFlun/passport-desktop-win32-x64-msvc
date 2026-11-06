# @flun/passport-desktop-win32-x64-msvc

## 简介

提供 **x86_64-pc-windows-msvc** 的 Windows Hello 操作原生二进制,
构建自 [passport-desktop](https://github.com/OpenFlun/passport-desktop) 源码;

用于需要在 Node.js 项目中直接调用 Windows Hello API 的场景;

---

## 安装

```bash
npm install @flun/passport-desktop-win32-x64-msvc
```

本包仅支持 Windows 64 位(x64);安装时 npm 会依据 `os` 与 `cpu` 字段自动跳过不匹配的平台;

---

## 许可证

ISC