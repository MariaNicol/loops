













----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------









# Object-oriented programming (OOP) 💯 
#ООП - обектно ориентирано програмиране  

#2 


грешна -
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace zavrushtaneVminaloto
{
    class Program
    {

        public class Student
        {
            public string Name { get; set; }
            public int Age { get; set; }
            public string FacultyNumber { get; set; }

            // Конструктор
            public Student(string studentName, int studentAge, string studentFacultyNumber)
            {
                Name = studentName;
                Age = studentAge;
                FacultyNumber = studentFacultyNumber;
            }

            public void PrintInfo()
            {
                Console.WriteLine($"Име: {Name}");
                Console.WriteLine($"Възраст: {Age}");
                Console.WriteLine($"Факултетен номер: {FacultyNumber}");
            }
        }

        public class University
        {
            public string Name { get; set; }
            public List<Student> Students { get; } = new List<Student>();

            // Конструктор
            public University(string name)
            {
                Name = name;
            }

            public void AddStudent(Student student)
            {
                Students.Add(student);
            }

            public void PrintStudents()
            {
                Console.WriteLine($"Студенти в университета '{Name}':");
                foreach (var student in Students)
                {
                    student.PrintInfo();
                    Console.WriteLine();
                }
            }
        }

        static void Main(string[] args)
        {
            University university = new University("Моят университет");

            Student student1 = new Student("Иван", 20, "12345");
            Student student2 = new Student("Мария", 22, "54321");
            Student student3 = new Student("Петър", 24, "28944");
    }
        
        

        }
        }
    
    




--------------

вярна + 
   public class Student //klas
        { 
            public string name;
            public int age;  // poleta
            public string fn;
            /*
            public Student(string studentname, int studentage, string studentfn)
            {
                name = studentname;
                age = studentage;
                fn = studentfn; 
            }
            */
            public void PrintInfo() // metod
            {
                Console.WriteLine(name);
                Console.WriteLine(age);
                Console.WriteLine(fn);
            }
        }
        static void Main(string[] args)
        {
            Student student1 = new Student();
            student1.name = Console.ReadLine();
            student1.age = int.Parse(Console.ReadLine());
            student1.fn = Console.ReadLine();
            student1.PrintInfo();
            Student student2 = new Student();
            student2.name = Console.ReadLine();
            student2.age = int.Parse(Console.ReadLine());
            student2.fn = Console.ReadLine();
            student2.PrintInfo(); 
              } 
#1 
        public class VOLUME
        {
            private int volume;
            public int Volume
            {
                set
                {
                    if (value <= 0)
                    {
                        Console.WriteLine("0");
                    }
                    else if (value > 100)
                    {
                        Console.WriteLine("100");
                    }
                    else
                    {
                        Console.WriteLine(value);
                    }
                    this.volume = value;
                }
                get
                {
                    return this.volume;
                }
            }

            public VOLUME()
            {
                this.volume = 0;
            }

            public VOLUME(int vv)
            {
                this.volume = vv;
            }

            static void Main(string[] args)
            {
                VOLUME volume = new VOLUME();
                int inputVolume = int.Parse(Console.ReadLine());
                volume.Volume = inputVolume;
                Console.WriteLine(volume.Volume);
            }





-------------------------------------------------------------------------------------------------------------------------------------

# loops 
задачи_сорсове за цикли(преговор)💯

//изпитни задачи  - https://csharp-book.softuni.bg/chapter-05-loops-exam-problems.html
// #3 пътуване във времето        
       
                int ytl = int.Parse(Console.ReadLine());
                double n = double.Parse(Console.ReadLine());
                int years = 18;

                for (int i = 1800; i <= ytl; i++)
                {
                    if (i % 2 == 0)
                    {
                        n -= 12000;
                    }
                    else
                    {
                        n -= 12000 + 50 * years;
                    }
                    years++;
                }

                if (n > 0)
                {
                    Console.WriteLine("Yes, left money: " + Math.Round(n, 2));
                }
                else
                {
                    Console.WriteLine("No, not enough money. Need more: " + Math.Abs(Math.Round(n, 2)));
                }
         }
     }
}



    




#2 - грешна

 int age = int.Parse(Console.ReadLine());
            double cp = double.Parse(Console.ReadLine()); // цена пералня
            int ci = int.Parse(Console.ReadLine()); // цена на играчка

            int moneyFromBD = 0;
            int BrIgracki = 0;
            int spr = 0; // prd = pari ot rd-ta , bri = broi igra4ki , spesteni pari

            for (int i = 0; i <= age; i++)
            {
                if (age % 2 == 0)
                {
                    spr = moneyFromBD - 1;
                    moneyFromBD += 10;
                }
                else
                {
                    BrIgracki++;
                }

                spr = BrIgracki * ci;

            }
            if (spr > cp) { Console.WriteLine("YEZ" + Math.Round((spr - cp), 2)); }

            else { Console.WriteLine("NO" + Math.Round((cp - spr), 2)) ; }
