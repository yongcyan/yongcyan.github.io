---
layout: post
title:  Bash Positional Parameters 相关
date:   2018-05-18 11:13:17 +0800
tags:   [Bash]
---


#### All Positional Parameters

`$*` 和 `$@` 用来表示所有的参数。当处于双引号之中时两者稍有区别：

 * The `$@` with double quoted expands to the equivalent of: "$1" "$2" "$3" "$4" ….. "$N".
```
> cat demo.sh
for i in "$@"; do
        echo $i;
done
> bash demo.sh 1 2 3 4 5
1
2
3
4
5
```

 * The `$*` with double quoted expands to the equivalent of: "$1c$2c$3c$4c……..$N", where c is the first character of IFS.
```
> cat demo.sh
for j in "$*"; do
        echo $j
done
> ./demo.sh 1 2 3 4 5
1 2 3 4 5
```


#### Range Of Positional Parameters

下面四种形式可以提取特定范围内的参数（等价的）：
```
${@:START:COUNT}
${*:START:COUNT}
"${@:START:COUNT}"
"${*:START:COUNT}"
```
 * 可以省略`COUNT` - all positional parameters beginning at `START` are expanded
```
> cat demo.sh
echo "${@:3}"
> bash demo.sh 1 2 3 4 5
3 4 5
```

 * 如果`START`是负数 - starts in reverse with the last one (leave space after the ":")
```
> cat demo.sh
echo "${@: -2}"
> bash demo.sh 1 2 3 4 5
4 5
```

 * 如果设定为0 - (since Bash 4) includes the special parameter $0.
```
> cat demo.sh
echo "${@:0}"
> bash demo.sh 1 2 3 4 5
demo.sh 1 2 3 4 5
> bash --version
GNU bash, version 4.3.42(1)-release (x86_64-redhat-linux-gnu)
...
```

## Reference
 * [Handling positional parameters (bash-hackers wiki)](http://wiki.bash-hackers.org/scripting/posparams)
