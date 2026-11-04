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

- **Oprogramowanie** wykonuje zadania użytkownika. Błąd w aplikacji może zmienić wynik obliczeń.
- **Sprzęt** umożliwia wykonanie tych zadań. Awaria urządzenia może zatrzymać poprawnie działający program.
- **Ludzie** wprowadzają dane, obsługują system i korzystają z wyników.
- **Procesy i procedury** określają, kto sprawdza dane i jak reaguje na błąd.
- **Zasoby informacji**, np. zewnętrzne źródła danych i bazy wiedzy, wpływają na poprawność wyniku.

Znaczenie każdego elementu zależy od zastosowania systemu. Nie ma stałych udziałów procentowych.

<a id="pytanie-2"></a>

### 2. Czy u źródeł każdej awarii systemu informatycznego stoi błąd programistów?

**Nie.** Awaria może mieć kilka przyczyn jednocześnie. Przykłady to:

- błędne wymaganie, które pomija ważny przypadek;
- błąd projektu, np. brak niezależnego zabezpieczenia;
- awaria sprzętu;
- nieprawidłowe dane wejściowe;
- pomyłka podczas obsługi;
- niewłaściwa procedura, np. ponowienie operacji mimo alarmu.

**Defekt prowadzi do awarii dopiero w warunkach, w których się ujawni.** Zabezpieczenie może zatrzymać dalszy rozwój zdarzeń.

<a id="pytanie-3"></a>

### 3. Dlaczego wytwórcy oprogramowania nie mogą zagwarantować 100% bezbłędności swojego produktu?

- Ze względu na złożoność oprogramowania nie da się w praktyce sprawdzić **wszystkich kombinacji** danych, stanów i warunków działania.
- Błędy mogą też występować w wymaganiach i **specyfikacji**.
- Testy potwierdzają poprawność **tylko w sprawdzonych przypadkach**.

**Dowody formalne** mogą potwierdzić określone własności programu przy przyjętych założeniach. Nie dają jednak bezwarunkowej gwarancji poprawności całego systemu.

<a id="pytanie-5"></a>

### 5. Dlaczego rozumienie jakości oprogramowania jako stopnia spełnienia wyspecyfikowanych wymagań jest niewystarczająca?

**Specyfikacja może być niepełna albo błędna.** Nawet program zgodny z jej treścią może nie nadawać się do pracy. W ocenie trzeba uwzględnić np.:

- **bezpieczeństwo** osób, na które wpływa działanie programu;
- **ochronę danych** przed nieuprawnionym dostępem;
- **użyteczność** podczas rzeczywistych zadań;
- **wydajność** przy obciążeniu typowym dla użytkowników;
- **wymagania obowiązkowe**, nawet jeśli klient ich nie wymienił.

Jakość zależy również od spełnienia potrzeb domyślnych i jeszcze nierozpoznanych.

<a id="pytanie-6"></a>

### 6. Dlaczego przy zbieraniu wymagań dla oprogramowania nie wystarczy o nie pytać przedstawiciela klienta?

**Jedna osoba może znać cele klienta, ale tylko część potrzeb użytkowników.** Wywiad z przedstawicielem nie wystarczy, bo może on:

- nie znać przebiegu codziennej pracy;
- pominąć potrzeby innych grup, np. odbiorców raportów;
- przemilczeć wymaganie, które uważa za oczywiste;
- nie rozpoznać potrzeby, która ujawni się dopiero w użyciu;
- nie mieć uprawnień do rozstrzygnięcia sprzecznych oczekiwań.

Wymagania warto sprawdzić z użytkownikami, dostawcami danych i odbiorcami wyników. Pomagają w tym obserwacja pracy, analiza sytuacji wyjątkowych oraz wspólny przegląd prototypu.

<a id="pytanie-8"></a>

### 8. Z jakich elementów składa się model „drzewa” jakości?

**Korzeniem drzewa jest ogólna jakość.** Dzieli się ją na główne atrybuty, a każdy atrybut na szczegółowe cechy, które oceniamy za pomocą metryk. Przykłady gałęzi i należących do nich cech:

- **Funkcjonalność** — np. kompletność wymaganych funkcji.
- **Wydajność** — np. szybkość reakcji systemu.
- **Wiarygodność** — np. odporność na błędy.
- **Satysfakcja** — np. łatwość nauki obsługi.
- **Elastyczność** — np. możliwość dostosowania konfiguracji.

**Wagi** określają znaczenie składowych. Ocenę atrybutu można obliczyć jako średnią ważoną `A = Σ(w·M)/Σw`, gdy suma wag jest dodatnia. Podział na gałęzie zależy od modelu jakości.

<a id="pytanie-9"></a>

### 9. Co to są atrybuty jakości i jak się mają do wymagań?

**Atrybut jakości** to cecha produktu. **Wymaganie** określa oczekiwany poziom tej cechy w danych warunkach. Przykładowe powiązania:

- wymagania funkcjonalne dotyczą **funkcjonalności**;
- wymagania czasowe dotyczą **wydajności**;
- wymagania niezawodnościowe dotyczą **wiarygodności**;
- ograniczenia, np. dotyczące platformy, mogą dotyczyć **elastyczności**.

„95% odpowiedzi poniżej 2 s przy 100 jednoczesnych użytkownikach” to sprawdzalne wymaganie dotyczące wydajności.

<a id="pytanie-10"></a>

### 10. Czy dla każdego atrybutu jakości można wyznaczyć metrykę?

