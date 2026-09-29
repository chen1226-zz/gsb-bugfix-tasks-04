# 11008 · UintSlice 对十六进制输入的处理

本目录是开源项目 `spf13/pflag` 在该版本下的完整源代码副本（许可见同目录的 LICENSE 文件，
版权归原作者所有），并额外包含用于验收的测试用例。

## 运行与验收

```
go test ./...
```

当前 `go test ./...` **是失败的**，失败用例：`TestUISHex`

## 已知现象

`--uis=0x1,0x2,0x10` 这种十六进制写法会被拒绝，报 `invalid argument ... strconv.ParseUint: parsing "0x1": invalid syntax`；十进制写法正常。
