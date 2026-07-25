# Changelog
## [1.0.3] - 2026-07-26 11:51
- 修复了在某些情况下应用首次调用 Windows hello 弹窗弹出时没有置顶的问题;

## [1.0.2] - 2026-07-25 08:41
- 修复了 Windows hello 弹窗弹出时没有置顶的问题;

## [1.0.1] - 2026-07-24 16:25
### 新增
- 首次发布 `@flun/passport-desktop-win32-x64-msvc` 🎉
- 提供 Windows Hello 身份验证的 Node.js 原生模块（基于 MSVC 编译的 `.node` 文件）
- 支持通过 Windows 后端调用生物识别（指纹、面部识别、PIN 码）
- 专为 Windows x64 平台优化，无需本地构建工具即可直接安装使用
- 模块严格限定 `os` 为 `win32`、`cpu` 为 `x64`，避免误装到不兼容环境
- 公开 npm 权限，任何项目均可通过 `@flun/passport-desktop-win32-x64-msvc` 引用

### 技术细节
- 基于 Node-API（或 N-API）保证跨 Node 版本的 ABI 稳定性
- 内部调用 Windows Security Support Provider Interface (SSPI) 和 Windows Hello API
- 该包作为平台特定实现，不发布与之对应的抽象主包（由内部集成使用）

### 已知限制
- 仅支持 Windows 10/11 且已配置 Windows Hello 的设备
- 需要系统开启生物识别功能，否则调用会返回相应错误码