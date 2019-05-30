## to create object from class in python
    class Car():  
    def __init__(self, make, model, year):  
    """Initialize attributes to describe a car."""  
    self.make = make  
    self.model = model  
    self.year = year  
    self.odometer_reading = 0  
    def get_descriptive_name(self):  
       
    def read_odometer(self):  
    """Print a statement showing the car's mileage."""  
    print("This car has " + str(self.odometer_reading) + " miles on it.")  
    
    my_new_car = Car('audi', 'a4', 2016)  
    print(my_new_car.get_descriptive_name())  
    my_new_car.read_odometer()  
 
## Setting a Default Value for an Attribute
     self.odometer_reading = 0 


## inheritance python
    class Car():  
        def __init__(self,door):  
            self.d = door  
    class Ecar(Car):  
        def __init__(self,door,battery):  
            super().__init__(door)  
            self.bat = battery  
    inst = Ecar(40,2)   
    print(inst.d)    
 
