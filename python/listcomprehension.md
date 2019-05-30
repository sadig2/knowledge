## list comprehension

    string = "sadig"  
    
    bits = list(map(int, ''.join([bin(ord(i)).lstrip('0b') for i in string])))
    print(bin(ord('s')))  
    for i in bits:  
        print(i)  
        
    map(int,any type)  -- converts to integers  
    bin file =    0b1110011   looks like this thus we lstrip   

## comprehension

    
    list_a = [1, 2, 3]
    list_b = [2, 7]
    
    different_num = [[a,b] for a in list_a for b in list_b if a != b]
    
    print(different_num) 
    
    first -  execution   
    second loop   
    third -  condition  