**Nie dla każdego atrybutu da się wyznaczyć bezpośrednią, obiektywną metrykę.** Nawet cecha mierzalna, taka jak wydajność systemu, może wymagać kilku pomiarów. Można zmierzyć np.:

- **czas odpowiedzi** — ile użytkownik czeka na wynik;
- **czas przetwarzania** — jak długo trwa wykonanie całego zadania, np. przygotowanie raportu;
- **przepustowość** — ile żądań system obsługuje na sekundę;
- **zużycie pamięci** — ile pamięci zajmuje program podczas pracy;
- **wykorzystanie procesora** — jaką część jego czasu zajmuje obsługa danego obciążenia.

Aby porównać wyniki, trzeba ustalić warunki pomiaru, np. liczbę jednoczesnych użytkowników. **Satysfakcję** trudniej mierzyć bezpośrednio. Można ją ocenić ankietą, ale przypisanie odpowiedziom liczb nie usuwa subiektywności ocen.

<a id="pytanie-11"></a>

### 11. Czym różnią się metryki jakościowe od miar?

**Metryka** określa, **co oceniamy**, a **miara** określa, **jak wyznaczamy tę ocenę**: sposób obliczenia, skalę lub jednostkę.

Przykładowo oceniamy kompletność funkcjonalną, a jej miarą jest iloraz liczby zrealizowanych funkcji i liczby funkcji wymaganych. Wynik można wyrazić jako ułamek lub procent.

- Należy odróżniać samą cechę, definicję wskaźnika, procedurę pomiaru i otrzymany wynik.
- Metryki nie muszą mieć skali `[0,1]`; mogą być wyrażone np. czasem.

<a id="pytanie-12"></a>

### 12. Jakie problemy występują przy pomiarach jakości?

Przy pomiarach jakości występują m.in. następujące problemy:

- **Wiele cech naraz.** Jedna liczba może ukryć słaby wynik w ważnym obszarze.
- **Subiektywność.** Dwie osoby mogą inaczej ocenić tę samą cechę.
- **Brak punktu odniesienia.** Trudno stwierdzić, czy wynik jest wystarczająco dobry.
- **Normalizacja.** Żeby połączyć wyniki w różnych jednostkach, trzeba ustalić wspólną skalę.
- **Dobór wag.** Zmiana znaczenia atrybutów może zmienić ocenę końcową.
- **Zebranie i interpretacja danych.** Wiele pomiarów kosztuje czas, a długa ankieta może obniżyć rzetelność odpowiedzi.

Pytania tak/nie ułatwiają liczenie odpowiedzi, ale same nie zapewniają obiektywności.

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

**Model drzewa** pokazuje, jak oceny poszczególnych cech składają się na ocenę jakości. Pozwala:

- rozłożyć ogólną jakość na konkretne atrybuty;
- powiązać każdy atrybut z pomiarami;
- nadać cechom wagi odpowiednie dla danego zastosowania;
- porównać produkty według wspólnych kryteriów;
- wskazać, którą cechę trzeba poprawić.

**Ocena łączna może ukryć krytyczną słabość.** Dlatego warto zachować wyniki składowe i oddzielnie sprawdzać wymagania obowiązkowe.

<a id="pytanie-16"></a>

### 16. Czym różni się wiarygodność systemu informatycznego od jego niezawodności?

**Wiarygodność** (*dependability*) oznacza stopień zaufania do systemu. W modelu z wprowadzenia składa się na nią pięć cech:

- **Niezawodność** (*reliability*) — system świadczy usługę bez awarii.
- **Odporność na błędy** — system toleruje błędy podczas pracy.
- **Bezpieczeństwo** — system chroni ludzi i otoczenie przed szkodą.
- **Ochrona** — system ogranicza dostęp do uprawnionych osób.
- **Łatwość testowania** — można wykrywać i identyfikować błędy.

Niezawodność jest więc częścią wiarygodności. System może działać bez przerwy, a mimo to ujawniać dane osobom nieuprawnionym.

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

Wypadki Therac-25 miały **przyczyny techniczne i organizacyjne**.

- **Konstrukcja.** Usunięto część niezależnych blokad sprzętowych i powierzono ochronę pacjenta programowi.
- **Synchronizacja.** Po szybkiej korekcie parametrów ekran mógł pokazywać nowy tryb, choć urządzenie nadal było ustawione inaczej.
- **Błąd licznika.** Co 256 przebiegów zmienna `Class3` przyjmowała wartość zero. Program mógł wtedy pominąć kontrolę położenia kolimatora.
- **Interfejs.** Niejasne komunikaty i mylące wskazania dawki utrudniały ocenę sytuacji. Operator mógł ponowić zabieg po błędzie.
- **Weryfikacja.** Analiza bezpieczeństwa skupiała się na sprzęcie, a testy oprogramowania nie ujawniły niebezpiecznych przebiegów.
- **Reakcja na wypadki.** Wcześniejsze zdarzenia niedostatecznie dokumentowano i analizowano.

Działanie operatora mogło uruchomić wadliwy scenariusz. Projekt urządzenia powinien był w takiej sytuacji zablokować emisję.

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

**SQA** (*Software Quality Assurance*) to zaplanowane, systematyczne działania, które organizacja prowadzi przez cały proces wytwarzania:

- ustala metody pracy inżynierskiej;
- przeprowadza formalne przeglądy techniczne;
- testuje oprogramowanie;
- sprawdza przestrzeganie standardów;
- kontroluje zmiany;
- mierzy jakość produktu i przebieg prac;
- zapisuje i raportuje wyniki.

