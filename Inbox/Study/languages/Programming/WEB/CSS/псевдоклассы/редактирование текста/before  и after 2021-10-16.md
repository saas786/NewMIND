---
type: paper
tags: 📥️/📜️/🩳/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[before  и after 2021-10-16]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-16]]

если нужно перед каждым абзацем ставить тире (`-`), то сделать можно при помощи псевдоэлемента `before` и правила для генерации содержимого `content`

```css
p:before {  
	content: '- ';  
}
```

И еще вдруг нам нужно ставить точки в конце абзацев. Для этого есть псевдоэлемент `after`.

```css
p:after {  
	content: '.';  
}
```

[[before&after.html|пример]]