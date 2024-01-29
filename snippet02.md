## CSS-Per modificare il cursore in tutta la pagina

```
jQuery(document).ready(function( $ ){
    $(document).mousemove(function(e){
    $("#image").css({left:e.pageX, top:e.pageY});
});
});
```
