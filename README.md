# Japy
Japy - проект, ставящий цель унифицировать и упростить языки программирования, которые существуют сейчас, а также уменьшить к минимуму присутствие языков хотя бы на уровне основных структур.  

## Структура данного языка программирования:
### Операции с числами
+, -, /, *;  
% - Остаток от деления;  
^ - Возведение в степень;  
!^ - Корень;  
!! - Не;  
!+ - минус и т.д.  
^^^ - Тетрация;  
!^^^ - Обратное от тетрации;  
### Условные конструкции
Для сравнения равенств будет использовано ==.  
if, else, switch/case не будет.  
Будут &&, ||  
a==8&&print(a);  
Также будут добавлены знаки &, |.  
Их работа будет схожа с &&, ||, но они будут указывать на первое равенство. Пример:  
a==8&print(a)|  
    9&print(b)||  
print(c);  
0==b&print(a)|  
  c&print(b)||  
1==b&print(a);  
(a>0)&&
{A+5+6;
2+3}
!!a==b&print(c);  
Вместо ; в таких выражениях будут использованы эти символы.  
; Будет означать завершение выражения.  

Поразрядные операции:  
$* - AND  
$/ - OR  
$% - XOR  
$! - Инверсия  
`$>`, `$<` - логический сдвиг  

Также можно объединить, например:  
${a*b/c>3};  
`${a*b/c}>3&print(a);`  

### Функции  
Функции будут обозначены знаком =>:  
abc(a, i=0, i<m&i++)=>{}  
Рекурсивные функции:  
abc(a, i, n)=>{  
i<m&print(a)&i++;  
}  
Функции с условием:  
abc(i, i<m)=>{  
print(a);  
i++;  
}  
Плюсы функций, в которых присутствуют циклы:

Как это должно быть устроено - при достижении конструкций, отвечающих за цикл, функция должна переходить в "цикл".
### Циклы:
(a>n)^^c+5&a++;  
(a>n|a++)^^c+5;  
(a>n$a++)^^c+5;  
Именованный цикл:  
a=(a, b, c;i>n&i++)^^{c+5; a+3; d+6}
a(a, b, c).
Берет все данные оттуда, откуда была вызвана. Проводит вычисления с введенными переменными.
### Типы данных:
Объявляться будут с помощью таких конструкций:  
a: number;  
Виды типов данных:  
number, string, array, object.  
#### Number
3+4=7;  
3-2=1;  
5*3=15;  
6/3=2;  
4^2=16;  
#### String
"" = ''. Они однострочные.  
`` - многострочные. Шаблонные строки -  `${a}`;  
Может существовать такая конструкция -   
Символы указываются с помощью переменных, дополнительных библиотек или ограничений на один элемент массива  
```pug  
  
```  
'A'+'B'=='AB';  
'A'*3=='AAA';  
'ABA'/3==`['A', 'B', 'A']`. Принимаются только строки, которые можно поделить нацело.  
#### Массивы
Элементы массива извлекаются так:  
`a[4];`  
Также есть срезы:  
`a[4:6]`. Отрицательное число - извлечение с конца.  
`a[4:6:'a']` - извлечение, используя определенный символ.  
Также будет существовать отдельный файл с таким типом данных - abc.arr  
a[a,b,c];  
b[a,b,c];  
Основной разделитель - запятая  
#### Объекты:
a{  
a: c;  
d: 1  
}  
Основной разделитель - ;  
Вызов будет происходить через точку:  
a.a;  
Также присутствуют условные конструкции:  
a.a&print(b)|  
  d&print(c)||  
b==a&print(f);  
Расширение - тип данных .arrbj. Смесь объекта и массива. Можно будет извлекать только объекты или только массивы или, используя вспомогательные файлы типа json, arr, obj, конвертировать этот формат.  
a{  
a:4;  
b,  
}  
Определяться, элемент массива это или объекта будет с помощью запятой или точки с запятой.  
Также будут json - javascript/string object notation  
jsan - javascript/string array notation  
## Список языков, под которые планируется вестись адаптация и причины, по которым адаптация будет вестись под эти языки:
gas - на нем написан gcc - компилятор c/c++.  
python - улучшенная работа со строками и простой синтаксис.  
js/ts/node - хорошо оформленная архитектура построения модулей. Основной язык web-разработки  
c - база, на которой реализовано большинство вещей в программировании. C++ и python написаны на этом языке.  
C++ - Улучшенная база, написанная на C. На этом языке программирования написан js.  

Приветствуется материальная помощь и помощь в написании кода.  
## Для тех, кто хочет материально помочь тем, кто разрабатывает данный язык:
https://boosty.to/vosirandr/donate  
0xE683392f477B278dE6ce03198BFdf9c3E01EAc6D  
