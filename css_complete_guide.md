# CSS - To'liq va Mukammal O'quv Qo'llanma

## 1. CSS Kirish (CSS Introduction)

CSS (Cascading Style Sheets) - bu web sahifalarning ko'rinishini va formatini belgilovchi til. HTML mazmunni yaratsa, CSS uni chiroyli qilib bezaydi.

### CSS ning afzalliklari:
- HTML va dizaynni ajratish
- Bir necha sahifalarga bir xil stil berish
- Sahifa yuklanish tezligini oshirish
- Responsive dizayn yaratish imkoniyati

## 2. CSS Sintaksis (CSS Syntax)

CSS qoidasi ikki qismdan iborat:

```css
selector {
    property: value;
}
```

**Misol:**
```css
h1 {
    color: blue;
    font-size: 24px;
}
```

- `h1` - selektor (qaysi elementga stil berish)
- `color` - xususiyat (property)
- `blue` - qiymat (value)

## 3. CSS Selektorlar (CSS Selectors)

### Element selektori
```css
p {
    color: red;
}
```

### ID selektori
```css
#my-id {
    background-color: yellow;
}
```

### Class selektori
```css
.my-class {
    font-weight: bold;
}
```

### Universal selektor
```css
* {
    margin: 0;
    padding: 0;
}
```

### Attribute selektori
```css
input[type="text"] {
    border: 1px solid gray;
}
```

## 4. CSS Qo'llash Usullari (CSS How To)

### 1. Inline CSS
```html
<p style="color: blue; font-size: 16px;">Matn</p>
```

### 2. Internal CSS
```html
<head>
<style>
p {
    color: blue;
    font-size: 16px;
}
</style>
</head>
```

### 3. External CSS
```html
<head>
<link rel="stylesheet" href="styles.css">
</head>
```

## 5. CSS Izohlar (CSS Comments)

```css
/* Bu bir qatorli izoh */

/*
Bu
ko'p qatorli
izoh
*/

p {
    color: red; /* Matn rangini qizil qilish */
}
```

## 6. CSS Ranglar (CSS Colors)

### Rang belgilash usullari:

```css
/* Rang nomi */
color: red;

/* Hex kod */
color: #FF0000;

/* RGB */
color: rgb(255, 0, 0);

/* RGBA (shaffoflik bilan) */
color: rgba(255, 0, 0, 0.5);

/* HSL */
color: hsl(0, 100%, 50%);

/* HSLA */
color: hsla(0, 100%, 50%, 0.5);
```

## 7. CSS Fon (CSS Backgrounds)

```css
div {
    /* Fon rangi */
    background-color: lightblue;
    
    /* Fon rasmi */
    background-image: url("image.jpg");
    
    /* Rasmni takrorlash */
    background-repeat: no-repeat;
    
    /* Rasmni joylashish */
    background-position: center;
    
    /* Rasmni o'lchami */
    background-size: cover;
    
    /* Qisqa yozuv */
    background: lightblue url("image.jpg") no-repeat center/cover;
}
```

## 8. CSS Chegaralar (CSS Borders)

```css
div {
    /* Chegara kengligi */
    border-width: 2px;
    
    /* Chegara turi */
    border-style: solid;
    
    /* Chegara rangi */
    border-color: black;
    
    /* Qisqa yozuv */
    border: 2px solid black;
    
    /* Alohida tomonlar */
    border-top: 1px solid red;
    border-right: 2px dashed blue;
    border-bottom: 3px dotted green;
    border-left: 4px double yellow;
    
    /* Yumaloq burchaklar */
    border-radius: 10px;
}
```

## 9. CSS Chetki bo'shliqlar (CSS Margins)

```css
div {
    /* Barcha tomonlar */
    margin: 20px;
    
    /* Vertikal va gorizontal */
    margin: 10px 15px;
    
    /* Yuqori, yon, pastki */
    margin: 10px 15px 20px;
    
    /* Har bir tomon alohida */
    margin: 10px 15px 20px 25px;
    
    /* Alohida belgilash */
    margin-top: 10px;
    margin-right: 15px;
    margin-bottom: 20px;
    margin-left: 25px;
    
    /* Markazlash */
    margin: 0 auto;
}
```

## 10. CSS Ichki bo'shliqlar (CSS Padding)

