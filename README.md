# Seminarium-En-gruppuppgift-av-Git-och-Github

### Grundläggande programmeringskoncept:

1. **Skillnad mellan int och double:**
   - `int` representerar heltal utan decimaler, medan `double` representerar flyttal med decimaler och med dubbel precision jämfört med float.
   - Exempel: `int x = 5;` och `double y = 5.0;`

2. **Representera textsträngar i C#:**
   - Använd datatypen `string` för att representera textsträngar.
   - Exempel: `string text = "Hello, World!";`

3. **Booleska datatyper i C#:**
   - `bool` används för booleska värden (sant/falskt) true eller false. Är det bool? kan värdet även vara null.
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
   - switchen är snabbare då den vet om sina cases men if:satsen kan kolla nestlad logik.
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
   - **for:** Används när antalet iterationer är känt. Har oftast en räknare, condition och en ökning eller minskning av räknaren.
   - **while:** Fortsätter att loopa så länge villkoret är sant. Används när man ej vet hur många varv som ska loopas som när t.ex. användaren bestämmer det.
   - **do-while:** Liknande while-loop, men garantin för minst en iteration. Den kollar condition efter att ett varv har körts sist.
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
   - `continue`: Hoppar över återstående kod i loopvarvet och börjar nästa iteration.
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

8. **Vad är en Array och hur deklareras den:**
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
   - Det kan även vara en jaggedArray. Den kan ha olika antal längd på sina inre arrayer.
     ```csharp
     int[][] myJaggedArray = new int[2][];
     myJaggedArray[0] = new int[4];
     myJaggedArray[1] = new int[2];
     ```

10. **Skillnad mellan == och Equals() för strängar:**
    - `==` jämför referenser, medan `Equals()` jämför innehållet och ger vanligtvis det resultat som förväntas. Det är säkrare att använda
    - Equals men vet man säkert att strängarna inte är null och man får förväntade resultat kan == användas för enklare syntax.
    - Exempel:
      ```csharp
      string str1 = "hello";
      string str2 = "hello";
      bool isEqual = (str1 == str2);      // true
      bool isContentEqual = str1.Equals(str2); // true
      ```

### Objektorienterad programmering (OOP):

11. **Klass och objekt:**
    - En klass är en ritning för att skapa objekt, som är instanser av klassen. Klassen beskriver alltså hur ett objekt ska vara. Vilken data och metoder som den ska ha finns i klassen.
    - Objekt eller instanser från samma klass kan alltså ha olika värden på sina variabler. 
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
    - Det ger ett sätt att kontrollera åtkomst och ändring av klassens medlemsvariabler som ofta kan vara
    - privata för utomstående klasser så att de inte kan ändra på värderna rakt på utan måste gå via get- och setmetoderna.
    - Exempel:
      ```csharp
      class Person
      {
          public string Name { get; set; }
      }
      
      Person person = new Person();
      person.Name = "John";
      ```

13. **Vad är en konstruktor och hur används den:**
    - Används för att initialisera objekt av en klass. Den körs automatiskt när ett nytt objekt skapas.
    - Syftet är att ställa in en lämplig och giltig startpunkt för objektets tillstånd.
    - Man kan ha flera konstruktorer i en klass som tar in olika parametrar. Det kallas för constructor overloading.
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
    - Klassen som ärver kalls den härledda klassen eller child eller subklass.
    - Klassen man ärver ifrån kallas basklass eller parentklass.
    - Arvet möjliggör återanvändning av kod och skapar hierakier av klasser.
    - Exempel:
      ```csharp
      class Animal { /* kod */ }
      
      class Dog : Animal { /* kod */ }
      ```

15. **Polymorfism:**
    - Ett objekt kan användas som en instans av dess överordnade typ.
    - Det är då möjligt att t.ex. skapa en lista med olika objekt som är av basklassen. Sedan kan man t.ex.
    - anropa samma metodnamn på de olika instanserna från olika klasser som genomför metoden på olika sätt.
    - Exempel:
      ```csharp
      Animal myDog = new Dog();
      ```

16. **Inkapsling:**
    - Döljer implementationens detaljer och tillåter åtkomst genom gränssnitt.
    - Man gör detta genom att använda olika nyckelord beroende på hur inkapslad (skyddad) koden ska vara mot övrig kod att nå.
    - Nyckelorden är:
    - private: Klasser, Variabler och metoder med private nås enbart i samma klass. Den mest restriktiva åtkomstnivån (störst skydd).
    - public: Klasser, Variabler och metoder med public nås från vilken kod som helst. Den mest öppna åtkomstnivån (minst skydd).
    - protected: Klasser, Variabler och metoder med protected nås endast i den egna klassen och i subklasser till denna klass.
    - internal: Klasser, Variabler och metoder med internal nås i samma assembly
    - protected internal: Klasser, Variabler och metoder med protected internal nås i samma assembly och av dess subklasser.  
    - Exempel:
      ```csharp
      private int age; // inkapslad medlem
      public int Age
      {
          get { return age; }
          set { age = value; }
      }
      ```

