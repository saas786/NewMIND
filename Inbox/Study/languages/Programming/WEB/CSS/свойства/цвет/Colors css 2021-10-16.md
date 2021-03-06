---
type: paper
tags: 📥️/📜️/🩳/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Colors css 2021-10-16]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-16]]


## **именованные цвета**

-   `silver`, `aqua`, `fuchsia`
-   `lime`, `olive`, `red`
-   `white`, `black`, `gray`
-   `maroon`, `orange`, `yellow`
-   `blue`, `green`, `navy`
-   `purple`, `teal`

```css
p { color: green; }
```

## Цветовая модель RGB

Общий вид функционального формата: `rgb(цвет)`, где «цвет», это комбинация из трех целых чисел (от 0 до 255) или трех процентных значений (от 0% до 100%), перечисленных через запятую. Далее несколько примеров.

```css
rgb(255, 255, 255) /* белый цвет */
rgb(0, 0, 0) /* черный цвет */
rgb(255, 0, 0) /* красный цвет */
```

Далее те же цвета, только при помощи процентных значений.

```css
rgb(100%, 100%, 100%) /* белый цвет */
rgb(0%, 0%, 0%) /* черный цвет */
rgb(100%, 0%, 0%) /* красный цвет */
```

## Шестнадцатеричный формат записи цвета в CSS (Hex)

Отличий от RGB почти нет. Указывается три цвета RRGGBB в диапазоне от 00 до FF (FF это 255 в десятичной системе)

```css
p { color: #FFFFFF; } /* белый цвет текста */
p { color: #000000; } /* черный цвет текста */
p { color: #FF0000; } /* красный цвет текста */
```


сокращенный формат
```css
p { color: #000; } /* то же самое #000000 */  
p { color: #123; } /* то же самое #112233 */  
p { color: #0FB; } /* то же самое #00FFBB */
```