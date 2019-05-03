
<script>
   numbers = [7, 23, 6, 74]
   numbers.sort(function(a,b){return a - b})
   document.write(numbers + "<br>")
</script>



<script>
   words = fixNames("the", "DALLAS", "CowBoys")
       document.write(words[1] + "<br>")


   function fixNames()
   {
       var s = new Array()
       for (j = 0 ; j < fixNames.arguments.length ; ++j)
           s[j] = fixNames.arguments[j].charAt(0).toUpperCase() + fixNames.arguments[j].substr(1).toLowerCase()

       return s
   }
</script>