17. **Gränssnitt (Interface) jämfört med en klass:**
    - En kontrakt för att implementera vissa metoder och egenskaper.
    - Gränssnittet tillåter dig att definiera funktionalitet utan att ange implementation.
    - Det beskriver vad en klass bör göra men inte hur det ska göras.
    - En klass kan använda flera gränssnitt samtidigt, vilket möjliggör en form av flerfaldigt arv för metoder och egenskaper.
    - En klass kan endast ärva från en basklass direkt.
    - Gränssnitt använder nyckelordet interface för att definiera gränssnittet och en klass använder class för att definiera klasser.
    - Exempel:
      ```csharp
      interface IDrawable
      {
          void Draw();
      }
      ```

18. **Abstract klasser:**
    - En klass som inte kan instansieras direkt och kan innehålla abstrakta medlemmar men också vanliga medlemmar (egenskaper och metoder).
    - Används för att tillhandahålla en basstruktur för andra klasser.
    - Den klass som ärver av en abstrakt klass måste implementera de abstrakta metoderna som finns i den abstrakta klassen.
    - Exempel:
      ```csharp
      abstract class Shape
      {
          public abstract void Draw();
      }
      ```

19. **Skillnad mellan static metod och instansmetod:**
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
    - `try`: Block av kod där undantag kan uppstå.
    - `catch`: Fångar och hanterar undantag som kan ske i try-blocket.
    - `finally`: Kod som alltid körs sist, oavsett undantag eller ej.
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
    - En enskild del kan vara en funktion, metod, klass eller någon annan isolerad del av koden.

22. **Definiera ett testfall:**
    - Enheten av testning, inklusive förväntat beteende och testdata.
    - Testramverk som t.ex. NUnit, MSTest och xUnit eller liknande används för att utföra testfall.
    - Man skriver [TestFixture] ovanför klassnamnet som ska göra testet och [Test] ovanför en testmetod.
    - I ett test så har man:
    - Arrange: som förbereder objektet och tillstånd som behövs för testet.
    - Act: som utför den specifika åtgärd som testet fokuserar på.
    - Assert: som validerar att resultatet är som förväntat.

23. **Positivt och negativt testfall:**
    - Positivt: Testar förväntat beteende i koden, alltså det man vill ska hända i programmet.
    - Negativt: Testar oväntat eller ogiltigt beteende, alltså det man inte vill ska hända i koden som undantag och fel som kan uppstå. Exempelvis om man ska testa om koden kan hantera vad som ska hända om vi dividerar med noll.

24. **Assert-klassen:**
    - Används för att verifiera att ett påstående är sant under enhetstestning. Det kan vara exempelvis om ett förväntat värde är lika med ett faktiskt värde, eller inte, eller kollar om något är sant (boll-uttryck), Null-kontroller, Exception-hantering. Kan även vara om två värden är lika inom en viss tolerans.
    - Exempel:
      ```csharp
      Assert.AreEqual(expected, actual);
      ```

25. **Mockning:**
    - Skapar simuleringar av objekt för att testa isolerade enheter med ett mockingramverk som exempelvis Moq (Rhino Mocks, NSubstitute beror på vilket testramverk som används).
    - Med mocking skapas falska (mockade) objektför att ersätta verkliga beroenden i din kod.
    - Syftet är att isolera den enhet av koden som testas genom att simulera beteendet hos externa beroenden och verifiera hur enheten integrerar med dem.
    - Externa tjänster, databaser eller andra resurseer kan simuleras.
    - Skapa förutsägbara tester.
    - Ökar prestandan om dina beroenden är långsamma eller kostsamma att använda.
    - Testa undantagssituationer.

26. **Tillförlitliga tester:**
    - Skapa test som är deterministiska och inte beroende av externa faktorer.
    - Följa AAA-mönstret med Arrange, Act och Assert.
    - Variera testdatan med olika typer av inmatning.
    - Använd assertions klokt, tydliga och korrekta assertions.
    - Automatisera testerna så de är enkla att köra och ofta.
    - Kör tester i isolerade miljöer.
    - Följ god praxis.
    - Utvärdera testtäckning (hur stor del av koden som testas). Sträva efter hög testtäckning.
    - Granska tester tillsammans med andra och ta emot feedback från dem. 

