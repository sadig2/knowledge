## reading from file
class Readerr():  
    def read(self,name):  
        self.name = name  
        with open(name) as xerna:  
            temp = xerna.read()  
            print(temp.rstrip())  
R1 = Readerr()  
R1.read('info.txt')   

for line in xerna:  
  print(line.rstrip)    --  because in file \n newline is added unduely    

**with** - The keyword with closes the file once access to it is no longer needed.  

## combine lines in one string
with open('info.txt') as xx:  
    list1 = xx.readlines()  
sum1 = ''  
for x in list1:  
    sum1 += x  

check = input("enter here  ")  
if check in sum1:  
    print("it is inside")  


## write to file

filename = 'programming.txt'  
with open(filename, 'w') as file_object:  
   file_object.write("I love programming.")  

## append to a file
with open(filename, 'a') as file_object:  


   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   

