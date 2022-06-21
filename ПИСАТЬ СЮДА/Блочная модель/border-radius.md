Устанавливает радиус скругления уголков рамки. Если рамка не задана, то скругление также происходит и с фоном.

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
			 <td>Ко всем элементам, за исключением таблиц с <span class="attribute">border-collapse</span>:&nbsp;<span class="value">collapse</span></td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Да</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
border-radius: <радиус>{1,4} [ / <радиус>{1,4}]
```

### Значения
Разрешается использовать одно, два, три или четыре значения, перечисляя их через пробел. Также допустимо писать два значения через косую черту (/). В качестве значений указываются числа в любом допустимом для CSS формате. В случае применения процентов, отсчёт ведётся относительно ширины блока.

<table>
	<tbody>
		<tr>
			<th>Число значений</th>
			<th>Результат</th>
		</tr>
		<tr>
			<td class="sel">1</td>
			<td align="left">Радиус указывается для всех четырёх уголков.</td>
		</tr>
		<tr>
			<td class="sel">2</td>
			<td align="left">Первое значение задаёт радиус верхнего левого и нижнего правого уголков, второе значение&nbsp;— верхнего правого и нижнего левого  уголков.</td>
		</tr>
		<tr>
			<td class="sel">3</td>
			<td align="left">Первое значение устанавливает радиус для верхнего левого уголка,  второе&nbsp;— одновременно для верхнего правого и нижнего левого уголков, а  третье&nbsp;— для нижнего правого уголка.</td>
		</tr>
		<tr>
			<td class="sel">4</td>
			<td align="left">По очереди устанавливает радиус для верхнего левого, верхнего правого, нижнего правого и нижнего левого уголков.</td>
		</tr>
	</tbody>
</table>

В случае задания двух параметров через косую черту, то первый параметр задаёт радиус по горизонтали, а второй по вертикали (эллиптические уголки).

![[css_border-radius_1.png]]

### Пример
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>border-radius</title>
  <style>
   .radius {
    background: #f0f0f0; /* Цвет фона */
    border: 1px solid black; /* Параметры рамки */
    padding: 15px; /* Поля вокруг текста */
    margin-bottom: 10px; /* Отступ снизу */
   }
  </style>
 </head> 
 <body> 
  <div style="border-radius: 50px 0 0 50px;" class="radius">
   border-radius: 50px 0 0 50px;
  </div>
  <div style="border-radius: 40px 10px" class="radius">
   border-radius: 40px 10px;
  </div>
  <div style="border-radius: 10em/1em;" class="radius">
   border-radius: 13em/3em;
  </div>
  <div style="border-radius: 13em 0.5em/1em 0.5em;" class="radius">
   border-radius: 13em 0.5em/1em 0.5em;
  </div>
  <div style="border-radius: 8px;" class="radius">
   border-radius: 8px;
  </div>
 </body> 
</html>
```

