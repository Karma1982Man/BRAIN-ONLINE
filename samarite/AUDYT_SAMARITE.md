---
title: "Audyt widoczności i sprzedaży — Samarité (samarite.eu)"
date: "23.10.2026"
---

# Podsumowanie

Cel marki: **jak najwięcej sprzedaży przez własny sklep samarite.eu**, lepsza widoczność w Google i polecenia przez AI (ChatGPT, Google AI, Perplexity).

**3 największe straty:**

1. **Strona główna na telefonie ładuje się ok. 14 s** (wynik 35/100, 21,9 MB) — głównie przez 4 filmy .mov (~19 MB).
2. **Błędne dane produktu Divine Cream dla Google** — zła cena (269,99 zł zestawu Grand zamiast ceny 45 ml), brak EAN, opis = lista słów. Psuje Google Zakupy i wyniki z AI.
3. **Ryzyko prawne:** „Najniższa cena z 30 dni: 0,00” przy zestawach (Omnibus) oraz deklaracje typu „JEDYNY krem na ABSOLUTNIE WSZYSTKIE potrzeby skóry”.

**3 najszybsze wygrane:**

1. Kompresja/lazy-load filmów → strona szybsza o kilkanaście sekund na telefonie.
2. Gwiazdki 4,9/5 z 2096 opinii widoczne w Google (Merchant Center + oceny produktów).
3. Poprawa tytułów, opisów i nagłówka H1 — praca na godziny, nie tygodnie.

# Metoda i ograniczenia

- Sprawdzone 23.10.2026 bezpośrednio na samarite.eu: kod stron (strona główna, Divine Cream, Divine Elixir, Eksperci, artykuł blogowy), robots.txt, sitemap.xml, llms.txt, dane strukturalne (schema.org), dostęp botów AI.
- Szybkość: Lighthouse 12 (test laboratoryjny, profil mobilny). **To nie są dane prawdziwych użytkowników** — te są w Google Search Console → Podstawowe wskaźniki internetowe.
- Rynek i konkurencja: wyszukiwanie w sieci (rankingi Elle, Superpharm, Wizaż, natu.care, sklepy).
- **Nie sprawdzono:** Search Console, Merchant Center, Google Ads, GA4 (brak dostępu), realnych wolumenów fraz, odpowiedzi ChatGPT/Google AI na pytania klientek (do zrobienia — patrz sekcja „Kolejne kroki”).

# Fakty o marce (sprawdzone)

- Polska marka, firma: **Zeme Pharm Anna Mrowińska**, Warszawa. Butik: Westfield Mokotów (poziom 0).
- Pozycjonowanie: „Słowiańska pielęgnacja w cyklu 8 kroków”, 33 zioła, multifunkcyjność („mniej kosmetyków, więcej możliwości”).
- Bestsellery na stronie: Grand Divine Cream 4,9/5 (2096 opinii), Supreme Balm 5,0 (1081), Supreme Cleanser 5,0 (647), Divine Elixir 5,0 (1292).
- Zewnętrznie: Wizaż KWC — Divine Cream 4,5/5 (ok. 407 opinii); Glamour: „krem sprzedaje się co 7 minut”. Część testów Wizaż była sponsorowana, większość tekstów ma 1,5–2,5 roku.
- W wynikach na nazwę produktu pojawia się negatywna recenzja blogowa „Divine Cream – nieudana inwestycja” (mojalepszawersja.pl, 2020).
- Eksperci na stronie: mgr chemii Barbara Zapisek (główny technolog), dr n. med. Marcin Wrona (ginekolog, endokrynolog).
- Google Ads: marka płaci za kampanię na własną nazwę (`perfo_sea_brand_exact` w linku z reklamy).
- Dystrybucja: perfumeria.pl ma tylko 2 produkty Samarité, oba niedostępne — sieci praktycznie nie zabierają sprzedaży.

# Problemy i działania

