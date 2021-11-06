---
type: paper
tags: 📥️/📜️/🩳/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство background-origin 2021-10-17]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-17]]

## background-origin для позиционирования фона

С помощью свойства `background-origin` можно позиционировать фон, при этом свойство __`background-attachment` не должно иметь значение `fixed`__.

```css
background-origin: [border-box |padding-box | content-box];
```

### значения
1.  `border-box` – позиционирование фона осуществляется относительно границы;
2.  `padding-box` – позиционирование фона осуществляется относительно края элемента, при чем толщина границы учитывается;
3.  `content-box` – позиционирование фона осуществляется относительно содержимого элемента;

```css
.origin {  
background: url("img.jpg") no-repeat;  
background-origin: content-box;  
border: 10px solid #000;  
padding: 10px;  
height: 100px;  
}
```