# tipical
A summary of most typical mistakes in C++ and programming languages in general

Под TL ещё берётся OL

WA/RE/TL/ML:
* переполнение (типы данных)
* инциализация (заполнить нулями / default значениями)
* выйти за границы массива
* неправильная формулка (неправильный код)

WA/RE:
* отсуствие возврата из функции (функция должна была что-то вернуть, но ничего не вернула (то есть вернула мусор))
* обратится к неправильному указателю
* перепутали порядок обхода многомерного массива

RE/TL/ML:
* бесконечная рекурсия

WA:
* неправильно работаете с float/double (неправильно их сравниваете)
```cpp
#include <iostream>
#include <cmath>

#define EPS 0.00000001
#define double_cmp(a, b) std::fabs(a - b) < EPS

int main() {
    double a = 1.0/3;
    double b = 1.0/33;
    if (double_cmp(a, b * 11)) {
        std::cout << "OK\n";
    } else {
        std::cout << "not OK\n";
    }
}
```

RE:
* обратится к `nullptr`

TL:
* бесконечный цикл
* отсутствие оптимизации ввода-вывода

TL/ML:
* Делаете `push_back` без `reserve`

Упоротые ошибки:
* `;`
* конфликт имён
* `if (a = 0) ...`
* `double x = 1/3;`
