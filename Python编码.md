# Python编码

```
import base64
import binascii


s1 = 'A'
s2 = '中'

# encode()，将字符串转为bytes类型（二进制）
print(s1.encode())
print(s2.encode())

print('*'*100)

# decode()，将bytes类型（二进制）转为字符串
print(b'A'.decode())
print(b'\xe4\xb8\xad'.decode())

print('*'*100)

# ord()，返回一个字符的unicode编码，包括中文和英文
print(ord(s1))
print(ord(s2))

print('*'*100)

# chr(), 根据一个unicode编码，返回这个这个字符
print(chr(65))
print(chr(20013))

print('*'*100)

# base64.encodebytes(), 将一个bytes类型（二进制）转换为一个base64的bytes,
# Encode a bytestring into a bytes object containing multiple lines of base-64 data
print(base64.encodebytes(s1.encode()))
print(base64.encodebytes(s2.encode()))

print('*'*100)

# base64.decodebytes()，功能正好相反
print(base64.decodebytes(b'QQ==\n'))
print(base64.decodebytes(b'5Lit\n'))

print('*'*100)

# binascii.b2a_hex()，返回一个字节类型（二进制）的十六进制bytes串
# 原来二进制的每个字节用相应的2位十六进制表示
# Every byte of data is converted into the corresponding 2-digit hex representation.
# The returned bytes object is therefore twice as long as the length of data.
print(binascii.b2a_hex(s1.encode()))
print(binascii.b2a_hex(s2.encode()))
print(len(s1.encode()))
print(len(binascii.b2a_hex(s1.encode())))
print(len(s2.encode()))
print(len(binascii.b2a_hex(s2.encode())))

print('*'*100)

# binascii.a2b_hex() 功能相反
print(binascii.a2b_hex(b'41'))
print(binascii.a2b_hex(b'e4b8ad'))
```

![](https://github.com/yabolu/Python-coding-issues/blob/main/images/%E8%BF%90%E8%A1%8C%E7%BB%93%E6%9E%9C.jpg)
