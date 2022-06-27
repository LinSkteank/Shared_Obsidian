---
type: paper
tags: 📥️/📜️/💻/🕸/🪟
aliases:
  - 
cssclass: 
---



# Title: **[[Свойство justify-content 2022-06-27]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2022-06-27]]

# justify-content

Определяет, как браузер распределяет пространство вокруг флекс-элементов вдоль главной оси контейнера. Это делается после того, как применяются размеры и автоматические отступы, за исключением ситуации, когда по крайней мере у одного элемента [[Свойство flex-grow 2022-06-27|flex-grow]] больше нуля. При этом не остаётся никакого свободного пространства для манипулирования.

### Краткая информация
<table>
	<tbody>
		<tr>
			<th>Значение по умолчанию</th>
			<td>flex-start</td>
		</tr>
		<tr>
			<th>Наследуется</th>
			<td>Нет</td>
		</tr>
		<tr>
			<th>Применяется</th>
			<td>К флекс-контейнерам</td>
		</tr>
		<tr>
			<th>Анимируется</th>
			<td>Нет</td>
		</tr>
	</tbody>
</table>

### Синтаксис
```css
justify-content: flex-start | flex-end | center | space-between | 
                 space-around | space-evenly
```

### Значения
__1) flex-start__

Флексы прижаты к началу строки.

__2) flex-end__

Флексы прижаты к концу строки.

__3) center__

Флексы выравниваются по центру строки.

__4) space-between__

Флексы равномерно распределяются по всей строке. Первый и последний элемент прижимаются к соответствующим краям контейнера.

__5) space-around__

Флексы равномерно распределяются по всей строке. Пустое пространство перед первым и после последнего элементов равно половине пространства между двумя соседними элементами.

__6) space-evenly__

Флексы распределяются так, что расстояние между любыми двумя соседними элементами, а также перед первым и после последнего, было одинаковым.

### Пример
##### code
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>justify-content</title>
  <style>
   section {
    display: flex;
    margin-bottom: 10px;
   }
   section > div { 
    border: 1px solid #ccc;
    width: 100px;
    height: 100px;
    background: repeating-radial-gradient(circle at 50% 50%, #fff, #fff 25px, #f96 25px, #f96 50px);
   }
   .flex-start {
    justify-content: flex-start;
   }
   .flex-end {
    justify-content: flex-end;
   }
   .center {
    justify-content: center;
   }
   .space-between {
    justify-content: space-between;
   }
   .space-around {
    justify-content: space-around;
   }
  </style>
 </head>
 <body>
  <section class="flex-start">
   <div></div><div></div><div></div>
  </section>
  <section class="flex-end">
   <div></div><div></div><div></div>
  </section>
  <section class="center">
   <div></div><div></div><div></div>
  </section>
  <section class="space-between">
   <div></div><div></div><div></div>
  </section>
  <section class="space-around">
   <div></div><div></div><div></div>
  </section>
 </body>
</html>
```

##### result
<iframe src="http://localhost:50000/justify-content.html" style="background: white; border: none; width: 500px; height: 500px;"/></iframe>


