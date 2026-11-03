# Jakość systemów informatycznych: powtórka przed egzaminem

Krótkie odpowiedzi na 62 pytania do samosprawdzenia, gotowe do zapisania na egzaminie. Zachowano treść pytań, numerację i podział na działy. Wyjaśnienia, przykłady, komentarze do nieścisłości i numery stron są dostępne w [pełnym opracowaniu](Odpowiedzi_do_samosprawdzenia.md).

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

Główne źródło: [1.Wprowadzenie.pdf](1.Wprowadzenie.pdf).

<a id="pytanie-1"></a>

### 1. Jaki jest wpływ jakości oprogramowania na jakość systemu informatycznego w porównaniu z innymi elementami (np. sprzęt, ludzie, organizacja)?

Jakość systemu informatycznego zależy od **współdziałania** oprogramowania, sprzętu, ludzi, procesów, procedur i danych.

- Nawet poprawny program może dawać niewłaściwe wyniki przy **błędnych danych**, niesprawnym sprzęcie lub złej organizacji pracy.
- Znaczenie poszczególnych elementów **zależy od zastosowania** systemu. Nie można przypisać im stałych udziałów procentowych.

<a id="pytanie-2"></a>

### 2. Czy u źródeł każdej awarii systemu informatycznego stoi błąd programistów?

**Nie każda awaria wynika z błędu programisty.**

- Jej przyczyną mogą być błędne wymagania, wadliwy projekt, niesprawny sprzęt, nieprawidłowe dane, błędy obsługi lub niewłaściwa organizacja pracy.
- Często kilka takich przyczyn występuje jednocześnie.

**Sam defekt** nie musi prowadzić do awarii. Ujawnia się dopiero w określonych warunkach, a zabezpieczenia mogą powstrzymać jego skutki.

<a id="pytanie-3"></a>

### 3. Dlaczego wytwórcy oprogramowania nie mogą zagwarantować 100% bezbłędności swojego produktu?

- Ze względu na złożoność oprogramowania nie da się w praktyce sprawdzić **wszystkich kombinacji** danych, stanów i warunków działania.
- Błędy mogą też występować w wymaganiach i **specyfikacji**.
- Testy potwierdzają poprawność **tylko w sprawdzonych przypadkach**.

**Dowody formalne** mogą potwierdzić określone własności programu przy przyjętych założeniach. Nie dają jednak bezwarunkowej gwarancji poprawności całego systemu.

<a id="pytanie-5"></a>

### 5. Dlaczego rozumienie jakości oprogramowania jako stopnia spełnienia wyspecyfikowanych wymagań jest niewystarczająca?

- Specyfikacja może być **niepełna, błędna** lub nie odpowiadać rzeczywistym potrzebom użytkowników.
- Jakość obejmuje także wymagania domyślne i obowiązkowe, oczekiwania użytkowników oraz **przydatność produktu w użyciu**.

Program może więc spełniać zapisane wymagania, a mimo to nie rozwiązywać właściwego problemu.

<a id="pytanie-6"></a>

### 6. Dlaczego przy zbieraniu wymagań dla oprogramowania nie wystarczy o nie pytać przedstawiciela klienta?

**Przedstawiciel klienta** może nie znać potrzeb wszystkich użytkowników, pomijać wymagania uznawane za oczywiste albo nie mieć uprawnień do podejmowania decyzji.

- Dlatego trzeba rozmawiać z **różnymi grupami interesariuszy**, obserwować rzeczywistą pracę i analizować sytuacje wyjątkowe.
- **Prototypy** i wspólne przeglądy pomagają sprawdzić, czy wymagania odpowiadają potrzebom użytkowników.

<a id="pytanie-8"></a>

### 8. Z jakich elementów składa się model „drzewa” jakości?

**Korzeniem drzewa** jest ogólna jakość.

- Niżej znajdują się **główne atrybuty**, ich szczegółowe cechy oraz metryki i pomiary służące do oceny.
- Przykładowe główne atrybuty to funkcjonalność, wydajność, wiarygodność, satysfakcja i elastyczność.

**Wagi** określają znaczenie poszczególnych składowych. Ocenę można obliczyć ze wzoru `A = Σ(w·M)/Σw`, pod warunkiem że suma wag jest dodatnia.

Podział na atrybuty zależy od przyjętego modelu jakości.

<a id="pytanie-9"></a>

### 9. Co to są atrybuty jakości i jak się mają do wymagań?

**Atrybut jakości** opisuje cechę produktu, a **wymaganie** określa oczekiwany poziom tej cechy w danych warunkach.

Wymagania funkcjonalne wiążą się z funkcjonalnością, czasowe z wydajnością, niezawodnościowe z wiarygodnością, a ograniczenia mogą dotyczyć elastyczności.

Przykładowo wydajność jest atrybutem, a „95% odpowiedzi poniżej 2 s przy 100 użytkownikach” to wymaganie. Jego spełnienie można sprawdzić za pomocą pomiaru.

<a id="pytanie-10"></a>

### 10. Czy dla każdego atrybutu jakości można wyznaczyć metrykę?

Dla wielu atrybutów jakości można wyznaczyć metryki, ale **nie zawsze istnieje jedna obiektywna metryka, która w pełni opisuje daną cechę**.

Przykładowo **wydajność systemu** można oceniać przez:

- **czas odpowiedzi**, czyli czas oczekiwania na wynik;
- **przepustowość**, czyli liczbę żądań obsługiwanych w jednostce czasu;
- **zużycie zasobów**, np. pamięci i procesora.

Przy każdym pomiarze trzeba określić warunki, np. liczbę jednoczesnych użytkowników. Do oceny wydajności może więc być potrzebny zestaw metryk.

