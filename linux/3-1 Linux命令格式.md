# Linux命令格式

## 起始符
`[root@localhost ~]#`
- `root` 当前登录用户
- `localhost` 主机名
- `~` 当前所在目录（家目录）
- `/` 根目录
- `#` 超级用户的提示符
- `$` 普通用户的提示符

## ls命令选项
- `ls -a`  显示所有文件，包括隐藏文件
- `ls -l`  显示详细信息， 别名 `ll`
- `ls -lh` 显示详细信息 人性化显示文件大小
- `ls -ld`  查看目录属性
- `ls -i`  显示inode

## 文件权限

`-rw-r--r--`

*共10位，第一位为文件类型，后面每3位一组*
- `-` 文件类型（`-` 文件 `d` 目录 `l` 软链接目录）
- `rw-` u所有者
- `r--` g所属组
- `r--` o其他人
- `r ` 可读 `w` 可写 `x` 可执行

*在 linux 中 `.` 开头的文件是隐藏文件*

例 `drwxr-xr-x. 3 root root  4096 Oct 26  2016 home`
- `d` `home` 是个文件目录
- `rwx` 所有者 `root` 用户 可读可写可执行权限
- `r-x` 所属于 `root` 组的用户，有可读可写执行权限
- `r-x` 其他用户，有可读可写执行权限
- `.` 代表ACL权限 
- `3` 代表引用计数
- `4096` 文件大小单位字节
- `Oct 26  2016` 最后一次修改时间