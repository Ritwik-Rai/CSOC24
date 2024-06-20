# WEEK2
## INTRODUCTION
#### 1) FINDING FLAGS
flag is :crypto{y0ur_f1rst_fl4g}  
no script needed

#### 2) Great Snakes
flag is :crypto{z3n_0f_pyth0n}  
Just have to download file and run it hence no script needed.  

import sys  
if sys.version_info.major == 2:  
print("You are running Python 2, which is no longer supported. Please update to Python 3.")

ords = [81, 64, 75, 66, 70, 93, 73, 72, 1, 92, 109, 2, 84, 109, 66, 75, 70, 90, 2, 92, 79]

print("Here is your flag:")
print("".join(chr(o ^ 0x32) for o in ords))

#### 3) Network Attacks
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/45885140-1b44-4a3d-a70b-2a33701f7bc8)
image shows script+flag.  

## GENERAL
### ENCODING

#### 1) ASCII
No script is needed can just convert ASCII to char by memory.  
flag is : crypto{ASCII_pr1nt4bl3}

#### 2) Hex
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/b8bf6df1-763b-465a-9824-54465d908357)
Has both script + flag.

#### 3) Base64
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/04d4852d-e153-4e17-9e14-fc248d6d98b5)
Has both script + flag.

#### 4) Bytes and Big Integers
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/b4dbaca6-c24d-464a-964e-ed527ce129d6)
Has both script + flag.

### XOR
####  1) XOR STARTER  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/c0f88938-56f1-46b9-91e4-ee20ba5a5122)
flag is : crypto{aloha}

#### 2) XOR Properties
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/80645d48-76d6-4ca1-9683-6b6111fe872c)

#### 3)Favourite byte
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/86f38e27-7f6f-4088-8186-e2ad159af74e)
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/d319652f-1987-4014-8da1-17a112ba7831)
flag is : crypto{0x10_15_my_f4v0ur173_by7e}  

#### 4)You either know , XOR you dont
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/6e9078d4-0585-4d86-b809-0643beb1a0b3)

### MATHEMATICS
#### 1) GREATEST COMMON DIVISOR
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/fc2683a4-7593-4895-8cd7-6c9319474d9d)
Its 1512

#### 2) Extended GCD
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/aa84e93f-2673-4244-90dd-6a12cc176cf3)
Its -8404.  
Just implement code of extended euclidean algorithm.  

#### 3) Modular Arithmetic 1
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/814ff797-eefe-40ad-a45e-24763f1df0e2)

#### 4) Modular Arithmetic 2
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/b6bc2feb-1954-4eb0-9d3b-828e467fbf02)  

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/99d59178-0983-4dde-ac80-c80dbc220ec3)  

We use 1st one here.                  (Here ^ is exponent)  

a^(p-1)=1modp  

273246787654^(65536) mod 65537=1

#### 5)Modular Inverting
3 = 3mod13  
As its of type a = bmodp  
where : a=b , p is prime  
a^(-1)=a^(-1)(modp)
Here we can use fermats little theorem as we know a^(p-1)=1modp  
so 3^(12) = 1mod13  

so a^(-1)=3^(11)mod13  
which is = 9
Hence our inverse is 9(mod13)

## SYMMETRIC CIPHERS
#### 1)Keyed Permutations
Bijective

#### 2)Resisting Bruteforce
Biclique attack

#### 3)Structure of AES














## RSA
### STARTER
#### RSA Starter 1
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/a875bdab-ad49-4ad3-a048-f0c5e6690dc3)  
Just use pow function.  
Answer is 19906.

#### RSA Starter 2
cipher_text = m ^(e) (mod n)  
where : m is message  
        e is exponent  
        n is product of chosen 2 primes 
12^(65537)mod 391 =  301
cipher text is 301. can be solved with power function.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/9f131756-7f74-4253-b5c8-b7024ae5ec91)

#### RSA Starter 3



