Cechy trudniejsze do zmierzenia, np. satysfakcję użytkownika, można oceniać za pomocą wskaźników pośrednich, ankiet lub ocen eksperckich. Trzeba jednak znać ograniczenia tych metod. **Wyrażenie subiektywnej oceny liczbą nie czyni jej obiektywną**.

<a id="pytanie-11"></a>

### 11. Czym różnią się metryki jakościowe od miar?

**Metryka** określa, jaką cechę jakości oceniamy i jak wyrażamy jej ocenę. **Miara** wiąże tę ocenę ze sposobem pomiaru, skalą lub jednostką.

Przykładowo kompletność można ocenić, dzieląc liczbę zrealizowanych funkcji przez liczbę funkcji wymaganych.

- Należy odróżniać samą cechę, definicję wskaźnika, procedurę pomiaru i otrzymany wynik.
- Metryki nie muszą mieć skali `[0,1]`; mogą być wyrażone np. czasem.

<a id="pytanie-12"></a>

### 12. Jakie problemy występują przy pomiarach jakości?

- Jakość obejmuje **wiele cech**, które trudno sprowadzić do jednej liczby.
- Pomiary utrudniają **subiektywność ocen**, brak punktu odniesienia, problemy z normalizacją wyników, arbitralny dobór wag oraz koszt zbierania danych.
- Wyniki mogą być trudne do **interpretacji**.
- Długie ankiety obniżają **rzetelność odpowiedzi**, a pytania tak/nie ułatwiają obliczenia, lecz nie zapewniają obiektywności oceny.

<a id="pytanie-13"></a>

### 13. Czy zawsze wyniki pomiarów uśrednia się wg średniej arytmetycznej?

**Nie zawsze stosuje się zwykłą średnią arytmetyczną.**

- Sposób łączenia wyników zależy od rodzaju danych i celu oceny.
- Można stosować **średnią ważoną**, a przy czasach odpowiedzi także medianę i percentyle.

Przy łączeniu odsetków trzeba uwzględniać **liczbę prób**: wyniki `1/1` i `1/9` dają łącznie `2/10 = 20%`. Zwykła średnia tych dwóch odsetków nie opisuje łącznej skuteczności.

<a id="pytanie-14"></a>

### 14. Czy zawsze miary się przelicza na metryki wg skali liniowej?

**Przeliczenie nie musi być liniowe.**

- Sposób przeliczenia wyniku pomiaru na ocenę jakości powinien odpowiadać wymaganiom.
- Zależność może być **liniowa, progowa lub odcinkowa**.

Na przykład przekroczenie dopuszczalnego czasu reakcji może oznaczać niespełnienie wymagania, nawet jeśli pozostałe cechy uzyskały dobre oceny.

Trzeba również ustalić, czy lepsza jest większa, czy mniejsza wartość wskaźnika.

<a id="pytanie-15"></a>

### 15. Co daje ocena jakości z użyciem modelu drzewa?

Model drzewa dzieli ogólne pojęcie jakości na **konkretne cechy** i wiąże je z pomiarami.

- Umożliwia **ustalanie wag**, porównywanie produktów według wspólnych kryteriów oraz wskazywanie słabych stron.
- Wynik zależy jednak od modelu i wag.

Ocena łączna może ukryć **krytyczną słabość**, dlatego należy zachować oceny składowe i osobno sprawdzać wymagania obowiązkowe.

<a id="pytanie-16"></a>

### 16. Czym różni się wiarygodność systemu informatycznego od jego niezawodności?

- **Wiarygodność** (dependability) oznacza stopień zaufania do systemu. Obejmuje niezawodność, odporność na błędy, bezpieczeństwo, ochronę i testowalność.
- **Niezawodność** (reliability) dotyczy działania bez awarii i zachowania ciągłości usług.

Niezawodność jest więc częścią wiarygodności. System może działać nieprzerwanie, a mimo to być niebezpieczny lub ujawniać dane osobom nieuprawnionym.

<a id="pytanie-17"></a>

### 17. Czym różni się bezpieczeństwo systemu informatycznego od jego ochrony?

- **Bezpieczeństwo** (safety) oznacza zapobieganie szkodom, które system może wyrządzić ludziom i otoczeniu.
- **Ochrona** (security) dotyczy zabezpieczenia systemu i informacji przed nieuprawnionym dostępem i działaniem, przy zachowaniu dostępu dla osób uprawnionych.

Niedopuszczenie do podania nadmiernej dawki promieniowania jest przykładem bezpieczeństwa. Zablokowanie nieuprawnionej zmiany tej dawki jest przykładem ochrony.

Kontrola dostępu jest tylko jednym z mechanizmów ochrony.

<a id="pytanie-18"></a>

### 18. Czym różni się konfigurowalność systemu informatycznego od jego modyfikowalności?

- **Konfigurowalność** oznacza łatwość dostosowania istniejących możliwości systemu bez zmiany jego funkcji.
- **Modyfikowalność** to łatwość zmieniania lub dodawania funkcji.

Wybór języka interfejsu jest konfiguracją, natomiast dodanie nowego algorytmu naliczania opłat wymaga modyfikacji systemu.

<a id="pytanie-19"></a>

### 19. Czym różni się łatwość testowania systemu informatycznego od łatwości śledzenia?

- **Łatwość testowania** oznacza łatwość przygotowania i wykonania sprawdzeń poprawności oraz wykrywania błędów.
- **Łatwość śledzenia** oznacza, że działanie systemu można łatwo odtworzyć i zrozumieć, np. na podstawie logów.

W modelu McCalla **traceability** oznacza także możliwość powiązania wymagań z implementacją.

Takie powiązania i informacje o wykonaniu wspierają testowanie, ale go nie zastępują.

<a id="studium"></a>

## 1a. Studium przypadku: Therac-25

Główne źródło: [1a.StudiumPrzypadku.pdf](1a.StudiumPrzypadku.pdf).

<a id="pytanie-4"></a>

