Оператор **`typeof`** возвращает строку, указывающую тип операнда.
В таблице приведены возможные возвращаемые значения `typeof`.

<table>
 <thead>
  <tr>
   <th>Type</th>
   <th>Result</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>Undefined</td>
   <td><code>"undefined"</code></td>
  </tr>
  <tr>
   <td>Null</td>
   <td><code>"object" </code>(смотрите ниже)</td>
  </tr>
  <tr>
   <td>Boolean</td>
   <td><code>"boolean"</code></td>
  </tr>
  <tr>
   <td>Number</td>
   <td><code>"number"</code></td>
  </tr>
  <tr>
   <td>String</td>
   <td><code>"string"</code></td>
  </tr>
  <tr>
   <td>Symbol (новый тип из ECMAScript 2015)</td>
   <td><code>"symbol"</code></td>
  </tr>
  <tr>
   <td>Host object (определено JS окружением)</td>
   <td><em>Зависит от реализации</em></td>
  </tr>
  <tr>
   <td>Function object (реализует [[Call]] в терминах ECMA-262)</td>
   <td><code>"function"</code></td>
  </tr>
  <tr>
   <td>Любой другой тип</td>
   <td><code>"object"</code></td>
  </tr>
 </tbody>
</table>

### Синтаксис
```javascript
typeof _operand_
```

### Примеры
```javascript
// Числа
typeof 37 === 'number';
typeof 3.14 === 'number';
typeof(42) === 'number';
typeof Math.LN2 === 'number';
typeof Infinity === 'number';
typeof NaN === 'number'; // несмотря на то, что это "Not-A-Number" (не число)
typeof Number(1) === 'number'; // никогда не используйте эту запись!


// Строки
typeof '' === 'string';
typeof 'bla' === 'string';
typeof '1' === 'string'; // обратите внимание, что число внутри строки всё равно имеет тип строки
typeof (typeof 1) === 'string'; // typeof всегда вернёт в этом случае строку
typeof String('abc') === 'string'; // никогда не используйте эту запись!


// Booleans
typeof true === 'boolean';
typeof false === 'boolean';
typeof Boolean(true) === 'boolean'; // никогда не используйте эту запись!


// Символы
typeof Symbol() === 'symbol'
typeof Symbol('foo') === 'symbol'
typeof Symbol.iterator === 'symbol'


// Undefined
typeof undefined === 'undefined';
typeof declaredButUndefinedVariable === 'undefined';
typeof undeclaredVariable === 'undefined';


// Объекты
typeof {a: 1} === 'object';

// используйте Array.isArray или Object.prototype.toString.call
// чтобы различить обычные объекты и массивы
typeof [1, 2, 4] === 'object';

typeof new Date() === 'object';


// То что ниже приводит к ошибкам и проблемам. Не используйте!
typeof new Boolean(true) === 'object';
typeof new Number(1) === 'object';
typeof new String('abc') === 'object';


// Функции
typeof function() {} === 'function';
typeof class C {} === 'function';
typeof Math.sin === 'function';
```

#### null

```javascript
// Это было определено с рождения JavaScript
typeof null === 'object';
```


#### Использование оператора `new`)

```javascript
// Все функции-конструкторы, созданные с помощью 'new', будут иметь тип 'object'
var str = new String('String');
var num = new Number(100);

typeof str; // Вернёт 'object'
typeof num; // Вернёт 'object'

// Но существует исключение для конструктора Function

var func = new Function();

typeof func; // Вернёт 'function'
```

#### Регулярные выражения

Вызываемые регулярные выражения были нестандартным дополнением в некоторых браузерах.

```javascript
typeof /s/ === 'function'; // Chrome 1-12 Не соответствует ECMAScript 5.1
typeof /s/ === 'object';   // Firefox 5+  Соответствует ECMAScript 5.1
```

#### Исключения

Во всех текущих браузерах существует нестандартный host-объект `document.all`, который имеет тип Undefined.

```javascript
typeof document.all === 'undefined';
```

Хотя спецификация разрешает собственные имена типов для нестандартных экзотических объектов, требуется чтобы эти имена отличались от предопределённых. Ситуация, когда `document.all` имеет тип `undefined` должна рассматриваться как исключительное нарушение правил.