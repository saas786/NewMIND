---
type: paper
tags: 📥️/📜️/🩳/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство background-clip 2021-10-17]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-17]]

## background-clip определяет отображение фона под границами

Фон может отображаться под границами, внутри их или внутри контента. Чтобы это реализовать, необходимо использовать свойство `background-clip`.

```css
background-clip: [border-box |padding-box | content-box];    
```

### значения
1.  `border-box` – фон будет отображаться под рамкой;
2.  `padding-box` – фон будет отображаться внутри рамки;
3.  `content-box` – фон будет отображаться внутри контента.

```css
.clip {  
background: #f1f1f1;  
border: 20px dotted #000000;  
background-clip: border-box;  
padding: 10px;  
height: 50px;  
}
```