### 4. Jakie były źródłowe przyczyny wypadków z systemem do radioterapii Therac-25 w połowie lat ’80 XX wieku w USA i Kanadzie (błędy użytkowników, programistów, konstruktorów, projektantów)?

Wypadki Therac-25 wynikały z połączenia błędów konstrukcyjnych, programistycznych i organizacyjnych.

- Usunięto część niezależnych **blokad sprzętowych** i nadmiernie zaufano programowi.
- Występowały błędy **współbieżności i synchronizacji**. Dodatkowo przepełnienie zmiennej `Class3` co 256 przebiegów mogło pozwolić na pominięcie kontroli kolimatora.
- Ryzyko zwiększały **niejasne komunikaty**, mylące wskazania dawki i możliwość ponawiania zabiegu. Testy i analiza bezpieczeństwa były niewystarczające, a reakcje na wcześniejsze wypadki niewłaściwe.

Działanie operatora mogło uruchomić wadliwy scenariusz, lecz **przyczyny były systemowe**.

<a id="proces"></a>

## 2. Jakość w procesie wytwarzania

Główne źródło: [2.JakoscWProcesie.pdf](2.JakoscWProcesie.pdf).

<a id="pytanie-20"></a>

### 20. Dlaczego o jakość oprogramowania warto dbać od samego początku projektu?

- Błędy wymagań i projektu mogą przechodzić do kodu oraz testów i powodować **kolejne defekty**.
- Im później zostaną wykryte, tym więcej zależnych elementów trzeba poprawić i tym większy jest **koszt naprawy**.

**Wczesne przeglądy**, uzgodnienia wymagań i kontrola projektu ograniczają rozprzestrzenianie się błędów oraz liczbę defektów pozostających w gotowym produkcie.

<a id="pytanie-21"></a>

### 21. Jak wygląda kosztowność zmian w różnych fazach cyklu życia oprogramowania?

**Koszt zmian** zwykle rośnie wraz z przechodzeniem od definiowania, przez opracowywanie, do utrzymywania oprogramowania.

Przykładowa **proporcja względnych kosztów** to `1 : 10 : 100`.

- **Późna zmiana** wymaga poprawienia większej liczby zależnych elementów. Konieczne są też testy regresyjne, wdrożenie poprawki, a czasem migracja danych.
- Dokładne proporcje zależą od projektu i rodzaju zmiany.

<a id="pytanie-22"></a>

### 22. Co to jest i co daje model wzmocnienia defektów?

**Model wzmocnienia defektów** opisuje, jak defekty przechodzą między etapami wytwarzania. Uwzględnia defekty odziedziczone bez zmian, defekty powodujące kolejne błędy, defekty nowo wprowadzone oraz te usuwane dzięki kontroli.

Pozwala porównywać **skuteczność i koszty** kontroli prowadzonej na różnych etapach.

W przykładowym obliczeniu kontrola dopiero podczas testów pozostawia 12 błędów przy koszcie 2177. Kontrola prowadzona w całym procesie pozostawia 3 błędy przy koszcie 693.

Wczesne wykrywanie ogranicza wzmocnienie defektów i koszt ich usuwania.

<a id="pytanie-23"></a>

### 23. Dlaczego tradycyjna kontrola jakości produktu zawodzi w przypadku oprogramowania?

- Kontrola gotowego produktu **wykrywa błędy późno**, gdy wadliwe wymagania i decyzje projektowe wpłynęły już na wiele elementów.
- W oprogramowaniu defekt jest **powielany w kolejnych kopiach**, więc odrzucenie wadliwej kopii nie usuwa jego przyczyny.

Usunięcie przyczyny wymaga poprawienia wymagań, projektu lub kodu.

Zapewnianie jakości powinno obejmować **cały proces wytwarzania**, a testy końcowe powinny być jednym z działań jakościowych.

<a id="pytanie-24"></a>

### 24. Na czym polega polityka zapewniania jakości oprogramowania (SQA) w organizacji?

**SQA** (Software Quality Assurance) obejmuje planowe i systematyczne działania służące zapewnieniu jakości w całym procesie wytwarzania.

- Organizacja ustala **standardy** i metody pracy oraz zasady prowadzenia przeglądów, testów, kontroli zmian, pomiarów i raportowania.
- Sprawdza zarówno **jakość produktu**, jak i zgodność pracy z ustalonym procesem.

SQA ogranicza ryzyko defektów, lecz **nie gwarantuje** całkowitej bezbłędności.

<a id="pytanie-25"></a>

### 25. Jakie są zadania zespołu zapewniania jakości (SQA) w organizacji?

- Zespół SQA **ocenia produkt** z perspektywy klienta i sprawdza zgodność pracy ze standardami oraz wymaganiami. Nadzoruje też wykonanie zadań jakościowych, w tym przeglądów, testów i pomiarów.
- Zespół zapisuje i **raportuje niezgodności**, a nierozwiązane problemy przekazuje wyższemu kierownictwu.

**Odpowiedzialność** za jakość nadal spoczywa także na wykonawcach i kierownictwie.

<a id="pytanie-26"></a>

### 26. Jakie formy przeglądów technicznych produktów programowych stosuje się w projekcie?

- Podczas przeglądu typu **walkthrough** uczestnicy przechodzą przez dokument lub inny produkt pracy w logicznej kolejności.
- **Inspekcja** polega na systematycznym sprawdzaniu według listy kontrolnej.
- **Peer review** oznacza ocenę prowadzoną przez współpracowników. Może mieć formę inspekcji lub walkthrough.

Przeglądy mogą obejmować wymagania, projekt, kod i testy.

<a id="pytanie-27"></a>

### 27. Co oznacza kompleksowe zarządzanie jakością (TQM) w organizacji?

**TQM** (Total Quality Management) to zarządzanie jakością obejmujące całą organizację i cały cykl życia produktu.

