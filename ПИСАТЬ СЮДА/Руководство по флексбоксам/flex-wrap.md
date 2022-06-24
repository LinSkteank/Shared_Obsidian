Указывает, следует ли флексам располагаться в одну строку или можно занять несколько строк. Если перенос строк допускается, то свойство также позволяет контролировать направление, в котором выкладываются строки.

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию</th>
			<td>nowrap</td>
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
flex-wrap: nowrap | wrap | wrap-reverse
```

### Значения
__1) nowrap__

Флексы выстраиваются в одну линию.

__2) wrap__

Флексы выстраиваются в несколько строк, их направление задаётся свойством [[flex-direction]].

__3) wrap-reverse__

Флексы выстраиваются в несколько строк, в направлении, противоположном flex-direction.

### Пример
```html
<!DOCTYPE html> 
<html> 
 <head> 
  <meta charset="utf-8"> 
  <title>flex-wrap</title>
  <style>
   .flex-container {
    padding: 0;
    margin: 0;
    list-style: none;
    display: flex;
    flex-wrap: wrap;
   }
   .flex-item {
    padding: 20px;
    background: #f0f0f0;
    border-radius: 5px;
    margin: 1rem;
    text-align: center; 
   }
  </style>
 </head> 
 <body> 
  <ul class="flex-container">
   <li class="flex-item"><img src="image/aquaria1.jpg" alt=""></li>
   <li class="flex-item"><img src="image/aquaria2.jpg" alt=""></li>
   <li class="flex-item"><img src="image/aquaria3.jpg" alt=""></li>
  </ul>
 </body> 
</html>
```
