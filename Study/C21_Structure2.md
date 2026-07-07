```csharp
using static System.Runtime.InteropServices.JavaScript.JSType;

namespace C21_Structure2
{
    class Program
    {
        private struct Character
        {
            public string Name;
            public float Hp;
            public float Attack;

            public string GetData()
            {
                string temp = $"Name : {Name}, Hp : {Hp}";

                return temp;
            }

            public void Damage(float InAmount)
            {
                Hp -= InAmount;
                Hp = Math.Clamp(Hp, 0, 100);
            }
        }

        private static void Main(string[] args)
        {
            Character player;
            player.Name = "Player";
            player.Hp = 100;
            player.Attack = 10;
            Console.WriteLine(player.GetData());

            Character monster;
            monster.Name = "Oak";
            monster.Hp = 30;
            monster.Attack = 5;
            Console.WriteLine(monster.GetData());

            Console.WriteLine();


            string[] names = new string[]
            { 
                "Goblin", "Dwarf", "Poring",
            };

            Character[] monsters = new Character[3];
            for (int i = 0; i < monsters.Length; i++)
            {
                monsters[i].Name = names[i];
                monsters[i].Hp = (i + 1) * 10;
                monsters[i].Attack = 3;
            }

            foreach(string name in names)
                Console.WriteLine(name);
            
            Console.WriteLine();

            foreach (Character m in monsters)
                Console.WriteLine(m.GetData());


            while(true)
            {
                Console.Write("공격할 몬스터 : ");
                int number = int.Parse(Console.ReadLine()!);

                if (number < monsters.Length) //0, 1, 2
                    monsters[number].Damage(player.Attack);
                else if (number == monsters.Length) //3
                    monster.Damage(player.Attack);
                else
                    break;


                foreach (Character m in monsters)
                    Console.WriteLine(m.GetData());
                
                Console.WriteLine(monster.GetData());
            }
            
        }//Main
    }
}
```