27. **Kodtäckning (testtäckning):**
    - Mäter hur stor del av koden som täcks av enhetstester.
    - Man kan hitta otestad kod.
    - Stödjer refaktorisering.
    - Stödjer regressionstestning genom att hjälpa till att säkerställa att befintlig funktionalitet inte bryts när ny kod läggs till. Man får indikationer på vilken kod som ska testas efter förändringar.
    - Identifiera onödig eller oanvänd kod. Detta kan visa på att kod ska tas bort eller att testsviten kan förbättras.
    - Hög kodtäckning är nödvändigtvis inte garanti för att koden är helt felfri från buggar. Man kan ändå ha missat att testa viktiga scenarier.

28. **Isolering av tester:**
    - Säkerställer att tester inte påverkar varandra och körs oberoende.
    - Använda mockade objekt så kan man undvika att påverka andra tester som använder samma resurser eftersom de simuleras och inte förändras på direkt.
    - Återställa tillstånd mellan varje test. Det kan vara att återställa databasen, objektinstanser eller andra resurser som har ändrats under testet.
    - Använd testfiktioner (fixtures) för att etablera en känd startpunkt för testerna. [SetUp] och [TearDown].
    - Använd unik testdata för varje test.
    - Undvik att använda globala tillståndsvariabler som kan påverkas mellan testerna.
    - Använd parallell körning om det går så att man ej behöver delade resurser på varje test.
    - Använda dependency injection (DI). Man tar t.ex. in ett objekt i konstruktorn och sätter värdet på den där istället för att skapa objektet i klassen.

29. **Testuppsättning och testnedrivning:**
    - Testuppsättning: Förbereder testmiljö och data.
    - Testnedrivning: Återställer testmiljön efter testningen.
    - Genom att använda testuppsättning och testnedrivning kan du skapa en konsekvent och pålitlig testmiljö för varje test. Detta gör att testerna blir mer isolerade och upprepningsbara och bidrar till att säkerställa att testerna ger korrekta och förutsägbara resultat.

30. **Hantera externa beroenden i tester:**
    - Använda mockning eller stubbing för att isolera externa beroenden.
    - Använda In-Memory-databaser som körs snabbt och temporärt i minnet, exempelvis SQLite eller ORM (Object-Relational Mapping)-ramverk.
    - Använda textfixturer som implementerar och rensar upp mellan varje test.
    - Rulla tillbaka ändringar som sker under testet om det går (stöds) i databasen.
    - Använd separata konfigurationsfiler. Exempel använda en annan testdatabas än den som används i produktionsmiljön.
    - Använd Dependency injection (DI).
    - Använda databas-backuper. Detta görs så att man inte påverkar den "riktiga" databasen utan bara en kopia under testerna. Man vet också en känd mängd som testet körs mot då det är bestämt i databaskopian.

### Testdriven utveckling (TDD):

31. **Vad är TDD:**
    - En metod där tester skrivs innan kod implementeras.

32. **Tre steg i TDD-cykeln:**
    - 1. Skriv ett test.
    - 2. Implementera kod för att passera testet.
    - 3. Refaktorisera kod utan att ändra beteendet, alltså gör den mer lättläslig men ändra inte beteendet. 

33. **Varför börja med att skriva ett test:**
    - Garanterar att koden uppfyller specifikationen och är testbar.
    - Lättare att förstå kraven.
    - Säkerhetställer testbarheten.
    - Tydligare kravspecifikation.
    - Säkerhetställer testtäckning så att det som är viktigt att testa faktiskt testas.
    - Förändringshantering så man ser att förändringar inte har saboterat(ändrat beteende) hos tidigare kod.
    - Agil iterativ utveckling. Den cykliska processen att skriva test, implementera kod och refaktorisera möjliggör ständiga förbättringar och anpassningar till koden.
    - Snabb återkoppling. Koden blir testbar från början direkt.

34. **Hur TDD hjälper till att designa kod:**
    - Främjar modulär design och fokus på användning.
    - Enkla och klara implementationer.
    - Förebygger kodupprepning (DRY-principen).
    - Iteration och förbättring. Koden utvecklas stegvis.
    - Förändringsvänlig kod. Kan enkelt kolla om koden fortfarande uppfyller kraven genom att köra testerna snabbt.
    - Tydligare ansvar och rollfördelning på koden (vilken kod som ska göra vad).
    - Man får feedback om designbesluten från testerna. Är koden svår att testa kan det vara ett tecken på att den behöver förenklas eller omarbetas.

35. **Refaktorisering inom TDD:**
    - Omstrukturering av kod för att förbättra dess design och läsbarhet utan att ändra beteendet.
    - Underlättar förändringar.
    - Minskar buggar.

