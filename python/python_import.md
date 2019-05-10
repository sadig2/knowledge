## import specific funciton 
from module_name import function_name
## Using as to Give a Function an Alias
from pizza import make_pizza as mp  
## Using as to Give a Module an Alias
import pizza as p
p.make_pizza(16, 'pepperoni')
## Importing All Functions in a Module
from pizza import *
make_pizza(16, 'pepperoni')    