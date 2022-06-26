Определяет порядок вывода флексов внутри флекс-контейнера. Элементы располагаются согласно значениям свойства order от меньшего к большему. При равных значениях order элементы выводятся в том порядке, в каком они появляются в исходном коде.

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию</th>
			<td>0</td>
		</tr>
		<tr>
			<th>Наследуется</th>
			<td>Нет</td>
		</tr>
		<tr>
			<th>Применяется</th>
			<td>К флекс-элементам</td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Да</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
order: <число>
```

### Пример
##### code
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>order</title>
  <style>
   .flex-container {
    padding: 0;
    margin: 0;
    list-style: none; 
    display: flex; 
    flex-flow: row wrap;
   }
   .flex-item {
    background: #69489d;
    color: white;
    padding: 20px 30px;
    margin: 5px; 
    font-size: 2em;
   }
   .flex-item:nth-of-type(1) { order: 5; }
   .flex-item:nth-of-type(2) { order: 4; }
   .flex-item:nth-of-type(3) { order: 3; }
   .flex-item:nth-of-type(4) { order: 2; }
   .flex-item:nth-of-type(5) { order: 1; }
  </style>
 </head>
 <body>
  <ul class="flex-container">
   <li class="flex-item">1</li>
   <li class="flex-item">2</li>
   <li class="flex-item">3</li>
   <li class="flex-item">4</li>
   <li class="flex-item">5</li>
  </ul>
 </body>
</html>
```

##### result
<iframe src="http://localhost:50000/order_original.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>

