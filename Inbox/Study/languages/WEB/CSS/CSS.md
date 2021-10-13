# CSS

**CSS** (Cascading Style Sheets, или каскадные таблицы стилей) - это декларативный язык, который отвечает за то, как страницы выглядят в [веб браузере](https://developer.mozilla.org/ru/docs/Glossary/Browser). CSS стили содержат свойства и их значения, которые и определяют, как будет выглядеть сайт.

CSS одна из ключевых Web технологий, наряду с [HTML](https://developer.mozilla.org/ru/docs/Glossary/HTML) и [JavaScript](https://developer.mozilla.org/ru/docs/Glossary/JavaScript). Как правило CSS используется для определения стилей [HTML элементов](https://developer.mozilla.org/ru/docs/Glossary/Element), но также может быть применён совместно с другими языками разметки, такими как [SVG](https://developer.mozilla.org/ru/docs/Glossary/SVG) или [XML](https://developer.mozilla.org/ru/docs/Glossary/XML).

CSS правило состоит из селектора и набора [свойств (en-US)](https://developer.mozilla.org/en-US/docs/Glossary/property/CSS "Currently only available in English (US)") с их значениями. В этом примере все HTML параграфы будут иметь текст жёлтого цвета на чёрном фоне:

```css
/* Селектор "p" означает, что данное правило будет применено ко всем параграфам в документе */
p {
  /* Свойство "color" определяет цвет текста, в данном случае желтый. */
  color: yellow;

  /* Свойство "background-color" определяет цвет фона элемента, в данном случае черный. */
  background-color: black;
}
```

Copy to Clipboard

"Каскадность" CSS - это правила, которые регулируют приоритет селекторов при отображении внешнего вида элементов страницы. Это очень важная особенность, поскольку сложный веб-сайт может иметь тысячи CSS-селекторов.


[[connection point]]