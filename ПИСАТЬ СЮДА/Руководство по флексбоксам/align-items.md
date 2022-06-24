Свойство align-items выравнивает флекс-элементы внутри контейнера в перпендикулярном направлении.

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию </th>
			<td>stretch</td>
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
align-items: flex-start | flex-end | center | baseline | stretch
```

### Значения
<table>
	<tbody>
		<tr>
			<th>Значение</th>
			<th>Положение</th>
			<th>Описание</th>
		</tr>
		<tr>
			<td>flex-start</td>
			<td><img src="https://webref.ru/assets/images/css/align-items/flex-start.png" alt="flex-start" width="230" height="180"></td>
			<td>Флексы выравниваются в начале поперечной оси контейнера.</td>
		</tr>
		<tr>
			<td>center</td>
			<td><img src="https://webref.ru/assets/images/css/align-items/center.png" alt="center" width="230" height="180"></td>
			<td>Флексы выравниваются по линии поперечной оси</td>
		</tr>
		<tr>
			<td>flex-end</td>
			<td><img src="https://webref.ru/assets/images/css/align-items/flex-end.png" alt="flex-end" width="230" height="180"></td>
			<td>Флексы выравниваются в конце поперечной оси контейнера.</td>
		</tr>
		<tr>
			<td class="value">stretch</td>
			<td><img src="https://webref.ru/assets/images/css/align-items/stretch.png" alt="stretch" width="230" height="180"></td>
			<td>Флексы растягиваются таким образом, чтобы занять всё доступное пространство контейнера. </td>
		</tr>
		<tr>
			<td>baseline</td>
			<td><img src="https://webref.ru/assets/images/css/align-items/baseline.png" alt="baseline"></td>
			<td>Флексы выравниваются по их базовой линии.</td>
		</tr>
	</tbody>
</table>

### Пример
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>align-items</title>
  <style>
   .flex-container {
    display: flex;
    align-items: stretch; /* Растягиваем */
   }
   .flex-item {
    margin-left: 1rem; /* Расстояние между блоков */
    padding: 10px; /* Поля вокруг текста */
    width: 33.333%; /* Ширина блоков */
   }
   .flex-item:first-child { margin-left: 0; }
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

