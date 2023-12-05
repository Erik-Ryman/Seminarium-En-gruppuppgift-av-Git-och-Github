# Seminarium-En-gruppuppgift-av-Git-och-Github

### Grundläggande programmeringskoncept:

1. **Skillnad mellan int och double:**
   - `int` representerar heltal utan decimaler, medan `double` representerar flyttal med decimaler.
   - Exempel: `int x = 5;` och `double y = 5.0;`

2. **Representera textsträngar i C#:**
   - Använd `string` för att representera textsträngar.
   - Exempel: `string text = "Hello, World!";`

3. **Booleska datatyper i C#:**
   - `bool` används för booleska värden (sant/falskt).
   - Exempel: `bool isTrue = true;`

4. **If-else-sats:**
   - Kontrollerar en villkorlig uttryck och utför olika handlingar baserat på dess sanning.
   - Exempel:
     ```csharp
     if (condition)
     {
         // kod om villkoret är sant
     }
     else
     {
         // kod om villkoret är falskt
     }
     ```

5. **Switch-sats:**
   - Används för att välja mellan olika alternativ.
   - Skiljer sig från if-else genom att hantera flera möjliga värden.
   - Exempel:
     ```csharp
     switch (variable)
     {
         case value1:
             // kod
             break;
         case value2:
             // kod
             break;
         default:
             // kod om ingen matchning
             break;
     }
     ```

6. **Loopar (for, while, do-while):**
   - **for:** Används när antalet iterationer är känt.
   - **while:** Fortsätter att loopa så länge villkoret är sant.
   - **do-while:** Liknande while-loop, men garantin för minst en iteration.
   - Exempel:
     ```csharp
     for (int i = 0; i < 5; i++)
     {
         // kod som upprepas 5 gånger
     }
     
     while (condition)
     {
         // kod så länge villkoret är sant
     }
     
     do
     {
         // kod som körs minst en gång
     } while (condition);
     ```

7. **Användning av break och continue i loopar:**
   - `break`: Avbryter loopen och fortsätter med koden efter loopen.
   - `continue`: Hoppar över återstående kod i loopen och börjar nästa iteration.
   - Exempel:
     ```csharp
     for (int i = 0; i < 10; i++)
     {
         if (i == 5)
             break; // avsluta loopen om i är 5
         
         if (i % 2 == 0)
             continue; // hoppa över resten av loopen om i är jämnt
         
         // kod som utförs om varken break eller continue aktiveras
     }
     ```

8. **Array i C#:**
   - En samling av element av samma typ.
   - Deklaration och initiering:
     ```csharp
     int[] numbers = new int[3] { 1, 2, 3 };
     ```

9. **Flerdimensionella arrayer i C#:**
   - En array där varje element självt kan vara en array.
   - Exempel:
     ```csharp
     int[,] matrix = new int[2, 3] { { 1, 2, 3 }, { 4, 5, 6 } };
     ```

10. **Skillnad mellan == och Equals() för strängar:**
    - `==` jämför referenser, medan `Equals()` jämför innehållet.
    - Exempel:
      ```csharp
      string str1 = "hello";
      string str2 = "hello";
      bool isEqual = (str1 == str2);      // true
      bool isContentEqual = str1.Equals(str2); // true
      ```

### Objektorienterad programmering (OOP):

11. **Klass och objekt:**
    - En klass är en blåsprint för att skapa objekt, som är instanser av klassen.
    - Exempel:
      ```csharp
      class Car
      {
          // medlemsvariabler och metoder
      }
      
      Car myCar = new Car(); // skapa ett objekt av klassen Car
      ```

12. **Egenskaper (Properties) i en klass:**
    - Getter och setter för att hämta och sätta värden.
    - Exempel:
      ```csharp
      class Person
      {
          public string Name { get; set; }
      }
      
      Person person = new Person();
      person.Name = "John";
      ```

13. **Konstruktor:**
    - Används för att initialisera objekt.
    - Exempel:
      ```csharp
      class Dog
      {
          public Dog(string name)
          {
              Name = name;
          }
          
          public string Name { get; set; }
      }
      
      Dog myDog = new Dog("Buddy");
      ```

14. **Arv i C#:**
    - En klass kan ärva egenskaper och metoder från en annan klass.
    - Exempel:
      ```csharp
      class Animal { /* kod */ }
      
      class Dog : Animal { /* kod */ }
      ```

15. **Polymorfism:**
    - Ett objekt kan användas som en instans av dess överordnade typ.
    - Exempel:
      ```csharp
      Animal myDog = new Dog();
      ```

16. **Inkapsling:**
    - Döljer implementationens detaljer och tillåter åtkomst genom gränssnitt.
    - Exempel:
      ```csharp
      private int age; // inkapslad medlem
      public int Age
      {
          get { return age; }
          set { age = value; }
      }
      ```

