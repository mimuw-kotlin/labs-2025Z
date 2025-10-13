# Laboratorium 2
## Dlaczego Kotlin?
W skrócie - bo nie jest Javą.

W dłuższym skrócie - JetBrains używało wyłącznie Javy, ale z racji, że jest firmą, która zajmuje się głównie DevX (którego Java nie spełniała), postanowiło stworzyć swój język, w którym pracuje się przyjemnie (ale który może być stosowany zamiennie z Javą, dla umożliwienia okresu przejściowego). Język przyjął się na tyle, że w 2019 roku Google (również z powodu [problemów prawnych](https://en.wikipedia.org/wiki/Google_LLC_v._Oracle_America,_Inc.#:~:text=verdict%20was%20proper.-,Decision,the%20case%20for%20further%20hearing.) wynikających z używania Javy) ogłosiło go preferowanym językiem do programowania aplikacji na Androida.

Techniczne porównanie z Javą:
https://kotlinlang.org/docs/comparison-to-java.html

Laurka dla Kotlina:
https://machine-learning-made-simple.medium.com/why-kotlin-is-eating-java-df5afde4c553

## 5 kluczowych OOP różnic w stosunku do Javy
### 1. Properties
Ujednolicone `field`, `getter` i `setter`.

```kotlin
var name: String = "Kotlin"
```

```java
private String name = "Java";
public String getName() { return name; }
public void setName(String name) { this.name = name; }
```
### 2. Extension functions
Kotlin pozwala rozszerzać istniejące klasy o nowe funkcje bez dziedziczenia czy modyfikowania kodu źródłowego. W Javie nie ma takiej możliwości.
### 3. Data classes
Poniekąd nieaktualne, bo w Javie 14 jest już odpowiednik (rekord).
### 4. Singletons/objects

```Kotlin
object AppConfig
```

```java
public class AppConfig {
    private static final AppConfig INSTANCE = new AppConfig();
    private AppConfig() {}
    public static AppConfig getInstance() { return INSTANCE; }
}
```
### 5. Companion objects
W Kotlinie nie używa się słowa kluczowego `static`. Zamiast tego wszystkie pola i metody, które należą do klasy, a nie do jej instancji, są zgrupowane w zagnieżdżonym `companion object`.

## Ćwiczenia na dzisiaj
Wszystkie rozdziały (poza `Collections` i podrozdziałem `Lambda expressions` w rozdziale `Functions`) ze strony:
https://kotlinlang.org/docs/kotlin-tour-hello-world.html