W ten sposób organizacja sprawdza zarówno **jakość produktu z perspektywy klienta**, jak i **zgodność pracy z przyjętym procesem**. SQA ogranicza ryzyko defektów.

<a id="pytanie-25"></a>

### 25. Jakie są zadania zespołu zapewniania jakości (SQA) w organizacji?

**Zespół SQA** ma następujące zadania:

- ocenia powstający produkt z punktu widzenia klienta;
- sprawdza zgodność pracy ze standardami i wymaganiami;
- sprawdza, czy uczestnicy projektu wykonują przypisane im zadania jakościowe;
- nadzoruje przeglądy, testowanie, kontrolę zmian i pomiary;
- dokumentuje wyniki i zgłasza niezgodności zainteresowanym osobom;
- przekazuje wyższemu kierownictwu problemy, których zespół projektowy nie może rozwiązać.

Za jakość swojej pracy odpowiadają również wykonawcy i kierownictwo.

<a id="pytanie-26"></a>

### 26. Jakie formy przeglądów technicznych produktów programowych stosuje się w projekcie?

Podstawowe formy **formalnych przeglądów technicznych (FTR)** to walkthrough i inspekcje.

- Podczas przeglądu typu **walkthrough** uczestnicy przechodzą przez dokument lub inny produkt pracy w logicznej kolejności.
- **Inspekcja** polega na systematycznym sprawdzaniu według listy kontrolnej.
- **Peer review** oznacza ocenę prowadzoną przez współpracowników. Może mieć formę inspekcji lub walkthrough.

Przeglądy mogą obejmować wymagania, projekt, kod i testy.

<a id="pytanie-27"></a>

### 27. Co oznacza kompleksowe zarządzanie jakością (TQM) w organizacji?

**TQM** (*Total Quality Management*) angażuje całą organizację w spełnianie oczekiwań klientów przez cały cykl życia produktu. W praktyce oznacza to, że:

- oczekiwania klientów wyznaczają cele jakościowe;
- kierownictwo ustala kierunek działań i zapewnia środki;
- każdy pracownik odpowiada za jakość swojej pracy;
- organizacja analizuje i poprawia procesy, w których powstają błędy;
- zespół zapobiega defektom już podczas wytwarzania;
- decyzje o zmianach opiera się na pomiarach;
- usprawnienia planuje się i wprowadza także podczas utrzymania produktu.

„Zero defektów” wyraża cel tych działań.

<a id="pytanie-28"></a>

### 28. Jak się ma zapewnianie jakości oprogramowania (SQA) do kompleksowego zarządzania jakością (TQM) w organizacji?

- **SQA** obejmuje planowe działania zapewniające jakość oprogramowania, w tym wielokrotne przeglądy i kontrole produktów na każdym etapie wytwarzania.
- **TQM** obejmuje zarządzanie jakością procesów w całej organizacji i całym cyklu życia produktu, również podczas utrzymania. Angażuje kierownictwo, pracowników, dostawców i klientów.

**SQA może realizować zasady TQM** w obszarze oprogramowania.

Skuteczność obu podejść zależy od stosowania przyjętych zasad i wsparcia kierownictwa. Samo ustanowienie procedur nie wystarcza.

<a id="pytanie-29"></a>

### 29. Co oznacza odpowiedzialność kierownictwa za kompleksowe zarządzanie jakością (TQM) w organizacji?

**Kierownictwo odpowiada za warunki, w których pracownicy mogą osiągać wymaganą jakość.** Do jego obowiązków należą:

- ustalenie polityki i celów jakościowych;
- określenie odpowiedzialności i uprawnień;
- zapewnienie ludzi, czasu i środków;
- zorganizowanie doskonalenia procesów;
- okresowy przegląd wyników i działania systemu jakości;
- rozwiązywanie problemów, na które pojedynczy zespół nie ma wpływu.

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

**Łatwość użycia** oznacza, że użytkownik może wykonać zadanie i poradzić sobie z pomyłką. Pomagają w tym:

- **Spójny interfejs.** Te same polecenia i pola wyglądają podobnie w całym programie.
- **Zrozumiałe etykiety i podpowiedzi.** Użytkownik wie, co wpisać i do czego służy przycisk.
- **Odpowiednie jednostki i formaty.** Dane można odczytać bez samodzielnego przeliczania.
- **Informacja o stanie.** Program pokazuje nazwę otwartego dokumentu i postęp długiej operacji.
- **Podgląd wyniku.** Użytkownik może obejrzeć dokument przed wydrukiem.
- **Walidacja i komunikaty błędów.** Program wskazuje błędną wartość i podpowiada, jak ją poprawić.
- **Cofanie zmian i odzyskiwanie danych.** Użytkownik może naprawić skutki pomyłki.

Skuteczność tych rozwiązań sprawdza się podczas wykonywania rzeczywistych zadań.

<a id="pytanie-33"></a>

### 33. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia łatwości nauki?

**Łatwość nauki** oznacza, że nowy użytkownik szybko opanowuje obsługę programu. Pomagają w tym:

- **Znane konwencje interfejsu** — polecenia działają podobnie jak w innych programach tej klasy.
- **Wprowadzenie przy pierwszym użyciu** — pokazuje podstawowe możliwości programu.
- **Pomoc i podpowiedzi** — wyjaśniają znaczenie menu i przycisków w chwili, gdy są potrzebne.
- **Szablony** — pozwalają wykonać pierwsze zadanie od gotowego wzoru.
- **Dokumenty przykładowe** — pokazują, jaki wynik można uzyskać.
- **Demonstracje i samouczki** — prowadzą użytkownika przez kolejne czynności.
- **Dostosowanie do poziomu użytkownika** — początkujący otrzymuje więcej wskazówek.