Legenda: **P1** = zrobić w 1. tygodniu, **P2** = 2–4 tydzień, **P3** = 2. miesiąc.

## 1. Szybkość strony na telefonie — P1

| Strona | Wynik | Wczytanie głównej treści (LCP) | Waga | Blokada skryptów (TBT) |
|---|---|---|---|---|
| Strona główna /pl | 35/100 | 14,1 s | 21,9 MB | 3,2 s |
| Divine Cream | 47/100 | 5,4 s | 9,7 MB | 0,9 s |

Norma Google dla dobrego wyniku: LCP ≤ 2,5 s.

**Przyczyny (strona główna):**

- `baner-bajka-1080x2400-cta-....mov` — 6,1 MB
- `film-o-marce-baner-desktop-....mov` — 6,1 MB
- `film-koe-desktop-....mov` — 3,5 MB (wczytywany także na telefonie)
- `film-koe-mobile-....mov` — 3,1 MB
- Skrypty zewnętrzne (Google Tag Manager, gtag) blokują stronę na 1,15 s; ok. 450 KB nieużywanego JavaScriptu.

**Co zrobić:**

- Przekonwertować filmy do MP4 (H.264) i/lub WebM, cel ≤ 1–1,5 MB każdy.
- Dodać obraz zastępczy (poster) i ładować film dopiero po wejściu w widok lub po kliknięciu; `preload="none"`.
- Na telefonie nie ładować wersji desktopowych.
- Przejrzeć tagi w GTM i usunąć nieużywane.
- Po wdrożeniu: sprawdzić PageSpeed Insights i raport Core Web Vitals w Search Console.

**Dlaczego:** wolna strona na telefonie = porzucone wizyty i koszyki, za które marka często płaci reklamą. Szybkość jest też czynnikiem w Google.

## 2. „Najniższa cena z 30 dni: 0,00” — P1

- **Gdzie:** zestawy Mini Basic Set, Holy Grail Set, Anti-Aging Set, Ready to Go Set, All Set (widoczne na stronie głównej i kartach produktów).
- **Co zrobić:** wyświetlać rzeczywistą najniższą cenę z 30 dni przed obniżką.
- **Dlaczego:** wymóg dyrektywy Omnibus / ustawy o informowaniu o cenach. „0,00” przy prezentowaniu obniżki to ryzyko kontroli i kary (**wymaga potwierdzenia z prawnikiem**).

## 3. Dane produktu Divine Cream (strona `/pl/product/divine-cream`) — P1

| Problem | Stan | Poprawka |
|---|---|---|
| Nagłówek H1 | „GRAND DIVINE CREAM” na stronie Divine Cream | H1 zgodny z produktem lub wyraźny wybór wariantu |
| Cena w danych dla Google | „DIVINE CREAM” za 269,99 zł (cena zestawu Grand 2×45 ml) | Osobne warianty z własnymi cenami (ProductGroup / hasVariant lub osobne Offer) |
| Kod EAN (GTIN) | Brak | Dodać EAN każdego produktu |
| Opis w danych Product | Lista słów: „krem do twarzy, krem na dzień, …, dla nastolatków” | Normalny opis 1–3 zdania |
| Adresy w danych | `https://samarite.eu//pl/...` (podwójny ukośnik) w okruszkach i ofercie | Poprawić na `https://samarite.eu/pl/...` |
| Marka w danych | „Samarite” | „Samarité” (alternateName: „Samarite”) |

**Dlaczego:** Google Zakupy, darmowe wyniki produktowe i odpowiedzi AI biorą cenę i opis z tych danych. Niezgodna cena = odrzucenia w Merchant Center i dezorientacja klientki.

## 4. Merchant Center i gwiazdki w Google — P1/P2

