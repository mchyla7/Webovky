# Zápis stylů

Styly se dají zapsat trojím způsobem:

1. Přímo u měněného elementu atributem s `style=""`
2. stylopisem = seznamem stylů zapsaným `<style></style>` ve hlavičce dokumentu
3. externím souborem CSS (externí stylopis)

---

## Přímy styl

CSS se dá použít ve zdroji i přímo u stylovaného elementu

`<p style="text-align: center">Text odstavce... </p>`

---

## Stylopis

```html
<!DOCTYPE html>
<html lang="cs">

    <head>
        <meta charset="UTF-8">
        <style type="text/css">
            h2 { color: blue; font-style: italic;}
        </style>
    </head>

    <body>
        <h1>Hlavní Nadpis</h1>
        <h2>Nadpis druhé úrovně</h2>
        <p>Odstavec s textem</p>
        <h2>Nadpis druhé úrovně</h2>
        <p>Odstavec s textem</p>
    </body>
</html>
```

* h2  je selektor (Jméno tagu, jehož formátování se mění)
* {} složené závorky vzmezují deklaraci formátu selektoru
* color je vlastnost
* blue je hodnota

Vlastnost a hodnota jsou odděleny dvojtečkou a mezerou. Pomocí stylopisů se dají formátovat libovolné HTML tagy.

## Externí stylopis

### Soubor pokus.css

```css
p    {text-indent: 30px; margin: 0px 0px 0px 0px;}
a    {text-decoration: none;}
a:link    {color: green;}
a:visited {color: navy;}
a:active  {color: black;}
a:hover   {color: red; text-decoration: underline;}
h2        {color: blue; font-style: italic;}
h1        {color: green; text-align: center;}
```

### HTML stránka

```html
<html lang="cs">

    <head>
        <meta charset="UTF-8">
        <title>Pozadí CSS</title>
        <link rel="stylesheet" href="/CSS/Zaklady-Chyla/css/styly.css">
    </head>

    <body>
  
        <h1>Nadpis 1</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum iusto provident reprehenderit libero maxime veritatis aliquid, modi corrupti hic et neque eos id quae fugit dolorum eligendi, voluptatum atque mollitia?</p>
```

### Typy médií

`<link rel="stylesheet" type="text/css" media="print" href="pokus.css">`

* all - všechny typy zařízení (default)
* aural - hlasový syntezátor
* braille - dotykové zařízení
* embossed - plastická tiskárna pro nevidomé
* hanheld - PDA
* print - tiskárna
* screen - obrazovka počítače
* projection - projekce
* tty - neproporční znakový výstup
* tv - televize

---

### Barvy a pozadí

Barva se může zadávat následujícími způsoby:

* Název barvy: `red`
* Hexadecimálně:
  * `#FF00000`
  * `#ff0000`
  * `#f00`
* Procentuelně: `rgb(100%, 0%, 0%)`
* Absolutně: `rgb(255, 0, 0)`

| Vlastnost             | Hodnoty                                                                   | Význam                                                                                      | Příklady                                                  |
| --------------------- | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| color                 | Barva                                                                     | Barva písma                                                                                 | color: blue                                                 |
| background-color      | Barva<br />transparent                                                    | Barva pozadí<br />Průhledné pozadí                                                       | background-color: yellow<br />background-color: transparent |
| background-image      | none<br />url(cesta)                                                      | obrázek na pozadí                                                                          | background-image:url(../images/gradient_bg.png)             |
| background-repeat     | repeat<br />no-repeat<br />repeat-x<br />repeat-y                         | pozadí se opakuje<br />pozadí se neopakuje<br />opakuje se v ose x<br />opakuje se v ose y | background-repeat: no-repeat;                               |
| background-attachment | scroll<br />fixed                                                         | pozadí se posouvá<br />pozadí se neposouvá                                               | background-attachment: fixed;: no-repeat;                   |
| background-position   | top<br />center<br />bottom<br />left<br />right<br />delka<br />procento | Poloha obrázku na ...                                                                       |                                                             |
| background            | Všechno výše                                                           |                                                                                              |                                                             |
