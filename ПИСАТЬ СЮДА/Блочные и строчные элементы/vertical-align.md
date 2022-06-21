Выравнивает элемент по вертикали относительно своего родителя, окружающего текста или ячейки таблицы.

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию </th>
			<td>baseline</td>
		</tr>
		<tr>
			<th>Наследуется</th>
			<td>Нет</td>
		</tr>
		<tr>
			<th>Применяется</th>
			<td>К строчным элементам или ячейкам таблицы</td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Да</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
vertical-align: baseline|bottom|middle|sub|super|text-bottom|text-top|top| 
  <размер> | <проценты>
```

### Значения
<table>
	<tbody>
		<tr>
			<th>Значение</th>
			<th>Описание</th>
			<th style="min-width: 200px;">Вид</th>
		</tr>
		<tr>
			<td class="value">baseline</td>
			<td>Выравнивает базовую линию блока по базовой линии родителя. Если у блока нет базовой линии, то за неё принимается нижняя граница. 
       </td>
			<td><img src="/assets/images/html/chrome_option.png" alt="" style="vertical-align: baseline;"> <span style="font-size: 20px; vertical-align: baseline;">Заголовок</span> <span style="vertical-align: baseline;">Текст</span></td>
		</tr>
		<tr>
			<td class="value">bottom</td>
			<td>Выравнивает низ блока по нижней части строки.</td>
			<td><img src="/assets/images/html/chrome_option.png" alt="" style="vertical-align: bottom;"> <span style="font-size: 20px; vertical-align: bottom;">Заголовок</span> <span style="vertical-align: bottom;">Текст</span></td>
		</tr>
		<tr>
			<td class="value">middle</td>
			<td>Выравнивает вертикальную среднюю точку блока по базовой линии родительского блока плюс половина высоты буквы «x».</td>
			<td><img src="/assets/images/html/chrome_option.png" alt="" style="vertical-align: middle;"> <span style="font-size: 20px; vertical-align: middle;">Заголовок</span> <span style="vertical-align: middle;">Текст</span></td>
		</tr>
		<tr>
			<td class="value">sub</td>
			<td>Опускает базовую линию блока вниз для создания нижнего индекса. Не оказывает влияние на размер текста.</td>
			<td><span style="font-size: 20px;">Заголовок</span> <span style="vertical-align: sub;">Текст</span></td>
		</tr>
		<tr>
			<td class="value">super</td>
			<td>Поднимает базовую линию блока вверх для создания верхнего индекса. Не оказывает влияние на размер текста.</td>
			<td><span style="font-size: 20px;">Заголовок</span> <span style="vertical-align: super;">Текст</span></td>
		</tr>
		<tr>
			<td class="value">text-bottom</td>
			<td>Нижняя граница элемента выравнивается по нижнему краю содержимого родителя.</td>
			<td><img src="/assets/images/html/chrome_option.png" alt="" style="vertical-align: text-bottom;"> <span style="font-size: 20px; vertical-align: middle;">Заголовок</span> <span style="vertical-align: middle;">Текст</span></td>
		</tr>
		<tr>
			<td class="value">text-top</td>
			<td>Верхняя граница элемента выравнивается по верхнему краю содержимого родителя.</td>
			<td><img src="/assets/images/html/chrome_option.png" alt="" style="vertical-align: text-top;"> <span style="font-size: 20px; vertical-align: text-top;">Заголовок</span> <span style="vertical-align: text-top;">Текст</span></td>
		</tr>
		<tr>
			<td class="value">top</td>
			<td>Выравнивает верх блока по верхней части строки.</td>
			<td><img src="/assets/images/html/chrome_option.png" alt="" style="vertical-align: top;"> <span style="font-size: 20px; vertical-align: top;">Заголовок</span> <span style="vertical-align: top;">Текст</span></td>
		</tr>
	</tbody>
</table>

В качестве значения также можно использовать проценты, пиксели или другие доступные единицы. Положительное число смещает элемент вверх относительно базовой линии, в то время как отрицательное число опускает его вниз. При использовании процентов, отсчёт ведётся от значения свойства _line-height_, при этом 0% аналогично значению baseline.

Для выравнивания по вертикали в ячейках таблицы применяются следующие значения.

__1) baseline__

Выравнивает базовую линию ячейки с базовой линией первой текстовой строки или другого вложенного элемента.

__2) bottom__

Выравнивает по нижнему краю ячейки.

__3) middle__

Выравнивает по середине ячейки.

__4) top__

Выравнивает содержимое ячейки по её верхнему краю.

### Пример
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>vertical-align</title>
  <style>
  .tex { font-size: 2rem; }
  .tex sub {
   vertical-align: sub;
   font-size: 1.8rem;
  }
  .tex sup {
   vertical-align: 5px; 
   font-size: 1.6rem;
  } 
  </style>
 </head>
 <body>
  <div class="tex">
  T<sub>E</sub>X и L<sup>A</sup>T<sub>E</sub>X
  </div>
 </body>
</html>
```
