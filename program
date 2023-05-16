Console.WriteLine("Enter the name of the first Pokemon");
string pok1Name = Console.ReadLine();
Console.WriteLine("Enter the name of the second Pokemon");
string pok2Name = Console.ReadLine();


int pok1Hp = 100; 
int pok2Hp = 100;

Random rng = new Random();
int pok1Dmg = 0;
int pok2Dmg = 0;
int pok1MultiDmg = 0;
int turnCount = 0;

while (pok1Hp > 0 || pok2Hp > 0)
{
    Console.WriteLine("------------Turn " + turnCount++ + "------------");
    Console.WriteLine("Choose your attack!");
    Console.WriteLine("1: Tackle");
    Console.WriteLine("2: Fury Swipes");
    pok1Dmg = rng.Next(10, 21);
    pok2Dmg = rng.Next(10, 21);
    pok1MultiDmg = rng.Next(2, 5);
    string choice = Console.ReadLine();
    if(choice == "1")
    {
        Console.WriteLine(pok1Name + " attacks " + pok2Name + " and deals " + pok1Dmg + " damage");
        Console.WriteLine(pok2Name + " attacks " + pok1Name + " and deals " + pok2Dmg + " damage");
        pok1Hp -= pok2Dmg;
        pok2Hp -= pok1Dmg;

        Console.WriteLine(pok1Name + ": " + pok1Hp);
        Console.WriteLine(pok2Name + ": " + pok2Hp);
    }
    else if(choice == "2")
    {
        for(int i = 0; i < 5; i++) 
        {
            Console.WriteLine(pok1Name + " attacks " + pok2Name + " and deals " + pok1MultiDmg + " damage");
            pok1MultiDmg = rng.Next(2, 5);
            pok2Hp -= pok1MultiDmg;
        }
        pok1Hp -= pok2Dmg;
        Console.WriteLine(pok2Name + " attacks " + pok1Name + " and deals " + pok2Dmg + " damage");
        Console.WriteLine(pok1Name + ": " + pok1Hp);
        Console.WriteLine(pok2Name + ": " + pok2Hp);

    }
    else
    {
        Console.WriteLine("Please choose a valid attack!");
        turnCount--;
    }
    if(pok1Hp <= 0 || pok2Hp <= 0)
    {
        Console.WriteLine("Battle Complete! The winner is:");
        if(pok1Hp > pok2Hp)
        {
            Console.WriteLine(pok1Name + "! You got 69 exp for battle!");
        }
        else if(pok2Hp > pok1Hp)
        {
            Console.WriteLine(pok2Name + "! Your " + pok1Name + " has fainted! Take it to the hospital now! Poor " + pok1Name + "!");
        }
        Console.ReadKey();
        break;
    }

}
