Сокращённое свойство, которое позволяет указать параметры элемента, чтобы он эффективно заполнял доступное пространство. Элементы могут быть растянуты пропорционально с учётом заданного соотношения или сжаты, чтобы целиком вместить все элементы без переносов в одну строку.

### Краткая информация

<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию</th>
			<td>flex-grow: 0<br>flex-shrink: 1<br>flex-basis: auto</td>
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
flex: none | [ flex-grow flex-shrink? || flex-basis ]
```

### Значения

__none__

Соответствует значению 0 0 auto.

### Пример
##### code
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>flex</title>
  <style>
   body {
    margin: 0; /* Убираем отступы */
    display: flex; /* Включаем флексы */
    height: 100vh; /* Занимает всю высоту */
    flex-direction: column; /* Главная ось располагается вертикально */
   }
   main {
    flex: 1; /* Соответствует flex: 1 1 0% */
   }
   footer {
    background: #e4efc7; /* Цвет фона */
    padding: 10px; /* Поля вокруг текста */
   }
  </style>
 </head> 
 <body> 
  <main>
  </main>
  <footer>Подвал</footer>
 </body> 
</html>
```

##### result
<iframe src="http://localhost:50000/flex_original.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>
