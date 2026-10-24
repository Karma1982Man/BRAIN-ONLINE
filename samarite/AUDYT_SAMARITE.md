---
title: "Audyt widoczności i sprzedaży — Samarité (samarite.eu)"
subtitle: "Wersja 2 — po weryfikacji drugiej opinii"
date: "23.10.2026"
---

# Podsumowanie

Cel marki: **jak najwięcej sprzedaży przez własny sklep samarite.eu**, lepsza widoczność w Google i większa szansa na polecenia przez AI (ChatGPT, Google AI, Perplexity).

**Najpoważniejsze znalezione problemy** (to nie jest ranking strat finansowych — ten wymaga danych sprzedażowych, patrz pkt 1):

1. **Ciężkie filmy na stronie głównej** — w teście mobilnym pobrało się 12 plików wideo (19,4 MB, ok. 90% wagi strony), w tym wersje desktopowe; strona: wynik 35/100, główna treść po 14,1 s (test laboratoryjny).
2. **„Najniższa cena z 30 dni: 0,00” przy zestawach** — wymaga pilnej korekty.
3. **Dane produktów dla Google** — opis w danych strukturalnych to lista fraz, brak EAN w kodzie strony, jeden adres oferty dla różnych wariantów.

**Największa luka:** nie zbadano jeszcze ścieżki zakupu (koszyk, płatność, porzucenia, powtórne zakupy, marża). Pod cel „sprzedaż na samarite.eu” to pierwszy krok — pkt 1.

# Metoda i ograniczenia

- Sprawdzone 23.10.2026 bezpośrednio na samarite.eu: kod stron (strona główna, Divine Cream w obu wariantach, Divine Elixir, Eksperci, artykuł blogowy), robots.txt, sitemap.xml, llms.txt, dane strukturalne schema.org.
- Szybkość: Lighthouse 12, emulacja telefonu (test laboratoryjny). **To nie są dane prawdziwych użytkowników** — te są w Google Search Console → Podstawowe wskaźniki internetowe.
- Rynek i konkurencja: wyszukiwanie w sieci (rankingi Elle, Superpharm, Wizaż, natu.care, sklepy).
- **Nie sprawdzono:** Search Console, Merchant Center, Google Ads, GA4, systemu sklepu, ścieżki zakupu do płatności, marży, logów serwera, wolumenów fraz, odpowiedzi AI na pytania klientek.
- Oznaczenie **WYMAGA SPRAWDZENIA** = hipoteza do potwierdzenia danymi.

# Fakty o marce (sprawdzone)

- Polska marka, firma: **Zeme Pharm Anna Mrowińska**, Warszawa. Butik: Westfield Mokotów (poziom 0).
- Pozycjonowanie: „Słowiańska pielęgnacja w cyklu 8 kroków”, 33 zioła, multifunkcyjność („mniej kosmetyków, więcej możliwości”).
- Oceny **wyświetlane** w sklepie (autentyczności i sposobu zbierania nie weryfikowano): Grand Divine Cream 4,9/5 (2096 opinii), Supreme Balm 5,0 (1081), Supreme Cleanser 5,0 (647), Divine Elixir 5,0 (1292).
- Zewnętrznie: Wizaż KWC — Divine Cream 4,5/5 (ok. 407 opinii); Glamour: „krem sprzedaje się co 7 minut”. Część testów Wizaż była sponsorowana, większość tekstów ma 1,5–2,5 roku.
- W wynikach na nazwę produktu pojawia się negatywna recenzja blogowa „Divine Cream – nieudana inwestycja” (mojalepszawersja.pl, 2020).
- Eksperci na stronie: mgr chemii Barbara Zapisek (główny technolog), dr n. med. Marcin Wrona (ginekolog, endokrynolog).
- Google Ads: marka prowadzi kampanię na własną nazwę (`perfo_sea_brand_exact` w linku z reklamy).
- Strona Divine Cream: domyślnie wybrany wariant **Grand 2×45 ml — 269,99 zł**; wariant **45 ml (`?v=793`) — 149,99 zł**. Dane strukturalne zmieniają cenę zgodnie z wybranym wariantem.
- Promocje widoczne jednocześnie: 15% za zapis do newslettera, „2+1 / kod TRIO” (najtańszy za 1 gr), zestawy z ceną niższą od sumy produktów.

# Problemy i działania

Legenda: **P1** = 1. tydzień, **P2** = tydzień 2–4, **P3** = 2. miesiąc.