```css
div {
    /* Barcha tomonlar */
    padding: 20px;
    
    /* Vertikal va gorizontal */
    padding: 10px 15px;
    
    /* Yuqori, yon, pastki */
    padding: 10px 15px 20px;
    
    /* Har bir tomon alohida */
    padding: 10px 15px 20px 25px;
    
    /* Alohida belgilash */
    padding-top: 10px;
    padding-right: 15px;
    padding-bottom: 20px;
    padding-left: 25px;
}
```

## 11. CSS Balandlik/Kenglik (CSS Height/Width)

```css
div {
    width: 300px;
    height: 200px;
    
    /* Foizda */
    width: 50%;
    height: 100vh;
    
    /* Minimal va maksimal */
    min-width: 200px;
    max-width: 500px;
    min-height: 100px;
    max-height: 400px;
}
```

## 12. CSS Box Model

Box model har bir HTML elementining tuzilishini tushuntiradi:

```
+------------------------+
|        Margin          |
|  +------------------+  |
|  |     Border       |  |
|  |  +------------+  |  |
|  |  |  Padding   |  |  |
|  |  |  +------+  |  |  |
|  |  |  |Content |  |  |
|  |  |  +------+  |  |  |
|  |  +------------+  |  |
|  +------------------+  |
+------------------------+
```

```css
div {
    width: 300px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
    
    /* Jami kenglik = 300 + 40 + 10 + 20 = 370px */
}

/* Box-sizing bilan */
div {
    box-sizing: border-box;
    width: 300px;
    padding: 20px;
    border: 5px solid black;
    /* Jami kenglik = 300px */
}
```

## 13. CSS Kontur (CSS Outline)

```css
div {
    outline-width: 2px;
    outline-style: solid;
    outline-color: red;
    
    /* Qisqa yozuv */
    outline: 2px solid red;
    
    /* Konturdan masofa */
    outline-offset: 5px;
}
```

## 14. CSS Matn (CSS Text)

```css
p {
    /* Matn rangi */
    color: blue;
    
    /* Matnni hizalash */
    text-align: center; /* left, right, justify */
    
    /* Matn bezaklari */
    text-decoration: underline; /* overline, line-through, none */
    
    /* Matn transformatsiyasi */
    text-transform: uppercase; /* lowercase, capitalize */
    
    /* Matn soyasi */
    text-shadow: 2px 2px 4px #000000;
    
    /* Qatorlar orasidagi masofa */
    line-height: 1.5;
    
    /* Harflar orasidagi masofa */
    letter-spacing: 2px;
    
    /* So'zlar orasidagi masofa */
    word-spacing: 5px;
    
    /* Matnni qirqish */
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
}
```

## 15. CSS Shriftlar (CSS Fonts)

```css
p {
    /* Shrift oilasi */
    font-family: Arial, sans-serif;
    
    /* Shrift o'lchami */
    font-size: 16px;
    
    /* Shrift og'irligi */
    font-weight: bold; /* normal, 100-900 */
    
    /* Shrift uslubi */
    font-style: italic; /* normal, oblique */
    
    /* Qisqa yozuv */
    font: italic bold 16px/1.5 Arial, sans-serif;
}

/* Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

body {
    font-family: 'Roboto', sans-serif;
}
```

## 16. CSS Ikonkalar (CSS Icons)

### Font Awesome
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```

```css
.icon {
    font-size: 24px;
    color: blue;
}
```

```html
<i class="fas fa-home icon"></i>
```

## 17. CSS Linklar (CSS Links)

```css
/* Link holatlari */
a:link { color: blue; }      /* Tashrif buyurilmagan */
a:visited { color: purple; } /* Tashrif buyurilgan */
a:hover { color: red; }      /* Sichqoncha ustida */
a:active { color: yellow; }  /* Bosilgan payt */

/* Linkni bezash */
a {
    text-decoration: none;
    padding: 10px;
    background-color: #f0f0f0;
    border-radius: 5px;
    transition: all 0.3s ease;
}

a:hover {
    background-color: #ddd;
    transform: scale(1.05);
}
```

## 18. CSS Ro'yxatlar (CSS Lists)

```css
/* Ro'yxat uslubi */
ul {
    list-style-type: disc; /* circle, square, none */
}

ol {
    list-style-type: decimal; /* lower-roman, upper-alpha */
}

/* Maxsus belgilar */
ul {
    list-style-image: url("bullet.png");
}

/* Belgi joylashishi */
li {
    list-style-position: inside; /* outside */
}

/* Qisqa yozuv */
ul {
    list-style: square inside;
}

/* Gorizontal menyu */
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
}

li {
    margin-right: 20px;
}
```

## 19. CSS Jadvallar (CSS Tables)

```css
table {
    border-collapse: collapse; /* separate */
    width: 100%;
}

