# Neighbour-Wars
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Neighbour_Wars
{
    class Program
    {
        static void Main(string[] args)
        {
            int peshosDamage = int.Parse(Console.ReadLine());
            int goshosDamage = int.Parse(Console.ReadLine());

            int peshosHelth = 100;
            int goshosHelth = 100;

            int count = 0;

            while (true)
            {
                count++;
                if (count % 2 == 0)
                {
                    peshosHelth -= goshosDamage;

                    if (peshosHelth <= 0)
                    {
                        Console.WriteLine($"Gosho won in {count}th round.");
                        return;
                    }
                    else
                    {
                        Console.WriteLine($"Gosho used Thunderous fist and reduced Pesho to {peshosHelth} health.");
                    }
                }
                else
                {
                    goshosHelth -= peshosDamage;

                    if (goshosHelth <= 0)
                    {
                        Console.WriteLine($"Pesho won in {count}th round.");
                        return;
                    }
                    else
                    {
                        Console.WriteLine($"Pesho used Roundhouse kick and reduced Gosho to {goshosHelth} health.");
                    }
                }

                if (count % 3 == 0)
                {
                    peshosHelth += 10;
                    goshosHelth += 10;
                }
            }
        }
    }
}
