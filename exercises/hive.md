# Hive


### Creating Hive tables from web logs using RegexSerDe
```
CREATE EXTERNAL TABLE apache_log (
    ip string,
    auth_unused string,
    auth_user string,
    request_time string,
    request string,
    status_code int
)
ROW FORMAT
SERDE 'org.apache.hadoop.hive.serde2.RegexSerDe'
WITH SERDEPROPERTIES (
    "input.regex" = '^(\\S*) (\\S*)(\\S*) \\[([^\\]]*)\\] "([^"]*)" (\\S*) .*$'
)
LOCATION '/home/jovyan/sandbox/data/apache.access.log';
```