Устанавливает расстояние между рамкой, созданной с помощью свойства [[outline]], и краем или границей элемента добавленной через [[border]].

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию </th>
			<td>0</td>
		</tr>
		<tr>
			<th>Наследуется</th>
			<td>Нет</td>
		</tr>
		<tr>
			<th>Применяется</th>
			<td>Ко всем элементам </td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Да</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
outline-offset: <размер>
```

### Значения

__<размер>__

Задаёт расстояние от края элемента до рамки. Отрицательное значение отображает рамку внутри элемента, положительное — вокруг элемента.

### Пример
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>outline-offset</title>
  <style>
   .clue {
    background: url(/example/image/leather.jpg); /* Фоновый рисунок */
    outline: 2px dashed rgba(255,255,255,0.8); /* Пунктирная рамка */
    outline-offset: -10px; /* Выводим рамку внутри элемента */
    padding: 10px; /* Поля */
    min-height: 100px; /* Минимальная высота */
   }
  </style>
 </head>
 <body>
   <div class="clue"></div>
 </body>
</html>
```

