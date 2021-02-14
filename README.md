# TestingGlossary (Polish)

Nie za krótkie wprowadzenie do technicznych testów

1. Java jako idealny przykład języka obiektowego

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| Trzy zasady programowania obiektowego | Hermetyzacja - Ograniczenie dostępu do wnętrza programu przez koncepcję klasy, ze względów bezpieczeństwa lub czysto praktycznych <br/> Dziedziczenie - Proces w którym jeden obiekt otrzymuje właściwości innego obiektu <br/> Polimorfizm -To cecha, dzięki której jeden interfejs może być stosowany do wykonania różnych zadań |
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
| Klasa abstrakcyjna | Klasa, która stanowi w pewnym sensie jedynie strukturę dla klas podrzędnych. Dopiero klasy dziedziczące implementują np. metody |
| Pakiet | Przestrzeń nazw i sterowanie dostępem. Innymi słowy w pakiecie może istnieć tylko jedna klasa o danej nazwie |
| Interfejs | To coś jak klasa abstrakcyjna ale ma jedną dużą zaletę, klasa może implementować dowolną liczbę interfejsów |
| Modyfikatory dostępu | private - mamy dostęp jedynie w klasie, w której obiekt został zdefiniowany <br/> brak modyfikatora - mamy dostęp w klasie, w której został obiekt zdefiniowany, w podklasach i innych klasach ale dla danego pakietu <br/> protected - to samo co w przypadku braku modyfikatora + podklasy z innego pakietu <br/> public - dostępny w klasach i podklasach we wszystkich pakietach |
| Typy wyjątków | |
| Klauzula try catch | |
| Garbage Collection | Jak już wiemy np. każdemu nowemu obiektowi przydzielana jest pamięć. W javie pamięcią i jej zwalnianiem nie zajmuje się programista, ale specjalna funkcja/metoda zwana garbage collector |
| Kolekcje w Javie | Lista <br/> Zbiór <br/> Mapa|


2. REST - podstawy architektury

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| Czym jest REST? | To zestaw metod i dobrych praktyk definiujących sposób komunikacji między systemami. Może to być np. komunikacja Klient - Serwer. Komunikacja odbywa się przez protokół HTTP |
| Czym jest API? | To samo co powyżej ale ogólnie. Zestaw protokołów, rutyn, narzędzi |
| Serwer | Utożsamiany z backendem program, który świadczy usługi dla innych programów. Komunikuje się z bazą i klientem |
| Klient | Program komputerowy występujący w roli klienta usług dostarczanych przez serwer |
| Po co REST API? | Ustandaryzowanie zasad tak by każdy ze swoją technologią mógł się komunikować z "obcą" technologią potencjalnie niekompatybilną |
| Metody HTTP | GET - request danych ze źródła <br/> POST - update danych w źródle <br/> PUT - zapisanie danych w źródle <br/> DELETE - usunięcie danych  <br/> OPTIONS <br/> HEAD |
| Najważniejsze Statusy Odpowiedzi | 200 - OK <br/> 201 - Created <br/> 500 - Internal Server Error <br/> 400 - Bad request <br/> 401 - Unauthorized <br/> 404 - Not found |
| Co testować? | Backend validation - walidacja pól <br/> Uwierzytelnianie - czy endpointy są zabezpieczone przed nieporządanym dostępem |
| CORS requests | Mechanizm umożliwiający współdzielenie zasobów pomiędzy serwerem i klientem znajdującymi się w różnych domenach, czyli wykonywania żądań AJAXowych przy zachowaniu pewnych ograniczeń co do dopuszczalnego źródła danych |
| Headers | Nagłówki to pewnego rodzaju polecenia służące do komunikacji między serwerem a klientem np. Access-Control-Allow-Headers, Access-Control-Allow-Origin, Access-Control-Allow-Methods |


