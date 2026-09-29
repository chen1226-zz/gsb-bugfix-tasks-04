# 11012 · 相对时间的空标签

本目录是开源项目 `dustin/go-humanize` 在该版本下的完整源代码副本（许可见同目录的 LICENSE 文件，
版权归原作者所有），并额外包含用于验收的测试用例。

## 运行与验收

```
go test ./...
```

当前 `go test ./...` **是失败的**，失败用例：`TestRelTimeEmptyLabel`

## 已知现象

在 ago 标签和 from-now 标签都为空字符串时，`RelTime` 的结果尾部会多出一个空格（返回 `"3 weeks "`），期望是 `"3 weeks"`。
