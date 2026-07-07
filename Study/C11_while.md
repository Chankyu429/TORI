# C# 배운 코드 정리

```csharp
namespace C11_While
{
    class Program
    {
        private static void Main(string[] args)
        {
            int a = 1;
            

            int b = ++a;
            Console.WriteLine($"a = {a},b = {b}");

            int c = a++;
            Console.WriteLine($"a = {a}, c = {c}");

            int d = --a;
            Console.WriteLine($"a = {a}, d = {d}");

            int e = a--;
            Console.WriteLine($"a = {a}, e = {e}");


            int i = 0;
            while(i < 5)
            {
                Console.WriteLine($"i = {i}");

                i++;
            }

            i = 5;
            while (i < 5)
            {
                i++;
                Console.WriteLine($"while = {i}");
            }
            while (i < 5);
        }//Main
    }
}
```