Łatwość nauki można ocenić, mierząc czas potrzebny do samodzielnego opanowania funkcji.

<a id="pytanie-34"></a>

### 34. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia operatywności?

**Operatywność** dotyczy tego, jak sprawnie użytkownik wykonuje znane mu zadania. Zwiększają ją:

- **Menu kontekstowe** z poleceniami dla wybranego obiektu.
- **Przyciski na pasku narzędzi** zapewniające szybki dostęp do częstych poleceń.
- **Skróty klawiszowe** ograniczające liczbę kroków.
- **Dostosowanie menu, przycisków i skrótów** do sposobu pracy użytkownika.
- **Podpowiedzi przy wprowadzaniu danych** ułatwiające wybór wartości.
- **Powtarzanie i grupowanie operacji**, np. zmiana kilku rekordów naraz.
- **Automatyzacja** powtarzalnych czynności.

Łatwość nauki dotyczy czasu opanowania funkcji, a operatywność — sprawności późniejszej pracy.

<a id="pytanie-35"></a>

### 35. Jakie mechanizmy w oprogramowaniu się stosuje dla zapewnienia elastyczności w zakresie funkcjonalnym?

**Elastyczność funkcjonalna** pozwala rozszerzać możliwości programu. Przykładowe mechanizmy to:

- **Makra** — użytkownik nagrywa sekwencję działań do ponownego wykonania.
- **Własne funkcje i skrypty** — użytkownik definiuje nowe operacje.
- **Własne polecenia w interfejsie** — skrypt można wywołać z menu lub przyciskiem.
- **Dodatki** (*add-ins*) — użytkownik instaluje rozszerzenie napisane przez innego autora.
- **Osadzanie obiektów** — dokument zawiera obiekt obsługiwany przez inną aplikację.
- **Moduły** — komponent można doinstalować lub wykorzystać ponownie w innym programie.

Konfiguracja zmienia ustawienia istniejącej funkcji. Rozszerzenie dodaje nową możliwość.

<a id="pomiary"></a>

## 4. Pomiary

Główne źródło: [4.Pomiary.pdf](4.Pomiary.pdf).

<a id="pytanie-38"></a>

### 38. W jaki sposób zapewnić dane do pomiaru procesów w inżynierii oprogramowania?

Najpierw trzeba określić **cel pomiarów**, metryki, sposób zapisu danych i osoby odpowiedzialne. Po pomiarze próbnym zespół regularnie gromadzi i analizuje zapisy, m.in.:

- **wyniki testów** — co sprawdzono i z jakim wynikiem;
- **raporty problemowe** — jakie defekty zgłoszono;
- **żądania zmian** — co i dlaczego trzeba zmienić;
- **raporty z audytów** — jakie niezgodności stwierdzono;
- **protokoły z przeglądów i inspekcji** — jakie błędy wykryto i ile pracy wymagała kontrola;
- **ewidencję pracy i kosztów** — ile czasu i środków pochłonęły działania.

W zbieraniu danych pomagają systemy zgłoszeń, repozytoria i automatyczne raporty. Zapisy muszą być kompletne, porównywalne, chronione i możliwe do odczytania po czasie.

<a id="pytanie-39"></a>

### 39. Czy metryki zorientowane na rozmiar kodu są wiarygodne?

**Metryki oparte na liczbie linii kodu (LOC/KLOC)** są użyteczne przy porównywaniu podobnych projektów, jeśli obowiązują te same zasady liczenia.

- Po implementacji łatwo policzyć linie kodu.
- Rozmiar kodu można wykorzystać w modelach szacowania kosztów i pracochłonności.
- Wynik zależy od języka i stylu programowania.
- Zwięzły program może uzyskać gorszy wskaźnik oparty na LOC mimo dobrej jakości.
- Porównania są szczególnie trudne dla języków nieproceduralnych.
- Przed implementacją liczbę linii trzeba oszacować, więc wynik zależy od trafności prognozy.

**Defekty/KLOC** to liczba wykrytych defektów na tysiąc linii. Częstość awarii podczas użytkowania wymaga odrębnego pomiaru.

<a id="pytanie-40"></a>

### 40. Czy punkty funkcjonalne rzeczywiście mierzą funkcjonalność systemu?

Punkty mierzą **rozmiar funkcjonalny systemu**. W metodzie *Function Points* zlicza się elementy pięciu kategorii i uwzględnia ich złożoność:

- **wejścia** od użytkownika;
- **wyjścia** przekazywane użytkownikowi;
- **zapytania**;
- **pliki**;
- **interfejsy zewnętrzne**.

Metoda *Feature Points* uwzględnia dodatkowo **algorytmy**. Obie metody można stosować przed napisaniem kodu. Wynik jest mniej zależny od języka niż LOC, ale dobór wag bywa subiektywny, a dane są trudniejsze do zebrania.

Liczba punktów nie mówi, czy funkcje działają poprawnie, odpowiadają potrzebom użytkowników i są łatwe w obsłudze.

<a id="pytanie-41"></a>

### 41. Jakie znaczenie mają metryki złożoności oprogramowania?

