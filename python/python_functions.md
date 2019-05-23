## python function optional argument 
def get_formatted_name(first_name, last_name, middle_name=' '):  
"""Return a full name, neatly formatted."""  <--- document commentary  
if middle_name:  
full_name = first_name + ' ' + middle_name + ' ' + last_name  
else:  
full_name = first_name + ' ' + last_name    
### Python interprets non-empty strings as True

## arbitrary number of arguments python function 
def make_pizza(*toppings):  
"""Print the list of toppings that have been requested."""  
print(toppings)  
## Using Arbitrary Keyword Arguments 
accepts any kind of information   
def build_profile(first, last, **user_info):  
profile = {}  
profile['first_name'] = first  
profile['last_name'] = last  
for key, value in user_info.items():  
profile[key] = value  
return profile  

##  math.ceil(x)
smallest integer number greater or equal to x

## int("".join(map(str,extracted[i:i+8])),2)  
2 - means it ll read first argument as bytes and convert into integer  
