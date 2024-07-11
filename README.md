# Praktika
Практика 1 
using System;

class Cube
{
    private double sideLength;

    // Конструктор класу Cube
    public Cube(double side)
    {
        sideLength = side;
    }

    // Метод для обчислення об'єму куба
    public double Volume()
    {
        return Math.Pow(sideLength, 3);
    }

    // Метод для обчислення площі бічної поверхні куба
    public double LateralSurfaceArea()
    {
        return 4 * Math.Pow(sideLength, 2);
    }
}

class Program
{
    static void Main(string[] args)
    {
        double sideLength;

        // Просимо користувача ввести довжину ребра
        Console.WriteLine("Введіть довжину ребра куба:");
        while (!double.TryParse(Console.ReadLine(), out sideLength) || sideLength <= 0)
        {
            Console.WriteLine("Неправильне значення. Введіть додатнє число:");
        }

        // Створення об'єкту куба з введеною довжиною ребра
        Cube cube = new Cube(sideLength);

        // Обчислення об'єму куба
        double volume = cube.Volume();
        Console.WriteLine("Об'єм куба: " + volume);

        // Обчислення площі бічної поверхні куба
        double lateralSurfaceArea = cube.LateralSurfaceArea();
        Console.WriteLine("Площа бічної поверхні куба: " + lateralSurfaceArea);
    }
}
