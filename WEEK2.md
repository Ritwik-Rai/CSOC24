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

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/fac68a33-d0a3-40ae-9550-4cb7e503dfc4)
For converting back to bytes first all elements of 1st list are added(in order of appearance in array). then all elements of next list are added and so on.

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
Euler totient = (p-1)(q-1)  
p=857504083339712752489993810777  
q=1029224947942998075080348647219  

totient = 882564595536224140639625987657529300394956519977044270821168

#### RSA Starter 4
inverse(d) = e^(-1)(mod (euler totient))   
d=121832886702415731577073962957377780195510499965398469843281  

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/516066b4-4a3f-4767-9713-e0c33c7dc48d)

#### RSA Starter 5
cipher_text = m ^(e) (mod n)  
where : m is message  
        e is exponent  
        n is product of chosen 2 primes  
        on adjusting we get  
        c^(d)=(m^(e))^(d)(mod n) = m mod n  
        m = c^(d)(mod n)  
        d=121832886702415731577073962957377780195510499965398469843281  
n=882564595536224140639625987659416029426239230804614613279163     
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/d0b7d4e9-8b3a-4f30-a29b-4b52861e2946)
answer is 13371337

#### RSA Starter 6

First get the  hash  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/a2b8f539-c3dd-4027-9b53-9b066a595509)  

Getting long form for RSA operations
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/0be4247f-78b4-4dee-9a68-105a9377c692)

What we have got now is hash in long form.  
Hash is converted to sign via:  
Sign=(H(M))^(d1)mod(N1)  
where    : H(M) IS our hash  
           d1 is our private key.  
           N is product of chosen primes.  
N= 15216583654836731327639981224133918855895948374072384050848479908982286890731769486609085918857664046075375253168955058743185664390273058074450390236774324903305663479046566232967297765731625328029814055635316002591227570271271445226094919864475407884459980489638001092788574811554149774028950310695112688723853763743238753349782508121985338746755237819373178699343135091783992299561827389745132880022259873387524273298850340648779897909381979714026837172003953221052431217940632552930880000919436507245150726543040714721553361063311954285289857582079880295199632757829525723874753306371990452491305564061051059885803  

d1= 11175901210643014262548222473449533091378848269490518850474399681690547281665059317155831692300453197335735728459259392366823302405685389586883670043744683993709123180805154631088513521456979317628012721881537154107239389466063136007337120599915456659758559300673444689263854921332185562706707573660658164991098457874495054854491474065039621922972671588299315846306069845169959451250821044417886630346229021305410340100401530146135418806544340908355106582089082980533651095594192031411679866134256418292249592135441145384466261279428795408721990564658703903787956958168449841491667690491585550160457893350536334242689  

![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/f912319c-dfd8-4788-b328-d5e2f04ce092)

pow(H(M),d1,N)  
gives answer = 13480738404590090803339831649238454376183189744970683129909766078877706583282422686710545217275797376709672358894231550335007974983458408620258478729775647818876610072903021235573923300070103666940534047644900475773318682585772698155617451477448441198150710420818995347235921111812068656782998168064960965451719491072569057636701190429760047193261886092862024118487826452766513533860734724124228305158914225250488399673645732882077575252662461860972889771112594906884441454355959482925283992539925713424132009768721389828848907099772040836383856524605008942907083490383109757406940540866978237471686296661685839083475

### PUBLIC EXPONENT
#### 1) SALTY

The given file salty.py has e=1 and chooses a random d we dont know.  
For decryption of message length of message should be less than N(product of chosen primes).  
Hence for e=1 , message<N  
As a result in  
cipher_text = m ^(e) (mod n)  
where : m is message  
        e is exponent  
        n is product of chosen 2 primes   
c^(d)=(m^(e))^(d)(mod n) = m mod n    
Here e=1 hence d=1  
Our result is  cipher text = message  =44981230718212183604274785925793145442655465025264554046028251311164494127485.  
![image](https://github.com/Ritwik-Rai/CSOC24/assets/143336354/702195dd-163d-48a6-8883-4d325a700a19)


## OTHER CHALLENGES
### CHALLENGE 1



### CHALLENGE 2

01000011 01010011 01001111 01000011 00110010 33 7b 6a 75 35 37 5f ZDFmZjNyM243XzNuYw== 60 144 61 156 66 65 137 154 60 154 175

First 5 sets are in binary. They give ASCII codes which give us letters.  Gives "CSOC2"
The next 7 sets are hexadecimal. They also give ASCII codes that give letters.  Gives "2{ju57_"
The next set is base64 encoded. Gives "diff3r3n7_enc"
The leftover sets are octal and give "0d1n65_l0l}"  
Whole flag is "CSOC23{ju57_diff3r3n7_3nc0d1n65_l0l}  
No script was needed.























