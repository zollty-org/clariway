# clariway-okr 贡献指南

欢迎参与 clariway-okr 开源项目！本指南将帮助您了解如何为项目做出贡献。在开始前，请花几分钟阅读这份文档。

## 📜 行为准则

所有参与者需遵守我们的[行为准则](CODE_OF_CONDUCT.md)。我们致力于创建开放、友好且尊重的社区环境。

## 🐛 报告问题

发现Bug或有改进建议？请：
1. 在[Issues页面](https://github.com/zollty-org/clariway/issues)搜索是否已有相关讨论
2. 创建新Issue，选择对应模板
3. 清晰描述问题（环境、复现步骤、期望结果等）
4. 添加相关标签（bug, enhancement, question等）

## 💡 功能建议

有新功能想法？请：
1. 创建"Feature Request"类型的Issue
2. 描述功能背景、价值和使用场景
3. 如有设计草图或参考实现请附上

## 🛠 开发环境搭建

### 后端环境
```bash
# 克隆项目
git clone https://github.com/zollty-org/clariway.git
cd clariway/src/backend

# 安装依赖
mvn install

# 启动服务
mvn spring-boot:run
```

### 前端环境 (PC Web端)
```bash
cd frontend/web-app
npm install
npm run serve
```

### 前端环境 (移动端H5)
```bash
cd frontend/mobile-h5
npm install
npm run serve
```

### 数据库
项目使用MySQL，请使用`scripts/db-migration/init.sql`初始化数据库

## ✍ 代码规范

### 通用要求
- 使用有意义的变量/方法名
- 添加必要的注释（特别是复杂逻辑）
- 保持方法短小（不超过50行）
- 删除调试代码和注释掉的代码

### Java 规范
- 遵循Google Java风格指南
- 使用4空格缩进
- 类/方法需有Javadoc注释
```java
/**
 * 创建OKR目标
 * @param objective 目标对象
 * @return 创建后的目标ID
 */
public Long createObjective(Objective objective) {
    // 实现逻辑
}
```

### Vue 规范
- 组件使用PascalCase命名
- 单文件组件结构顺序：template > script > style
- Props需定义类型和默认值
```vue
<script>
export default {
  props: {
    // 带默认值的数字类型
    rating: {
      type: Number,
      default: 0
    }
  }
}
</script>
```

## ✅ 测试要求

提交代码前请确保：
- 后端：所有单元测试通过
  ```bash
  cd backend
  mvn test
  ```
- 前端：关键组件有单元测试
  ```bash
  cd frontend/web-app
  npm run test:unit
  ```
- 新功能需添加相应测试用例
- 重要路径需有集成测试

## 🔀 Pull Request流程

1. Fork项目仓库
2. 创建特性分支：
   ```bash
   git checkout -b feat/add-new-feature
   # 或
   git checkout -b fix/login-issue
   ```
3. 提交代码变更
4. 推送分支到您的Fork
5. 创建Pull Request(PR)
6. 等待CI验证和代码审查

### PR规范
- 标题格式：`[类型] 简短描述` (如：`[Feat] 添加用户导出功能`)
- 类型前缀：
  - `Feat`：新功能
  - `Fix`：Bug修复
  - `Docs`：文档更新
  - `Style`：代码样式调整
  - `Refactor`：重构代码
  - `Test`：测试相关
- 内容需包含：
  - 变更目的和背景
  - 测试情况
  - 相关Issue编号（如：Closes #123）

## 🔍 代码审查

所有PR需经过至少2位核心成员审查：
- 审查者会在3个工作日内回复
- 请及时处理审查意见
- 通过审查后代码将被合并

## 🎉 致谢

感谢每位贡献者！您的名字将被列在[项目贡献者列表](CONTRIBUTORS.md)中。

---

**准备好贡献了吗？** 查看[Good First Issues](https://github.com/zollty-org/clariway/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22)开始您的第一个贡献！