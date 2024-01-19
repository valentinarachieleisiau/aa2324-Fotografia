## CSS-Per modificare il cursore in tutta la pagina
`body {`  
      `cursor: url('https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/donut.png'), auto;`  
`}`  

`/*tutti i link del sito*/`
`a {`  
      `cursor: url('https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/donut.png'), auto;`  
`}` 

`/*tutte le immagini del sito*/`
`img {`  
      `cursor: url('https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/donut.png'), auto;`  
`}` 

`/*aggiungendo :active all'elemento su cui si vuole che cambi il cursore, il cursore cambierà solo quando si fa click*/` 
`figure.immaginecursore:active {`
	`cursor: url('https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/donut.png'), auto;`
`}`

---
## CSS-Per modificare il cursore quando si è su un elemento preciso
`/*modificare ".et_pb_image_wrap" col nome dell'elemento desiderato*/`  
`.et_pb_image_wrap {`  
      `cursor: url('https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/donut.png'), auto;`  
`}`  

---
## CSS-Per nascondere il cursore quando si è su un elemento preciso
`/*modificare ".et_pb_image_wrap" col nome dell'elemento desiderato*/`  
`.et_pb_image_wrap {`  
      `cursor:none;`  
`}`  

---
## JS-Slider con cursore che diventa freccetta sx e dx
`jQuery(document).ready(function($) {`  
`//dappertutto modificare ".wpsisac-slick-slider-wrp" col nome del contenitore dello slider`  
   `$slideshow = $('.wpsisac-slick-slider-wrp');`  
  `$('.wpsisac-slick-slider-wrp').click(function(e) {`  
       `var pWidth = $(this).innerWidth();`  
       `var pOffset = $(this).offset();`  
       `var x = e.pageX - pOffset.left;`  
   
      `if(pWidth/2 > x) {`  
        `$slideshow.slick('slickNext');`  
      `} else if(pWidth/2 < x) {`  
        `$slideshow.slick('slickPrev');`  
      `}`  
  `});`  
   
    `$('.wpsisac-slick-slider-wrp').click(function(e) {`  
       `var pWidth = $(this).innerWidth();`  
       `var pOffset = $(this).offset();`  
       `var x = e.pageX - pOffset.left;`  
   
      `if(pWidth/2 > x) {`  
        `$slideshow.slick('slickNext');`  
      `} else if(pWidth/2 < x) {`  
        `$slideshow.slick('slickPrev');`  
      `}`  
  `});`  
   
  `$('.wpsisac-slick-slider-wrp').on('mousemove', function(e){`  
       `var pWidth = $(this).innerWidth();`  
       `var pOffset = $(this).offset();`  
       `var x = e.pageX - pOffset.left;`  
   
      `if(pWidth/2 > x) {`  
        `$('.slick-slide').css('cursor','url([https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/left.png](https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/left.png)), pointer');`  
      `} else if(pWidth/2 < x) {`  
        `$('.slick-slide').css('cursor','url([https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/right.png](https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/right.png)), pointer');`  
      `}`  
  `});`  
  `});`  

---
## CSS-Slider con cursore che diventa freccetta sx e dx
`/*Non dovrebbe essere necessario modificare i selettori...*/`  
`.wpsisac-slick-slider.design-1 .slick-prev, .wpsisac-slick-slider.design-1 .slick-next {`  
    `width: 50%;`  
    `background-color: transparent;`  
    `top: 0 !important;`  
    `height: 100%;`  
`}`  
`.wpsisac-slick-slider.design-1 .slick-prev svg, .wpsisac-slick-slider.design-1 .slick-next svg {`  
    `display: none;`  
`}`  
`.wpsisac-slick-slider.design-1 .slick-prev {`  
  `cursor: url("https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/left-e1705220241430.png'), move;`  
`}`  
`.wpsisac-slick-slider.design-1 .slick-next {`  
  `cursor: url("https://valentinarachiele.altervista.org/wp-content/uploads/2024/01/right-e1705220225464.png'), move;`  
`}`  

---
## CSS-Marquee
`.marquee {`  
  `--gap: 1rem;`  
  `position: relative;`  
  `display: flex;`  
  `overflow: hidden;`  
  `user-select: none;`  
  `gap: var(--gap);`  
`}`  
`.marquee__content {`  
  `flex-shrink: 0;`  
  `display: flex;`  
  `justify-content: space-around;`  
  `gap: var(--gap);`  
  `min-width: 100%;`  
  `animation: scroll 30s linear infinite;`  
