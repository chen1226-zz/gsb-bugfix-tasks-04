# 11005 · 夏令时时区的日期边界

本目录是开源项目 `jinzhu/now` 在该版本下的完整源代码副本（许可见同目录的 LICENSE 文件，
版权归原作者所有），并额外包含用于验收的测试用例。

## 运行与验收

```
go test ./...
```

当前 `go test ./...` **是失败的**，失败用例：`TestBeginningOf`、`TestEndOf`、`TestMondayAndSunday`

## 已知现象

在启用夏令时的时区里，`BeginningOfDay`、`BeginningOfWeek`、`BeginningOfMonth`、`BeginningOfQuarter`、`BeginningOfYear` 算出来的边界时刻整体偏移一小时（返回 01:00 而不是 00:00），个别时区（如 Caracas）的年边界会落到上一年。
