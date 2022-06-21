Универсальное свойство, одновременно устанавливающее цвет, стиль и толщину внешней границы на всех четырёх сторонах элемента. В отличие от линии, задаваемой через [[border]], у свойства outline есть следующие особенности:

-   outline не влияет на размеры и положение самого элемента;
-   outline не занимает место, не влияет на окружающие элементы и отображается поверх них;
-   нельзя задать параметры линии на отдельных сторонах элемента, outline применяется сразу ко всем четырём сторонам;
-   свойство [[border-radius]] не действует.

### Краткая информация
<table>
<tbody>
	<tr>
		<th>Значение по умолчанию </th>
		<td>Нет</td>
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
		<td>Да</td>
	</tr>
</tbody>
</table>

### Синтаксис
```css
outline: outline-color || outline-style || outline-width
```

### Значения
__1) outline-color__

Задаёт цвет линии в любом допустимом для CSS формате.

__2) outline-style__

Стиль линии.

__3) outline-width__

Толщина границы.

### Пример 
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>outline</title>
  <style>
   .photo img {
    padding: 20px; /* Поля вокруг изображения */
    margin-right: 10px; /* Отступ справа */
    margin-bottom: 10px; /* Отступ снизу */
    outline: 1px solid #666; /* Параметры рамки */
    background: #f0f0f0; /* Цвет фона */
    float: left; /* Обтекание по правому краю */
   }
  </style>
 </head> 
 <body> 
  <div class="photo">
   <img src="image/girl.jpg" alt="Девочка с муфтой">
   <img src="image/owl.jpg" alt="Сова">
   <img src="image/boy.jpg" alt="Эвенкийский мальчик">
  </div>
 </body>
</html>
```
