# Anaconda常用命令




#### <font color=#CC3300>查看虚拟环境</font>

```powershell
##创建虚拟环境
conda create -n env-name python=X.X

##切换虚拟环境
conda activate env-name

##关闭虚拟环境
deactivate

##删除虚拟环境
conda remove -n env-name --all

##查看存在的虚拟环境
conda env list
```

#### <font color=#CC3300>包管理</font>



```powershell
##查看安装了那些包
conda list

## 在虚拟环境中安装额外的包
conda install -n env-name [package]
```