17. **Gränssnitt (Interface):**
    - En kontrakt för att implementera vissa metoder och egenskaper.
    - Exempel:
      ```csharp
      interface IDrawable
      {
          void Draw();
      }
      ```

18. **Abstract klasser:**
    - En klass som inte kan instansieras direkt och kan innehålla abstrakta medlemmar.
    - Exempel:
      ```csharp
      abstract class Shape
      {
          public abstract void Draw();
      }
      ```

19. **Skillnad mellan static metod och

 instansmetod:**
    - En statisk metod tillhör klassen och kallas på klassnivå.
    - En instansmetod kräver en instans av klassen för att kallas.
    - Exempel:
      ```csharp
      class MathOperations
      {
          public static int Add(int a, int b) { /* kod */ }
          
          public int Multiply(int a, int b) { /* kod */ }
      }
      ```

20. **Undantagshantering (try, catch, finally):**
    - `try`: Block där undantag kan uppstå.
    - `catch`: Fångar och hanterar undantag.
    - `finally`: Kod som alltid körs, oavsett undantag eller ej.
    - Exempel:
      ```csharp
      try
      {
          // kod som kan generera undantag
      }
      catch (Exception ex)
      {
          // hantera undantaget
      }
      finally
      {
          // kod som alltid körs
      }
      ```

### Enhetstestning i C#:

21. **Syftet med enhetstestning:**
    - Säkerställer att enskilda delar av koden fungerar som förväntat.

22. **Definiera ett testfall:**
    - Enheten av testning, inklusive förväntat beteende och testdata.

23. **Positivt och negativt testfall:**
    - Positivt: Testar förväntat beteende.
    - Negativt: Testar oväntat eller ogiltigt beteende.

24. **Assert-klassen:**
    - Används för att verifiera att ett påstående är sant under enhetstestning.
    - Exempel:
      ```csharp
      Assert.AreEqual(expected, actual);
      ```

25. **Mockning:**
    - Skapar simuleringar av objekt för att testa isolerade enheter.

26. **Tillförlitliga tester:**
    - Skapa test som är deterministiska och inte beroende av externa faktorer.

27. **Kodtäckning:**
    - Mäter hur mycket av koden som täcks av enhetstester.

28. **Isolering av tester:**
    - Säkerställer att tester inte påverkar varandra och körs oberoende.

29. **Testuppsättning och testnedrivning:**
    - Testuppsättning: Förbereder testmiljö och data.
    - Testnedrivning: Återställer testmiljön efter testningen.

30. **Hantera externa beroenden i tester:**
    - Använda mockning eller testdubbel för att isolera externa beroenden.

### Testdriven utveckling (TDD):

31. **Vad är TDD:**
    - En metod där tester skrivs innan kod implementeras.

32. **Tre steg i TDD-cykeln:**
    - 1. Skriv ett test.
    - 2. Implementera kod för att passera testet.
    - 3. Refaktorisera kod utan att ändra beteendet.

33. **Varför börja med att skriva ett test:**
    - Garanterar att koden uppfyller specifikationen och är testbar.

34. **Hur TDD hjälper till att designa kod:**
    - Främjar modulär design och fokus på användning.

35. **Refaktorisering inom TDD:**
    - Omstrukturering av kod för att förbättra dess design utan att ändra beteendet.

36. **Minska antalet buggar med TDD:**
    - Tidig upptäckt och rättning av buggar genom kontinuerlig testning.

37. **Utmaningar med TDD:**
    - Inlärningskurva, initial tid och motstånd från teamet.

38. **TDD:s påverkan på samarbete i team:**
    - Främjar kommunikation och tydlig förståelse för krav.

39. **Fördelar med TDD jämfört med traditionell utveckling:**
    - Högre kodkvalitet, bättre underhållbarhet och tidig upptäckt av problem.

40. **Använda TDD i större projekt med många beroenden:**
    - Dela upp systemet i moduler och testa dem separat.

### Allmänna instuderingsfrågor:

41. **Användning av bibliotek och using-direktivet:**
    - `using` används för att inkludera namespaces och använda externa bibliotek.

42. **LINQ och dess användning för att bearbeta samlingar:**
    - Language-Integrated Query för att söka, filtrera och manipulera data i samlingar.

43. **Asynkron programmering med async och await:**
    - Används för att skapa asynkrona metoder och vänta på resultat.

44. **Delegate och dess användning i C#:**
    - En typ som representerar referens till en metod med specifik signatur.

45. **Hantering av händelser med event och delegate:**
    - Används för att informera om händelser och hantera deras hantering.

46. **Lambda-uttryck och dess användning i C#:**
    - Anonyma funktioner för att skapa korta och koncisa uttryck.

47. **Nullable<T> för att representera nullbara värden:**
    - Tillåter variabler att ha värdet null för vissa datatyper.