36. **Minska antalet buggar med TDD:**
    - Tidig upptäckt och rättning av buggar genom kontinuerlig testning.
    - Automatiserade tester.
    - Förhindrande av överimplementering.
    - Bättre förståelse av krav för det behöver förstås innan koden skrivs.
    - Ökad testtäckning ökar sannorlikheten att buggar hittas.
    - Förebyggande av teknisk skuld så att man inte skjuter upp refaktorisering till senare.
    - Snabb återkoppling.

37. **Utmaningar med TDD:**
    - Inlärningskurva, initial tid och motstånd från teamet.
    - Kräver diciplin.
    - Startkostnaden.
    - Underhåll av testerna.
    - Fokus på kvantitet istället för kvalitet. Risk att man gör för många tester istället för att fokusera på det som är viktigt att testa.
    - Integrering i befintliga processer kan vara en utmaning.
    - Ytterligare tidsåtgång: Initialt så kan detta uppfattas som tidskrävande men på lång sikt blir det mer effektivt då tester är förberedda och buggar kan upptäckas enklare.

38. **TDD:s påverkan på samarbete i team:**
    - Främjar kommunikation och tydlig förståelse för krav vilket ledertill minskad risk för missförstånd inom teamet.
    - Förbättrad kommunikation eftersom teamet behöver i förväg diskutera och förstå vad koden ska göra.
    - Förbättrad kodkvalitet vilket förenklar för teamet att lättare kunna läsa och kunna förstå koden.
    - Ökar förtroende och säkerhet eftersom man får snabb feedback av testerna om man brytit något i koden.
    - Ökad delning av kunskap i teamet vilket ger jämnare kunskapsfördelning.

39. **Fördelar med TDD jämfört med traditionell utveckling:**
    - Högre kodkvalitet, bättre underhållbarhet och tidig upptäckt av problem, snabbare utveckling, bättre skalbarhet.

40. **Använda TDD i större projekt med många beroenden:**
    - Dela upp systemet i moduler och testa dem separat.
    - Mocka externa beroenden.
    - Använd dependency injection.
    - Ha klara och väldefinierade kodstandarder.
    - Uppmuntra till kommunikation och samarbete.

### Allmänna instuderingsfrågor:

41. **Användning av bibliotek och using-direktivet:**
    - `using` används för att inkludera namespaces, använda externa bibliotek och NuGet-paket.
    - Sammanfattningsvis används using-direktivet för att inkludera namnområden och göra dem tillgängliga i koden. Referenser till externa bibliotek används för att inkludera kod från andra assemblys i ditt projekt. Detta bidrar till att organisera och återanvända kod på ett effektivt sätt.

42. **LINQ och dess användning för att bearbeta samlingar:**
    - Language-Integrated Query för att söka, filtrera och manipulera data i samlingar på ett standardmässigt sätt.
    - Language Integrated Query (LINQ) är en funktion i C# och andra .NET-språk som ger en samlingsorienterad syntax för att utföra frågor och operationer på datakällor, såsom samlingar, databaser och XML. LINQ möjliggör enklare och mer deklarativ kod för att bearbeta och analysera data.
   - LINQ använder en deklarativ syntax som liknar SQL. Detta gör koden mer läsbar och uttrycksfull. Till exempel:
     ```csharp
     var result = from person in persons
                  where person.Age > 18
                  select person.Name;
     ```
   - LINQ erbjuder en uppsättning standard query operators (metoder) som kan användas för att utföra vanliga operationer som filter, sortering, projektion och gruppering på samlingar.

     ```csharp
     var adults = persons.Where(person => person.Age > 18);
     var names = persons.Select(person => person.Name);
     var sortedNames = persons.OrderBy(person => person.Name);
     ```
   - LINQ integreras sömlöst med olika typer av samlingar i C#. Du kan använda LINQ-uttryck för att bearbeta arrayer, listor, dictionaries och andra samlingar.
   - LINQ använder principen om deferred execution. Det innebär att en LINQ-fråga inte utförs omedelbart när den skapas, utan fördröjs tills resultatet behövs. Detta kan vara fördelaktigt för prestanda.
   - LINQ fungerar väl med anonyma typer, vilket är användbart när du vill projicera resultatet av en fråga till ett tillfälligt format.

     ```csharp
     var query = from person in persons
                 where person.Age > 18
                 select new { person.Name, person.Age };
     ```
   - LINQ kan användas för att skriva förfrågningar mot databaser genom LINQ to SQL eller Entity Framework. Det ger en enhetlig syntax för att arbeta med både samlingar och databaser.

     ```csharp
     var query = from customer in dbContext.Customers
                 where customer.City == "New York"
                 select customer;
     ```
   - LINQ kan också användas för att utföra frågor och operationer på XML-data. Det finns LINQ to XML för att underlätta XML-bearbetning.

     ```csharp
     var query = from element in xml.Elements("Person")
                 where (int)element.Element("Age") > 18
                 select element.Element("Name").Value;
     ```
