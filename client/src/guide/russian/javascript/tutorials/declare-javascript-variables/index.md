---
title: Declare Variables
localeTitle: Объявлять переменные
---
# Объявлять переменные

Объявления переменных JavaScript могут быть отсортированы по трем различным компонентам: тип переменной, имя переменной и значение переменной.

```js
    var myName = "Rafael"; 
```

Давайте разложим вышеприведенную строку кода на части, которые составляют:

```js
    var/const/let 
```

Переменные JavaScript могут иметь три типа объявлений: var, const и let. Переменные типа Var являются глобальными, если объявлены вне функции, к которой они могут быть доступны любым JS-файлом (или консолью), и если они созданы внутри функции, они доступны независимо от области блока. Переменные типа Let-type ограничены в своем блоке. См. Пример ниже для разницы.

```js
     function varTest() { 
      var x = 1; 
      if (true) { 
        var x = 2;  // same variable! 
        console.log(x);  // 2 
      } 
      console.log(x);  // 2 
    } 
 
    function letTest() { 
      let x = 1; 
      if (true) { 
        let x = 2;  // different variable 
        console.log(x);  // 2 
      } 
      console.log(x);  // 1 
    } 
```

Константные переменные имеют ту же область действия, что и переменные let (масштаб блока), но неизменяемы. Независимо от значения, которое должна быть назначена переменная const-типа, должно произойти, когда объявлена ​​переменная, а JavaScript будет вызывать ошибку, если переменная будет изменена позже.

```js
    const genre = "non-fiction"; 
    console.log(genre); // "non-fiction"; 
    genre = "fantasy"; // error 
```

Теперь, когда мы можем определить тип переменной, давайте посмотрим на это имя. Имена переменных JavaScript написаны в формате `camel case` . Примером случая с верблюдом является: `camelCase` . В контексте нашего примера:

```js
    myName 
```

Имя также мы снова получим эту переменную:

```js
    console.log(myName); // "Rafael" 
```

Наконец, наше значение:

```js
    "Rafael" 
```

JavaScript динамически типизирован, что означает, что любая заданная переменная может представлять любой заданный тип данных в любой момент времени. Например:

```js
    var example = "This is an example"; 
    example = [0, 1, 2, 3] 
    example = {test: "Result"} 
    example = 5 
```

Все эти утверждения совершенно верны - переменные JavaScript могут переходить от строки к массиву к объекту с целым числом.

### Объявить объект как const

Как уже упоминалось выше, константная переменная является неизменной, значение, присвоенное такой переменной во время объявления, не может быть обновлено, но есть смысл отметить в случае объявления объекта с константой. Объект типа const также не может обновляться после определения, но свойства объекта cab be. Например.

```js
    const Car1 = { 
        name: 'BMW', 
        model: 'X1', 
        color: 'black' 
    } 
```

Здесь мы не можем обновить объект, но мы можем обновить свойства, обратившись через оператор dot (.), Как показано ниже.

```js
    Car1.color = 'Red'; 
    console.log(Car1); 
    O/P - {name: "BMW", model: "X1", color: "Red"} 
```

Если нам нужно сделать объект enitre неизменным (включая свойства), тогда мы должны использовать метод замораживания.