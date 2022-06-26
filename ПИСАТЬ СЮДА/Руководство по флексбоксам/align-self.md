Свойство align-self выравнивает флекс-элементы текущей строки, переписывая значение [[align-items]].

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию </th>
			<td>auto</td>
		</tr>
		<tr>
			<th>Наследуется</th>
			<td>Нет</td>
		</tr>
		<tr>
			<th>Применяется</th>
			<td>К флекс-элементу</td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Нет</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
align-self: auto | flex-start | flex-end | center | baseline | stretch
```

### Значения
__1) auto__

Берёт родительское значение align-items или stretch, если нет родителя.

__2) flex-start__

Элемент выравнивается в начале поперечной оси контейнера.

__3) flex-end__

Элемент выравнивается в конце поперечной оси контейнера.

__4) center__

Элемент выравнивается по центральной линии на поперечной оси.

__5) baseline__

Элемент выравнивается по базовой линии текста.

__6) stretch__

Элемент растягивается таким образом, чтобы занять всё свободное пространство контейнера по поперечной оси.

### Пример
##### code
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>align-items</title>
  <style>
   .flex-container {
    display: flex;
    align-items: flex-start;
    height: 160px; /* Высота контейнера */
   }
   .flex-item {
    margin-left: 1rem; /* Расстояние между блоками */
    padding: 10px; /* Поля вокруг текста */
    width: 33.333%; /* Ширина блоков */
   }
   .flex-item:first-child { margin-left: 0; }
   .flex-item:hover { 
     align-self: stretch; /* Растягиваем при наведении */
   }
   .item1 { background: #F0BA7D; }
   .item2 { background: #CAE2AA; }
   .item3 { background: #A6C0C9; }
  </style>
 </head> 
 <body>
  <div class="flex-container">
   <div class="flex-item item1">
    Фенек — лисица, живущая в пустынях Северной Африки. 
    Имеет достаточно миниатюрный размер и своеобразную внешность 
    с большими ушами.
   </div>
   <div class="flex-item item2">
    Корсак — хищное млекопитающее рода лисиц.
   </div>
   <div class="flex-item item3">
    Лисица — хищное млекопитающее семейства псовых, 
    наиболее распространённый и самый крупный вид рода лисиц.
   </div>
  </div>
 </body>
</html>
```

##### result
<iframe src="http://localhost:50000/align-self.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>

