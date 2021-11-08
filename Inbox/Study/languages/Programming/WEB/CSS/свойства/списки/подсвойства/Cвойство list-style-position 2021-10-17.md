---
type: paper
tags: 📥️/📜️/🩳/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Cвойство list-style-position 2021-10-17]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-17]]


Маркеры списка могут обтекаться текстом в случае необходимости. Для этого существует специальное свойство `list-style-position`.

![[Pasted image 20211017232254.png]] ![[Pasted image 20211017232319.png]]

```css
list-style-position: outside  | inside | inherit;
```

```css
li {  
list-style-position: inside;  
}
```
__Свойство `list-style-position` применяется к элементам `dd`, `dt`, `li`, `ol`, `ul` и имеющим свойство `display: list-item`.__

#### значения
==inside== - Маркер является частью текстового блока и отображается в элементе списка.

==outside== - Текст выравнивается по левому краю, а маркеры размещаются за пределами текстового блока.