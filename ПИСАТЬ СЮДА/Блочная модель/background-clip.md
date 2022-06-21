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
```css
background-clip: [padding-box | border-box | content-box | text]#
```

### Значения 
__1) padding-box__

Фон отображается внутри границ.

__2) border-box__

Фон выводится под границами.

__3) content-box__

Фон отображается только внутри контента.

__4) text__ _Нестандартный_

Фон отображается только внутри текста.

Значений может быть несколько (для каждого из множественных фоновых рисунков), при этом значения разделяются между собой запятой.

Результат использования значений свойства background-clip для элемента с пунктирной рамкой толщиной 10 пикселей.

![[css_background-clip_1.png]]

### Пример 
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>background-clip</title>
  <style>
   .example {
    background: #5f392f url(/example/image/gear.png); /* Фоновый рисунок */
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