- Sprawdzić w Merchant Center: diagnostykę (odrzucone produkty, niezgodność ceny), czy włączone są **bezpłatne informacje o produktach** i **oceny produktów**.
- 2096 opinii 4,9/5 to najmocniejszy argument sprzedażowy — powinny wyświetlać się w Google przy cenie.
- Uzupełnić w feedzie: GTIN, warianty, zdjęcia, darmowa dostawa, czas dostawy, zwroty.

## 5. Deklaracje marketingowe (claims) — P1

Przykłady ze stron produktów:

- „JEDYNY KREM DO TWARZY ODPOWIADAJĄCY NA ABSOLUTNIE WSZYSTKIE POTRZEBY SKÓRY”
- „inteligentna formuła identyfikuje potrzeby skóry”
- „ZASTĘPUJE 5 INNYCH KREMÓW”
- „100%* Dogłębnie nawilża przez 48h” — przypis bez liczby badanych, czasu i metody
- Divine Cream rekomendowany dla skóry wrażliwej; skład zawiera składniki zapachowe (m.in. limonene, coumarin wg INCIDecoder)

**Co zrobić:**

- Przy każdym „%” podać: liczbę osób, czas badania, rodzaj (aparaturowe/aplikacyjne), laboratorium.
- Stopnie najwyższe („jedyny”, „absolutnie wszystkie”) złagodzić lub udokumentować.
- Informację „naturalne / X% składników naturalnych” opierać na normie ISO 16128.

**Dlaczego:** Rozporządzenie (UE) 655/2013 — deklaracje kosmetyczne muszą być prawdziwe i poparte dowodami. UOKiK aktywnie sprawdza greenwashing i wprowadzające w błąd obietnice (**wymaga potwierdzenia z prawnikiem**).

## 6. Zablokowane wersje krajowe — P2

- robots.txt blokuje: `/de/`, `/at/`, `/fr/`, `/it/`, `/es/`, `/nl/` i 18 innych krajów.
- Jednocześnie: sitemap.xml zawiera **48 adresów /de** (oraz /en, /uk, /ww), a znaczniki hreflang wskazują wszystkie 30 wersji.
- **Decyzja do podjęcia:**
  - Jeśli Niemcy/Austria/inne kraje są rynkiem docelowym → odblokować w robots.txt.
  - Jeśli nie → usunąć te adresy z sitemap i hreflang.
- **Dlaczego:** obecnie Google dostaje sprzeczne sygnały; zablokowane strony nie mogą się pozycjonować.

## 7. Strona główna — P2

- **Brak nagłówka H1.** Dodać np.: „Samarité – polskie kosmetyki naturalne: krem do twarzy i pod oczy, eliksir, balsam”.
- Mało treści (ok. 540 słów, głównie hasła). Dodać krótki tekst: co to za marka, dla kogo, bestsellery, dlaczego 8 kroków, darmowa dostawa, opinie.
- **25 z 52 zdjęć bez opisu (alt)**; na karcie Divine Cream **74 ze 131**. Uzupełnić opisy (nazwa produktu + co pokazuje zdjęcie).

## 8. Tytuły i opisy stron — P2

| Problem | Przykład | Poprawka |
|---|---|---|
| Podwójna marka w tytule | „… \| Samarité \| Samarite” | Jedna marka na końcu |
| Za długie tytuły | Divine Cream: 81 znaków; blog: 93 znaki | Max ok. 60 znaków |
| Ten sam szablon opisu | „Sprawdź ofertę naturalnych kosmetyków Samarité!” na każdej karcie | Unikalny opis: korzyść + ocena 4,9 (liczba opinii) + darmowa dostawa |
| Błąd w opisie artykułów | Opis zaczyna się od `**` (znaczniki formatowania) | Usunąć znaczniki |

Przykład opisu Divine Cream:
„Divine Cream – krem do twarzy i pod oczy, na dzień i na noc. 4,9/5 z ponad 2000 opinii. Formuła z 33 ziołami i niacynamidem. Darmowa dostawa.”

## 9. Dane o marce dla Google i AI — P2

