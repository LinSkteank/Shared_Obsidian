Псевдоэлемент ::before применяется для отображения контента до содержимого элемента, к которому он добавляется. Работает совместно со свойством [[content]].

По умолчанию _::before_ создаёт строчный элемент.

### Синитаксис 
```html
Селектор::before { content: "текст" }
```

### Пример 
```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>before</title>
  <style>
   li::before {
     content: "¶ "; /* Добавляем желаемый символ перед элементом списка */ 
   }
   li {
     list-style: none; /* Убираем исходные маркеры */ 
   }
  </style>
 </head>
 <body>
   <ul>
     <li>Альфа</li>
     <li>Бета</li>
     <li>Гамма</li>
   </ul>
 </body>
</html>
```