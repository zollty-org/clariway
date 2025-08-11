# clariway-okr 更新日志

本项目遵循[语义化版本](https://semver.org/lang/zh-CN/)规范，所有版本变更都会记录在此文件中。

## [Unreleased]
### Added
- 新增OKR进度可视化图表功能
- 添加移动端手势操作支持

### Changed
- 优化目标对齐关系展示方式
- 改进后端API响应时间

### Fixed
- 修复用户权限缓存失效问题 (#123)
- 修正移动端日期选择器时区问题 (#156)

---

## [1.2.0] - 2024-03-15
### Added
- 🎉 新增团队OKR对比分析功能
- 支持OKR模板导入/导出
- 添加Slack通知集成

### Changed
- ⚡ 性能优化：减少前端首屏加载时间30%
- 重构权限校验中间件
- 更新Vue3到最新稳定版

### Fixed
- 修复周报生成格式错乱问题 (#98)
- 修正目标进度计算偏差 (#102)
- 解决Safari浏览器兼容性问题 (#115)

### Breaking Changes
- 🔧 数据库迁移：需要执行 `ALTER TABLE objectives ADD template_id INT`
- 废弃API：`GET /api/v1/okr/list` 改用 `GET /api/v2/okrs`

---

## [1.1.3] - 2024-02-10
### Fixed
- 紧急修复登录令牌过期异常
- 修正移动端键盘遮挡输入框问题

---

## [1.1.0] - 2024-01-20
### Added
- 新增多语言支持（中/英）
- 实现OKR树形结构展示
- 添加JWT自动续期功能

### Changed
- 优化移动端适配方案
- 升级Spring Boot到3.1.5

### Deprecated
- 标记旧版导出接口将在v2.0移除

---

## [1.0.0] - 2023-12-01
### Initial Release
- 核心OKR管理功能
  - 目标/关键结果创建
  - 进度跟踪
  - 对齐视图
- 基础用户权限系统
- PC端和移动H5基础版

---

## 版本格式说明
版本号遵循 `MAJOR.MINOR.PATCH` 格式：
- `MAJOR`：不兼容的API修改
- `MINOR`：向后兼容的功能新增
- `PATCH`：向后兼容的问题修正

## 如何查看历史版本
```bash
git tag -n  # 查看所有版本标签
git checkout v1.1.0  # 切换到特定版本
```

> 提示：项目使用[Keep a Changelog](https://keepachangelog.com/)规范记录变更