3. Technologie i frameworki developerskie

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| Maven | Build Manager (java) |
| Gradle | Build Manager (java) |
| npm | Package Manager (js) |
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
| Angularjs | Js framework. Najważniejszymi składowymi aplikacji angularowej są: <br/>
Routing         - zarządza przekierowaniami <br/>
Controller      - pośrednik między kodem HTML a serwisem <br/>
Directive       - zestaw funkcji do wykonania. ng-repeat, ng-show lub customowe <br/>
Service         - serwis służy do komunikacji z backendem <br/>
Scope           - odwzorowanie HTML'a na js? |
| JDBC | API pod Javę określające sposób komunikacji Backend-DB. Inne np. ODBC dla C# |
| XMLHttpRequest | Asynchroniczne przesyłanie danych dzięki czemu w trakcie pobierania danych użytkownik może wykonywać inne czynności |
| node.js | Środowisko uruchomieniowe dla JS |
| JRE | Środowisko uruchomieniowe dla Javy |
| JDK | Środowisko do programowania w Javie. Zawiera kompilatory Javy, wirtualne maszyny itd |
| JQuery | Biblioteka JS-owa |
| Ant | Build Manager (java) |


4. Continuous Integration - kroki i proces

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| Po co? | Szybka możliwość weryfikacja i przetestowanie zmian wrzucanych na środowisko połączona z integracją z innymi systemami oraz możliwość zaprezentowania na demo |
| Konfiguracja | Określenie nazwy builda i build countera <br/>
Zintegrowanie joba ze zdalnym repozytorium <br/>
Określenie build stepów i gdzie powinny się odpalać <br/> 
Określenie triggerów <br/>
Określenie w jakich warunkach job powinien failować i jeszcze dodatkowe parametry jak odpalanie dodatkowych skryptów po buildzie. |
| Night build | Zazwyczaj pełna lista testów jest odpalana. Job zaskedżulowany |
| Daily build | Przetestowanie korowych funkcjonalności po każdym komicie |
| Narzędzia CI | Jenkins, TeamCity, CruiseControl, Bamboo, Firebase, Bitrise |


5. GIT komendy i VCS

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| Narzędzia VCS | GIT, Perforce, SVN |
| Klienci VCS i wtyczki | Stash, Bitbucket, GitLab, Tortoise |
| git config | Konfiguracja np. Credentiali, wielkości danych puszowanych |
| git init | Inicjalizuje lokalne repozytorium |
| git clone | Klonuje zawartość zdalnego repozytorium do lokalnego |
| git add | Umożliwia dodanie plików do zakomitowania |
| git commit | Komituje pliki do spuszowania |
| git push origin master | Wysyła pliki na zdalne repo z master brancha lokalnego na zdalnego |
| git status | Pokazuje, na którym branchu jesteśmy |
| git remote add origin | Powiązanie ze zdalnym repozytorium |
| git checkout <branchname>  | Tworzy nowego brancha lub przeskakuje na istniejącego |
| git branch | Tworzy nowego brancha |
| git branch -d <branchname> | Usuwa istniejącego brancha |
| git pull | Zaciąga dane ze zdalnego repozytorium |
| git merge <branchname> | Łączy dane ze zdalnego brancha z danymi na lokalnym branchu |
| git diff | Pokazuje różnice między commitami |
| git tag 1.0.0 <commitID> | Oznaczenie komita |
| git log | Pokazuje historię commitów |
| git fetch  | git fetch = git pull + git merge |
| git reset --hard <branchname> | Przeskakuje do ostatniego zakomitowanego brancha |
| git grep "string" | Szukamy określonego wzorca w lokalnym repo |
| git stash | Wyrzuca dane do schowka |
| git stash pop | Przywraca dane ze schowka |
| git pull --rebase | Jak nie chcemy merdżować kodu? |  
| git fork | Tworzy kopię istniejącego projektu |    


