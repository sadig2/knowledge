## pack into bites 
from struct import *


fmt = "2h"   h- means short , it can be i - integer  2 is how many shorts

packed = pack("2h",4556,45)

print(packed)


## conver bytes to string 

bytes = [112, 52, 52]
"".join(map(chr, bytes))

## bitwise and & extracts numbers from bytes  : bitwise or |  inserts new value  

1011 & 1  ->  1    i extracted first numbers last value  
(1011 & 100) |  10  ->  1010    i inserted new value   

## int to bytes

(1024).to_bytes(2, byteorder='big')  
b'\x04\x00'  