系统架构：
- 后端 API / 服务层
- 前端 Web
- 移动端 APP 或小程序
数据库类型：MySQL / PostgreSQL / MongoDB

开发原则：
- API 只能在 API 层定义
- 业务逻辑必须在服务层
- 前端 / 移动端只调用 API
- Controller 不包含业务逻辑
- Service 层处理所有业务逻辑
- Mapper 只负责数据库访问