6. Teoria testowa

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| Test Strategy | Typowy dokument powinien zawierać: Scope and Objectives, Roles and Responsibilities, Test deliverables, Testing metrics - stworzony przez Project Managera. High Level document |
| Test Plan | Typowy dokument powinien zawierać: Test Scope, Type of tests, Entry Criteria, Exit Criteria, Bugs definitions, Environments, Testing approach (manual, automated) - Lower level document |
| Traceability Matrix | Pokrycie wymagań testami|
| Test Scenario | Jest pojęciem szerszym niż przypadek testowy. Może zawierać wiele przypadków testowych. To po prostu procedura testowa na jakąś funkcjonalność |
| Test Case | Zbiór kroków do odtworzenia, oczekiwanych rezultatów, a także krótkiego opisu testu |
| Podejście Testowe | CRUD |
| Wyrocznia Testowa | Źródło dostarczające oczekiwanych rezultatów umożliwiające porównanie ich z otrzymanymi rezultatami. Wyrocznią może być istniejący system podręcznik użytkownika, wiedza testera, ale nie może być nią kod |
| Testing Metrics | Pokrycie wymagań, liczba defektów znalezionych (critical, blockers, major) i naprawionych, czas potrzebny na naprawę defektu |
| SDLC | Analiza, planowanie, Zbieranie wymagań, Development i Testing,  Utrzymanie, Czynności zamykające projekt |
| Waterfall | Każdy krok rozwoju aplikacji następuje po sobie. Wady dłużej trwa projekt, ciężko o wprowadzanie zmian. Zalety: bardziej uporządkowany, istnieje dokumentacja |
| Cykl życia defektu | Report, assign, fix, resolve, test, approve or reject and assign, close |
| Raportowanie defektu | Title, environment, sometimes sprint number, steps to reproduce, expected result ,actual result, screenshot |
| Techniki testowe | Klasy równoważności - zbiór danych, których wykorzystanie powoduje takie samo działanie systemu <br/>
Wartości graniczne - specjalny przypadek klas równoważności, badamy wartości na granicy danych zbiorów i tuż poza <br/>
Przejścia pomiędzy stanami - przypadki testowe projektowane tak by sprawdzały dozwolone i niedozwolone przejścia między stanami <br/>
Tablica decyzyjna |
| Smoke Testy | Testy korowych funkcjonalności |
| Testy Regresyjne | Przeprowadzane po smoke testach, weryfikują czy system się nie popsuł po dokonaniu zmian, wprowadzeniu nowych funkcjonalności, poprawieniu błędów |
| Co automatyzować | Korowe funkcjonalności (wykorzystywane w wielu miejscach) <br/>
Testy odpalane wielokrotnie (regresyjne, smoke testy) <br/>
Testy z dużą ilością danych testowych <br/>
Testy odpalane na wielu przeglądarkach <br/>
Funkcjonalności, które mają tendencję do psucia się |
| White box testing | Unit testing, zaglądamy co tam w bebechach piszczy. Weryfikujemy działanie metod, klas, procedur, tabel itd |
| Black box testing | Bez zaglądania w kod. Testujemy w oparciu o techniki testowe |
| Ad Hoc testing | Bez przygotowania, bazujemy jedynie na własnym doświadczeniu |
| Exploratory testing  | Bazujemy na własnym doświadczeniu. Przygotowujemy się do tego. Może być odrobina dokumentacji |
| Sesja eksploracyjna | Session based testing (2-3 sessions) each session 30-45 minutes. <br/>
The session metrics are the primary means to express the status of the exploratory test process. They contain the following elements:<br/>
Number of sessions completed <br/>
Number of problems found <br/>
Function areas covered <br/>
Percentage of session time spent setting up for testing <br/>
Percentage of session time spent testing <br/>
Percentage of session time spent investigating problems |
| TDD | Koncepcja developmentu, w którym wpierw piszemy test pod funkcjonalność, piszemy funkcjonalność, jeśli failuje to poprawiamy funkcjonalność i raz jeszcze odpalamy test |
| BDD | Rozwinięcie koncepcji TDD o dodatkową warstwę przedstawiającą testy w języku naturalnym, zrozumiałym dla biznesu |
| Testing | Sprawdzenie czy wymagania zostały zaimplementowane poprawnie |
| QA | Szersze pojęcie niż testing. Testing jest składową QA, ale QA dba również o odczucia klienta np. estetyka, innowacyjność a także czy jakieś standardy zostały zachowane |
| Waga | Jak ważny bug jest dla biznesu |
| Priorytet | Jak szybko buga rozwiązać |
| Poziomy testowania | Modułowe(jednostkowe) <br/>
Integracyjne <br/>
Systemowe <br/>
Akceptacyjne |
| Analiza Statyczna | Testowanie  modułu lub systemu na etapie pisania specyfikacji i projektowania bez uruchamiania kodu |
| Analiza dynamiczna | Tu uruchamiamy kod i przeglądamy ręcznie kod |
| Model Wodospadowy | W tym modelu każda faza rozwoju oprogramowania następuje po sobie: Zbieranie Wymagań -> Projektowanie -> Development -> Testing -> Utrzymanie|
| Model V | Rozwinięcie modelu wodospadowego, gdzie każdy etap projektowania ma swój odpowiednik po stronie weryfikacji. I tak wymagania są sprawdzane przez testy akceptacyjne architektura komponentów sprawdzana przez testy komponentów, architektura systemu sprawdzana przez testy systemowe itd. Na dole jest implementacja |
| Testy niefunkcjonalne | performance, security, usability, portability, accessibility |
| Testy obciążeniowe | Ile requestów jest w stanie obsłużyć system w określonym czasie |
| Testy przeciążeniowe | Sprawdzamy kiedy system padnie i czy padnie w oczekiwany sposób |
| Testy wydajnościowe | Ile czasu trwa wykonanie jakiejś czynności, jakiegoś requesta |
| Sesja usability | Testy z użytkownikami. Badamy jak długo czasu spędzał na stronie, jakie są odczucia odnośnie aplikacji, czas potrzebny na wykonanie jakiegoś zadania |
| Testy bezpieczeństwa | Np. sql injection, cross site scripting |
| Piramida testów | W pewnym sensie usystematyzowanie ilościowe testów. Piramida zakłada, że najwięcej odpalamy unit testów, dalej testów funkcjonalnych i akceptacyjnych. Najmniej E2E |
| UML | Modelowanie obiektowe. Przykładowe diagramy: <br/>
Activity <br/>
Use cases <br/>
Classes |
| WSDL | (Web Services Description Language) - informacje odnośnie web-serwisu- akceptowane typy danych, port działania, operacje, informacje o end-pointach |
| PairWise Testing | Czarnoskrzynkowa technika projektowania przypadków testowych, której celem jest redukcja ilości przypadków testowych w celu szybszego ukończenia testowania. Dobre zastosowanie tej techniki nie powinno obniżać pokrycia |
| Jarzmo testowe | Środowisko testowe, składające się z zaślepek i sterowników potrzebnych do wykonania testu |
| Hot-Fix | Poprawka wprowadzona do aplikacji będącej już na produkcji bez nowego releasu całej aplikacji. Poprawka jest wpierw testowana na środowisku akceptacyjnym będącym kopią produkcji |
| Change Request | Prośba ze strony biznesu o wprowadzenie zmian do funkcjonalności aplikacji będącej na produkcji |
| Środowiska | Rozwinięcie koncepcji TDD o dodatkową warstwę przedstawiającą testy w języku naturalnym, zrozumiałym dla biznesu |
| BDD | DEV - zazwyczaj lokalnie u developera ale też często współdzielone przez innych developerów. <br/>
TEST - dedykowane testerom do testów automatycznych i manualnych <br/>
UAT - środowisko przeznaczone dla klienta do testów akceptacyjnych <br/>
PROD - nie muszę chyba pisać co to oznacza  |


