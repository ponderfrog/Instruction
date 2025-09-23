# 指定编码
`# -*- coding: utf-8 -*-`

# 字符串
str以Unicode编码
```
# 单字符的编号
ord('A')

# 编码对应的字符
chr(66)

# str编码为bytes
# 无法编码为ascii的字节在bytes中用\x##表示
'abc'.encode('ascii')

# 把bytes解码为str
# 设置error忽略错误无效的字节
b'abc'.decode('ascii', errors='ignore')
```

# 函数

```
def func(a, b, c):
    
    # 检查参数的类型
    if not isinstance(a, (int, float)):
        raise TypeError('bad type')

    return 10*a, 10*b
```
