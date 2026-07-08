# C# 배운 코드 정리

```csharp
using System.Runtime.InteropServices;

namespace C23_Factorial
{
    class Program
    {
        private static int Factorial(int x)
        {
            int result = 0;

            Console.WriteLine($"시작 : x = {x}");

            if (x == 1)
                result = 1;
            else
                result = x * Factorial(x - 1);

            Console.WriteLine($"완료 : x = {x}, result = {result}");

            return result;
        }

        private static void Main(string[] args)
        {
            Console.WriteLine($"최종 값 : {Factorial(4)}");
        }//Main
    }
}
```