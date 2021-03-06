---
type: paper
tags: 📥️/📜️/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство linear-gradient() 2021-10-17]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-17]]


##  linear-gradient() добавляет  градиент к фону элемента

Градиентом называется вектор, который состоит из нескольких частных производных функций и указывает направление возрастания функции. В CSS функция `linear-gradient()` дополняет линейный градиент к фону элемента. Она применяется вместе со свойствами `background-image` и `background`.

```css
background: linear-gradient(угол или позиция, цвет1, цвет2);
```

В первом значении функции `linear-gradient()` указывается угол или позиция, то есть направление того самого вектора, который указывается направление изменение цвета. Угол может быть как отрицательным, так и положительным (движение направления вектора идет по часовой стрелке). Ноль градусов будет эквивалентно положению вектора снизу вверх. После указания числового значения, слитно приписывается `deg`.

```css
background: linear-gradient(45deg, #000000, #FFFFFF);
```

Вместо угла можно указывать позицию, которая является буквенным эквивалентом градусов.

1.  `to top` – снизу вверх;
2.  `to bottom` – сверху вниз;
3.  `to left` – справа налево;
4.  `to right` – слева направо;
5.  `to top left` – от правого нижнего угла к левому верхнему;
6.  `to bottom left` – от правого верхнего угла к левому нижнему;
7.  `to top right` – от левого нижнего угла к правому верхнему;
8.  `to bottom right` – от левого верхнего угла к правому нижнему.

```css
background: linear-gradient(to top right, #000000, #FFFFFF);
```

Вторым значением в функции `linear-gradient()` устанавливается цвет, а точнее два и более цвета через запятую в любом из следующих форматов: шестнадцатеричный код, название цвета, RGB, RGBA, HSL или HSLA. [[Свойство color 2021-10-07]]