- Opiera się na zaspokajaniu **potrzeb klientów**, przywództwie kierownictwa, odpowiedzialności wszystkich pracowników i podejściu procesowym.
- Wymaga zapobiegania defektom, podejmowania decyzji na podstawie pomiarów i **ciągłego doskonalenia**.

Dążenie do zera defektów jest celem, a nie gwarancją bezbłędnego produktu.

<a id="pytanie-28"></a>

### 28. Jak się ma zapewnianie jakości oprogramowania (SQA) do kompleksowego zarządzania jakością (TQM) w organizacji?

- **SQA** dotyczy zapewniania jakości oprogramowania i procesu jego wytwarzania.
- **TQM** obejmuje zarządzanie jakością w całej organizacji, w tym ludzi, procesy, dostawców i relacje z klientami.

**SQA może realizować zasady TQM** w obszarze oprogramowania.

Skuteczność obu podejść zależy od stosowania przyjętych zasad i wsparcia kierownictwa. Samo ustanowienie procedur nie wystarcza.

<a id="pytanie-29"></a>

### 29. Co oznacza odpowiedzialność kierownictwa za kompleksowe zarządzanie jakością (TQM) w organizacji?

- Kierownictwo ustala **politykę i cele jakościowe** oraz określa, kto za co odpowiada i jakie ma uprawnienia. Zapewnia też ludzi, czas i środki potrzebne do realizacji tych celów.
- Organizuje **doskonalenie procesów**, przegląda wyniki i usuwa problemy systemowe.

Odpowiada za **stworzenie warunków**, w których pracownicy mogą osiągać wymaganą jakość.

<a id="pytanie-30"></a>

### 30. Czy kierownictwo organizacji może przenieść odpowiedzialność za kompleksowe zarządzanie jakością (TQM) na niższy szczebel zarządzania?

**Kierownictwo nie może przenieść swojej nadrzędnej odpowiedzialności za jakość na niższy szczebel.**

- Może jednak **delegować zadania i uprawnienia**.
- Nadal odpowiada za politykę, cele, zasoby, nadzór i **skuteczność** systemu zarządzania jakością.

Przekazanie zadań na niższy szczebel nie zwalnia go z oceny wyników i organizowania doskonalenia.

<a id="mccall"></a>

## 3. Model McCalla

Główne źródło: [3.ModelMcCalla.pdf](3.ModelMcCalla.pdf).

<a id="pytanie-32"></a>

### 32. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia łatwości użycia?

- Łatwość użycia zapewniają **prosty i spójny interfejs**, zrozumiałe etykiety i komunikaty oraz odpowiednie formaty i jednostki danych.
- Pomagają **podpowiedzi**, informowanie o stanie programu i postępie operacji oraz możliwość podglądu wyników.
- **Walidacja danych**, cofanie zmian i odzyskiwanie po błędach ułatwiają radzenie sobie z pomyłkami.

Skuteczność tych rozwiązań należy sprawdzać podczas wykonywania rzeczywistych zadań przez użytkowników.

<a id="pytanie-33"></a>

### 33. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia łatwości nauki?

- Naukę programu ułatwiają **znane konwencje interfejsu**, spójne nazewnictwo i przewidywalne zachowanie.
- Naukę wspierają również **pomoc w programie**, podpowiedzi, szablony, przykłady, demonstracje i samouczki.
- Interfejs i objaśnienia należy dostosować do **umiejętności użytkownika**.

Łatwość nauki można oceniać przez czas potrzebny do opanowania funkcji.

<a id="pytanie-34"></a>

### 34. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia operatywności?

Operatywność zwiększa **ograniczenie liczby kroków** potrzebnych do wykonania częstych zadań.

- Służą temu menu kontekstowe, paski narzędzi, **skróty klawiszowe** i możliwość ich dostosowania.
- Pracę usprawniają podpowiedzi, powtarzanie, grupowanie oraz **automatyzacja operacji**.

Operatywność dotyczy sprawnego wykonywania pracy, a łatwość nauki określa wysiłek potrzebny do opanowania obsługi programu.

<a id="pytanie-35"></a>

### 35. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia elastyczności w zakresie funkcjonalnym?

- Elastyczność funkcjonalną zapewniają **makra**, rejestrowanie działań, własne skrypty i funkcje, dodatki oraz możliwość dołączania poleceń do interfejsu.
- Pomaga także **osadzanie obiektów** obsługiwanych przez inne aplikacje.
- **Modularność** i ponowne użycie komponentów ułatwiają rozszerzanie programu.

Dodawanie funkcji należy odróżnić od konfigurowania już dostępnych możliwości.

<a id="pomiary"></a>

## 4. Pomiary

Główne źródło: [4.Pomiary.pdf](4.Pomiary.pdf).

<a id="pytanie-38"></a>

### 38. W jaki sposób zapewnić dane do pomiaru procesów w inżynierii oprogramowania?

- Trzeba ustalić **cel pomiarów**, wybrać metryki oraz określić sposób zbierania danych i odpowiedzialne za to osoby. Następnie należy przeprowadzić pomiary próbne.
- Dane o kosztach, pracochłonności, defektach, testach i przeglądach należy **regularnie rejestrować**, przechowywać i analizować.

Źródłem mogą być systemy zgłoszeń, repozytoria i automatyczne raporty.

Należy zadbać o **kompletność danych** oraz porównywalne zasady ich zbierania.

<a id="pytanie-39"></a>

### 39. Czy metryki zorientowane na rozmiar kodu są wiarygodne?

**Metryki LOC/KLOC** są przydatne, gdy porównuje się podobne projekty i stosuje jednakowe zasady liczenia linii kodu.

- Ich wyniki zależą jednak od **języka i stylu** kodowania, a przed implementacją rozmiar trzeba szacować.
- **Krótszy kod** nie oznacza mniejszej produktywności ani gorszej jakości.

