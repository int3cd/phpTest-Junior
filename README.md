# Тестовое задание: Junior PHP Developer

Привет, %username%!

Что с этим всем делать? - Решать)  
Варианты ответы и код нужно потом отправить нам на почту.

### Легкие задания:
1. Какого оператора в PHP не существует?  
A) !==  
B) +=  
C) !===  
D) >=  

---

2. Каков результат выполнения у данного скрипта:

```php
<?
$x = 5;
echo 'Переменная $x = 5';
```

A) Переменная 5 = 5  
B) Переменная х = 5  
C) Ошибка синтаксиса  
D) Переменная $х = 5  

---

3 . Каков результат выполнения у данного скрипта: 

```php
<?
$myArray = [1, 2, 3, 4, 5];
foreach ($myArray as $value); echo $value;
echo 'end';
```

A) end  
B) 12345end  
C) Другой ответ  
D) Ошибка синтаксиса  

---

4. Каков результат выполнения у данного скрипта:

```php
<?
$s = 2

switch ($s) {
    case 1:
        echo 1;
    case 2:
        echo 2;
    case 3
        echo 3;
    default:
        echo 'default';
}
```

A) 2  
B) 23  
C) 23default  
D) 123default  

---

5. Что будет, если запустить такой скрипт:

```php
<?
echo null == 0 ? 'true' : 'false';
```

A) false  
B) Ошибка, поскольку null нельзя сравнивать с 0  
C) true  
D) Ошибка, поскольку null в PHP нет  

---

6. Что будет отображаться, после запуска скрипта?

```php
<?
for ($i = 0; $i < 5; $i++) {
    if ($i % 2 == 0) continue;
    echo $i;
}
```

A) 013  
B) 24  
C) 024  
D) 13  

---

7. Что выведет данный код:

```php
<?
$items = [
    'key1' => 'value1',
    'key2' => 'value2',
];

foreach ($items as $key => $value) {
    if ((int) $value == 0) echo $key . '...';
}
```

A) key1...key2...  
B) ничего  
C) value1...value2...  
D) 1…2...  

---

8. Как сделать редирект (например, на google.ru) на PHP?  
A) location.href = http://google.ru  
B) header("Redirect: http://google.ru")  
C) document.location = "http://google.ru  
D) header("Location: http://google.ru")  

---

9. Каков будет результат выполнения скрипта?

```php
<?
function myFunc(x = 0) 
{
    echo $x;
}

myFunc();
myFunc(5);
```

A) 0  
B) Ошибка, поскольку параметрам в функции нельзя присваивать значения  
C) 05  
D) 5  

---

10. Как в PHP правильно присвоить переменной строку?  
A) a = 'строка';  
B) $a == 'строка';  
C) $a = 'строка';  
D) a = строка;  
E) $a = строка;  

---

11. Какая из приведенных ниже функций добавляет один или несколько элементов в начало массива?  
A) array_unshift();  
B) array_flip();  
C) array_intersect();  
D) array_push();  

---

12. Какой будет результат работы кода:

```php
<?
var_dump(in_array('test', [0, 1]));
```

A) bool(true)  
B) 0  
C) 1  
D) false  
E) test  
F) bool(false)  
G) true  

---

13. Перечислите, какие варианты из этих конструкций выведут «123»?

```php
<?
$line = '321123';
echo substr($line, strlen($line) / 2, strlen($line) - strlen('123')); // Вариант 1
echo substr($line, -3); // Вариант 2
echo strrev(str_replace('123', '', $line)); // Вариант 3
echo $line[3] . $line[4] . $line[0]; // Вариант 4
```

---

14. Какой будет результат кода:

```php
<?
$items = [
    ['sort' => 1],
    ['sort' => 3],
    ['sort' => 5],
    ['name' => 'item 1'],
    [
        ['sort' => 8],
        ['sort' => 10],
    ]
];

$sum = 0;
foreach ($items as $item) $sum += $item['sort'];
echo $sum;
```

A) 0  
B) 9  
C) 10  
D) 28  
E) Ошибка выполнения  

---

15. Где допущены ошибки?

```php
class Coffe
{
    public static function init($count = 0)
    {
        $result = self::getLong($count);
        return $result;
    }
	
    private static function getLong ($count = 0)
    {
        $str = $count . ' чашек';
    }
}

echo Coffe::getLong(5);
```

### Задания посложнее:
#### Задача. Array structuring:
Небходимо придумать удобную структуру результирующего массива, с помощью которого можно решить следующую задачу.
В системе (программе или базе данных) есть авторы и книги, у каждой книги только один автор.
Создайте массив, в котором будет не менее 3-х авторов и не менее 5-ти книг.
Необходимо вывести информацию по всем авторам, на каждой строке : имя Автора – его email – год рождения.
Затем необходимо вывести информацию по книгам, на каждой строке: Название книги – Имя автора - год выпуска книги.

##### Например:
Николай Васильевич – gogol@gogol.ru - 1809  
Пушкин – alexandr@sergeevich.ru - 1799  
Мертвые души – Николай Васильевич - 1841  
Вий – Николая Васильевич - 1834  
Пиковая дама - Пушкин - 1833  

---

#### Задача. Like a fizz buzz:
Реализовать функцию checkBraces($str), проверяющую на синтаксическую верность последовательность скобок

1. Необходимо учитывать вложенность
2. Обратите внимание на производительность вашего решения
3. В случае ошибки возвращаем false, в противном случае true
4. Минимальный набор тестов:

```
checkBraces('---(++++)----') === true
checkBraces('') -> true
checkBraces('before ( middle []) after ') === true
checkBraces(') (') === false
checkBraces('} {') === false
checkBraces('<(   >)') === false
checkBraces('(  [  <>  ()  ]  <>  )') === true
checkBraces('   (      [)') === false
```
