using System;

namespace ConsoleApp3
{
    class Program
    {
        static void Main(string[] args)
        {
            

            //se crea el vector
            int[] miVector = CrearVector(10);

            //se muestran los datos iniciales
            MostrarDatos(miVector);

            //AQUI EL LLAMADO A SU METODO
            MostrarDatosQuiz(miVector);

            Console.WriteLine("Fin del programa!");

        }
        public static int[] CrearVector(int tamaño)
        {
            try
            {
                int[] nuevo_vector = null;

                Console.WriteLine("Creando vector");
                if (tamaño > 0)
                {
                    nuevo_vector = new int[tamaño];
                    GenerarAleatorios(nuevo_vector);
                }
                return nuevo_vector;
            }
            catch (Exception e)
            {
                Console.WriteLine("Se generó un error creando vector." + e.Message);
                throw new Exception("ERROR CREANDO VECTOR");
            }
        }
        public static void GenerarAleatorios(int[] mi_vec, int min = 1, int max = 50)
        {
            try
            {
                Random rnd = new Random();
                Console.WriteLine("\n-- Generando datos aleatorios --");

                for (int pos = 0; pos < mi_vec.Length; pos++)
                {
                    mi_vec[pos] = rnd.Next(min, max);
                }
            }
            catch (Exception e)
            {
                Console.WriteLine("ERROR generando aleatorios: " + e.Message);
                throw new Exception("ERROR GENERANDO ALEATORIOS");
            }
        }
        public static void MostrarDatos(int[] mi_Vec)
        {
            try
            {
                Console.WriteLine("\n-- Mostrando datos originales --");

                for (int pos = 0; pos < mi_Vec.Length; pos++)
                {
                    Console.Write("| " + mi_Vec[pos]);
                }
                Console.WriteLine("| ");
            }
            catch (Exception e)
            {
                throw new Exception("ERROR MOSTRANDO DATOS: " + e.Message);
            }
        }

        public static void MostrarDatosQuiz(int[] mi_Vec)
        {
            try
            {
               for(int pos = 0; pos< mi_Vec.Length; pos++)
                {
                   if()  
                    {

                    }
                }
            }
            catch (Exception e)
            {
                throw new Exception("ERROR MOSTRANDO DATOS: " + e.Message);
            }
        }
    }
}
