# Japy
Japy - проект, ставящий цель унифицировать и упростить языки программирования, которые существуют сейчас, а также уменьшить к минимуму присутствие языков хотя бы на уровне основных структур.  

Данный синтаксис также может являться максимально приближенной версией языка программирования для данного уровня развития языков. Необязательно все отсюда будет реализовано. 
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
>>, << - потоки.
Поразрядные операции:  
$* - AND  
$/ - OR  
$% - XOR  
$! - Инверсия  
$!* - NAND  
$!/ - NOR  
$!% - XNOR  
$>= - Импликация  
$<= - Обратная импликация  
`$>`, `$<` - Циклический сдвиг
1010$>1=0101; 
`$!>`, `$!<` - Циклический сдвиг через бит переноса  
`$>>`, `$<<` - Арифметический сдвиг  
`$!<<`, `$!>>` - Логический сдвиг  
Также можно объединить, например:  
${a*b/c>3};  
`${a*b/c}>3&print(a);`  
$$ - Вычисления в исходной кодировке.
'a'$$+'B' //(u+0041)+(u+0042)=u+0083. Также можно пропускать невалидные символы.

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
Функция - изолированный кусок кода. Это и плюс - Легче производить операции, которые в теории должны мешать другим частям программы, и минус - увеличивается нагрузка на машину. 

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
432[1]==3;
#### String
"" = ''. Они однострочные.  
`` - многострочные. Шаблонные строки -  `${a}`;  
Может существовать такая конструкция -   
Символы указываются с помощью переменных, дополнительных библиотек или ограничений на один элемент массива  
```pug  
  
```
D='ABCDeCfg'-'C'=='ABDefg';  
'A'+'B'=='AB';  
a='A ';  
a[1]==' ';  
b='b';  
a+b+a+b+a-' '+b=='A bA bA bAb';  
'A'*3=='AAA';  
'ABA'/3==`['A', 'B', 'A']`. Принимаются только строки, которые можно поделить нацело.  
'ABA'/0==3; Подсчет количества элементов.  
'ABA'[-1]*-1>>c==3; Подсчет количества элементов. Альтернативный метод  
'ABA'/'CDS'=='ACBDAS';  
'ABA'/'CDSQ'=='AC!D!SQ'; B в unicode - u+0042. ! - u+0021;  
'ABA'*'CDSQ' == 'ABACDSQABACDSQABACDSQABACDSQ'; ('ABA'+'CDSQ'*4) Дублирование строк столько раз, сколько букв во втором выражении.  

#### Массивы
Элементы массива извлекаются так:  
`a[4];`  
Также есть срезы:  
`a[4:6]`. Отрицательное число - извлечение с конца.  
`a[4:6:'a']` - извлечение, используя определенный символ.  Python
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
#### Классы
.User{
=>{
int n;
-<.n=n;
}
Mysha(){

}
}

.Main=>.User{
=<()

}
### Импорт/Экспорт
import bs as ds from './abc' - Пользовательские библиотеки  
import bs as ds from 'abc' - Встроенные библиотеки  
## Список языков, под которые планируется вестись адаптация и причины, по которым адаптация будет вестись под эти языки:
asm-gas - на нем написан gcc - компилятор c/c++. Имеется возможность вести более оптимизированный код. Кросплатформенность по сравнению с другими ассемблерами. Встраиваемость в c/c++  
python - улучшенная работа со строками и простой синтаксис.  
js/ts/node - хорошо оформленная архитектура построения модулей. Основной язык web-разработки  
c - база, на которой реализовано большинство вещей в программировании. C++ и python написаны на этом языке.  
C++ - Улучшенная база, написанная на C. На этом языке программирования написан js.  

Приветствуется материальная помощь и помощь в написании кода.  
## Для тех, кто хочет материально помочь тем, кто разрабатывает данный язык:
https://boosty.to/vosirandr/donate  
0xE683392f477B278dE6ce03198BFdf9c3E01EAc6D  
