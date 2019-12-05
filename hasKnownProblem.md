## 1. Failed to connect to github.com port 443: Timed out
```git
#问题：Failed to connect to github.com port 443: Timed out
harveyhwliu@harveyhwliu-PC0 MINGW64 /i/codeRepo/Machine_Learning_Repository (master)
$ git pull origin master
fatal: unable to access 'https://github.com/harveyhwliu/Machine_Learning_Repository/': Failed to connect to github.com port 443: Timed out

#解决方案：设置http访问代理
harveyhwliu@harveyhwliu-PC0 MINGW64 /i/codeRepo/Machine_Learning_Repository (master)
$ git config --global http.proxy web-proxy.tencent.com:8080

#验证：
harveyhwliu@harveyhwliu-PC0 MINGW64 /i/codeRepo/Machine_Learning_Repository (master|MERGING)
$ git config --get http.proxy
web-proxy.tencent.com:8080

#业务再次访问，正常

```
