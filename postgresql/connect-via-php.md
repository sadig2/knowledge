## <?php  

    require_once 'login.php';  
    $dbconnection = pg_connect("host=$db_hostname dbname=$db_database user=$db_username  
     password=$db_password")  
    or die("Unable to connect to Postgres");  
    
    
       $query = pg_query($dbconnection,"select * from classics");  
      
    
       $row = pg_fetch_row($query);  
    
       $size =  sizeof($row);  
    
    
       for ($i= 0; $i<$size;$i++){  
    
           echo  $row[$i] . '<br>';  
       }  
    
    pg_close($dbconnection);  
    
    
    ?>  

