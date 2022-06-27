---
type: paper
tags: 📥️/📜️/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство text-orientation 2022-06-28]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2022-06-28]]

# text-orientation
Свойство text-orientation устанавливает ориентацию текстовых символов в строке и применяется только к вертикальному тексту (когда свойство [[Свойство writing-mode 2022-06-28|writing-mode]] задано как vertical-lr или vertical-rl).

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию </th>
			<td>mixed</td>
		</tr>
		<tr>
			<th>Наследуется</th>
			<td>Да</td>
		</tr>
		<tr>
			<th>Применяется</th>
			<td>Ко всем элементам, за исключением строк и колонок таблицы</td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Нет</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
text-orientation: mixed | upright
```

### Значения
__1) mixed__

В вертикальном режиме символы разворачиваются на 90° по часовой стрелке.

__2) upright__

В вертикальном режиме символы размещаются естественным путём друг под другом.

### Пример
##### code
```html
<!DOCTYPE html> 
<html> 
 <head> 
  <meta charset="utf-8"> 
  <title>text-orientation</title>
  <style>
   .logo {
    background: #1c59a5; /* Цвет фона */
    color: #fff; /* Цвет текста */
    padding: 10px; /* Поля вокруг текста */
    font-size: 2rem; /* Размер шрифта */
    writing-mode: vertical-lr; /* Вертикальный режим */
    text-orientation: upright; /* Ориентация букв */
   }
  </style>
 </head> 
 <body>
  <div class="logo">WebRef</div>
 </body> 
</html>
```
##### result
<iframe src="http://localhost:50000/text-orientation_example.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>