Wskaźnik defekty/KLOC opisuje **gęstość wykrytych defektów**, a nie częstość awarii podczas użytkowania.

<a id="pytanie-40"></a>

### 40. Czy punkty funkcjonalne rzeczywiście mierzą funkcjonalność systemu?

Punkty mierzą umowny **rozmiar funkcjonalny**, lecz nie stanowią pełnej oceny funkcjonalności systemu.

**Function Points** uwzględniają wejścia, wyjścia, zapytania, pliki i interfejsy zewnętrzne, a **Feature Points** dodatkowo uwzględniają algorytmy.

- Punkty można wyznaczać przed napisaniem kodu. Są mniej zależne od języka programowania niż LOC.
- Dobór wag i klas złożoności bywa subiektywny.

Liczba punktów **nie dowodzi poprawności** funkcji, ich kompletności względem potrzeb ani użyteczności.

<a id="pytanie-41"></a>

### 41. Jakie znaczenie mają metryki złożoności oprogramowania?

**Metryki złożoności** opisują strukturę kodu i pomagają ocenić trudność implementacji, testowania oraz utrzymania.

**Metryki Halsteada** opierają się na liczbach operatorów i operandów. **Złożoność McCabe’a** odpowiada liczbie liniowo niezależnych ścieżek w grafie przepływu sterowania.

Dla pojedynczego połączonego grafu z jednym wejściem i wyjściem stosuje się wzór `V(G)=E-N+2`, gdzie E oznacza liczbę krawędzi, a N liczbę węzłów.

**Indeks utrzymywalności** łączy te miary z LOC.

Metryki pomagają wskazać ryzykowne moduły, lecz nie gwarantują określonego czasu pracy ani liczby błędów.

<a id="iso9126"></a>

## 4a. ISO/IEC 9126

Główne źródło: [4a.ISO-9126.pdf](4a.ISO-9126.pdf).

<a id="pytanie-7"></a>

### 7. Czym różni się jakość wewnętrzna oprogramowania od zewnętrznej i użytkowej?

- **Jakość wewnętrzna** dotyczy cech kodu, projektu i dokumentacji. Można ją ocenić bez uruchamiania programu.
- **Jakość zewnętrzna** opisuje zachowanie uruchomionego programu, np. poprawność uzyskiwanych wyników i czas odpowiedzi.
- **Jakość użytkowa** odnosi się do efektów korzystania z systemu w określonych warunkach. Obejmuje skuteczność i produktywność pracy użytkownika, jego bezpieczeństwo oraz satysfakcję.

Na podstawie potrzeb użytkowników określa się wymagania zewnętrzne, a następnie wynikające z nich wymagania wewnętrzne. Sama dobra struktura kodu nie gwarantuje, że system będzie użyteczny.

<a id="pytanie-36"></a>

### 36. Jakie jest znaczenie modelu ISO/IEC 9126 w praktyce?

**ISO/IEC 9126** porządkuje wymagania i pomiary jakości oraz pozwala porównywać produkty według wspólnych kryteriów.

Rozróżnia **jakość wewnętrzną, zewnętrzną i użytkową**.

- W ocenie jakości wewnętrznej i zewnętrznej wyróżnia funkcjonalność, niezawodność, użyteczność, efektywność, utrzymywalność i przenośność.
- **Jakość użytkowa** obejmuje skuteczność, produktywność, bezpieczeństwo i satysfakcję.

Stosowanie modelu utrudniają duża liczba miar, koszt zbierania danych i konieczność ustalenia skal oceny.

Jest to **model historyczny**; ISO/IEC 9126-1:2001 zastąpiono przez ISO/IEC 25010:2011.

<a id="pytanie-37"></a>

### 37. Skąd zdobyć dane pomiarowe dla metryk wewnętrznych, zewnętrznych i użytkowych w modelu ISO/IEC 9126?

- Dane do **metryk wewnętrznych** pochodzą ze specyfikacji, projektu, dokumentacji i kodu.
- Dane do **metryk zewnętrznych** uzyskuje się z obserwacji działającego programu, wyników testów, raportów i kwestionariuszy.
- Dane do **metryk użytkowych** zbiera się przez obserwację wykonywania zadań, monitorowanie użycia i badanie satysfakcji użytkowników.

Przy każdym pomiarze trzeba określić wersję produktu, warunki i kontekst oceny.

<a id="cmmi"></a>

## 5. CMM/CMMI

Główne źródło: [5.CMM-CMMI.pdf](5.CMM-CMMI.pdf). Poniższe skale dotyczą historycznych modeli omawianych na wykładzie.

<a id="pytanie-44"></a>

### 44. Jak należy rozumieć dojrzałość procesu wytwarzania oprogramowania w sensie CMM/CMMI?

Dojrzałość określa **stopień uporządkowania i utrwalenia** procesu wytwarzania w organizacji.

- Wraz z jej wzrostem proces jest lepiej zdefiniowany, **powtarzalny**, konsekwentnie stosowany i doskonalony.
- **Standardy**, szkolenia, polityka organizacji i określony podział odpowiedzialności pozwalają zachować sposób pracy mimo zmian personelu.

Ułatwia to przewidywanie wyników projektów, lecz nie gwarantuje bezbłędności każdego produktu.

<a id="pytanie-45"></a>

### 45. Który poziom dojrzałości w CMM/CMMI oznacza wprowadzenie procesu zdefiniowanego i na czym to polega?

Proces zdefiniowany wprowadza się na **poziomie 3, Defined**.

- Organizacja ma **wspólny, udokumentowany standard** procesów zarządczych i inżynierskich, który jest rzeczywiście stosowany.
- Poszczególne projekty dostosowują go według ustalonych zasad (**tailoring**).

Wdrożenie wymaga szkoleń, koordynacji i przeglądów. Samo opisanie procesu w dokumentacji nie wystarcza.

