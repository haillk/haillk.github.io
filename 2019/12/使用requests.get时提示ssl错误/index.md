# 使用requests


<!--more-->

## Can't connect to HTTPS URL because the SSL module is not available.在anaconda环境中使用requests.get()时提示的错误

解决方法：将正在使用的环境中的此目录下的libcrypto\*.\*  和libssl\*.\* 四个文件复制到该环境中的根目录下去。

from

```
D:\soft\Anaconda\envs\hk-learn\Library\bin
```

to

```
D:\soft\Anaconda\envs\hk-learn\
```

hk-learn是我的环境名。