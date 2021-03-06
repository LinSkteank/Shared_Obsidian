---
type: paper
tags: 📥️/📜️/🩳/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство background-repeat 2021-10-17]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-17]]

Устанавливает, как будет повторяться фон, установленный при помощи свойства `background-image`. Повторение может быть по вертикали, по горизонтали или сразу в обе стороны.

```css
background-repeat: значение;
```

### значения

1.  `repeat` – Фоновое изображение повторяется как по вертикали, так и по горизонтали. Последнее изображение будет обрезано, если оно не помещается. Это по умолчанию;
2.  `repeat-x` – Фоновое изображение повторяется только по горизонтали;
3.  `repeat-y` – Фоновое изображение повторяется только по вертикали;
4.  `no-repeat` – Фоновое изображение не повторяется. Изображение будет показано только один раз;
5.  `space` – Фоновое изображение повторяется в максимально возможной степени без отсечения. При необходимости добавляются свободные пространства между изображениями;
6.  `round` – Фоновое изображение повторяется и сжимается или растягивается, чтобы заполнить пространство (без пропусков);

```css
body {  
background-image: url(bg.jpg);  
background-repeat: repeat;  
}
```