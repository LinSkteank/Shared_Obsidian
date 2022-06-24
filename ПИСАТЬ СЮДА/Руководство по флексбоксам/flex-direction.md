Свойство __flex-direction__ задаёт направление основных осей в контейнере и тем самым определяет положение флексов в контейнере. На само направление также влияет значение атрибута _dir_ у контейнера.

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию</th>
			<td>row</td>
		</tr>
		<tr>
			<th>Наследуется</th>
			<td>Нет</td>
		</tr>
		<tr>
			<th>Применяется</th>
			<td>К флекс-контейнеру</td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Нет</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
flex-direction: row | row-reverse | column | column-reverse
```

### Значения
__1) row__

Главная ось направлена так же, как и ориентация текста, по умолчанию слева направо. Если значение dir задано как rtl, то направление оси идёт справа налево.

__2) row-reverse__

Похоже на значение row, но меняются местами начальная и конечная точки и главная ось направлена справа налево. Если значение dir задано как rtl, то направление оси идёт слева направо.

__3) column__

Главная ось располагается вертикально и направлена сверху вниз.

__4) column-reverse__

Главная ось располагается вертикально, но меняется положение начальной и конечной точек и ось направлена снизу вверх.

### Пример
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>flex-direction</title>
  <style>
   .flex-row {
    padding: 0;
    margin: 0;
    list-style: none;
    display: flex;
    flex-direction: row-reverse;
   }
  </style>
 </head>
 <body>
  <ul class="flex-row">
   <li><img src="image/thumb1.jpg" alt=""></li>
   <li><img src="image/thumb2.jpg" alt=""></li>
   <li><img src="image/thumb3.jpg" alt=""></li>
  </ul> 
 </body>
</html>
```

