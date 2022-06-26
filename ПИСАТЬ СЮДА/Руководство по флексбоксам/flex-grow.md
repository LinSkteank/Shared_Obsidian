Определяет, сколько пространства может занимать флекс внутри контейнера. В качестве значения принимаются числа, они задают пропорции каждого флекса. К примеру, если для всех элементов установлено значение 1, то они получатся равного размера. Если какой-то элемент получил значение 2, то его размер будет в два раза больше остальных.

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию</th>
			<td>0</td>
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

### Значения
Принимаются целые (1, 2, 3,…) или дробные числа (например: 0.6). Отрицательные значения игнорируются.

### Пример
##### code
```html
<!DOCTYPE html> 
<html> 
 <head> 
  <meta charset="utf-8"> 
  <title>flex-grow</title>
  <style>
   form {
    width: 400px;
    margin: auto;
   }
   p {
    display: flex;
   }
   label {
    margin-right: 10px;
   }
   input, select {
    flex-grow: 1;
   }
  </style>
 </head> 
 <body> 
  <form action="handler.php">
   <p>
    <label>Имя:</label>
    <input name="name" id="name">
   </p> 
   <p>
    <label>Какая у вас операционная система?:</label>
    <select name="os">
     <option value="1">Windows</option>
     <option value="2">Linux</option>
     <option value="3">Mac OS</option>
    </select> 
   </p> 
   <p><button>Отправить</button></p>
  </form> 
 </body> 
</html>
```

##### result
<iframe src="http://localhost:50000/flex-grow.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>