**Metryki złożoności** opisują strukturę kodu. Pomagają wskazać moduły trudniejsze do zrozumienia, przetestowania lub utrzymania.

- **Metryki Halsteada** opierają się na liczbie operatorów i operandów w kodzie.
- **Złożoność McCabe’a** podaje liczbę liniowo niezależnych ścieżek w grafie przepływu sterowania. Dla pojedynczego połączonego grafu z jednym wejściem i wyjściem `V(G) = E − N + 2`, gdzie E to liczba krawędzi, a N to liczba węzłów.
- **Indeks utrzymywalności** łączy miary Halsteada i McCabe’a z rozmiarem kodu (LOC).

Wysoki wynik może wskazać moduł wymagający przeglądu. Sam wynik nie wyznacza dokładnego czasu pracy ani liczby błędów.

<a id="iso9126"></a>

## 4a. ISO/IEC 9126

Główne źródło: [4a.ISO-9126.pdf](4a.ISO-9126.pdf).

<a id="pytanie-7"></a>

### 7. Czym różni się jakość wewnętrzna oprogramowania od zewnętrznej i użytkowej?

- **Jakość wewnętrzna** dotyczy cech kodu, projektu i dokumentacji. Można ją ocenić bez uruchamiania programu.
- **Jakość zewnętrzna** opisuje zachowanie uruchomionego programu, np. poprawność uzyskiwanych wyników i czas odpowiedzi.
- **Jakość użytkowa** odnosi się do efektów korzystania z systemu w określonych warunkach. Obejmuje skuteczność i produktywność pracy, bezpieczeństwo użytkowników i otoczenia oraz satysfakcję użytkownika.

Na podstawie potrzeb użytkowników określa się wymagania zewnętrzne, a następnie wynikające z nich wymagania wewnętrzne. Sama dobra struktura kodu nie gwarantuje, że system będzie użyteczny.

<a id="pytanie-36"></a>

### 36. Jakie jest znaczenie modelu ISO/IEC 9126 w praktyce?

**ISO/IEC 9126** daje wspólny sposób opisywania wymagań, doboru pomiarów i porównywania produktów. Do oceny jakości wewnętrznej i zewnętrznej służy sześć charakterystyk:

- **Funkcjonalność** — np. poprawność wyników.
- **Wiarygodność** (*reliability*, czyli niezawodność) — np. zdolność odzyskania sprawności po awarii.
- **Użyteczność** — np. łatwość nauki obsługi.
- **Efektywność** — np. czas odpowiedzi i zużycie zasobów.
- **Utrzymywalność** — np. łatwość wprowadzania i testowania zmian.
- **Przenośność** — np. łatwość instalacji w innym środowisku.

Osobno ocenia się **jakość użytkową** przez skuteczność i produktywność pracy, bezpieczeństwo i satysfakcję. W praktyce trzeba dobrać miary i skale do celu oceny oraz uwzględnić koszt zbierania danych.

To model historyczny. ISO/IEC 9126-1:2001 zastąpiono przez ISO/IEC 25010:2011.

<a id="pytanie-37"></a>

### 37. Skąd zdobyć dane pomiarowe dla metryk wewnętrznych, zewnętrznych i użytkowych w modelu ISO/IEC 9126?

- Dane do **metryk wewnętrznych** pochodzą ze specyfikacji wymagań, kodu źródłowego i dokumentacji. Pomocniczo można korzystać z zapisanych wyników testów; ocena dotyczy własności produktu.
- Dane do **metryk zewnętrznych** pochodzą ze specyfikacji wymagań, dokumentacji i raportów z testów. Opisują zachowanie działającego programu w określonych warunkach.
- Dane do **metryk użytkowych** pochodzą z raportów z obserwacji użytkowników, monitorowania użycia i kwestionariuszy. Opisują wykonywanie zadań oraz satysfakcję użytkowników.

Przy każdym pomiarze trzeba określić wersję produktu, warunki i kontekst oceny.

<a id="cmmi"></a>

## 5. CMM/CMMI

Główne źródło: [5.CMM-CMMI.pdf](5.CMM-CMMI.pdf). Poniższe skale dotyczą historycznych modeli omawianych na wykładzie.

<a id="pytanie-44"></a>

### 44. Jak należy rozumieć dojrzałość procesu wytwarzania oprogramowania w sensie CMM/CMMI?

**Dojrzałość procesu** określa, na ile organizacja potrafi powtarzać, kontrolować i doskonalić sposób wytwarzania oprogramowania. W reprezentacji stopniowanej CMMI kolejne poziomy oznaczają:

1. **Początkowy** — sposób pracy zależy głównie od osób i sytuacji.
2. **Zarządzany** — poszczególne projekty planują i kontrolują swoją pracę.
3. **Zdefiniowany** — projekty korzystają ze wspólnego standardu organizacji.
4. **Zarządzany ilościowo** — organizacja wykorzystuje pomiary do zarządzania procesami.
5. **Optymalizowany** — organizacja systematycznie doskonali procesy.

Standardy, szkolenia i podział odpowiedzialności utrwalają sposób pracy mimo zmian personelu. Ułatwia to przewidywanie wyników projektów, ale nie gwarantuje bezbłędności produktu.

<a id="pytanie-45"></a>

### 45. Który poziom dojrzałości w CMM/CMMI oznacza wprowadzenie procesu zdefiniowanego i na czym to polega?

**Proces zdefiniowany to poziom 3 (Defined).** Organizacja ma wspólny, udokumentowany standard procesów zarządczych i inżynierskich. Projekty dostosowują go do swoich potrzeb według zatwierdzonych zasad (*tailoring*). W praktyce oznacza to m.in.:

- planowanie prac zgodnie z dostosowanym procesem projektu;
- zbieranie doświadczeń z projektów i doskonalenie wspólnego standardu;
- uzgadnianie wymagań i zobowiązań między zespołami;
- koordynowanie zadań inżynierskich i dbanie o spójność ich wyników;
- prowadzenie przeglądów wzajemnych w celu wykrywania defektów;
- szkolenie pracowników do ról przewidzianych w procesie.

<a id="pytanie-46"></a>

### 46. Czym różni się reprezentacja stopniowana CMMI od reprezentacji ciągłej?

- **Reprezentacja stopniowana** ocenia dojrzałość organizacji względem wymaganych zestawów obszarów procesowych. Uzyskanie poziomu wymaga spełnienia całego przypisanego mu zestawu wymagań, z zachowaniem wymagań niższych poziomów.
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

**Decyzja oparta na faktach** powinna wynikać z pomiarów, a jej skuteczność trzeba sprawdzić po wdrożeniu.

1. Określić problem i mierzalny cel.
2. Ustalić punkt odniesienia i zebrać porównywalne dane, np. liczbę i rodzaj reklamacji.
3. Przeanalizować możliwe przyczyny problemu.
4. Wybrać i wdrożyć usprawnienie.
5. Powtórzyć pomiar, ocenić skutki i udokumentować decyzję.

**Korelacja nie rozstrzyga przyczyny.** Dłuższa inspekcja może ujawnić więcej błędów, ale znalezienie wielu błędów może też wydłużyć inspekcję.

<a id="pytanie-47"></a>

### 47. Co oznacza wprowadzenie polityki jakościowej w organizacji wg ISO 9000?

Wprowadzenie **polityki jakościowej** oznacza, że kierownictwo przekłada cele jakościowe na zasady codziennej pracy. W tym celu:

- dokumentuje politykę i cele związane z potrzebami klienta;
- ustala, kto za co odpowiada i jakie ma uprawnienia;
- zapewnia ludzi, czas i środki;
- wdraża wymagania systemu jakości i dba o ich przestrzeganie;
- okresowo przegląda wyniki i decyduje o usprawnieniach.

W wydaniach z 2015 r. **ISO 9000** opisuje podstawy i terminologię, a **ISO 9001** określa wymagania dotyczące systemu zarządzania jakością.

<a id="pytanie-48"></a>

### 48. Co to jest i co obejmuje księga jakości?

**Księga jakości** opisuje system zarządzania jakością organizacji. Przykładowa księga obejmuje:

- zakres systemu i podstawy normatywne;
- politykę i cele jakościowe;
- strukturę organizacji, obowiązki i uprawnienia;
- nadzór nad dokumentami i zapisami;
- odpowiedzialność kierownictwa i zarządzanie zasobami;
- realizację wyrobu, od rozpoznania wymagań klienta po wytwarzanie;
- pomiary, analizę niezgodności i doskonalenie.

Księga może odsyłać do procedur i rejestrów, np. rejestru reklamacji. Starsze wydania ISO 9001 wymagały księgi jakości. Wydanie z 2015 r. wymaga udokumentowanych informacji, ale pozostawia organizacji wybór formy.

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

**Przewagą GQM jest dobór metryk do konkretnego celu.** Drzewo jakości porządkuje cechy produktu, a GQM pozwala ustalić, które dane są potrzebne do podjęcia danej decyzji. Przykład z inspekcji kodu:

1. **Cel (Goal).** Chcemy trafniej planować pracochłonność inspekcji.
2. **Pytanie (Question).** Ile pracy wymaga przegląd kodu?
3. **Metryki (Metrics).** Rejestrujemy rozmiar przejrzanego kodu w KLOC i średnią pracochłonność inspekcji na KLOC.

Każda metryka odpowiada na konkretne pytanie, co ogranicza zbieranie zbędnych danych. GQM można łączyć z drzewem jakości ISO/IEC 9126. Źle dobrany cel może jednak spowodować pominięcie ważnych cech.

Cały proces GQM obejmuje planowanie, definiowanie, zbieranie danych i interpretację wyników.

<a id="ahp"></a>

## 7b. AHP

Główne źródło: [7b.AHP.pdf](7b.AHP.pdf).

<a id="pytanie-43"></a>

### 43. Kiedy warto stosować metodę Saaty’ego (Analytic Hierarchy Process) do oceny jakości?

AHP warto stosować, gdy porównujemy kilka systemów według **wielu kryteriów o różnym znaczeniu**, a trudno ocenić jakość w skali bezwzględnej. Łatwiej wtedy porównać dwa warianty pod jednym względem, np. wskazać, który system szybciej reaguje.

1. Ułożyć kryteria w hierarchię i porównać je **parami**, aby ustalić ich wagi.
2. Dla każdego kryterium porównać systemy parami.
3. Połączyć oceny cząstkowe z wagami, aby uzyskać ranking zgodny z przyjętymi priorytetami.

Wynik zależy od ocen osób wykonujących porównania. Trzeba sprawdzić **spójność ocen**, a wymagania obowiązkowe rozpatrzyć osobno.

<a id="agile"></a>

## 8. Jakość w Agile

Główne źródło: [8.Jakość w Agile.pdf](<8.Jakość w Agile.pdf>). Wiele przykładów dotyczy XP; nie opisują automatycznie wszystkich metod zwinnych.