7. Trochę o automatyzacji i technicznych spraw ciąg dalszy

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| ssh | Protokół komunikacyjny, który umożliwia uwierzytelnianie użytkownika w trakcie komunikacji |
| json array | array of objects - [{},{}] |
| json object | Np. { name: "name", lastName: "lastName"} |
| Assert | Kiedy step się wywali egzekucja testu się zatrzymuje |
| Verify | Kiedy step się wywali egzekucja testu jest kontynuowana |
| Implicit Wait | Taki globalny wait dla wszystkich elementów. Czekaj aż wyskoczy wyjątek, że nie można znaleźć elementu |
| Explicit Wait | Taki lokalny dla konkretnego elementu wait |
| Fluent Wait | Przeznaczony dla elementów, których czas pojawienia się jest bardzo zmienny |
| Page Object Pattern | Odwzorowanie np. strony webowej pod postacią klasy z metodami odpowiadającymi danej funkcjonalności. Z Takiego obiektu, czyli wystąpienia klasy wywołujemy metody |
| Page Object Model | Rozwinięcie albo dodatek do Page object pattern. Stworzona po to by nie powielać kodu i składować i inicjalizować web elementy w jednym miejscu. Najprościej jest utworzyć klasę z web elementami i zainicjalizować je (wyszukać). W ten sposób nie musimy w przypadku zmiany lokatora w wielu miejscach go zmieniać. Oszczędzamy czas i miejsce |
| Page Factory | Możemy sobie sami stworzyć taki model, ale po co jak Selenium WebDriver ma to już stworzone i zoptymalizowane. Nazywa się to Page Factory |
| BDD w praktyce | BDD binding in C# and Java - [Binding] and @Binding. <br/>
Przykłady frameworków: <br/>
Specflow - BDD dla C# używa atrybutów [] <br/>
JBhave - BDD dla Javy używa annotacji <br/>
Cucumber -  BDD dla Javy używa annotacji i co ważne sklejanie stepów z featurami używacie poprzez słówko kluczowe “glue” w klasie z runner’em testów. <br/>
Jasmine - BDD dla JS |
| TestNG | Framework javowy do unit testów i funkcjonalnych. Najczęściej stosowany w połączeniu z selenium.
Annotacje TestNG: @Test, @BeforeClass, @AfterClass, @BeforeSuite, @AfterSuite, @BeforeMethod, @AfterMethod |
| Locators | Można generalnie podzielić na dwie grupy: związane z DOM (xpath, id, name) i CSS |
| Aplikacje Mobilne | Native - instalowane na mobilkach z takich źródeł jak GooglePlay. Są dedykowane konkretnym urządzeniom. Mogą używać funkcjonalności telefonu np. Kamery <br/>
Hybrid - Są dostępne np. z GooglePlay ale odpalane przeglądarkowo <br/>
Web - apki odpalane przez przeglądarkę, zazwyczaj napisane w HTML5 |
| Testowanie mobilek | Narzędzia do testowania automatycznego urządzeń mobilnych: appium, robotium, espresso. W przypadku webowych można używać emulatorów selenium webdriver na aplikacje mobilne |
| Event Listenery | Zestaw metod, które umożliwiają logowanie akcji ale jedynie tych związanych z webdriverem |
| Regexp | Ciąg znaków określający szukany wzorzec. Np. .* szukamy plików dowolnego formatu |
| Programowanie niskopoziomowe | Programowanie niskiego poziomu to język zrozumiały dla peceta [język maszynowy (kod binarny)] np. assambler |
| Programowanie wysokopoziomowe | Programowanie wysokiego poziomu to programowanie zrozumiałe dla ludzi np. java. |
| Cache | Pamięć podręczna. Jest wykorzystywana do szybszego dostępu do danych.
Np. Pamięć podręczna przeglądarki powoduje, że elementy już kiedyś załadowane ponownie nie muszą być ładowane po prostu są pobierane z pamięci podręcznej |
| Protractor | Framework jsowy dedykowany dla angularJS, służący do testów funkcjonalnych. Działa na selenium webdriverze |
| Środowisko uruchomieniowe | W językach wysokopoziomowych potrzebny jest specjalny interpreter, który przetłumaczy kod na postać binarną zrozumiałą dla maszyny. Przykładami są node.js i jre. |
| Package Manager | Ciąg znaków określający szukany wzorzec. Np. .* szukamy plików dowolnego formatu |
| Regexp | System do automatycznej instalacji, konfiguracji, aktualizacji i usuwania pakietów oprogramowania |


