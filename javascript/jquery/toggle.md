
## jquery toggle button

    <button id='toggle'>Toggle</button>  
    <p id='text'>Click the Toggle button</p>  
    <script>  
        \$('#toggle').click(function() { $('#text').toggle('slow', 'linear') })  
    </script>




### set attributes jquary  
    <p><a id='link' href='http://google.com' title='Google'>Visit Google</a></p>  
    
    $('#link').attr( { href :'http://yahoo.com', title:'Yahoo!' } ) 


## jquery append, prepend, remove ,empty  

    <a href='http://google.com' title='Google'>Visit Google\</a>    
    <code>   
        This is a code section   
    </code>  
    <p>  
        <button id='a'>Remove the image\</button>  
        <button id='b'>Empty the quote\</button>  
    </p>  
     <img id='ball' src='ball.png'>  
      <blockquote id='quote' style='border:1px dotted #444; height:20px;'>  
        test  
    </blockquote>  
    <script>  
        $('a').prepend('Link: ')  
        $("[href^='http']").append(" <img src='ball.png'>")  
        $('code').before('<hr>').after('<hr>')  
        $('#a').click(function() { $('#ball').remove() } )  
        $('#b').click(function() { $('#quote').empty() } )<h2>Example Document</h2>]  
        