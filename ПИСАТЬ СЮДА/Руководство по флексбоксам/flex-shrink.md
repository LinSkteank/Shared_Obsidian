Устанавливает коэффициент сжатия флексов в контейнере и задаёт, насколько элемент будет уменьшаться по отношению к другим флексам, чтобы разместить все элементы в одну строку.

<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию</th>
			<td>1</td>
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
flex-shrink: <число>
```

### Значения
Принимаются целые (1, 2, 3,…) или дробные числа (например: 0.6). Отрицательные значения игнорируются.

### Пример
##### code
```html
<!DOCTYPE html> 
<html> 
 <head> 
  <meta charset="utf-8"> 
  <title>flex-shrink</title>
  <style>
   .flex-container {
    display: flex;
   }
   .flex1 {
    flex-shrink: 3;
    margin-right: 2rem;
   }
   .flex1 img {
    width: 100%;
   }
   .flex2 {
    flex-shrink: 2;
   }
  </style>
 </head> 
 <body> 
  <div class="flex-container">
   <div class="flex-item flex1"><img src="image/aquaria.jpg" alt=""></div>
   <div class="flex-item flex2">Понравились готовые инсталляции, некоторые 
    даже без рыбок смотрятся так, что хочется фотографию на рабочий 
    стол поставить и любоваться.</div>
  </div>
 </body> 
</html>
```

##### result
<iframe src="http://localhost:50000/flex-shrink.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>