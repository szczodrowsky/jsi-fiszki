# Jakość systemów informatycznych: odpowiedzi do samosprawdzenia

Opracowanie zawiera odpowiedzi na wszystkie 62 pytania z pliku [Pytania do samosprawdzenia][PYT]. Podstawę stanowi 11 prezentacji Jarosława Kuchty. Zachowano oryginalną treść i numerację pytań oraz podział według prezentacji.

- *Według prezentacji* i *Synteza prezentacji*: odpowiedź oparta na materiałach wykładowych.
- *Uzupełnienie własne* i *Przykład własny*: wyjaśnienie lub przykład wykraczający poza treść slajdów.
- Bloki **Komentarz / korekta**: zastrzeżenia i doprecyzowania, z odsyłaczami do źródeł zewnętrznych tam, gdzie je wykorzystano. Są to uwagi do odpowiedzi, nie cytaty z prezentacji.

Numery stron dotyczą PDF-ów i obejmują stronę tytułową. Opisy norm i modeli odnoszą się przede wszystkim do wersji omawianych na wykładzie. W spisie treści można wybrać prezentację lub numer pytania.

## Spis treści i przypisanie pytań

| Prezentacja | Pytania |
|---|---|
| [1. Wprowadzenie](#wprowadzenie) | [1](#pytanie-1), [2](#pytanie-2), [3](#pytanie-3), [5](#pytanie-5), [6](#pytanie-6), [8](#pytanie-8), [9](#pytanie-9), [10](#pytanie-10), [11](#pytanie-11), [12](#pytanie-12), [13](#pytanie-13), [14](#pytanie-14), [15](#pytanie-15), [16](#pytanie-16), [17](#pytanie-17), [18](#pytanie-18), [19](#pytanie-19) |
| [1a. Studium przypadku](#studium) | [4](#pytanie-4) |
| [2. Jakość w procesie wytwarzania](#proces) | [20](#pytanie-20), [21](#pytanie-21), [22](#pytanie-22), [23](#pytanie-23), [24](#pytanie-24), [25](#pytanie-25), [26](#pytanie-26), [27](#pytanie-27), [28](#pytanie-28), [29](#pytanie-29), [30](#pytanie-30) |
| [3. Model McCalla](#mccall) | [32](#pytanie-32), [33](#pytanie-33), [34](#pytanie-34), [35](#pytanie-35) |
| [4. Pomiary](#pomiary) | [38](#pytanie-38), [39](#pytanie-39), [40](#pytanie-40), [41](#pytanie-41) |
| [4a. ISO/IEC 9126](#iso9126) | [7](#pytanie-7), [36](#pytanie-36), [37](#pytanie-37) |
| [5. CMM/CMMI](#cmmi) | [44](#pytanie-44), [45](#pytanie-45), [46](#pytanie-46) |
| [6. ISO 9000/9001](#iso9001) | [31](#pytanie-31), [47](#pytanie-47), [48](#pytanie-48), [49](#pytanie-49) |
| [7a. GQM](#gqm) | [42](#pytanie-42) |
| [7b. AHP](#ahp) | [43](#pytanie-43) |
| [8. Jakość w Agile](#agile) | [50](#pytanie-50), [51](#pytanie-51), [52](#pytanie-52), [53](#pytanie-53), [54](#pytanie-54), [55](#pytanie-55), [56](#pytanie-56), [57](#pytanie-57), [58](#pytanie-58), [59](#pytanie-59), [60](#pytanie-60), [61](#pytanie-61), [62](#pytanie-62) |

<a id="wprowadzenie"></a>

## 1. Wprowadzenie

Prezentacja: [1.Wprowadzenie.pdf][W].

<a id="pytanie-1"></a>

### 1. Jaki jest wpływ jakości oprogramowania na jakość systemu informatycznego w porównaniu z innymi elementami (np. sprzęt, ludzie, organizacja)?

*Według prezentacji:*

Oprogramowanie współdziała ze sprzętem, ludźmi, procesami, procedurami oraz zasobami informacji, takimi jak zewnętrzne dane i bazy wiedzy. Każdy z tych elementów wpływa na działanie systemu. **Jakość systemu zależy od ich współdziałania.** Nawet poprawny program nie zapewni dobrych wyników przy błędnych danych, zawodnym sprzęcie lub niewłaściwych procedurach.

*Uzupełnienie własne:*

Nie można podać uniwersalnego procentowego udziału oprogramowania w jakości systemu. Wpływ poszczególnych elementów zależy od zastosowania i od tego, który element ogranicza skuteczność lub bezpieczeństwo całości.

*Źródło:* [W], s. 2-3; [T], s. 17-21.

<a id="pytanie-2"></a>

### 2. Czy u źródeł każdej awarii systemu informatycznego stoi błąd programistów?

*Według prezentacji:*

Nie. Awarię mogą spowodować błędy projektu, niesprawny sprzęt, nieprawidłowa obsługa, błędne dane lub niewłaściwa organizacja pracy. Często nakłada się na siebie kilka takich przyczyn. Slajd przedstawiający ciąg „pomyłka → defekt → błąd wykonania → awaria → wypadek → katastrofa” pokazuje możliwą drogę powstawania szkody, a nie jedyną przyczynę wszystkich awarii. Therac-25 ilustruje współudział wad programu, konstrukcji urządzenia i procedur organizacyjnych.

*Uzupełnienie własne:*

**Sam defekt nie musi spowodować awarii**. Muszą wystąpić warunki, które go ujawnią; niezależne zabezpieczenia mogą zatrzymać dalszy rozwój zdarzeń.

*Źródło:* [W], s. 3, 6; [T], s. 5, 17-20.

<a id="pytanie-3"></a>

### 3. Dlaczego wytwórcy oprogramowania nie mogą zagwarantować 100% bezbłędności swojego produktu?

*Według prezentacji:*

Oprogramowanie jest złożone, a błędy projektowe są trudne do wykrycia i usunięcia. Same testy systemowe nie wystarczają. W studium Therac-25 wcześniejsze testy i zaufanie do programu nie zapobiegły błędom zależnym od szczególnej kolejności działań i czasu ich wykonania.

*Uzupełnienie własne:*

W rozbudowanym produkcie liczba kombinacji danych, stanów, interakcji i środowisk przekracza praktyczne możliwości testowania. Ponadto specyfikacja może być niepełna lub błędna. Pozytywne wyniki testów potwierdzają zachowanie w zbadanych warunkach, a nie we wszystkich możliwych.

> **Korekta.** Zdanie ze studium przypadku, że stworzenie oprogramowania bez błędów jest niemożliwe, jest zbyt kategoryczne. Można udowodnić określone własności programu względem formalnej specyfikacji i założeń, czego przykładem jest seL4. Taki dowód nie jest bezwarunkową gwarancją poprawności całego systemu, sprzętu i rzeczywistych wymagań. Źródło zewnętrzne: [seL4, Verification](https://sel4.systems/Verification/).

*Źródło prezentacji:* [W], s. 4; [T], s. 4, 14, 17, 19, 21.

<a id="pytanie-5"></a>

### 5. Dlaczego rozumienie jakości oprogramowania jako stopnia spełnienia wyspecyfikowanych wymagań jest niewystarczająca?

*Według prezentacji:*

Jakość obejmuje również **spełnienie oczekiwań klienta i użytkownika**. Specyfikacja może pomijać potrzeby uznawane za oczywiste, potrzeby jeszcze nierozpoznane albo wymagania wynikające z warunków użycia. Produkt może więc spełnić zapisane wymagania i nadal nie nadawać się do rzeczywistej pracy.

Trzeba uwzględnić m.in. bezpieczeństwo, ochronę danych, użyteczność, wydajność i wymagania obowiązkowe. Ocenę zgodności ze specyfikacją należy uzupełnić oceną przydatności produktu w docelowym zastosowaniu.

*Źródło:* [W], s. 7-15; [I], s. 19-20; [AG], s. 6-7, 13.

<a id="pytanie-6"></a>

### 6. Dlaczego przy zbieraniu wymagań dla oprogramowania nie wystarczy o nie pytać przedstawiciela klienta?

*Według prezentacji:*

Przedstawiciel klienta może nie znać potrzeb wszystkich użytkowników, mieć ograniczoną wiedzę o pracy operacyjnej lub nie mieć odpowiednich uprawnień decyzyjnych. Może też pominąć wymagania, które uważa za oczywiste, albo nie wspomnieć o potrzebach, których sam jeszcze nie rozpoznał. Jego oczekiwania mogą różnić się od potrzeb osób faktycznie korzystających z systemu.

Wymagania należy uzgadniać również z użytkownikami bezpośrednimi i pośrednimi, dostawcami danych oraz odbiorcami wyników. Pomagają prototypy, przeglądy z użytkownikami i sprawdzenie wymagań dotyczących zamierzonego użycia oraz wymagań obowiązkowych.

*Uzupełnienie własne:*

Warto obserwować rzeczywistą pracę i analizować przypadki wyjątkowe, zamiast opierać się wyłącznie na deklaracjach jednej osoby.

*Źródło:* [W], s. 3, 7; [PR], s. 24; [I], s. 19-21, 27; [AG], s. 7, 10, 13.

<a id="pytanie-8"></a>

### 8. Z jakich elementów składa się model „drzewa” jakości?

*Według prezentacji:*

Korzeniem jest ogólna jakość. Niżej znajdują się główne atrybuty, następnie bardziej szczegółowe cechy, a ich ocenę umożliwiają metryki i pomiary. W modelu ze wprowadzenia główne gałęzie to **funkcjonalność, wydajność, wiarygodność, satysfakcja i elastyczność**. Przykładowo funkcjonalność obejmuje kompletność, adekwatność i spójność.

Metrykom przypisuje się wagi. Ocena atrybutu może być średnią ważoną:

`A_i = Σ(w_j · M_j) / Σ(w_j)`, przy `Σ(w_j) > 0`.

> **Komentarz własny.** Nazwa „drzewo” jest umowna. Ta sama cecha, np. testowalność, może wspierać kilka gałęzi. Nie należy utożsamiać pięciu gałęzi ze wprowadzenia z sześcioma charakterystykami ISO/IEC 9126 ani z jedenastoma czynnikami McCalla.

*Źródło:* [W], s. 10, 21-22; [M], s. 2-11; [ISO], s. 8.

<a id="pytanie-9"></a>

### 9. Co to są atrybuty jakości i jak się mają do wymagań?

*Według prezentacji:*

Atrybuty to cechy jakościowe produktu świadczące o jego wartości dla użytkownika. Porządkują wymagania według rodzaju ocenianej jakości. Wprowadzenie łączy wymagania funkcjonalne z funkcjonalnością, czasowe z wydajnością, niezawodnościowe z wiarygodnością, a ograniczenia z elastycznością.

*Uzupełnienie własne:*

Atrybut jest ogólną cechą, a wymaganie określa oczekiwany poziom tej cechy w danych warunkach. „Wydajność” jest atrybutem; „95% odpowiedzi w czasie poniżej 2 sekund przy 100 równoczesnych użytkownikach” jest przykładowym wymaganiem. Metryka i procedura pomiaru pozwalają sprawdzić jego spełnienie.

*Źródło:* [W], s. 8-9, 21.

<a id="pytanie-10"></a>

### 10. Czy dla każdego atrybutu jakości można wyznaczyć metrykę?

*Według prezentacji:*

Model zakłada ocenianie atrybutów za pomocą metryk, ale pomiary mogą być subiektywne, pozbawione punktu odniesienia lub trudne do interpretacji. Materiały nie dowodzą, że każdy atrybut ma jedną obiektywną i uniwersalną metrykę.

*Uzupełnienie własne:*

Dla wielu atrybutów można zaproponować wskaźnik pośredni, zestaw pomiarów albo ocenę ekspercką. Nie oznacza to, że liczba w pełni oddaje cechę. Przykładowo czas nauki i liczba popełnianych błędów opisują różne aspekty łatwości nauki.

Przy cechach trudno mierzalnych trzeba jawnie określić, co dany wskaźnik obejmuje, czego nie obejmuje i w jakich warunkach jest wiarygodny.

*Źródło:* [W], s. 21-25; [P], s. 3, 22; [ISO], s. 6, 20.

<a id="pytanie-11"></a>

### 11. Czym różnią się metryki jakościowe od miar?

*Według prezentacji:*

Slajd 23 używa rozróżnienia „metryka: to, co się mierzy” i „miara: jak się mierzy”. W tym ujęciu metryka określa ilościowy sposób oceny atrybutu. Miara wiąże tę ocenę z konkretną skalą, jednostką lub sposobem wyznaczenia wartości. Dla kompletności funkcjonalnej pokazano iloraz liczby zrealizowanych funkcji i liczby funkcji wymaganych.

*Przykład własny:*

Przy 90 zrealizowanych funkcjach ze 100 wymaganych otrzymujemy wskaźnik `90/100 = 0,9`, czyli 90%. Liczby funkcji są danymi pomiarowymi, iloraz jest regułą obliczania wskaźnika, a 0,9 jest wynikiem oceny według tej reguły.

> **Komentarz własny.** Terminologia prezentacji nie jest całkowicie konsekwentna. W „Pomiarach” rozmiar kodu jest nazwany metryką bezpośrednią, a ISO 9126 dopuszcza metryki wyrażone czasem. Nie należy więc przyjmować, że każda metryka musi należeć do przedziału `[0,1]`, a każda miara mieć jednostkę fizyczną.
>
> Aby uniknąć nieporozumień, warto osobno wskazać ocenianą cechę, definicję wskaźnika, procedurę pomiaru i uzyskany wynik.

*Źródło:* [W], s. 21-24; [P], s. 5-6; [ISO], s. 3-7.

<a id="pytanie-12"></a>

### 12. Jakie problemy występują przy pomiarach jakości?

*Według prezentacji:*

- jakość obejmuje wiele cech, które trudno sprowadzić do jednej liczby;
- oceny bywają subiektywne;
- często brakuje punktu odniesienia i kryterium interpretacji wyniku;
- wyniki wymagają normalizacji, a dobór skali może zmienić ocenę;
- wagi atrybutów bywają arbitralne;
- zebranie wielu miar jest kosztowne i trudne;
- długie ankiety zniechęcają respondentów i mogą obniżać rzetelność odpowiedzi.

> **Komentarz własny.** Pytania tak/nie ułatwiają kodowanie odpowiedzi, lecz same nie zapewniają obiektywności. Nadal trzeba uzgodnić znaczenie pytań, warunki oceny i sposób doboru respondentów.

*Źródło:* [W], s. 24-25; [P], s. 22; [ISO], s. 20.

<a id="pytanie-13"></a>

### 13. Czy zawsze wyniki pomiarów uśrednia się wg średniej arytmetycznej?

*Według prezentacji:*

Nie ma takiej ogólnej zasady. Wprowadzenie pokazuje zwykłe uśrednianie ocen ekspertów oraz średnią ważoną metryk. Gdy cechy mają różne znaczenie, ich wkład w ocenę powinien być różny.

*Uzupełnienie własne:*

Sposób agregacji zależy od rodzaju danych i celu oceny. Dla czasów odpowiedzi można analizować medianę i percentyle, ponieważ średnia może ukryć rzadkie, bardzo długie opóźnienia.

Przy łączeniu odsetków obliczonych dla grup o różnej liczebności trzeba uwzględnić liczbę prób. Jeśli w pierwszej grupie mamy 1 sukces na 1 próbę, a w drugiej 1 sukces na 9 prób, łącznie uzyskujemy `2/10 = 20%`. Zwykła średnia obu odsetków dałaby około 55,6% i nie opisywałaby wyniku wszystkich prób.

W przypadku wymagania krytycznego można uzależnić pozytywną ocenę od jego bezwzględnego spełnienia. Wysokie oceny pozostałych cech nie muszą wtedy rekompensować jego niespełnienia.

*Źródło podstawy:* [W], s. 22, 24-25. Slajdy nie zawierają kompletnej odpowiedzi statystycznej; przykłady i dobór agregacji są uzupełnieniem własnym.

<a id="pytanie-14"></a>

### 14. Czy zawsze miary się przelicza na metryki wg skali liniowej?

*Według prezentacji:*

Nie ma obowiązku liniowego przeliczania. Materiał wskazuje problem normalizacji i nieustalonych skal; ISO 9126 stosuje m.in. ilorazy, ich dopełnienia, czasy i częstości zdarzeń. Nie każda metryka jest już znormalizowaną oceną jakości.

*Uzupełnienie własne:*

Przeliczenie wyniku pomiaru na ocenę powinno odpowiadać wymaganiom. Może być liniowe, progowe albo odcinkowe. Jeśli dopuszczalny czas reakcji wynosi maksymalnie 100 ms, przekroczenie tego progu może oznaczać niespełnienie wymagania, nawet gdy wzrost czasu był niewielki. Należy też określić kierunek skali: większa kompletność jest korzystna, większa liczba błędów na godzinę zwykle nie.

*Źródło podstawy:* [W], s. 23-25; [ISO], s. 3-7, 20. Funkcje progowe i odcinkowe są uzupełnieniem własnym.

<a id="pytanie-15"></a>

### 15. Co daje ocena jakości z użyciem modelu drzewa?

*Synteza prezentacji:*

Model drzewa pozwala przejść od ogólnego pojęcia jakości do konkretnych cech i wskaźników. Umożliwia określenie priorytetów, przypisanie wag, porównanie produktów według wspólnych kryteriów oraz wskazanie cech wymagających poprawy. Pokazuje też, że znaczenie atrybutów zależy od klasy aplikacji.

> **Komentarz własny.** Wynik końcowy zależy od przyjętego modelu, kryteriów i wag. Dwa produkty z taką samą oceną łączną mogą mieć zupełnie inne słabości. Obok wyniku zbiorczego warto zachować wyniki składowe oraz osobno sprawdzać wymagania krytyczne.

*Źródło:* [W], s. 10, 16-25; [M], s. 6, 10-14.

<a id="pytanie-16"></a>

### 16. Czym różni się wiarygodność systemu informatycznego od jego niezawodności?

*Według wprowadzenia:*

- Wiarygodność (*dependability*) oznacza stopień zaufania do systemu. Obejmuje niezawodność, odporność na błędy, bezpieczeństwo, ochronę i testowalność.
- Niezawodność (*reliability*) dotyczy możliwości korzystania z usług systemu bez jego upadku. Jest zatem częścią szerszej wiarygodności.

*Przykład własny:*

System może działać nieprzerwanie, lecz ujawniać dane osobom nieuprawnionym. Ma wtedy dobrą ciągłość działania, ale nie zasługuje na pełne zaufanie.

> **Komentarz terminologiczny.** W prezentacjach McCalla i ISO 9126 słowo *reliability* przetłumaczono jako „wiarygodność”. Przy tym pytaniu należy stosować rozróżnienie z „Wprowadzenia” i podawać angielskie terminy, aby uniknąć pomieszania modeli.

*Źródło:* [W], s. 13; porównawczo [M], s. 3, oraz [ISO], s. 10.

<a id="pytanie-17"></a>

### 17. Czym różni się bezpieczeństwo systemu informatycznego od jego ochrony?

*Według prezentacji:*

- Bezpieczeństwo (*safety*) oznacza zapobieganie szkodom wyrządzanym przez system w jego otoczeniu.
- Ochrona (*security*) dotyczy zabezpieczenia systemu i danych przed nieuprawnionym dostępem i działaniem.

*Przykład własny:*

Niedopuszczenie do podania nadmiernej dawki promieniowania to *safety*. Uniemożliwienie osobie nieuprawnionej zmiany parametrów zabiegu to *security*. Naruszenie ochrony może spowodować zagrożenie bezpieczeństwa.

> **Doprecyzowanie na podstawie innej prezentacji.** Definicja ochrony jako samej kontroli dostępu jest skrótem. ISO 9126 uwzględnia także uniemożliwienie nieautoryzowanego odczytu i modyfikacji oraz zachowanie dostępu dla osób uprawnionych. W języku potocznym „bezpieczeństwo” bywa używane w obu znaczeniach.

*Źródło:* [W], s. 13; [ISO], s. 9, 18.

<a id="pytanie-18"></a>

### 18. Czym różni się konfigurowalność systemu informatycznego od jego modyfikowalności?

*Według prezentacji:*

- Konfigurowalność to łatwość dostosowania systemu do potrzeb użytkownika bez konieczności zmiany jego funkcji.
- Modyfikowalność oznacza łatwość wprowadzania zmian w funkcjach systemu.

*Przykłady własne:*

Wybór języka interfejsu, ustawienie dostępnych opcji lub dostosowanie skrótów klawiszowych to konfiguracja. Dodanie nowego algorytmu naliczania opłat lub nowego rodzaju raportu wymaga modyfikacji funkcjonalnej. Konfiguracja wykorzystuje przewidziane warianty, a modyfikacja zmienia lub rozszerza możliwości produktu.

*Źródło:* [W], s. 15; [M], s. 17, 20.

<a id="pytanie-19"></a>

### 19. Czym różni się łatwość testowania systemu informatycznego od łatwości śledzenia?

*Według prezentacji:*

- Łatwość testowania oznacza łatwość przygotowania i wykonania sprawdzeń poprawności działania oraz wykrywania błędów.
- Łatwość śledzenia pomaga zrozumieć działanie systemu i ustalić, co się w nim wydarzyło. W przykładach służą temu logi oraz dokumenty pośrednie.

> **Doprecyzowanie.** Materiały używają *traceability* w dwóch znaczeniach. W klasycznym opisie McCalla są to powiązania od wymagań do implementacji; w późniejszych przykładach przede wszystkim obserwowalność działania programu. Oba zastosowania mogą wspierać testowanie, lecz nie zastępują testów.

*Przykład własny:*

Log wyjaśnia, jak wyliczono cenę; test porównuje cenę z oczekiwanym wynikiem; powiązanie testu z wymaganiem pokazuje, jaką regułę biznesową sprawdzono.

*Źródło:* [W], s. 11, 13, 15; [M], s. 4, 7, 16; [C], s. 26.

<a id="studium"></a>

## 1a. Studium przypadku: Therac-25

Prezentacja: [1a.StudiumPrzypadku.pdf][T].

<a id="pytanie-4"></a>

### 4. Jakie były źródłowe przyczyny wypadków z systemem do radioterapii Therac-25 w połowie lat ’80 XX wieku w USA i Kanadzie (błędy użytkowników, programistów, konstruktorów, projektantów)?

*Według prezentacji:*

Wypadki wynikały ze splotu błędów technicznych i organizacyjnych, a nie z jednej pomyłki operatora.

| Obszar | Przyczyny opisane na slajdach |
|---|---|
| Konstrukcja i architektura zabezpieczeń | Usunięcie części niezależnych zabezpieczeń sprzętowych i zbyt duże zaufanie do sterowania programowego. W Therac-20 podobny problem programu nie doprowadził do przedawkowania, ponieważ zadziałała blokada sprzętowa. |
| Projektowanie i programowanie | Błędy zależne od czasu wykonania i współbieżności. Szybka korekta trybu zabiegu mogła zmienić dane widoczne na ekranie bez odpowiedniej zmiany stanu sterowania. Materiał omawia też niewłaściwe rozpoznawanie położenia obrotnicy. |
| Interfejs i obsługa | Niejasne komunikaty, mylące wskazania dawki i możliwość ponawiania zabiegu po błędzie. W jednym zdarzeniu odłączona kamera i interkom utrudniły reakcję na sygnały pacjenta. |
| Analiza ryzyka i weryfikacja | Analiza bezpieczeństwa skupiona na sprzęcie, założenie braku pozostałych błędów programu i niewystarczające testowanie oraz analiza oprogramowania. |
| Zarządzanie i procedury | Brak odpowiedniej reakcji na wcześniejsze wypadki, słaba dokumentacja zdarzeń, niedostatki wymiany informacji i procedur analizy awarii. |

Pomyłka operatora lub szybka korekta danych mogły uruchomić wadliwy scenariusz. System powinien jednak bezpiecznie obsługiwać przewidywalne pomyłki i nie dopuszczać do niebezpiecznej emisji. Przypisanie winy wyłącznie użytkownikowi pomija źródłowe wady projektu.

> **Korekta.** Slajd 16 sprowadza przypadek Yakima z 1987 r. do wyścigu procedur. Opis Leveson wskazuje także konkretny mechanizm: jednobajtowa zmienna `Class3` była zwiększana i co 256 przebiegów przyjmowała wartość zero. Mogło to pominąć sprawdzenie położenia kolimatora. Zależność czasowa była istotna, ale bez informacji o przepełnieniu wyjaśnienie jest niepełne. Źródło zewnętrzne: [Nancy Leveson, opis Therac-25, część o zmiennej Class3](https://www.cse.msu.edu/~cse435/Handouts/Therac25-Leveson.pdf).

*Źródło prezentacji:* [T], s. 3-5, 8-9, 11-14, 16-21.

<a id="proces"></a>

## 2. Jakość w procesie wytwarzania oprogramowania

Prezentacja: [2.JakoscWProcesie.pdf][PR].

<a id="pytanie-20"></a>

### 20. Dlaczego o jakość oprogramowania warto dbać od samego początku projektu?

*Według prezentacji:*

Niewykryte defekty przechodzą do kolejnych etapów i mogą powodować następne błędy. Niepoprawne wymaganie może zostać przeniesione do projektu, implementacji i testów. Później trzeba poprawić wszystkie zależne od niego elementy, dlatego koszt usunięcia błędu rośnie.

Wczesne przeglądy wymagań i projektu, uzgodnienia z użytkownikami oraz zaplanowane działania jakościowe zmniejszają liczbę defektów docierających do testów i eksploatacji. W przykładzie z prezentacji kontrola jakości w całym procesie pozostawia 3 błędy po wydaniu zamiast 12.

*Źródło:* [PR], s. 2-6, 10-19, 24.

<a id="pytanie-21"></a>

### 21. Jak wygląda kosztowność zmian w różnych fazach cyklu życia oprogramowania?

*Według prezentacji:*

Względny koszt zmiany rośnie od definiowania przez opracowywanie do utrzymywania. Wykres podaje odpowiednio wartości `1 : 10 : 100`.

*Uzupełnienie własne:*

Zmiana wymagania na początku może wymagać głównie poprawienia opisu i uzgodnień. Po implementacji może obejmować kod, testy, dokumentację i integrację. Po wdrożeniu dochodzą np. migracja danych, aktualizacja instalacji i usuwanie skutków u użytkowników.

> **Komentarz własny.** Proporcje 1:10:100 są ilustracją z wykładu, a nie prawem obowiązującym w każdym projekcie. Koszt zależy od rodzaju zmiany, architektury, automatyzacji i skutków wdrożenia. Wniosek egzaminacyjny pozostaje ten sam: opłaca się wcześnie wykrywać błędne decyzje.

*Źródło:* [PR], s. 2, 6.

<a id="pytanie-22"></a>

### 22. Co to jest i co daje model wzmocnienia defektów?

*Według prezentacji:*

Model opisuje przepływ defektów między etapami. Uwzględnia defekty odziedziczone bez zmian, defekty wzmocnione, czyli powodujące kolejne błędy, defekty nowo wprowadzone oraz skuteczność ich wykrywania. Pozwala porównać, jak wynik zależy od etapu, na którym prowadzi się kontrolę jakości, oraz od jej skuteczności.

*Uzupełnienie własne, zapis schematu:*

Jeśli `D_p` to defekty przepuszczone bez wzmocnienia, `D_w` to defekty podlegające wzmocnieniu, `x` to mnożnik, `D_n` to defekty nowe, a `e` to wykrywana część defektów, wówczas:

`D_wyjściowe = (D_p + x · D_w + D_n) · (1 - e)`.

Na slajdach kontrola dopiero przy testowaniu prowadzi do 12 defektów po wydaniu, a kontrola w całym procesie do 3. Zestawione koszty wynoszą odpowiednio 2177 i 693 umowne jednostki. Model pokazuje korzyść wczesnego usuwania defektów, zanim się rozprzestrzenią.

> **Korekta rachunkowa.** Na slajdzie 6 wpisano `3 × 67 = 202`, choć iloczyn wynosi 201. Suma drugiego wariantu, liczona z widocznych danych, wynosi więc `33 + 234 + 225 + 201 = 693`. Z kolei suma kosztów cząstkowych wydrukowanych na slajdzie wynosi 694. Podany łączny wynik 693 jest zgodny z poprawnym iloczynem 201. To błąd w jednej komórce tabeli, bez wpływu na główny wniosek.

*Źródło:* [PR], s. 3-6; wzór i sprawdzenie rachunku: opracowanie własne.

<a id="pytanie-23"></a>

### 23. Dlaczego tradycyjna kontrola jakości produktu zawodzi w przypadku oprogramowania?

*Według prezentacji:*

Sprawdzanie gotowego produktu następuje zbyt późno, aby tanio zapobiec skutkom błędów wymagań i projektu. Również pojedyncza kontrola po każdym etapie nie zastępuje ciągłych działań jakościowych. Defekty mogą przechodzić dalej i ulegać wzmocnieniu.

*Uzupełnienie własne:*

W typowym oprogramowaniu defekt projektu jest powielany w kolejnych kopiach tego samego programu. Wyeliminowanie wadliwej kopii nie usuwa przyczyny. Trzeba poprawić wymagania, projekt lub kod, a następnie ponownie sprawdzić produkt. Same testy końcowe nie gwarantują też poprawności wszystkich scenariuszy.

> **Komentarz własny.** Kontrola produktu pozostaje potrzebna. Zawodzi traktowanie jej jako jedynego mechanizmu zapewniania jakości, a nie samo testowanie czy przegląd gotowego wyniku.

*Źródło:* [PR], s. 3-10, 20-24; [T], s. 21.

<a id="pytanie-24"></a>

### 24. Na czym polega polityka zapewniania jakości oprogramowania (SQA) w organizacji?

*Według prezentacji:*

SQA (*Software Quality Assurance*) jest **planowym, usystematyzowanym zbiorem działań** służących zapewnieniu jakości. Organizacja ustanawia standardy i procedury oraz stosuje je na wszystkich etapach wytwarzania. Obejmuje to metody techniczne, formalne przeglądy, testowanie, kontrolę zmian, pomiary i raportowanie.

Działania SQA obejmują ocenę produktu z perspektywy klienta oraz sprawdzanie, czy zespół pracuje zgodnie z przyjętymi standardami. Są prowadzone podczas wytwarzania, a także przy końcowym odbiorze.

> **Komentarz własny.** Zapewnianie jakości ma dawać uzasadnione zaufanie do produktu i procesu jego wytwarzania. Nie jest obietnicą całkowitego braku defektów.

*Źródło:* [PR], s. 7, 9-10, 20.

<a id="pytanie-25"></a>

### 25. Jakie są zadania zespołu zapewniania jakości (SQA) w organizacji?

*Według prezentacji zespół SQA:*

- ocenia powstające oprogramowanie z punktu widzenia klienta i czynników jakości;
- sprawdza zgodność pracy z ustanowionymi standardami;
- sprawdza, czy uczestnicy procesu wykonują przypisane zadania jakościowe;
- wspiera i nadzoruje przeglądy, testowanie, kontrolę zmian oraz pomiary;
- zapisuje i raportuje wyniki oraz niezgodności.

Prezentacja CMM dopowiada, że ocena powinna być obiektywna. Zainteresowane osoby muszą otrzymywać informacje o wynikach, a problemy, których zespół projektowy nie może rozwiązać, należy przekazywać wyższemu kierownictwu.

> **Komentarz własny.** Zespół SQA nie musi osobiście wykonywać wszystkich testów i przeglądów. Odpowiedzialność za jakość pozostaje również po stronie wykonawców i kierownictwa.

*Źródło:* [PR], s. 9-10; [C], s. 14.

<a id="pytanie-26"></a>

### 26. Jakie formy przeglądów technicznych produktów programowych stosuje się w projekcie?

*Według prezentacji podstawowe formy FTR (*Formal Technical Review*) to:*

- *walkthrough*: przejście przez dokument lub inny produkt pracy w jego logicznej kolejności, np. omówienie kolejnych fragmentów;
- inspekcja: systematyczne sprawdzanie według listy kontrolnej.

Przeglądy obejmują wymagania, analizę, projekt, kod i dokumentację testów. Mają wykrywać defekty, potwierdzać zgodność z wymaganiami i standardami oraz ułatwiać utrzymanie. Materiał wymienia także przeglądy wzajemne (*peer review*) przy implementacji.

*Uzupełnienie własne:*

Określenie *peer review* wskazuje, że ocenę prowadzą współpracownicy. Taki przegląd może mieć formę inspekcji lub walkthrough, więc te nazwy nie muszą oznaczać rozłącznych kategorii.

*Źródło:* [PR], s. 11-19, 24.

<a id="pytanie-27"></a>

### 27. Co oznacza kompleksowe zarządzanie jakością (TQM) w organizacji?

*Według prezentacji:*

TQM (*Total Quality Management*) angażuje **całą organizację** w rozumienie i spełnianie oczekiwań klientów. Każdy pracownik odpowiada za jakość swojej pracy, a kierownictwo przewodzi działaniom i zapewnia warunki ich realizacji.

Obejmuje zarządzanie procesami, zapobieganie problemom, mierzenie jakości, planowanie usprawnień i ciągłe doskonalenie. Dotyczy całego cyklu życia produktu, łącznie z utrzymaniem, oraz relacji między wewnętrznymi klientami i dostawcami.

> **Komentarz własny.** Slajdowe hasło o standardzie wolnym od defektów należy rozumieć jako kierunek działania i oczekiwanie zapobiegania błędom, nie jako dowód, że każdy produkt organizacji jest bezbłędny.

*Źródło:* [PR], s. 21-24.

<a id="pytanie-28"></a>

### 28. Jak się ma zapewnianie jakości oprogramowania (SQA) do kompleksowego zarządzania jakością (TQM) w organizacji?

*Według prezentacji:*

SQA skupia się na planowych działaniach zapewniających jakość oprogramowania i jego wytwarzania. TQM rozszerza perspektywę na całą organizację, jej zarządzanie, kulturę pracy, procesy, dostawców i relacje z klientami. SQA można traktować jako część praktycznej realizacji TQM w obszarze oprogramowania.

> **Komentarz własny.** Zdanie ze slajdu 20, że SQA nie zapewnia wysokiej jakości, odczytuję jako ostrzeżenie przed samym formalnym wykonywaniem procedur. Nie wynika z niego, że SQA jest nieskuteczne lub zbędne. Działania inżynierskie wymagają wsparcia organizacyjnego, zasobów i właściwie określonych celów.

*Źródło:* [PR], s. 7, 9-10, 20-24.

<a id="pytanie-29"></a>

### 29. Co oznacza odpowiedzialność kierownictwa za kompleksowe zarządzanie jakością (TQM) w organizacji?

*Według prezentacji:*

Kierownictwo odpowiada za organizowanie działań jakościowych i aktywne przewodzenie ich realizacji. Ustanawia politykę i cele, określa odpowiedzialności i uprawnienia, zapewnia ludzi, czas i środki oraz organizuje doskonalenie procesów.

Powinno też okresowo przeglądać działanie systemu jakości i reagować na problemy przekraczające możliwości pojedynczego zespołu. Odpowiedzialność obejmuje decyzje organizacyjne wpływające na jakość w całym cyklu życia produktu.

*Źródło:* [PR], s. 21-24; [I], s. 5, 11, 15-16; [C], s. 14.

<a id="pytanie-30"></a>

### 30. Czy kierownictwo organizacji może przenieść odpowiedzialność za kompleksowe zarządzanie jakością (TQM) na niższy szczebel zarządzania?

*Odpowiedź wynikająca z prezentacji:*

Kierownictwo **może delegować zadania i uprawnienia**, ale zachowuje odpowiedzialność za politykę, zasoby i skuteczność zarządzania jakością całej organizacji. TQM wymaga zaangażowania i przywództwa kierownictwa.

*Uzupełnienie własne:*

Kierownik zespołu może odpowiadać np. za przeglądy kodu, a pełnomocnik jakości za audyty. Nie zwalnia to zarządu z reagowania na brak zasobów, sprzeczne cele lub presję organizacyjną prowadzącą do systematycznego pomijania działań jakościowych.

*Źródło:* [PR], s. 22-23; [I], s. 15. Rozróżnienie delegowania zadań i odpowiedzialności nadrzędnej jest syntezą tych zasad.

<a id="mccall"></a>

## 3. Model jakości McCalla

Prezentacja: [3.ModelMcCalla.pdf][M]. Pytania dotyczą głównie praktycznych mechanizmów opisanych w drugiej części prezentacji. Rozróżnienia terminologiczne związane z modelem znajdują się także w odpowiedziach 16 i 19.

<a id="pytanie-32"></a>

### 32. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia łatwości użycia?

*Według prezentacji łatwość użycia wspierają:*

- prosty i spójny interfejs, zrozumiałe ikony, nazwy poleceń i etykiety pól;
- prezentowanie danych w formacie i jednostkach odpowiednich dla użytkownika;
- podpowiedzi oraz ograniczenie konieczności zapamiętywania i przeliczania danych;
- informowanie o stanie programu, bieżącym dokumencie i postępie operacji;
- zrozumiałe komunikaty błędów wskazujące przyczynę i możliwe działanie;
- walidacja danych, cofanie zmian i mechanizmy odzyskiwania;
- podgląd dokumentu lub wydruku oraz wygodny dostęp do często używanych operacji.

*Uzupełnienie własne:*

Dobór mechanizmów należy sprawdzać na rzeczywistych zadaniach użytkowników. Sama obecność wielu przycisków czy podpowiedzi nie dowodzi łatwości obsługi.

*Źródło:* [M], s. 17, 21-23, 25-27; [W], s. 14.

<a id="pytanie-33"></a>

### 33. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia łatwości nauki?

*Według prezentacji:*

Naukę programu ułatwiają interfejs zgodny ze znanymi standardami oraz przewidywalne zachowanie. Nowy użytkownik powinien otrzymać informacje o podstawowych możliwościach i mieć dostęp do pomocy oraz podpowiedzi. Przydatne są również szablony, dokumenty przykładowe, demonstracje i samouczek. Sposób obsługi warto dostosować do umiejętności użytkownika.

Chodzi o zmniejszenie wysiłku potrzebnego do przejścia od pierwszego kontaktu z programem do sprawnego wykonywania zadań. Materiał ISO 9126 pokazuje, że można to sprawdzać np. przez pomiar czasu nauki funkcji.

*Źródło:* [M], s. 9, 32; [W], s. 14; [ISO], s. 6, 11.

<a id="pytanie-34"></a>

### 34. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia operatywności?

*Według prezentacji:*

Operatywność ułatwia bieżące wykonywanie pracy i sterowanie programem. Służą jej odpowiednio krótkie sekwencje kroków, menu kontekstowe, przyciski narzędziowe, skróty klawiszowe oraz możliwość dostosowania menu, przycisków i skrótów. Znaczenie mają również podpowiedzi przy wprowadzaniu danych, powtarzanie i grupowanie operacji oraz automatyzacja pracy.

*Przykład własny:*

Doświadczony użytkownik może zaznaczyć wiele rekordów i wykonać na nich jedną operację, zamiast otwierać każdy rekord osobno. Łatwość nauki dotyczy opanowania takiej funkcji, a operatywność jej sprawnego używania.

*Źródło:* [M], s. 9, 17; [ISO], s. 11.

<a id="pytanie-35"></a>

### 35. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia elastyczności w zakresie funkcjonalnym?

*Według prezentacji:*

Rozszerzanie funkcji wspierają rejestrowanie sekwencji działań do ponownego użycia, własne funkcje i skrypty, dodawanie ich wywołań do interfejsu, dodatki (*add-ins*) oraz osadzanie obiektów obsługiwanych przez inne aplikacje. Elastyczność wspierają także modularność, ogólność rozwiązań i możliwość ponownego wykorzystania komponentów.

*Uzupełnienie własne:*

Ważne jest udostępnienie przewidzianych punktów rozszerzeń, tak aby nowa funkcja nie wymagała przebudowy całego systemu. Nie należy mylić rozszerzenia funkcjonalnego ze zmianą ustawień w ramach istniejących funkcji, opisaną w pytaniu 18.

*Źródło:* [M], s. 4, 7-8, 10-11, 20, 24, 33; [W], s. 15.

<a id="pomiary"></a>

## 4. Pomiary w inżynierii oprogramowania

Prezentacja: [4.Pomiary.pdf][P].

<a id="pytanie-38"></a>

### 38. W jaki sposób zapewnić dane do pomiaru procesów w inżynierii oprogramowania?

*Synteza prezentacji:*

Najpierw trzeba określić, czemu mają służyć pomiary, jakie wskaźniki będą potrzebne i jak zbierać dane. Następnie należy przygotować system wspomagający pomiary i sprawdzić go w próbie. Dopiero na tej podstawie można rozpocząć regularne zbieranie, przechowywanie i analizowanie wyników. Dane mogą obejmować pracochłonność, koszty, liczbę defektów, rozmiar produktów pracy i wyniki przeglądów lub testów. Dokumentacja procesu powinna zachowywać raporty problemów, zmian, audytów, inspekcji i testowania.

*Uzupełnienie własne, praktyczna realizacja:*

1. Zdefiniować zdarzenia i jednostki, np. co oznacza „defekt usunięty” oraz od kiedy liczymy czas jego obsługi.
2. Przypisać odpowiedzialność i miejsce rejestracji danych.
3. Wykorzystywać historię zgłoszeń, system kontroli wersji, wyniki automatycznych testów i ewidencję pracy.
4. Powiązać dane z wersją produktu, etapem procesu i warunkami pomiaru.
5. Kontrolować kompletność i porównywalność danych przed wyciągnięciem wniosków.

*Źródło:* [P], s. 2-6; [G], s. 5-12; [I], s. 27. Lista kroków jest własnym uszczegółowieniem materiałów.

<a id="pytanie-39"></a>

### 39. Czy metryki zorientowane na rozmiar kodu są wiarygodne?

*Według prezentacji:*

Są użyteczne, ale mają ograniczenia. Liczbę linii kodu, wyrażoną jako LOC lub tysiące linii KLOC, można stosunkowo łatwo ustalić. Miary te występują w modelach szacowania, a zależności między rozmiarem kodu i innymi cechami były przedmiotem badań. Można obliczać np. liczbę defektów na KLOC, koszt na KLOC lub liczbę KLOC na osobomiesiąc.

Rozmiar zależy jednak od języka i sposobu zapisu. Zwięzły program może otrzymać gorszy wskaźnik „produktywności” niż rozwlekły. Przed rozpoczęciem kodowania LOC trzeba oszacować. Slajdy wskazują też niedopasowanie tych metryk do języków nieproceduralnych.

> **Komentarz własny.** Wiarygodność samego zliczenia linii nie oznacza trafności oceny jakości lub pracy człowieka. Porównanie wymaga wspólnej definicji linii i podobnego kontekstu, w tym zasad traktowania kodu wygenerowanego.
>
> Liczba defektów na KLOC opisuje gęstość wykrytych defektów; nie jest tym samym co częstość awarii podczas eksploatacji, choć slajd 6 nazywa ją „awaryjnością”.

*Źródło:* [P], s. 5-7, 14.

<a id="pytanie-40"></a>

### 40. Czy punkty funkcjonalne rzeczywiście mierzą funkcjonalność systemu?

*Według prezentacji:*

Mierzą umowny rozmiar systemu na podstawie elementów związanych z funkcjami, a nie bezpośrednio jakość ich realizacji. Materiał rozróżnia:

- punkty funkcyjne (*Function Points*): ważone wejścia, wyjścia, zapytania, pliki i interfejsy zewnętrzne, z pokazanym współczynnikiem korekcyjnym;
- punkty funkcjonalne (*Feature Points*): podobne zliczanie z dodatkowym uwzględnieniem algorytmów.

Punkty są mniej zależne od języka programowania niż LOC. Można je również wyznaczać przed napisaniem kodu. Dobór klasy złożoności i wag może jednak zawierać element subiektywny, a zebranie danych bywa trudne.

> **Komentarz własny.** FP nie odpowiadają na pytania, czy funkcje są poprawne, kompletne względem potrzeb, łatwe w obsłudze lub przydatne użytkownikowi. Dwa systemy z podobną liczbą punktów mogą różnić się pod tymi względami. Punkty opisują rozmiar funkcjonalny według przyjętej metody, ale nie stanowią pełnej oceny atrybutu „funkcjonalność”. Nazwy obu odmian zachowano zgodnie ze slajdami.

*Źródło:* [P], s. 8-14; dla znaczenia atrybutu funkcjonalności [W], s. 11.

<a id="pytanie-41"></a>

### 41. Jakie znaczenie mają metryki złożoności oprogramowania?

*Według prezentacji:*

Pozwalają ilościowo opisywać strukturę kodu i wspierać ocenę trudności implementacji oraz utrzymania. Materiał omawia metryki Halsteada, oparte na liczbach operatorów i operandów, oraz złożoność cyklomatyczną McCabe'a, opartą na grafie przepływu sterowania. Podaje też indeks utrzymywalności łączący objętość Halsteada, złożoność cyklomatyczną i LOC.

*Uzupełnienie własne:*

Metryki pomagają wybrać moduły do dokładniejszego przeglądu, testowania lub uproszczenia. Są sygnałem ryzyka, a nie dowodem obecności albo braku błędów.

> **Korekta.** Slajd 20 określa złożoność McCabe'a jako liczbę potencjalnych ścieżek wykonania. Ściślej jest to liczba liniowo niezależnych ścieżek, czyli rozmiar bazy ścieżek grafu. Wszystkich możliwych przebiegów może być znacznie więcej, a przy pętlach nawet nieskończenie wiele.
>
> Dla pojedynczego połączonego grafu przepływu z jednym wejściem i wyjściem stosuje się `V(G) = E - N + 2`, gdzie `E` to liczba krawędzi, a `N` liczba węzłów. Źródło zewnętrzne: [Thomas J. McCabe, A Complexity Measure, 1976, s. 308-309](https://www.cs.du.edu/~snarayan/sada/teaching/COMP3705/lecture/p1/mccabe.pdf).
>
> **Komentarz własny.** Progi ze slajdów oraz wzory Halsteada szacujące czas pracy i liczbę błędów nie powinny być traktowane jako gwarancje. Także sformułowanie, że trudność Halsteada „wyznacza stopień odporności na błędy”, jest zbyt silne: liczby operatorów i operandów same nie wykazują zdolności systemu do tolerowania usterek.

*Źródło prezentacji:* [P], s. 15-21.

<a id="iso9126"></a>

## 4a. Metryki jakości według ISO/IEC 9126

Prezentacja: [4a.ISO-9126.pdf][ISO].

<a id="pytanie-7"></a>

### 7. Czym różni się jakość wewnętrzna oprogramowania od zewnętrznej i użytkowej?

*Według prezentacji są to powiązane perspektywy oceny:*

| Perspektywa | Przedmiot oceny | Przykład własny |
|---|---|---|
| Jakość wewnętrzna | Własności kodu, projektu i dokumentacji; perspektywa projektanta lub programisty | Złożoność modułu, modularność, możliwość prześledzenia wymagań w kodzie |
| Jakość zewnętrzna | Zachowanie działającego produktu, oceniane m.in. przez testy | Czas odpowiedzi, poprawność obliczeń, zachowanie po awarii |
| Jakość użytkowa, czyli jakość w użyciu | Wyniki pracy użytkownika w określonym kontekście | Skuteczność wykonania zadania, czas pracy, satysfakcja i ryzyko szkody |

Potrzeby użytkownika służą określeniu wymagań zewnętrznych, a te są podstawą wymagań wewnętrznych. Jakość wewnętrzna wpływa na zewnętrzną, a zewnętrzna na użytkową. To zależność między perspektywami, a nie automatyczna gwarancja: dobra struktura kodu nie dowodzi jeszcze, że użytkownik osiągnie swój cel.

*Źródło:* [ISO], s. 2-3, 8, 15-19. Przykłady w tabeli są własną ilustracją tych kategorii.

<a id="pytanie-36"></a>

### 36. Jakie jest znaczenie modelu ISO/IEC 9126 w praktyce?

*Według prezentacji:*

Model daje wspólny sposób opisu jakości i pomaga przełożyć ogólne oczekiwania na cechy oraz pomiary. Rozróżnia jakość wewnętrzną, zewnętrzną i użytkową oraz odpowiadające im perspektywy oceny.

W jakości wewnętrznej i zewnętrznej wyróżnia funkcjonalność, niezawodność, użyteczność, efektywność, utrzymywalność i przenośność. W jakości użytkowej obejmuje skuteczność, produktywność, bezpieczeństwo i satysfakcję. Pomaga więc ustalać wymagania, projektować ocenę produktu i porównywać wyniki przy wspólnych kryteriach.

Prezentacja wskazuje również ograniczenia modelu. Zebranie danych do dużej liczby miar może być trudne, a część skal wymaga dodatkowych ustaleń, zanim wynik pomiaru da się przełożyć na ocenę jakości.

> **Kontekst historyczny.** ISO/IEC 9126-1:2001 jest normą wycofaną, zastąpioną przez ISO/IEC 25010:2011. Odpowiedź opisuje historyczny model wymagany w pytaniu; nie należy przedstawiać go jako aktualnej edycji normy. Źródło zewnętrzne: [katalog ISO, ISO/IEC 9126-1:2001](https://www.iso.org/standard/22749.html). Samo wskazanie następcy nie oznacza, że wydanie 25010:2011 pozostaje aktualne.

*Źródło prezentacji:* [ISO], s. 2-3, 8-20, 24. W slajdach *reliability* nazwano „wiarygodnością”; zob. komentarz do pytania 16.

<a id="pytanie-37"></a>

### 37. Skąd zdobyć dane pomiarowe dla metryk wewnętrznych, zewnętrznych i użytkowych w modelu ISO/IEC 9126?

*Według prezentacji:*

| Typ metryki | Źródła danych | Sposób uzyskania |
|---|---|---|
| Wewnętrzna | Specyfikacja, projekt, dokumentacja, kod źródłowy | Przeglądy i analiza cech produktu, porównanie z wymaganiami |
| Zewnętrzna | Wyniki i raporty testów, dokumentacja, kwestionariusze | Uruchamianie programu i obserwowanie jego zachowania w określonych warunkach |
| Użytkowa | Raporty z obserwacji użytkowników, monitoring użycia, kwestionariusze satysfakcji | Obserwowanie realizacji rzeczywistych lub reprezentatywnych zadań |

Na slajdach dokładność obliczeniową ocenia się przez udział funkcji spełniających wymagania dokładności. Łatwość nauki można oceniać na podstawie czasu potrzebnego użytkownikowi na opanowanie funkcji. W ocenie jakości w użyciu bierze się pod uwagę m.in. ukończenie zadań, czas ich wykonania i satysfakcję użytkownika.

*Uzupełnienie własne:*

O typie metryki decyduje przede wszystkim przedmiot oceny. Ten sam raport może zawierać dane przydatne dla kilku perspektyw. Trzeba też zapisać wersję produktu, środowisko, profil użytkowników i definicje liczników oraz mianowników.

*Źródło:* [ISO], s. 2-7, 15-19.

<a id="cmmi"></a>

## 5. Dojrzałość procesu: CMM/CMMI

Prezentacja: [5.CMM-CMMI.pdf][C]. Odpowiedzi odnoszą się do historycznych modeli SW-CMM oraz CMMI 1.1 omawianych w materiale.

<a id="pytanie-44"></a>

### 44. Jak należy rozumieć dojrzałość procesu wytwarzania oprogramowania w sensie CMM/CMMI?

*Według prezentacji:*

Dojrzałość oznacza, że proces jest coraz lepiej zdefiniowany, powtarzalny i konsekwentnie stosowany w organizacji. Polityka organizacji, standardy, procedury, szkolenia i przypisane odpowiedzialności utrwalają ten sposób pracy. Sposób pracy przestaje zależeć wyłącznie od konkretnych osób i może być zachowany po ich odejściu.

Na kolejnych poziomach przechodzi się od działań doraźnych, przez zarządzanie i wspólne standardy, do zarządzania ilościowego i ciągłego doskonalenia. Dzięki temu łatwiej przewidywać koszty, harmonogram i wyniki jakościowe.

> **Komentarz własny.** Dojrzałość dotyczy zdolności organizacji do realizowania i doskonalenia procesów. Nie jest tożsama z bezbłędnością konkretnego produktu. Slajdowe zapewnienia o stałej lub wysokiej jakości należy odczytywać jako oczekiwany efekt dojrzałego procesu, nie bezwarunkową gwarancję każdego projektu.

*Źródło:* [C], s. 4-11, 17-18.

<a id="pytanie-45"></a>

### 45. Który poziom dojrzałości w CMM/CMMI oznacza wprowadzenie procesu zdefiniowanego i na czym to polega?

*Według prezentacji:*

Jest to **poziom 3, „zdefiniowany” (*Defined*)**. Organizacja dokumentuje i standaryzuje procesy zarządcze i inżynierskie oraz integruje je we wspólny proces organizacyjny. Projekty stosują zatwierdzone wersje tego procesu dopasowane do swoich potrzeb, czyli poddane *tailoringowi*.

Obejmuje to m.in. wspólne zasady pracy, szkolenia, koordynację między zespołami i przeglądy wzajemne. Na poziomie 2 nacisk pada na zarządzanie poszczególnymi projektami. Poziom 3 wprowadza dodatkowo spójny standard procesów dla całej organizacji.

*Uzupełnienie własne:*

Proces zdefiniowany musi być rzeczywiście stosowany i utrzymywany. Samo napisanie dokumentacji procesu nie wystarcza. Dopasowanie nie oznacza dowolnego pomijania niewygodnych praktyk.

*Źródło:* [C], s. 7-8, 12, 15-16, 21-22.

<a id="pytanie-46"></a>

### 46. Czym różni się reprezentacja stopniowana CMMI od reprezentacji ciągłej?

*Według prezentacji, s. 20:*

Reprezentacja stopniowana wyznacza kolejne poziomy obejmujące z góry ustalone wymagania dla organizacji. Reprezentacja ciągła pozwala wybierać obszary procesu i poziomy, do których organizacja chce je doprowadzić, zgodnie ze swoimi potrzebami.

> **Korekta.** Slajdy 21 i 22 mają zamienione przyporządkowanie list poziomów do reprezentacji. Dla CMMI 1.1 właściwe rozróżnienie jest następujące:
>
> | Reprezentacja | Co podlega ocenie | Poziomy w omawianej wersji |
> |---|---|---|
> | Stopniowana (*staged*) | Dojrzałość organizacji w określonym zakresie oceny, względem wymaganych zestawów obszarów procesowych | 1 Initial, 2 Managed, 3 Defined, 4 Quantitatively Managed, 5 Optimizing |
> | Ciągła (*continuous*) | Zdolność poszczególnych obszarów procesowych; wynik tworzy profil | 0 Incomplete, 1 Performed, 2 Managed, 3 Defined, 4 Quantitatively Managed, 5 Optimizing |
>
> Nie należy zapamiętywać poziomu 0 i poziomu 1 „wykonywanego” jako skali dojrzałości stopniowanej CMMI 1.1. Nie należy też przenosić tych historycznych skal bez sprawdzenia do innych wydań CMMI. Źródła zewnętrzne: [CMMI Product Team, model 1.1 Continuous Representation](https://doi.org/10.1184/R1/6572141) oraz [Sandra L. Cepeda, CMMI: Staged or Continuous?, 2005, s. 5, 8-9](https://www.sei.cmu.edu/documents/2948/2005_017_001_22691.pdf).

*Przykład własny:*

Organizacja może w reprezentacji ciągłej wybrać poprawę zarządzania wymaganiami i weryfikacji, otrzymując różne oceny obu obszarów. Reprezentacja stopniowana sprawdza zestaw obszarów potrzebny do uzyskania danego poziomu dojrzałości.

*Źródło prezentacji:* [C], s. 20-24, 28.

<a id="iso9001"></a>

## 6. ISO 9000/9001 i zarządzanie jakością

Prezentacja: [6.ISO_9001.pdf][I]. Materiał łączy opis kilku wydań norm, w szczególności ISO 9001:1994 i ISO 9001:2000. Różnicę dotyczącą księgi jakości w ISO 9001:2015 wskazano przy pytaniu 48.

<a id="pytanie-31"></a>

### 31. Jak w praktyce zrealizować w organizacji zasadę TQM „podejmowania decyzji w oparciu o fakty”?

*Według prezentacji:*

Decyzje powinny wynikać z analizy danych i informacji. Trzeba mierzyć procesy i produkty, zachowywać zapisy jakości, analizować wyniki oraz sprawdzać skuteczność działań doskonalących. Wsparciem są audyty, raporty z testów i przeglądów oraz metody statystyczne.

*Uzupełnienie własne:*

Należy określić problem i mierzalny cel, zebrać porównywalne dane, ustalić punkt odniesienia, przeanalizować możliwe przyczyny, wprowadzić zmianę i ponownie wykonać pomiar. Przykładowo przy wzroście liczby reklamacji warto ustalić ich typy, dotkliwość i związek z wersjami produktu, zamiast od razu uznawać, że testerzy pracują gorzej.

> **Komentarz na podstawie GQM.** Współwystępowanie zjawisk nie rozstrzyga kierunku przyczynowości. Slajdy pokazują, że wolniejsze inspekcje mogą ujawniać więcej błędów, ale samo znalezienie wielu błędów również spowalnia inspekcję.

*Źródło:* [I], s. 6, 14, 25, 27; [PR], s. 22; [G], s. 17-19.

<a id="pytanie-47"></a>

### 47. Co oznacza wprowadzenie polityki jakościowej w organizacji wg ISO 9000?

*Według prezentacji:*

Kierownictwo określa i dokumentuje kierunek działania w sprawach jakości, cele oraz związane z nimi obowiązki i uprawnienia. Zapewnia środki, wdraża odpowiednie zasady pracy i okresowo przegląda działanie systemu jakości. Polityka musi wiązać się z potrzebami klienta, planowaniem i doskonaleniem procesów.

*Uzupełnienie własne:*

Praktyczne wdrożenie oznacza przełożenie deklaracji na działania. Jeśli celem jest ograniczenie defektów trafiających do użytkowników, trzeba ustalić sposób ich pomiaru, zakres przeglądów i testów, odpowiedzialnych oraz zasoby. Sam podpisany dokument nie zmienia sposobu pracy.

> **Doprecyzowanie.** „ISO 9000” bywa na slajdach nazwą całej rodziny norm. W wydaniach 2015 norma ISO 9000 opisuje podstawy i terminologię, a ISO 9001 wymagania systemu zarządzania jakością. Źródło zewnętrzne: [ISO/TC 176/SC2, informacje o ISO 9000:2015 i ISO 9001:2015](https://committee.iso.org/sites/tc176sc2/home/projects/published/iso-9001-2015.html).

*Źródło prezentacji:* [I], s. 3, 5-6, 15-16, 22-24.

<a id="pytanie-48"></a>

### 48. Co to jest i co obejmuje księga jakości?

*Według prezentacji:*

Księga jakości (*Quality Manual*) opisuje system zarządzania jakością organizacji i porządkuje odwołania do jego dokumentacji. Przedstawiony przykład obejmuje:

- informacje o organizacji, podstawy normatywne i zakres systemu;
- politykę, cele i zadania jakościowe;
- strukturę organizacyjną, odpowiedzialności i uprawnienia;
- zarządzanie dokumentacją i zapisami;
- odpowiedzialność kierownictwa i zarządzanie zasobami;
- realizację wyrobu, w tym wymagania klienta, projektowanie, zakupy i wytwarzanie;
- pomiary, analizę, nadzór nad niezgodnościami oraz doskonalenie;
- powiązane rejestry, np. reklamacji, działań korygujących, dostawców i audytów.

> **Komentarz własny.** Lista ze slajdów jest przykładem. Nie każdy rejestr musi być fizycznie częścią jednego dokumentu; księga może odsyłać do procedur i zapisów.
>
> **Kontekst historyczny.** Obowiązkowa księga jakości odpowiada starszym wydaniom normy omawianym w materiale. ISO 9001:2015 wymaga określonych udokumentowanych informacji, lecz nie wymaga dokumentu o nazwie „księga jakości”. Może on nadal być użyteczny. Źródło zewnętrzne: [ISO/TC 176/SC2, Guidance on the requirements for Documented Information of ISO 9001:2015, s. 2-3](https://www.iso.org/iso/documented_information.pdf).

*Źródło prezentacji:* [I], s. 16, 22-27.

<a id="pytanie-49"></a>

### 49. Czy wprowadzenie ISO 9001 zapewnia zauważalną poprawę jakości produktów?

*Odpowiedź wynikająca z prezentacji:*

**Samo wprowadzenie ISO 9001 nie gwarantuje poprawy jakości produktów.** Norma porządkuje zarządzanie jakością, odpowiedzialności, procesy, pomiary i doskonalenie. Takie wdrożenie może poprawić powtarzalność i jakość wyników, ale materiał sam stawia pytanie, czy jakość procesu gwarantuje jakość produktów.

*Uzupełnienie własne:*

Poprawa będzie zależeć od tego, czy procesy rozwiązują rzeczywiste problemy i czy organizacja reaguje na wyniki pomiarów. Formalna zgodność dokumentacji bez zmiany praktyki nie daje podstaw do obietnicy zauważalnej poprawy. Trzeba ją wykazać wskaźnikami produktu i użytkowania, np. spadkiem liczby poważnych defektów lub reklamacji, przy porównywalnych warunkach.

> **Doprecyzowanie zewnętrzne.** ISO 9001:2015 dotyczy wymagań wobec systemu zarządzania jakością i zdolności do powtarzalnego dostarczania zgodnych produktów oraz usług. Nie należy utożsamiać tego z dowodem bezbłędności każdego produktu. Źródło: [ISO/TC 176/SC2, zakres ISO 9001:2015](https://committee.iso.org/sites/tc176sc2/home/projects/published/iso-9001-2015.html).

*Źródło prezentacji:* [I], s. 4-6, 11-17, 25, 28-29.

<a id="gqm"></a>

## 7a. Goal-Question-Metrics

Prezentacja: [7a.GQM.pdf][G].

<a id="pytanie-42"></a>

### 42. Jaka jest przewaga metody pomiaru jakości Goal-Question-Metrics w porównaniu do metod klasycznych opartych o drzewo jakości (jak ISO/IEC 9126)?

*Według prezentacji:*

**GQM zaczyna od celów konkretnego przedsięwzięcia**. Następnie formułuje pytania pozwalające ocenić te cele i dobiera metryki, które dostarczą odpowiedzi. Obejmuje planowanie, definiowanie, zbieranie danych oraz interpretację wyników i ocenę kosztów oraz korzyści.

W porównaniu z korzystaniem z szerokiego katalogu cech i miar przewagą jest jawne uzasadnienie każdego pomiaru: wiadomo, jakiej decyzji lub jakiemu usprawnieniu ma służyć. Ogranicza to zbieranie danych tylko dlatego, że łatwo je uzyskać. ISO 9126 w przedstawionej ocenie ma m.in. problem dużej liczby trudnych do zebrania miar.

*Przykład własny:*

- Cel: zmniejszyć liczbę poważnych defektów wykrywanych dopiero przez użytkowników.
- Pytanie: jakie defekty wymykają się przeglądom i testom oraz na którym etapie powstały?
- Metryki: liczba i udział takich defektów według dotkliwości, etapu pochodzenia i etapu wykrycia, przy ustalonym okresie obserwacji.

> **Komentarz własny.** GQM nie zastępuje automatycznie modelu jakości. ISO 9126 może pomóc wybrać cechy i miary, a GQM powiązać je z celem. Źle wybrany cel w GQM może pominąć ważny aspekt jakości, dlatego warto sprawdzać kompletność oceny.

*Źródło:* [G], s. 2-13, 14-19; [ISO], s. 20.

<a id="ahp"></a>

## 7b. Metoda Saaty'ego: Analytic Hierarchy Process

Prezentacja: [7b.AHP.pdf][A].

<a id="pytanie-43"></a>

### 43. Kiedy warto stosować metodę Saaty’ego (Analytic Hierarchy Process) do oceny jakości?

*Według prezentacji:*

AHP jest przydatne przy wyborze spośród kilku alternatyw według wielu kryteriów, zwłaszcza gdy trudno zastosować skalę bezwzględną. Łatwiej ocenić, który z dwóch wariantów jest lepszy pod danym względem lub które kryterium jest ważniejsze, niż od razu nadać oceny wszystkim wariantom.

Tworzy się hierarchię kryteriów, **porównuje je parami** i wyznacza wagi. Następnie porównuje się warianty względem kryteriów i oblicza ocenę łączną. Slajdy używają ocen 1, 3, 5, 7, 9 oraz ich odwrotności; pokazują normalizację kolumn macierzy i uśrednianie wierszy.

Prezentacja zwraca uwagę na subiektywność ocen i możliwość nieprzechodnich porównań. Przyjęta skala liczbowa może też nie odpowiadać temu, jak oceniający intuicyjnie rozumie różnicę między wariantami.

*Uzupełnienie własne:*

Wynik należy rozumieć jako ranking przy przyjętych kryteriach i preferencjach. Warto sprawdzić, czy niewielka zmiana wag zmienia zwycięzcę i czy oceny parami nie są sprzeczne. Warunki obowiązkowe, np. minimalny wymagany poziom bezpieczeństwa, powinny zostać sprawdzone osobno.

> **Korekta rachunkowa.** Na slajdzie 9 macierz wynosi `[[1, 0,2], [5, 1]]`. Zgodnie z pokazaną metodą:
>
> - bezpieczeństwo: `(1/6 + 0,2/1,2)/2 = 1/6 ≈ 0,1667`;
> - ochrona: `(5/6 + 1/1,2)/2 = 5/6 ≈ 0,8333`.
>
> Na slajdzie wpisano odwrotnie: 0,84 dla bezpieczeństwa i 0,16 dla ochrony. Przy tej macierzy większą wagę musi otrzymać ochrona. Błędne wagi wykorzystano również na slajdach 15-16, więc pokazany wynik liczbowy nie jest poprawnym wynikiem tej macierzy. Ponadto między tabelami na s. 15 i 16 zmieniają się zaokrąglone wartości dla programu 3. Korekta wynika z własnego przeliczenia danych prezentacji.

*Źródło:* [A], s. 2-18, szczególnie 4-9 i 15-18.

<a id="agile"></a>

## 8. Jakość w metodykach zwinnych

Prezentacja: [8.Jakość w Agile.pdf][AG]. Znaczna część przykładów dotyczy Extreme Programming (XP). Uwagi o praktykach XP nie muszą opisywać wszystkich podejść zwinnych. Zastrzeżenia do uogólnień autora znajdują się w komentarzach.

<a id="pytanie-50"></a>

### 50. Z jakich powodów sygnatariusze manifestu zwinności odrzucili klasyczne metodyki wytwarzania?

*Według prezentacji:*

Autor wskazuje duży nakład pracy nad dokumentacją i późne dostarczanie działających rezultatów. Problemem była również trudność pełnego określenia wymagań na początku projektu. Podczas implementacji zespół mógł stracić kontakt z klientem, a rozbudowany proces nadal nie dawał pewności co do końcowej jakości.

Proponowaną odpowiedzią były częste dostawy działającego oprogramowania, bliska współpraca z klientem, reagowanie na zmiany, krótkie cykle informacji zwrotnej i doskonalenie sposobu pracy.

> **Korekta.** Słowo „odrzucili” jest zbyt mocne. Manifest nadaje większą wartość ludziom, działającemu oprogramowaniu, współpracy i reagowaniu na zmiany, ale nadal uznaje wartość procesów, narzędzi, dokumentacji, umów i planu. Źródło zewnętrzne: [Manifest programowania zwinnego](https://agilemanifesto.org/iso/pl/manifesto.html).

*Źródło prezentacji:* [AG], s. 2-4.

<a id="pytanie-51"></a>

### 51. Czy motywacje ludzi i zaufanie do nich są wystarczające dla sukcesu projektu informatycznego?

*Odpowiedź wynikająca z prezentacji:*

Nie. Motywacja i zaufanie wymagają uzupełnienia o kompetencje, odpowiednie środowisko pracy, współpracę z klientem, przepływ informacji, standardy inżynierskie, projektowanie i testowanie. Zespół może być zaangażowany, a mimo to realizować błędnie rozpoznane potrzeby albo nie zauważyć istotnego ryzyka.

Materiał wskazuje problemy wynikające z braków wiedzy, rotacji personelu i braku dokumentacji. Potrzebne są szkolenia oraz utrwalanie wiedzy i zasad pracy.

> **Doprecyzowanie zewnętrzne.** Sam Manifest również wymienia odpowiednie wsparcie zespołu, doskonałość techniczną, dobre projektowanie oraz regularne usprawnianie pracy. Nie sprowadza sukcesu wyłącznie do zaufania. Źródło: [Założenia Manifestu Programowania Zwinnego](https://agilemanifesto.org/iso/pl/principles.html).

*Źródło prezentacji:* [AG], s. 3-4, 15-20, 24-25.

<a id="pytanie-52"></a>

### 52. Czy utożsamianie jakości oprogramowania z zadowoleniem klienta w metodykach zwinnych jest słuszne?

*Według prezentacji:*

Zadowolenie klienta jest zbyt wąskim kryterium, aby stanowiło pełną definicję jakości. Klient może być zadowolony z demonstracji, choć produkt nie spełnia potrzeb użytkowników końcowych, wymagań domyślnych, wymagań bezpieczeństwa lub obowiązkowych ograniczeń. Satysfakcja może też zmienić się po dłuższym użytkowaniu i ujawnieniu problemów.

Trzeba uwzględnić wymagania wypowiedziane, niewypowiedziane oraz jeszcze nierozpoznane, a także rzeczywiste zastosowanie produktu. Zadowolenie jest jednym z aspektów jakości, obok m.in. funkcjonalności i wiarygodności.

> **Komentarz własny.** Przyznanie satysfakcji klienta wysokiego priorytetu nie oznacza, że jest ona jedynym kryterium jakości. Sama deklaracja „klient tak chciał” nie zwalnia zespołu z analizy skutków i ograniczeń rozwiązania.

*Źródło:* [AG], s. 6-8, 13, 24; [W], s. 7, 10-15; [ISO], s. 15-19.

<a id="pytanie-53"></a>

### 53. Jakie są podstawowe warunki zapewnienia jakości oprogramowania w metodykach zwinnych?

*Według prezentacji, s. 24:*

1. Dobra, codzienna współpraca z klientami i użytkownikami końcowymi przez cały proces.
2. Cele wydań wynikające z rzeczywistych wymagań, a nie wyłącznie z opowieści użytkownika.
3. Dobry przepływ informacji w zespole i między zainteresowanymi stronami; częsty kontakt, gdy bezpośrednia współpraca jest niemożliwa.
4. Znajomość i stosowanie standardów pracy inżynierskiej.
5. Rygorystyczne testy jednostkowe przed opublikowaniem każdego wydania.
6. Testy akceptacyjne wydań z udziałem wybranych użytkowników przed rozpowszechnieniem.

Materiał wskazuje ponadto praktyki wspierające te warunki: standardy kodowania, refaktoryzację, częstą integrację, testy regresyjne oraz poprawianie procesu.

*Uzupełnienie zewnętrzne:*

W Scrumie wymagania jakościowe przyrostu ujmuje Definition of Done. Niespełniający jej element nie jest ukończonym przyrostem. Źródło: [Schwaber i Sutherland, Scrum Guide 2020, Definition of Done](https://scrumguides.org/scrum-guide.html#commitment-definition-of-done).

*Źródło prezentacji:* [AG], s. 9, 24.

<a id="pytanie-54"></a>

### 54. W jaki sposób problemy z klientem w metodykach zwinnych mogą wpłynąć negatywnie na jakość produktu?

*Według prezentacji:*

Brak kontaktu i zaangażowania utrudnia zbieranie wymagań, wyjaśnianie szczegółów i ustalanie priorytetów. Brak informacji zwrotnej po wydaniu opóźnia wykrycie rozbieżności. Zespół może czekać na decyzje albo realizować niepotwierdzone założenia, co obniża wydajność i zwiększa ryzyko niepowodzenia.

*Synteza własna:*

W takich warunkach zespół może zbudować niewłaściwe funkcje lub pominąć ważne scenariusze. Kiedy rozbieżności zostaną w końcu zauważone, poprawki mogą wymagać pracy pod presją czasu. Brak udziału użytkowników w akceptacji może pozwolić, by błędy zastosowania ujawniły się dopiero po wdrożeniu.

*Źródło:* [AG], s. 10-14, 23-24.

<a id="pytanie-55"></a>

### 55. Skąd mogą wynikać problemy z klientem w metodykach zwinnych?

*Według prezentacji przyczynami są:*

- niezrozumienie roli klienta w pracy zwinnej i sceptycyzm wobec tego sposobu pracy;
- odległość, różne strefy czasowe i trudności komunikacyjne;
- niski priorytet projektu po stronie klienta oraz brak czasu i zaangażowania;
- przywiązanie dużej organizacji do tradycyjnego trybu pracy i kontraktowania;
- niedostateczna wiedza lub brak uprawnień decyzyjnych przedstawiciela;
- rozbieżność między oczekiwaniami przedstawiciela a potrzebami użytkowników końcowych.

> **Komentarz własny.** Slajd 10 sugeruje, że z góry ustalone wynagrodzenie odbiera klientowi motywację finansową do współpracy. To możliwy problem konstrukcji umowy, ale nie reguła. Także przy stałej cenie klient ponosi skutki opóźnienia lub otrzymania nieprzydatnego produktu.

*Źródło:* [AG], s. 10, 13, 15.

<a id="pytanie-56"></a>

### 56. Jak firmy stosujące metodyki zwinne sobie radzą przy problemach z klientem?

*Według prezentacji stosują m.in.:*

- wyjaśnianie klientowi sposobu współpracy i korzyści z częstej informacji zwrotnej;
- różne opcje kontraktowe, np. finansowanie kolejnych wydań i możliwość zmiany zakresu;
- margines czasowy oraz wcześniejszą ocenę ryzyka braku zaangażowania;
- odkładanie opowieści czekających na wyjaśnienia i sprawdzanie ich gotowości do implementacji;
- przypisywanie właścicieli konkretnym opowieściom;
- zastępczego przedstawiciela klienta, np. analityka biznesowego;
- regularne demonstracje działającego produktu.

Slajd wymienia również ukrywanie zwinnego sposobu pracy przed klientem.

> **Komentarz własny.** Nie traktowałbym ukrywania istotnych zasad współpracy jako zalecenia. Wewnętrzne techniki organizacji pracy mogą być sprawą wykonawcy, ale warunki podejmowania decyzji, odbioru i zmian zakresu powinny być jasne. Przedstawiciel zastępczy pomaga tylko wtedy, gdy ma dostęp do wiedzy i decyzji klienta.
>
> **Doprecyzowanie zewnętrzne.** Product Owner w Scrumie odpowiada za wartość produktu i zarządzanie Product Backlogiem. Może reprezentować potrzeby wielu interesariuszy; nie musi być tożsamy z klientem kontraktowym ani wszystkimi użytkownikami. Źródło: [Scrum Guide 2020, Product Owner](https://scrumguides.org/scrum-guide.html#product-owner).

*Źródło prezentacji:* [AG], s. 12-13.

<a id="pytanie-57"></a>

### 57. Jak należy rozumieć formułowanie celów wydań na podstawie rzeczywistych wymagań klientów, a nie tylko ich opowieści?

*Według prezentacji:*

Opowieści użytkownika są z założenia niepełne i wymagają doprecyzowania. Mogą pomijać wymagania niefunkcjonalne, sytuacje wyjątkowe lub potrzeby użytkowników innych niż przedstawiciel klienta. Cel wydania powinien wynikać z tego, co użytkownik rzeczywiście musi osiągnąć i w jakich warunkach.

*Uzupełnienie własne:*

Przed realizacją trzeba ustalić wynik biznesowy, zainteresowane grupy użytkowników, reguły działania, ograniczenia, przypadki błędne oraz sprawdzalne kryteria akceptacji. Opowieść jest początkiem rozmowy o wymaganiach, a nie dowodem ich kompletności.

*Przykład własny:*

Prośbę „chcę eksportować raport” trzeba uzupełnić m.in. o odbiorcę raportu, wymagane dane i format, zakres uprawnień, dopuszczalny czas generowania oraz zachowanie przy braku danych. Dopiero wtedy da się ocenić, czy wydanie rozwiązuje właściwy problem.

*Źródło:* [AG], s. 7, 12-13, 23-24; [I], s. 19-20, 27.

<a id="pytanie-58"></a>

### 58. Jak zapewnić znajomość i stosowanie odpowiednich standardów pracy inżynierskiej w zespole zwinnym?

*Według prezentacji:*

Nie wolno zakładać, że wysokie wynagrodzenie lub doświadczenie części zespołu zapewnia wszystkim odpowiednie kompetencje. Potrzebne są szkolenia, standardy kodowania, współpraca, przeglądy, właściwe projektowanie, integracja i testowanie.

*Uzupełnienie własne:*

Standardy powinny być konkretne, dostępne i sprawdzane w codziennej pracy. Można wykorzystać przykłady dobrego kodu, wdrożenie nowych osób, mentoring, przeglądy zmian oraz automatyczne kontrole formatowania, analizy statycznej i testów.

Warto też utrwalać decyzje projektowe, aby wiedza nie znikała wraz z pracownikiem.

> **Komentarz własny.** Slajdy 16 i 20 kategorycznie określają programowanie w parach jako nieefektywne finansowo, a slajd 20 także jako niestosowane w praktyce. Prezentacja nie podaje danych uzasadniających taki ogólny wniosek. Ocenę tej praktyki należy oprzeć na wynikach w danym zespole, uwzględniając czas pracy, jakość i przekazywanie wiedzy, zamiast automatycznie zakładać jej opłacalność lub nieopłacalność.

*Źródło:* [AG], s. 9, 16, 19-20, 24; [PR], s. 24.

<a id="pytanie-59"></a>

### 59. Czy rygorystyczne testowanie w metodykach zwinnych jest wystarczające dla zapewnienia jakości oprogramowania?

*Według prezentacji:*

Nie. Testy mogą sprawdzać niepełne lub błędnie rozpoznane wymagania. Program może przechodzić testy i nadal nie odpowiadać potrzebom użytkownika. Trudno też sprawdzić wszystkie możliwe przebiegi programu i warunki użycia. Potrzebne są analiza wymagań i wyjątków, projektowanie, przeglądy, standardy oraz udział użytkowników w akceptacji.

> **Korekta i komentarz własny.** Slajd 21 przedstawia możliwość napisania bezbłędnego kodu dzięki TDD jako założenie, a slajd 22 łączy pokrycie kodu z pokryciem wszystkich ścieżek. Należy rozdzielić trzy kwestie:
>
> - spełnienie napisanych testów nie dowodzi spełnienia wszystkich potrzeb i warunków;
> - 100% pokrycia instrukcji albo gałęzi może być osiągalne w określonym kodzie, ale nie oznacza sprawdzenia wszystkich danych i przebiegów;
> - niezależna ocena testów może ujawnić przeoczenia autora, lecz z tego nie wynika, że każdy test jednostkowy musi być pisany lub uruchamiany przez inną osobę.
>
> Podstawa rozróżnienia ścieżek: [McCabe, A Complexity Measure, 1976, s. 308-309](https://www.cs.du.edu/~snarayan/sada/teaching/COMP3705/lecture/p1/mccabe.pdf). Pozostałe zastrzeżenia są własną oceną logiczną zakresu wniosków, jakie można wyprowadzić z testów.

*Źródło prezentacji:* [AG], s. 21-25; [T], s. 21.

<a id="pytanie-60"></a>

### 60. Kto powinien przeprowadzać testy akceptacyjne w metodykach zwinnych i jak się to ma do realiów?

*Według prezentacji:*

Klient powinien odpowiadać za **warunki akceptacji i ocenę wyników**, a wybrani użytkownicy powinni uczestniczyć w testach wydań przed rozpowszechnieniem. Pozwala to sprawdzić rzeczywiste zastosowania produktu.

W praktyce opisanej na slajdach testy bywają przygotowywane, wykonywane i oceniane przez testerów wykonawcy. Użytkownicy sprawdzają tylko wybrane działania, nie testują regularnie i zwykle zakładają, że wcześniej działające funkcje nadal działają. Wtedy część problemów ujawnia się dopiero w eksploatacji.

*Uzupełnienie własne:*

Należy odróżnić techniczne wykonanie testów od decyzji o akceptacji. Testerzy mogą przygotować i zautomatyzować testy, ale kryteria i ocenę przydatności trzeba uzgodnić z uprawnionym przedstawicielem klienta oraz reprezentatywnymi użytkownikami. Regresję powinien systematycznie zapewniać proces wytwarzania, a nie przypadkowe sprawdzanie przez klienta.

*Źródło:* [AG], s. 9, 23-24; [PR], s. 24.

<a id="pytanie-61"></a>

### 61. Dla jakich projektów informatycznych metodyki zwinne się nie nadają (przykłady)?

*Według prezentacji:*

Autor wiąże metodyki zwinne przede wszystkim z prostymi projektami, małymi i skoncentrowanymi organizacjami, niskim ryzykiem oraz możliwością stałego utrzymywania produktu. Ostrzega przed takim podejściem w projektach złożonych i wysokiego ryzyka, zwłaszcza gdy potrzebna jest trwała dokumentacja lub współpraca jest utrudniona.

*Przykłady własne ilustrujące te ograniczenia:*

- sterowanie aparatem do radioterapii lub funkcjami krytycznymi samolotu, jeśli sposób pracy nie zapewnia analizy zagrożeń, wymaganej weryfikacji i dowodów bezpieczeństwa;
- oprogramowanie sondy kosmicznej z bardzo ograniczoną możliwością aktualizacji po uruchomieniu;
- projekt dla niedostępnego decyzyjnie klienta, gdy zespół ma wyłącznie ogólne opowieści i nie może wyjaśniać wymagań;
- system utrzymywany przez wiele lat przez zmieniające się zespoły, jeśli wiedza pozostaje wyłącznie w głowach autorów.

> **Komentarz własny.** Nie zgadzam się z ogólnym wnioskiem, że sama zwinność wyklucza projekty duże lub krytyczne. Powyższe przykłady pokazują niewystarczalność procesu pozbawionego potrzebnych zabezpieczeń i dokumentacji. Można łączyć iteracyjny rozwój z formalną analizą, kontrolą zmian, dokumentacją i niezależną weryfikacją.
>
> O wyborze powinny decydować wymagania projektu i wykazana skuteczność procesu. Jest to moje doprecyzowanie, a nie twierdzenie ze slajdu ani potwierdzenie zgodności konkretnego projektu z normami branżowymi.

*Źródło prezentacji:* [AG], s. 16-17, 24-26; kontekst bezpieczeństwa: [T], s. 19-21.

<a id="pytanie-62"></a>

### 62. Jakie są wady/zagrożenia dla procesu wytwarzania w metodykach zwinnych?

*Według prezentacji:*

- silne uzależnienie od ludzi i stabilności składu zespołu;
- utrata wiedzy przy rotacji personelu oraz trudność wznowienia prac przy braku dokumentacji;
- pominięcie wymagań niefunkcjonalnych i sytuacji wyjątkowych;
- problemy współpracy z klientem i brak wiarygodnej informacji zwrotnej;
- narastanie długu technicznego pod presją kolejnych iteracji;
- wzrost kosztów wskutek ciągłych zmian;
- trudności komunikacji w zespołach rozproszonych;
- niewystarczające testy oraz przeniesienie faktycznego sprawdzania produktu na użytkowników.

> **Korekta.** Są to zagrożenia sposobu realizacji projektu, a nie nieuchronne skutki każdej metody zwinnej. Manifest nie wymaga braku dokumentacji. Scrum Guide mówi, że jakość nie powinna spadać podczas Sprintu, a nieukończona praca nie spełnia Definition of Done. Presja terminu nie jest więc uzasadnieniem nazywania wadliwego przyrostu ukończonym. Źródła zewnętrzne: [Manifest](https://agilemanifesto.org/iso/pl/manifesto.html), [Scrum Guide 2020, Sprint](https://scrumguides.org/scrum-guide.html#the-sprint) i [Definition of Done](https://scrumguides.org/scrum-guide.html#commitment-definition-of-done).

*Uzupełnienie własne:*

Ryzyko ograniczają utrwalanie potrzebnej wiedzy, sprawdzalne wymagania jakościowe, kontrola zmian, utrzymywanie testów regresyjnych i planowanie prac technicznych obok funkcjonalnych.

*Źródło prezentacji:* [AG], s. 10-16, 19-26.

## Materiały źródłowe

### Przekazane pliki

Wszystkie prezentacje są autorstwa Jarosława Kuchty. Skróty w odsyłaczach pozwalają rozróżnić źródła w pytaniach korzystających z kilku prezentacji.

| Skrót | Plik | Liczba stron |
|---|---|---:|
| PYT | [Pytania do samosprawdzenia.pdf][PYT] | 3 |
| W | [1.Wprowadzenie.pdf][W] | 26 |
| T | [1a.StudiumPrzypadku.pdf][T] | 22 |
| PR | [2.JakoscWProcesie.pdf][PR] | 25 |
| M | [3.ModelMcCalla.pdf][M] | 39 |
| P | [4.Pomiary.pdf][P] | 23 |
| ISO | [4a.ISO-9126.pdf][ISO] | 24 |
| C | [5.CMM-CMMI.pdf][C] | 28 |
| I | [6.ISO_9001.pdf][I] | 29 |
| G | [7a.GQM.pdf][G] | 20 |
| A | [7b.AHP.pdf][A] | 19 |
| AG | [8.Jakość w Agile.pdf][AG] | 27 |

### Źródła zewnętrzne użyte w komentarzach

1. [seL4, Verification](https://sel4.systems/Verification/). Zakres formalnych dowodów i ich założenia; pytanie 3.
2. [Nancy Leveson, opis wypadków Therac-25](https://www.cse.msu.edu/~cse435/Handouts/Therac25-Leveson.pdf). Mechanizm przepełnienia `Class3`; pytanie 4.
3. [Thomas J. McCabe, A Complexity Measure, IEEE Transactions on Software Engineering, 1976](https://www.cs.du.edu/~snarayan/sada/teaching/COMP3705/lecture/p1/mccabe.pdf). Znaczenie złożoności cyklomatycznej i niezależnych ścieżek; pytania 41 i 59.
4. [ISO, karta ISO/IEC 9126-1:2001](https://www.iso.org/standard/22749.html). Status normy i jej następca; pytanie 36.
5. [CMMI Product Team, CMMI Version 1.1, Continuous Representation, 2002](https://doi.org/10.1184/R1/6572141) oraz [Sandra L. Cepeda, CMMI: Staged or Continuous?, 2005](https://www.sei.cmu.edu/documents/2948/2005_017_001_22691.pdf). Przedmiot oceny i skale reprezentacji; pytanie 46.
6. [ISO/TC 176/SC2, ISO 9001:2015 oraz ISO 9000:2015](https://committee.iso.org/sites/tc176sc2/home/projects/published/iso-9001-2015.html). Zakres i rola norm; pytania 47 i 49.
7. [ISO/TC 176/SC2, Guidance on the requirements for Documented Information of ISO 9001:2015](https://www.iso.org/iso/documented_information.pdf). Status księgi jakości w wydaniu 2015; pytanie 48.
8. [Manifest programowania zwinnego](https://agilemanifesto.org/iso/pl/manifesto.html) oraz [jego zasady](https://agilemanifesto.org/iso/pl/principles.html). Priorytety i zakres założeń Agile; pytania 50, 51 i 62.
9. [Ken Schwaber, Jeff Sutherland, Scrum Guide 2020](https://scrumguides.org/scrum-guide.html). Product Owner, jakość w Sprincie i Definition of Done; pytania 53, 56 i 62.

[PYT]: <Pytania do samosprawdzenia.pdf>
[W]: <1.Wprowadzenie.pdf>
[T]: <1a.StudiumPrzypadku.pdf>
[PR]: <2.JakoscWProcesie.pdf>
[M]: <3.ModelMcCalla.pdf>
[P]: <4.Pomiary.pdf>
[ISO]: <4a.ISO-9126.pdf>
[C]: <5.CMM-CMMI.pdf>
[I]: <6.ISO_9001.pdf>
[G]: <7a.GQM.pdf>
[A]: <7b.AHP.pdf>
[AG]: <8.Jakość w Agile.pdf>
