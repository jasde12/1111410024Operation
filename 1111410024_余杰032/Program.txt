using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _1111410024_余杰032
{
    internal class Program
    {
        static void Main(string[] args)
        { try
            {
                string[] one = { "", "I", "II", "III", "IV", "V", "VI", "VII", "VIII", "IX" };
                string[] ten = { "", "X", "XX", "XXX", "XL", "L", "LX", "LXX", "LXXX", "XC" };
                string[] hundred = { "", "C", "CC", "CCC", "CD", "D", "DC", "DCC", "DCCC", "CM" };
                string[] thousand = { "", "M", "MM", "MMM" };
                Console.Write("輸入： num=");
                int num = int.Parse(Console.ReadLine());


                if (num < 1 || num > 3999)
                    throw new Exception("發生錯誤答案只能介於1與3999之間");
                    
                
                

                Console.WriteLine($"輸出： {thousand[num / 1000] + hundred[(num % 1000) / 100] + ten[(num % 100) / 10] + one[num % 10]}");
            }
            catch ( Exception e ) { Console.WriteLine( e.ToString() ); }

        }
    }
}
