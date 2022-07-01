---
type: paper
tags: 📥️/📜️/🔱
aliases:
cssclass: 
---

- `Links:` [link](https://ru.stackoverflow.com/questions/435546/%D0%A7%D1%82%D0%BE-%D0%B7%D0%BD%D0%B0%D1%87%D0%B8%D1%82-use-strict#:~:text=%22use%20strict%22%3B%20(%D0%BF%D0%B5%D1%80%D0%B5%D0%B2%D0%BE%D0%B4,%D0%B8%20%D0%BC%D0%BB%D0%B0%D0%B4%D1%88%D0%B5)%20%D0%B5%D0%B3%D0%BE%20%D0%BD%D0%B5%20%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%B8%D0%B2%D0%B0%D1%8E%D1%82)
- `Type:` [[&]]
- `Reviewed Date:` [[2022-01-16]]
# Title: **[[js mode strict 2022-01-16]]**


`"use strict";` (перевод: «использовать строгий») - это установка, которая заставляет код обрабатываться в _строгом режиме_. Без этой установки код обрабатывается в _неограниченном режиме_.

Строгий режим был введён в ECMAScript 5, и старые браузеры ([IE9 и младше](http://caniuse.com/#feat=use-strict)) его не поддерживают. То есть, не обращают внимания на установку по умолчанию и всё обрабатывается в неограниченном режиме.

## Зачем использовать "use strict";?

В строгом режиме:

-   некоторые ошибки можно найти быстрее,
-   более опасные и не полезные черты JavaScript либо запрещены, либо приводят к ошибке.

## Как использовать "use strict";?

Чтобы включить строгий режим в целом скрипте, надо поставить установку `"use strict";` или `'use strict';` в начало скрипта.

```javascript
"use strict";
// код здесь обрабатывается в строгом режиме
```

Чтобы включить строгий режим в функции, надо поставить установку в начало кода функции.

```javascript
// код здесь обрабатывается в неограниченном режиме
function f() {
  "use strict";
  // код здесь обрабатывается в строгом режиме
}
// код здесь обрабатывается в неограниченном режиме
```

## В чём различие между строгим режимом и неограниченным режимом?

В строгом режиме:

-   **нельзя присваивать значение в неопределённую переменную** (спецификация [§11.13.1](http://es5.javascript.ru/x11.html#x11.13.1)). В неограниченном режиме создается глобальная переменная.
    
    ```javascript
    (function() {
      "use strict";
      x = 5; // ReferenceError: x is not defined
    })(); 
    
    x = 5; // Создает глобальную переменную x
    ```
    
    Также нельзя присваивать значение в свойство данных только для чтения.
    
    ```javascript
    (function() {
      "use strict";
      window.undefined = 5; // TypeError: Cannot assign to read only
    })();                   // property 'undefined' of [object Object]
    
    window.undefined = 5; // Ничего не делает
    ```
    
-   **нельзя использовать инструкцию `with`** (спецификация [§12.10](http://es5.javascript.ru/x12.html#x12.10)).
    
    ```javascript
    (function() {
      "use strict";
      with(Object) {} // SyntaxError: Strict mode code may not include a with statement
    })();
    ```
    
-   **в ES5 нельзя определить повторные свойства в литерале объекта** (спецификация [§11.1.5](http://es5.javascript.ru/x11.html#x11.1.5)).
    
    ```javascript
    (function() {
      "use strict";
      var x = {
        a: 1,
        a: 2
      };  // SyntaxError: Duplicate data property in object literal 
    })(); // not allowed in strict mode
    
    var x = {
      a: 1,
      a: 2
    }; // x равно {a: 2} 
    ```
    
-   **нельзя определить повторные формальные параметры функции** (спецификация [§13.1](http://es5.javascript.ru/x13.html#x13.1), [§15.3.2](http://es5.javascript.ru/x15.3.html#x15.3.2)).
    
    ```javascript
    function f(a, a) {
      "use strict";
    } // SyntaxError: Strict mode function may not have duplicate parameter names
    
    function f(a, a) {
      return a;
    }
    f(1,2); // возвращает 2
    ```
    
-   **изменения объекта `arguments` не изменяют аргументы** (спецификация [§10.6](http://es5.javascript.ru/x10.html#x10.6)).
    
    ```javascript
    function f(x) {
      "use strict";
      arguments[0] = 5;
      return x;
    }
    f(10); // возвращает 10
    
    function f(x) {
      arguments[0] = 5;
      return x;
    }
    f(10); // возвращает 5
    ```
    
-   **`delete` приводит к ошибке, если аргумент - не изменяемое свойство объекта** (спецификация [§11.4.1](http://es5.javascript.ru/x11.html#x11.4.1)).
    
    ```javascript
    (function f(x) {
      "use strict";
      var y = 4;
      delete f; // SyntaxError: Delete of an unqualified identifier in strict mode.
      delete x; // SyntaxError: Delete of an unqualified identifier in strict mode.
      delete y; // SyntaxError: Delete of an unqualified identifier in strict mode.
      delete window.undefined; // TypeError: Cannot delete property 
    })();                      // 'undefined' of [object Object]
    
    (function f(x) {
      var y = 4;
      delete f; // Возвращает false
      delete x; // Возвращает false
      delete y; // Возвращает false
      delete window.undefined; // Возвращает false
    })();
    ```
    
-   **`eval` не может инстанциировать переменные и функции в контексте вызова** (спецификация [§10.4.2](http://es5.javascript.ru/x10.html#x10.4.2)).
    
    ```javascript
    (function () {
      "use strict";
      eval("var x = 5");
      return x; // ReferenceError: x is not defined
    })();
    
    (function () {
      eval("var x = 5");
      return x;
    })(); // Возвращает 5
    ```
    
-   **`this` не преобразуется в объект**, а **если значение `this` - `undefined` или `null`, то не преобразуется в глобальный объект** (спецификация [§10.4.3](http://es5.javascript.ru/x10.html#x10.4.3)).
    
    ```javascript
    function f() {
      "use strict";
      return this;
    };
    f.call(4); // возвращает 4
    f.call(null); // возвращает null
    f.call(undefined); // возвращает undefined
    
    function f() {
      return this;
    };
    f.call(4); // возвращает [object Number]
    f.call(null); // возвращает [object global]
    f.call(undefined); // возвращает [object global]
    ```
    
-   **`eval` и `arguments` - нельзя изменить или использовать в качестве имени** (спецификация [§11.4.4](http://es5.javascript.ru/x11.html#x11.4.4), [§11.4.5](http://es5.javascript.ru/x11.html#x11.4.5), [§11.13](http://es5.javascript.ru/x11.html#x11.13), [§12.2.1](http://es5.javascript.ru/x12.html#x12.2.1), [§12.10](http://es5.javascript.ru/x12.html#x12.10), [§12.14.1](http://es5.javascript.ru/x12.html#x12.14.1), [§13.1](http://es5.javascript.ru/x13.html#x13.1)).
    
    ```javascript
    function eval(arguments) {     // SyntaxError: Unexpected eval or arguments in strict mode
      "use strict";
      eval = "5";                  // SyntaxError: Unexpected eval or arguments in strict mode
      ++eval;                      // SyntaxError: Unexpected eval or arguments in strict mode
      arguments++;                 // SyntaxError: Unexpected eval or arguments in strict mode
      try {
        var arguments = 5;         // SyntaxError: Unexpected eval or arguments in strict mode
      } catch(eval) {}             // SyntaxError: Unexpected eval or arguments in strict mode
      return arguments.eval;
    }
    
    function eval(arguments) {
      eval = "5";
      ++eval;
      arguments++;
      try {
        var arguments = 5;
      } catch(eval) {}
      return arguments.eval;
    }
    eval(); // возвращает 5
    ```
    
-   **нельзя использовать `argument.caller` и `arguments.callee`** (спецификация [§13.2](http://es5.javascript.ru/x13.html#x13.2)).
    
    ```javascript
    (function f() {
      "use strict";
      arguments.caller; // TypeError: 'caller', 'callee', and 'arguments' properties may not be accessed on strict mode functions or the arguments objects for calls to them
      arguments.callee; // TypeError: 'caller', 'callee', and 'arguments' properties may not be accessed on strict mode functions or the arguments objects for calls to them
      f.arguments;      // TypeError: 'caller', 'callee', and 'arguments' properties may not be accessed on strict mode functions or the arguments objects for calls to them
    })();
    ```
    
-   **больше слов, зарезервированных для использования в будущем** (спецификация [§7.6.1.2](http://es5.javascript.ru/x7.html#x7.6.1.2)).
    
    ```javascript
    (function () {
      "use strict";
      var implements, let, private, public, yield, interface, package, protected, static;
    })(); // SyntaxError: Unexpected strict mode reserved word
    ```
    
-   **нельзя использовать литералы восьмеричной СС** (спецификация [B.1.1](http://es5.javascript.ru/B.html#B.1.1), [B.1.2](http://es5.javascript.ru/B.html#B.1.2)).
    
    ```javascript
    (function () {
      "use strict";
      return 010 + // SyntaxError: Octal literals are not allowed in strict mode.
        "\077";    // SyntaxError: Octal literals are not allowed in strict mode.
    })();
    
    (function () {
      return 010 + "\077";
    })(); // возвращает "8?"
    ```