8. SQL
8.1 Union
Łączenie tabel o tej samej liczbie kolumn i typie. Usuwa duplikaty. 
8.2 Union ALL
Łączenie tabel o tej samej liczbie kolumn i typie. Nie usuwa duplikatów.
8.3 Joins
left join - pokazuje część wspólną dwóch tabel oraz pozostałe rekordy w "lewej" tabeli.

right join - pokazuje część wspólną dwóch tabel oraz pozostałe rekordy w "prawej" tabeli.

inner join - pokazuje część wspólną tabel.

outer join - pokazuje część wspólną i nie wspólną tabel.

cross join - łączy każdy element z tabeli 1 z każdym elementem z tabeli 2.
8.4 Agregacje w SQL
AVG, SUM, MAX, MIN
8.5 EXCEPT
(SQL Server) odejmuje dwie tabele o takiej samej ilości kolumn i tych samych typach danych.
8.6 MINUS
(Oracle) odejmuje dwie tabele o takiej samej ilości kolumn i tych samych typach danych.
8.7 Count
Count(*) - zlicza ilość rekordów po wszystkich kolumnach
Count(1) - zlicza ilość rekordów po pierwszej kolumnie
8.8 Hurtownia danych
Baza skonstruowana z innych baz relacyjnych celem szybszego dostępu do danych. 
Podstawowymi elementami są: Staging area, Atomisation, Dimensions i Tabele faktów.
8.9 Dynamiczny SQL
Czyli jak przechowywać zapytania w zmiennej, odpalać je z dowolnego miejsca kodu i przechowywać zwróconą wartość w innej zmiennej. Ma słabą wydajność.
Oracle - Execute Immediate
SQL Server - exec sp_executesql
8.10 SQL hints
W SQL Server możemy dopomóc przy egzekucji zapytania pewnymi hintami celem przyspieszenia działania zapytania.
join hints - merge, loop, hash
table hints - NO LOCK
8.11 Pivot
Obracanie tabeli.
8.12 Tabela CTE
Common table expression - służąca chociażby do insertowania w jednym zapytaniu dużej ilości rekordów.  
8.13 Klucze
Primary key
Foreign key
8.14 Constraints
Określają ograniczenia kolumn: not null, unique, primary key, foreign key, index.
8.15 Grupowanie
Grupowanie należy wykonywać po niezagregowanych kolumnach.
8.16 Transakcje
Insert, update, delete. 
8.17 Indeksy 
Klastrone
Nieklastrowe
8.18 Konwertowanie danych
Convert - więcej możemy zrobić z datą niż w przypadku cast
Cast - jest standardem ANSI
8.19 Trimming
ltrim - wycina spację z lewej strony
rtrim - wycina spację z prawej strony
8.20 Truncate
Chyba nie zwraca uwagi na klucze. Usuwa jak leci.
8.21 Delete
Tutaj niestety errory wyskoczą, jak są indeksy i klucze pozakładane.

