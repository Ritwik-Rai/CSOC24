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
