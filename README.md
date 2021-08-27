# Aplicacion.2
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.IO;

namespace Aplicación_2
{
    class Program
{
    static void Main(string[] args)
    {
        string Dirección = " Agenda.txt ";
        string Nombre = "";
        string Apellido = "";
        string Teléfono = "";

        string liena = "";

        for (int x = 0; x < 4; x++)
        {
            Console.WriteLine("Ingrese Nombre");
            Nombre = Console.ReadLine();
            Console.WriteLine("Ingrese Apellido");
            Apellido = Console.ReadLine();

            Console.WriteLine("Ingrese teléfono");
            Teléfono = Console.ReadLine();

            liena = Nombre + ";" + Apellido + ";" + Teléfono;
            EscribirArchivo(Dirección, liena);

        }

        static void EscribirArchivo(string ruta, string dato)
        {

            StreamWriter ar;
            ar = File.AppendText(ruta);
            ar.WriteLine(dato);
            ar.Close();

        }
    }
}
}
