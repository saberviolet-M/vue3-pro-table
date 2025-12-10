# GitHub 版本管理指南

## 📋 已完成的工作

### 1. 版本文档创建 ✅
- **CHANGELOG.md**: 完整的版本变更记录
- **README.md**: 更新了版本信息和徽章
- **README.zh-CN.md**: 中文版本信息更新

### 2. 自动化工具 ✅
- **scripts/generate-release-md.js**: Release Markdown 生成脚本
- **CREATE_RELEASE.md**: 详细的 Release 创建指南

### 3. CI/CD 配置 ✅
- **.github/workflows/ci.yml**: 自动化测试工作流
- **.github/workflows/publish.yml**: 自动发布工作流

## 🚀 如何在 GitHub 上体现版本更新

### 方法 1: 创建 GitHub Release (推荐)

#### 步骤:
1. **访问 Releases 页面**: https://github.com/saberviolet-M/vue3-pro-table/releases
2. **点击 "Draft a new release"**
3. **填写 Release 信息**:
   - **Tag version**: `v1.0.0-alpha.2`
   - **Target**: `main`
   - **Title**: `v1.0.0-alpha.2 - 类型支持、测试增强和文档完善`
   - **Description**: 使用脚本生成的内容
4. **发布选项**:
   - ☑️ Set as latest release
   - ☑️ Create a discussion for this release (可选)
5. **点击 "Publish release"**

#### 快速生成 Release 内容:
```bash
# 运行生成脚本
node scripts/generate-release-md.js

# 输出可以直接复制到 GitHub Release 描述区域
```

### 方法 2: 使用 GitHub Actions 自动发布

已配置的 `publish.yml` 工作流会在创建 Release 时自动:
1. ✅ 运行所有测试
2. ✅ 构建项目
3. ✅ 发布到 npm
4. ✅ 发布到 GitHub Packages

### 方法 3: 手动更新 GitHub 项目信息

1. **更新项目描述**: 在仓库设置中更新描述
2. **添加 Topics**: 添加相关标签如 `vue3`, `table`, `ant-design-vue`, `typescript`
3. **更新 README 预览**: GitHub 会自动显示更新后的 README

## 📊 版本信息在 GitHub 的体现位置

### 1. **Releases 页面**
- 版本历史记录
- 下载统计
- 版本说明文档

### 2. **README 徽章**
- npm 版本徽章: ![npm version](https://img.shields.io/npm/v/vue3-pro-table-antd.svg)
- GitHub Actions 状态: ![GitHub Actions](https://img.shields.io/github/actions/workflow/status/saberviolet-M/vue3-pro-table/ci.yml)

### 3. **仓库首页**
- README 中的版本信息
- 最近更新摘要
- 安装说明

### 4. **Insights 页面**
- 发布频率统计
- 下载量统计
- 版本趋势

## 🔄 版本发布流程

### 标准发布流程
1. **开发完成** → 提交代码到 `main` 分支
2. **版本更新** → 更新 `package.json` 版本号
3. **文档更新** → 更新 CHANGELOG.md 和 README
4. **创建 Release** → 在 GitHub 创建 Release
5. **自动发布** → GitHub Actions 自动发布到 npm

### 版本命名规范
- `v1.0.0-alpha.2`: Alpha 版本
- `v1.0.0-beta.1`: Beta 版本
- `v1.0.0`: 正式版本
- `v1.0.1`: 补丁版本
- `v1.1.0`: 小版本更新
- `v2.0.0`: 大版本更新

## 📈 监控和统计

### 发布后验证
1. **npm 验证**: https://www.npmjs.com/package/vue3-pro-table-antd
2. **CDN 验证**: https://unpkg.com/vue3-pro-table-antd@1.0.0-alpha.2/
3. **GitHub 验证**: https://github.com/saberviolet-M/vue3-pro-table/releases

### 统计指标
- **npm 下载量**: `npm view vue3-pro-table-antd`
- **GitHub 星标**: 仓库星标数
- **Release 下载**: Releases 页面下载统计
- **CI/CD 状态**: Actions 页面构建状态

## 🛠 维护工具

### 常用命令
```bash
# 查看当前版本
npm view vue3-pro-table-antd version

# 生成 Release Markdown
node scripts/generate-release-md.js

# 运行测试
npm test

# 构建项目
npm run build

# 发布新版本 (手动)
npm publish --access public
```

### 版本更新脚本示例
```bash
#!/bin/bash
# 更新版本号
npm version patch  # 或 minor, major, prerelease

# 生成 Release 内容
node scripts/generate-release-md.js > RELEASE_NOTES.md

# 提交和推送
git add .
git commit -m "chore: release v$(node -p "require('./package.json').version")"
git push

# 创建 Git tag
git tag -a "v$(node -p "require('./package.json').version")" -m "Release v$(node -p "require('./package.json').version")"
git push --tags
```

## 📞 支持与反馈

- **问题报告**: GitHub Issues
- **功能请求**: GitHub Discussions
- **文档问题**: 提交 Pull Request
- **紧急问题**: 创建 Issue 并标记为 `bug`

---

**最后更新**: 2025-12-09
**当前版本**: v1.0.0-alpha.2
**维护状态**: 活跃开发中