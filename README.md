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
| Angularjs | Js framework. Najważniejszymi składowymi aplikacji angularowej są: <br/> Routing - zarządza przekierowaniami <br/> Controller - pośrednik między kodem HTML a serwisem <br/> Directive - zestaw funkcji do wykonania. ng-repeat, ng-show lub customowe <br/> Service - serwis służy do komunikacji z backendem <br/> Scope - odwzorowanie HTML'a na js? |
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
| Konfiguracja | Określenie nazwy builda i build countera <br/> Zintegrowanie joba ze zdalnym repozytorium <br/> Określenie build stepów i gdzie powinny się odpalać <br/> Określenie triggerów <br/> Określenie w jakich warunkach job powinien failować i jeszcze dodatkowe parametry jak odpalanie dodatkowych skryptów po buildzie. |
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
| git cherrypick | Jeżeli chcemy przerzucić commita z jednego brancha na drugiego, tak żeby nie merdżować jednego brancha do drugiego|   


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
| Techniki testowe | Klasy równoważności - zbiór danych, których wykorzystanie powoduje takie samo działanie systemu <br/> Wartości graniczne - specjalny przypadek klas równoważności, badamy wartości na granicy danych zbiorów i tuż poza <br/> Przejścia pomiędzy stanami - przypadki testowe projektowane tak by sprawdzały dozwolone i niedozwolone przejścia między stanami <br/> Tablica decyzyjna |
| Smoke Testy | Testy korowych funkcjonalności |
| Testy Regresyjne | Przeprowadzane po smoke testach, weryfikują czy system się nie popsuł po dokonaniu zmian, wprowadzeniu nowych funkcjonalności, poprawieniu błędów |
| Co automatyzować | Korowe funkcjonalności (wykorzystywane w wielu miejscach) <br/> Testy odpalane wielokrotnie (regresyjne, smoke testy) <br/> Testy z dużą ilością danych testowych <br/> Testy odpalane na wielu przeglądarkach <br/> Funkcjonalności, które mają tendencję do psucia się |
| White box testing | Unit testing, zaglądamy co tam w bebechach piszczy. Weryfikujemy działanie metod, klas, procedur, tabel itd |
| Black box testing | Bez zaglądania w kod. Testujemy w oparciu o techniki testowe |
| Ad Hoc testing | Bez przygotowania, bazujemy jedynie na własnym doświadczeniu |
| Exploratory testing  | Bazujemy na własnym doświadczeniu. Przygotowujemy się do tego. Może być odrobina dokumentacji |
| Sesja eksploracyjna | Session based testing (2-3 sessions) each session 30-45 minutes. <br/> The session metrics are the primary means to express the status of the exploratory test process. They contain the following elements: <br/> Number of sessions completed <br/> Number of problems found <br/> Function areas covered <br/> Percentage of session time spent setting up for testing <br/> Percentage of session time spent testing <br/> Percentage of session time spent investigating problems |
| TDD | Koncepcja developmentu, w którym wpierw piszemy test pod funkcjonalność, piszemy funkcjonalność, jeśli failuje to poprawiamy funkcjonalność i raz jeszcze odpalamy test |
| BDD | Rozwinięcie koncepcji TDD o dodatkową warstwę przedstawiającą testy w języku naturalnym, zrozumiałym dla biznesu |
| Testing | Sprawdzenie czy wymagania zostały zaimplementowane poprawnie |
| QA | Szersze pojęcie niż testing. Testing jest składową QA, ale QA dba również o odczucia klienta np. estetyka, innowacyjność a także czy jakieś standardy zostały zachowane |
| Waga | Jak ważny bug jest dla biznesu |
| Priorytet | Jak szybko buga rozwiązać |
| Poziomy testowania | Modułowe(jednostkowe) <br/> Integracyjne <br/> Systemowe <br/> Akceptacyjne |
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
| UML | Modelowanie obiektowe. Przykładowe diagramy: <br/> Activity <br/> Use cases <br/> Classes |
| WSDL | (Web Services Description Language) - informacje odnośnie web-serwisu- akceptowane typy danych, port działania, operacje, informacje o end-pointach |
| PairWise Testing | Czarnoskrzynkowa technika projektowania przypadków testowych, której celem jest redukcja ilości przypadków testowych w celu szybszego ukończenia testowania. Dobre zastosowanie tej techniki nie powinno obniżać pokrycia |
| Jarzmo testowe | Środowisko testowe, składające się z zaślepek i sterowników potrzebnych do wykonania testu |
| Hot-Fix | Poprawka wprowadzona do aplikacji będącej już na produkcji bez nowego releasu całej aplikacji. Poprawka jest wpierw testowana na środowisku akceptacyjnym będącym kopią produkcji |
| Change Request | Prośba ze strony biznesu o wprowadzenie zmian do funkcjonalności aplikacji będącej na produkcji |
| Środowiska | DEV - zazwyczaj lokalnie u developera ale też często współdzielone przez innych developerów. <br/> TEST - dedykowane testerom do testów automatycznych i manualnych <br/> UAT - środowisko przeznaczone dla klienta do testów akceptacyjnych <br/> PROD - nie muszę chyba pisać co to oznacza  |


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
| BDD w praktyce | BDD binding in C# and Java - [Binding] and @Binding. <br/> Przykłady frameworków: <br/> Specflow - BDD dla C# używa atrybutów [] <br/> JBhave - BDD dla Javy używa annotacji <br/> Cucumber -  BDD dla Javy używa annotacji i co ważne sklejanie stepów z featurami używacie poprzez słówko kluczowe “glue” w klasie z runner’em testów. <br/> Jasmine - BDD dla JS |
| TestNG | Framework javowy do unit testów i funkcjonalnych. Najczęściej stosowany w połączeniu z selenium. Annotacje TestNG: @Test, @BeforeClass, @AfterClass, @BeforeSuite, @AfterSuite, @BeforeMethod, @AfterMethod |
| Locators | Można generalnie podzielić na dwie grupy: związane z DOM (xpath, id, name) i CSS |
| Aplikacje Mobilne | Native - instalowane na mobilkach z takich źródeł jak GooglePlay. Są dedykowane konkretnym urządzeniom. Mogą używać funkcjonalności telefonu np. Kamery <br/> Hybrid - Są dostępne np. z GooglePlay ale odpalane przeglądarkowo <br/> Web - apki odpalane przez przeglądarkę, zazwyczaj napisane w HTML5 |
| Testowanie mobilek | Narzędzia do testowania automatycznego urządzeń mobilnych: appium, robotium, espresso. W przypadku webowych można używać emulatorów selenium webdriver na aplikacje mobilne |
| Event Listenery | Zestaw metod, które umożliwiają logowanie akcji ale jedynie tych związanych z webdriverem |
| Regexp | Ciąg znaków określający szukany wzorzec. Np. .* szukamy plików dowolnego formatu |
| Programowanie niskopoziomowe | Programowanie niskiego poziomu to język zrozumiały dla peceta [język maszynowy (kod binarny)] np. assambler |
| Programowanie wysokopoziomowe | Programowanie wysokiego poziomu to programowanie zrozumiałe dla ludzi np. java. |
| Cache | Pamięć podręczna. Jest wykorzystywana do szybszego dostępu do danych. Np. Pamięć podręczna przeglądarki powoduje, że elementy już kiedyś załadowane ponownie nie muszą być ładowane po prostu są pobierane z pamięci podręcznej |
| Protractor | Framework jsowy dedykowany dla angularJS, służący do testów funkcjonalnych. Działa na selenium webdriverze |
| Środowisko uruchomieniowe | W językach wysokopoziomowych potrzebny jest specjalny interpreter, który przetłumaczy kod na postać binarną zrozumiałą dla maszyny. Przykładami są node.js i jre. |
| Package Manager | Ciąg znaków określający szukany wzorzec. Np. .* szukamy plików dowolnego formatu |
| Regexp | System do automatycznej instalacji, konfiguracji, aktualizacji i usuwania pakietów oprogramowania |


