---
type: paper
tags: 📥️/📜️/🩳/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[свойство list-style 2021-10-17]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-17]]


Универсальное свойство, позволяющее одновременно задать стиль маркера, его положение, а также изображение, которое будет использоваться в качестве маркера. [[свойство list-style-type 2021-10-17|list-style-type]], [[Cвойство list-style-position 2021-10-17|list-style-position]]и [[свойство list-style-image 2021-10-17|list-style-image]]

```css
list-style: list-style-type || list-style-position || list-style-image | inherit
```



Любые комбинации трех значений определяющих стиль маркеров, они разделяются между собой пробелом. Комбинации значений должны следовать в указанном порядке: вначале идет тип маркера, затем положение и картинка. Ни одно значение не является обязательным, поэтому неиспользуемые можно опустить.

==inherit== - Наследует значение родителя.

```css
list-style: square inside;    
```

```css
list-style: inside square;
```