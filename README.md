# TestingGlossary (Polish)

Nie za krótkie wprowadzenie do technicznych testów

1. Java jako idealny przykład języka obiektowego

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| Trzy zasady programowania obiektowego | Hermetyzacja (Enkapsulacja) - Ograniczenie dostępu do wnętrza programu przez koncepcję klasy, ze względów bezpieczeństwa lub czysto praktycznych <br/> Dziedziczenie - Proces w którym jeden obiekt otrzymuje właściwości innego obiektu <br/> Polimorfizm -To cecha, dzięki której jeden interfejs może być stosowany do wykonania różnych zadań |
| Przygotowanie danych testowych. Zaprojektowanie testów weryfikujących jakość i ilość przeprocesowanych danych | Baza Danych - Test |
| Typy danych | Proste/podstawowe <br/> Całkowite <br/> Zmiennoprzecinkowe <br/> Znakowe <br/> Logiczne |
| Instrukcje sterujące | Instrukcje wyboru <br/> Konstrukcja switch  |
| Instrukcje iteracji | Pętla while <br/> Pętla do-while <br/> Pętla for <br/> Pętla for-each |
| Instrukcje skoku | Instrukcja break <br/> Instrukcja continue <br/> Instrukcja return |
| Klasa | To konstrukcja logiczna, zbiór metod zmiennych itp. które definiują obiekt. Ważne klasa definiuje nowy typ danych |
| Obiekt | To zastosowanie klasy, wystąpienie klasy w praktyce |
| new | Operator, który alokuje pamięć do działania obiektu i zwraca referencję do niego |
| Konstruktor | Metoda o tej samej nazwie co klasa. inicjalizuje obiekt zaraz po jego utworzeniu. Czyli inicjalizuje wszystkie metody i zmienne w klasie |
| this | Operator stosuje się w: <br/> Chaining - chcemy wywołać ze zmiennej obiektowej metody, które mają typ obiektu <br/> Parametryzacja - odróżnienie zmiennej lokalnej od parametru o tej samej nazwie |
| Metoda przeciążona | Metoda o tej samej nazwie co istniejąca ale o innej liczbie i typie parametrów. Może zwracać też inny typ wartości. Plus jest taki, że możemy wykorzystywać wielokrotnie tę samą nazwę metody |
| Metoda rekurencyjna | Metoda wywołująca samą siebie |
| static | Zmienna statyczna - to zmienna globalna współdzielona przez wszystkie obiekty klasy <br/> Metoda statyczna - może wywoływać jedynie inne metody statyczne, ma dostęp jedynie do danych statycznych i nie można korzystać z this i super |
| final | Zmienne - uniemożliwia modyfikację zmiennej <br/> Metody - uniemożliwia przesłanianiu i dziedziczeniu |
| super (uwaga w C# nie istnieje) | Można wywołać konstruktor klasy bazowej <br/> Można wywołać, uzyskać dostęp do np. metoda klasy nadrzędnej, które zostały przesłonięte przez klasę pochodną |
| Metoda przesłonięta | To taka metoda, która ma taką samą nazwę co metoda klasy bazowej. Zostanie ona wykonana. A ta z klasy bazowej ukryta |
| Klasa abstrakcyjna | Klasa, która stanowi w pewnym sensie jedynie strukturę dla klas podrzędnych. Dopiero klasy dziedziczące implementują np. metody. specjalna klasa zawierająca metody abstrakcyjne i nieabstrakcyjne. Z takiej klasy nie można utworzyć obiektu w tradycyjny sposób, ale można dziedziczyć. |
| Pakiet | Przestrzeń nazw i sterowanie dostępem. Innymi słowy w pakiecie może istnieć tylko jedna klasa o danej nazwie |
| Interfejs | To coś jak klasa abstrakcyjna ale ma jedną dużą zaletę, klasa może implementować dowolną liczbę interfejsów. interfejsy zawierają jedynie deklaracje metod ale klasa może dziedziczyć wiele interfejsów używając słówka implements |
| Modyfikatory dostępu | private - mamy dostęp jedynie w klasie, w której obiekt został zdefiniowany <br/> brak modyfikatora - mamy dostęp w klasie, w której został obiekt zdefiniowany, w podklasach i innych klasach ale dla danego pakietu <br/> protected - to samo co w przypadku braku modyfikatora + podklasy z innego pakietu <br/> public - dostępny w klasach i podklasach we wszystkich pakietach |
| Typy wyjątków | |
| Klauzula try catch | |
| Garbage Collection | Jak już wiemy np. każdemu nowemu obiektowi przydzielana jest pamięć. W javie pamięcią i jej zwalnianiem nie zajmuje się programista, ale specjalna funkcja/metoda zwana garbage collector |
| Kolekcje w Javie | Mapa - lista wartości z kluczem <br/> Lista - lista wartości z duplikatami <br/> Set - lista wartości bez duplikatów, nieposortowane, można je odnaleźć po indeksie |
| Setter i Getter | Settery i Gttery to specjalne metody pozwalające na dostanie się do prywatnych zmiennych z poza klasy, w której ta zmienna została zdefiniowana|
| Lombok Data Model | klasa z adnotacją @Data. Adnotacja mówi np. Mavenowi, że w trakcie budowania aplikacji ma dodać brakujacy kod i go uruchomić. Ma dodać definicje seterów geterów i inne  |
| Jackson Object Mapper | służy do parsowania json'a z pliku, stringa do obiektu javowego. Używamy tutaj geterów i seterów z osobnej klasy, lub datamodel class np. używając lomboka z wbudowanymi getterami i setterami. Co zawiera metoda readValue: parametr1 - wartości dla setterów, np. z pliku yaml / parametr2 - datamodel class |
| Jackson | biblioteka do procesowania jsona |
| Hashcode i Equals | metody służące do porówania obiektów: Hashcode zwraca integera obiektu |
| @NoArgsConstructor | generuje konstruktor bez argumentów |
| SOLID | wzorzec projektowy, programowania obiektowego: <br/> Klasa powinna mieć tylko jedną odpowiedzialność np. za "kontakt" z bazą danych <br/> Wiele interfejsów zamiast jednego ogólnego <br/> Klasy powinny być otwarte na rozszerzenia a nie na modyfikacje |

2. Technologie i frameworki developerskie

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| gulp | Build Manager (js) |
| NuGet | Package Manager (C#) |
| Proxy | Serwer pośredniczący w przekazywaniu danych w sieci komputerowej z wykorzystaniem jakiegoś protokołu np. HTTP |
| curl | Programik do transferowania danych różnymi protokołami np. HTTP |
| SSIS | Paczka ETL-owa w SQL Server pozwalająca na wyciąganie danych, konwertowanie, procesowanie i załadowanie do bazy |
| Tomcat | Serwer aplikacyjny |
| Hibernate | Framework pod Javę do mapowania obiektów relacyjnej bazy danych |
| Spring | Framework javowy |
| NoSQL | Nierelacyjna baza danych. Np. MongoDB |
| Ajax | Technologia wspierająca dynamiczne zmiany elementów na stronie bez konieczności  przeładowywania strony. Na technikę składa się xml, javascript, XMLHttpRequest |
| Flask | Framework pythonowy |
| Angularjs | Js framework. Najważniejszymi składowymi aplikacji angularowej są: <br/> Routing - zarządza przekierowaniami <br/> Controller - pośrednik między kodem HTML a serwisem <br/> Directive - zestaw funkcji do wykonania. ng-repeat, ng-show lub customowe <br/> Service - serwis służy do komunikacji z backendem <br/> Scope - odwzorowanie HTML'a na js? |
| JDBC | API pod Javę określające sposób komunikacji Backend-DB. Inne np. ODBC dla C# |
| XMLHttpRequest | Asynchroniczne przesyłanie danych dzięki czemu w trakcie pobierania danych użytkownik może wykonywać inne czynności |
| node.js | Środowisko uruchomieniowe dla JS |
| JQuery | Biblioteka JS-owa |
| Ant | Build Manager (java) |
