 ## 
     
     <?php
    
    require_once 'login.php';
    
    $connectic =  pg_connect("host=$db_hostname dbname=$db_database user=$db_username password=$db_password ");
    
    if (isset($_POST['author'])){  
       echo "author is sent\n";  
    
       $name = get_p('author');  
       $book = get_p('title');  
       $genre = get_p('category');  
       $year = get_p('year');  
    
       $query = "insert into classics values ('$name','$book','$genre','$year')";  
    
       pg_query($connectic,$query);  
    
       echo $book ;  
    
    }
    
    function get_p($d){   
       return pg_escape_string($_POST[$d]);  
    }  
    
    
    
    echo <<<_END  
    <form action="postingg.php" method="post"><pre>  
    Author <input type="text" name="author">  
    Title <input type="text" name="title">  
    Category <input type="text" name="category">  
    Year <input type="text" name="year">  
    <input type="submit" value="ADD RECORD">  
    </pre></form>  
    _END;  
    
    
    
    ?>