8. SQL

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| Union | Łączenie tabel o tej samej liczbie kolumn i typie. Usuwa duplikaty |
| Union ALL | Łączenie tabel o tej samej liczbie kolumn i typie. Nie usuwa duplikatów |
| Joins | left join - pokazuje część wspólną dwóch tabel oraz pozostałe rekordy w "lewej" tabeli <br/> right join - pokazuje część wspólną dwóch tabel oraz pozostałe rekordy w "prawej" tabeli <br/> inner join - pokazuje część wspólną tabel <br/> outer join - pokazuje część wspólną i nie wspólną tabel <br/> cross join - łączy każdy element z tabeli 1 z każdym elementem z tabeli 2 |
| Agregacje w SQL | AVG, SUM, MAX, MIN |
| EXCEPT | (SQL Server) odejmuje dwie tabele o takiej samej ilości kolumn i tych samych typach danych |
| MINUS | (Oracle) odejmuje dwie tabele o takiej samej ilości kolumn i tych samych typach danych |
| Count | Count(*) - zlicza ilość rekordów po wszystkich kolumnach <br/> Count(1) - zlicza ilość rekordów po pierwszej kolumnie |
| Hurtownia danych | Baza skonstruowana z innych baz relacyjnych celem szybszego dostępu do danych <br/> Podstawowymi elementami są: Staging area, Atomisation, Dimensions i Tabele faktów |
| Dynamiczny SQL | Czyli jak przechowywać zapytania w zmiennej, odpalać je z dowolnego miejsca kodu i przechowywać zwróconą wartość w innej zmiennej. Ma słabą wydajność. Oracle - Execute Immediate, SQL Server - exec sp_executesql |
| SQL hints | W SQL Server możemy dopomóc przy egzekucji zapytania pewnymi hintami celem przyspieszenia działania zapytania. join hints - merge, loop, hash table hints - NO LOCK|
| Pivot | Obracanie tabeli |
| Tabela CTE | Common table expression - służąca chociażby do insertowania w jednym zapytaniu dużej ilości rekordów |
| Klucze | Primary key <br/> Foreign key |
| Constraints | Określają ograniczenia kolumn: not null, unique, primary key, foreign key, index |
| Grupowanie | Grupowanie należy wykonywać po niezagregowanych kolumnach |
| Transakcje | Insert, update, delete |
| Indeksy | Klastrone <br/> Nieklastrowe |
| Konwertowanie danych | Convert - więcej możemy zrobić z datą niż w przypadku cast <br/> Cast - jest standardem ANSI |
| Trimming | ltrim - wycina spację z lewej strony <br/ >rtrim - wycina spację z prawej strony |
| Truncate | Chyba nie zwraca uwagi na klucze. Usuwa jak leci |
| Delete | Tutaj niestety errory wyskoczą, jak są indeksy i klucze pozakładane |


