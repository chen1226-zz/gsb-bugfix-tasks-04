# 11009 · 自定义 IsBoolFlag 的兼容行为

本目录是开源项目 `spf13/pflag` 在该版本下的完整源代码副本（许可见同目录的 LICENSE 文件，
版权归原作者所有），并额外包含用于验收的测试用例。

## 运行与验收

```
go test ./...
```

当前 `go test ./...` **是失败的**，失败用例：`TestCustomIsBoolFlagGetsNoOptDefaultAutomatically`、`TestCustomIsBoolFlagShortFormGetsNoOptDefaultAutomatically`、`TestPrintDefaultsCustomIsBoolFlagOmitsDefault`

## 已知现象

自定义实现 `IsBoolFlag()` 的取值类型没有按布尔标志处理：使用该标志时必须显式给参数（报 `flag needs an argument`），短选项同样如此，而且 usage 里该标志的默认值没有被省略。
