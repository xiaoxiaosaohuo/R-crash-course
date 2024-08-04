## CSV

```
data <- read.csv("sites.csv", encoding="UTF-8")
print(data)
print(is.data.frame(data))  # 查看是否是数据框
print(ncol(data))  # 列数
print(nrow(data))  # 行数
```

## 保存

```
data <- read.csv("sites.csv", encoding="UTF-8")

# likes 为 222 的数据
retval <- subset(data, likes == 222)

# 写入新的文件
write.csv(retval,"runoob.csv")
newdata <- read.csv("runoob.csv")
print(newdata)
```