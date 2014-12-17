git 相关
======
### 1、配置文件
```
touch ~/.gitconfig
```
在.gitconfig内贴入[gitconfig](https://github.com/kingner/config/blob/master/gitconfig)内容，修改帐号信息


*****
### 2、HTTP协议免输用户名密码

```
touch ~/.netrc
echo 'machine Domain
login username 
password email@example.com' >> ~/.netrc
```

vim 相关
========
### 1、新建文件加入作者版本等信息
在.vimrc 中加入以下代码
```
autocmd BufNewFile *.php exec ":call SetTitle()"
    func SetTitle()
    call setline(1,"<?php") 
    call append(line("."),"/**") 
    call append(line(".")+1, "*   Copyright (C) kingner.domain ".strftime("%Y")." All rights reserved.")
    call append(line(".")+2, "*") 
    call append(line(".")+3, "*   FileName      ：".expand("%:t")) 
    call append(line(".")+4, "*   Author        ：kingner")
    call append(line(".")+5, "*   Email         ：kingner@email.com")
    call append(line(".")+6, "*   Date          ：".strftime("%Y/%m/%d %H:%m:%S")) 
    call append(line(".")+7, "*   Version       ：1.0") 
    call append(line(".")+8, "*   Description   ：") 
    call append(line(".")+9, "*/") 
    call append(line(".")+10, "") 
    endfunc

"自动将光标定位到末尾
autocmd BufNewFile * normal G
```
