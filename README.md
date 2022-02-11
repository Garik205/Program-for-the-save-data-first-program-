# Program-for-the-save-data-first-program-
It's  my first program on the language C# and start my way in programming 

 Console.WriteLine("Welcome in security app!(for the continue click the 'enter')");
            Console.ReadLine();
            Console.WriteLine("You have 6 cell for your the data, to get more cell's please buy to premium version(click on the 'enter')" );
            Console.ReadLine();
            Console.WriteLine("You can enter their data and then create a password for their cell");
            Console.ReadLine();
            string[] data = new string[3];
            
            string[] password = new string[3];
             
            for (int i = 0; i < 2; i++)
            {
                for (int p = 0; p < 2; p++)
                {

                    Console.WriteLine("Enter number created cell");
                    byte numbercell = byte.Parse(Console.ReadLine());
                    if (numbercell < 7)
                    {

                        Console.WriteLine("Enter your data in cell number: " + numbercell, i);
                        data[numbercell] = Console.ReadLine();
                        Console.WriteLine("Create new password for their cell under the number: " + numbercell, i);
                        password[numbercell] = Console.ReadLine();
                        Console.WriteLine("Your data has been recorded in cell: " + numbercell, i);
                       
                    }
                    else
                    {
                        Console.WriteLine("For then get to more cell, please buy premium version!");
                    }
                }
                for (int y = 0; y < 20; y++)
                {
                    Console.WriteLine("Enter number your cell for the viewing in it data: ", y);
                    byte index = byte.Parse(Console.ReadLine());
                    if (index <= 6)
                    {
                        Console.WriteLine("Enter your password for the " + index, y);
                        string passwordusercell = Console.ReadLine();
                        if (passwordusercell == password[index])
                        {
                            Console.WriteLine("Your data: " + data[index], y);
                        }
                        else
                        {
                            Console.WriteLine("ERROR! Enter you password again", y);
                        }
                    }
                }
            }