- Na stronie głównej jest tylko LocalBusiness (butik Westfield Mokotów). Organization pojawia się na blogu z opisem po angielsku („Premium cosmetics and beauty products brand”).
- **Niespójność:** foundingDate 2019 w danych vs „od 8 lat” w tekście strony głównej.
- **Co zrobić:** na stronie głównej dodać Organization: name „Samarité”, alternateName „Samarite”, legalName „Zeme Pharm Anna Mrowińska”, polski opis, logo, foundingDate (spójny z tekstem), `sameAs` → Instagram, Facebook, TikTok, YouTube, profil marki na Wizaż.
- **Dlaczego:** nazwa jest mylona z „Samaritans”, „Samaria”, „Samaritaine” — wyszukiwarki i AI potrzebują jednoznacznych sygnałów, kim jest marka.

## 10. Mapa strony (sitemap.xml) — P3

- Wszystkie adresy mają datę zmiany `2025-01-01`. Generować prawdziwe daty modyfikacji.
- **Dlaczego:** Google używa lastmod tylko, gdy jest wiarygodny.

## 11. Eksperci i autorzy — P3

- Literówka w nagłówku: „eksperów Samaritè” → „ekspertów Samarité”.
- Autor artykułów w danych: „mgr chemii\nBARBARA ZAPISEK -\nGŁÓWNY TECHNOLOG” → name: „Barbara Zapisek”, jobTitle: „Główny technolog”, osobny profil autora.
- Linkować ekspertów z kart produktów (kto stworzył recepturę, kto ją ocenia).
- **Dlaczego:** Google w wytycznych o wartościowych treściach ocenia „kto, jak i po co” stworzył treść; AI chętniej cytuje źródła z widocznymi ekspertami.

## 12. Widoczność w AI (ChatGPT, Google AI, Perplexity) — P2/P3

**Działa dobrze:**

- Boty OAI-SearchBot, GPTBot, PerplexityBot i Googlebot dostają stronę bez blokady (sprawdzone).
- Jest plik llms.txt (Google go nie wykorzystuje, ale nie szkodzi).
- Blog ma autora, datę, dane Article, FAQ i linki do produktów.

**Do zrobienia:**

- **Obecność w rankingach i mediach**, z których AI buduje odpowiedzi: Elle („polskie marki naturalne”, „kremy 40+”), blog Superpharm, Wizaż TOP, natu.care. W sprawdzonych zestawieniach polecana jest konkurencja. → PR / wysyłka produktów do redakcji.
- **FAQ na kartach produktów** odpowiadające na realne obawy z opinii: „czy można stosować pod oczy” (są skargi na szczypanie), „czy dla cery wrażliwej”, „czy w ciąży”, „jak łączyć z Elixirem”.
- **Świeże opinie zewnętrzne:** nowa kampania testów (Wizaż KWC, Ceneo), żeby przykryć starą negatywną recenzję.

# Frazy kluczowe

**Wolumenów nie zweryfikowano** — sprawdzić w Planerze słów kluczowych Google Ads.

| Grupa | Frazy | Cel |
|---|---|---|
| Marka | samarite, samarite opinie, divine cream opinie, samarite skład, samarite gdzie kupić | Klientka ma trafić na samarite.eu, nie na Ceneo/Wizaż |
| Produkt | krem do twarzy i pod oczy, krem na dzień i na noc w jednym, naturalny krem odmładzający, krem z niacynamidem, krem 40+ / 50+ | Karty produktów + blog |
| Kategoria | polskie kosmetyki naturalne, słowiańskie kosmetyki, luksusowe polskie kosmetyki | Strona główna, „O marce” |
| Prezenty / sezon | zestaw kosmetyków na prezent dla kobiety, kosmetyki naturalne na prezent, prezent dla mamy | Strony zestawów (przed Dniem Matki, Świętami) |

