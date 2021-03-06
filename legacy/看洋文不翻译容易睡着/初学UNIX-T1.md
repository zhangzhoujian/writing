#####1.1 列印文件和目录
ls（list）
一开始登录的时候，你的工作目录就是你的用户目录。用户目录的名字和你的用户名是一样的，比如ee91ab之类的，在这个目录下会保存你的私人文件和子目录。
看看目录下有什么，就可以键入
`%ls (short for list)`
ls命令会列印出你工作目录里的内容。
如果在目录下什么都没有的话，那么就会返回提示符，有些情况下，在系统管理员创建用户的时候就会在用户目录下创建一些文件。
ls实际上不会列印目录下的所有文件，有一些文件，是以点开头（.）,也就是隐藏文件，他们一般是保存重要的程序配置信息的。不是非常熟悉UNIX的话最好不要更改配置文件。
如果要列印包含隐藏文件在内的所有内容，输入：
`%ls -a`
ls是一个可以接受选项的命令：-a就是一个选项。选项的作用就是改变命令的功能表现。在线手册会告诉你命令会有什么选项以及如何改变命令的功能。（稍后表述）。

#####1.2 创建目录
mkdir （make directory）
在用户目录下创建子目录，输入代码创建一个叫做unixstuff的子目录。
`% mkdir unixstuff`
之后可以看看刚刚创建的目录
`%ls`

#####1.3 切换目录
cd （change directory）
命令cd的作用是切换工作目录到制定的目录去，当前工作目录的意思就是现在所处的目录。
`% cd unixstuff`
之后输入ls来查看内容（应该是空的）。
习题 1a
在目录unixstuff中创建一个叫做backups的目录

#####1.4 两个特别的目录 . 和 ..
仍然是在unixstuff目录中，输入
`% ls -a`
会看见在unixstuff的目录下（其他所有的目录也是），有两个特别的目录（.）和（..）。所以输入
`% cd .`
的意思就是切换到当前目录，注意cd和.之间有一个空格。
（..）的意思是当前目录的父目录，上层目录，输入
`% cd ..`
会切换到上层目录。
注意：没有参数的cd会切换柜用户目录，这个功能是非常有用的。

#####1.5 路径名
pwd （print working directory）
路径名可以让你操作整个文件系统。例如，找出用户目录的据对路径。
`% pwd`
全路径看起来是这样子
`/a/fservb/fservb/fservb22/eebeng99/ee91ab`
意思是你的用户目录（ee91ab）是出于你的组目录（eebeng99）之中，存储在文件服务器fservb上。
注意：
`/a/fservb/fservb/fservb22/eebeng99/ee91ab`
也可以缩短成
`/user/eebeng99/ee91ab`

习题 1b
使用命令ls，pwd，还有cd浏览文件系统。

#####1.6 关于用户目录和路径名的一些信息
理解路径名
首先切回用户目录，之后输入
`% ls unixstuff`
就会列印出unixstuff目录中的内容。
`% ls backups`
会报出这样的信息
`backups: No such file or directory`
原因是backups不在你的用户目录中。必须是在正确的目录下或者使用绝对路径名才可以列出内容
`% ls unixstuff/backups`

~（用户目录）
用户目录本身也可以使用波浪号~来指代。这个功能可以用在指代用户目录开始的路径，
`% ls ~/unixstuff`
这样就可以列印出内容了，无论是不是在用户目录下都可以。

#####小结
命令|功能
---|---
ls|列印文件和目录
ls -a|列印所有的文件和目录
mkdir|创建一个目录
cd 目录名|切换到制定目录
cd|切换到用户目录
cd ~|切换到用户目录
cd ..|切换到上层目录
pwd|显示当前工作目录
