# loops
задачи_сорсове за цикли(преговор)💯



//11
//Задача: елемент, равен на сумата на останалите
//Да се напише програма, която въвежда n цели числа и проверява дали сред тях съществува число, което е равно на сумата на всички останали. Ако има такъв //елемент, се отпечатва "Yes" + неговата стойност, в противен случай - "No" + разликата между най-големия елемент и сумата на останалите (по абсолютна стойност).



 int n = int.Parse(Console.ReadLine());
            int sum = 0;
            int max = 0;
            for (int i = 0; i < n; i++)
            {
                int k = int.Parse(Console.ReadLine());
                sum = sum + k;
                if (k > max)
                    max = k;
            }
            if (max == sum - max)
            {
                Console.WriteLine("YEZ  " + max);
            }
            else
            {
                //l = sum - max;
                Console.WriteLine(Math.Abs(max - (sum - max)) + " no"); 
            }
            
//#10
//сумиране на гласните букви 
            // a =1 , e=2, i=3, o=4, u=5

            string s = Console.ReadLine();
            int sum = 0;

            for (int i = 0; i <= s.Length - 1; i++)
            {
                if (s[i] == 'a') sum = sum + 1;
                else if (s[i] == 'e') sum = sum + 2;
                else if (s[i] == 'i') sum = sum + 3;
                else if (s[i] == 'o') sum = sum + 4;
                else if (s[i] == 'u') sum = sum + 5;

            }
            Console.WriteLine("sum= " + sum); 



//#9
//Въвеждаме числата едно по едно и изчисляваме двете суми (на числата на четни позиции и на числата на нечетни позиции). Както в предходната задача, изчисляваме //абсолютната стойност на разликата и отпечатваме резултата ("Yes" + сумата при разлика 0 или "No" + разликата в противен случай).
            int n = int.Parse(Console.ReadLine());
            int i, k;
                int sumn = 0;
                int sumc = 0;

            for ( i = 0; i < n; i++)
            {
                 k = int.Parse(Console.ReadLine());
                 if(i%2==0)
                {
                    sumc = sumc + k;
                }
                 else
                {
                    sumn = sumn + k;
                }
               
            }
            int deff = Math.Abs(sumc - sumn);

            if (deff != 0)
            {
                Console.WriteLine("No " + deff);
            }
            else
            {
                Console.WriteLine("Yes " + sumc);
            }
            
            Console.WriteLine("четна сума " + sumc + " нeчетна сум " + sumn);


//#8
//Пример: лява и дясна сума
Да се напише програма, която въвежда 2 * n цели числа и проверява дали сумата на първите n числа (лява сума) е равна на сумата на вторите n числа (дясна сума). При равенство се печата "Yes" + сумата, иначе се печата "No" + разликата. Разликата се изчислява като положително число (по абсолютна стойност).
int n = int.Parse(Console.ReadLine());
            int sumd = 0, suml = 0;

            for (int i = 0; i < n; i++)
            {
                int k = int.Parse(Console.ReadLine());
                suml = suml + k;
            }

            for (int i = 0; i < n; i++)
            {
                int p = int.Parse(Console.ReadLine());
                sumd = sumd + p;
            }

            int deff = Math.Abs(suml - sumd);

            if (deff != 0)
            {
                Console.WriteLine("No " + deff);
            }
            else
            {
                Console.WriteLine("Yes " + suml);
            }

// #7
// намира сумата на ел и мин ел
            int n = int.Parse(Console.ReadLine());
            int sum = 0;
            int min = 1000000; // за разлика от макс където може да му дадем първоначално стойност=0, при мин не можем,
                         // защото 0 може да се окаже най-малката стойност дори и сред въведените от числа 


                         
            for (int i = 0; i < n; i++)
            {
                int k = int.Parse(Console.ReadLine());
                sum = sum + k;
                if (k < min) min = k;
            }
            Console.WriteLine("sum= " + sum + ", min= " + min);
//#6
            // намира сумата на ел и макс ел
            int n = int.Parse(Console.ReadLine());
            int sum = 0;
            int max = 0; 
            for ( int i=0; i<n; i++)
            {
                 int k = int.Parse(Console.ReadLine());
                sum = sum + k ;
                if (k > max) max = k;
            }
            Console.WriteLine("sum= "+ sum+ ", max= " + max);
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
