# 11010 · 忽略未知参数并回填 args

本目录是开源项目 `spf13/pflag` 在该版本下的完整源代码副本（许可见同目录的 LICENSE 文件，
版权归原作者所有），并额外包含用于验收的测试用例。

## 运行与验收

```
go test ./...
```

当前 `go test ./...` **是失败的**，失败用例：`TestIgnoreUnknownFlagsAndPassToArgsBackwardsCompat`

## 已知现象

打开「忽略未知参数」的兼容开关后，解析含未知选项的命令行仍然直接报错（`unknown shorthand flag`），而且解析完没有把未识别的参数回填到 `Args()`。
