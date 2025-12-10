# 创建 GitHub Release 指南

## 步骤 1: 访问 GitHub Releases 页面

1. 打开浏览器，访问: https://github.com/saberviolet-M/vue3-pro-table/releases
2. 点击 "Draft a new release" 按钮

## 步骤 2: 填写 Release 信息

### Tag 版本
- **Tag version**: `v1.0.0-alpha.2`
- **Target**: `main` (默认)

### Release 标题
```
v1.0.0-alpha.2 - 类型支持、测试增强和文档完善
```

### Release 描述
复制以下内容到描述区域：

```
## 🚀 新版本亮点

### ✅ 新增功能
- **完整的 TypeScript 支持**: 所有组件都有完整的类型定义
- **增强的测试覆盖**: 全面的边缘情况测试
- **CDN 支持**: 可通过 unpkg 和 jsDelivr 使用
- **CI/CD 流水线**: 自动化测试和发布工作流
- **详细的示例**: 基础、高级和 CDN 使用示例

### 🔧 技术改进
- 修复 TypeScript 类型生成问题
- 标准化属性命名 (`hideInSearch`)
- 改进表单验证处理
- 优化组件引用暴露
- 更新构建配置

### 📚 文档更新
- 完整的更新日志 (CHANGELOG.md)
- 详细的用法示例
- CDN 使用指南
- 版本信息徽章

## 📦 安装方式

```bash
# npm
npm install vue3-pro-table-antd

# yarn
yarn add vue3-pro-table-antd

# pnpm
pnpm add vue3-pro-table-antd

# CDN
<script src="https://unpkg.com/vue3-pro-table-antd/dist/pro-table.umd.js"></script>
```

## 🔗 相关链接
- [npm 包页面](https://www.npmjs.com/package/vue3-pro-table-antd)
- [完整文档](README.md)
- [更新日志](CHANGELOG.md)
- [示例代码](examples/)

## 📝 详细变更
查看完整的变更记录: [CHANGELOG.md](CHANGELOG.md)

---

**🤖 此版本由 Claude Code 协助生成**
```

## 步骤 3: 发布选项

- **☑️ Set as latest release**: 勾选（设置为最新版本）
- **☑️ Create a discussion for this release**: 可选（创建讨论）
- **📁 Attach binaries**: 可选附加文件

## 步骤 4: 发布

点击 "Publish release" 按钮完成发布。

## 自动发布说明

项目已配置 GitHub Actions 工作流 (`publish.yml`)，当创建新的 Release 时会自动：
1. 运行测试
2. 构建项目
3. 发布到 npm
4. 发布到 GitHub Packages

## 版本标签说明

- `v1.0.0-alpha.2`: 当前版本
- `latest`: 最新稳定版本标签
- `alpha`: Alpha 版本通道
- `beta`: Beta 版本通道（未来使用）

## 验证发布

发布后可以访问以下链接验证：
- https://github.com/saberviolet-M/vue3-pro-table/releases
- https://www.npmjs.com/package/vue3-pro-table-antd
- https://unpkg.com/vue3-pro-table-antd@1.0.0-alpha.2/