# RSA公開金鑰[密碼學演算法]
```
Key Pairs Generation:產生金鑰對
使用公鑰加密
使用私鑰解密
```
## Key Pairs Generation:產生金鑰對
```
產生金鑰:
1. 先找兩個質數: p , q 
    計算 n = p * q 
    計算 φ(n) = (p - 1) * (q - 1) 

2.找出 e 滿足  gcd(e ,φ(n) ) = 1

3.算出 d 
  e* d mod φ(n) = 1
  d 是e 在模數 φ(n) 下的模反元素(module inverse)
```
```
加密: C(密文) = M(明文) ^ e mod n 
    
解密: M(明文) = C(密文) ^ d mod n 
```
# 範例
```
明文M = 2


產生金鑰:
1. 先找兩個質數: p = 3 , q = 11
    ==> n = p * q = 33
    ==> φ(n) = (p - 1) * (q - 1) = 2 * 10 = 20
    
2. 找到 e = 13滿足底下條件:
    gcd(13 , 20) = 1

3. 算出d = 17
       (13 * 17 )mod 20 = 1

加密: C = 2 ^ 13 mod 33 = 8
解密: M = 8 ^ 17 mod 33 = 2
```
# 作業
```
https://en.wikipedia.org/wiki/RSA_(cryptosystem)

p=61, q=53 
計算ＲＳＡ
```
