## JS-Loop di immagini che segue il mouse

```
jQuery(document).ready(function( $ ){
    $(document).mousemove(function(e){
    $("#image").css({left:e.pageX, top:e.pageY});
});
});
```

---

## HTML+JS-Mostrare la risoluzione (larghezza e altezza) dello schermo

```
<!--questo è l'HTML-->
<div id="screen"></div>
```
```
//e questo è il JS
jQuery(document).ready(function( $ ){
	var width = $(window).width();
	var height = $(window).height();
   $("#screen").text(width + "x" + height);
});
```

---

## JS-Scroll orizzontale col mouse
```
jQuery(document).ready(function( $ ){
    $.fn.hScroll = function (amount) {
        amount = amount || 120;
        $(this).bind("DOMMouseScroll mousewheel", function (event) {
            var oEvent = event.originalEvent,
                direction = oEvent.detail ? oEvent.detail * -amount : oEvent.wheelDelta,
                position = $(this).scrollLeft();
            position += direction > 0 ? -amount : amount;
            $(this).scrollLeft(position);
            event.preventDefault();
        })
    };
    //nella riga successiva sostituire ".scroll" col nome della classe del vostro contenitore che scrolla
	$('.scroll').hScroll(70); // qui si può modificare "70" con un numero a piacere che rappresenta quanti px vengono scrollati
});
```

---

## JS-Hover su testo mostra altri testi e immagini in blur
```
jQuery(document).ready(function( $ ){
    $(".titolo01").hover(function(){
  		$(".img01").show();
		$(".show01").show();
	},function(){
    $('.img01').hide();
	$(".show01").hide();
});
	
	    $(".titolo02").hover(function(){
  		$(".img02").show();
		$(".show02").show();
	},function(){
    $('.img02').hide();
	$(".show02").hide();
});
});
```