## 1. Ścieżka zakupu i dane sprzedażowe — P1 (najpierw)

To diagnoza, która pokaże, gdzie sklep realnie traci pieniądze. Bez niej pozostałe priorytety są oparte na obserwacjach strony, nie na wynikach.

| Co dokładnie | Gdzie | Dlaczego |
|---|---|---|
| Przejść zakup na 2–3 telefonach (iOS/Android): wybór wariantu → koszyk → kod rabatowy → dostawa → płatność | Sklep | Błąd na tym etapie traci klientki już gotowe do zakupu. **Obecność błędów: WYMAGA SPRAWDZENIA** |
| Porównać zamówienia i przychód z systemu sklepu z GA4 | Panel sklepu, GA4 | Czy pomiar jest wiarygodny, zanim na nim oprzemy decyzje |
| Lejek zakupu wg urządzenia i źródła ruchu: wejście → karta → koszyk → checkout → zakup | GA4 | Pokazuje, na którym etapie i na jakim urządzeniu odpadają klientki |
| Sprawdzić nieudane płatności i porzucone koszyki | Panel sklepu / operator płatności | Bezpośrednio utracona sprzedaż |
| Najważniejsze strony wejścia (z reklam i Google) | GA4, Search Console | Optymalizować te strony w pierwszej kolejności, nie tylko stronę główną |

## 2. Cena „Najniższa cena z 30 dni: 0,00” — P1

- **Gdzie:** 8 zestawów na /pl/shop/sets: Mini Basic Set, Holy Grail Set, Anti-Aging Set, Supreme Gift Set, Supreme Help Kit, Longevity Set, Ready to Go Set, All Set; także strona główna („Zestawy prezentowe”) i sekcje „Dostępny w zestawie” na kartach produktów. Produkty pojedyncze mają poprawne wartości.
- **Co zrobić:**
  - Sprawdzić historię cen każdego zestawu i rodzaj komunikacji (obniżka ceny zestawu czy porównanie z sumą produktów kupowanych osobno).
  - Jeśli to obniżka — pokazać rzeczywistą najniższą cenę z 30 dni przed obniżką.
  - Jeśli to tylko porównanie z sumą produktów — nie wyświetlać pola „0,00”, a porównanie opisać jednoznacznie.
  - Nie wpisywać mechanicznie przypadkowej kwoty.
