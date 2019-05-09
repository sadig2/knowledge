## python function optional argument 
def get_formatted_name(first_name, last_name, middle_name=' '):  
"""Return a full name, neatly formatted."""  <--- document commentary  
if middle_name:  
full_name = first_name + ' ' + middle_name + ' ' + last_name  
else:  
full_name = first_name + ' ' + last_name    
### Python interprets non-empty strings as True