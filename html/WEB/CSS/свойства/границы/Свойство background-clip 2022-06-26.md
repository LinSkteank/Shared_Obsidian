
---
type: paper
tags: 📥️/📜️/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство background-clip 2022-06-26]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2022-06-26]]


# background-clip

Определяет, как цвет фона или фоновая картинка должна выводиться под границами. Эффект заметен при прозрачных или пунктирных границах.

### Краткая информация
<table>
<tbody>
	<tr>
		<th>Значение по умолчанию </th>
		 <td class="value">border-box</td>
	</tr>
	<tr>
		<th>Наследуется</th>
		<td>Нет</td>
	</tr>
	<tr>
		<th>Применяется</th>
		<td>Ко всем элементам</td>
	</tr>
	<tr>
		<th>Анимируется</th>
		<td>Нет</td>
	</tr>
</tbody>
</table>

### Синтаксис 

**Значений может быть несколько (для каждого из множественных фоновых рисунков), при этом значения разделяются между собой запятой.**

```css
background-clip: [padding-box | border-box | content-box | text]#
```

### Значения 
- ==padding-box== Фон отображается внутри границ.

- ==border-box==  Фон выводится под границами.

- ==content-box== Фон отображается только внутри контента.

- ==text== _Нестандартный_ Фон отображается только внутри текста.

### Пример 
Результат использования значений свойства background-clip для элемента с пунктирной рамкой толщиной 10 пикселей.

![[css_background-clip_1.png]]

##### code

```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>background-clip</title>
  <style>
   .example {
    background: #5f392f url(http://localhost:50000/8s.jpg); /* Фоновый рисунок */
    border: 10px dotted red; /* Параметры рамки */   
    background-clip: border-box; /* Фон под рамкой */    
    padding: 10px; /* Поля */
    color: #fff; /* Цвет текста */    
    min-height: 48px; /* Минимальная высота */
   }
  </style>
 </head>
 <body>
  <div class="example">Содержимое страницы</div>
 </body>
</html>
```

##### result
<iframe src="http://localhost:50000/background-clip.html" style="background: white; border: none; width: 100%; height: 100%;"/></iframe>