9. Komendy bash

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| cat [filename] | Pokazuje zawartość pliku |
| cd /directorypath  | Przechodzimy pomiędzy katalogami |
| chmod [options] mode filename | Zmienia uprawnienia do pliku |
| chown [options] filename | Zmienia właściciela pliku |
| clear | Czyści konsolę |
| cp [options] source destination | Kopiuje plik do katalogu |
| date [options]  | Pokazuje lub ustawia datę systemową |
| df [options]  | Pokazuje jak zajęty jest dysk twardy |
| du [options] | Pokazuje ile ważą pliki |
| file [options] filename | Określa jaki typ danych jest wewnątrz pliku |
| find [pathname] [expression] | Znajdź pliki dla danego wzorca |
| grep [options] pattern [filesname] | Pokaż pliki dla danego wzorca |
| kill [options] pid | Zatrzymuje proces. kill -9 bezwarunkowo |
| less [options] [filename] | Pokazuje zawartość zawartość pliku strona po stronie |
| ln [options] source [destination] | Miękkie dowiązanie |
| ls [options] | Wylistuj zawartość katalogu |
| man [command] | Pomoc |
| mkdir [options] directory  | Stwórz nowy katalog |
| mv [options] source destination | Zmień nazwę pliku lub wytnij i wklej go do innej lokalizacji |
| passwd [name [password]] | Zmiana hasła |
| ps [options]  | Pokazuje działające procesy |
| pwd | Ścieżka do katalogu, z którego wykonano komendę |
| rm [options] directory  | Usuwa pliki lub katalogi |
| rmdir [options] directory  | Usuwa katalogi |
| ssh [options] user@machine | Zdalne łączenie się z inną linuxową maszyną |
| su [options] [user [arguments]] | Przechodzenie pomiędzy użytkownikami |
| tail [options] [filename] | Pokazuje ostatnich 10 linijek pliku |
| tar [options] filename  | Pakowanie i rozpakowanie pliku |
| touch filename  | Tworzy pusty plik |
| who [options] | Pokazuje kto jest zalogowany |
| Union | |


10. Agile

| Zagadnienie       | Opis    |
| :------------- |:-------------|
| Zalety agile | Łatwiejsza reakcja na zmiany, szybciej trwa projekt |
| Wady agile | Większy chaos, dużo bugów, zero dokumentacji |
| Kanban |  |
| Ceremonie Scrumowe | Planning <br/> Daily Stand-up <br/> Review i Retrospective <br/> Backlog grooming <br/> Scrum of Scrums <br/> Poker planning |
| Produkty Scrumowe | Product backlog - lista high-levelowych wymagań <br/> Sprint backlog - lista tasków brana na sprint <br/> Burndown-chart - pokazuje progres pracy <br/> Zależność czasu wyestymowanych tasków od czasu w sprincie <br/> User Story - historyjka brana na sprinta. Zazwyczaj funkcjonalność |
| Zespół w Scrumie | Developer (Dev Team) - wiadomo co robi <br/> Product Owner - zarządza backlogiem, reprezentuje interesy klienta <br/> Scrum Master - zarządza procesem i ceremoniami scrumowymi |
| SAFe | Scaled Agile Framework- Podejście agilowe dla dużych projektów w którym istnieje wiele zespołów scrumowych współpracujących ze sobą |


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
