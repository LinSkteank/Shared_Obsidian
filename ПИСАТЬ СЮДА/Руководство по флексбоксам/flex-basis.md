Свойство flex-basis определяет основу флекса, которая является начальным размером элемента. Похоже на свойства width и height, к которым добавляется содержимое элемента.

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
			<td>К флекс-элементам </td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Да</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
flex-basis: auto | <размер>
```

### Значения
__1) auto__

Указывает автоматический размер, основанный на содержимом элемента.

__2) <размер>__

Задаёт размер элемента в px, mm, pt или в процентах вдоль главной оси. При этом размер вычисляется относительно родителя. Отрицательное значение недопустимо.

### Пример
##### code
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>flex-basis</title>
  <style>
   .flex-container {
    display: flex; /* Флексы */
    height: 300px; /* Высота */
    color: #fff; /* Белый цвет текста */
    font-size: 2.6em; /* Размер шрифта */
    flex-flow: column wrap; /* Располагаем в виде колонок */
   }
   .flex-item {
    display: flex; /* Флексы */
    align-items: center; /* Выравнивание текста по вертикали */
    justify-content: center; /* Выравнивание текста по горизонтали */
   }
   .one {
    background: #508694; /* Цвет фона */
    margin-right: 10px; /* Отступ справа */
    flex-basis: 100%;
    order: 1; /* Первый блок */
   }
   .two {
    background: #BB844C; /* Цвет фона */
    margin-bottom: 10px; /* Отступ снизу */
    flex: 1 1 0;
    order: 2; /* Второй блок */
   }
   .three {
    background: #929D79; /* Цвет фона */
    flex: 1 1 0;
    order: 3; /* Третий блок */
   }
  </style>
 </head>
 <body>
  <div class="flex-container">
   <div class="flex-item one">Первый</div>
   <div class="flex-item two">Второй</div>
   <div class="flex-item three">Третий</div>
  </div>
 </body>
</html>
```

##### result
<iframe src="http://localhost:50000/flex-basis.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>