<a id="pytanie-46"></a>

### 46. Czym różni się reprezentacja stopniowana CMMI od reprezentacji ciągłej?

- **Reprezentacja stopniowana** ocenia dojrzałość organizacji względem wymaganych zestawów obszarów procesowych.
- **Reprezentacja ciągła** pozwala osobno oceniać zdolność poszczególnych obszarów procesowych. Wyniki tworzą profil, a organizacja może ustalać własne priorytety doskonalenia.

W **CMMI 1.1** obowiązują następujące poziomy:

| Stopniowana: dojrzałość | Ciągła: zdolność obszaru |
|---|---|
| Brak poziomu 0 | 0 Incomplete |
| 1 Initial | 1 Performed |
| 2 Managed | 2 Managed |
| 3 Defined | 3 Defined |
| 4 Quantitatively Managed | 4 Quantitatively Managed |
| 5 Optimizing | 5 Optimizing |

<a id="iso9001"></a>

## 6. ISO 9000/9001

Główne źródło: [6.ISO_9001.pdf](6.ISO_9001.pdf).

<a id="pytanie-31"></a>

### 31. Jak w praktyce zrealizować w organizacji zasadę TQM „podejmowania decyzji w oparciu o fakty”?

1. Należy **określić cel**, zebrać wiarygodne dane o procesach i produktach, ustalić punkt odniesienia oraz przeanalizować przyczyny problemu.
2. Na tej podstawie **wybiera się usprawnienie**, a po jego wdrożeniu ponawia pomiary i ocenia skutki.
3. Dane, wyniki i decyzje trzeba **dokumentować**.

Sama **korelacja nie dowodzi związku przyczynowego**. Dłuższe inspekcje mogą prowadzić do wykrycia większej liczby błędów, ale większa liczba błędów może też wydłużać inspekcję.

<a id="pytanie-47"></a>

### 47. Co oznacza wprowadzenie polityki jakościowej w organizacji wg ISO 9000?

Aby wprowadzić **politykę jakościową**, kierownictwo ustala cele i zasady zarządzania jakością. Następnie dokumentuje je i wdraża w codziennej pracy.

Trzeba określić **odpowiedzialności i uprawnienia**, zapewnić zasoby oraz regularnie oceniać wyniki i doskonalić procesy.

W wydaniach z 2015 r. **ISO 9000** określa podstawy i terminologię, natomiast **ISO 9001** zawiera wymagania dotyczące systemu zarządzania jakością.

<a id="pytanie-48"></a>

### 48. Co to jest i co obejmuje księga jakości?

**Księga jakości** jest dokumentem opisującym system zarządzania jakością organizacji.

- Obejmuje **zakres systemu**, politykę i cele, odpowiedzialności, zasoby, dokumentację, realizację wyrobu, pomiary, postępowanie z niezgodnościami i doskonalenie.
- Może odsyłać do szczegółowych procedur i rejestrów.

Księga jakości była wymagana w starszych wydaniach ISO 9001. **Wydanie z 2015 r.** wymaga udokumentowanych informacji, ale nie odrębnej księgi jakości.

<a id="pytanie-49"></a>

### 49. Czy wprowadzenie ISO 9001 zapewnia zauważalną poprawę jakości produktów?

**Samo wdrożenie ISO 9001 nie gwarantuje poprawy jakości produktów.**

- ISO 9001 porządkuje system zarządzania jakością i może zwiększyć **powtarzalność wyników**.
- Poprawa jakości produktów zależy od rzeczywistego **stosowania i doskonalenia procesów**. Trzeba ją potwierdzić pomiarami cech produktu oraz wyników jego użytkowania.

Sam certyfikat ani dokumentacja zgodna z normą **nie gwarantują** wysokiej jakości lub bezbłędności produktu.

<a id="gqm"></a>

## 7a. GQM

Główne źródło: [7a.GQM.pdf](7a.GQM.pdf).

<a id="pytanie-42"></a>

### 42. Jaka jest przewaga metody pomiaru jakości Goal-Question-Metrics w porównaniu do metod klasycznych opartych o drzewo jakości (jak ISO/IEC 9126)?

W metodzie GQM najpierw określa się **cel oceny**, następnie formułuje **pytania**, a na końcu dobiera **metryki** potrzebne do udzielenia odpowiedzi.

Każdy pomiar służy więc konkretnej potrzebie i decyzji, co ogranicza zbieranie nieprzydatnych danych z rozbudowanego katalogu miar.

Metoda obejmuje **planowanie, definiowanie, zbieranie danych i interpretację**.

Można ją łączyć z modelami takimi jak ISO/IEC 9126, lecz błędny dobór celu może spowodować pominięcie ważnych cech jakości.

<a id="ahp"></a>

## 7b. AHP

Główne źródło: [7b.AHP.pdf](7b.AHP.pdf).

<a id="pytanie-43"></a>

### 43. Kiedy warto stosować metodę Saaty’ego (Analytic Hierarchy Process) do oceny jakości?

Metodę Saaty’ego (AHP) warto stosować do porównywania jakości kilku systemów według **wielu kryteriów o różnym znaczeniu**. Przydaje się szczególnie wtedy, gdy trudno nadać systemom oceny bezwzględne, ale łatwiej wskazać, który z dwóch jest lepszy pod określonym względem.

W AHP porządkuje się kryteria w hierarchię, **porównuje je parami i ustala ich wagi**. Następnie porównuje się systemy względem każdego kryterium. Połączenie ocen cząstkowych z wagami pozwala uzyskać ranking systemów zgodny z przyjętymi priorytetami.

AHP porządkuje ocenę, ale wynik nadal zależy od subiektywnych porównań. Należy sprawdzać **spójność ocen**, a wymagania obowiązkowe oceniać osobno.

<a id="agile"></a>

## 8. Jakość w Agile

