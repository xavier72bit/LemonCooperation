# LemonCooperation

* 为从事软件开发行业的公司提供“人力资源管理”，“交流”，“会议”，“知识库”，“进度追踪”等一站式服务
* 基于[Odoo-15](www.odoo.com)开发

# 环境

| 类型         | 版本  |
|:-----------|-----|
| Python     | 3.9 |
| PostgreSQL | 15  |
| Redis      | 7   |

# PostgreSQL

```sql
CREATE USER odoo WITH PASSWORD 'odoo123';
ALTER USER odoo CREATEDB;
```