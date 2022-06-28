---
type: paper
tags: 📥️/📜️/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство writing-mode 2022-06-28]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2022-06-28]]

# writing-mode
Устанавливает направление текста на странице — по горизонтали или вертикали.

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию </th>
			<td>horizontal-tb</td>
		</tr>
		<tr>
			<th>Наследуется</th>
			<td>Да</td>
		</tr>
		<tr>
			<th>Применяется</th>
			<td>Ко всем элементам, за исключением ячеек и строк таблицы</td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Нет</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
writing-mode: horizontal-tb | vertical-rl | vertical-lr
```

### Значения
__1) horizontal-tb__

Устанавливает направление текста по горизонтали слева направо и сверху вниз.

__2) vertical-rl__

Задаёт направление текста по вертикали сверху вниз и справа налево.

__3) vertical-lr__

Задаёт направление текста по вертикали сверху вниз и слева направо.

### Пример
##### code
```html
<!DOCTYPE html> 
<html> 
 <head> 
  <meta charset="utf-8"> 
  <title>writing-mode</title>
 </head> 
 <body>
  <table>
   <tbody>
    <tr>
     <th>horizontal-tb</th>
     <th>vertical-rl</th>
     <th>vertical-lr</th>
    </tr>
    <tr>
     <td><p style="writing-mode: horizontal-tb">Образец текста</p></td>
     <td><p style="writing-mode: vertical-rl">Образец текста</p></td>
     <td><p style="writing-mode: vertical-lr">Образец текста</p></td>
    </tr>
   </tbody>
  </table>
 </body> 
</html>
```

##### result
<iframe src="http://localhost:50000/writing-mode_example.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>
