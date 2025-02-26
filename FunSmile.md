<!-- press F gif -->
<!-- фамилии табличка -->
<!-- орфография -->
<!-- fparsec использовали -->

## 😄 FunSmile: Функциональный язык программирования на основе ASCII смайликов

FunSmile - это экспериментальный функциональный язык программирования, который использует ASCII смайлики в качестве синтаксиса. Цель языка - предоставить забавный способ изучения функционального программирования.

### Основные типы данных

- Логические значения: `Bool` - true
- Целые числа: `Int` - 24
- Вещественные числа: `Float` - 2.7
- Строки: `String` - "улыбнись!\n"
- Списки: `List` - [12, "Abc", 1.234]

### Синтаксис

#### Основы

```
"Hello, FunSmile!"
```

<!-- todo hello world tutorial -->
- Простейшая программа на FunSmile
- `dotnet run test.smile` - команда для запуска кода в файле `test.smile`.
- Библиотека `fparsec` должна скачаться автоматически.

#### Арифметические и логические операции

```
__ :+ 5 3
```

- `:+` - сложение (заклеен рот).
- `:-` - вычитание (только нос).
- `:*` - умножение (поцелуй).
- `:/` - деление (лицо, когда поделил на 0).
- `:@` - присваивание (кусающий рот с языком).
- `B<` - меньше (грустный в очках).
- `B>` - больше (весёлый в очках).
- `B=` - равно (приподнял очки, чтобы лучше разглядеть).
- `>B=` - больше или равно (брови вниз за очками).
- `<B=` - меньше или равно (удивлённые брови за очками).
- `:|` - логическое отрицание (лицо безразличия).
- `>V<` - объединенение списков (краб с клешнями).
- `_` - аппликация (просто нижнее подчёркивание).

#### Лямбда выражения

```
:F x (/>_<)/~o x
```

- `:F` - смайлик объявления лямбда функции.
- `(/>-<)/~o ` - "возвращает" значение из лямбда функции. Смайлик "броска меча в баскетбольное кольцо".

#### Функции

```
(F_F)> add :@
    :F a (/>_<)/~o 
        :F b (/>_<)/~o
            __ :+ a b

__ add 5 3
```

- `(F_F)>` - определение функции. Смайлик "press F to pay respect". За ним имя функции, знак присваивания и лямбда выражение, а затем тело функции.
- `((F_F)>>` - определение рекурсивной функции.

#### Определение "переменных"

```
(F_F)> name = __ :+ 1 1
```

- `(F_F)>` - смайлик объявления, после него знак присваивания и значение "переменной"

#### Условные выражения

```
(?_?) __ B= a 5
(T_T) "a is 5" 
(E_E) "a is not 5"
```

- `(?_?)`- условный оператор, аналог `if` в других языках. Используется вместе с `(T_T)` для `then` и `(E_E)` для `else`.

#### Списки

```
(F_F)> myList :@ [12, "Abc", 1.234]
_ head myList
```

- `head` и `tail` - голова и хвост списка.

#### Стандартная библиотека

```
#include stdlib.smile

_ fact 3
```

- `#include` - подключение нужной библиотеки FunSmile
- `fold`, `map`, `filter` и `fact` - функции стандартной библиотеки FunSmile

#### Функции высших порядков

- `map` - применяет функцию к каждому элементу списка.

```
__ map функция список
__ map fact [1, 2, 3]
```

- `filter` - выбирает элементы списка, удовлетворяющие условию.

```
__ filter _ условие список
__ filter _ B> 3. [1.8, 4.1]
```

#### Примеры функций высших порядков

```
#include stdlib.smile

(F_F)> doubled :@ __ map :F x (/>_<)/~o __ :* x 2 [1, 2, 3]
doubled
```

```
#include stdlib.smile

(F_F)> greater3f :@ __ filter _ B> 3. [1.8, 4.1]
greater3f
```

### Примеры программ

#### Сложение трёх чисел

```
(F_F)> x :@ 10
(F_F)> y :@ 20
(F_F)> result :@ __ :+ x y
result
```

#### Рекурсия и факториал

```
((F_F)>> factorial :@ 
    :F x (/>_<)/~o 
        (F_F)> sub1 :@ 
            :F x (/>_<)/~o __ :- x 1
        (?_?) __ <B= x 1
        (T_T) 1
        (E_E) __ :* x _ fact _ sub1 x

_ factorial 6
```

_или_

```
#include stdlib.smile

_ fact 6
```

#### Частичное применение

```
(F_F)> addFive :@ 
    :F a (/>_<)/~o __ :+ a 5

_ addFive 10
```
