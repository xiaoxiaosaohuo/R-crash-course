## List

列表是 R 语言的对象集合，可以用来保存不同类型的数据，可以是数字、字符串、向量、另一个列表、矩阵、数据框等，当然还可以包含矩阵和函数。

列表是一种灵活的数据结构，可以存储和操作多种类型的数据对象。

```
> list_data = list('runoob','google',c(1,2,3),123,TRUE)
> list_data
[[1]]
[1] "runoob"

[[2]]
[1] "google"

[[3]]
[1] 1 2 3

[[4]]
[1] 123

[[5]]
[1] TRUE

> 

```

example 2

```
# 创建一个列表
my_list <- list(name = "John", age = 30, scores = c(85, 92, 78))

# 访问列表元素
my_list$name     # "John"
my_list[[2]]     # 30 
my_list[["scores"]] # 85 92 78
```

### 访问列表

```
# 列表包含向量、矩阵、列表
list_data <- list(c("Google","Runoob","Taobao"), matrix(c(1,2,3,4,5,6), nrow = 2),
   list("runoob",12.3))

# 给列表元素设置名字
names(list_data) <- c("Sites", "Numbers", "Lists")

# 显示列表
print(list_data[1])

# 访问列表的第三个元素
print(list_data[3])

# 访问第一个向量元素
print(list_data$Numbers)
```

### 操作列表元素

```
# 列表包含向量、矩阵、列表
list_data <- list(c("Google","Runoob","Taobao"), matrix(c(1,2,3,4,5,6), nrow = 2),
   list("runoob",12.3))

# 给列表元素设置名字
names(list_data) <- c("Sites", "Numbers", "Lists")

# 添加元素
list_data[4] <- "新元素"
print(list_data[4])

# 删除元素
list_data[4] <- NULL

# 删除后输出为 NULL
print(list_data[4])

# 更新元素
list_data[3] <- "我替换来第三个元素"
print(list_data[3])
```

### 遍历列表
```
# 创建一个包含数字和字符的列表
my_list <- list(1, 2, 3, "a", "b", "c")

# 使用 for 循环遍历列表中的每个元素
for (element in my_list) {
  print(element)
}
```
## Matrix
矩阵里的元素可以是数字、符号或数学式。

一个 M x N 的矩阵是一个由 M（row） 行 和 N 列（column）元素排列成的矩形阵列。

```
matrix(data = NA, nrow = 1, ncol = 1, byrow = FALSE,dimnames = NULL)
```

## 创建Matrix
```
# byrow 为 TRUE 元素按行排列
M <- matrix(c(3:14), nrow = 4, byrow = TRUE)
print(M)

# Ebyrow 为 FALSE 元素按列排列
N <- matrix(c(3:14), nrow = 4, byrow = FALSE)
print(N)

# 定义行和列的名称
rownames = c("row1", "row2", "row3", "row4")
colnames = c("col1", "col2", "col3")

P <- matrix(c(3:14), nrow = 4, byrow = TRUE, dimnames = list(rownames, colnames))
print(P)
```

## 转置矩阵
R 语言矩阵提供了 t() 函数，可以实现矩阵的行列互换。

例如有个 m 行 n 列的矩阵，使用 t() 函数就能转换为 n 行 m 列的矩阵。

```
# 创建一个 2 行 3 列的矩阵
M = matrix( c(2,6,5,1,10,4), nrow = 2,ncol = 3,byrow = TRUE)
print(M)
     [,1] [,2] [,3]
[1,]    2    6    5
[2,]    1   10    4
# 转换为 3 行 2 列的矩阵
print(t(M))
```

## 矩阵计算

大小相同（行数列数都相同）的矩阵之间可以相互加减，具体是对每个位置上的元素做加减法。矩阵的乘法则较为复杂。两个矩阵可以相乘，当且仅当第一个矩阵的列数等于第二个矩阵的行数。

```
# 创建 2 行 3 列的矩阵
matrix1 <- matrix(c(7, 9, -1, 4, 2, 3), nrow = 2)
print(matrix1)

matrix2 <- matrix(c(6, 1, 0, 9, 3, 2), nrow = 2)
print(matrix2)

# 两个矩阵相加
result <- matrix1 + matrix2
cat("相加结果：","\n")
print(result)

# 两个矩阵相减
result <- matrix1 - matrix2
cat("相减结果：","\n")
print(result) 
```
## Array
R 语言数组是一个同一类型的集合,数组是一种多维的数据结构,可以看作是矩阵的扩展版本。数组中的元素必须是相同的数据类型,可以通过维度来访问。

```
# 创建一个3维数组
my_array <- array(1:24, dim = c(3, 4, 2))

# 访问数组元素
my_array[2, 3, 1]   # 15

# 数组的维度
dim(my_array)   # 3 4 2
```