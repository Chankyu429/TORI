# C# 배운 코드 정리

```csharp
namespace C14_For2
{
    class Program
    {
        private static void Main(string[] args)
        {
            for(int i = 0; i < 20; i++)
            {
                for(int j = 0; j < 5; j++)
                {
                    Console.Write($"i = {i:000}, j = {j}\t");
                }

                Console.WriteLine("");
            }
        }//Main
    }
}
```
