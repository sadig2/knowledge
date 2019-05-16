## write into json
import json  
numbers = [2, 3, 5, 7, 11, 13]  
filename = 'numbers.json'  
with open(filename, 'w') as f_obj:  
    json.dump(numbers, f_obj)    

## read from json 
import json  
    filename = 'numbers.json'  
    with open(filename) as f_obj:  
     numbers = json.load(f_obj)  
    print(numbers)
    
## refactored json

import json  
def get_stored_username():

      filename = 'username.json'
                try:
                    with open(filename) as f_obj:
                        username = json.load(f_obj)
                except FileNotFoundError:
                    return None
                else:
                    return username  


def greet_user():

    username = get_stored_username()

    if username:
        print("Welcome back, " + username + "!")
    else:
        username = input("What is your name? ")
        filename = 'username.json'
        with open(filename, 'w') as f_obj:
        json.dump(username, f_obj)
        print("We'll remember you when you come back, " + username + "!")

greet_user()    
    
    
    
    
    