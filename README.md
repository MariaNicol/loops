# loops
задачи_сорсове за цикли(преговор)💯

// #5 
// Да се напише програма, която въвежда n цели числа и ги сумира.
// Вход: 2  -> Изход: 14
// 4
//10 
int n = int.Parse(Console.ReadLine());


            int sum = 0;
            for ( int i=0; i<n; i++)
            {
                int k = int.Parse(Console.ReadLine());
                sum = sum + k;
            }
            Console.WriteLine(sum);
            // #4
            // Предоставената програма пресмята сумата на числата от 0 до въведено число (n) и я извежда на конзолата.
            // Вход:3 Изход:6 
            int n = int.Parse(Console.ReadLine());
            int sum = 0;
            for ( int i=0; i<=n; i++)
            {
                sum = sum + i;
            }
            Console.WriteLine(sum);
            // #3
            // Да се напише програма, която отпечатва буквите от латинската азбука: a, b, c, …, z.
            for (int i = 'A'; i <= 'Z'; i++)
            {
                char letter = (char)i; 
                Console.WriteLine(letter);
            }
             // #2    
             //Да се напише програма, която намира всички числа в интервала [1 … 1000], които завършват на 7.           
            /*
                int i;
                for( i = 1; i<=100; i++)
                { if (i % 10 == 7)        
                        Console.WriteLine(i);               
                }
              */
            // #1
            // Да се напише програма, която печата числата от 1 до 100.
            // Програмата не приема вход и отпечатва числата от 1 до 100 едно след друго, по едно на ред.

            /*
            for (int i=1; i <= 100; i++)
            {
                Console.WriteLine(i);
            }
            */
