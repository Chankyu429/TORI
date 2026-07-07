# C# 배운 코드 정리

```csharp
namespace C22_Reference
{
    class Program
    {
        private static void Mutiply(int[] values)
        {
            for(int i = values.Length - 1; i >= 0; i--)
            {
                values[i] = values[i] * 10;
            }
        }

        private static void Test(ref int a)
        {
            a *= 10;
        }

        private static void Main(string[] args)
        {
            //값 형식 : 정적 할당
            //참조 형식 : 동정 할당 (new)

            //int[] arr = new int[] { 1, 2, 3, 4, 5 };
            int[] arr = { 1, 2, 3, 4, 5 };
            Mutiply(arr);

            for(int i = 0; i < arr.Length; i++)
            {
                Console.WriteLine($"arr[{i}] = {arr[i]}");
            }


            int r = new int(); //참조 형식 X
            r = 1;
            Test(ref r);
            Console.WriteLine($"r = {r}");
        }//Main
    }
}
```
