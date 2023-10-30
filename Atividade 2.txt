using System;

public class Exercise_03
{
    public void run()
    {
        int[] vetor = { 1, 100, 30, 50, 11, 13, 5, 7, 78 };

        Console.WriteLine("Vetor não ordenado:");
        ImprimirVetor(vetor);

        InsertionSort(vetor);

        Console.WriteLine("\nVetor ordenado com Insertion Sort:");
        ImprimirVetor(vetor);
    }

    static void InsertionSort(int[] array)
    {
        int n = array.Length;
        for (int i = 1; i < n; i++)
        {
            int chave = array[i];
            int j = i - 1;

            while (j >= 0 && array[j] > chave)
            {
                array[j + 1] = array[j];
                j--;
            }
            array[j + 1] = chave;
        }
    }

    static void ImprimirVetor(int[] array)
    {
        foreach (int num in array)
        {
            Console.Write(num + " ");
        }
        Console.WriteLine();
    }
}
