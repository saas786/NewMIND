---
type: paper
tags: 📥️/📜️/🩳/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство background-position 2021-10-17]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-17]]


## background-position для определения начального положения фона

С помощью свойства `background-position` достаточно просто устанавливается начальное положение фона. Это свойство имеет два значения, которые могут быть заданы ключевым словом, в процентах или в иных значениях допустимых в CSS. Первое значение определяет положение по горизонтали (`left`, `center`, `right`), второе – по вертикали (`top`, `center`, `bottom`). Через запятую можно указывать значения для нескольких фонов.

```css
background-position: значение1 значение2;
```

### значения 
1.  `left top`
2.  `left center`
3.  `left bottom`
4.  `right top`
5.  `right center`
6.  `right bottom`
7.  `center top`
8.  `center center`
9.  `center bottom`

```css
body {  
background-image: url(bg.jpg);  
background-position: 50% 50%;  
}
```
