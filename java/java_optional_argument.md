## java optional parameter or argument
    void foo(String a, Integer... b) {  
        Integer b1 = b.length > 0 ? b[0] : 0;  
        Integer b2 = b.length > 1 ? b[1] : 0;  
        //...  
    }  
    foo("a");  
    foo("a", 1, 2);  