LINQ gör kodbasen mer uttrycksfull och minskar mängden boilerplate-kod som krävs för att bearbeta samlingar och andra datakällor. Det ger även en enhetlig syntax oavsett vilken typ av datakälla du arbetar med. LINQ är kraftfullt och kan göra din kod mer läsbar och underhållbar genom att förenkla bearbetningen av data.
   
43. **Asynkron programmering med async och await:**
    - Används för att skapa asynkrona metoder och vänta på resultat.
    - Asynkron programmering i C# med `async` och `await` introducerades för att hantera situationer där en operation tar tid att slutföra, till exempel nätverksanrop, databasanrop eller andra I/O-operationer. Genom att använda asynkrona metoder kan du undvika att blockera den exekverande tråden och därmed förhindra att gränssnittet låses under långa väntetider.

   - När du skapar en metod som innehåller asynkron kod, märk metoden med `async`-modifikatorn. Till exempel:

     ```csharp
     private async Task<string> GetDataAsync()
     {
         // Asynkron kod här
         // ...
         return result;
     }
     ```
   - Inuti en asynkron metod används `await` för att invänta en asynkron operation. `await` används med en uppgift (Task) och säger att metoden ska vänta på att uppgiften slutförs innan den går vidare.

     ```csharp
     private async Task<string> ProcessDataAsync()
     {
         string data = await GetDataAsync();
         // Fortsätt med bearbetning efter att GetDataAsync är klart
         // ...
         return processedData;
     }
     ```
   - `Task` används för att representera asynkrona operationer. `Task<T>` representerar en asynkron operation som returnerar ett resultat av typen T. Du kan använda inbyggda .NET-metoder som returnerar uppgifter eller konvertera synkrona metoder till asynkrona genom att använda `Task.Run()`.

     ```csharp
     private async Task<int> AddAsync(int a, int b)
     {
         return await Task.Run(() => a + b);
     }
     ```
   - Du kan hantera flera asynkrona operationer samtidigt genom att använda `Task.WhenAll` eller `Task.WhenAny`. `Task.WhenAll` inväntar att alla givna uppgifter är slutförda, medan `Task.WhenAny` inväntar att åtminstone en av dem är klar.

     ```csharp
     private async Task DoMultipleAsync()
     {
         Task<int> task1 = SomeAsyncOperation();
         Task<string> task2 = AnotherAsyncOperation();

         await Task.WhenAll(task1, task2);

         int result1 = task1.Result;
         string result2 = task2.Result;
     }
     ```

   - Användning av `async` och `await` förhindrar onödig blockering av den exekverande tråden. När en asynkron operation väntar på att slutföras, frigörs tråden för att utföra andra uppgifter, vilket förhindrar låsning av gränssnittet.
   - Asynkron programmering med `async` och `await` möjliggör förbättrad prestanda och responsivitet i applikationer genom att undvika blockeringar under väntetider för I/O- eller nätverksoperationer. Det ger också en enhetlig och läsbar syntax för att hantera asynkrona uppgifter i C#.

44. **Delegate och dess användning i C#:**
    - En typ som representerar referens till en metod med specifik signatur.
  I C# är en delegat en typ som representerar referenser till metoder med en särskild signatur. Delegater möjliggör hantering av funktioner som förstklassiga medborgare, vilket innebär att du kan behandla metoder som data och passa dem som argument till andra metoder eller returnera dem som resultat.

   - Du definierar en delegattyp med `delegate`-nyckelordet. Delegattypen anger signaturerna (parameterlista och returtyp) för de metoder som kan refereras till av den här delegaten.

     ```csharp
     // Delegatdefinition för en metod som tar två heltal och returnerar en heltal
     public delegate int MathOperation(int x, int y);
     ```
   - Du skapar en instans av en delegat genom att tilldela den en referens till en befintlig metod eller genom att använda en anonym metod eller lambda-uttryck.

     ```csharp
     MathOperation add = (a, b) => a + b;  // Användning av ett lambda-uttryck
     MathOperation multiply = delegate (int x, int y) { return x * y; };  // Användning av en anonym metod
     ```
   - Du anropar en delegat på samma sätt som du anropar en metod. Detta kommer att leda till att den refererade metoden exekveras.

     ```csharp
     int resultAdd = add(5, 3);        // Resultat: 8
     int resultMultiply = multiply(4, 6);  // Resultat: 24
     ```
   - En delegat kan referera till flera metoder samtidigt. Detta kallas multicast-delegater och uppnås genom att använda `+=` och `-=` för att lägga till eller ta bort metoder från delegatens invocation-lista.

     ```csharp
     MathOperation operation = add;
     operation += multiply;

     int result = operation(2, 3);
     // Resultatet kommer att vara resultatet av både add och multiply: (2 + 3) * 2 = 10
     ```
   - .NET erbjuder flera fördefinierade generiska delegater i `System`-namnområdet, t.ex. `Func<T1, T2, TResult>` och `Action<T1, T2>`. Dessa används ofta för att undvika att skapa egna delegatdefinitioner.

     ```csharp
     Func<int, int, int> add = (a, b) => a + b;
     Action<int, int> displaySum = (x, y) => Console.WriteLine($"Sum: {x + y}");
     ```
   - Delegater används ofta för att implementera callback-mönster, där en metod överförs som en parameter till en annan metod för senare exekvering.

     ```csharp
     void PerformOperation(int x, int y, MathOperation operation)
     {
         int result = operation(x, y);
         Console.WriteLine($"Result: {result}");
     }

     PerformOperation(8, 4, add);       // Resultat: 12
     PerformOperation(5, 3, multiply);  // Resultat: 15
     ```
