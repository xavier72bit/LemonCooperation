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

# 项目启动

## odoo.conf例子

```
[options]
addons_path = addons,cust
; data_dir = /var/lib/odoo
admin_passwd = admin
db_host = localhost
init = base,base_sso
db_port = 5432
db_user = odoo
db_password = odoo123
db_name = odoo
limit_time_real = 2400
list_db = False
session_type = redis_session
session_age = 600
orm_redis_cache_age = 600
orm_redis_cache = True
make_migration = True
stop_after_init = False
redis_db_index = 6
redis_host = localhost
redis_port = 6379
csv_internal_sep = ,
db_maxconn = 64
db_maxconn_age = 300
workers = 4
threads = 4
limit_memory_hard = 0
; limit_memory_soft = 2147483648
; limit_request = 8192
; limit_time_cpu = 60
; debug_mode = False
; log_db = False
; log_handler = [':INFO']
log_level = info
; logfile = None
; longpolling_port = 8072
; max_cron_threads = 2
; osv_memory_age_limit = 1.0
; osv_memory_count_limit = False
; email_from = False
; smtp_password = False
; smtp_port = 25
; smtp_server = localhost
; smtp_ssl = False
; smtp_user = False

```

```shell
odoo-bin -c odoo.conf
```