Główne źródło: [8.Jakość w Agile.pdf](<8.Jakość w Agile.pdf>). Wiele przykładów dotyczy XP; nie opisują automatycznie wszystkich metod zwinnych.

<a id="pytanie-50"></a>

### 50. Z jakich powodów sygnatariusze manifestu zwinności odrzucili klasyczne metodyki wytwarzania?

Podejścia zwinne powstały w odpowiedzi na **nadmiar dokumentacji** i późne uzyskiwanie działających rezultatów. Problemami były też trudność ustalenia wszystkich wymagań z góry, słaby kontakt z klientem i niepewność co do końcowej jakości.

Dlatego większe znaczenie przyznano **działającemu oprogramowaniu**, współpracy i reagowaniu na zmiany.

Manifest nadal uznaje wartość dokumentacji, procesów, narzędzi, umów i planowania, choć **nadaje im niższy priorytet** niż pozostałym wartościom.

<a id="pytanie-51"></a>

### 51. Czy motywacje ludzi i zaufanie do nich są wystarczające dla sukcesu projektu informatycznego?

**Sama motywacja i zaufanie nie wystarczają do osiągnięcia sukcesu projektu.**

- Zespół potrzebuje również odpowiednich **kompetencji**, zasobów, współpracy z klientem i dobrego przepływu informacji.
- Potrzebne są także **standardy pracy**, odpowiednie projektowanie, testowanie, utrwalanie wiedzy i doskonalenie procesu.

Nawet zaangażowany zespół może **błędnie rozpoznać wymagania** lub przeoczyć ryzyko.

<a id="pytanie-52"></a>

### 52. Czy utożsamianie jakości oprogramowania z zadowoleniem klienta w metodykach zwinnych jest słuszne?

**Nie można utożsamiać jakości wyłącznie z zadowoleniem klienta.**

- Satysfakcja klienta jest **jednym z aspektów jakości**.
- Klient może być zadowolony z produktu, który nie spełnia **wymagań bezpieczeństwa**, obowiązkowych ograniczeń albo potrzeb użytkowników końcowych.

Ocena jakości musi uwzględniać wymagania wypowiedziane, domyślne i jeszcze nierozpoznane oraz rzeczywistą przydatność produktu w użyciu.

<a id="pytanie-53"></a>

### 53. Jakie są podstawowe warunki zapewnienia jakości oprogramowania w metodykach zwinnych?

Podstawowe warunki zapewnienia jakości to:

1. **Codzienna współpraca** z klientami i użytkownikami przez cały proces.
2. **Cele wydań** wynikające z rzeczywistych wymagań.
3. Dobry **przepływ informacji** w zespole i między zainteresowanymi stronami.
4. Znajomość i stosowanie **standardów pracy inżynierskiej**.
5. Rygorystyczne **testy jednostkowe** przed wydaniem.
6. **Testy akceptacyjne** z wybranymi użytkownikami przed rozpowszechnieniem.

W Scrumie ukończony przyrost musi spełniać uzgodnione kryteria **Definition of Done**.

<a id="pytanie-54"></a>

### 54. W jaki sposób problemy z klientem w metodykach zwinnych mogą wpłynąć negatywnie na jakość produktu?

- **Brak kontaktu**, zaangażowania lub decyzji klienta utrudnia rozpoznanie wymagań, wyjaśnianie szczegółów i ustalanie priorytetów.
- Zespół może czekać na decyzje albo realizować **niepotwierdzone założenia**.
- Bez regularnej informacji zwrotnej rozbieżności **wykrywa się późno**.

Skutkiem są niewłaściwe funkcje, pominięte scenariusze, opóźnienia oraz kosztowne poprawki. Część błędów ujawnia się dopiero u użytkowników.

<a id="pytanie-55"></a>

### 55. Skąd mogą wynikać problemy z klientem w metodykach zwinnych?

- Problemy mogą wynikać z **niezrozumienia roli klienta** w pracy zwinnej, sceptycyzmu, braku czasu i zaangażowania lub niskiego priorytetu projektu.
- Współpracę utrudniają **odległość**, różne strefy czasowe oraz tradycyjne procedury i warunki umowy.
- Przedstawiciel może mieć zbyt małą wiedzę lub oczekiwania odmienne od potrzeb użytkowników. Może też **nie mieć uprawnień do podejmowania decyzji**.

Stała cena sama nie przesądza o braku motywacji do współpracy.

<a id="pytanie-56"></a>

### 56. Jak firmy stosujące metodyki zwinne sobie radzą przy problemach z klientem?

- Firmy **wyjaśniają klientowi zasady współpracy**, dopasowują umowy i organizują regularne demonstracje. Mogą też wyznaczyć zastępczego przedstawiciela, który ma dostęp do potrzebnej wiedzy i decyzji klienta.
- **Oceniają ryzyko** braku zaangażowania, planują rezerwy czasu, przypisują właścicieli opowieściom użytkownika i odkładają te, które wymagają wyjaśnienia.

Zasady podejmowania decyzji, odbioru i zmian zakresu **powinny być jawne**.

W Scrumie **Product Owner** odpowiada za wartość produktu i zarządzanie Product Backlogiem, ale nie musi być klientem kontraktowym.

<a id="pytanie-57"></a>

### 57. Jak należy rozumieć formułowanie celów wydań na podstawie rzeczywistych wymagań klientów, a nie tylko ich opowieści?

Cel wydania powinien określać **rezultat potrzebny użytkownikom** i warunki jego osiągnięcia.

- Opowieści użytkownika są punktem wyjścia i **wymagają doprecyzowania**.
- Trzeba ustalić cel biznesowy, reguły działania, ograniczenia, wymagania niefunkcjonalne, sytuacje wyjątkowe i sprawdzalne **kryteria akceptacji**.

Dzięki temu można ocenić, czy wydanie zaspokaja rzeczywistą potrzebę, a nie tylko realizuje dosłowny zapis opowieści.