Delegater är användbara i många situationer, inklusive händelsesystemet, asynkron programmering och mönstret observer (observer pattern), där de möjliggör löst kopplade och återanvändbara komponenter. De gör det möjligt att skriva mer flexibla och utbytbara kodbaser genom att tillåta dynamiskt utbyte av implementationer av metoder.

45. **Hantering av händelser med event och delegate:**
    - Används för att informera om händelser och hantera deras hantering.
   I C# används delegater och händelser (events) för att implementera mönstret Observer, vilket möjliggör kommunikation och återkoppling mellan olika delar av en applikation. Här är en grundläggande förklaring av hur du kan hantera händelser med event och delegate:
   - Definiera en delegattyp som kommer att användas för att hantera händelsen. Detta kan vara en delegat med en passande signatur beroende på det data som ska skickas när händelsen inträffar.

     ```csharp
     public delegate void MyEventHandler(object sender, EventArgs e);
     ```
   - Deklarera en händelse som använder den tidigare definierade delegaten. Händelsen kan användas av andra klasser för att prenumerera på händelsemeddelanden.

     ```csharp
     public class MyClass
     {
         public event MyEventHandler MyEvent;
     }
     ```
   - Inuti klassen som har händelsen (oftast kallad utgivaren) utlöses händelsen vid behov. Detta görs genom att anropa delegatet associerat med händelsen.

     ```csharp
     public class MyClass
     {
         public event MyEventHandler MyEvent;

         public void RaiseEvent()
         {
             // Kolla om någon prenumererar på händelsen innan du utlöser den
             MyEvent?.Invoke(this, EventArgs.Empty);
         }
     }
     ```
   - Andra klasser (oftast kallade prenumeranter eller lyssnare) kan prenumerera på händelsen genom att ansluta sina metoder till händelsedelegatet. Detta görs med hjälp av `+=`-operatorn.

     ```csharp
     public class AnotherClass
     {
         public void Subscribe(MyClass myObject)
         {
             myObject.MyEvent += MyEventHandlerMethod;
         }

         private void MyEventHandlerMethod(object sender, EventArgs e)
         {
             Console.WriteLine("Händelse inträffade!");
         }
     }
     ```
   - Många klasser kan prenumerera på samma händelse. När händelsen inträffar, kommer alla prenumeranter att få meddelandet.

     ```csharp
     MyClass myObject = new MyClass();
     AnotherClass subscriber1 = new AnotherClass();
     AnotherClass subscriber2 = new AnotherClass();

     subscriber1.Subscribe(myObject);
     subscriber2.Subscribe(myObject);

     myObject.RaiseEvent();  // Båda prenumeranter kommer att få meddelandet
     ```
   - Klasser kan också avsluta sin prenumeration på händelsen genom att använda `-=`-operatorn.

     ```csharp
     public class AnotherClass
     {
         public void Unsubscribe(MyClass myObject)
         {
             myObject.MyEvent -= MyEventHandlerMethod;
         }

         // ...
     }
     ```

Händelser och delegater ger en lös koppling mellan olika delar av din applikation, vilket möjliggör flexibilitet och återanvändbarhet. De används ofta inom GUI-programmering, asynkron programmering och andra situationer där lös koppling och observermönstret är fördelaktiga.

46. **Lambda-uttryck och dess användning i C#:**
    - Anonyma funktioner för att skapa korta och koncisa uttryck.
    - Lambda-uttryck är en kort och kompakt syntax i C# som gör det möjligt att definiera anonyma metoder. De används främst för att skapa snabbt och enkelt läslig kod när du behöver skicka en funktion som parameter till en metod eller när du vill skapa korta och enkla metoder direkt i koden.
     ```csharp
      (parameters) => expression
     ```
