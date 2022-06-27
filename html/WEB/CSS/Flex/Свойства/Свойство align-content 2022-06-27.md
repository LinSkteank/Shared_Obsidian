---
type: paper
tags: 📥️/📜️/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство align-content 2022-06-27]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2022-06-27]]

# align-content

Задаёт тип выравнивания строк внутри флекс-контейнера по поперечной оси при наличии свободного пространства. ^c42b0a

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию</th>
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
align-content: flex-start | flex-end | center | 
  space-between | space-around | space-evenly | stretch
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
			<td><img src="https://webref.ru/assets/images/css/align-content/flex-start.png" alt="flex-start" width="230" height="180"></td>
			<td>Строки располагаются в начале поперечной оси. Каждая следующая строка идёт вровень с предыдущей.</td>
		</tr>
		<tr>
			<td>center</td>
			<td><img src="https://webref.ru/assets/images/css/align-content/flex-center.png" alt="center" width="230" height="180"></td>
			<td>Строки располагаются по центру контейнера.</td>
		</tr>
		<tr>
			<td>flex-end</td>
			<td><img src="https://webref.ru/assets/images/css/align-content/flex-end.png" alt="flex-end" width="230" height="180"></td>
			<td>Строки располагаются начиная с конца поперечной оси. Каждая предыдущая строка идёт вровень со следующей.</td>
		</tr>
		<tr>
			<td>space-between</td>
			<td>
				<img src="https://webref.ru/assets/images/css/align-content/space-between.png" alt="space-between" width="230" height="180"></td>
			<td>Строки равномерно распределяются в контейнере и расстояние между ними одинаково.</td>
		</tr>
		<tr>
			<td>space-around</td>
			<td><img src="https://webref.ru/assets/images/css/align-content/space-around.png" alt="space-around"></td>
			<td>Строки равномерно распределяются таким образом, чтобы пространство между двумя соседними строками было одинаковым. Пустое пространство перед первой строкой и после последней строки равно половине пространства между двумя соседними строками.</td>
		</tr>
		<tr>
			<td>space-evenly</td>
			<td><img src="https://webref.ru/assets/images/css/align-content/space-evenly.png" alt="space-evenly"></td>
			<td>Строки равномерно распределяются таким образом, чтобы пространство между двумя соседними строками, а также пространство перед первой строкой и после последней строки было одинаковым.</td>
		</tr>
		<tr>
			<td>stretch</td>
			<td><img src="https://webref.ru/assets/images/css/align-content/stretch.png" alt="stretch" width="230" height="180"></td>
			<td>Строки равномерно растягиваются, заполняя свободное пространство. </td>
		</tr>
	</tbody>
</table>

### Пример
##### code
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>align-content</title>
  <style>
   .flex-container {
    width: 70px;
    height: 240px;
    border: 1px solid #333;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    align-content: center;
   }
   .flex-container div {
    width: 70px; height: 70px;
    border-radius: 50%;
   }
   .red { background: red; }
   .yellow { background: yellow; }
   .green { background: green; }
  </style>
 </head>
 <body> 
  <div class="flex-container">
   <div class="red"></div>
   <div class="yellow"></div>
   <div class="green"></div>
  </div>
 </body>
```

##### result
<iframe src="http://localhost:50000/align-content.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>
