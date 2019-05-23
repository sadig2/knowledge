## args  
import getopt

try:
    opts , args = getopt.getopt(sys.argv[1:],'s:f:')  

except:  
        print("no file assigned")  

for opt ,arg  in opts:  
    if opt in "-s":  
        soundfile = arg  
    elif opt in "-f":  
      filename = arg  
      
      
      