parameters: En lista med parametrar som metoden tar emot.
 
=>: Lambda-operatören, som ersätter delegate-nyckelordet.
 
expression: Uttrycket som utvärderas och returneras av metoden.

Lambda-uttryck som en enkel metod:
```csharp
// Traditionell metod
int Square(int x) => x * x;

// Lambda-uttryck
Func<int, int> square = x => x * x;
```
I det här fallet används lambda-uttrycket för att definiera en enkel metod för att beräkna kvadraten av ett tal.

Lambda-uttryck som en anonym metod:
```csharp
// Traditionell anonym metod
var list = new List<int> { 1, 2, 3, 4, 5 };
var evenNumbers = list.FindAll(delegate (int i) { return i % 2 == 0; });

// Lambda-uttryck som anonym metod
var evenNumbersLambda = list.FindAll(i => i % 2 == 0);
```
Lambda-uttryck kan användas för att skapa anonyma metoder direkt vid användningen, vilket gör koden mer kompakt och läsbar.

Lambda-uttryck gör koden mer läsbar och minskar behovet av att deklarera separata metoder när en kort och enkel operation är önskad. De är särskilt användbara i situationer där du behöver passera en funktion som parameter eller när du arbetar med LINQ och andra funktionella programvarumönster i C#.

47. **Nullable<T> för att representera nullbara värden:**
    - Tillåter variabler att ha värdet null för vissa datatyper.
    - Används främst där ett värde är okänt eller inte tillämpligt och du vill ha möjlighet att skilja på ett giltigt värde och frånvaron av ett värde. 

48. **Tuple och dess användning för att returnera flera värden:**
    - En datatyp som kan innehålla en ordnad uppsättning element.
    - En tuple är en typ i C# som möjliggör att gruppera flera värden i en enda struktur. Detta är användbart när du behöver returnera eller hantera flera värden som en enhet. Tuples är särskilt användbara när antalet värden är litet och när du inte vill skapa en egen klass eller använda en out-parametrar för att returnera flera värden från en metod.

Du kan skapa en tuple på flera sätt, men ett av de vanligaste sätten är att använda `Tuple`-klassen eller att använda tupel-syntaxen introducerad i C# 7.

   ```csharp
   // Skapa en Tuple med två värden
   Tuple<int, string> myTuple = new Tuple<int, string>(42, "Hello");

   // Åtkomst till Tuple-värden
   int value1 = myTuple.Item1;
   string value2 = myTuple.Item2;
   ```

