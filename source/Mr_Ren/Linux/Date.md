# Linux Date时间

## 常规时间输出

```
# 查看日志为 2022-03-03-16:09:36 格式
$ date '+%Y-%m-%d-%H:%M:%S'  

# 查看明天日期
$ date -d next-day +%Y-%m-%d-%H:%M:%S
$ date -d tomorrow +%Y-%m-%d-%H:%M:%S

# 查看昨天日期
$ date -d last-day +%Y-%m-%d-%H:%M:%S
$ date -d yesterday +%Y-%m-%d-%H:%M:%S

# 查看上个月日期
$ date -d last-month +%Y-%m-%d-%H:%M:%S

# 查看下个月日期
$ date -d next-month +%Y-%m-%d-%H:%M:%S

# 查看明年日期
$ date -d next-year +%Y

# 获取昨天或多天前的日期
$ date -d 'n days ago' +%Y%m%d   //n换为数字,默认是昨天
```
