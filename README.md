# GSB 修复类任务 · 初始环境仓库 04

本仓库用于给「修复类」标注任务提供**初始（带 bug 的）代码仓库**。

## 目录约定

一个仓库承载多个任务，**每个任务一个子目录**：

```
tasks/<UID>-<短名>/
```

`UID` 对应标注表里的任务编号，`短名` 是英文短标识。

**一个仓库最多放 10 个任务**，超出就另开新仓库（`gsb-bugfix-tasks-05` …）。

## 当前任务

| 子目录 | UID | 主题 |
| --- | --- | --- |
| `tasks/11004-uuid-v7-monotonic/` | 11004 | UUIDv7 毫秒内单调性 |
| `tasks/11005-time-dst-boundary/` | 11005 | 夏令时时区的日期边界 |
| `tasks/11006-time-regexp-parse/` | 11006 | 带时间部分的时间串解析 |
| `tasks/11007-time-parse-format/` | 11007 | 常见时间格式的解析 |
| `tasks/11008-pflag-uintslice-hex/` | 11008 | UintSlice 对十六进制输入的处理 |
| `tasks/11009-pflag-isbool-compat/` | 11009 | 自定义 IsBoolFlag 的兼容行为 |
| `tasks/11010-pflag-unknown-flags/` | 11010 | 忽略未知参数并回填 args |
| `tasks/11011-humanize-bytes/` | 11011 | 字节数格式化取整 |
| `tasks/11012-humanize-reltime/` | 11012 | 相对时间的空标签 |
| `tasks/11013-humanize-commaf-nan/` | 11013 | 千分位格式化对 Inf/NaN 的处理 |

## 代码来源与许可

各任务子目录中的源代码取自下列开源项目，均为宽松许可；每个子目录内保留了对应项目的
LICENSE 文件，版权归原作者所有。子目录在上游代码基础上只加入了用于验收的测试用例。

| 上游项目 | 许可 |
| --- | --- |
| `github.com/google/uuid` | BSD-3-Clause |
| `github.com/jinzhu/now` | MIT |
| `github.com/spf13/pflag` | BSD-3-Clause |
| `github.com/dustin/go-humanize` | MIT |
