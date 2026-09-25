# PR_2
//***********************************************************                                                     
//* Практическая работа №2                                  *                                              
//* Выполнила: Старкова Е.И.                                *                                                 
//* Задание: составить программу работы алгоритма ветвления *                                               
//***********************************************************




using System;

namespace PR_2
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.BackgroundColor = ConsoleColor.DarkCyan;                  // изменение фона консоли
            Console.Clear();                                                  // чистка консоли

            double x, y, z, R;                                                // объявление переменных, z - дистанция в круге

            Console.BackgroundColor = ConsoleColor.DarkMagenta;
            Console.WriteLine("Практическая работа №5");
            Console.Write("Введите координаты. \n");
            Console.Write("Введите координату х: ");
            x = Convert.ToDouble(Console.ReadLine());
            Console.Write("Введите координату y: ");
            y = Convert.ToDouble(Console.ReadLine());
            Console.Write("Введите координату R: ");
            R = Convert.ToDouble(Console.ReadLine());

            if (R < 0)                                                       // проверка радиуса круга
            {
                Console.WriteLine("Радиус не может быть ОТРИЦАТЕЛЬНЫМ.");
            }
            else
            {
                z = Math.Sqrt(x * x + y * y);                                // расстояние от точки до центра
                if (z < R)
                {
                    Console.WriteLine("Точка находится ВНУТРИ круга");
                }
                else if (z > R)
                {
                    Console.WriteLine("Точка находится ЗА ПРЕДЕЛАМИ круга");
                }
                else
                {
                    Console.WriteLine("Точка находится НА ГРАНИЦЕ круга");
                }

                Console.ReadKey();                                            // задержка консоли
            }
        }
    }
}

[Практическая работа №5(блок схема).drawio.pdf](https://github.com/user-attachments/files/32501111/5.drawio.pdf)
