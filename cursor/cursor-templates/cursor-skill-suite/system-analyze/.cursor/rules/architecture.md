系统架构：
前端 → API → 服务层 → 数据库

规则：
- Controller 不直接操作数据库
- Service 层处理所有业务逻辑
- Mapper 仅负责数据访问