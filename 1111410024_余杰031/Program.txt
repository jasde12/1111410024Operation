using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _1111410024_余杰031
{
    internal class Program
    {
        static void Main(string[] args)
        {
            try
            {
                Console.WriteLine("輸入:");
                Console.Write("word=");
                string input = Console.ReadLine();
                Console.Write("x=");
                string str2 = Console.ReadLine();

                string[] word = input.Split(',');

                Console.WriteLine("輸出:");

                int i = 0;
                Console.Write("[");
                foreach (char c in str2)
                {
                    bool s = char.IsLower(c);
                    if (s==false)
                    {
                        throw new Exception("x 只能使用小寫字母。");
                    }
                }
                foreach (string str in word)
                {
                    
                    bool a = str.Contains(str2);
                    int b = str.Length;
                    if (b < 1 || b > 50)
                    {
                        throw new Exception("輸入字串必須介於1到50之間");
                    }

                    if (i < 0 || i > 49)
                    {
                        throw new Exception("輸入陣列長度只能1到50之間");
                    }

                    switch (a)
                    {
                        case true:
                            Console.Write(i + " ");
                            break;
                    }
                    i++;
                }

                Console.Write("]");

            }

            catch (Exception e) 
            {
                Console.WriteLine("發生錯誤" + e.Message);
            }

        }

    }
}