- **Dlaczego:** wiarygodność oferty i zgodność z przepisami o informowaniu o obniżkach (Omnibus). **Ocenę prawną potwierdzić z prawnikiem.**
- Źródło: [UOKiK — informacje o obniżkach cen](https://prawakonsumenta.uokik.gov.pl/prawo-do-informacji/informacje-o-obnizkach-cen/)

## 3. Szybkość — strona główna i karty produktów — P1

**Dane prawdziwych użytkowników (PageSpeed Insights, telefony, 28 dni, stan 23.10.2026) — rozstrzygające:**

| Wskaźnik | Wynik | Norma Google | Ocena |
|---|---|---|---|
| LCP (wyświetlenie głównej treści) | 1,6 s | ≤ 2,5 s | dobrze |
| INP (reakcja na dotyk) | 220 ms | ≤ 200 ms | do poprawy |
| CLS (przesunięcia układu) | 0,14 | ≤ 0,1 | do poprawy |

Ocena Core Web Vitals: **niezaliczona** (przez INP i CLS). Wniosek o LCP 14,1 s z testu laboratoryjnego nie dotyczy prawdziwych użytkowników; test laboratoryjny pozostaje użyteczny do wykrycia wagi wideo i blokowania przez skrypty.

**Wyniki testu laboratoryjnego (Lighthouse, emulacja telefonu):**

| Strona | Wynik | Wczytanie głównej treści (LCP) | Waga | Blokada skryptów (TBT) |
|---|---|---|---|---|
| Strona główna /pl | 35/100 | 14,1 s | 21,4 MB | 3,2 s |
| Divine Cream | 47/100 | 5,4 s | 9,4 MB | 0,9 s |

Norma Google dla dobrego LCP: ≤ 2,5 s.

**Co ustalono:**

- W teście mobilnym pobrało się **12 plików wideo — 19,4 MB** (ok. 90% wagi strony): `film-o-marce-baner-desktop.mov` (6,1 MB, wersja desktopowa), `baner-bajka-1080x2400-cta.mp4` (6,0 MB), `film-koe-desktop.mov` (3,6 MB, wersja desktopowa), `film-koe-mobile.mov` (3,4 MB). MB = 1024 KiB.
- Odpowiedź serwera: 140 ms — **serwer nie jest przyczyną**.
- Skrypty zewnętrzne (Google Tag Manager, gtag) blokują stronę na 1,15 s; ok. 450 KB nieużywanego JavaScriptu.
- **Nie ustalono**, który element odpowiada za LCP — Lighthouse go nie wskazał. Dlatego nie da się z góry podać, ile sekund przyniesie sama optymalizacja filmów.

**Co zrobić:**

1. Ustalić element LCP (PageSpeed Insights / Chrome DevTools → Performance) dla strony głównej i najważniejszych kart produktów.
2. Przekonwertować filmy do MP4 (H.264) i/lub WebM, cel ≤ 1–1,5 MB każdy; na telefonie nie ładować wersji desktopowych.
3. Filmy **poniżej pierwszego ekranu**: obraz zastępczy (poster) + ładowanie po wejściu w widok. **Elementu LCP nie ładować leniwie** — to by go opóźniło.
4. Przejrzeć tagi w GTM, usunąć nieużywane.
5. Powtórzyć pomiar i sprawdzić raport Core Web Vitals w Search Console (dane realnych użytkowników).

**Dlaczego:** ciężkie strony na telefonie zwiększają ryzyko porzucenia wizyty, w tym wizyt opłaconych reklamą. Źródła: [Web Vitals](https://web.dev/articles/vitals), [metryki wydajności](https://web.dev/articles/user-centric-performance-metrics).

## 4. Merchant Center — P1

Właścicielka ma dostęp. Sprawdzić:

- Diagnostykę: odrzucone produkty, niezgodności ceny i dostępności, warianty, linki prowadzące do właściwego wariantu.
- Czy przekazywane są **GTIN/EAN** — jeśli produkt ma nadany kod, przekazać właściwy dla danego produktu lub zestawu; **nie wymyślać kodów**. Brak w kodzie strony nie przesądza o braku w Merchant Center.
- Czy włączone są bezpłatne informacje o produktach.
- Program **Product Ratings** (oceny produktów w Zakupach): sprawdzić wymagania i czy sklep może przekazywać opinie. Gwiazdki są możliwym efektem, **nie gwarancją** — Google decyduje o wyświetleniu, a liczba i średnia mogą się różnić od tych w sklepie.

Źródła: [GTIN](https://support.google.com/merchants/answer/6324461?hl=en), [Product Ratings](https://support.google.com/merchants/answer/6098512?hl=en)

## 5. Dane produktów na stronie (schema.org) — P2

| Problem | Stan (sprawdzony) | Poprawka |
|---|---|---|
| Opis w danych Product | Divine Cream: „krem do twarzy, krem na dzień, krem na noc, …, dla nastolatków”; Divine Elixir: „tonik, esencja, aktywator młodości, …” | Normalny opis 1–3 zdania |
| Adres oferty wariantów | Wariant 45 ml i Grand mają ten sam `offers.url` bez parametru wariantu | Osobny adres dla każdego wariantu (np. `?v=793`) zgodnie z wytycznymi Google dla wariantów |
| Podwójny ukośnik | `https://samarite.eu//pl/...` w okruszkach i ofercie | `https://samarite.eu/pl/...` |
| GTIN/EAN | Brak w kodzie strony | Dodać, jeśli kody istnieją |
| Marka | „Samarite” | „Samarité” |

Źródła: [dane produktów](https://developers.google.com/search/docs/appearance/structured-data/product), [warianty produktów](https://developers.google.com/search/blog/2024/02/product-variants)

## 6. Polityka promocji i marża — P2

- Jednocześnie działają: 15% za newsletter, 2+1 (kod TRIO), zestawy poniżej sumy produktów, obniżki na bestsellerach.
- **Co zrobić:** policzyć, czy rabaty się łączą; marżę po rabatach, reklamie i obsłudze zamówienia; udział nowych i powracających klientek; czy nowe klientki kupują ponownie bez kolejnej dużej zniżki.
- Rozdzielić wyniki kampanii na nazwę marki i pozostałych.
- **Dlaczego:** wysoki przychód lub ROAS nie mówi, czy sprzedaż jest dodatkowa i rentowna. **Stan obecny: WYMAGA SPRAWDZENIA.**

## 7. E-mail i SMS — P2

Sprawdzić, czy działają i jak konwertują:

- seria powitalna po zapisie (kod 15%),
- porzucony koszyk,
- instrukcja użycia po zakupie (np. jak łączyć Divine Cream z Elixirem),
- przypomnienie o ponownym zamówieniu (po czasie zużycia produktu),
- prośba o opinię.

**Stan obecny: WYMAGA SPRAWDZENIA.** To rozwój sprzedaży z istniejącego ruchu i bazy — bez dodatkowych kosztów reklamy.

## 8. Deklaracje marketingowe (claims) — P2

Przykłady ze stron produktów:

- „JEDYNY KREM DO TWARZY ODPOWIADAJĄCY NA ABSOLUTNIE WSZYSTKIE POTRZEBY SKÓRY”
- „inteligentna formuła identyfikuje potrzeby skóry”
- „ZASTĘPUJE 5 INNYCH KREMÓW”
- „100%* Dogłębnie nawilża przez 48h” — przypis „% osób potwierdzających rezultaty na podstawie badań aplikacyjnych lub aparaturowych” bez liczby badanych i czasu badania
- Divine Cream polecany dla skóry wrażliwej; skład zawiera składniki zapachowe (m.in. limonene, coumarin wg INCIDecoder)

**Co zrobić:** przegląd deklaracji razem z dokumentacją badań. Przy każdym „%” podać liczbę osób, czas, rodzaj badania. Oczywista hiperbola reklamowa może być dopuszczalna, ale twierdzenia o działaniu wymagają dowodów, a przypisywanie wyjątkowości cechom wspólnym z innymi produktami jest niedozwolone. Deklaracje „naturalności” opierać na ISO 16128.

**Dlaczego:** Rozporządzenie (UE) 655/2013. **Nie przesądzam naruszenia — ocenę potwierdzić z prawnikiem.** Źródło: [Rozporządzenie 655/2013](https://eur-lex.europa.eu/eli/reg/2013/655/oj/eng/pdf)

## 9. Sprzeczne sygnały: robots.txt vs sitemap i hreflang — P2

- robots.txt blokuje: `/de/`, `/at/`, `/fr/`, `/it/`, `/es/`, `/nl/` i 18 innych krajów.
- Jednocześnie sitemap.xml zawiera **48 adresów /de**, a znaczniki hreflang wskazują wszystkie 30 wersji.
- **Decyzja:** jeśli Niemcy/Austria/inne kraje są rynkiem docelowym → odblokować; jeśli nie → usunąć te adresy z sitemap i hreflang.

## 10. Strona główna, tytuły i opisy — P2

**Strona główna:**

- Brak nagłówka H1. Propozycja: „Samarité – polskie kosmetyki naturalne: krem do twarzy i pod oczy, eliksir, balsam”.
- 25 z 52 zdjęć bez opisu (alt); na karcie Divine Cream 74 ze 131.

**Tytuły i opisy (obecny → problem → propozycja):**

| Obecnie | Problem | Propozycja |
|---|---|---|
| „Divine Cream - Krem do twarzy i pod oczy, na dzień i na noc \| Samarité \| Samarite” | Marka 2×, 81 znaków — ucinany | „Divine Cream – krem do twarzy i pod oczy, dzień i noc \| Samarité” |
| Opis: „Divine Cream - Krem do twarzy i pod oczy, na dzień i na noc. Sprawdź ofertę naturalnych kosmetyków Samarité!” (ten sam szablon na każdej karcie) | Brak powodu do kliknięcia | „Krem do twarzy i pod oczy na dzień i noc. 4,9/5 z ponad 2000 opinii w naszym sklepie. 33 zioła i niacynamid. Darmowa dostawa.” |
| Tytuł bloga: „KREM NA ZMARSZCZKI: JAK WYBRAĆ NAJLEPSZY KREM DOSTOSOWANY DO WIEKU I POTRZEB SKÓRY \| Samarite” | 93 znaki, wersaliki | „Krem na zmarszczki – jak wybrać do wieku i skóry \| Samarité” |
| Opis artykułu zaczyna się od `**Zanim wybierzesz…` | Znaczniki formatowania w opisie | Usunąć `**` |

Wpływ na sprzedaż: pośredni (klikalność z Google) — mierzyć CTR w Search Console przed i po.

## 11. Dane o marce, eksperci, mapa strony — P3

- **Organization:** na stronie głównej tylko LocalBusiness (butik). Organization (na blogu) ma opis po angielsku. Dodać na stronie głównej: name „Samarité”, alternateName „Samarite”, legalName „Zeme Pharm Anna Mrowińska”, polski opis, `sameAs` → Instagram, Facebook, TikTok, YouTube, profil na Wizaż.
- **Niespójność:** foundingDate 2019 w danych vs „od 8 lat” w tekście strony głównej — ujednolicić.
- **Eksperci:** literówka „eksperów Samaritè” → „ekspertów Samarité”; autor w danych artykułu: „mgr chemii\nBARBARA ZAPISEK -\nGŁÓWNY TECHNOLOG” → name „Barbara Zapisek”, jobTitle „Główny technolog”.
- **sitemap.xml:** 56 z 320 adresów (m.in. strona główna, sklep, blog) ma zastępczą datę `2025-01-01` — generować prawdziwe daty zmian.

## 12. Widoczność w AI (ChatGPT, Google AI, Perplexity) — P2/P3

**Nie ma metody gwarantującej polecenie marki przez AI.** Można zwiększyć dostępność i jakość informacji.

**Stan:**

- robots.txt nie blokuje botów AI. Test z identyfikatorami OAI-SearchBot, GPTBot, PerplexityBot i Googlebot zwrócił stronę (200), **ale test podszywał się tylko pod nazwę bota** — prawdziwe boty mogą być filtrowane przez zabezpieczenia serwera/CDN. **WYMAGA SPRAWDZENIA w logach serwera.**
- Plik llms.txt istnieje — **niski priorytet**: Google informuje, że do AI Overviews/AI Mode nie są potrzebne specjalne pliki ani dodatkowe schema.
- Blog ma autora, datę, dane Article, FAQ i linki do produktów — dobry fundament.

**Co zrobić:**

- **P2:** spójne dane produktów (pkt 5) i jasne opisy: dla kogo, zastosowania, skład, zapach, sposób użycia, podsumowania badań (metoda, liczebność, czas, wynik).
- **P2:** FAQ na kartach produktów odpowiadające na obawy z opinii: „czy można pod oczy” (są skargi na szczypanie), „czy dla cery wrażliwej”, „czy w ciąży”, „jak łączyć z Elixirem”.
- **P3:** rzetelne testy i porównania w mediach (z ujawnieniem współpracy). W sprawdzonych zestawieniach (Elle, Superpharm, natu.care, Wizaż TOP) polecana jest konkurencja. To kierunek budowania rozpoznawalności, **nie potwierdzona recepta na cytowanie przez AI**.
- **P3 — pomiar:** co miesiąc te same neutralne pytania w nowych rozmowach (ChatGPT, Perplexity, Google); zapisywać datę, odpowiedź, źródła, wskazany sklep. Pojedyncza odpowiedź AI nie jest stabilnym rankingiem.

Źródła: [Google — AI features](https://developers.google.com/search/docs/appearance/ai-features), [OpenAI — boty](https://developers.openai.com/api/docs/bots), [Perplexity — boty](https://docs.perplexity.ai/docs/resources/perplexity-crawlers)

# Frazy kluczowe — kandydaci do weryfikacji

To **nie jest potwierdzona lista szans**. Najpierw sprawdzić w Search Console zapytania, które już dają wyświetlenia, wejścia i zakupy, a wolumeny nowych fraz w Planerze słów kluczowych.

| Grupa | Przykłady | Docelowe miejsce |
|---|---|---|
| Marka i produkt | samarite divine cream, samarite opinie, divine cream opinie, samarite skład | Karta produktu i opinie |
| Zastosowanie | krem do twarzy i pod oczy, krem na dzień i na noc w jednym, krem z niacynamidem | Karta produktu i poradnik wyboru |
| Prezent | zestaw kosmetyków na prezent, kosmetyki na prezent do 150 zł, prezent dla mamy | Sekcja prezentowa / zestawy |
| Kategoria | polskie kosmetyki naturalne, słowiańskie kosmetyki | Strona marki, treści o ofercie |

**Reklama na nazwę marki:** Google Ads → Statystyki aukcji. Jeśli konkurencja nie licytuje „samarite”, a strona jest na 1. miejscu w bezpłatnych wynikach — przetestować niższy budżet przez 2–4 tygodnie i porównać łączną sprzedaż z wyszukiwań na markę.

# Konkurencja (z rankingów i artykułów, nie z danych o udziale w rynku)

| Segment | Marki |
|---|---|
| Słowiańskie / ziołowe | Mokosh, Slavia Cosmetics, Polny Warkocz, Kwiat Paproci |
| Naturalne anti-aging (PL) | Orientana, Resibo, Iossi, Veoli Botanica |
| Polskie premium dermo | Dr Irena Eris, Dr Ambroziak |

Dystrybucja: perfumeria.pl ma 2 produkty Samarité (oba niedostępne); marka jest też w innych sklepach (eZebra, Minti Shop, Topestetic, MUA Store, Ceneo). **Udział kanałów w sprzedaży nieznany.**

# Plan wdrożenia

| Termin | Działania | Miernik |
|---|---|---|
| Tydzień 1 | Pkt 1 (ścieżka zakupu, dane), 2 (cena „0,00”), 3 (diagnoza LCP + filmy), 4 (Merchant Center) | Lista błędów zakupu; poprawne ceny; LCP na kluczowych stronach; 0 odrzuceń w Merchant Center |
| Tydzień 2–4 | Pkt 5, 6, 7, 8, 9, 10 | Konwersja wg urządzenia; marża po rabatach; przychód z e-maili; CTR w Search Console |
| Miesiąc 2 | Pkt 11, 12 (FAQ, media, pomiar AI) | Obecność w zestawieniach; test AI co miesiąc |

**Mierzyć co miesiąc:** przychód, konwersja i średni koszyk (sklep + GA4), udział powracających klientek, marża po rabatach i reklamie, ruch bezpłatny (Search Console), kliknięcia z Zakupów Google, wynik testu AI.

# Źródła

- samarite.eu: /pl, /pl/product/divine-cream, /pl/product/divine-cream?v=793, /pl/product/divine-elixir, /pl/experts, /pl/blog/krem-na-zmarszczki, /robots.txt, /sitemap.xml, /llms.txt
- Wizaż – Divine Cream: https://wizaz.pl/kosmetyki/produkt,307802,samarite-divine-cream.html
- Glamour: https://www.glamour.pl/uroda/przetestowalam-krem-ktory-sprzedaje-sie-w-polsce-co-7-minut/
- Recenzja negatywna: https://www.mojalepszawersja.pl/2020/04/samarite-divine-cream-nieudana.html
- INCI: https://incidecoder.com/products/samarite-divine-cream
- Superpharm: https://www.superpharm.pl/blog/naturalny-krem-do-twarzy-jaki-wybrac-polecane-produkty
- Elle – marki naturalne: https://www.elle.pl/uroda/najlepsze-kremy-nawilzajace-do-twarzy-od-polskich-marek-naturalnych-przeglad-i-opinie/
- Elle – kremy 40+: https://www.elle.pl/uroda/ranking-6-polecanych-polskich-kremow-do-pielegnacji-skory-40-kosztuja-od-14-do-249-zl/
- natu.care: https://natu.care/pl/kosmetyki/krem-do-twarzy
- puderikrem.pl: https://puderikrem.pl/Polskie-kosmetyki-naturalne-i-dermokosmetyki-ranking-TOP-18-marek-ktore-musisz-znac-blog-pol-1733397695.html
- perfumeria.pl: https://www.perfumeria.pl/collections/samarite
- Google, UOKiK, EUR-Lex, OpenAI, Perplexity — linki w odpowiednich sekcjach.

# Zmiany względem wersji 1

- Wersja 2.1: poprawione dane o filmach (3 pliki .mov i 1 .mp4 wśród największych; 19,4 MB wideo), wagi stron w MB (1024 KiB) oraz zakres zastępczej daty w mapie strony (56 z 320 adresów).

- Wycofano zarzut „błędnej ceny Divine Cream” — cena w danych odpowiada wybranemu wariantowi (Grand 269,99 zł / 45 ml 149,99 zł). Pozostaje problem wspólnego adresu oferty dla wariantów.
- „3 największe straty” → „najpoważniejsze znalezione problemy” (bez danych sprzedażowych nie da się ustalić strat).
- Usunięto obietnicę „szybciej o kilkanaście sekund”; dodano diagnozę elementu LCP i zakaz leniwego ładowania elementu LCP.
- Gwiazdki w Google — możliwość, nie gwarancja; GTIN — sprawdzić w Merchant Center, nie wymyślać.
- Doprecyzowano kwestie prawne (porównanie zestawu vs obniżka; hiperbola vs twierdzenia o działaniu).
- Wycofano wniosek, że dystrybutorzy „nie zabierają sprzedaży”.
- Test botów AI opisany jako podszycie pod nazwę bota — wymaga potwierdzenia w logach.
- Dodano: ścieżkę zakupu i dane sprzedażowe (pkt 1), politykę promocji i marżę (pkt 6), e-mail/SMS (pkt 7), przykłady „obecnie → propozycja” dla tytułów i opisów.
