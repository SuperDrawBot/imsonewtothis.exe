# imsonewtothis.exe
I have no idea what a respository even really is, but Ima put a code that I wrote in here, idunno.
I basicly did a thing that inverses the number you put in, and still mantains it as a valid natural number (no 0's to the left).
My coments are all in Portuguese cause thats my main lenguage.
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace testedemedia.lol
{
    class Program
    {
        static void Main(string[] args)
        {   
            //Inversor de Números V1.0 - Philemon da Silva Souza - 23/24.08.18
            //Teste do Desafio: Transformar um número de 4 algarismos em um algarismo inverso.

            int a, b, c, d, x, z;

            //console recebe número
            Console.WriteLine("    Inversor de números de 4 algarismos ");
            Console.WriteLine("\n Digite um número de 4 algarismos.");
            x = int.Parse(Console.ReadLine()); 

            //isola a 1 casa decimal (da esquerda pra direita), o reso é dispensado, ja que é um div
            a = x / 1000;                     
            
            //Se divirmos por 1000 e pegarmos o resto, ignoramos o primeiro número (da esquerda)
            b = ((x % 1000)/100)*10;           
            
            //Repito o processo com menos casas decimais na divisão
            c = ((x % 100) / 10)*100;

            d = ((x % 10) / 1)*1000;
            
            //Se multiplicarmos pelo inverso das casas decimais e somarmos temos o novo algarismo
            z = a + b + c + d;
            Console.WriteLine("\n O novo algarismo criado é: "+z);
            
            Console.ReadKey();
        }
    }
}