th, td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: left;
}

th {
    background-color: #f2f2f2;
}

/* Qator rangi */
tr:nth-child(even) {
    background-color: #f9f9f9;
}

tr:hover {
    background-color: #f5f5f5;
}

/* Responsive jadval */
.table-container {
    overflow-x: auto;
}
```

## 20. CSS Display

```css
/* Display turlari */
.block { display: block; }
.inline { display: inline; }
.inline-block { display: inline-block; }
.none { display: none; }
.flex { display: flex; }
.grid { display: grid; }

/* Visibility */
.hidden { visibility: hidden; } /* Joy egallaydi */
.visible { visibility: visible; }
```

## 21. CSS Max-width

```css
div {
    max-width: 500px;
    margin: 0 auto; /* Markazlash */
}

img {
    max-width: 100%;
    height: auto; /* Nisbatni saqlash */
}
```

## 22. CSS Position

```css
/* Static (standart) */
.static { position: static; }

/* Relative */
.relative {
    position: relative;
    top: 20px;
    left: 30px;
}

/* Absolute */
.absolute {
    position: absolute;
    top: 0;
    right: 0;
}

/* Fixed */
.fixed {
    position: fixed;
    bottom: 0;
    right: 0;
}

/* Sticky */
.sticky {
    position: sticky;
    top: 0;
}
```

## 23. CSS Overflow

```css
div {
    width: 200px;
    height: 100px;
    overflow: visible; /* hidden, scroll, auto */
}

/* Faqat bir yo'nalishda */
.scroll-y {
    overflow-x: hidden;
    overflow-y: scroll;
}
```

## 24. CSS Float

```css
.left { float: left; }
.right { float: right; }

/* Float ni bekor qilish */
.clearfix::after {
    content: "";
    display: table;
    clear: both;
}
```

## 25. CSS Inline-block

```css
.inline-block {
    display: inline-block;
    width: 200px;
    height: 100px;
    vertical-align: top;
}
```

## 26. CSS Z-index

```css
.layer1 { z-index: 1; }
.layer2 { z-index: 2; }
.layer3 { z-index: 999; }

/* Faqat positioned elementlarda ishlaydi */
.positioned {
    position: relative;
    z-index: 10;
}
```

## 27. CSS Hizalash (CSS Align)

```css
/* Markazda hizalash */
.center {
    text-align: center;
    margin: 0 auto;
}

/* Vertikal hizalash */
.vertical-center {
    position: relative;
    top: 50%;
    transform: translateY(-50%);
}

/* Flexbox bilan */
.flex-center {
    display: flex;
    justify-content: center;
    align-items: center;
}

/* Grid bilan */
.grid-center {
    display: grid;
    place-items: center;
}
```

## 28. CSS Kombinatorlar (CSS Combinators)

```css
/* Avlod selektori */
div p { color: blue; }

/* Bola selektori */
div > p { color: red; }

/* Qo'shni aka-uka selektori */
h2 + p { color: green; }

/* Umumiy aka-uka selektori */
h2 ~ p { color: purple; }
```

## 29. CSS Pseudo-class

```css
/* Link holatlari */
a:hover { color: red; }
a:active { color: blue; }
a:focus { outline: 2px solid orange; }

/* Element holatlari */
input:disabled { background-color: #f5f5f5; }
input:enabled { background-color: white; }
input:checked + label { color: green; }

/* Tuzilma selektorlari */
p:first-child { font-weight: bold; }
p:last-child { margin-bottom: 0; }
p:nth-child(odd) { background-color: #f9f9f9; }
p:nth-child(even) { background-color: #ffffff; }
p:nth-child(3) { color: red; }

/* Mazmun selektorlari */
div:empty { display: none; }
input:not(.special) { border: 1px solid gray; }
```

## 30. CSS Pseudo-element

```css
/* Before va After */
p::before {
    content: "★ ";
    color: gold;
}

p::after {
    content: " ★";
    color: gold;
}

/* Birinchi harf */
p::first-letter {
    font-size: 2em;
    font-weight: bold;
    color: red;
}

/* Birinchi qator */
p::first-line {
    font-weight: bold;
    color: blue;
}

/* Tanlangan matn */
::selection {
    background-color: yellow;
    color: black;
}

/* Placeholder */
input::placeholder {
    color: #999;
    font-style: italic;
}
```

## 31. CSS Shaffoflik (CSS Opacity)

```css
.transparent {
    opacity: 0.5; /* 0 dan 1 gacha */
}

.semi-transparent {
    background-color: rgba(255, 0, 0, 0.5);
}

/* Hover effekti */
.fade:hover {
    opacity: 0.7;
    transition: opacity 0.3s ease;
}
```

## 32. CSS Navigatsiya Paneli (CSS Navigation Bar)

```css
/* Gorizontal menyu */
nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    background-color: #333;
    overflow: hidden;
}

nav li {
    float: left;
}

nav li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
}

nav li a:hover {
    background-color: #111;
}

/* Vertikal menyu */
.vertical-nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    width: 200px;
    background-color: #f1f1f1;
}

