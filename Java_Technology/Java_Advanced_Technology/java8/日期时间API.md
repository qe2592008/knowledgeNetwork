# 日期时间API
## 综述
|序号|类|意义|用法|
|:---:|:---:|:---|:---|
|1|Instant|表示一个精确的时间点|Instant now = Instant.now();|
|2|Duration|表示两个时间点之间的时间量(天级以下)|Duration dura = Duration.between(now,now.plusSeconds(10));|
|3|Period|表示两个时间点之间的时间量(天级以上)|Period per = Period.between(nowDate,nowDate.plusDays(2));|
|4|LocalDate|表示日期|LocalDate nowDate = LocalDate.now();|
|5|LocalTime|表示时间|LocalTime nowTime = LocalTime.now();|
|6|LocalDateTime|表示日期和时间|LocalDateTime nowDateTime = LocalDateTime.now();|
|7|ZonedDateTime|表示带时区信息的日期和时间|ZonedDateTime zonedDateTime = ZonedDateTime.now();|
|8|DateTimeFormatter|提供格式化和解析功能||
## Instant
Instant表示一个时间瞬点，有两部分组成：
- 原点（格林威治标准时：1970-1-1 00:00:00）到指定时间点的秒数
- 距离该秒数的纳秒数
### Instant的使用
```java

```