---
type: paper
tags: 📥️/📜️/🩳/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство background-blend-mode 2021-10-17]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-17]]

## background-blend-mode определяет режим наложения фонового изображения

Определяет, как будет накладываться одно фоновое изображение, на другое или на фоновый цвет. То есть, первым задается какой-то фон, при помощи свойства `background-image`, вторым задается фоновое изображение, для которого мы определяем стиль наложения. Позволительно указывать несколько фоновых изображений, т.е. больше двух при помощи `background-image` и в `background-blend-mode` использовать ряд значений, перечисленных через запятую. Стоит обратить внимание на версии браузеров, с которых начинается поддержка свойства `background-blend-mode`, например, Internet Explorer не поддерживает его вовсе.

```css
background-blend-mode: normal | multiply | screen | overlay | darken | lighten | color-dodge | color-burn | hard-light | soft-light | difference | exclusion | hue | saturation | color | luminosity;
```

### значения

1.  `normal` – Обычный. Режим по умолчанию.
2.  `multiply` – Умножение.
3.  `screen` – Осветление.
4.  `overlay` – Перекрытие.
5.  `darken` – Темнее.
6.  `lighten` – Светлее.
7.  `color-dodge` – Осветление основы.
8.  `color-burn` – Затемнение основы.
9.  `hard-light` – Направленный свет.
10.  `soft-light` – Рассеянный свет.
11.  `difference` – Разница.
12.  `exclusion` – Исключение.
13.  `hue` – Тон.
14.  `saturation` – Насыщенность.
15.  `color` – Цвет.
16.  `luminosity` – Яркость.

```css
div {  
width: 500px;  
height: 500px;  
background-image: url("bg.jpg"), url("superimposed.png");  
background-blend-mode: darken;  
}
```