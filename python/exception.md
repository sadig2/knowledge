## exceptions
    while True:  
    first_number = input("\nFirst number: ")  
    if first_number == 'q':  
    break  
    second_number = input("Second number: ")  
    try:  
    answer = int(first_number) / int(second_number)  
    except ZeroDivisionError:  
    print("You can't divide by 0!")  
    else:  
    print(answer)  

## Filenotfound exception
    try:  
    with open(filename) as f_obj:  
    contents = f_obj.read()    
    except FileNotFoundError:  
    msg = "Sorry, the file " + filename + " does not exist."  
    print(msg)  

## Failing silently  - do nothing finding exception  
    def count_words(filename):    
    try:  
    except FileNotFoundError:  
    **pass**  
    else:  
    --snip--