9. Komendy bash
9.1 cat [filename]
Pokazuje zawartość pliku.
9.2 cd /directorypath 
Przechodzimy pomiędzy katalogami.
9.3 chmod [options] mode filename
Zmienia uprawnienia do pliku.
9.4 chown [options] filename
Zmienia właściciela pliku.
9.5 clear
Czyści konsolę.
9.6 cp [options] source destination
Kopiuje plik do katalogu.
9.7 date [options] 
Pokazuje lub ustawia datę systemową.
9.8 df [options] 
Pokazuje jak zajęty jest dysk twardy.
9.9 du [options] 
Pokazuje ile ważą pliki.
9.10 file [options] filename
Określa jaki typ danych jest wewnątrz pliku.
9.11 find [pathname] [expression]
Znajdź pliki dla danego wzorca.
9.12 grep [options] pattern [filesname]
Pokaż pliki dla danego wzorca.
9.13 kill [options] pid 
Zatrzymuje proces. kill -9 bezwarunkowo.
9.14 less [options] [filename] 
Pokazuje zawartość zawartość pliku strona po stronie.
9.15 ln [options] source [destination] 
Miękkie dowiązanie.
9.16 ls [options] 
Wylistuj zawartość katalogu.
9.17 man [command] 
Pomoc.
9.18 mkdir [options] directory 
Stwórz nowy katalog.
9.19 mv [options] source destination
Zmień nazwę pliku lub wytnij i wklej go do innej lokalizacji.
9.20 passwd [name [password]] 
Zmiana hasła.
9.21 ps [options] 
Pokazuje działające procesy.
9.22 pwd 
Ścieżka do katalogu, z którego wykonano komendę.
9.23 rm [options] directory 
Usuwa pliki lub katalogi.
9.24 rmdir [options] directory 
Usuwa katalogi.
9.25 ssh [options] user@machine
Zdalne łączenie się z inną linuxową maszyną.
9.26 su [options] [user [arguments]]
Przechodzenie pomiędzy użytkownikami.
9.27 tail [options] [filename] 
Pokazuje ostatnich 10 linijek pliku.
9.28 tar [options] filename 
Pakowanie i rozpakowanie pliku.
9.29 touch filename 
Tworzy pusty plik.
9.30 who [options]
Pokazuje kto jest zalogowany.

