# 11013 · 千分位格式化对 Inf/NaN 的处理

本目录是开源项目 `dustin/go-humanize` 在该版本下的完整源代码副本（许可见同目录的 LICENSE 文件，
版权归原作者所有），并额外包含用于验收的测试用例。

## 运行与验收

```
go test ./...
```

当前 `go test ./...` **是失败的**，失败用例：`TestCommafs`、`TestBigCommafs`

## 已知现象

`Commaf(math.Inf(1))` 输出 `+,Inf`、`Commaf(math.Inf(-1))` 输出 `-+,Inf`，期望分别是 `+Inf` 和 `-Inf`；`BigCommaf` 同样。
