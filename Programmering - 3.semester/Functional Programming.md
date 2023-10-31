# Funktionel Programmering i Java
Funktionel programmering er en programmeringsstil, der behandler beregninger som evaluering af matematiske funktioner. I matematik er en funktion et udtryk, der relaterer et input sæt til et output sæt. Outputtet af en funktion afhænger kun af sit input. Vi kan sammensætte to eller flere funktioner sammen for at få en ny funktion.

## First Class Functions, Lambda, Higher Order Functions
Java understøtter konceptet om "first-class functions". Det betyder, at det behandler funktioner som udtryk af enhver anden type. Funktioner er som ethvert andet objekt. Dette kan illustreres ved hjælp af følgende kode:

```
function runFunction(fn, data) {
  return fn(data);
}
```

Lambda udtryk i Java er en nem og effektiv måde at implementere funktionelle interfaces på, hvilket gør implementeringen af højere ordens funktioner meget nemmere. Højere ordens funktioner er funktioner, der tager en eller flere funktioner som parametre eller returnerer en funktion som resultat.

## Brugen af Streams i Java
Java 8 introducerede konceptet om streams, som er en sekvens af elementer, der understøtter forskellige metoder til effektivt at håndtere data i funktionel stil. Metoderne inkluderer map, reduce, filter, collect osv.

- Map metoden bruges til at transformere elementerne i en strøm ved at anvende en funktion til hvert element og returnere en ny strøm, der indeholder de transformerede elementer.

```
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
List<Integer> squares = numbers.stream()
                               .map(n -> n * n)
                               .collect(Collectors.toList());
System.out.println(squares); // Prints [1, 4, 9, 16, 25]
```

- Reduce metoden bruges til at kombinere elementerne i en strøm ved hjælp af en binær operation for at producere en enkelt outputværdi.

```
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
int sum = numbers.stream()
                 .reduce(0, Integer::sum);
System.out.println(sum); // Prints 15
```

- Filter metoden bruges til at vælge elementer fra en strøm, der opfylder en bestemt betingelse.

```
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
List<Integer> oddNumbers = numbers.stream()
                                  .filter(n -> n % 2 != 0)
                                  .collect(Collectors.toList());
System.out.println(oddNumbers); // Prints [1, 3, 5]
```

- Collect metoden bruges til at transformere outputtet af en strøm til en anden datastruktur.

```
Stream<Integer> stream = Stream.of(1, 2, 3, 4, 5);
List<Integer> numbers = stream.collect(Collectors.toList());
System.out.println(numbers); // Prints [1, 2, 3, 4, 5]
```

## Avancerede Koncepter
### Partial Application og Currying
Partial application er en teknik, hvor en funktion, der tager flere argumenter, er transformeret til en sekvens af funktioner, hver tager et enkelt argument. Med andre ord, i stedet for at give alle argumenter på én gang, tillader currying dig at anvende funktionen delvist, ét argument ad gangen, hvilket producerer en ny funktion med hver ansøgning, indtil alle argumenter er givet, og det endelige resultat er opnået medium.com.

### Rekursion
Rekursion er en teknik, hvor en funktion kalder sig selv. I funktionel programmering kan rekursion bruges til at implementere løkker. Her er et eksempel på en rekursiv funktion i Java, der beregner det faktorielle af et tal deepu.tech:

```
public class FactorialSample {
    static long factorialTailRec(long num) {
        return factorial(1, num);
    }
    static long factorial(long accumulator, long val) {
        return val == 1 ? accumulator : factorial(accumulator * val, val - 1);
    }
    public static void main(String[] args) {
        System.out.println(factorialTailRec(20)); // 2432902008176640000
    }
}
```
