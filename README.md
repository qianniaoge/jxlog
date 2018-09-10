# jxlog
jxlog是基于kafka+streamsets+clickhouse+redash构建的用于查询、分析、可视化jxwaf日志的系统。

#功能
- 提供HTTP接口对jxwaf日志进行查询、分析
- 基于SQL的查询语言，大部分与SQL标准相同
- 使用redash构建仪表板及数据可视化

# 安装
docker-compose -f docker-compose.yml run --rm server create_db 

sh ./click_cretables.sh

# 日志说明
字段名 | 字符类型 | 描述 
---|--- |--- 
rule_id |字符串 | 规则ID
rule_var| 字符串| 规则匹配参数类型
rule_transform |数组| 规则参数处理函数
rule_operator| 字符串| 规则操作函数
rule_category| 字符串| 规则种类
rule_action| 字符串| 规则匹配处理方法
http_request_host| 字符串 |服务端IP
http_request_time| 字符串| 请求处理的时间
rule_remote_ip| 字符串 |客户端IP
rule_uri| 字符串 |请求URL
rule_detail| 字符串| 规则详情
rule_serverity| 字符串| 规则危害程度
rule_negated| 字符串| 规则结果是否取反
rule_match_key| 字符串 |请求匹配参数名
rule_match_var| 字符串 |请求匹配参数值
rule_match_captures| 字符串 |请求匹配正则值

#待更新。。。。