#1 Задача: хистограма

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace procenti_masivi_izpitnizad1
{
    class Program
    {
        static void Main(string[] args)
        {
            int br1 = 0, br2 = 0, br3 = 0, br4 = 0, br5 = 0;
            double pr1 = 0, pr2 = 0, pr3 = 0, pr4 = 0, pr5 = 0;
            int n = int.Parse(Console.ReadLine()); // br nums
            for (int i = 0; i < n; i++)
            {
                int k = int.Parse(Console.ReadLine());
                if (k >= 0 && k < 200)
                { br1++; }
                else if (k >= 200 && k <=399)
                { br2++; }
                else if (k >= 400 && k <=599)
                { br3++; }
                else if (k >= 600 && k <=799)
                { br4++; }
                else 
                { br5++; }
            }

             pr1 = ((double)br1 / n) * 100;
             pr2 = ((double)br2 / n) * 100;
             pr3 = ((double)br3 / n) * 100;
             pr4 = ((double)br4 / n) * 100;
             pr5 = ((double)br5 / n) * 100;

            Console.WriteLine(Math.Round(pr1,2));
            Console.WriteLine(Math.Round(pr2, 2));
            Console.WriteLine(Math.Round(pr3, 2));
            Console.WriteLine(Math.Round(pr4, 2));
            Console.WriteLine(Math.Round(pr5, 2));

        }
    }
}


//12 Задача: четни / нечетни позиции

Напишете програма, която чете n числа и пресмята сумата, минимума и максимума на числата на четни и нечетни позиции (броим от 1). Когато няма минимален / максимален елемент, отпечатайте "No"
ГРЕШНА!!!!!!!!!!!!!!!!!
    double n = double.Parse(Console.ReadLine());
     double minc = double.MaxValue;
    double minn = double.MaxValue;

double maxc = double.MinValue;
double maxn = double.MinValue;

double sumc = 0.0;
double sumn = 0.0;

for (int i = 0; i < n; i++)
{
    int k = int.Parse(Console.ReadLine());

    if (i % 2 == 0) // Even numbers
    {
        sumc = sumc + k;
        if (k > maxc) maxc = k;
        if (k < minc) minc = k;
    }
    else // Odd numbers
    {
        sumn = sumn + k;
        if (k > maxn) maxn = k;
        if (k < minn) minn = k;
    }
}

Console.WriteLine("Sum of even numbers = " + sumc);
Console.WriteLine("Max of even numbers = " + maxc);
Console.WriteLine("Min of even numbers = " + minc);

Console.WriteLine("Sum of odd numbers = " + sumn);
Console.WriteLine("Max of odd numbers = " + maxn);
Console.WriteLine("Min of odd numbers = " + minn);


//11 : елемент , равен на сумата на останалите
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
            
//#6 намира сумата на ел и макс ел
            
            int n = int.Parse(Console.ReadLine());
            int sum = 0;
            int max = 0; 
            for ( int i=0; i<n; i++)
            {
                 int k = int.Parse(Console.ReadLine()); 
                sum = sum + k ; /// к , не ен 
                if (k > max) max = k;
            }
            Console.WriteLine("sum= "+ sum+ ", max= " + max);
            
// #5 Да се напише програма, която въвежда n на бр числа цели числа и ги сумира.
// Вход: 2  -> Изход: 14
// 4
//10 

            int n = int.Parse(Console.ReadLine());
            int sum = 0;
            for ( int i=0; i<n; i++)
            {
                int k = int.Parse(Console.ReadLine()); // ел-те трябва да се въвеждат в цикъла, за да има всеки ен бр пъти въртенете различни стойности !!! 
                // не се дек при n , защото K ще има 1 стойност, която ще се сум ен бр пъти - пр к =10, н= 3 => сум = 30 !
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
            
            
                int i;
                for( i = 1; i<=100; i++)
                { if (i % 10 == 7)        
                        Console.WriteLine(i);               
                }
              
              
// #1
            // Да се напише програма, която печата числата от 1 до 100.
            // Програмата не приема вход и отпечатва числата от 1 до 100 едно след друго, по едно на ред.

            /*
            for (int i=1; i <= 100; i++)
            {
                Console.WriteLine(i);
            }
            */
