## 查看 R 包的安装目录

```
> .libPaths()
[1] "/Library/Frameworks/R.framework/Versions/4.0/Resources/library"
>
```

## 查看已安装的包
```
library()
```

## 查看已载入的包

```
> search()
 [1] ".GlobalEnv"        "tools:RGUI"        "package:stats"    
 [4] "package:graphics"  "package:grDevices" "package:utils"    
 [7] "package:datasets"  "package:methods"   "Autoloads"        
[10] "package:base" 
```

## 安装新包

```
install.packages("要安装的包名")
```
国内一般建议大家使用国内镜像，以下实例使用中国科学技术大学源进行安装：
```
# 安装 XML 包
install.packages("XML", repos = "https://mirrors.ustc.edu.cn/CRAN/")
```

## 使用包
新安装的包需要先载入 R 编译环境中才可以使用
```
library("包名")
```
