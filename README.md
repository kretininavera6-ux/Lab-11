# Lab-11
Условие вариант 10 



<img width="698" height="53" alt="image" src="https://github.com/user-attachments/assets/544a3d5d-c711-49ca-9ec5-5805b7102234" />

Описание программы




Программа вычисляет сумму элементов массива, расположенных после элемента с наименьшим значением по модулю.
1. Ввод размера и элементов массива
2. Поиск элемента с минимальным модулем
3. Суммирование элементов после найденного
4. Вывод результата

Контрольный пример


Пусть кол-во элементов массива 4, тогда вводим 4 случайных числа:
1
2
3
6


минимальное по модулю: 1



Сумма после элемента с мин. модулем: 2+3+6=11



Программа
```
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "rus");
    int n, i, min_i = 0, sum = 0;
    printf("Количество элементов массива: ");
    scanf("%d", &n);
    int* a = (int*)malloc(n * sizeof(int));
    printf("Введите %d чисел:\n", n);
    for (i = 0; i < n; i++)
        scanf("%d", &a[i]);
    for (i = 1; i < n; i++)
        if (abs(a[i]) < abs(a[min_i]))
            min_i = i;
    for (i = min_i + 1; i < n; i++)
        sum += a[i];
    printf("Сумма после элемента с мин. модулем: %d\n", sum);
    free(a);
    return 0;
}
```


Блок схема