.vertical-nav li a {
    display: block;
    color: #000;
    padding: 8px 16px;
    text-decoration: none;
}

.vertical-nav li a:hover {
    background-color: #555;
    color: white;
}
```

## 33. CSS Dropdown

```css
.dropdown {
    position: relative;
    display: inline-block;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 1;
}

.dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}

.dropdown-content a:hover {
    background-color: #f1f1f1;
}

.dropdown:hover .dropdown-content {
    display: block;
}
```

## 34. CSS Rasm Galereyasi (CSS Image Gallery)

```css
.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    padding: 20px;
}

.gallery-item {
    position: relative;
    overflow: hidden;
    border-radius: 8px;
}

.gallery-item img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    transition: transform 0.3s ease;
}

.gallery-item:hover img {
    transform: scale(1.1);
}

.gallery-item .overlay {
    position: absolute;
    bottom: 0;
    background: linear-gradient(transparent, rgba(0,0,0,0.7));
    width: 100%;
    height: 100%;
    display: flex;
    align-items: flex-end;
    padding: 20px;
    color: white;
    opacity: 0;
    transition: opacity 0.3s ease;
}

.gallery-item:hover .overlay {
    opacity: 1;
}
```

## 35. CSS Image Sprites

```css
.icon {
    width: 32px;
    height: 32px;
    background-image: url('sprite.png');
    background-repeat: no-repeat;
}

.icon-home { background-position: 0 0; }
.icon-user { background-position: -32px 0; }
.icon-mail { background-position: -64px 0; }
.icon-phone { background-position: -96px 0; }
```

## 36. CSS Attribute Selektorlar

```css
/* Atribut mavjudligi */
input[required] { border: 2px solid red; }

/* Aniq qiymat */
input[type="email"] { background-color: lightblue; }

/* Qiymatning boshi */
a[href^="https"] { color: green; }

/* Qiymatning oxiri */
a[href$=".pdf"] { color: red; }

/* Qiymat ichida */
a[href*="youtube"] { color: purple; }

/* So'z sifatida */
div[class~="highlight"] { background-color: yellow; }

/* Tire bilan boshlangan */
div[lang|="en"] { font-style: italic; }

/* Katta-kichik harfga sezgir emas */
input[type="email" i] { text-transform: lowercase; }
```

## 37. CSS Formalar (CSS Forms)

```css
/* Form konteyneri */
form {
    max-width: 500px;
    margin: 0 auto;
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 8px;
}

/* Input maydonlari */
input[type="text"],
input[type="email"],
input[type="password"],
textarea,
select {
    width: 100%;
    padding: 12px;
    border: 1px solid #ddd;
    border-radius: 4px;
    box-sizing: border-box;
    margin-bottom: 16px;
    font-size: 16px;
}

/* Focus holati */
input:focus,
textarea:focus,
select:focus {
    outline: none;
    border-color: #007bff;
    box-shadow: 0 0 5px rgba(0, 123, 255, 0.3);
}

/* Label */
label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #333;
}

/* Button */
button,
input[type="submit"] {
    background-color: #007bff;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
}

button:hover,
input[type="submit"]:hover {
    background-color: #0056b3;
}

/* Checkbox va Radio */
input[type="checkbox"],
input[type="radio"] {
    width: auto;
    margin-right: 8px;
}

/* Xato holati */
.error {
    border-color: #dc3545 !important;
    box-shadow: 0 0 5px rgba(220, 53, 69, 0.3);
}

.error-message {
    color: #dc3545;
    font-size: 14px;
    margin-top: -12px;
    margin-bottom: 16px;
}
```

## 38. CSS Hisoblagichlar (CSS Counters)

```css
body {
    counter-reset: section;
}

h2 {
    counter-increment: section;
}

h2::before {
    content: "Bo'lim " counter(section) ": ";
}

/* Ichki hisoblagichlar */
ol {
    counter-reset: item;
}