10. Agile
10.1 Zalety agile
Łatwiejsza reakcja na zmiany, szybciej trwa projekt.
10.2 Wady agile
Większy chaos, dużo bugów, zero dokumentacji.
10.3 Kanban

10.4 Ceremonie Scrumowe
Planning
Daily Stand-up
Review i Retrospective
Backlog grooming
Scrum of Scrums
Poker planning
10.5 Produkty Scrumowe
Product backlog - lista high-levelowych wymagań.
Sprint backlog - lista tasków brana na sprint.
Burndown-chart - pokazuje progres pracy. Zależność czasu wyestymowanych tasków od czasu w sprincie.
User Story - historyjka brana na sprinta. Zazwyczaj funkcjonalność.
10.6 Zespół w Scrumie
Developer (Dev Team) - wiadomo co robi
Product Owner - zarządza backlogiem, reprezentuje interesy klienta
Scrum Master - zarządza procesem i ceremoniami scrumowymi
10.7 SAFe
Scaled Agile Framework- Podejście agilowe dla dużych projektów w którym istnieje wiele zespołów scrumowych współpracujących ze sobą.

11. Pytania otwarte
11.1 
Developerzy nie wyrobią się z taskiem w sprincie. Co robię i jak komunikuję to klientowi?

11.2
Project Manager chce by testować funkcjonalność na produkcji. Jak reaguję na taką prośbę?

11.3
Jak motywuję podwładnych do wykonywania zadań?

11.4
Jak weryfikuję progres pracy podwładnych?

11.5
Jak zarządzam rozproszonym zespołem?

11.6
Co robię w momencie kiedy źle oszacowałem ilość pracy potrzebnej na zakończenie zadań w sprincie dla zespołu testerów.

11.7
Czy byłem kiedyś pochwalony i/lub zganiony za swoją pracę?

11.8
Jak organizuję sobie pracę w projekcie, który dopiero startuje?
