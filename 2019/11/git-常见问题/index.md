# Git 常见问题


<!--more-->

#### <font color=#CC3300>1、git add 时提示 The file will have its original line endings in your working directory.</font>

```shell
git add -A
warning: LF will be replaced by CRLF in .gitmodules.
The file will have its original line endings in your working directory.
```

问题原因：由于linux使用的是(0x0A)LF,windows使用的是(0x0D0A)CRLF,而git 提供了autocrlf配置项，默认配置替换回车换行成统一的CRLF

解决办法: 根据需要更改此配置

```shell
# 提交时转换为LF，
git config --global core.autocrlf true

# 提交时转换为LF
git config --global core.autocrlf input

# 提交检出均不转换
git config --global core.autocrlf false
```

>如果把 autocrlf 设置为 false 时，那另一个配置项 `safecrlf` 最好设置为 **ture**。该选项用于检查文件是否包含混合换行符，其有三个可选项：
>
>- **true:** 拒绝提交包含混合换行符的文件
>- **false:** 允许提交包含混合换行符的文件
>- **warn:** 提交包含混合换行符的文件时给出警告



```shell
# 拒绝提交包含混合换行符的文件
git config --global core.safecrlf true

# 允许提交包含混合换行符的文件
git config --global core.safecrlf false

# 提交包含混合换行符的文件时给出警告
git config --global core.safecrlf warn
```