<a id="pytanie-58"></a>

### 58. Jak zapewnić znajomość i stosowanie odpowiednich standardów pracy inżynierskiej w zespole zwinnym?

- Należy ustalić zrozumiałe **standardy kodowania**, projektowania, integracji i testowania oraz zapewnić zespołowi dostęp do nich. W ich poznaniu pomagają szkolenia, mentoring i przykłady.
- Stosowanie standardów trzeba sprawdzać podczas **przeglądów kodu**, integracji i testów, a także za pomocą automatycznej analizy.
- Decyzje projektowe należy **dokumentować**, aby wiedza nie znikała przy zmianach personelu.

Przydatność praktyk, np. programowania w parach, trzeba oceniać na podstawie ich wyników i kosztów w konkretnym zespole.

<a id="pytanie-59"></a>

### 59. Czy rygorystyczne testowanie w metodykach zwinnych jest wystarczające dla zapewnienia jakości oprogramowania?

**Samo rygorystyczne testowanie nie wystarcza do zapewnienia jakości.**

- Testy mogą opierać się na **niepełnych wymaganiach** i pomijać istotne dane oraz scenariusze.
- Nawet **100% pokrycia** instrukcji lub gałęzi nie oznacza sprawdzenia wszystkich przebiegów, a TDD **nie gwarantuje bezbłędności**.

Potrzebne są także analiza wymagań, projektowanie, przeglądy, standardy i udział użytkowników w akceptacji.

Niezależna ocena testów pomaga wykryć przeoczenia, ale nie oznacza konieczności wykonywania każdego testu jednostkowego przez inną osobę.

<a id="pytanie-60"></a>

### 60. Kto powinien przeprowadzać testy akceptacyjne w metodykach zwinnych i jak się to ma do realiów?

- **Klient** powinien ustalać warunki akceptacji i odpowiadać za ocenę przydatności produktu. W testach wydań powinni uczestniczyć reprezentatywni użytkownicy.
- **Testerzy** mogą przygotować i technicznie wykonać testy.

W praktyce zdarza się, że wszystkie testy wykonują testerzy dostawcy, a użytkownicy jedynie nieregularnie sprawdzają wybrane funkcje. Zwiększa to ryzyko wykrycia problemów dopiero po wdrożeniu.

**Testy regresyjne** powinny być stałą częścią procesu wytwarzania. Decyzję o akceptacji trzeba uzgodnić z klientem.

<a id="pytanie-61"></a>

### 61. Dla jakich projektów informatycznych metodyki zwinne się nie nadają (przykłady)?

- Podejście oparte na częstej informacji zwrotnej i kolejnych aktualizacjach trudno stosować, gdy **klient jest niedostępny** lub produktu nie można łatwo zmieniać. Przykładem takiego produktu jest oprogramowanie **sondy kosmicznej**.
- W systemach radioterapii i systemach sterowania samolotem konieczne są **analiza zagrożeń i rygorystyczna weryfikacja**. Wieloletnie utrzymywanie systemu wymaga także trwałej dokumentacji.

Zwinność można łączyć z tymi praktykami. Sama wielkość lub krytyczność projektu **nie wyklucza** iteracyjnego rozwoju.

<a id="pytanie-62"></a>

### 62. Jakie są wady/zagrożenia dla procesu wytwarzania w metodykach zwinnych?

- Zagrożenia obejmują **zależność od konkretnych osób**, utratę wiedzy przy rotacji i braku dokumentacji, pomijanie wymagań jakościowych oraz sytuacji wyjątkowych.
- **Słaby kontakt** z klientem i trudności komunikacyjne utrudniają weryfikację potrzeb.
- Presja kolejnych wydań może zwiększać **dług techniczny**, koszty zmian i ryzyko niedostatecznych testów.

Są to zagrożenia związane z realizacją projektu, a nie konieczne cechy Agile. Podejścia zwinne nie wymagają rezygnacji z dokumentacji. W Scrumie jakość nie powinna spadać podczas Sprintu, a ukończony przyrost musi spełniać **Definition of Done**.

## Źródła uzupełniające

Pytanie 3: [seL4](https://sel4.systems/Verification/).

Pytanie 4: [Nancy Leveson](https://www.cse.msu.edu/~cse435/Handouts/Therac25-Leveson.pdf).

Pytanie 41: [McCabe, 1976](https://www.cs.du.edu/~snarayan/sada/teaching/COMP3705/lecture/p1/mccabe.pdf).

Pytanie 36: [katalog ISO](https://www.iso.org/standard/22749.html).

Pytanie 46: [CMMI 1.1](https://doi.org/10.1184/R1/6572141), [porównanie reprezentacji, SEI](https://www.sei.cmu.edu/documents/2948/2005_017_001_22691.pdf).

Pytanie 47: [ISO/TC 176](https://committee.iso.org/sites/tc176sc2/home/projects/published/iso-9001-2015.html).

Pytanie 48: [wytyczne ISO, s. 2-3](https://www.iso.org/iso/documented_information.pdf).

Pytanie 50: [Manifest](https://agilemanifesto.org/iso/pl/manifesto.html).

Pytanie 51: [zasady Manifestu](https://agilemanifesto.org/iso/pl/principles.html).

Pytanie 53: [Scrum Guide 2020](https://scrumguides.org/scrum-guide.html#commitment-definition-of-done).

Pytanie 56: [Scrum Guide](https://scrumguides.org/scrum-guide.html#product-owner).

Pytanie 59: [McCabe](https://www.cs.du.edu/~snarayan/sada/teaching/COMP3705/lecture/p1/mccabe.pdf).

Pytanie 62: [Manifest](https://agilemanifesto.org/iso/pl/manifesto.html), [Scrum Guide](https://scrumguides.org/scrum-guide.html#the-sprint).
