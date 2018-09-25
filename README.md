# Examen-U1
8 programas.
Console.ForegroundColor = ConsoleColor.Black;
            Console.BackgroundColor = ConsoleColor.White;
            Console.Clear();
            string uno = "", dos = "";
            int mayor1 = 0, op = 0, menor = 0, pip, rep = 0, pos = 0, mayor = 0, a, b, c, rep1 = 0, pos1 = 0, mayor2 = 0, pop = 5, Suma1 = 0, Suma2 = 0;
            int[] vektor = new int[10]; int[] viktor = new int[50];int[] viktor1 = new int[50]; int[] victor = new int[100];int[] Vektour = new int[pop];
            while (op != 9)
            {
                Console.WriteLine("Elija una opcion: ");
                Console.WriteLine("1.-Numero mayor y menor.");
                Console.WriteLine("2.-Inversa.");
                Console.WriteLine("3.-Índice de la última ocurrencia.");
                Console.WriteLine("4.-Elemento menor entre a, b y c.");
                Console.WriteLine("5.-Índice de la primera ocurrencia.");
                Console.WriteLine("6.-");
                Console.WriteLine("7.-Lista de números random del 1 al 100 .");
                Console.WriteLine("8.-Número palindrómico.");
                op = int.Parse(Console.ReadLine());
                Console.WriteLine();
                Console.Clear();
                switch (op)
                {
                    case 1:
                        Console.WriteLine("1.-Numero mayor y menor.");
                        Console.WriteLine();
                        Random ran = new Random();
                        for (int n = 0; n < 10; n++)
                        {
                            vektor[n] = ran.Next(1, 20);
                            Console.WriteLine(vektor[n]);
                        }
                        for (int n = 0; n < 10; n++)
                        {
                            if (n == 0)
                            {
                                mayor1 = vektor[0];
                            }
                            else if (vektor[n] > mayor1)
                            {
                                mayor1 = vektor[n];
                            }
                        }
                        for (int n = 0; n < 10; n++)
                        {
                            if (n == 0)
                            {
                                menor = vektor[0];
                            }
                            else if (vektor[n] < menor)
                            {
                                menor = vektor[n];
                            }
                        }
                        Console.WriteLine(" El mayor es: " + mayor1);
                        Console.WriteLine(" El menor es: " + menor);
                        Console.WriteLine();
                        break;
                    case 2:
                        Console.WriteLine("2.-Inversa.");
                        Console.WriteLine();
                        Console.Write("Ingrese datos: ");
                        uno = Console.ReadLine();
                        for (int x = uno.Length - 1; x >= 0; x--)
                        {
                            dos = dos + uno[x];
                        }
                        Console.WriteLine("Invertido: " + dos);
                        Console.WriteLine();
                        break;
                    case 3:
                        Console.WriteLine("3.-Índice de la última ocurrencia.");
                        Console.WriteLine();
                        Random ren = new Random();
                        for (int n = 0; n < 50; n++)
                        {
                            viktor[n] = ren.Next(1, 30);
                            Console.WriteLine(viktor[n]);
                        }

                        for (int n = 0; n < 50; n++)
                        {
                            if (n == 0)
                            {
                                mayor = viktor[0];
                            }
                            else if (viktor[n] > mayor)
                            {
                                mayor = viktor[n];
                            }
                        }
                        for (int n = 0; n < 50; n++)
                        {
                            if (mayor == viktor[n])
                            {
                                rep = rep + 1;
                                pos = n + 1;
                            }

                        }
                        Console.WriteLine("Mayor: " + mayor);
                        Console.WriteLine("Numero de repeticiones: " + rep);
                        Console.WriteLine("Posicion: " + pos);
                        Console.WriteLine();
                        break;
                    case 4:
                        Console.WriteLine("4.-Elemento menor entre a, b y c.");
                        Console.WriteLine();
                        Console.WriteLine("Ingrese valor del primer dato: ");
                        a = int.Parse(Console.ReadLine());
                        Console.WriteLine("Ingrese valor del segundo dato: ");
                        b = int.Parse(Console.ReadLine());
                        Console.WriteLine("Ingrese valor del tercer dato: ");
                        c = int.Parse(Console.ReadLine());
                        if (a < b && a < c)
                        {
                            Console.WriteLine("El numero menor es " + a);
                        }
                        else
                        {
                            if (b < a && b < c)
                            {
                                Console.WriteLine("El numero menor es " + b);
                            }
                            else
                            {
                                Console.WriteLine("El numero menor es " + c);
                            }
                        }
                        Console.WriteLine();
                        break;
                    case 5:
                        Console.WriteLine("5.-Índice de la primera ocurrencia.");
                        Console.WriteLine();
                        Random ron = new Random();
                        for (int n = 0; n < 50; n++)
                        {
                            viktor1[n] = ron.Next(1, 30);
                            Console.WriteLine(viktor1[n]);
                        }

                        for (int n = 0; n < 50; n++)
                        {
                            if (n == 0)
                            {
                                mayor2 = viktor1[0];
                            }
                            else if (viktor1[n] > mayor2)
                            {
                                mayor2 = viktor1[n];
                            }
                        }
                        for (int n = 0; n < 50; n++)
                        {
                            if (mayor2 == viktor1[n])
                            {
                                rep1 = rep1 + 1;
                                pos1 = n;
                            }

                        }
                        Console.WriteLine("Mayor: " + mayor2);
                        Console.WriteLine("Numero de repeticiones: " + rep1);
                        Console.WriteLine("Posicion: " + pos1);
                        Console.WriteLine();
                        break;
                    case 6:
                        break;
                    case 7:
                        Console.WriteLine("7.-Lista de números random del 1 al 100 .");
                        Console.WriteLine();
                        Random run = new Random();
                        for (int n = 0; n < 100; n++)
                        {
                            victor[n] = run.Next(1, 100);
                            Console.WriteLine(victor[n]);

                        }
                        for (int k = 1; k < victor.Length; k++)
                            for (int y = victor.Length - 1; y >= k; y--)
                            {
                                if (victor[y - 1] > victor[y])
                                {
                                    pip = victor[y - 1];
                                    victor[y - 1] = victor[y];
                                    victor[y] = pip;
                                }
                            }
                        Console.WriteLine("Orden: ");
                        for (int n = 0; n < 100; n++)
                        {
                            Console.WriteLine(victor[n]);

                        }
                        Console.WriteLine();
                        break;
                    case 8:
                        Console.WriteLine("8.-Número palindrómico.");
                        Console.WriteLine();
                        for (int r = 0; r < Vektour.Length; r++)
                        {
                            try
                            {
                                Console.WriteLine("Ingrese 5 digitos: {0} ", r + 1);
                                Vektour[r] = int.Parse(Console.ReadLine());
                            }
                            catch (Exception)
                            {

                                Console.WriteLine("Ingrese lo indicado.");
                            }

                        }
                        Suma1 = Vektour[0] - Vektour[4];
                        Suma2 = Vektour[1] - Vektour[3];
                        if (Vektour[0] == Vektour[1] && Vektour[2] == Vektour[3] && Vektour[4] == Vektour[0])
                        {
                            Console.WriteLine("Es palíndromo");
                        }
                        else
                        {
                            if (Suma1 == 0 && Suma2 == 0 && Vektour[2] != 0)
                            {
                                Console.WriteLine("Es palíndromo");
                            }
                            else
                            {
                                Console.WriteLine("No es palíndromo");
                            }
                        }
                        Console.WriteLine();
                        break;
                }
            }
            Console.ReadKey();