- Användning av tupel-syntax (C# 7 och senare):
   ```csharp
   // Skapa en Tuple med tupel-syntax
   var myTuple = (42, "Hello");

   // Åtkomst till Tuple-värden
   int value1 = myTuple.Item1;
   string value2 = myTuple.Item2;
   ```
Du kan använda en tuple för att returnera flera värden från en metod, vilket gör koden mer läsbar och kompakt.

```csharp
public (int, string) GetValues()
{
    // Utför någon logik för att generera värden
    int intValue = 42;
    string stringValue = "Hello";

    // Returnera en tuple
    return (intValue, stringValue);
}
```

När du använder metoden kan du direkt dekonstruera tupeln för att få åtkomst till dess värden.

```csharp
var result = GetValues();

// Dekonstruera tupeln
int resultValue1 = result.Item1;
string resultValue2 = result.Item2;

// Eller med tupel-syntax
var (resultValue1, resultValue2) = GetValues();
```

Namngivna tuplar (C# 7.1 och senare):
Från C# 7.1 och framåt kan du använda namngivna tuplar, vilket gör det ännu tydligare vilket värde som representerar vad.

```csharp
public (int Value, string Text) GetNamedValues()
{
    int intValue = 42;
    string stringValue = "Hello";

    // Returnera en namngiven tuple
    return (Value: intValue, Text: stringValue);
}
```

Och när du använder resultaten:

```csharp
var result = GetNamedValues();

// Åtkomst med namngivna tupel-element
int resultValue = result.Value;
string resultText = result.Text;
```

- Tuples är särskilt användbara när du vill returnera eller hantera en mindre mängd värden utan att behöva skapa egna klasser eller använda out-parametrar. De gör koden mer läsbar och minskar mängden boilerplate-kod. Namngivna tuplar ytterligare förbättrar tydligheten i koden.

49. **Funktion av var-nyckelordet och när det bör användas:**
   - Användningen av var i C# kan göra koden mer läsbar genom att reducera redundansen och förbättra underhållbarheten i vissa situationer. Här är några sätt på vilka var kan bidra till ökad läsbarhet:
   - Kortare kod: Användning av var resulterar i kortare kodrader, särskilt när du skapar objekt eller instanser av komplexa datatyper, som generiska listor eller dictionaries. Detta minskar mängden upprepade datatyper och gör koden mer koncis.
   - Tydligare kod med anonyma typer och LINQ:
När du arbetar med anonyma typer eller LINQ-frågor kan var göra koden tydligare genom att minska komplexiteten och fokusera på logiken snarare än de specifika typerna.
   - Tydligare deklaration med komplexa typer:
När datatypen är uppenbar från tilldelningen, gör var deklarationen tydligare genom att fokusera på variabelns syfte snarare än den exakta datatypen.
   - Enklare hantering av generiska typer:
Användning av var underlättar hanteringen av generiska typer, särskilt när de är komplexa och deras namn är långa. Detta bidrar till att undvika onödig förbenning.
Viktigt att notera:
Tydlig tilldelning:
Använd var när tilldelningen tydligt indikerar datatypen. Om datatypen inte är uppenbar, kan det minska kodens läsbarhet.
Använd med omdöme:
Använd var med omdöme och överväg läsbarheten. För vissa typer av variabler kan det vara bättre att explicit ange datatypen för att göra koden tydligare.
Kommentarer:
Använd kommentarer när det är nödvändigt att klargöra variabeltypen för andra utvecklare.
I slutändan är användningen av var en stildirektivsfråga, och koden bör skrivas på ett sätt som gör den mest förståelig för teamet och underhållare av koden.

50. Vad är en dynamic typ i C# och hur skiljer den sig från andra datatyper?
`dynamic` är en datatyp i C# som introducerades med C# 4.0. Till skillnad från statiska typer som `int`, `string` och `List<T>`, är `dynamic` en typ som tillåter dynamisk typning vid körtid. Det innebär att datatypen för en variabel som deklareras som `dynamic` bestäms vid körtid snarare än vid kompileringstid. Detta ger mer flexibilitet och löst kopplad kod.

Här är några viktiga egenskaper och skillnader för `dynamic` jämfört med andra datatyper:
   - Med `dynamic` kan du skapa variabler utan att deklarera en specifik datatyp vid kompileringstid. Typen bestäms istället vid körtid.

     ```csharp
     dynamic myVariable = 10;
     myVariable = "Hello, World!";
     ```
   - Typen för en `dynamic`-variabel kontrolleras vid körtid snarare än vid kompileringstid. Detta innebär att fel relaterade till typning upptäcks vid körning istället för vid kompilering.

     ```csharp
     dynamic myVariable = 10;
     myVariable = "Hello, World!";
     int length = myVariable.Length;  // Kastar ett undantag vid körning
     ```
   - Eftersom `dynamic` bestämmer datatyp vid körtid, saknas kompiltidsintellisens. Kompilatorn ger inte samma nivå av statisk kontroll och kodkomplettering som med statiska typer.

     ```csharp
     dynamic myVariable = "Hello, World!";
     int length = myVariable.Length;  // Ingen kodkomplettering för Length
     ```
   - Användningen av `dynamic` ger större flexibilitet, men det kan också öka risken för fel vid körning om du inte är försiktig med hur du använder variabler av dynamisk typ.

     ```csharp
     dynamic x = 10;
     dynamic y = "Hello";
     dynamic result = x + y;  // Kommer att orsaka fel vid körning (RuntimeBinderException)
     ```
   - `dynamic` är användbart i scenarier där du arbetar med objekt vars datatyp inte är känt vid kompileringstid, till exempel när du interagerar med dynamiska objekt från andra plattformar, reflection, eller när du skapar generiska och flexibla API:er.

     ```csharp
     dynamic dynamicObject = GetDynamicObject();
     var propertyValue = dynamicObject.SomeProperty;
     ```

### Viktigt att notera:
  - Användningen av `dynamic` kan påverka prestanda, eftersom typinformationen måste utvinnas vid körning. Dessutom ökar risken för typrelaterade fel. Använd därför `dynamic` med omdöme och överväg de specifika kraven för ditt scenario.
  - I allmänhet är det bästa att använda statiska typer för att dra nytta av kompilatorns typkontroll och för att förbättra kodens läsbarhet och underhållbarhet.

```csharp
// Undvik dynamisk typ om möjligt
dynamic myVariable = GetDynamicObject();
var propertyValue = myVariable.SomeProperty;
```
Sammanfattningsvis ger `dynamic` flexibilitet i situationer där datatypen är okänd vid kompileringstid, men användningen bör balanseras med medvetenhet om dess påverkan på kodens säkerhet och prestanda. Använd det i situationer där dynamisk typning är nödvändig och ger en fördel.

### Allmänna instuderingsfrågor:

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
    - Tillåter runtime-typning och skiljer sig från statiska typer vid kompilering.# studyToOOPTest
