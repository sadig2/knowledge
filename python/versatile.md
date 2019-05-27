## make .py script runnable as well as a module to be included add following line 

    if __name__ == "__main__":
        import sys
        fib(int(sys.argv[1]))
        
## to make python to treat a directory like a package add file ot it's root
    __init__.py         
    
## calling modules from package 
     __all__ = ["echo", "surround", "reverse"]
is not defined in __init__.py file you can not reach modules with  
    
        from sound.effects import *    
    