**Reklama na nazwę marki:** w Google Ads → Statystyki aukcji. Jeśli konkurencja nie licytuje „samarite”, a strona jest na 1. miejscu w bezpłatnych wynikach — przetestować niższy budżet przez 2–4 tygodnie i porównać sprzedaż.

# Konkurencja

| Segment | Marki | Źródło |
|---|---|---|
| Słowiańskie / ziołowe | Mokosh, Slavia Cosmetics, Polny Warkocz, Kwiat Paproci | puderikrem.pl, strony marek |
| Naturalne anti-aging (PL) | Orientana, Resibo, Iossi, Veoli Botanica | Superpharm, Elle, natu.care |
| Polskie premium dermo | Dr Irena Eris, Dr Ambroziak | Elle, puderikrem.pl |

Uwaga: lista z rankingów i artykułów, nie z danych o udziale w rynku.

# Plan wdrożenia

| Termin | Działania | KPI |
|---|---|---|
| Tydzień 1 | Pkt 1 (filmy, szybkość), 2 (cena 30 dni), 3 (dane Divine Cream), 5 (claims – przegląd) | LCP mobile < 2,5 s; 0 błędów ceny w Merchant Center |
| Tydzień 2–4 | Pkt 4 (Merchant Center, gwiazdki), 7, 8, 9 | Gwiazdki w Google; CTR z Search Console |
| Miesiąc 2 | Pkt 6, 10, 11, 12 (PR, FAQ, opinie) | Obecność w 3+ rankingach; test AI co miesiąc |

**Mierzyć co miesiąc:** przychód i współczynnik konwersji sklepu (GA4), ruch bezpłatny z Google (Search Console), kliknięcia z Google Zakupów, wynik testu AI (te same pytania w ChatGPT/Perplexity/Google — czy poleca Samarité).

# Kolejne kroki

1. Udostępnić Search Console, Merchant Center, Google Ads (lub zrzuty) — weryfikacja danych realnych użytkowników, błędów feedu i aukcji na markę.
2. Test AI: zadać 10–15 pytań klientek w ChatGPT (czat tymczasowy), Perplexity i Google; zapisać, czy i jak pojawia się Samarité oraz jakie źródła są cytowane.
3. Konsultacja prawna: pkt 2 i 5.

# Źródła

- samarite.eu: /pl, /pl/product/divine-cream, /pl/product/divine-elixir, /pl/experts, /pl/blog/krem-na-zmarszczki, /robots.txt, /sitemap.xml, /llms.txt
- Wizaż – Divine Cream: https://wizaz.pl/kosmetyki/produkt,307802,samarite-divine-cream.html
- Glamour – krem co 7 minut: https://www.glamour.pl/uroda/przetestowalam-krem-ktory-sprzedaje-sie-w-polsce-co-7-minut/
- Recenzja negatywna: https://www.mojalepszawersja.pl/2020/04/samarite-divine-cream-nieudana.html
- INCI: https://incidecoder.com/products/samarite-divine-cream
- Superpharm: https://www.superpharm.pl/blog/naturalny-krem-do-twarzy-jaki-wybrac-polecane-produkty
- Elle – marki naturalne: https://www.elle.pl/uroda/najlepsze-kremy-nawilzajace-do-twarzy-od-polskich-marek-naturalnych-przeglad-i-opinie/
- Elle – kremy 40+: https://www.elle.pl/uroda/ranking-6-polecanych-polskich-kremow-do-pielegnacji-skory-40-kosztuja-od-14-do-249-zl/
- natu.care: https://natu.care/pl/kosmetyki/krem-do-twarzy
- puderikrem.pl – TOP 18 marek: https://puderikrem.pl/Polskie-kosmetyki-naturalne-i-dermokosmetyki-ranking-TOP-18-marek-ktore-musisz-znac-blog-pol-1733397695.html
- perfumeria.pl: https://www.perfumeria.pl/collections/samarite