li {
    counter-increment: item;
    list-style: none;
}

li::before {
    content: counter(item) ". ";
    font-weight: bold;
}
```

## 39. CSS Veb-sayt Maketi (CSS Website Layout)

```css
/* Grid Layout */
.container {
    display: grid;
    grid-template-areas: 
        "header header header"
        "nav content aside"
        "footer footer footer";
    grid-template-columns: 200px 1fr 200px;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
    gap: 20px;
}

.header { grid-area: header; }
.nav { grid-area: nav; }
.content { grid-area: content; }
.aside { grid-area: aside; }
.footer { grid-area: footer; }

/* Flexbox Layout */
.flex-container {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

.flex-header,
.flex-footer {
    flex-shrink: 0;
}

.flex-main {
    display: flex;
    flex: 1;
}

.flex-nav,
.flex-aside {
    flex-basis: 200px;
}

.flex-content {
    flex: 1;
}
```

## 40. CSS Birliklar (CSS Units)

```css
/* Absolut birliklar */
.px { width: 100px; }      /* Piksel */
.pt { font-size: 12pt; }   /* Point */
.cm { width: 2cm; }        /* Santimetr */
.mm { width: 20mm; }       /* Millimetr */
.in { width: 1in; }        /* Dyuym */
.pc { font-size: 1pc; }    /* Pica */

/* Nisbiy birliklar */
.em { font-size: 1.5em; }    /* Ota-element shriftiga nisbatan */
.rem { font-size: 1.5rem; }  /* Root element shriftiga nisbatan */
.percent { width: 50%; }     /* Ota-elementga nisbatan */

/* Viewport birliklar */
.vw { width: 50vw; }         /* Viewport kengligi */
.vh { height: 100vh; }       /* Viewport balandligi */
.vmin { width: 50vmin; }     /* Viewport minimal o'lchami */
.vmax { width: 50vmax; }     /* Viewport maksimal o'lchami */

/* Ch va ex */
.ch { width: 20ch; }         /* "0" belgisining kengligi */
.ex { height: 2ex; }         /* "x" harfining balandligi */
```

## 41. CSS Xususiylik Darajasi (CSS Specificity)

Xususiylik darajasi quyidagi tartibda hisoblanadi:

1. Inline styles (1000 ball)
2. ID selektorlar (100 ball)
3. Class, attribute, pseudo-class (10 ball)
4. Element va pseudo-element (1 ball)

```css
/* 1 ball */
p { color: blue; }

/* 10 ball */
.red { color: red; }

/* 100 ball */
#main { color: green; }

/* 1000 ball */
/* style="color: purple;" */

/* 111 ball */
#main .content p { color: orange; }
```

## 42. CSS !important

```css
p { 
    color: blue !important; 
}

/* Bu qoida yuqoridagini bekor qila olmaydi */
p { 
    color: red; 
}
```

**Eslatma:** `!important` ni juda kam hollarda ishlating!

## 43. CSS Matematik Funksiyalar (CSS Math Functions)

```css
.calc-example {
    width: calc(100% - 40px);
    height: calc(100vh - 60px);
    margin: calc(10px + 5px);
}

.min-max {
    width: min(400px, 100%);
    height: max(200px, 50vh);
    font-size: clamp(16px, 4vw, 24px);
}

.trigonometry {
    transform: rotate(calc(45deg + 90deg));
    width: calc(sin(45deg) * 100px);
    height: calc(cos(30deg) * 100px);
}
```

## 44. CSS Yumaloq Burchaklar (CSS Rounded Corners)

```css
.rounded {
    border-radius: 10px;
}

.different-corners {
    border-top-left-radius: 10px;
    border-top-right-radius: 20px;
    border-bottom-right-radius: 30px;
    border-bottom-left-radius: 40px;
}

.elliptical {
    border-radius: 50px / 25px;
}

.circle {
    width: 100px;
    height: 100px;
    border-radius: 50%;
}
```

## 45. CSS Border Images

```css
.border-image {
    border: 10px solid transparent;
    border-image: url("border.png") 30 round;
}

.gradient-border {
    border: 3px solid;
    border-image: linear-gradient(45deg, red, blue) 1;
}
```

## 46-47. CSS Fon va Ranglar (Qo'shimcha)

```css
/* Ko'p fonli rasmlar */
.multiple-bg {
    background: 
        url("image1.png") top left no-repeat,
        url("image2.png") top right no-repeat,
        linear-gradient(to bottom, #fff, #ccc);
}

/* Rang