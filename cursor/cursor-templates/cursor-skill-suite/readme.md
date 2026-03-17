# Cursor Skill Suite

这是一个 Cursor IDE 的技能套件集合，用于增强开发和项目管理体验。每个套件包含专门的提示、规则和技能，帮助开发者更高效地处理各种任务。

## 技能套件

| 套件名称 | 描述 | 状态 |
|----------|------|------|
| system-analyze | 自动系统分析套件，用于扫描项目仓库、识别工程类型并生成系统架构文档 | ✅ 已发布 |

### system-analyze

**system-analyze** 是一个用于自动系统分析的 Cursor 技能套件。它能够扫描项目仓库，识别工程类型，并生成详细的系统架构文档。

#### 功能特性

- **项目扫描**：自动识别后端、前端、移动端等工程类型
- **架构图生成**：创建系统架构图和模块调用链图
- **API 映射**：列出所有 API 接口和调用链
- **数据库建模**：生成数据库 ER 图
- **前端映射**：分析前端/移动端页面结构和流程
- **文档输出**：将所有分析结果输出到 `docs/system-map/` 目录

#### 输出文件

分析完成后，会在 `docs/system-map/` 目录下生成以下文档：

- `architecture.md` - 系统架构说明
- `modules.md` - 核心模块列表
- `api-map.md` - API 接口映射
- `database-er.md` - 数据库 ER 图
- `frontend-map.md` - 前端页面结构
- `call-chain.md` - 调用链分析

#### 使用方法

1. 在 Cursor 中打开项目
2. 要求cursor根据项目情况更新 `.cursor`中的`rules`和`skills`，以及`@analyze-system`
```
根据本目录下的项目情况，@proj1 @proj2 修正@.cursor/rules 中的规则和@.cursor/skills 中的技能。更新@.cursor/prompts/analyze-system.md
```
3. 要求cursor根据项目情况更新`.cursorignore`
```
生成符合本项目的 .cursorignore
```
4. 使用 `@analyze-system` 提示开始系统分析
```
执行 @.cursor/prompts/analyze-system.md 里定义的系统分析任务。
```
5. 查看生成的文档和图表

#### 架构规则

遵循标准的系统架构设计：

- 前端 → API → 服务层 → 数据库
- Controller 不直接操作数据库
- Service 层处理所有业务逻辑
- Mapper 仅负责数据访问

## 即将推出的技能套件

本目录将陆续添加更多 Cursor 技能套件，包括但不限于：

- 代码审查套件
- 测试生成套件
- 文档生成套件
- 性能优化套件

敬请期待！

## 贡献

欢迎提交 Issue 和 Pull Request 来改进和扩展这些技能套件。

## 许可证

[待定]
