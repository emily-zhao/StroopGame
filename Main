using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Would you like to encrypt or decrypt?");
            string answerRaw = Console.ReadLine();
            string answer = answerRaw.ToLower();

            if (answer == "encrypt")
            {
                encryption();
            }
            else
            {
                decryption();
            }
        }

        static void encryption()
        {
            Console.WriteLine("Please enter a word or phrase without any punctuation.");
            string response = Console.ReadLine();
            string lower = response.ToLower();
            Console.WriteLine("Please enter a positive interger.");
            string tempKey = Console.ReadLine();
            int key = Convert.ToInt32(tempKey);

            List<string> alphabet = new List<string>() { "a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " " };
            List<int> codedNumbers = new List<int>();
            List<string> codes = new List<string>();

            int count = 0;
            foreach (char c in lower)
            {
                string temp = Convert.ToString(c);
                while (temp != alphabet[count])
                {
                    count++;
                }
                codedNumbers.Add(count + key);
                count = 0;
            }

            StringBuilder code = new StringBuilder();

            foreach (int i in codedNumbers)
            {
                if (i > 26)
                {
                    int fix;
                    fix = i % 26;
                    code.Append(alphabet[fix]);
                }
                else
                {
                    code.Append(alphabet[i]);
                }

            }

            Console.WriteLine(code);

            Console.ReadLine();
        }

        static void decryption()
        {
            Console.WriteLine("Enter your secret code.");
            string secretCode = Console.ReadLine();
            Console.WriteLine("Enter the secret key.");
            string tempKey = Console.ReadLine();
            int secretKey = Convert.ToInt32(tempKey);

            List<string> alphabet = new List<string>() { "a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", " " };
            List<int> codedNumbers = new List<int>();
            List<string> codes = new List<string>();

            int count = 0;
            foreach (char c in secretCode)
            {
                string temp = Convert.ToString(c);
                while (temp != alphabet[count])
                {
                    count++;
                }
                codedNumbers.Add(count - (secretKey % 26));
                count = 0;
            }

            StringBuilder code = new StringBuilder();

            foreach (int i in codedNumbers)
            {
                if (i == secretKey % 26)
                {
                    int fix;
                    fix = i - ((secretKey % 26) - 1);
                    code.Append(alphabet[fix]);
                }
                else if (i < -26)
                {
                    int fix;
                    fix = -1 * (i % 26);
                    code.Append(alphabet[fix]);
                }
                else if (i > -26 && i < 0)
                {
                    int fix;
                    fix = i + 26;
                    code.Append(alphabet[fix]);
                }
                else if (i > 26)
                {
                    int fix;
                    fix = i % 26;
                    code.Append(alphabet[fix]);
                }
                else
                {
                    code.Append(alphabet[i]);
                }

            }

            Console.WriteLine(code);

            Console.ReadLine();
        }
    }
}
