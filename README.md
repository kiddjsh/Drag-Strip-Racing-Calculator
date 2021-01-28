# Drag-Strip-Racing-Calculator
An application, using a solution algorithm that employs loops, simple data structures, and uses arrays, the application tracks the racing times of two teams, then lists the winner of each pair, giving the number of seconds the winner won by, declaring which team won based on which team had the most wins. 

# IPO Model
![Variables & IPO Model_1](https://raw.githubusercontent.com/kiddjsh/Drag-Strip-Racing-Calculator/main/images/Variable%20%26%20IPO%20Model_1.PNG)
![Variables & IPO Model_2](https://raw.githubusercontent.com/kiddjsh/Drag-Strip-Racing-Calculator/main/images/Variable%20%26%20IPO%20Model_2.PNG)

# Flowchart
![Flowchart_1](https://raw.githubusercontent.com/kiddjsh/Drag-Strip-Racing-Calculator/main/images/Flowchart_1.PNG)
![Flowchart_2](https://raw.githubusercontent.com/kiddjsh/Drag-Strip-Racing-Calculator/main/images/Flowchart_2.PNG)
![Flowchart_3](https://raw.githubusercontent.com/kiddjsh/Drag-Strip-Racing-Calculator/main/images/Flowchart_3.PNG)
![Flowchart_4](https://raw.githubusercontent.com/kiddjsh/Drag-Strip-Racing-Calculator/main/images/Flowchart_4.PNG)

# My C# Solution
```C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace fordChevy_W6
{
    class Program
    {
        static void Main(string[] args)
        {
            //variables
            double[] chevy = new double[8];
            double[] ford = new double[8];
            int chevyCount = 0, fordCount = 0; 
            double seconds = 0;

            //output greeting
            Console.ForegroundColor = ConsoleColor.Green;
            Console.WriteLine();
            Console.WriteLine("Hi! Welcome to the Race Track Time Keeper.");
            Console.WriteLine();
            Console.ForegroundColor = ConsoleColor.Green;

            //chevy input
            for (int i = 0; i < 8; i++)
            {
                Console.Write("Enter Chevy Time " + (i + 1) + ": ");
                chevy[i] = Convert.ToDouble(Console.ReadLine());
            }
            //ford input
            Console.WriteLine();
            for (int i = 0; i < 8; i++)
            {               
                Console.Write("Enter Ford Time " + (i + 1) + ": ");
                ford[i] = Convert.ToDouble(Console.ReadLine());
            }

            Console.WriteLine();
            Console.Write("And the winners are: ");

            //count
            for (int i = 0; i < 8; i++)            
            {   
                //ford count               
                if (chevy[i] > ford[i])
                {
                    Console.WriteLine();
                    seconds = chevy[i] - ford[i];
                    seconds = Math.Round(seconds, 1);  //rounding
                    Console.Write("Ford wins by " + seconds + " sec");
                    chevyCount++;
                }
                //chevy count
                else if (ford[i] > chevy[i])
                {
                    Console.WriteLine();
                    seconds = ford[i] - chevy[i];
                    seconds = Math.Round(seconds, 1);  //rounding
                    Console.Write("Chevy wins by " + seconds + " sec");
                    fordCount++;
                }

                //tie count
                else if (chevy[i] == ford[i]) 
                {
                    Console.WriteLine();
                    seconds = chevy[i] - ford[i];
                    Console.Write("Tie!");
                }
                     
            }
            if (chevyCount > fordCount)
            {
                Console.WriteLine();
                Console.WriteLine();
                Console.Write("And the winning team is: FORD");
                Console.WriteLine();
                Console.WriteLine();
                Console.Write("Press any key to continue...");
            }
            Console.ReadLine(); 
        }
    }
}
```

# Complete Working Program
![Complete Working Program](https://raw.githubusercontent.com/kiddjsh/Drag-Strip-Racing-Calculator/main/images/Complete%20Working%20Program.PNG)