`}`  
`.marquee ul {`  
    `list-style: none;`  
`}`  
`.marquee li img {`  
    `margin: 0 90px;`  
`}`  
`.marquee a:hover {`  
    `text-decoration: underline;`  
`}`  
`@keyframes scroll {`  
  `from {`  
    `transform: translateX(0);`  
  `}`  
  `to {`  
    `transform: translateX(calc(-100% - var(--gap)));`  
  `}`  
`}`  
`.marquee:hover .marquee__content {`  
    `animation-play-state: paused !important;`  
 `}`  

---
## HTML-Marquee
`<div class="marquee">`  
    `<ul class="marquee__content">`  
      `<li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li>`  
      `<li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li>`  
      `<li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li>`  
`<li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li><li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li>`  
  `</ul>`  
`<ul aria-hidden="true" class="marquee__content">`  
      `<li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li>`  
     `<li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li>`  
      `<li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li>`  
`<li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li><li>marketing A.I. physical boy neon assassin motion tank-traps dolphin corporation katana girl sub-orbital refrigerator Legba courier.</li>`  
    `</ul>`  
`</div>`  

---
## CSS-Custom scrollbars
`/* width */`  
`::-webkit-scrollbar {`  
  `width: 5px;`  
  `height: 5px;`  
`}`  
  
`/* Track */`  
`::-webkit-scrollbar-track {`  
  `background: #f1f1f1;`  
`}`  
  
`/* Handle */`  
`::-webkit-scrollbar-thumb {`  
  `background: #ccc;`  
`}`  
  
`/* Handle on hover */`  
`::-webkit-scrollbar-thumb:hover {`  
  `background: #111;`  
`}`  

---

**JS-Mouse drag per scrolling orizzontale**  
`//Nella riga successiva sostituire ".scroll" col nome del vostro contenitore che scrolla`  
  `const slider = document.querySelector('.scroll');`  
  `let isDown = false;`  
  `let startX;`  
  `let scrollLeft;`  
  `slider.addEventListener('mousedown', (e) => {`  
    `isDown = true;`  
    `slider.classList.add('active');`  
    `startX = e.pageX - slider.offsetLeft;`  
    `scrollLeft = slider.scrollLeft;`  
    `cancelMomentumTracking();`  
  `});`  
  `slider.addEventListener('mouseleave', () => {`  
    `isDown = false;`  
    `slider.classList.remove('active');`  
  `});`  
  `slider.addEventListener('mouseup', () => {`  
    `isDown = false;`  
    `slider.classList.remove('active');`  
    `beginMomentumTracking();`  
  `});`  
  `slider.addEventListener('mousemove', (e) => {`  
    `if(!isDown) return;`  
    `e.preventDefault();`  
    `const x = e.pageX - slider.offsetLeft;`  
    `const walk = (x - startX) * 3; //scroll-fast`  
    `var prevScrollLeft = slider.scrollLeft;`  
    `slider.scrollLeft = scrollLeft - walk;`  
    `velX = slider.scrollLeft - prevScrollLeft;`  
  `});`  
  `// Momentum`  
  `var velX = 0;`  
  `var momentumID;`  
  `slider.addEventListener('wheel', (e) => {`  
    `cancelMomentumTracking();`  
  `});`    
  `function beginMomentumTracking(){`  
    `cancelMomentumTracking();`  
    `momentumID = requestAnimationFrame(momentumLoop);`  
  `}`  
  `function cancelMomentumTracking(){`  
    `cancelAnimationFrame(momentumID);`  
  `}`  
  `function momentumLoop(){`  
    `slider.scrollLeft += velX;`  
    `velX *= 0.9;`  
    `if (Math.abs(velX) > 0.5){`  
      `momentumID = requestAnimationFrame(momentumLoop);`  
    `}`  
  `}`  

---
##  CSS-Hover text to show image
`/*".titolo" è la classe che va data al testo; ".img" è la classe che va data alle immagini*/`  
`.titolo:hover + .img {`
    `display: block;`
`}`

`.titolo {`
	`top: 100px;`
`}`

`.img {`
	`position: absolute;`
   ` right: 0;`
  `  width: 50% !important;`
    `top: 0;`
`}`  

---
## CSS-Hover image to show text
`.immagine:hover + .titolo {`
    `display: block;`
`}`

`.titolo {`
	`position: absolute;`
	`top: 100px;`
	`left: 60px;`
`}`

