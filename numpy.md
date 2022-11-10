# Библиотека NumPy

>Библиотека с открытым исходным кодом для языка программирования Python.

- [Библиотека NumPy](#библиотека-numpy)
  - [Атрибуты массива NumPy](#атрибуты-массива-numpy)
    - [`ndarray.ndim`](#ndarrayndim)
    - [`ndarray.shape`](#ndarrayshape)
    - [`ndarray.size`](#ndarraysize)
    - [`ndarray.dtype`](#ndarraydtype)
    - [`ndarray.itemsize`](#ndarrayitemsize)
    - [`ndarray.data`](#ndarraydata)
    - [`ndarray.sum()`](#ndarraysum)
    - [`ndarray.min()`](#ndarraymin)
    - [`ndarray.max()`](#ndarraymax)
  - [Функции NumPy](#функции-numpy)
    - [`type(numpy.ndarray)`](#typenumpyndarray)
    - [`numpy.zeroes()`](#numpyzeroes)
    - [`numpy.ones()`](#numpyones)
    - [`numpy.arrange()`](#numpyarrange)
    - [`numpy.empty()`](#numpyempty)
    - [`numpy.linspace()`](#numpylinspace)
    - [`numpy.logspace()`](#numpylogspace)
    - [`umpy.sin()`](#umpysin)
    - [`numpy.reshape()`](#numpyreshape)
    - [`numpy.random.random()`](#numpyrandomrandom)
    - [`numpy.exp()`](#numpyexp)
    - [`numpy.sqrt()`](#numpysqrt)
    - [`numpy.flags`](#numpyflags)
    - [`unravel_index()`](#unravel_index)
    - [`a.argmax()` и `a.argmin()`](#aargmax-и-aargmin)
    - [`allclose()`](#allclose)

## Атрибуты массива NumPy

### `ndarray.ndim`

`ndarray.ndim` – возвращает количество измерений массива.

```text
import numpy as np 
a = np.array([[1,2,3],[4,5,6]])
print(a.ndim)
Вывод кода сверху будет 2, поскольку «a» - это 2-мерный массив.
```

### `ndarray.shape`

`ndarray.shape` — возвращает кортеж размера массива, то есть (n,m), где n - это количество строк, а m - количество колонок.

```text
import numpy as np 
a = np.array([[1,2,3],[4,5,6]])
print(a.shape)
Вывод кода - (2,3), то есть 2 строки и 3 колонки.
```

### `ndarray.size`

`ndarray.size` — возвращает общее количество элементов в массиве.

```text
import numpy as np 
a = np.array([[1,2,3],[4,5,6]])
print(a.size)
Вывод - 6, потому что 2 х 3.
```

### `ndarray.dtype`

`ndarray.dtype` — возвращает объект, описывающий тип элементов в массиве.

```text
import numpy as np 
a = np.array([[1,2,3],[4,5,6]])
print(a.dtype)
Вывод - «int32», поскольку это 32-битное целое число.
```

### `ndarray.itemsize`

`ndarray.itemsize` — возвращает размер каждого элемента в массиве в байтах.

```text
import numpy as np 
a = np.array([[1,2,3],[4,5,6]])
print(a.itemsize)
Вывод - 4, потому что 32/8.
```

### `ndarray.data`

`ndarray.data` — возвращает буфер с актуальными элементами массива. Это альтернативный способ получения доступа к элементам через их индексы.

```text
import numpy as np
a= np.array([[1,2,3],[4,5,6]])
print(a.data)
Этот код вернет список элементов.
```

### `ndarray.sum()`

`ndarray.sum()` — функция вернет сумму все элементов ndarray.

```text
import numpy as np
a = np.random.random((2,3))
print(a)
print(a.sum())
Код вернет сгенерированную матрицу.
```

### `ndarray.min()`

`ndarray.min()` — функция вернет элемент с минимальным значением из ndarray.

```text
import numpy as np
a = np.random.random((2,3))
print(a.min())
Код вернет сгенерированную матрицу.
```

### `ndarray.max()`

`ndarray.max()` — функция вернет элемент с максимальным значением из ndarray.

```text
import numpy as np
a = np.random.random((2,3))
print(a.min())
Код вернет сгенерированную матрицу.
```

## Функции NumPy

### `type(numpy.ndarray)`

`type(numpy.ndarray)` — это функция Python, используемая, чтобы вернуть тип переданного параметра.

``` text
import numpy as np
a = np.array([[1,2,3],[4,5,6]])
print(type(a))
Код вернет нам <class 'numpy.ndarray'>
```

### `numpy.zeroes()`

`numpy.zeros((rows, columns), dtype)` —  эта функция создаст массив numpy с заданным количеством измерений, где каждый элемент будет равняться 0. Если dtype не указан, по умолчанию будет использоваться dtype.

```text
import numpy as np
a = np.zeros((3,3))
print(a)
Код вернет массив numpy 3×3, где каждый элемент равен 0.
```

### `numpy.ones()`

`numpy.ones((rows,columns), dtype)` — эта функция создаст массив numpy с заданным количеством измерений, где каждый элемент будет равняться 1. Если dtype не указан, по умолчанию будет использоваться dtype.

```text
import numpy as np
a = np.ones((3,3))
print(a)
Код вернет массив numpy 3 x 3, где каждый элемент равен 1.
```

### `numpy.arrange()`

`numpy.arrange(start, stop, step)` — эта функция используется для создания массива numpy, элементы которого лежат в диапазоне значений от start до stop с разницей равной step.

```text
import numpy as np 
a=np.arange(5,25,5)
print(a)
Вывод - [ 5 10 15 20].
```

### `numpy.empty()`

`numpy.empty((rows,columns))` — эта функция создаст массив, содержимое которого будет случайным - оно зависит от состояния памяти.

``` text
import numpy as np
a = np.empty((3,3))
print(a)
Код вернет массив numpy 3×3, где каждый элемент будет случайным.
```

### `numpy.linspace()`

`numpy.linspace(start, stop, num_of_elements)` — эта функция создаст массив numpy, элементы которого лежат в диапазоне значений между start до stop, а num_of_elements - это размер массива. Тип по умолчанию - float64.

```text
import numpy as np
a=np.linspace(5,25,5)
print(a)
Вывод -[ 5. 10. 15. 20. 25.]
```

### `numpy.logspace()`

`numpy.logspace(start, stop, num_of_elements)` — эта функция используется для создания массива numpy, элементы которого лежат в диапазоне значений от start до stop, а num_of_elements - это размер массива. Тип по умолчанию - float64. Все элементы находятся в пределах логарифмической шкалы, то есть представляют собой логарифмы соответствующих элементов.

```text
import numpy as np
a = np.logspace(5,25,5)
print(a)
Вывод - [1.e+05 1.e+10 1.e+15 1.e+20 1.e+25].
```

### `umpy.sin()`

`numpy.sin(numpy.ndarray)` — этот код вернет синус параметра.

```text
import numpy as np
a = np.logspace(5,25,2)
print(np.sin(a))
Вывод - [0.0357488 -0.3052578]. Также есть cos(), tan() и тд.
```

### `numpy.reshape()`

`numpy.reshape(dimensions)` — эта функция используется для изменения количества измерений массива numpy. От количества аргументов в reshape зависит, сколько измерений будет в массиве numpy.

``` text
import numpy as np
a = np.arange(9).reshape(3,3)
print(a)
Вывод - 2-мерный массив 3×3
```

### `numpy.random.random()`

`numpy.random.random((rows, column))` — эта функция возвращает массив с заданным количеством измерений, где каждый элемент генерируется случайным образом.

``` text
import numpy as np
a = np.random.random((3,3))
print(a)
Этот код вернет ndarray 2×2.
```

### `numpy.exp()`

`numpy.exp(numpy.ndarray)` — функция вернет ndarray с экспоненциальной величиной каждого элемента.

```text
import numpy as np
b = np.exp([10])
print(a)​
Вывод - [[0.02997357 0.67482656 0.12884391]
 [0.7937237  0.43831081 0.61778992]
 [0.80257984 0.19331923 0.83258906]]
 ```

### `numpy.sqrt()`

`numpy.sqrt(numpy.ndarray)` — эта функция вернет ndarray с квадратным корнем каждого элемента.

```text
import numpy as np
a = np.sqrt([16])
print(a)
Вывод - 4.
```

### `numpy.flags`

Объект ndarray имеет следующие атрибуты. Текущие значения возвращаются этой функцией

| Sr.No.                         | Атрибут и описание                    |
| ---------------------------------- | --------------------------------- |
|1 |`C_CONTIGUOUS`   Данные находятся в одном непрерывном сегменте в стиле C
|2 | `F_CONTIGUOUS` Данные находятся в одном непрерывном сегменте в стиле Фортрана. |
|3 |`СОБСТВЕННЫЕ ДАННЫЕ (OWNDATA)` Массив владеет используемой памятью или занимает ее у другого объекта.       |
|4 |`ПИСЬМО (WRITEABLE)` Область данных может быть записана в установке этого значения в False блокирует данные, делая их доступными только для чтения|
| 5|`ВЫРАВНИЛ (ALIGNED )` Данные и все элементы выровнены соответствующим образом для оборудован        |
|6 |`UPDATEIFCOPY ( UPDATEIFCOPY)` Этот массив является копией некоторого другого массива. Когда этот массив освобожден, базовый массив будет обновлен с содержанием этого массива                                 |

```text
import numpy as np 
x = np.array([1,2,3,4,5]) 
print x.flags
Вывод:
  C_CONTIGUOUS : True
  F_CONTIGUOUS : True
  OWNDATA : True
  WRITEABLE : True
  ALIGNED : True
  WRITEBACKIFCOPY : False
  UPDATEIFCOPY : False

```

### `unravel_index()`

`unravel_index()` — функция преобразует плоский массив индексов в кортеж массивов индексов.

### `a.argmax()` и `a.argmin()`

`a.argmax()` — возвращает индекс максимального элемента в массиве, `a.argmin()` делает противоположное

### `allclose()`

`allclose()` возвратит True, если элементы двух массивов равны в пределах допуска.


Объявим два массива, разница между соответствующими элементами которых не более 0.2:

