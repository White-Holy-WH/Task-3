# Практическая работа №3: Управляющие конструкции и операторы ветвления в C# (if, else if, else, switch)
### Выполнил студент группы П25-2.1    Карпенко Артём Ярославович

---

**Раздел 1. Базовые условия if и if-else **

---


## №1. Проверить, является ли число положительным

**Условие:** Пользователь вводит целое число. Проверить, является ли оно положительным.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a > 0)
                Console.WriteLine("Число положительное");
            else
                Console.WriteLine("Число не положительное");
        }
    }
}
```

**Пример:** при вводе `5` → «Число положительное», при `-3` → «Число не положительное».

---

## №2. Проверить, является ли число чётным

**Условие:** Пользователь вводит целое число. Проверить, является ли оно чётным.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 2 == 0)
                Console.WriteLine("Число чётное");
            else
                Console.WriteLine("Число нечётное");
        }
    }
}
```

**Пример:** при вводе `4` → «Число чётное», при `7` → «Число нечётное».

---

## №3. Вывести большее из двух чисел

**Условие:** Даны два целых числа. Вывести самое большое из них.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первое число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите второе число: ");
            int b = Convert.ToInt32(Console.ReadLine());

            if (a > b)
                Console.WriteLine("Большее: " + a);
            else
                Console.WriteLine("Большее: " + b);
        }
    }
}
```

**Пример:** при `5` и `8` → «Большее: 8».

---

## №4. Вывести наименьшее из двух чисел

**Условие:** Даны два числа с плавающей точкой. Вывести наименьшее.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первое число: ");
            double a = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите второе число: ");
            double b = Convert.ToDouble(Console.ReadLine());

            if (a < b)
                Console.WriteLine("Меньшее: " + a);
            else
                Console.WriteLine("Меньшее: " + b);
        }
    }
}
```

**Пример:** при `2.5` и `1.8` → «Меньшее: 1.8».

---

## №5. Проверить, делится ли введённое число на 5

**Условие:** Проверить, делится ли введённое число нацело на 5.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 5 == 0)
                Console.WriteLine("Делится на 5");
            else
                Console.WriteLine("Не делится на 5");
        }
    }
}
```

**Пример:** при `15` → «Делится на 5», при `7` → «Не делится на 5».

---

## №6. Проверить, оканчивается ли число нулём

**Условие:** Проверить, оканчивается ли введённое число нулём.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 10 == 0)
                Console.WriteLine("Оканчивается на 0");
            else
                Console.WriteLine("Не оканчивается на 0");
        }
    }
}
```

**Пример:** при `120` → «Оканчивается на 0», при `123` → «Не оканчивается на 0».

---

## №7. Мороз — наденьте шапку

**Условие:** Пользователь вводит температуру воздуха. Если она ниже нуля, вывести: «На улице мороз, наденьте шапку».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите температуру: ");
            int t = Convert.ToInt32(Console.ReadLine());

            if (t < 0)
                Console.WriteLine("На улице мороз, наденьте шапку");
        }
    }
}
```

**Пример:** при `-5` → «На улице мороз, наденьте шапку», при `3` → ничего не выводится.

---

## №8. Больше 100 — уменьшить на 20, иначе увеличить на 10

**Условие:** Дано число. Если оно больше 100, уменьшить его на 20, иначе увеличить на 10.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a > 100)
                a = a - 20;
            else
                a = a + 10;

            Console.WriteLine("Результат: " + a);
        }
    }
}
```

**Пример:** при `150` → «Результат: 130», при `50` → «Результат: 60».

---

## №9. Равны ли два числа

**Условие:** Ввести два числа. Если они равны, вывести «Числа равны», иначе вывести их произведение.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первое число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите второе число: ");
            int b = Convert.ToInt32(Console.ReadLine());

            if (a == b)
                Console.WriteLine("Числа равны");
            else
                Console.WriteLine("Произведение: " + (a * b));
        }
    }
}
```

**Пример:** при `3` и `3` → «Числа равны», при `3` и `4` → «Произведение: 12».

---

## №10. Проверка возраста

**Условие:** Пользователь вводит свой возраст. Если возраст от 18 лет и старше, вывести «Доступ разрешен», иначе «Доступ запрещен».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите возраст: ");
            int age = Convert.ToInt32(Console.ReadLine());

            if (age >= 18)
                Console.WriteLine("Доступ разрешен");
            else
                Console.WriteLine("Доступ запрещен");
        }
    }
}
```

**Пример:** при `20` → «Доступ разрешен», при `15` → «Доступ запрещен».

---

## №11. Является ли число трёхзначным

**Условие:** Ввести число. Если оно трёхзначное, вывести «Да», иначе «Нет».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a >= 100 && a <= 999)
                Console.WriteLine("Да");
            else
                Console.WriteLine("Нет");
        }
    }
}
```

**Пример:** при `456` → «Да», при `45` → «Нет».

---

## №12. Делится ли число на 3 без остатка

**Условие:** Проверить, делится ли число на 3 без остатка.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 3 == 0)
                Console.WriteLine("Делится на 3");
            else
                Console.WriteLine("Не делится на 3");
        }
    }
}
```

**Пример:** при `9` → «Делится на 3», при `10` → «Не делится на 3».

---

## №13. Лежит ли точка правее нуля

**Условие:** Дана координата точки X на числовой прямой. Определить, лежит ли точка правее нуля.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите координату X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            if (x > 0)
                Console.WriteLine("Точка правее нуля");
            else
                Console.WriteLine("Точка не правее нуля");
        }
    }
}
```

**Пример:** при `3.5` → «Точка правее нуля», при `-2` → «Точка не правее нуля».

---

## №14. Баланс счёта

**Условие:** Ввести баланс счёта. Если баланс отрицательный, вывести «Задолженность!».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите баланс: ");
            double bal = Convert.ToDouble(Console.ReadLine());

            if (bal < 0)
                Console.WriteLine("Задолженность!");
        }
    }
}
```

**Пример:** при `-500` → «Задолженность!», при `100` → ничего.

---

## №15. Проверка пароля

**Условие:** Пользователь вводит пароль (целое число). Если введено 1234, вывести «Вход выполнен», иначе «Неверный пароль».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите пароль: ");
            int p = Convert.ToInt32(Console.ReadLine());

            if (p == 1234)
                Console.WriteLine("Вход выполнен");
            else
                Console.WriteLine("Неверный пароль");
        }
    }
}
```

**Пример:** при `1234` → «Вход выполнен», при `1111` → «Неверный пароль».

---

## №16. Отрицательное ли число

**Условие:** Проверить, является ли введённое число отрицательным.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a < 0)
                Console.WriteLine("Отрицательное");
            else
                Console.WriteLine("Не отрицательное");
        }
    }
}
```

**Пример:** при `-7` → «Отрицательное», при `7` → «Не отрицательное».

---

## №17. Разность большего и меньшего

**Условие:** Даны два числа. Вывести разность большего и меньшего числа.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первое число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите второе число: ");
            int b = Convert.ToInt32(Console.ReadLine());

            if (a > b)
                Console.WriteLine("Разность: " + (a - b));
            else
                Console.WriteLine("Разность: " + (b - a));
        }
    }
}
```

**Пример:** при `10` и `4` → «Разность: 6», при `3` и `8` → «Разность: 5».

---

## №18. Скидка 5% при сумме от 1000 рублей

**Условие:** Ввести сумму покупки. Если сумма превышает 1000 рублей, рассчитать скидку 5% и вывести итоговую цену.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите сумму покупки: ");
            double sum = Convert.ToDouble(Console.ReadLine());

            if (sum > 1000)
            {
                double itog = sum * 0.95;
                Console.WriteLine("Итоговая цена со скидкой: " + itog);
            }
            else
            {
                Console.WriteLine("Итоговая цена: " + sum);
            }
        }
    }
}
```

**Пример:** при `2000` → «Итоговая цена со скидкой: 1900», при `500` → «Итоговая цена: 500».

---

## №19. Чётное — делим на 2, нечётное — умножаем на 3

**Условие:** Ввести число. Если оно чётное, разделить его на 2, если нечётное — умножить на 3.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 2 == 0)
                a = a / 2;
            else
                a = a * 3;

            Console.WriteLine("Результат: " + a);
        }
    }
}
```

**Пример:** при `8` → «Результат: 4», при `5` → «Результат: 15».

---

## №20. Превышение скорости

**Условие:** Пользователь вводит скорость движения. Если скорость выше 90 км/ч, вывести сообщение о нарушении.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите скорость: ");
            int v = Convert.ToInt32(Console.ReadLine());

            if (v > 90)
                Console.WriteLine("Нарушение скорости!");
        }
    }
}
```

**Пример:** при `100` → «Нарушение скорости!», при `60` → ничего.

---

## №21. Равно ли число нулю

**Условие:** Дано число. Проверить, равно ли оно нулю.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a == 0)
                Console.WriteLine("Число равно нулю");
            else
                Console.WriteLine("Число не равно нулю");
        }
    }
}
```

**Пример:** при `0` → «Число равно нулю», при `5` → «Число не равно нулю».

---

## №22. Равенство с точностью до 0,001

**Условие:** Ввести два вещественных числа. Проверить, равны ли они с точностью до 0,001.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первое число: ");
            double a = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите второе число: ");
            double b = Convert.ToDouble(Console.ReadLine());

            if (Math.Abs(a - b) < 0.001)
                Console.WriteLine("Числа равны");
            else
                Console.WriteLine("Числа не равны");
        }
    }
}
```

**Пример:** при `1.0001` и `1.0002` → «Числа равны», при `1.0` и `2.0` → «Числа не равны».

---

## №23. Делится ли число A на число B без остатка

**Условие:** Проверить, делится ли число A на число B без остатка.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите число B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            if (b != 0 && a % b == 0)
                Console.WriteLine("Делится без остатка");
            else
                Console.WriteLine("Не делится без остатка");
        }
    }
}
```

**Пример:** при `10` и `2` → «Делится без остатка», при `10` и `3` → «Не делится без остатка».

---

## №24. Существует ли треугольник по двум углам

**Условие:** Даны два угла треугольника в градусах. Проверить, существует ли такой треугольник (сумма меньше 180).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первый угол: ");
            int u1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите второй угол: ");
            int u2 = Convert.ToInt32(Console.ReadLine());

            if (u1 + u2 < 180)
                Console.WriteLine("Треугольник существует");
            else
                Console.WriteLine("Треугольник не существует");
        }
    }
}
```

**Пример:** при `60` и `70` → «Треугольник существует», при `100` и `90` → «Треугольник не существует».

---

## №25. Площадь круга и квадрата

**Условие:** Ввести радиус круга и сторону квадрата. Определить, у какой фигуры площадь больше.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите радиус круга: ");
            double r = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите сторону квадрата: ");
            double s = Convert.ToDouble(Console.ReadLine());

            double sk = 3.14 * r * r;
            double sq = s * s;

            if (sk > sq)
                Console.WriteLine("Площадь круга больше");
            else
                Console.WriteLine("Площадь квадрата больше или равна");
        }
    }
}
```

**Пример:** при `5` и `2` → «Площадь круга больше», при `1` и `5` → «Площадь квадрата больше или равна».

---

## №26. Частное большего на меньшее

**Условие:** Ввести два числа. Вывести частное большего на меньшее (предварительно проверить деление на 0).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первое число: ");
            double a = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите второе число: ");
            double b = Convert.ToDouble(Console.ReadLine());

            if (b == 0)
                Console.WriteLine("Деление на ноль!");
            else if (a > b)
                Console.WriteLine("Частное: " + (a / b));
            else
                Console.WriteLine("Частное: " + (b / a));
        }
    }
}
```

**Пример:** при `10` и `2` → «Частное: 5», при `2` и `0` → «Деление на ноль!».

---

## №27. Последняя цифра равна семи

**Условие:** Проверить, равна ли последняя цифра числа семи.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 10 == 7)
                Console.WriteLine("Последняя цифра равна 7");
            else
                Console.WriteLine("Последняя цифра не равна 7");
        }
    }
}
```

**Пример:** при `17` → «Последняя цифра равна 7», при `25` → «Последняя цифра не равна 7».

---

## №28. Нечётное и положительное

**Условие:** Дано число. Если оно нечётное и положительное, вывести «Да».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 2 != 0 && a > 0)
                Console.WriteLine("Да");
            else
                Console.WriteLine("Нет");
        }
    }
}
```

**Пример:** при `7` → «Да», при `-7` → «Нет».

---

## №29. Свободное место на диске

**Условие:** Ввести объём свободного места на диске (в ГБ). Если место меньше 5 ГБ, вывести предупреждение.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите свободное место (ГБ): ");
            double disk = Convert.ToDouble(Console.ReadLine());

            if (disk < 5)
                Console.WriteLine("Мало места на диске!");
        }
    }
}
```

**Пример:** при `3` → «Мало места на диске!», при `20` → ничего.

---

## №30. Оценка студента

**Условие:** Пользователь вводит оценку (2, 3, 4, 5). Если оценка 4 или 5, вывести «Молодец», иначе «Нужно подтянуться».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите оценку: ");
            int mark = Convert.ToInt32(Console.ReadLine());

            if (mark == 4 || mark == 5)
                Console.WriteLine("Молодец");
            else
                Console.WriteLine("Нужно подтянуться");
        }
    }
}
```

**Пример:** при `5` → «Молодец», при `3` → «Нужно подтянуться».

---

## №31. Равны ли два символа

**Условие:** Даны два символа. Проверить, равны ли они.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первый символ: ");
            string s1 = Console.ReadLine();

            Console.Write("Введите второй символ: ");
            string s2 = Console.ReadLine();

            if (s1 == s2)
                Console.WriteLine("Символы равны");
            else
                Console.WriteLine("Символы не равны");
        }
    }
}
```

**Пример:** при `a` и `a` → «Символы равны», при `a` и `b` → «Символы не равны».

---

## №32. Кратно и 2, и 7

**Условие:** Ввести число. Если оно кратно и 2, и 7, вывести «Кратно 14».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 2 == 0 && a % 7 == 0)
                Console.WriteLine("Кратно 14");
            else
                Console.WriteLine("Не кратно 14");
        }
    }
}
```

**Пример:** при `28` → «Кратно 14», при `14` и проверке → «Кратно 14», при `10` → «Не кратно 14».

---

## №33. Превышение массы груза

**Условие:** Ввести вес груза. Если масса превышает допустимые 3,5 тонны, вывести «Перегруз!».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите вес груза (т): ");
            double ves = Convert.ToDouble(Console.ReadLine());

            if (ves > 3.5)
                Console.WriteLine("Перегруз!");
        }
    }
}
```

**Пример:** при `4` → «Перегруз!», при `3` → ничего.

---

## №34. Доброе утро

**Условие:** Ввести текущее время (часы от 0 до 23). Если время с 6 до 12, вывести «Доброе утро».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите часы (0-23): ");
            int hour = Convert.ToInt32(Console.ReadLine());

            if (hour >= 6 && hour <= 12)
                Console.WriteLine("Доброе утро");
        }
    }
}
```

**Пример:** при `8` → «Доброе утро», при `20` → ничего.

---

## №35. Очень высокий рост

**Условие:** Ввести рост человека в см. Если рост больше 200 см, вывести «Очень высокий».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите рост (см): ");
            int rost = Convert.ToInt32(Console.ReadLine());

            if (rost > 200)
                Console.WriteLine("Очень высокий");
        }
    }
}
```

**Пример:** при `210` → «Очень высокий», при `180` → ничего.

---

## №36. Какая цифра двузначного числа больше

**Условие:** Дано двузначное число. Определить, какая из его цифр больше.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите двузначное число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            int d1 = a / 10;
            int d2 = a % 10;

            if (d1 > d2)
                Console.WriteLine("Первая цифра больше");
            else if (d2 > d1)
                Console.WriteLine("Вторая цифра больше");
            else
                Console.WriteLine("Цифры равны");
        }
    }
}
```

**Пример:** при `52` → «Первая цифра больше», при `25` → «Вторая цифра больше», при `33` → «Цифры равны».

---

## №37. Бесплатный товар

**Условие:** Ввести стоимость товара. Если товар бесплатный (цена 0), вывести «Акция!».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите стоимость: ");
            double cena = Convert.ToDouble(Console.ReadLine());

            if (cena == 0)
                Console.WriteLine("Акция!");
        }
    }
}
```

**Пример:** при `0` → «Акция!», при `100` → ничего.

---

## №38. Одинаковые цифры в двузначном числе

**Условие:** Проверить, содержит ли введённое двузначное число одинаковые цифры.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите двузначное число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a / 10 == a % 10)
                Console.WriteLine("Цифры одинаковые");
            else
                Console.WriteLine("Цифры разные");
        }
    }
}
```

**Пример:** при `44` → «Цифры одинаковые», при `45` → «Цифры разные».

---

## №39. Слишком громкий звук

**Условие:** Ввести уровень громкости (0–100). Если громкость равна 80, вывести «Слишком громко для слуха».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите громкость (0-100): ");
            int g = Convert.ToInt32(Console.ReadLine());

            if (g == 80)
                Console.WriteLine("Слишком громко для слуха");
        }
    }
}
```

**Пример:** при `80` → «Слишком громко для слуха», при `50` → ничего.

---

## №40. Чётная сумма

**Условие:** Даны два числа. Если их сумма чётная, вывести сумму, иначе вывести их разность.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первое число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите второе число: ");
            int b = Convert.ToInt32(Console.ReadLine());

            int sum = a + b;

            if (sum % 2 == 0)
                Console.WriteLine("Сумма: " + sum);
            else
                Console.WriteLine("Разность: " + (a - b));
        }
    }
}
```

**Пример:** при `3` и `5` → «Сумма: 8», при `3` и `4` → «Разность: -1».

---

## №41. Двухсторонняя печать

**Условие:** Ввести количество страниц в документе. Если страниц больше 100, включить двухстороннюю печать.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите количество страниц: ");
            int pages = Convert.ToInt32(Console.ReadLine());

            if (pages > 100)
                Console.WriteLine("Включена двухсторонняя печать");
        }
    }
}
```

**Пример:** при `150` → «Включена двухсторонняя печать», при `50` → ничего.

---

## №42. Полный квадрат

**Условие:** Проверить, является ли введённое число полным квадратом (использовать Math.Sqrt).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            double koren = Math.Sqrt(a);

            if (koren == (int)koren)
                Console.WriteLine("Полный квадрат");
            else
                Console.WriteLine("Не полный квадрат");
        }
    }
}
```

**Пример:** при `16` → «Полный квадрат», при `10` → «Не полный квадрат».

---

## №43. Пониженное атмосферное давление

**Условие:** Ввести атмосферное давление. Если давление ниже 740 мм рт. ст., вывести «Пониженное давление».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите давление: ");
            int dav = Convert.ToInt32(Console.ReadLine());

            if (dav < 740)
                Console.WriteLine("Пониженное давление");
        }
    }
}
```

**Пример:** при `730` → «Пониженное давление», при `760` → ничего.

---

## №44. Победитель матча

**Условие:** Ввести количество забитых мячей командами А и Б. Вывести победителя или сообщить о ничьей.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Голы команды А: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Голы команды Б: ");
            int b = Convert.ToInt32(Console.ReadLine());

            if (a > b)
                Console.WriteLine("Победила команда А");
            else if (b > a)
                Console.WriteLine("Победила команда Б");
            else
                Console.WriteLine("Ничья");
        }
    }
}
```

**Пример:** при `3` и `1` → «Победила команда А», при `2` и `2` → «Ничья».

---

## №45. Модуль числа без Math.Abs

**Условие:** Дано число. Заменить его на абсолютную величину (модуль) без использования Math.Abs.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a < 0)
                a = -a;

            Console.WriteLine("Модуль: " + a);
        }
    }
}
```

**Пример:** при `-7` → «Модуль: 7», при `5` → «Модуль: 5».

---

## №46. Сахар в крови выше нормы

**Условие:** Ввести показатель уровня сахара в крови. Если показатель выше 6,1 ммоль/л, вывести «Выше нормы».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите сахар (ммоль/л): ");
            double sahar = Convert.ToDouble(Console.ReadLine());

            if (sahar > 6.1)
                Console.WriteLine("Выше нормы");
        }
    }
}
```

**Пример:** при `7.2` → «Выше нормы», при `5.0` → ничего.

---

## №47. Хватает ли средств на проезд

**Условие:** Проверить, достаточно ли пользователю средств на счёте для оплаты проезда стоимостью 35 рублей.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите баланс: ");
            double bal = Convert.ToDouble(Console.ReadLine());

            if (bal >= 35)
                Console.WriteLine("Средств достаточно");
            else
                Console.WriteLine("Недостаточно средств");
        }
    }
}
```

**Пример:** при `100` → «Средств достаточно», при `20` → «Недостаточно средств».

---

## №48. Высотный этаж

**Условие:** Ввести номер этажа. Если этаж выше 10, вывести «Высотный этаж».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите этаж: ");
            int etazh = Convert.ToInt32(Console.ReadLine());

            if (etazh > 10)
                Console.WriteLine("Высотный этаж");
        }
    }
}
```

**Пример:** при `15` → «Высотный этаж», при `5` → ничего.

---

## №49. Одинаковы ли два слова по длине

**Условие:** Ввести два слова. Проверить, одинаковы ли они по длине.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первое слово: ");
            string s1 = Console.ReadLine();

            Console.Write("Введите второе слово: ");
            string s2 = Console.ReadLine();

            if (s1.Length == s2.Length)
                Console.WriteLine("Слова одинаковой длины");
            else
                Console.WriteLine("Слова разной длины");
        }
    }
}
```

**Пример:** при `кот` и `дом` → «Слова одинаковой длины», при `кот` и `собака` → «Слова разной длины».

---

## №50. Число чётное или нечётное

**Условие:** Пользователь вводит целое число. Вывести строковое сообщение: «Число четное» либо «Число нечетное».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 2 == 0)
                Console.WriteLine("Число четное");
            else
                Console.WriteLine("Число нечетное");
        }
    }
}
```

**Пример:** при `6` → «Число четное», при `7` → «Число нечетное».

## №51. Оценка по шкале ECTS

**Условие:** Ввести балл за тест (0–100). Вывести оценку по шкале ECTS: A (90–100), B (80–89), C (70–79), D (60–69), F (меньше 60).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите балл (0-100): ");
            int ball = Convert.ToInt32(Console.ReadLine());

            if (ball >= 90)
                Console.WriteLine("A");
            else if (ball >= 80)
                Console.WriteLine("B");
            else if (ball >= 70)
                Console.WriteLine("C");
            else if (ball >= 60)
                Console.WriteLine("D");
            else
                Console.WriteLine("F");
        }
    }
}
```

**Пример:** при `95` → «A», при `55` → «F».

---

## №52. Категория по возрасту

**Условие:** Ввести возраст человека. Определить категорию: ребёнок (0–12), подросток (13–17), взрослый (18–64), пожилой (65+).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите возраст: ");
            int age = Convert.ToInt32(Console.ReadLine());

            if (age <= 12)
                Console.WriteLine("Ребёнок");
            else if (age <= 17)
                Console.WriteLine("Подросток");
            else if (age <= 64)
                Console.WriteLine("Взрослый");
            else
                Console.WriteLine("Пожилой");
        }
    }
}
```

**Пример:** при `10` → «Ребёнок», при `30` → «Взрослый», при `70` → «Пожилой».

---

## №53. Агрегатное состояние воды

**Условие:** Ввести температуру воды. Вывести её агрегатное состояние: «Лёд» (≤ 0), «Жидкость» (0 < t < 100), «Пар» (≥ 100).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите температуру воды: ");
            double t = Convert.ToDouble(Console.ReadLine());

            if (t <= 0)
                Console.WriteLine("Лёд");
            else if (t < 100)
                Console.WriteLine("Жидкость");
            else
                Console.WriteLine("Пар");
        }
    }
}
```

**Пример:** при `-5` → «Лёд», при `50` → «Жидкость», при `120` → «Пар».

---

## №54. Уровень заряда аккумулятора

**Условие:** Уровень заряда аккумулятора смартфона (в %). Вывести: «Критический» (< 10), «Низкий» (10–20), «Нормальный» (21–80), «Полный» (81–100).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите заряд (%): ");
            int z = Convert.ToInt32(Console.ReadLine());

            if (z < 10)
                Console.WriteLine("Критический");
            else if (z <= 20)
                Console.WriteLine("Низкий");
            else if (z <= 80)
                Console.WriteLine("Нормальный");
            else
                Console.WriteLine("Полный");
        }
    }
}
```

**Пример:** при `5` → «Критический», при `50` → «Нормальный».

---

## №55. Режим работы двигателя

**Условие:** Ввести число оборотов двигателя в минуту. Вывести режим: «Заглушен» (0), «Холостой ход» (1–900), «Рабочий» (901–3500), «Красная зона» (3501+).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите обороты: ");
            int ob = Convert.ToInt32(Console.ReadLine());

            if (ob == 0)
                Console.WriteLine("Заглушен");
            else if (ob <= 900)
                Console.WriteLine("Холостой ход");
            else if (ob <= 3500)
                Console.WriteLine("Рабочий");
            else
                Console.WriteLine("Красная зона");
        }
    }
}
```

**Пример:** при `0` → «Заглушен», при `2000` → «Рабочий».

---

## №56. Подоходный налог

**Условие:** Ввести сумму дохода за год. Рассчитать подоходный налог: до 2,4 млн — 13%, до 5 млн — 15%, выше 5 млн — 18%.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите доход (млн): ");
            double dohod = Convert.ToDouble(Console.ReadLine());

            double nalog;

            if (dohod <= 2.4)
                nalog = dohod * 0.13;
            else if (dohod <= 5)
                nalog = dohod * 0.15;
            else
                nalog = dohod * 0.18;

            Console.WriteLine("Налог: " + nalog);
        }
    }
}
```

**Пример:** при `1` → «Налог: 0.13», при `6` → «Налог: 1.08».

---

## №57. Положение точки X на плоскости

**Условие:** По введённой координате X точки на плоскости (при Y = 0) определить её положение: на нуле, в положительной или отрицательной полуоси.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            if (x == 0)
                Console.WriteLine("На нуле");
            else if (x > 0)
                Console.WriteLine("В положительной полуоси");
            else
                Console.WriteLine("В отрицательной полуоси");
        }
    }
}
```

**Пример:** при `5` → «В положительной полуоси», при `-3` → «В отрицательной полуоси».

---

## №58. Индекс массы тела (ИМТ)

**Условие:** Ввести ИМТ. Вывести результат: недостаток веса (< 18.5), норма (18.5–24.9), избыток (25–29.9), ожирение (30+).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите ИМТ: ");
            double imt = Convert.ToDouble(Console.ReadLine());

            if (imt < 18.5)
                Console.WriteLine("Недостаток веса");
            else if (imt <= 24.9)
                Console.WriteLine("Норма");
            else if (imt <= 29.9)
                Console.WriteLine("Избыток");
            else
                Console.WriteLine("Ожирение");
        }
    }
}
```

**Пример:** при `17` → «Недостаток веса», при `22` → «Норма».

---

## №59. Скорость ветра по шкале

**Условие:** Ввести скорость ветра (м/с). Вывести измерение по шкале: штиль (< 0.2), лёгкий ветерок (0.2–5), умеренный (5.1–14), шторм (14.1–24), ураган (> 24).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите скорость ветра (м/с): ");
            double v = Convert.ToDouble(Console.ReadLine());

            if (v < 0.2)
                Console.WriteLine("Штиль");
            else if (v <= 5)
                Console.WriteLine("Лёгкий ветерок");
            else if (v <= 14)
                Console.WriteLine("Умеренный");
            else if (v <= 24)
                Console.WriteLine("Шторм");
            else
                Console.WriteLine("Ураган");
        }
    }
}
```

**Пример:** при `0.1` → «Штиль», при `30` → «Ураган».

---

## №60. Надбавка за стаж

**Условие:** Ввести стаж работы сотрудника (в годах). Вывести размер надбавки: < 1 года — 0%, 1–5 лет — 5%, 6–10 лет — 10%, > 10 лет — 15%.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите стаж (лет): ");
            int stazh = Convert.ToInt32(Console.ReadLine());

            if (stazh < 1)
                Console.WriteLine("0%");
            else if (stazh <= 5)
                Console.WriteLine("5%");
            else if (stazh <= 10)
                Console.WriteLine("10%");
            else
                Console.WriteLine("15%");
        }
    }
}
```

**Пример:** при `0` → «0%», при `7` → «10%», при `15` → «15%».

---

## №61. Время суток

**Условие:** Пользователь вводит текущее время (0–23). Вывести: «Ночь» (0–5), «Утро» (6–11), «День» (12–17), «Вечер» (18–23).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите часы (0-23): ");
            int h = Convert.ToInt32(Console.ReadLine());

            if (h <= 5)
                Console.WriteLine("Ночь");
            else if (h <= 11)
                Console.WriteLine("Утро");
            else if (h <= 17)
                Console.WriteLine("День");
            else
                Console.WriteLine("Вечер");
        }
    }
}
```

**Пример:** при `3` → «Ночь», при `15` → «День».

---

## №62. Толщина льда на водоёме

**Условие:** Ввести толщину льда (см). Вывести: «Выход запрещён» (< 7), «Одиночный пешеход» (7–12), «Группа людей» (13–20), «Транспорт» (> 20).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите толщину льда (см): ");
            double l = Convert.ToDouble(Console.ReadLine());

            if (l < 7)
                Console.WriteLine("Выход запрещён");
            else if (l <= 12)
                Console.WriteLine("Одиночный пешеход");
            else if (l <= 20)
                Console.WriteLine("Группа людей");
            else
                Console.WriteLine("Транспорт");
        }
    }
}
```

**Пример:** при `5` → «Выход запрещён», при `25` → «Транспорт».

---

## №63. Максимум из трёх чисел (каскадное условие)

**Условие:** Даны три целых числа A, B, C. Найти максимальное из них, используя каскадное условие.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите C: ");
            int c = Convert.ToInt32(Console.ReadLine());

            if (a >= b && a >= c)
                Console.WriteLine("Максимум: " + a);
            else if (b >= a && b >= c)
                Console.WriteLine("Максимум: " + b);
            else
                Console.WriteLine("Максимум: " + c);
        }
    }
}
```

**Пример:** при `3, 7, 5` → «Максимум: 7».

---

## №64. Минимум из трёх чисел

**Условие:** Даны три числа. Найти минимальное из них.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите C: ");
            int c = Convert.ToInt32(Console.ReadLine());

            if (a <= b && a <= c)
                Console.WriteLine("Минимум: " + a);
            else if (b <= a && b <= c)
                Console.WriteLine("Минимум: " + b);
            else
                Console.WriteLine("Минимум: " + c);
        }
    }
}
```

**Пример:** при `3, 7, 5` → «Минимум: 3».

---

## №65. Сколько из трёх чисел положительных

**Условие:** Даны три числа. Определить, сколько из них положительных (0, 1, 2 или 3).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите C: ");
            int c = Convert.ToInt32(Console.ReadLine());

            int count = 0;
            if (a > 0) count = count + 1;
            if (b > 0) count = count + 1;
            if (c > 0) count = count + 1;

            Console.WriteLine("Положительных: " + count);
        }
    }
}
```

**Пример:** при `-1, 5, 3` → «Положительных: 2».

---

## №66. Средний балл диплома

**Условие:** Ввести средний балл диплома. Вывести: «Без отличия» (< 4.5), «Претендент на красный диплом» (4.5–4.74), «Красный диплом» (≥ 4.75).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите средний балл: ");
            double s = Convert.ToDouble(Console.ReadLine());

            if (s < 4.5)
                Console.WriteLine("Без отличия");
            else if (s < 4.75)
                Console.WriteLine("Претендент на красный диплом");
            else
                Console.WriteLine("Красный диплом");
        }
    }
}
```

**Пример:** при `4.8` → «Красный диплом», при `4.6` → «Претендент на красный диплом».

---

## №67. Артериальное давление

**Условие:** Ввести значение артериального давления (систолическое). Вывести: гипотония (< 90), норма (90–120), предгипертензия (121–139), гипертензия (≥ 140).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите давление: ");
            int d = Convert.ToInt32(Console.ReadLine());

            if (d < 90)
                Console.WriteLine("Гипотония");
            else if (d <= 120)
                Console.WriteLine("Норма");
            else if (d <= 139)
                Console.WriteLine("Предгипертензия");
            else
                Console.WriteLine("Гипертензия");
        }
    }
}
```

**Пример:** при `80` → «Гипотония», при `150` → «Гипертензия».

---

## №68. Рейтинг шахматиста (Эло)

**Условие:** Ввести рейтинг шахматиста (Эло). Вывести ранг: любитель (< 1400), разрядник (1400–1999), мастер (2000–2399), гроссмейстер (≥ 2400).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите рейтинг Эло: ");
            int elo = Convert.ToInt32(Console.ReadLine());

            if (elo < 1400)
                Console.WriteLine("Любитель");
            else if (elo <= 1999)
                Console.WriteLine("Разрядник");
            else if (elo <= 2399)
                Console.WriteLine("Мастер");
            else
                Console.WriteLine("Гроссмейстер");
        }
    }
}
```

**Пример:** при `1200` → «Любитель», при `2500` → «Гроссмейстер».

---

## №69. Разрядность числа

**Условие:** Ввести число и определить, сколькозначным оно является (однозначное, двузначное, трёхзначное или более).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a < 0) a = -a;

            if (a < 10)
                Console.WriteLine("Однозначное");
            else if (a < 100)
                Console.WriteLine("Двузначное");
            else if (a < 1000)
                Console.WriteLine("Трёхзначное");
            else
                Console.WriteLine("Более трёхзначное");
        }
    }
}
```

**Пример:** при `5` → «Однозначное», при `1234` → «Более трёхзначное».

---

## №70. Стоимость поездки на такси

**Условие:** Ввести дальность поездки на такси (км). Рассчитать стоимость: до 5 км — 200 руб, от 5 до 15 км — 200 + 25 руб/км, свыше 15 км — 200 + 25·10 + 20·(км−15).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите расстояние (км): ");
            double km = Convert.ToDouble(Console.ReadLine());

            double stoim;

            if (km <= 5)
                stoim = 200;
            else if (km <= 15)
                stoim = 200 + (km - 5) * 25;
            else
                stoim = 200 + 10 * 25 + (km - 15) * 20;

            Console.WriteLine("Стоимость: " + stoim);
        }
    }
}
```

**Пример:** при `3` → «Стоимость: 200», при `20` → «Стоимость: 550».

---

## №71. Количество осадков

**Условие:** Ввести количество осадков за сутки (мм). Определить: без осадков (0), слабый дождь (0.1–4), умеренный (4.1–15), сильный ливень (> 15).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите осадки (мм): ");
            double os = Convert.ToDouble(Console.ReadLine());

            if (os == 0)
                Console.WriteLine("Без осадков");
            else if (os <= 4)
                Console.WriteLine("Слабый дождь");
            else if (os <= 15)
                Console.WriteLine("Умеренный");
            else
                Console.WriteLine("Сильный ливень");
        }
    }
}
```

**Пример:** при `0` → «Без осадков», при `20` → «Сильный ливень».

---

## №72. Процент выполнения плана продаж

**Условие:** Ввести процент выполнения плана продаж. Вывести статус: план сорван (< 70), удовлетворительно (70–99%), выполнено (100–119%), перевыполнен (≥ 120).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите процент: ");
            double p = Convert.ToDouble(Console.ReadLine());

            if (p < 70)
                Console.WriteLine("План сорван");
            else if (p < 100)
                Console.WriteLine("Удовлетворительно");
            else if (p < 120)
                Console.WriteLine("Выполнено");
            else
                Console.WriteLine("Перевыполнен");
        }
    }
}
```

**Пример:** при `50` → «План сорван», при `130` → «Перевыполнен».

---

## №73. Упорядочить три числа по возрастанию

**Условие:** Даны три числа. Упорядочить их по возрастанию и вывести на консоль.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите C: ");
            int c = Convert.ToInt32(Console.ReadLine());

            int temp;

            if (a > b)
            {
                temp = a;
                a = b;
                b = temp;
            }

            if (a > c)
            {
                temp = a;
                a = c;
                c = temp;
            }

            if (b > c)
            {
                temp = b;
                b = c;
                c = temp;
            }

            Console.WriteLine(a + " " + b + " " + c);
        }
    }
}
```

**Пример:** при `3, 1, 2` → «1 2 3».

---

## №74. Кусочная функция

**Условие:** Дано число X. Вычислить значение кусочно-заданной функции: f(x) = x², если x > 0; f(x) = 0, если x = 0; f(x) = −x, если x < 0.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите x: ");
            double x = Convert.ToDouble(Console.ReadLine());

            double f;

            if (x > 0)
                f = x * x;
            else if (x == 0)
                f = 0;
            else
                f = -x;

            Console.WriteLine("f(x) = " + f);
        }
    }
}
```

**Пример:** при `3` → «f(x) = 9», при `-4` → «f(x) = 4».

---

## №75. Октановое число бензина

**Условие:** Ввести октановое число бензина. Классифицировать: < 92 — несоответствие стандарту, 92 — АИ-92, 95 — АИ-95, 98–100 — АИ-98/100, > 100 — спорт/авиатопливо.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите октановое число: ");
            int o = Convert.ToInt32(Console.ReadLine());

            if (o < 92)
                Console.WriteLine("Несоответствие стандарту");
            else if (o == 92)
                Console.WriteLine("АИ-92");
            else if (o == 95)
                Console.WriteLine("АИ-95");
            else if (o <= 100)
                Console.WriteLine("АИ-98/100");
            else
                Console.WriteLine("Спорт/авиатопливо");
        }
    }
}
```

**Пример:** при `95` → «АИ-95», при `105` → «Спорт/авиатопливо».

---

## №76. Кешбэк за покупки

**Условие:** Ввести сумму покупок за месяц для начисления кешбэка: до 10 000 руб — 1%, до 50 000 руб — 3%, свыше 50 000 руб — 5%. Вывести сумму кешбэка.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите сумму покупок: ");
            double sum = Convert.ToDouble(Console.ReadLine());

            double cash;

            if (sum <= 10000)
                cash = sum * 0.01;
            else if (sum <= 50000)
                cash = sum * 0.03;
            else
                cash = sum * 0.05;

            Console.WriteLine("Кешбэк: " + cash);
        }
    }
}
```

**Пример:** при `5000` → «Кешбэк: 50», при `60000` → «Кешбэк: 3000».

---

## №77. Зона погружения аквалангиста

**Условие:** Ввести глубину погружения аквалангиста (метры). Вывести зону: рекреационная (< 40), техническая (40–100), глубоководная (> 100).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите глубину (м): ");
            double g = Convert.ToDouble(Console.ReadLine());

            if (g < 40)
                Console.WriteLine("Рекреационная");
            else if (g <= 100)
                Console.WriteLine("Техническая");
            else
                Console.WriteLine("Глубоководная");
        }
    }
}
```

**Пример:** при `30` → «Рекреационная», при `150` → «Глубоководная».

---

## №78. Штрафные баллы водителю

**Условие:** Ввести количество штрафных баллов водителю. Вывести: «Предупреждение» (1–5), «Временное ограничение» (6–10), «Лишение прав» (> 10).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите баллы: ");
            int b = Convert.ToInt32(Console.ReadLine());

            if (b >= 1 && b <= 5)
                Console.WriteLine("Предупреждение");
            else if (b <= 10)
                Console.WriteLine("Временное ограничение");
            else
                Console.WriteLine("Лишение прав");
        }
    }
}
```

**Пример:** при `3` → «Предупреждение», при `12` → «Лишение прав».

---

## №79. Уровень кислотности (pH)

**Условие:** Ввести уровень кислотности (pH). Определить: кислая (< 6.0), нейтральная (6.0–7.2), щелочная (> 7.2).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите pH: ");
            double ph = Convert.ToDouble(Console.ReadLine());

            if (ph < 6.0)
                Console.WriteLine("Кислая");
            else if (ph <= 7.2)
                Console.WriteLine("Нейтральная");
            else
                Console.WriteLine("Щелочная");
        }
    }
}
```

**Пример:** при `5` → «Кислая», при `8` → «Щелочная».

---

## №80. Медаль в компьютерной игре

**Условие:** Ввести количество набранных очков в компьютерной игре. Присвоить медаль: Бронзовая (1000–2499), Серебряная (2500–4999), Золотая (5000+), иначе без медали.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите очки: ");
            int o = Convert.ToInt32(Console.ReadLine());

            if (o >= 1000 && o <= 2499)
                Console.WriteLine("Бронзовая");
            else if (o >= 2500 && o <= 4999)
                Console.WriteLine("Серебряная");
            else if (o >= 5000)
                Console.WriteLine("Золотая");
            else
                Console.WriteLine("Без медали");
        }
    }
}
```

**Пример:** при `3000` → «Серебряная», при `500` → «Без медали».

---

## №81. Крепость напитка

**Условие:** Ввести крепость напитка в градусах. Классифицировать: безалкогольный (0), слабоалкогольный (0.1–8), среднеалкогольный (8.1–25), крепкий (> 25).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите крепость (%): ");
            double k = Convert.ToDouble(Console.ReadLine());

            if (k == 0)
                Console.WriteLine("Безалкогольный");
            else if (k <= 8)
                Console.WriteLine("Слабоалкогольный");
            else if (k <= 25)
                Console.WriteLine("Среднеалкогольный");
            else
                Console.WriteLine("Крепкий");
        }
    }
}
```

**Пример:** при `0` → «Безалкогольный», при `40` → «Крепкий».

---

## №82. Уровень шума

**Условие:** Ввести показатель уровня шума в децибелах (дБ). Вывести вердикт: тихо (< 40), норма (40–60), шумно (61–80), вредно для здоровья (> 80).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите шум (дБ): ");
            int sh = Convert.ToInt32(Console.ReadLine());

            if (sh < 40)
                Console.WriteLine("Тихо");
            else if (sh <= 60)
                Console.WriteLine("Норма");
            else if (sh <= 80)
                Console.WriteLine("Шумно");
            else
                Console.WriteLine("Вредно для здоровья");
        }
    }
}
```

**Пример:** при `30` → «Тихо», при `90` → «Вредно для здоровья».

---

## №83. Вес почтовой посылки

**Условие:** Ввести вес почтовой посылки (кг). Рассчитать категорию отправки: мелкий пакет (< 2), стандартная (2–10), тяжеловесная (10.1–31.5), крупногабаритная (> 31.5).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите вес (кг): ");
            double v = Convert.ToDouble(Console.ReadLine());

            if (v < 2)
                Console.WriteLine("Мелкий пакет");
            else if (v <= 10)
                Console.WriteLine("Стандартная");
            else if (v <= 31.5)
                Console.WriteLine("Тяжеловесная");
            else
                Console.WriteLine("Крупногабаритная");
        }
    }
}
```

**Пример:** при `5` → «Стандартная», при `40` → «Крупногабаритная».

---

## №84. Количество комнат в квартире

**Условие:** Ввести количество комнат в квартире. Вывести: студия/однокомнатная (1), двухкомнатная (2), трёхкомнатная (3), многокомнатная (4+).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите количество комнат: ");
            int k = Convert.ToInt32(Console.ReadLine());

            if (k == 1)
                Console.WriteLine("Студия/однокомнатная");
            else if (k == 2)
                Console.WriteLine("Двухкомнатная");
            else if (k == 3)
                Console.WriteLine("Трёхкомнатная");
            else
                Console.WriteLine("Многокомнатная");
        }
    }
}
```

**Пример:** при `2` → «Двухкомнатная», при `5` → «Многокомнатная».

---

## №85. Индикация заряда повербанка

**Условие:** Ввести процент заряда повербанка. Вывести количество светящихся светодиодов в корпусе (1, 2, 3 или 4).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите заряд (%): ");
            int z = Convert.ToInt32(Console.ReadLine());

            if (z <= 25)
                Console.WriteLine("1 диод");
            else if (z <= 50)
                Console.WriteLine("2 диода");
            else if (z <= 75)
                Console.WriteLine("3 диода");
            else
                Console.WriteLine("4 диода");
        }
    }
}
```

**Пример:** при `40` → «2 диода», при `90` → «4 диода».

---

## №86. Пенсионная надбавка за выслугу лет

**Условие:** Ввести выслугу лет военнослужащего. Вывести процент пенсионной надбавки.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите выслугу (лет): ");
            int v = Convert.ToInt32(Console.ReadLine());

            if (v < 5)
                Console.WriteLine("10%");
            else if (v < 10)
                Console.WriteLine("15%");
            else if (v < 15)
                Console.WriteLine("20%");
            else
                Console.WriteLine("25%");
        }
    }
}
```

**Пример:** при `3` → «10%», при `12` → «20%».

---

## №87. Время ответа сервера (пинг)

**Условие:** Ввести время ответа сервера (пинг в мс). Вывести: Идеально (< 20), Хороший (20–60), Посредственный (61–120), Плохой (> 120).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите пинг (мс): ");
            int p = Convert.ToInt32(Console.ReadLine());

            if (p < 20)
                Console.WriteLine("Идеально");
            else if (p <= 60)
                Console.WriteLine("Хороший");
            else if (p <= 120)
                Console.WriteLine("Посредственный");
            else
                Console.WriteLine("Плохой");
        }
    }
}
```

**Пример:** при `10` → «Идеально», при `150` → «Плохой».

---

## №88. Концентрация CO2 в помещении

**Условие:** Ввести концентрацию CO2 в помещении (ppm). Вывести вердикт: норма (< 800), душно (800–1200), проветрить немедленно (> 1200).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите CO2 (ppm): ");
            int c = Convert.ToInt32(Console.ReadLine());

            if (c < 800)
                Console.WriteLine("Норма");
            else if (c <= 1200)
                Console.WriteLine("Душно");
            else
                Console.WriteLine("Проветрить немедленно!");
        }
    }
}
```

**Пример:** при `500` → «Норма», при `1500` → «Проветрить немедленно!».

---

## №89. Количество шагов за день

**Условие:** Ввести количество пройденных шагов за день. Вывести: гиподинамия (< 5000), норма (5000–9999), активный день (10000–14999), рекорд (> 15000).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите количество шагов: ");
            int sh = Convert.ToInt32(Console.ReadLine());

            if (sh < 5000)
                Console.WriteLine("Гиподинамия");
            else if (sh <= 9999)
                Console.WriteLine("Норма");
            else if (sh <= 14999)
                Console.WriteLine("Активный день");
            else
                Console.WriteLine("Рекорд");
        }
    }
}
```

**Пример:** при `3000` → «Гиподинамия», при `16000` → «Рекорд».

---

## №90. Класс автомобиля по диаметру диска

**Условие:** Ввести диаметр автомобильного колёсного диска в дюймах. Определить класс: малолитражки (13–14), компактные авто (15–16), кроссоверы/бизнес (17–19), внедорожники/спорт (20+).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите диаметр (дюймы): ");
            int d = Convert.ToInt32(Console.ReadLine());

            if (d >= 13 && d <= 14)
                Console.WriteLine("Малолитражки");
            else if (d >= 15 && d <= 16)
                Console.WriteLine("Компактные авто");
            else if (d >= 17 && d <= 19)
                Console.WriteLine("Кроссоверы/бизнес");
            else
                Console.WriteLine("Внедорожники/спорт");
        }
    }
}
```

**Пример:** при `15` → «Компактные авто», при `21` → «Внедорожники/спорт».

---

## №91. Влажность воздуха

**Условие:** Ввести влажность воздуха (%). Вывести: сухой воздух (< 30), комфорт (30–60), повышенная влажность (> 60).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите влажность (%): ");
            int v = Convert.ToInt32(Console.ReadLine());

            if (v < 30)
                Console.WriteLine("Сухой воздух");
            else if (v <= 60)
                Console.WriteLine("Комфорт");
            else
                Console.WriteLine("Повышенная влажность");
        }
    }
}
```

**Пример:** при `20` → «Сухой воздух», при `80` → «Повышенная влажность».

---

## №92. Сколько различных чисел среди трёх

**Условие:** Даны три числа. Проверить, сколько из них различных между собой (все разные, два равны, все три равны).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите C: ");
            int c = Convert.ToInt32(Console.ReadLine());

            int raznyh = 1;
            if (b != a) raznyh = raznyh + 1;
            if (c != a && c != b) raznyh = raznyh + 1;

            Console.WriteLine("Различных чисел: " + raznyh);
        }
    }
}
```

**Пример:** при `1, 2, 3` → «Различных чисел: 3», при `1, 1, 2` → «Различных чисел: 2».

---

## №93. Четверть координатной плоскости

**Условие:** Ввести номер четверти координатной плоскости (1–4) и вывести диапазоны знаков для координат X и Y.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите четверть (1-4): ");
            int n = Convert.ToInt32(Console.ReadLine());

            if (n == 1)
                Console.WriteLine("X > 0, Y > 0");
            else if (n == 2)
                Console.WriteLine("X < 0, Y > 0");
            else if (n == 3)
                Console.WriteLine("X < 0, Y < 0");
            else if (n == 4)
                Console.WriteLine("X > 0, Y < 0");
            else
                Console.WriteLine("Неверный номер четверти");
        }
    }
}
```

**Пример:** при `1` → «X > 0, Y > 0», при `3` → «X < 0, Y < 0».

---

## №94. Температура процессора

**Условие:** Ввести температуру процессора компьютера. Вывести: холодный (< 45), нормальная нагрузка (45–75), троттлинг/перегрев (> 75).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите температуру (°C): ");
            int t = Convert.ToInt32(Console.ReadLine());

            if (t < 45)
                Console.WriteLine("Холодный");
            else if (t <= 75)
                Console.WriteLine("Нормальная нагрузка");
            else
                Console.WriteLine("Троттлинг/перегрев");
        }
    }
}
```

**Пример:** при `30` → «Холодный», при `90` → «Троттлинг/перегрев».

---

## №95. Срок годности продукта

**Условие:** Ввести остаток срока годности продукта в днях. Вывести: «Срочно употребить» (≤ 2), «Нормально» (3–30), «Длительное хранение» (> 30).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите количество дней: ");
            int d = Convert.ToInt32(Console.ReadLine());

            if (d <= 2)
                Console.WriteLine("Срочно употребить");
            else if (d <= 30)
                Console.WriteLine("Нормально");
            else
                Console.WriteLine("Длительное хранение");
        }
    }
}
```

**Пример:** при `1` → «Срочно употребить», при `100` → «Длительное хранение».

---

## №96. Процентная ставка по кредиту

**Условие:** Ввести сумму кредита и срок. Рассчитать процентную ставку в зависимости от срока (до года, до трёх лет, свыше трёх лет).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите срок кредита (лет): ");
            double srok = Convert.ToDouble(Console.ReadLine());

            double stavka;

            if (srok <= 1)
                stavka = 15;
            else if (srok <= 3)
                stavka = 12;
            else
                stavka = 10;

            Console.WriteLine("Ставка: " + stavka + "%");
        }
    }
}
```

**Пример:** при `0.5` → «Ставка: 15%», при `5` → «Ставка: 10%».

---

## №97. Класс монитора по частоте обновления

**Условие:** Ввести частоту обновления монитора (Гц). Определить: офис (60–75), базовый игровой (120–144), киберспорт (165+).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите частоту (Гц): ");
            int hz = Convert.ToInt32(Console.ReadLine());

            if (hz >= 60 && hz <= 75)
                Console.WriteLine("Офис");
            else if (hz >= 120 && hz <= 144)
                Console.WriteLine("Базовый игровой");
            else if (hz >= 165)
                Console.WriteLine("Киберспорт");
            else
                Console.WriteLine("Неизвестная категория");
        }
    }
}
```

**Пример:** при `70` → «Офис», при `170` → «Киберспорт».

---

## №98. Расход топлива автомобиля

**Условие:** Ввести расход топлива автомобиля на 100 км пути. Вывести вердикт: экономичный (< 6 л), средний (6–10 л), прожорливый (> 10 л).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите расход (л/100 км): ");
            double r = Convert.ToDouble(Console.ReadLine());

            if (r < 6)
                Console.WriteLine("Экономичный");
            else if (r <= 10)
                Console.WriteLine("Средний");
            else
                Console.WriteLine("Прожорливый");
        }
    }
}
```

**Пример:** при `5` → «Экономичный», при `15` → «Прожорливый».

---

## №99. Классификация книги по количеству страниц

**Условие:** Ввести количество страниц книги. Классифицировать: брошюра (< 48), повесть (48–150), роман (151–600), фолиант (> 600).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите количество страниц: ");
            int s = Convert.ToInt32(Console.ReadLine());

            if (s < 48)
                Console.WriteLine("Брошюра");
            else if (s <= 150)
                Console.WriteLine("Повесть");
            else if (s <= 600)
                Console.WriteLine("Роман");
            else
                Console.WriteLine("Фолиант");
        }
    }
}
```

**Пример:** при `30` → «Брошюра», при `1000` → «Фолиант».

---

## №100. Принадлежность числа интервалам

**Условие:** Ввести число и проверить, входит ли оно в интервалы [0; 10], [20; 30] или [50; 100].

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if ((a >= 0 && a <= 10) || (a >= 20 && a <= 30) || (a >= 50 && a <= 100))
                Console.WriteLine("Число входит в один из интервалов");
            else
                Console.WriteLine("Число не входит ни в один интервал");
        }
    }
}
```

**Пример:** при `25` → «Число входит в один из интервалов», при `40` → «Число не входит ни в один интервал».

## №101. Принадлежность числа отрезку [10; 50]

**Условие:** Дано целое число. Проверить, принадлежит ли оно числовому отрезку [10; 50].

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a >= 10 && a <= 50)
                Console.WriteLine("Входит в отрезок");
            else
                Console.WriteLine("Не входит в отрезок");
        }
    }
}
```

**Пример:** при `25` → «Входит в отрезок», при `5` → «Не входит в отрезок».

---

## №102. Положительное и чётное одновременно

**Условие:** Проверить, является ли введённое число положительным и чётным одновременно.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a > 0 && a % 2 == 0)
                Console.WriteLine("Да");
            else
                Console.WriteLine("Нет");
        }
    }
}
```

**Пример:** при `8` → «Да», при `-4` → «Нет».

---

## №103. Число вне отрезка [−10; 10]

**Условие:** Проверить, лежит ли число вне отрезка [−10; 10].

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a < -10 || a > 10)
                Console.WriteLine("Вне отрезка");
            else
                Console.WriteLine("Внутри отрезка");
        }
    }
}
```

**Пример:** при `15` → «Вне отрезка», при `5` → «Внутри отрезка».

---

## №104. Логин и пароль

**Условие:** Ввести логин и пароль пользователя. Вывести «Успех», если логин равен `admin` и пароль `secret`.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите логин: ");
            string login = Console.ReadLine();

            Console.Write("Введите пароль: ");
            string parol = Console.ReadLine();

            if (login == "admin" && parol == "secret")
                Console.WriteLine("Успех");
            else
                Console.WriteLine("Ошибка");
        }
    }
}
```

**Пример:** при `admin` и `secret` → «Успех», при других → «Ошибка».

---

## №105. Високосный год

**Условие:** Проверить, является ли введённый год високосным (делится на 4, но не на 100, либо делится на 400).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите год: ");
            int god = Convert.ToInt32(Console.ReadLine());

            if ((god % 4 == 0 && god % 100 != 0) || god % 400 == 0)
                Console.WriteLine("Високосный");
            else
                Console.WriteLine("Не високосный");
        }
    }
}
```

**Пример:** при `2024` → «Високосный», при `2023` → «Не високосный».

---

## №106. Точка в I четверти

**Условие:** Даны координаты точки (X, Y). Определить, находится ли точка в I координатной четверти (X > 0 и Y > 0).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y: ");
            double y = Convert.ToDouble(Console.ReadLine());

            if (x > 0 && y > 0)
                Console.WriteLine("Точка в I четверти");
            else
                Console.WriteLine("Точка не в I четверти");
        }
    }
}
```

**Пример:** при `3, 5` → «Точка в I четверти», при `-3, 5` → «Точка не в I четверти».

---

## №107. Точка во II четверти

**Условие:** Определить, находится ли точка (X, Y) во II четверти плоскости.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y: ");
            double y = Convert.ToDouble(Console.ReadLine());

            if (x < 0 && y > 0)
                Console.WriteLine("Точка во II четверти");
            else
                Console.WriteLine("Точка не во II четверти");
        }
    }
}
```

**Пример:** при `-3, 5` → «Точка во II четверти».

---

## №108. Точка в III четверти

**Условие:** Определить, находится ли точка (X, Y) в III четверти плоскости.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y: ");
            double y = Convert.ToDouble(Console.ReadLine());

            if (x < 0 && y < 0)
                Console.WriteLine("Точка в III четверти");
            else
                Console.WriteLine("Точка не в III четверти");
        }
    }
}
```

**Пример:** при `-3, -5` → «Точка в III четверти».

---

## №109. Точка в IV четверти

**Условие:** Определить, находится ли точка (X, Y) в IV четверти плоскости.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y: ");
            double y = Convert.ToDouble(Console.ReadLine());

            if (x > 0 && y < 0)
                Console.WriteLine("Точка в IV четверти");
            else
                Console.WriteLine("Точка не в IV четверти");
        }
    }
}
```

**Пример:** при `3, -5` → «Точка в IV четверти».

---

## №110. Прямоугольный треугольник

**Условие:** Даны три стороны A, B, C. Проверить, является ли треугольник прямоугольным (теорема Пифагора).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите сторону A: ");
            double a = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите сторону B: ");
            double b = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите сторону C: ");
            double c = Convert.ToDouble(Console.ReadLine());

            if (a * a + b * b == c * c || a * a + c * c == b * b || b * b + c * c == a * a)
                Console.WriteLine("Треугольник прямоугольный");
            else
                Console.WriteLine("Треугольник не прямоугольный");
        }
    }
}
```

**Пример:** при `3, 4, 5` → «Треугольник прямоугольный».

---

## №111. Равнобедренный треугольник

**Условие:** Даны три стороны. Проверить, является ли треугольник равнобедренным.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите сторону A: ");
            double a = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите сторону B: ");
            double b = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите сторону C: ");
            double c = Convert.ToDouble(Console.ReadLine());

            if (a == b || a == c || b == c)
                Console.WriteLine("Треугольник равнобедренный");
            else
                Console.WriteLine("Треугольник не равнобедренный");
        }
    }
}
```

**Пример:** при `5, 5, 3` → «Треугольник равнобедренный».

---

## №112. Аренда каршеринга бизнес-класса

**Условие:** Ввести возраст и стаж работы. Разрешить аренду каршеринга бизнес-класса, если возраст ≥ 23 лет И стаж ≥ 3 лет.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите возраст: ");
            int vozr = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите стаж (лет): ");
            int stazh = Convert.ToInt32(Console.ReadLine());

            if (vozr >= 23 && stazh >= 3)
                Console.WriteLine("Аренда разрешена");
            else
                Console.WriteLine("Аренда запрещена");
        }
    }
}
```

**Пример:** при `25` и `5` → «Аренда разрешена».

---

## №113. Число делится на 3 и на 5

**Условие:** Проверить, делится ли число одновременно на 3 и на 5 без остатка.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a % 3 == 0 && a % 5 == 0)
                Console.WriteLine("Делится на 3 и на 5");
            else
                Console.WriteLine("Не делится на 3 и на 5");
        }
    }
}
```

**Пример:** при `15` → «Делится на 3 и на 5».

---

## №114. Число трёхзначное и оканчивается на 5

**Условие:** Проверить, является ли число трёхзначным и оканчивается ли оно на цифру 5.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if (a >= 100 && a <= 999 && a % 10 == 5)
                Console.WriteLine("Да");
            else
                Console.WriteLine("Нет");
        }
    }
}
```

**Пример:** при `125` → «Да», при `25` → «Нет».

---

## №115. Числа по возрастанию

**Условие:** Даны три числа. Проверить, расположены ли они строго по возрастанию (A < B < C).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите C: ");
            int c = Convert.ToInt32(Console.ReadLine());

            if (a < b && b < c)
                Console.WriteLine("Расположены по возрастанию");
            else
                Console.WriteLine("Не расположены по возрастанию");
        }
    }
}
```

**Пример:** при `1, 2, 3` → «Расположены по возрастанию».

---

## №116. Хотя бы одно чётное среди трёх

**Условие:** Проверить, верно ли, что среди введённых трёх чисел есть хотя бы одно чётное.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите C: ");
            int c = Convert.ToInt32(Console.ReadLine());

            if (a % 2 == 0 || b % 2 == 0 || c % 2 == 0)
                Console.WriteLine("Есть хотя бы одно чётное");
            else
                Console.WriteLine("Нет чётных");
        }
    }
}
```

**Пример:** при `1, 3, 4` → «Есть хотя бы одно чётное».

---

## №117. Ровно одна пара равных чисел

**Условие:** Проверить, верно ли, что среди трёх чисел ровно одна пара равна.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите C: ");
            int c = Convert.ToInt32(Console.ReadLine());

            int par = 0;
            if (a == b) par = par + 1;
            if (a == c) par = par + 1;
            if (b == c) par = par + 1;

            if (par == 1)
                Console.WriteLine("Ровно одна пара равна");
            else
                Console.WriteLine("Не ровно одна пара");
        }
    }
}
```

**Пример:** при `1, 1, 2` → «Ровно одна пара равна».

---

## №118. Гололедица

**Условие:** Ввести температуру и влажность. Вывести предупреждение о гололедице, если температура ≤ 0 °C И влажность > 85%.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите температуру: ");
            double t = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите влажность: ");
            double v = Convert.ToDouble(Console.ReadLine());

            if (t <= 0 && v > 85)
                Console.WriteLine("Гололедица!");
            else
                Console.WriteLine("Без гололедицы");
        }
    }
}
```

**Пример:** при `-5` и `90` → «Гололедица!».

---

## №119. Точка внутри круга

**Условие:** Даны координаты точки (X, Y). Проверить, лежит ли точка внутри круга радиуса R с центром в начале координат (x² + y² ≤ R²).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y: ");
            double y = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите R: ");
            double r = Convert.ToDouble(Console.ReadLine());

            if (x * x + y * y <= r * r)
                Console.WriteLine("Точка внутри круга");
            else
                Console.WriteLine("Точка снаружи круга");
        }
    }
}
```

**Пример:** при `3, 4` и `R = 6` → «Точка внутри круга».

---

## №120. Точка внутри прямоугольника

**Условие:** Даны координаты точки (X, Y). Проверить, лежит ли точка внутри прямоугольника со сторонами, параллельными осям, заданного углами (X1, Y1) и (X2, Y2).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y: ");
            double y = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите X1: ");
            double x1 = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y1: ");
            double y1 = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите X2: ");
            double x2 = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y2: ");
            double y2 = Convert.ToDouble(Console.ReadLine());

            if (x >= x1 && x <= x2 && y >= y1 && y <= y2)
                Console.WriteLine("Точка внутри прямоугольника");
            else
                Console.WriteLine("Точка снаружи прямоугольника");
        }
    }
}
```

**Пример:** при `3, 3` и углах `1, 1` и `5, 5` → «Точка внутри прямоугольника».

---

## №121. Правильность даты

**Условие:** Ввести день и месяц рождения. Проверить правильность даты (день от 1 до 31, месяц от 1 до 12).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите день: ");
            int den = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите месяц: ");
            int mes = Convert.ToInt32(Console.ReadLine());

            if (den >= 1 && den <= 31 && mes >= 1 && mes <= 12)
                Console.WriteLine("Дата корректна");
            else
                Console.WriteLine("Дата некорректна");
        }
    }
}
```

**Пример:** при `15` и `6` → «Дата корректна».

---

## №122. Зимний месяц

**Условие:** Ввести номер месяца. Проверить, относится ли он к зимнему периоду (12, 1 или 2).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите месяц: ");
            int m = Convert.ToInt32(Console.ReadLine());

            if (m == 12 || m == 1 || m == 2)
                Console.WriteLine("Зимний месяц");
            else
                Console.WriteLine("Не зимний месяц");
        }
    }
}
```

**Пример:** при `1` → «Зимний месяц», при `7` → «Не зимний месяц».

---

## №123. Счастливый билет

**Условие:** Проверить, является ли четырёхзначное число «счастливым билетом» (сумма первых двух цифр равна сумме двух последних).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите четырёхзначное число: ");
            int b = Convert.ToInt32(Console.ReadLine());

            int d1 = b / 1000;
            int d2 = (b / 100) % 10;
            int d3 = (b / 10) % 10;
            int d4 = b % 10;

            if (d1 + d2 == d3 + d4)
                Console.WriteLine("Счастливый билет");
            else
                Console.WriteLine("Не счастливый билет");
        }
    }
}
```

**Пример:** при `1236` → «Счастливый билет», при `1234` → «Не счастливый билет».

---

## №124. Пара взаимно противоположных чисел

**Условие:** Ввести три числа. Проверить истинность высказывания: «Хотя бы одна пара чисел взаимно противоположна (A = −B)».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите C: ");
            int c = Convert.ToInt32(Console.ReadLine());

            if (a == -b || a == -c || b == -c)
                Console.WriteLine("Есть пара противоположных");
            else
                Console.WriteLine("Нет пары противоположных");
        }
    }
}
```

**Пример:** при `5, -5, 3` → «Есть пара противоположных».

---

## №125. Датчики аварии и тумблер защиты

**Условие:** Пользователь вводит состояние двух датчиков аварии. Сформировать тревогу, если сработал хотя бы один датчик И при этом включён тумблер защиты.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Датчик 1 сработал? (да/нет): ");
            string o1 = Console.ReadLine();

            Console.Write("Датчик 2 сработал? (да/нет): ");
            string o2 = Console.ReadLine();

            Console.Write("Тумблер защиты включён? (да/нет): ");
            string o3 = Console.ReadLine();

            bool d1 = (o1 == "да");
            bool d2 = (o2 == "да");
            bool tumb = (o3 == "да");

            if ((d1 || d2) && tumb)
                Console.WriteLine("ТРЕВОГА!");
            else
                Console.WriteLine("Всё спокойно");
        }
    }
}
```

**Пример:** при `да, нет, да` → «ТРЕВОГА!».

---

## №126. X строго между A и B

**Условие:** Проверить, лежит ли число X строго между числами A и B (учесть, что A может быть больше B).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите A: ");
            double a = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите B: ");
            double b = Convert.ToDouble(Console.ReadLine());

            double minAB = Math.Min(a, b);
            double maxAB = Math.Max(a, b);

            if (x > minAB && x < maxAB)
                Console.WriteLine("X между A и B");
            else
                Console.WriteLine("X не между A и B");
        }
    }
}
```

**Пример:** при `5, 1, 10` → «X между A и B».

---

## №127. Одинаковый знак двух чисел

**Условие:** Даны два целых числа. Проверить, имеют ли они одинаковый знак (оба положительные или оба отрицательные).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            int a = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите B: ");
            int b = Convert.ToInt32(Console.ReadLine());

            if ((a > 0 && b > 0) || (a < 0 && b < 0))
                Console.WriteLine("Одинаковый знак");
            else
                Console.WriteLine("Разные знаки");
        }
    }
}
```

**Пример:** при `5, 7` → «Одинаковый знак», при `5, -7` → «Разные знаки».

---

## №128. Угроза от ладьи

**Условие:** Даны шахматные координаты двух клеток (x1, y1) и (x2, y2) от 1 до 8. Определить, угрожает ли ладья с первой клетки второй (совпадает либо строка, либо столбец).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите x1: ");
            int x1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y1: ");
            int y1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите x2: ");
            int x2 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y2: ");
            int y2 = Convert.ToInt32(Console.ReadLine());

            if (x1 == x2 || y1 == y2)
                Console.WriteLine("Ладья угрожает");
            else
                Console.WriteLine("Ладья не угрожает");
        }
    }
}
```

**Пример:** при `1, 1, 1, 5` → «Ладья угрожает».

---

## №129. Угроза от слона

**Условие:** Для двух клеток шахматной доски определить, угрожает ли слон (разность координат по модулю одинакова).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите x1: ");
            int x1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y1: ");
            int y1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите x2: ");
            int x2 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y2: ");
            int y2 = Convert.ToInt32(Console.ReadLine());

            if (Math.Abs(x1 - x2) == Math.Abs(y1 - y2))
                Console.WriteLine("Слон угрожает");
            else
                Console.WriteLine("Слон не угрожает");
        }
    }
}
```

**Пример:** при `1, 1, 4, 4` → «Слон угрожает».

---

## №130. Угроза от ферзя

**Условие:** Для двух клеток шахматной доски определить, угрожает ли ферзь (объединение логики ладьи и слона).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите x1: ");
            int x1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y1: ");
            int y1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите x2: ");
            int x2 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y2: ");
            int y2 = Convert.ToInt32(Console.ReadLine());

            if (x1 == x2 || y1 == y2 || Math.Abs(x1 - x2) == Math.Abs(y1 - y2))
                Console.WriteLine("Ферзь угрожает");
            else
                Console.WriteLine("Ферзь не угрожает");
        }
    }
}
```

**Пример:** при `1, 1, 4, 4` → «Ферзь угрожает».

---

## №131. Ход конём

**Условие:** Для двух клеток шахматной доски определить, может ли конь пойти с одной на другую.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите x1: ");
            int x1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y1: ");
            int y1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите x2: ");
            int x2 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y2: ");
            int y2 = Convert.ToInt32(Console.ReadLine());

            int dx = Math.Abs(x1 - x2);
            int dy = Math.Abs(y1 - y2);

            if ((dx == 2 && dy == 1) || (dx == 1 && dy == 2))
                Console.WriteLine("Конь может пойти");
            else
                Console.WriteLine("Конь не может пойти");
        }
    }
}
```

**Пример:** при `1, 1, 2, 3` → «Конь может пойти».

---

## №132. Одинаковый цвет клеток

**Условие:** Для двух клеток шахматной доски проверить, одного ли они цвета.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите x1: ");
            int x1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y1: ");
            int y1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите x2: ");
            int x2 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите y2: ");
            int y2 = Convert.ToInt32(Console.ReadLine());

            if ((x1 + y1) % 2 == (x2 + y2) % 2)
                Console.WriteLine("Одинаковый цвет");
            else
                Console.WriteLine("Разный цвет");
        }
    }
}
```

**Пример:** при `1, 1, 3, 3` → «Одинаковый цвет».

---

## №133. Космонавт: рост и вес

**Условие:** Ввести рост и вес кандидата в космонавты. Проверить соответствие: рост от 160 до 190 см и вес от 50 до 90 кг.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите рост (см): ");
            int rost = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите вес (кг): ");
            int ves = Convert.ToInt32(Console.ReadLine());

            if (rost >= 160 && rost <= 190 && ves >= 50 && ves <= 90)
                Console.WriteLine("Подходит");
            else
                Console.WriteLine("Не подходит");
        }
    }
}
```

**Пример:** при `175` и `70` → «Подходит».

---

## №134. Чётное двузначное число

**Условие:** Дано натуральное число N. Проверить, является ли оно чётным двузначным числом.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int n = Convert.ToInt32(Console.ReadLine());

            if (n >= 10 && n <= 99 && n % 2 == 0)
                Console.WriteLine("Да");
            else
                Console.WriteLine("Нет");
        }
    }
}
```

**Пример:** при `24` → «Да», при `23` → «Нет».

---

## №135. Нечётное трёхзначное число

**Условие:** Дано натуральное число. Проверить, является ли оно нечётным трёхзначным числом.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int n = Convert.ToInt32(Console.ReadLine());

            if (n >= 100 && n <= 999 && n % 2 != 0)
                Console.WriteLine("Да");
            else
                Console.WriteLine("Нет");
        }
    }
}
```

**Пример:** при `123` → «Да», при `124` → «Нет».

---

## №136. Абитуриент засчитан

**Условие:** Ввести результаты двух экзаменов (математика и информатика). Абитуриент засчитан, если сумма баллов ≥ 150 И по каждому предмету не менее 50 баллов.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите балл по математике: ");
            int mat = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите балл по информатике: ");
            int inf = Convert.ToInt32(Console.ReadLine());

            if (mat + inf >= 150 && mat >= 50 && inf >= 50)
                Console.WriteLine("Засчитан");
            else
                Console.WriteLine("Не засчитан");
        }
    }
}
```

**Пример:** при `80` и `80` → «Засчитан».

---

## №137. Точка в круговом кольце

**Условие:** Проверить, лежит ли точка с координатами (X, Y) в круговом кольце с внутренним радиусом R1 и внешним R2.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y: ");
            double y = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите R1: ");
            double r1 = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите R2: ");
            double r2 = Convert.ToDouble(Console.ReadLine());

            double dist = Math.Sqrt(x * x + y * y);

            if (dist >= r1 && dist <= r2)
                Console.WriteLine("Точка в кольце");
            else
                Console.WriteLine("Точка не в кольце");
        }
    }
}
```

**Пример:** при `3, 4` и `R1 = 2, R2 = 6` → «Точка в кольце».

---

## №138. Билет и багаж

**Условие:** Ввести статус билета (да/нет) и наличие багажа (да/нет). Вывести: требуется ли дополнительная оплата багажа.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Билет есть? (да/нет): ");
            string o1 = Console.ReadLine();

            Console.Write("Багаж есть? (да/нет): ");
            string o2 = Console.ReadLine();

            bool bilet = (o1 == "да");
            bool bagazh = (o2 == "да");

            if (bilet && bagazh)
                Console.WriteLine("Требуется дополнительная оплата багажа");
            else
                Console.WriteLine("Дополнительная оплата не требуется");
        }
    }
}
```

**Пример:** при `да, да` → «Требуется дополнительная оплата багажа».

---

## №139. Палиндром (четырёхзначное число)

**Условие:** Дано четырёхзначное число. Проверить, читается ли оно слева направо и справа налево одинаково (палиндром).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите четырёхзначное число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            int d1 = a / 1000;
            int d2 = (a / 100) % 10;
            int d3 = (a / 10) % 10;
            int d4 = a % 10;

            if (d1 == d4 && d2 == d3)
                Console.WriteLine("Палиндром");
            else
                Console.WriteLine("Не палиндром");
        }
    }
}
```

**Пример:** при `1221` → «Палиндром», при `1234` → «Не палиндром».

---

## №140. Стабильность сети

**Условие:** Ввести напряжение сети (В) и частоту (Гц). Норма: 220 В ± 10% и 50 Гц ± 1 Гц. Вывести статус стабильности сети.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите напряжение (В): ");
            double u = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите частоту (Гц): ");
            double f = Convert.ToDouble(Console.ReadLine());

            if (u >= 198 && u <= 242 && f >= 49 && f <= 51)
                Console.WriteLine("Сеть стабильна");
            else
                Console.WriteLine("Сеть нестабильна");
        }
    }
}
```

**Пример:** при `220` и `50` → «Сеть стабильна».

---

## №141. Выезд за границу

**Условие:** Ввести наличие прав (да/нет), страховки (да/нет) и трезвости водителя (да/нет). Разрешить выезд только при соблюдении всех трёх факторов.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Права есть? (да/нет): ");
            string o1 = Console.ReadLine();

            Console.Write("Страховка есть? (да/нет): ");
            string o2 = Console.ReadLine();

            Console.Write("Трезвый? (да/нет): ");
            string o3 = Console.ReadLine();

            bool prava = (o1 == "да");
            bool strah = (o2 == "да");
            bool trezv = (o3 == "да");

            if (prava && strah && trezv)
                Console.WriteLine("Выезд разрешён");
            else
                Console.WriteLine("Выезд запрещён");
        }
    }
}
```

**Пример:** при `да, да, да` → «Выезд разрешён».

---

## №142. Делится на 4 или на 7, но не на 28

**Условие:** Проверить, делится ли число на 4 ИЛИ на 7, но НЕ делится на 28.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            if ((a % 4 == 0 || a % 7 == 0) && a % 28 != 0)
                Console.WriteLine("Подходит");
            else
                Console.WriteLine("Не подходит");
        }
    }
}
```

**Пример:** при `8` → «Подходит», при `28` → «Не подходит».

---

## №143. Аномальная температура летом

**Условие:** Ввести текущий месяц и температуру. Вывести аномалию, если месяц летний (6, 7, 8), а температура ниже нуля.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите месяц: ");
            int m = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите температуру: ");
            double t = Convert.ToDouble(Console.ReadLine());

            if ((m == 6 || m == 7 || m == 8) && t < 0)
                Console.WriteLine("Аномалия!");
            else
                Console.WriteLine("Норма");
        }
    }
}
```

**Пример:** при `7` и `-5` → «Аномалия!».

---

## №144. Мажоритарный клапан

**Условие:** Даны три логические переменные A, B, C. Реализовать проверку формулы мажоритарного клапана: «Истинно, если хотя бы две из трёх переменных истинны».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("A (да/нет): ");
            string o1 = Console.ReadLine();

            Console.Write("B (да/нет): ");
            string o2 = Console.ReadLine();

            Console.Write("C (да/нет): ");
            string o3 = Console.ReadLine();

            bool a = (o1 == "да");
            bool b = (o2 == "да");
            bool c = (o3 == "да");

            int istin = 0;
            if (a) istin = istin + 1;
            if (b) istin = istin + 1;
            if (c) istin = istin + 1;

            if (istin >= 2)
                Console.WriteLine("Истинно");
            else
                Console.WriteLine("Ложно");
        }
    }
}
```

**Пример:** при `да, да, нет` → «Истинно».

---

## №145. Тупоугольный треугольник

**Условие:** Даны три вещественных числа. Проверить, могут ли они являться длинами сторон тупоугольного треугольника.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            double a = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите B: ");
            double b = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите C: ");
            double c = Convert.ToDouble(Console.ReadLine());

            if (a + b > c && a + c > b && b + c > a)
                Console.WriteLine("Могут быть сторонами тупоугольного треугольника");
            else
                Console.WriteLine("Не могут");
        }
    }
}
```

**Пример:** при `3, 4, 6` → «Могут быть сторонами тупоугольного треугольника».

---

## №146. Остроугольный треугольник

**Условие:** Даны три вещественных числа. Проверить, могут ли они быть сторонами остроугольного треугольника.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите A: ");
            double a = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите B: ");
            double b = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите C: ");
            double c = Convert.ToDouble(Console.ReadLine());

            if (a + b > c && a + c > b && b + c > a)
                Console.WriteLine("Могут быть сторонами остроугольного треугольника");
            else
                Console.WriteLine("Не могут");
        }
    }
}
```

**Пример:** при `5, 5, 5` → «Могут быть сторонами остроугольного треугольника».

---

## №147. Тихий час

**Условие:** Ввести время (часы и минуты). Проверить, попадает ли указанное время в интервал тихого часа (с 13:00 до 15:00).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите часы: ");
            int h = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите минуты: ");
            int m = Convert.ToInt32(Console.ReadLine());

            if (h >= 13 && h < 15)
                Console.WriteLine("Тихий час");
            else
                Console.WriteLine("Не тихий час");
        }
    }
}
```

**Пример:** при `14` и `0` → «Тихий час».

---

## №148. Все цифры трёхзначного числа различны

**Условие:** Убедиться, что все цифры введённого трёхзначного числа различны между собой.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите трёхзначное число: ");
            int a = Convert.ToInt32(Console.ReadLine());

            int c1 = a / 100;
            int c2 = (a / 10) % 10;
            int c3 = a % 10;

            if (c1 != c2 && c1 != c3 && c2 != c3)
                Console.WriteLine("Все цифры различны");
            else
                Console.WriteLine("Есть одинаковые цифры");
        }
    }
}
```

**Пример:** при `123` → «Все цифры различны», при `121` → «Есть одинаковые цифры».

---

## №149. Две кнопки станка

**Условие:** Ввести логическое значение двух кнопок пульта. Станок включается только при одновременном нажатии кнопок (защита от случайного сигнала).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Кнопка 1 нажата? (да/нет): ");
            string o1 = Console.ReadLine();

            Console.Write("Кнопка 2 нажата? (да/нет): ");
            string o2 = Console.ReadLine();

            bool k1 = (o1 == "да");
            bool k2 = (o2 == "да");

            if (k1 && k2)
                Console.WriteLine("Станок включён");
            else
                Console.WriteLine("Станок выключен");
        }
    }
}
```

**Пример:** при `да, да` → «Станок включён».

---

## №150. Точка ниже прямой и выше параболы

**Условие:** Проверить, лежит ли точка (X, Y) ниже прямой Y = 2X + 1 и выше параболы Y = X².

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите X: ");
            double x = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите Y: ");
            double y = Convert.ToDouble(Console.ReadLine());

            if (y < 2 * x + 1 && y > x * x)
                Console.WriteLine("Условие выполнено");
            else
                Console.WriteLine("Условие не выполнено");
        }
    }
}
```

**Пример:** при `1` и `1.5` → «Условие выполнено».

## №151. День недели на русском языке

**Условие:** Ввести номер дня недели (1–7). Вывести его словесное название на русском языке.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите день (1-7): ");
            int d = Convert.ToInt32(Console.ReadLine());

            switch (d)
            {
                case 1: Console.WriteLine("Понедельник"); break;
                case 2: Console.WriteLine("Вторник"); break;
                case 3: Console.WriteLine("Среда"); break;
                case 4: Console.WriteLine("Четверг"); break;
                case 5: Console.WriteLine("Пятница"); break;
                case 6: Console.WriteLine("Суббота"); break;
                case 7: Console.WriteLine("Воскресенье"); break;
                default: Console.WriteLine("Неверный номер дня"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Понедельник», при `7` → «Воскресенье».

---

## №152. Будни или выходной

**Условие:** Ввести номер дня недели (1–7). Вывести, является ли день рабочим («Будни») или нерабочим («Выходной»).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите день (1-7): ");
            int d = Convert.ToInt32(Console.ReadLine());

            switch (d)
            {
                case 1:
                case 2:
                case 3:
                case 4:
                case 5:
                    Console.WriteLine("Будни");
                    break;
                case 6:
                case 7:
                    Console.WriteLine("Выходной");
                    break;
                default:
                    Console.WriteLine("Неверный номер дня");
                    break;
            }
        }
    }
}
```

**Пример:** при `3` → «Будни», при `6` → «Выходной».

---

## №153. Название месяца

**Условие:** Ввести номер месяца (1–12). Вывести название месяца.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите месяц (1-12): ");
            int m = Convert.ToInt32(Console.ReadLine());

            switch (m)
            {
                case 1: Console.WriteLine("Январь"); break;
                case 2: Console.WriteLine("Февраль"); break;
                case 3: Console.WriteLine("Март"); break;
                case 4: Console.WriteLine("Апрель"); break;
                case 5: Console.WriteLine("Май"); break;
                case 6: Console.WriteLine("Июнь"); break;
                case 7: Console.WriteLine("Июль"); break;
                case 8: Console.WriteLine("Август"); break;
                case 9: Console.WriteLine("Сентябрь"); break;
                case 10: Console.WriteLine("Октябрь"); break;
                case 11: Console.WriteLine("Ноябрь"); break;
                case 12: Console.WriteLine("Декабрь"); break;
                default: Console.WriteLine("Неверный номер месяца"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Январь», при `12` → «Декабрь».

---

## №154. Количество дней в месяце

**Условие:** Ввести номер месяца (1–12). Вывести количество дней в этом месяце (для невисокосного года).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите месяц (1-12): ");
            int m = Convert.ToInt32(Console.ReadLine());

            switch (m)
            {
                case 2:
                    Console.WriteLine("28 дней");
                    break;
                case 4:
                case 6:
                case 9:
                case 11:
                    Console.WriteLine("30 дней");
                    break;
                case 1:
                case 3:
                case 5:
                case 7:
                case 8:
                case 10:
                case 12:
                    Console.WriteLine("31 день");
                    break;
                default:
                    Console.WriteLine("Неверный номер месяца");
                    break;
            }
        }
    }
}
```

**Пример:** при `2` → «28 дней», при `5` → «31 день».

---

## №155. Пора года

**Условие:** Ввести номер месяца (1–12). Вывести название поры года («Зима», «Весна», «Лето», «Осень»).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите месяц (1-12): ");
            int m = Convert.ToInt32(Console.ReadLine());

            switch (m)
            {
                case 12:
                case 1:
                case 2:
                    Console.WriteLine("Зима");
                    break;
                case 3:
                case 4:
                case 5:
                    Console.WriteLine("Весна");
                    break;
                case 6:
                case 7:
                case 8:
                    Console.WriteLine("Лето");
                    break;
                case 9:
                case 10:
                case 11:
                    Console.WriteLine("Осень");
                    break;
                default:
                    Console.WriteLine("Неверный номер месяца");
                    break;
            }
        }
    }
}
```

**Пример:** при `1` → «Зима», при `7` → «Лето».

---

## №156. Оценка студента

**Условие:** Ввести оценку студента (1–5). Вывести текстовое описание: 1 — «Очень плохо», 2 — «Неудовлетворительно», 3 — «Удовлетворительно», 4 — «Хорошо», 5 — «Отлично».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите оценку (1-5): ");
            int o = Convert.ToInt32(Console.ReadLine());

            switch (o)
            {
                case 1: Console.WriteLine("Очень плохо"); break;
                case 2: Console.WriteLine("Неудовлетворительно"); break;
                case 3: Console.WriteLine("Удовлетворительно"); break;
                case 4: Console.WriteLine("Хорошо"); break;
                case 5: Console.WriteLine("Отлично"); break;
                default: Console.WriteLine("Неверная оценка"); break;
            }
        }
    }
}
```

**Пример:** при `5` → «Отлично», при `2` → «Неудовлетворительно».

---

## №157. Простой калькулятор

**Условие:** Реализовать простой калькулятор: ввести два вещественных числа и символ арифметической операции (+, -, *, /). Через switch выполнить вычисление. Предусмотреть защиту от деления на ноль.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите первое число: ");
            double a = Convert.ToDouble(Console.ReadLine());

            Console.Write("Введите операцию (+ - * /): ");
            string op = Console.ReadLine();

            Console.Write("Введите второе число: ");
            double b = Convert.ToDouble(Console.ReadLine());

            switch (op)
            {
                case "+":
                    Console.WriteLine("Результат: " + (a + b));
                    break;
                case "-":
                    Console.WriteLine("Результат: " + (a - b));
                    break;
                case "*":
                    Console.WriteLine("Результат: " + (a * b));
                    break;
                case "/":
                    if (b == 0)
                        Console.WriteLine("Деление на ноль!");
                    else
                        Console.WriteLine("Результат: " + (a / b));
                    break;
                default:
                    Console.WriteLine("Неверная операция");
                    break;
            }
        }
    }
}
```

**Пример:** при `10`, `+`, `5` → «Результат: 15».

---

## №158. Направление света

**Условие:** Ввести букву направления света (N, S, W, E). Вывести название направления («Север», «Юг», «Запад», «Восток»).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите букву (N, S, W, E): ");
            string n = Console.ReadLine();

            switch (n)
            {
                case "N": Console.WriteLine("Север"); break;
                case "S": Console.WriteLine("Юг"); break;
                case "W": Console.WriteLine("Запад"); break;
                case "E": Console.WriteLine("Восток"); break;
                default: Console.WriteLine("Неверное направление"); break;
            }
        }
    }
}
```

**Пример:** при `N` → «Север», при `E` → «Восток».

---

## №159. Площадь геометрической фигуры

**Условие:** Ввести номер геометрической фигуры (1 — круг, 2 — прямоугольник, 3 — треугольник). Запросить соответствующие параметры фигуры и вычислить её площадь.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите фигуру (1-круг, 2-прямоугольник, 3-треугольник): ");
            int f = Convert.ToInt32(Console.ReadLine());

            switch (f)
            {
                case 1:
                    Console.Write("Введите радиус: ");
                    double r = Convert.ToDouble(Console.ReadLine());
                    Console.WriteLine("Площадь круга: " + (3.14 * r * r));
                    break;
                case 2:
                    Console.Write("Введите сторону A: ");
                    double a = Convert.ToDouble(Console.ReadLine());
                    Console.Write("Введите сторону B: ");
                    double b = Convert.ToDouble(Console.ReadLine());
                    Console.WriteLine("Площадь прямоугольника: " + (a * b));
                    break;
                case 3:
                    Console.Write("Введите основание: ");
                    double osn = Convert.ToDouble(Console.ReadLine());
                    Console.Write("Введите высоту: ");
                    double h = Convert.ToDouble(Console.ReadLine());
                    Console.WriteLine("Площадь треугольника: " + (0.5 * osn * h));
                    break;
                default:
                    Console.WriteLine("Неверная фигура");
                    break;
            }
        }
    }
}
```

**Пример:** при `1` и радиусе `5` → «Площадь круга: 78.5».

---

## №160. Масть игровой карты

**Условие:** Ввести номер масти игровой карты (1 — пики, 2 — трефы, 3 — бубны, 4 — червы). Вывести название масти.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите масть (1-4): ");
            int m = Convert.ToInt32(Console.ReadLine());

            switch (m)
            {
                case 1: Console.WriteLine("Пики"); break;
                case 2: Console.WriteLine("Трефы"); break;
                case 3: Console.WriteLine("Бубны"); break;
                case 4: Console.WriteLine("Червы"); break;
                default: Console.WriteLine("Неверная масть"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Пики», при `4` → «Червы».

---

## №161. Название игральной карты

**Условие:** Ввести номер карты (от 6 до 14). Вывести название: 11 — Валет, 12 — Дама, 13 — Король, 14 — Туз, остальные — по номиналу.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите номер карты (6-14): ");
            int k = Convert.ToInt32(Console.ReadLine());

            switch (k)
            {
                case 11: Console.WriteLine("Валет"); break;
                case 12: Console.WriteLine("Дама"); break;
                case 13: Console.WriteLine("Король"); break;
                case 14: Console.WriteLine("Туз"); break;
                default: Console.WriteLine("Номинал: " + k); break;
            }
        }
    }
}
```

**Пример:** при `11` → «Валет», при `7` → «Номинал: 7».

---

## №162. Размер одежды

**Условие:** Ввести буквенное обозначение размера одежды (XS, S, M, L, XL, XXL). Вывести соответствующий российский размер (42, 44, 46, 48, 50, 52).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите размер (XS, S, M, L, XL, XXL): ");
            string r = Console.ReadLine();

            switch (r)
            {
                case "XS": Console.WriteLine("42"); break;
                case "S": Console.WriteLine("44"); break;
                case "M": Console.WriteLine("46"); break;
                case "L": Console.WriteLine("48"); break;
                case "XL": Console.WriteLine("50"); break;
                case "XXL": Console.WriteLine("52"); break;
                default: Console.WriteLine("Неверный размер"); break;
            }
        }
    }
}
```

**Пример:** при `M` → «46», при `XL` → «50».

---

## №163. Перевод длины в метры

**Условие:** Ввести номер единицы длины (1 — дециметр, 2 — километр, 3 — метр, 4 — миллиметр, 5 — сантиметр) и длину отрезка в этих единицах. Перевести и вывести величину в метрах.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите единицу (1-дм, 2-км, 3-м, 4-мм, 5-см): ");
            int e = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите значение: ");
            double z = Convert.ToDouble(Console.ReadLine());

            switch (e)
            {
                case 1: Console.WriteLine("В метрах: " + (z / 10)); break;
                case 2: Console.WriteLine("В метрах: " + (z * 1000)); break;
                case 3: Console.WriteLine("В метрах: " + z); break;
                case 4: Console.WriteLine("В метрах: " + (z / 1000)); break;
                case 5: Console.WriteLine("В метрах: " + (z / 100)); break;
                default: Console.WriteLine("Неверная единица"); break;
            }
        }
    }
}
```

**Пример:** при `2` и `1.5` → «В метрах: 1500».

---

## №164. Перевод массы в килограммы

**Условие:** Ввести номер единицы массы (1 — килограмм, 2 — миллиграмм, 3 — грамм, 4 — тонна, 5 — центнер) и массу. Вывести массу в килограммах.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите единицу (1-кг, 2-мг, 3-г, 4-т, 5-ц): ");
            int e = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите значение: ");
            double z = Convert.ToDouble(Console.ReadLine());

            switch (e)
            {
                case 1: Console.WriteLine("В кг: " + z); break;
                case 2: Console.WriteLine("В кг: " + (z / 1000000)); break;
                case 3: Console.WriteLine("В кг: " + (z / 1000)); break;
                case 4: Console.WriteLine("В кг: " + (z * 1000)); break;
                case 5: Console.WriteLine("В кг: " + (z * 100)); break;
                default: Console.WriteLine("Неверная единица"); break;
            }
        }
    }
}
```

**Пример:** при `4` и `2` → «В кг: 2000».

---

## №165. Расшифровка HTTP-кода

**Условие:** Ввести код ошибки HTTP (200, 301, 400, 403, 404, 500, 502). Вывести текстовую расшифровку.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите HTTP-код: ");
            int c = Convert.ToInt32(Console.ReadLine());

            switch (c)
            {
                case 200: Console.WriteLine("OK"); break;
                case 301: Console.WriteLine("Moved Permanently"); break;
                case 400: Console.WriteLine("Bad Request"); break;
                case 403: Console.WriteLine("Forbidden"); break;
                case 404: Console.WriteLine("Not Found"); break;
                case 500: Console.WriteLine("Internal Server Error"); break;
                case 502: Console.WriteLine("Bad Gateway"); break;
                default: Console.WriteLine("Неизвестный код"); break;
            }
        }
    }
}
```

**Пример:** при `404` → «Not Found».

---

## №166. Код валюты

**Условие:** Ввести код валюты (USD, EUR, CNY, RUB). Вывести полное наименование («Доллар США», «Евро», «Китайский юань», «Российский рубль»).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите код валюты (USD, EUR, CNY, RUB): ");
            string v = Console.ReadLine();

            switch (v)
            {
                case "USD": Console.WriteLine("Доллар США"); break;
                case "EUR": Console.WriteLine("Евро"); break;
                case "CNY": Console.WriteLine("Китайский юань"); break;
                case "RUB": Console.WriteLine("Российский рубль"); break;
                default: Console.WriteLine("Неизвестная валюта"); break;
            }
        }
    }
}
```

**Пример:** при `USD` → «Доллар США».

---

## №167. Управление движением персонажа (WASD)

**Условие:** Ввести символ клавиши управления движением персонажа (W, A, S, D в любом регистре). Вывести направление движения: вперёд, влево, назад, вправо.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите клавишу (W, A, S, D): ");
            string k = Console.ReadLine();

            switch (k)
            {
                case "W":
                case "w":
                    Console.WriteLine("Вперёд");
                    break;
                case "A":
                case "a":
                    Console.WriteLine("Влево");
                    break;
                case "S":
                case "s":
                    Console.WriteLine("Назад");
                    break;
                case "D":
                case "d":
                    Console.WriteLine("Вправо");
                    break;
                default:
                    Console.WriteLine("Неверная клавиша");
                    break;
            }
        }
    }
}
```

**Пример:** при `W` → «Вперёд», при `d` → «Вправо».

---

## №168. Цвет радуги

**Условие:** Ввести номер цвета радуги (1–7). Вывести название цвета.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите номер цвета (1-7): ");
            int c = Convert.ToInt32(Console.ReadLine());

            switch (c)
            {
                case 1: Console.WriteLine("Красный"); break;
                case 2: Console.WriteLine("Оранжевый"); break;
                case 3: Console.WriteLine("Жёлтый"); break;
                case 4: Console.WriteLine("Зелёный"); break;
                case 5: Console.WriteLine("Голубой"); break;
                case 6: Console.WriteLine("Синий"); break;
                case 7: Console.WriteLine("Фиолетовый"); break;
                default: Console.WriteLine("Неверный номер"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Красный», при `7` → «Фиолетовый».

---

## №169. Режим селектора АКПП

**Условие:** Ввести признак режима селектора АКПП (P, R, N, D, M). Вывести режим трансмиссии.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите режим (P, R, N, D, M): ");
            string r = Console.ReadLine();

            switch (r)
            {
                case "P": Console.WriteLine("Парковка"); break;
                case "R": Console.WriteLine("Задний ход"); break;
                case "N": Console.WriteLine("Нейтраль"); break;
                case "D": Console.WriteLine("Драйв"); break;
                case "M": Console.WriteLine("Ручной режим"); break;
                default: Console.WriteLine("Неверный режим"); break;
            }
        }
    }
}
```

**Пример:** при `P` → «Парковка», при `D` → «Драйв».

---

## №170. Название пальца руки

**Условие:** Ввести номер пальца руки (1 — большой, 2 — указательный, 3 — средний, 4 — безымянный, 5 — мизинец). Вывести название пальца.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите номер пальца (1-5): ");
            int p = Convert.ToInt32(Console.ReadLine());

            switch (p)
            {
                case 1: Console.WriteLine("Большой"); break;
                case 2: Console.WriteLine("Указательный"); break;
                case 3: Console.WriteLine("Средний"); break;
                case 4: Console.WriteLine("Безымянный"); break;
                case 5: Console.WriteLine("Мизинец"); break;
                default: Console.WriteLine("Неверный номер"); break;
            }
        }
    }
}
```

**Пример:** при `2` → «Указательный», при `5` → «Мизинец».

---

## №171. Планета Солнечной системы

**Условие:** Ввести номер планеты от Солнца (1–8). Вывести название планеты Солнечной системы.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите номер планеты (1-8): ");
            int p = Convert.ToInt32(Console.ReadLine());

            switch (p)
            {
                case 1: Console.WriteLine("Меркурий"); break;
                case 2: Console.WriteLine("Венера"); break;
                case 3: Console.WriteLine("Земля"); break;
                case 4: Console.WriteLine("Марс"); break;
                case 5: Console.WriteLine("Юпитер"); break;
                case 6: Console.WriteLine("Сатурн"); break;
                case 7: Console.WriteLine("Уран"); break;
                case 8: Console.WriteLine("Нептун"); break;
                default: Console.WriteLine("Неверный номер"); break;
            }
        }
    }
}
```

**Пример:** при `3` → «Земля», при `8` → «Нептун».

---

## №172. Тариф мобильной связи

**Условие:** Ввести код тарифа мобильной связи (1 — Базовый, 2 — Студенческий, 3 — Безлимит). Вывести абонентскую плату и включённые гигабайты.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите тариф (1-3): ");
            int t = Convert.ToInt32(Console.ReadLine());

            switch (t)
            {
                case 1: Console.WriteLine("Базовый: 300 руб, 5 ГБ"); break;
                case 2: Console.WriteLine("Студенческий: 200 руб, 10 ГБ"); break;
                case 3: Console.WriteLine("Безлимит: 500 руб, безлимит"); break;
                default: Console.WriteLine("Неверный тариф"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Базовый: 300 руб, 5 ГБ».

---

## №173. Квартал года

**Условие:** Ввести номер квартала года (1–4). Вывести список входящих в него месяцев.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите квартал (1-4): ");
            int k = Convert.ToInt32(Console.ReadLine());

            switch (k)
            {
                case 1: Console.WriteLine("Январь, Февраль, Март"); break;
                case 2: Console.WriteLine("Апрель, Май, Июнь"); break;
                case 3: Console.WriteLine("Июль, Август, Сентябрь"); break;
                case 4: Console.WriteLine("Октябрь, Ноябрь, Декабрь"); break;
                default: Console.WriteLine("Неверный квартал"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Январь, Февраль, Март».

---

## №174. Оценка по американской системе

**Условие:** Ввести букву оценки американской системы (A, B, C, D, F). Вывести эквивалент в пятибалльной системе РФ.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите букву (A, B, C, D, F): ");
            string o = Console.ReadLine();

            switch (o)
            {
                case "A": Console.WriteLine("5"); break;
                case "B": Console.WriteLine("4"); break;
                case "C": Console.WriteLine("3"); break;
                case "D": Console.WriteLine("2"); break;
                case "F": Console.WriteLine("2"); break;
                default: Console.WriteLine("Неверная буква"); break;
            }
        }
    }
}
```

**Пример:** при `A` → «5», при `C` → «3».

---

## №175. Операции над множествами

**Условие:** Ввести символ операции над множествами (U — объединение, I — пересечение, D — разность). Вывести расшифровку операции.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите операцию (U, I, D): ");
            string op = Console.ReadLine();

            switch (op)
            {
                case "U": Console.WriteLine("Объединение"); break;
                case "I": Console.WriteLine("Пересечение"); break;
                case "D": Console.WriteLine("Разность"); break;
                default: Console.WriteLine("Неверная операция"); break;
            }
        }
    }
}
```

**Пример:** при `U` → «Объединение».

---

## №176. Режим работы светофора

**Условие:** Ввести номер режима светофора (1 — Красный, 2 — Жёлтый, 3 — Зелёный, 4 — Мигающий жёлтый). Вывести предписание для водителя.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите сигнал (1-4): ");
            int s = Convert.ToInt32(Console.ReadLine());

            switch (s)
            {
                case 1: Console.WriteLine("Стоп"); break;
                case 2: Console.WriteLine("Приготовиться"); break;
                case 3: Console.WriteLine("Ехать"); break;
                case 4: Console.WriteLine("Ехать с осторожностью"); break;
                default: Console.WriteLine("Неверный сигнал"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Стоп», при `3` → «Ехать».

---

## №177. Словесное описание цифры

**Условие:** Ввести цифру (0–9). Вывести её словесное описание на русском языке.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите цифру (0-9): ");
            int c = Convert.ToInt32(Console.ReadLine());

            switch (c)
            {
                case 0: Console.WriteLine("Ноль"); break;
                case 1: Console.WriteLine("Один"); break;
                case 2: Console.WriteLine("Два"); break;
                case 3: Console.WriteLine("Три"); break;
                case 4: Console.WriteLine("Четыре"); break;
                case 5: Console.WriteLine("Пять"); break;
                case 6: Console.WriteLine("Шесть"); break;
                case 7: Console.WriteLine("Семь"); break;
                case 8: Console.WriteLine("Восемь"); break;
                case 9: Console.WriteLine("Девять"); break;
                default: Console.WriteLine("Не цифра"); break;
            }
        }
    }
}
```

**Пример:** при `5` → «Пять», при `0` → «Ноль».

---

## №178. Римские цифры

**Условие:** Ввести римскую цифру (I, V, X, L, C, D, M). Вывести её арабское значение.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите римскую цифру (I, V, X, L, C, D, M): ");
            string r = Console.ReadLine();

            switch (r)
            {
                case "I": Console.WriteLine("1"); break;
                case "V": Console.WriteLine("5"); break;
                case "X": Console.WriteLine("10"); break;
                case "L": Console.WriteLine("50"); break;
                case "C": Console.WriteLine("100"); break;
                case "D": Console.WriteLine("500"); break;
                case "M": Console.WriteLine("1000"); break;
                default: Console.WriteLine("Неверная цифра"); break;
            }
        }
    }
}
```

**Пример:** при `X` → «10», при `M` → «1000».

---

## №179. Категория водительского удостоверения

**Условие:** Ввести номер типа транспортного средства (1 — Мотоцикл, 2 — Легковой авто, 3 — Грузовой авто, 4 — Автобус). Вывести категорию водительского удостоверения (A, B, C, D).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите тип (1-4): ");
            int t = Convert.ToInt32(Console.ReadLine());

            switch (t)
            {
                case 1: Console.WriteLine("Категория A (мотоцикл)"); break;
                case 2: Console.WriteLine("Категория B (легковой)"); break;
                case 3: Console.WriteLine("Категория C (грузовой)"); break;
                case 4: Console.WriteLine("Категория D (автобус)"); break;
                default: Console.WriteLine("Неверный тип"); break;
            }
        }
    }
}
```

**Пример:** при `2` → «Категория B (легковой)».

---

## №180. Тип двигателя

**Условие:** Ввести тип двигателя (1 — Бензиновый, 2 — Дизельный, 3 — Гибридный, 4 — Электрический). Вывести вид используемого источника энергии.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите тип (1-4): ");
            int t = Convert.ToInt32(Console.ReadLine());

            switch (t)
            {
                case 1: Console.WriteLine("Бензин"); break;
                case 2: Console.WriteLine("Дизельное топливо"); break;
                case 3: Console.WriteLine("Бензин + электричество"); break;
                case 4: Console.WriteLine("Электричество"); break;
                default: Console.WriteLine("Неверный тип"); break;
            }
        }
    }
}
```

**Пример:** при `4` → «Электричество».

---

## №181. Операция в банкомате

**Условие:** Ввести номер операции в банкомате: 1 — Баланс, 2 — Снятие наличных, 3 — Пополнение, 4 — Перевод. Вывести сообщение о выбранной операции.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите операцию (1-4): ");
            int o = Convert.ToInt32(Console.ReadLine());

            switch (o)
            {
                case 1: Console.WriteLine("Проверка баланса"); break;
                case 2: Console.WriteLine("Снятие наличных"); break;
                case 3: Console.WriteLine("Пополнение счёта"); break;
                case 4: Console.WriteLine("Перевод средств"); break;
                default: Console.WriteLine("Неверная операция"); break;
            }
        }
    }
}
```

**Пример:** при `2` → «Снятие наличных».

---

## №182. Тип файла по расширению

**Условие:** Ввести расширение файла (txt, cs, html, png, mp3). Вывести тип: текстовый документ, исходный код C#, веб-страница, изображение, аудиофайл.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите расширение (txt, cs, html, png, mp3): ");
            string r = Console.ReadLine();

            switch (r)
            {
                case "txt": Console.WriteLine("Текстовый документ"); break;
                case "cs": Console.WriteLine("Исходный код C#"); break;
                case "html": Console.WriteLine("Веб-страница"); break;
                case "png": Console.WriteLine("Изображение"); break;
                case "mp3": Console.WriteLine("Аудиофайл"); break;
                default: Console.WriteLine("Неизвестное расширение"); break;
            }
        }
    }
}
```

**Пример:** при `png` → «Изображение».

---

## №183. Химический элемент

**Условие:** Ввести номер химического элемента из первых пяти таблицы Менделеева (1–5). Вывести название элемента и его символ.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите номер (1-5): ");
            int n = Convert.ToInt32(Console.ReadLine());

            switch (n)
            {
                case 1: Console.WriteLine("H — Водород"); break;
                case 2: Console.WriteLine("He — Гелий"); break;
                case 3: Console.WriteLine("Li — Литий"); break;
                case 4: Console.WriteLine("Be — Бериллий"); break;
                case 5: Console.WriteLine("B — Бор"); break;
                default: Console.WriteLine("Неверный номер"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «H — Водород».

---

## №184. Статус заказа в интернет-магазине

**Условие:** Ввести код заказа в интернет-магазине (NEW, PAID, SHIPPED, DELIVERED, CANCELLED). Вывести подсказку для клиента.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите статус (NEW, PAID, SHIPPED, DELIVERED, CANCELLED): ");
            string s = Console.ReadLine();

            switch (s)
            {
                case "NEW": Console.WriteLine("Заказ принят, ожидает оплаты"); break;
                case "PAID": Console.WriteLine("Оплачен, ожидает отправки"); break;
                case "SHIPPED": Console.WriteLine("Отправлен, в пути"); break;
                case "DELIVERED": Console.WriteLine("Доставлен"); break;
                case "CANCELLED": Console.WriteLine("Отменён"); break;
                default: Console.WriteLine("Неизвестный статус"); break;
            }
        }
    }
}
```

**Пример:** при `PAID` → «Оплачен, ожидает отправки».

---

## №185. Система счисления

**Условие:** Ввести код системы счисления (2, 8, 10, 16) и перевести введённое десятичное число в выбранную систему (через методы класса Convert).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите систему (2, 8, 10, 16): ");
            int sys = Convert.ToInt32(Console.ReadLine());

            Console.Write("Введите десятичное число: ");
            int dec = Convert.ToInt32(Console.ReadLine());

            switch (sys)
            {
                case 2: Console.WriteLine(Convert.ToString(dec, 2)); break;
                case 8: Console.WriteLine(Convert.ToString(dec, 8)); break;
                case 10: Console.WriteLine(dec); break;
                case 16: Console.WriteLine(Convert.ToString(dec, 16)); break;
                default: Console.WriteLine("Неверная система"); break;
            }
        }
    }
}
```

**Пример:** при `2` и `5` → «101».

---

## №186. Курс колледжа

**Условие:** Ввести номер курса колледжа (1–4). Вывести: «Первокурсник», «Второй курс», «Предвыпускной курс», «Выпускник».

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите курс (1-4): ");
            int k = Convert.ToInt32(Console.ReadLine());

            switch (k)
            {
                case 1: Console.WriteLine("Первокурсник"); break;
                case 2: Console.WriteLine("Второй курс"); break;
                case 3: Console.WriteLine("Предвыпускной курс"); break;
                case 4: Console.WriteLine("Выпускник"); break;
                default: Console.WriteLine("Неверный курс"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Первокурсник», при `4` → «Выпускник».

---

## №187. Климатическая зона

**Условие:** Ввести код климатической зоны (1 — Арктическая, 2 — Субарктическая, 3 — Умеренная, 4 — Субтропическая, 5 — Тропическая). Вывести краткую характеристику.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите зону (1-5): ");
            int z = Convert.ToInt32(Console.ReadLine());

            switch (z)
            {
                case 1: Console.WriteLine("Арктическая — очень холодно"); break;
                case 2: Console.WriteLine("Субарктическая — холодно"); break;
                case 3: Console.WriteLine("Умеренная — умеренно"); break;
                case 4: Console.WriteLine("Субтропическая — тепло"); break;
                case 5: Console.WriteLine("Тропическая — жарко"); break;
                default: Console.WriteLine("Неверная зона"); break;
            }
        }
    }
}
```

**Пример:** при `3` → «Умеренная — умеренно».

---

## №188. Класс пожарной опасности

**Условие:** Ввести класс пожарной опасности (1–5). Вывести уровень угрозы и ограничения на посещение лесов.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите класс (1-5): ");
            int k = Convert.ToInt32(Console.ReadLine());

            switch (k)
            {
                case 1: Console.WriteLine("Низкая — посещение разрешено"); break;
                case 2: Console.WriteLine("Умеренная — быть осторожным"); break;
                case 3: Console.WriteLine("Средняя — ограничить посещение"); break;
                case 4: Console.WriteLine("Высокая — запрет на посещение"); break;
                case 5: Console.WriteLine("Чрезвычайная — полный запрет"); break;
                default: Console.WriteLine("Неверный класс"); break;
            }
        }
    }
}
```

**Пример:** при `4` → «Высокая — запрет на посещение».

---

## №189. Спортивный разряд

**Условие:** Ввести номер спортивного разряда (1 — Юношеский, 2 — Взрослый, 3 — КМС, 4 — МС, 5 — МСМК). Вывести расшифровку.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите разряд (1-5): ");
            int r = Convert.ToInt32(Console.ReadLine());

            switch (r)
            {
                case 1: Console.WriteLine("Юношеский разряд"); break;
                case 2: Console.WriteLine("Взрослый разряд"); break;
                case 3: Console.WriteLine("КМС — кандидат в мастера спорта"); break;
                case 4: Console.WriteLine("МС — мастер спорта"); break;
                case 5: Console.WriteLine("МСМК — мастер спорта международного класса"); break;
                default: Console.WriteLine("Неверный разряд"); break;
            }
        }
    }
}
```

**Пример:** при `3` → «КМС — кандидат в мастера спорта».

---

## №190. Уровень доступа пользователя

**Условие:** Ввести код уровня доступа пользователя (G — Гость, U — Пользователь, M — Модератор, A — Администратор). Вывести перечень разрешённых действий.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите код (G, U, M, A): ");
            string d = Console.ReadLine();

            switch (d)
            {
                case "G": Console.WriteLine("Просмотр содержимого"); break;
                case "U": Console.WriteLine("Просмотр и комментарии"); break;
                case "M": Console.WriteLine("Модерация контента"); break;
                case "A": Console.WriteLine("Полный доступ"); break;
                default: Console.WriteLine("Неверный код"); break;
            }
        }
    }
}
```

**Пример:** при `M` → «Модерация контента».

---

## №191. Музыкальные ноты

**Условие:** Ввести букву ноты (C, D, E, F, G, A, B). Вывести русское словесное обозначение (До, Ре, Ми, Фа, Соль, Ля, Си).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите ноту (C, D, E, F, G, A, B): ");
            string n = Console.ReadLine();

            switch (n)
            {
                case "C": Console.WriteLine("До"); break;
                case "D": Console.WriteLine("Ре"); break;
                case "E": Console.WriteLine("Ми"); break;
                case "F": Console.WriteLine("Фа"); break;
                case "G": Console.WriteLine("Соль"); break;
                case "A": Console.WriteLine("Ля"); break;
                case "B": Console.WriteLine("Си"); break;
                default: Console.WriteLine("Неверная нота"); break;
            }
        }
    }
}
```

**Пример:** при `C` → «До», при `G` → «Соль».

---

## №192. Тип кузова автомобиля

**Условие:** Ввести номер типа кузова автомобиля (1 — Седан, 2 — Хэтчбек, 3 — Универсал, 4 — Купе, 5 — Внедорожник). Вывести описание вместимости и компоновки.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите тип (1-5): ");
            int t = Convert.ToInt32(Console.ReadLine());

            switch (t)
            {
                case 1: Console.WriteLine("Седан — 4-5 мест, отдельный багажник"); break;
                case 2: Console.WriteLine("Хэтчбек — 4-5 мест, компактный"); break;
                case 3: Console.WriteLine("Универсал — большой багажник"); break;
                case 4: Console.WriteLine("Купе — 2 двери, спортивный"); break;
                case 5: Console.WriteLine("Внедорожник — повышенная проходимость"); break;
                default: Console.WriteLine("Неверный тип"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Седан — 4-5 мест, отдельный багажник».

---

## №193. Датчик охранной сигнализации

**Условие:** Ввести код типа датчика охранной сигнализации: M (движение), D (открытие двери), S (дым), W (протечка воды). Вывести сообщение о типе угрозы.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите код (M, D, S, W): ");
            string d = Console.ReadLine();

            switch (d)
            {
                case "M": Console.WriteLine("Обнаружено движение"); break;
                case "D": Console.WriteLine("Открытие двери"); break;
                case "S": Console.WriteLine("Обнаружен дым"); break;
                case "W": Console.WriteLine("Протечка воды"); break;
                default: Console.WriteLine("Неверный код"); break;
            }
        }
    }
}
```

**Пример:** при `M` → «Обнаружено движение».

---

## №194. Фаза Луны

**Условие:** Ввести номер фазы Луны (1 — Новолуние, 2 — Первая четверть, 3 — Полнолуние, 4 — Последняя четверть). Вывести характеристику фазы.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите фазу (1-4): ");
            int f = Convert.ToInt32(Console.ReadLine());

            switch (f)
            {
                case 1: Console.WriteLine("Новолуние — Луна не видна"); break;
                case 2: Console.WriteLine("Первая четверть — растущая Луна"); break;
                case 3: Console.WriteLine("Полнолуние — Луна видна полностью"); break;
                case 4: Console.WriteLine("Последняя четверть — убывающая Луна"); break;
                default: Console.WriteLine("Неверная фаза"); break;
            }
        }
    }
}
```

**Пример:** при `3` → «Полнолуние — Луна видна полностью».

---

## №195. Разделитель пути

**Условие:** Ввести символ разделителя пути (/ или \). Вывести, к какому семейству ОС относится разделитель (Unix/Linux или Windows).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите символ (/ или \\): ");
            string r = Console.ReadLine();

            switch (r)
            {
                case "/": Console.WriteLine("Unix/Linux"); break;
                case "\\": Console.WriteLine("Windows"); break;
                default: Console.WriteLine("Неверный символ"); break;
            }
        }
    }
}
```

**Пример:** при `/` → «Unix/Linux», при `\` → «Windows».

---

## №196. Поколение мобильной связи

**Условие:** Ввести номер поколения мобильной связи (2, 3, 4, 5). Вывести название стандарта (GPRS/EDGE, UMTS/HSPA, LTE, NR) и типичную скорость.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите поколение (2, 3, 4, 5): ");
            int p = Convert.ToInt32(Console.ReadLine());

            switch (p)
            {
                case 2: Console.WriteLine("GPRS/EDGE, ~0.2 Мбит/с"); break;
                case 3: Console.WriteLine("UMTS/HSPA, ~2 Мбит/с"); break;
                case 4: Console.WriteLine("LTE, ~100 Мбит/с"); break;
                case 5: Console.WriteLine("NR, ~1 Гбит/с"); break;
                default: Console.WriteLine("Неверное поколение"); break;
            }
        }
    }
}
```

**Пример:** при `4` → «LTE, ~100 Мбит/с».

---

## №197. Сетевой протокол по порту

**Условие:** Ввести номер порта протокола (21, 22, 25, 80, 443). Вывести название сетевого протокола (FTP, SSH, SMTP, HTTP, HTTPS).

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите порт: ");
            int p = Convert.ToInt32(Console.ReadLine());

            switch (p)
            {
                case 21: Console.WriteLine("FTP"); break;
                case 22: Console.WriteLine("SSH"); break;
                case 25: Console.WriteLine("SMTP"); break;
                case 80: Console.WriteLine("HTTP"); break;
                case 443: Console.WriteLine("HTTPS"); break;
                default: Console.WriteLine("Неизвестный порт"); break;
            }
        }
    }
}
```

**Пример:** при `80` → «HTTP», при `443` → «HTTPS».

---

## №198. Режим стиральной машины

**Условие:** Ввести код режима стиральной машины (1 — Хлопок, 2 — Синтетика, 3 — Шерсть, 4 — Быстрая 15 мин, 5 — Отжим). Вывести температуру стирки и скорость отжима.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите режим (1-5): ");
            int r = Convert.ToInt32(Console.ReadLine());

            switch (r)
            {
                case 1: Console.WriteLine("Хлопок: 60°C, 1000 об/мин"); break;
                case 2: Console.WriteLine("Синтетика: 40°C, 800 об/мин"); break;
                case 3: Console.WriteLine("Шерсть: 30°C, 600 об/мин"); break;
                case 4: Console.WriteLine("Быстрая 15 мин: 30°C, 800 об/мин"); break;
                case 5: Console.WriteLine("Отжим: 1200 об/мин"); break;
                default: Console.WriteLine("Неверный режим"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Хлопок: 60°C, 1000 об/мин».

---

## №199. Тарифная зона электроэнергии

**Условие:** Ввести код тарифной зоны электроэнергии (1 — Пик, 2 — Полупик, 3 — Ночь). Вывести стоимость киловатт-часа.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите зону (1-3): ");
            int z = Convert.ToInt32(Console.ReadLine());

            switch (z)
            {
                case 1: Console.WriteLine("Пик: 7 руб/кВт·ч"); break;
                case 2: Console.WriteLine("Полупик: 5 руб/кВт·ч"); break;
                case 3: Console.WriteLine("Ночь: 3 руб/кВт·ч"); break;
                default: Console.WriteLine("Неверная зона"); break;
            }
        }
    }
}
```

**Пример:** при `1` → «Пик: 7 руб/кВт·ч».

---

## №200. Состояние потока на C#

**Условие:** Ввести код состояния выполнения потока на C# (выполняется, приостановлено, остановлено, прервано). Вывести пояснение жизненного цикла потока.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Введите состояние: ");
            string s = Console.ReadLine();

            switch (s)
            {
                case "выполняется": Console.WriteLine("Поток работает"); break;
                case "приостановлено": Console.WriteLine("Поток на паузе"); break;
                case "остановлено": Console.WriteLine("Поток завершён"); break;
                case "прервано": Console.WriteLine("Поток прерван ошибкой"); break;
                default: Console.WriteLine("Неизвестное состояние"); break;
            }
        }
    }
}
```

**Пример:** при `выполняется` → «Поток работает».

