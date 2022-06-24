Применяется для изменения алгоритма расчёта ширины и высоты элемента.

Согласно спецификации CSS ширина блока складывается из ширины содержимого (_width_), значений [[4) margin]], [[2) padding]] и [[3) border]]. Аналогично обстоит и с высотой блока. Свойство box-sizing позволяет изменить этот алгоритм, чтобы свойства width и height задавали размеры не содержимого, а размеры блока.

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию </th>
			<td>content-box</td>
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
			<td>Нет</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
box-sizing: content-box | border-box
```

### Значения
__1) content-box__

Основывается на стандартах CSS, при этом свойства width и height задают ширину и высоту содержимого и не включают в себя значения margin, padding и border.

__2) border-box__

Свойства width и height включают в себя значения padding и border, но не margin.

### Пример
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>box-sizing</title>
  <style>
   .box1 { 
    background: #f0f0f0; /* Цвет фона */
    width: 300px; /* Ширина блока */
    padding: 10px; /* Поля */
    border: 2px solid #000; /* Параметры рамки */
   }
   .box2 { 
    background: #fc0; /* Цвет фона */
    width: 300px; /* Ширина блока */
    padding: 10px; /* Поля */
    margin-top: 10px; /* Отступ сверху */
    border: 2px solid #000; /* Параметры рамки */
    box-sizing: border-box; /* Ширина блока с полями */
   }
  </style>
 </head>
 <body> 
  <div class="box1">Ширина с учетом значения свойства width, полей и границ.</div>
  <div class="box2">Ширина равна значению свойства width.</div>
 </body>
</html>
```
