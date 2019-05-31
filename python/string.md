## substring 
    >>> S = 'abcdefghijklmnop'
    >>> S[1:10:2]
    'bdfhj'
## why i need slicing 
    # File echo.py
    import sys
    print(sys.argv)
    % python echo.py −a −b −c
    ['echo.py', '−a', '−b', '−c']
# Convert binary to integer: built-in
    >>> int('1101', 2)
    13
# Convert integer to binary: built-in
    >>> bin(13)
    '0b1101'
## formatting expressions basics 
    >>> '%d %s %g you' % (1, 'spam', 4.0)
    '1 spam 4 you' 
## padding   before 'd' put positive number to pad after and negative  (-10) to pad after
       x = 1234
       res = '%100d + %d'%(x,x)
       print(res)      
## dictionary based formatting
     >>> '%(qty)d more %(food)s' % {'qty': 1, 'food': 'spam'}
       '1 more spam'

## formatting method basics
       >>> template = '{motto}, {0} and {food}'
       >>> template.format('ham', motto='spam', food='eggs')
       'spam, ham and eggs'

## with expressions 
    >>> template = '%(motto)s, %(pork)s and %(food)s'
    >>> template % dict(motto='spam', pork='ham', food='eggs')
    'spam, ham and eggs'
## advanced formatting methods
       >>> '{0:10} = {1:10}'.format('spam', 123.4567)
       'spam = 123.4567'
       import sys
       x ='{0.platform:>10} = {1[kind]:<10}'.format(sys, dict(kind='laptop'))
       
        
        >>> '{0:e}, {1:.3e}, {2:g}'.format(3.14159, 3.14159, 3.14159)
        '3.141590e+00, 3.142e+00, 3.14159'
        >>> '{0:f}, {1:.2f}, {2:06.2f}'.format(3.14159, 3.14159, 3.14159)
        '3.141590, 3.14, 003.14'
        
# Hex, octal, binary 
 
    >>> '{0:X}, {1:o}, {2:b}'.format(255, 255, 255)
    'FF, 377, 11111111' 

# to from binary
    >>> bin(255), int('11111111', 2), 0b11111111
    ('0b11111111', 255, 255)
# to from octal 
    >>> oct(255), int('377', 8), 0o377
    ('0o377', 255, 255)
## to hex , from hex 
     >>> hex(255), int('FF', 16), 0xFF
     ('0xff', 255, 255)

## franction formatting   10  -is * and  how many digits to show   1/3 is f
    c ='%.*f' % (10, 1 / 3.0)
    print(c)        
## special formatting 
    >>> 'My {1[kind]:<8} runs {0.platform:>8}'.format(sys, {'kind': 'laptop'})
    my laptop runs linux
## relative assign 
    >>> '{:,d} {:,d}'.format(9999999, 8888888)
    '9,999,999 8,888,888'                                         