<a id="pytanie-50"></a>

### 50. Z jakich powodów sygnatariusze manifestu zwinności odrzucili klasyczne metodyki wytwarzania?

W podejściu klasycznym dostrzegano pięć problemów:

- przygotowanie dokumentacji pochłaniało dużo czasu;
- działające oprogramowanie trafiało do klienta późno;
- trudno było określić wszystkie wymagania na początku projektu;
- podczas implementacji zespół tracił kontakt z użytkownikiem;
- mimo przestrzegania procedur końcowa jakość pozostawała niepewna.

Dlatego Manifest przyznaje większe znaczenie **ludziom i ich współpracy, działającemu oprogramowaniu, współpracy z klientem i reagowaniu na zmiany**. Nadal uznaje wartość dokumentacji, procesów, narzędzi, umów i planowania.

<a id="pytanie-51"></a>

### 51. Czy motywacje ludzi i zaufanie do nich są wystarczające dla sukcesu projektu informatycznego?

**Sama motywacja i zaufanie nie wystarczą.** Nawet zaangażowany zespół może źle rozpoznać wymagania lub przeoczyć ryzyko. Potrzebuje również:

- kompetencji technicznych i szkoleń;
- czasu, zasobów i odpowiednich warunków pracy;
- regularnego kontaktu z klientem i użytkownikami;
- dobrego przepływu informacji i utrwalania wiedzy;
- wspólnych standardów projektowania, kodowania i testowania;
- regularnego sprawdzania, co w sposobie pracy trzeba poprawić.

<a id="pytanie-52"></a>

### 52. Czy utożsamianie jakości oprogramowania z zadowoleniem klienta w metodykach zwinnych jest słuszne?

**Zadowolenie klienta jest jednym z aspektów jakości.** Klient może dobrze ocenić produkt po demonstracji, choć produkt nie spełnia wymagań bezpieczeństwa lub potrzeb użytkowników końcowych. W omawianym ujęciu modelu Kano trzeba uwzględnić trzy grupy wymagań:

- **Wypowiedziane** — klient zna je i przekazuje wykonawcy.
- **Znane, lecz niewypowiedziane** — klient zakłada, że produkt je spełni.
- **Jeszcze nierozpoznane** — klient sam nie potrafi ich wskazać na początku.

Jakość trzeba więc ocenić również podczas rzeczywistej pracy z systemem.

<a id="pytanie-53"></a>

### 53. Jakie są podstawowe warunki zapewnienia jakości oprogramowania w metodykach zwinnych?

Podstawowe warunki zapewnienia jakości to:

1. **Codzienna współpraca** z klientami i użytkownikami przez cały proces.
2. **Cele wydań** wynikające z rzeczywistych wymagań.
3. Dobry **przepływ informacji** w zespole i między zainteresowanymi stronami, przez bezpośrednią współpracę lub częste kontakty.
4. Znajomość i stosowanie **standardów pracy inżynierskiej**.
5. Rygorystyczne **testy jednostkowe** przed każdym wydaniem.
6. **Testy akceptacyjne** z wybranymi użytkownikami przed rozpowszechnieniem.

W Scrumie ukończony przyrost musi spełniać uzgodnione kryteria **Definition of Done**.

<a id="pytanie-54"></a>

### 54. W jaki sposób problemy z klientem w metodykach zwinnych mogą wpłynąć negatywnie na jakość produktu?

Gdy kontakt z klientem jest nieregularny, zespół traci możliwość **sprawdzenia wymagań i uzyskania informacji zwrotnej**. Skutki pojawiają się na kilku etapach:

- Klient może żądać ustalenia zakresu, terminu i ceny, zanim zespół pozna szczegóły.
- Podczas analizy nie udaje się wyjaśnić wyjątków i niejednoznacznych wymagań.
- Przy planowaniu brakuje decyzji, które funkcje są najważniejsze.
- Podczas implementacji zespół czeka na decyzję albo buduje funkcję na podstawie własnych założeń.
- Po wydaniu błędne założenia wychodzą na jaw z opóźnieniem, czasem dopiero podczas pracy użytkowników.

Rezultatem mogą być zbędne funkcje, pominięte scenariusze, kosztowne poprawki i opóźnienia.

<a id="pytanie-55"></a>

### 55. Skąd mogą wynikać problemy z klientem w metodykach zwinnych?

Problemy we współpracy z klientem mogą wynikać z kilku przyczyn:

- **Niezrozumienie roli.** Klient zakłada, że wystarczy przekazać wymagania na początku.
- **Odległość i różne strefy czasowe.** Trudniej szybko wyjaśnić wątpliwości.
- **Niski priorytet projektu.** Przedstawiciel klienta ma za mało czasu na bieżącą współpracę.
- **Procedury i umowa.** Organizacja może oczekiwać z góry ustalonego zakresu, a warunki umowy mogą osłabiać motywację do udziału w kolejnych wydaniach.
- **Brak wiedzy lub uprawnień.** Wyznaczona osoba nie zna szczegółów pracy albo nie może podjąć decyzji.
- **Różne potrzeby.** Oczekiwania przedstawiciela odbiegają od tego, czego potrzebują użytkownicy.

Sama stała cena nie przesądza o zaangażowaniu klienta.

<a id="pytanie-56"></a>

### 56. Jak firmy stosujące metodyki zwinne sobie radzą przy problemach z klientem?

Firmy starają się utrzymać **dostęp do decyzji klienta** i ograniczyć skutki opóźnionych odpowiedzi. Mogą:

- wyjaśnić klientowi jego rolę i ustalić zasady odbioru oraz zmian zakresu;
- dopasować umowę, np. finansować kolejne wydania osobno;
- ocenić ryzyko braku kontaktu i zaplanować rezerwę czasu;
- wyznaczyć przedstawiciela zastępczego, np. analityka z dostępem do klienta;
- przypisać konkretnej osobie odpowiedzialność za wyjaśnienie danej opowieści;
- odłożyć opowieść, dopóki nie ma określonego celu, oczekiwanego wyniku i szczegółów potrzebnych do oszacowania pracy;
- regularnie pokazywać działający produkt i zbierać uwagi.

W Scrumie **Product Owner** odpowiada za wartość produktu i zarządzanie Product Backlogiem. Może pełnić tę rolę również osoba inna niż klient kontraktowy.

<a id="pytanie-57"></a>

### 57. Jak należy rozumieć formułowanie celów wydań na podstawie rzeczywistych wymagań klientów, a nie tylko ich opowieści?

**Cel wydania określa rezultat potrzebny użytkownikowi i warunki jego osiągnięcia.** Opowieść użytkownika wymaga doprecyzowania. Na przykład przy prośbie „chcę eksportować raport” trzeba ustalić:

- kto będzie korzystać z raportu i do czego;
- jakie dane mają się w nim znaleźć;
- w jakim formacie trzeba je przekazać;
- kto ma uprawnienia do eksportu;
- jak długo może trwać przygotowanie raportu;
- co system ma zrobić, gdy brakuje danych.

Z odpowiedzi wynikają **sprawdzalne kryteria akceptacji**. Pozwalają ocenić, czy wydanie spełnia rzeczywistą potrzebę.

<a id="pytanie-58"></a>

### 58. Jak zapewnić znajomość i stosowanie odpowiednich standardów pracy inżynierskiej w zespole zwinnym?

Żeby zespół **znał i stosował standardy inżynierskie**, trzeba włączyć je do codziennej pracy:

- spisać i udostępnić zasady kodowania, projektowania, integracji i testowania;
- szkolić nowych pracowników na przykładach z projektu;
- zapewnić wsparcie doświadczonych osób, np. podczas wspólnej pracy nad zmianą;
- sprawdzać stosowanie zasad podczas przeglądów kodu;
- uruchamiać analizę statyczną i testy przy integracji zmian;
- zapisywać decyzje projektowe, żeby wiedza była dostępna po zmianie składu zespołu.

Przydatność programowania w parach warto ocenić na podstawie wyników i kosztów w danym zespole.

<a id="pytanie-59"></a>

### 59. Czy rygorystyczne testowanie w metodykach zwinnych jest wystarczające dla zapewnienia jakości oprogramowania?

**Samo rygorystyczne testowanie nie wystarcza do zapewnienia jakości.**

- Testy mogą opierać się na **niepełnych wymaganiach** i pomijać istotne dane oraz scenariusze. Program napisany „pod testy” może je przechodzić, a mimo to nie zaspokajać potrzeb użytkowników.
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

Trudności pojawiają się zwłaszcza przy **wysokim ryzyku, ograniczonej możliwości aktualizacji lub utrudnionej współpracy**. Przykłady projektów, w których trzeba uzupełnić typowe praktyki zwinne:

- **Aparat do radioterapii** — błędna dawka zagraża pacjentowi, więc przed użyciem trzeba zweryfikować zabezpieczenia.
- **Sterowanie samolotem** — funkcje krytyczne wymagają analizy zagrożeń i dowodów bezpieczeństwa.
- **Sonda kosmiczna** — po starcie możliwość aktualizowania produktu może być ograniczona.
- **Projekt bez dostępnego klienta** — zespół nie może na bieżąco wyjaśniać wymagań i sprawdzać rezultatów.
- **System utrzymywany latami przez kolejne zespoły** — potrzebna jest dokumentacja, z której następcy odtworzą decyzje i sposób działania.

Duża, rozproszona organizacja może dodatkowo utrudniać współpracę. Rozwój iteracyjny pozostaje możliwy, jeśli proces zapewnia wymaganą weryfikację, dokumentację i kontakt z użytkownikami.

<a id="pytanie-62"></a>

### 62. Jakie są wady/zagrożenia dla procesu wytwarzania w metodykach zwinnych?

Zagrożenia dla jakości w projekcie zwinnym obejmują m.in.:

- **Zależność od konkretnych osób.** Wraz z odejściem pracownika może zniknąć wiedza potrzebna do dalszej pracy.
- **Braki w dokumentacji.** Po przerwie trudno wznowić projekt lub przekazać go innemu zespołowi.
- **Pominięcie wymagań jakościowych i wyjątków.** Błąd projektu może ujawnić się dopiero podczas eksploatacji.
- **Słaby kontakt z klientem.** Zespół z opóźnieniem dowiaduje się, że źle zrozumiał potrzebę.
- **Presja terminu.** Odkładanie poprawek i ograniczanie testów prowadzi do długu technicznego.
- **Koszt ciągłych zmian.** Wielokrotne przeróbki mogą wyczerpać budżet.
- **Trudności komunikacyjne.** Odległość i różne strefy czasowe utrudniają uzgadnianie decyzji.

To ryzyka zależne od sposobu prowadzenia projektu. W Scrumie ukończony przyrost musi spełniać **Definition of Done**, a jakość nie powinna spadać podczas Sprintu.

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
