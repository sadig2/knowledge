```html
## remove jquery style class  
$('#post23').toggleClass('read')  or  removeClass  
## parents , ancestors  
$('#elem').parents('div').css('background', 'yellow')    parentsuntil  
#child element jquery
li_children = $('#elem').children('li')   $('#elem').find('*')  
##siblings  
selects elements of the same parent except the very element intself  
$('#two').siblings().css('font-weight', 'bold')   in this case except two  
## select siblings until  element with id old    
 $('#new').nextUntil('#old').css('font-weight', 'bold') 
 ## traverse jquery  
 $('ul>li').filter(':even').css('background', 'cyan')  ul is a parent of li  
 ## exclude in traverse  
 $('ul>li').not('#new').css('color', 'blue')  
 ## elements that has descentant  ol  
 $('ul>li').has('ol').css('text-decoration', 'line-through')  
 ## is method  returns true or false not creating new jquery object  
 $(this).parent().is('div')  = boolean  
 
 #maps in jquery is to analize array  
 guineapigs = $.map(pets, function(type, name)  
 {  
 if (type == 'Guinea Pig') return name  
 })  
 
 pets is map  