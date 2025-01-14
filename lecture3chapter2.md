# Организация таблиц символов
## Метод цепочек

Метод цепочек использует хеш-таблицу, элементы которой первоначально равны 0, собственно таблицу символов, вначале пустую, и указатель УК, который указывает на текущее положение последнего элемента в таблице символов. Элементы таблицы символов имеют дополнительное поле СНАIN, которое может содержать 0 или адрес другого элемента таблицы символов. Начальное состояние таблицы приведено на схеме:

|  №  | Хеш-таблица |
|:---:|:---:|
|  0  |     |
|  1  |     | 
| ... |     | 
| N-1 |     | 

**УК = 0**
|  №  | Аргумент | Значение| CHAIN |
|:---:|:---:|:----:|:----:|
|  1  |     |     |     |
|  2  |     |     |     |
| ... |     |     |     |
|  N  |     |     |     |

Хеш-функция, применённая к символу, даёт индекс указателя в хеш-таблице. Указатель либо равен 0, либо указывает на первый элемент таблицы символов с данным значением хеш-функции. Поле СНАIN каждого элемента используется для того, чтобы связать в цепочку элементы, для которых хеширование символа приводит к тому же самому указателю. Например, в таблицу необходимо записать символ S1, Функция хеширования вырабатывает адрес элемента хеш-таблицы, например 4. Содержимое этой ячейки равно 0. Тогда выполняется следующее:  
1.	Прибавляем 1 к УК.
2.	Вносим элемент (S1, значение, 0) в позицию таблицы символов,
на которую указывает УК.
3.	Заносим содержимое УК. в указатель 4 хеш-таблицы.
Пока поступают символы, хеширование которых даёт индексы разных указателей, они заносятся в таблицу аналогичным образом. Так, если мы записываем в таблицу символы S2, S3, S4, хеширование которых даёт ссылки на указатели 1, 3, 6, таблица примет вид, представленный на следующей схеме:

|  №  | Хеш-таблица |
|:---:|:---:|
|  0  |     |
|  1  |  2   | 
|  2  |     | 
|  3  |  3   | 
|  4  |  1   | 
|  5  |     | 
|  6  |  4   | 

**УК = 4**
|  №  | Аргумент | Значение| CHAIN |
|:---:|:---:|:----:|:----:|
|  1  |  S1   | ... |   0  |
|  2  |  S2   | ... |   0  |
|  3  |  S3   | ... |   0  |
|  4  |  S4   | ... |   0  |

В конце концов, поступит символ S5, который ссылается на указатель, использовавшийся ранее, например на 6. Вот здесь и начинает действовать поле CHAIN. Символ S5 записывается в таблицу символов и добавляется к концу цепочки для этого указателя:

|  №  | Хеш-таблица |
|:---:|:---:|
|  0  |     |
|  1  |  2   | 
|  2  |     | 
|  3  |  3   | 
|  4  |  1   | 
|  5  |     | 
|  6  |  4   | 


**УК = 5**
|  №  | Аргумент | Значение| CHAIN |
|:---:|:---:|:----:|:----:|
|  1  |  S1   | ... |   0  |
|  2  |  S2   | ... |   0  |
|  3  |  S3   | ... |   0  |
|  4  |  S4   | ... |   5  |
|  5  |  S5   | ... |   0  |

Пусть необходимо внести в таблицу символы S6, S7, S8, которые ссылаются на указатели 4, 3, 3 соответственно:

|  №  | Хеш-таблица |
|:---:|:---:|
|  0  |     |
|  1  |  2  | 
|  2  |     | 
|  3  |  3  | 
|  4  |  1  | 
|  5  |     | 
|  6  |  4  | 


**УК = 8**
|  №  | Аргумент | Значение| CHAIN |
|:---:|:---:|:----:|:----:|
|  1  |  S1   | ... |   6  |
|  2  |  S2   | ... |   0  |
|  3  |  S3   | ... |   7  |
|  4  |  S4   | ... |   5  |
|  5  |  S5   | ... |   0  |
|  6  |  S6   | ... |   0  |
|  7  |  S7   | ... |   8  |
|  8  |  S8   | ... |   0  |