48. **Tuple och dess användning för att returnera flera värden:**
    - En datatyp som kan innehålla en ordnad uppsättning element.

49. **Funktion av var-nyckelordet och när det bör användas:**

50. Sista 20 frågorna med kodexempel -----------------------

51. ### Allmänna instuderingsfrågor:

41. **Användning av bibliotek och using-direktivet:**
   - Exempel: Användning av `using` för att inkludera `System`-namespace och använda `Console`-klassen.
     ```csharp
     using System;

     class Program
     {
         static void Main()
         {
             Console.WriteLine("Hello, World!");
         }
     }
     ```

42. **LINQ och dess användning för att bearbeta samlingar:**
   - Exempel: Användning av LINQ för att filtrera och projicera en lista av tal.
     ```csharp
     using System;
     using System.Linq;
     using System.Collections.Generic;

     class Program
     {
         static void Main()
         {
             List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };

             var evenSquares = numbers.Where(n => n % 2 == 0).Select(n => n * n);

             foreach (var result in evenSquares)
             {
                 Console.WriteLine(result);
             }
         }
     }
     ```

43. **Asynkron programmering med async och await:**
   - Exempel: Asynkron metod som simulerar väntetid och användning av `await`.
     ```csharp
     using System;
     using System.Threading.Tasks;

     class Program
     {
         static async Task Main()
         {
             await DoAsyncOperation();
         }

         static async Task DoAsyncOperation()
         {
             Console.WriteLine("Start async operation");
             await Task.Delay(2000); // Simulerar en asynkron operation
             Console.WriteLine("Async operation completed");
         }
     }
     ```

44. **Delegate och dess användning i C#:**
   - Exempel: Användning av en enkel delegate för att representera en funktion.
     ```csharp
     using System;

     class Program
     {
         delegate int MathOperation(int x, int y);

         static void Main()
         {
             MathOperation add = Add;
             int result = add(3, 4);
             Console.WriteLine(result);
         }

         static int Add(int a, int b)
         {
             return a + b;
         }
     }
     ```

45. **Hantering av händelser med event och delegate:**
   - Exempel: Användning av event och delegate för att hantera en händelse.
     ```csharp
     using System;

     class Program
     {
         public delegate void EventHandler(string message);
         public static event EventHandler CustomEvent;

         static void Main()
         {
             CustomEvent += DisplayMessage;
             TriggerEvent("Hello from the event!");
         }

         static void TriggerEvent(string message)
         {
             CustomEvent?.Invoke(message);
         }

         static void DisplayMessage(string message)
         {
             Console.WriteLine(message);
         }
     }
     ```

46. **Lambda-uttryck och dess användning i C#:**
   - Exempel: Användning av lambda-uttryck för att skapa korta metoder.
     ```csharp
     using System;

     class Program
     {
         static void Main()
         {
             Func<int, int, int> add = (a, b) => a + b;
             Console.WriteLine(add(3, 4));
         }
     }
     ```

47. **Nullable<T> för att representera nullbara värden:**
   - Exempel: Användning av `Nullable<T>` för att tillåta null i en int.
     ```csharp
     using System;

     class Program
     {
         static void Main()
         {
             int? nullableInt = null;
             Console.WriteLine(nullableInt.HasValue); // False
         }
     }
     ```

48. **Tuple och dess användning för att returnera flera värden:**
   - Exempel: Användning av `Tuple` för att returnera två värden från en metod.
     ```csharp
     using System;

     class Program
     {
         static void Main()
         {
             var result = GetCoordinates();
             Console.WriteLine($"X: {result.Item1}, Y: {result.Item2}");
         }

         static Tuple<int, int> GetCoordinates()
         {
             return Tuple.Create(10, 20);
         }
     }
     ```

49. **Funktion av var-nyckelordet och när det bör användas:**
   - Exempel: Användning av `var` när datatypen kan infereras av kompilatorn.
     ```csharp
     using System;

     class Program
     {
         static void Main()
         {
             var name = "John";
             var age = 30;
             Console.WriteLine($"Name: {name}, Age: {age}");
         }
     }
     ```

50. **Dynamic typ i C# och dess skillnad från andra datatyper:**
   - Exempel: Användning av `dynamic` för runtime-typning.
     ```csharp
     using System;

     class Program
     {
         static void Main()
         {
             dynamic dynamicVariable = 10;
             Console.WriteLine(dynamicVariable);

             dynamicVariable = "Hello";
             Console.WriteLine(dynamicVariable);
         }
     }
     ```
    - Används för att deklarera variabler när typen kan infereras av kompilatorn.

52. **Dynamic typ i C# och dess skillnad från andra datatyper:**
    - Tillåter runtime-typning och skiljer sig från statiska typer vid kompilering.
