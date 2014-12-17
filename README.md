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
