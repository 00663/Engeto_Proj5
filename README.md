# Analýza mezigenerační distribuce bohatství v USA (Engeto Proj 5)

**Dobrý den,

rád bych k odevzdanému projektu připojil krátkou omluvu za zaslání na poslední chvíli (před termínem 19. 3.). Z důvodu mé vlastní chyby při plánování jsem žil v domnění, že termín pro odevzdání je až na konci měsíce, a skutečné datum jsem si uvědomil až nedávno. Do toho se mi bohužel sešel náročný nástup do nového zaměstnání a řešení osobních záležitostí, což mě časově velmi limitovalo. I přes tento časový pres jsem se ale snažil projekt neodbýt a vypracovat ho do maximální možné kvality (včetně detailní grafiky a kontextové analýzy).

Velice se omlouvám za případné komplikace s hodnocením na poslední chvíli a moc děkuji za vaše pochopení i za zpětnou vazbu, která mi při úpravách reportu hodně pomohla.**

# Cíl projektu

Tento projekt vizualizuje a analyzuje data o distribuci majetku ve Spojených státech napříč různými demografickými generacemi (Silent Generation, Baby Boomers, Gen X, Millennials). 

Cílem dashboardu je ukázat, jak se v čase mění koncentrace kapitálu, jaký vliv měly historické ekonomické milníky (finanční krize 2008, inflace a zvyšování sazeb v roce 2022) na majetek jednotlivých skupin a upozornit na bariéry akumulace kapitálu u mladších generací.

**Zdroj dat:** Původní data vycházejí z Distributional Financial Accounts (FED).

---

##  Náhled reportu

<img width="2052" height="1154" alt="image" src="https://github.com/user-attachments/assets/099a2ced-3cad-4a6e-a7b0-5a217f42398b" />

---

##  Splnění požadavků projektu

Tento projekt byl vytvořen jako závěrečná práce pro kurz datové analytiky a plně reflektuje zadané technické požadavky:

- [x] **Rozsah 2-5 stránek:** - Report je logicky rozdělen do **3 interaktivních stránek**, které umožňují postupný "drill-down" od celkového přehledu k detailním kvartálním maticím.
- [x] **Použití minimálně 5 různých typů vizuálů:** - V projektu jsou využity: Spojnicový graf (Line chart), Sloupcový graf (Bar chart), Prstencový graf (Donut chart), Interaktivní matice (Matrix) a Karty (Cards) pro klíčové metriky.
- [x] **Filtrování (primárně) pomocí průřezů/slicerů:** - Uživatel může data filtrovat pomocí dynamických průřezů podle časových období (Dekáda, Rok, Kvartál).
- [x] **Využití interaktivních prvků:** - V reportu je implementována **navigace po stranách** pomocí tlačítek a je zde funkční **odkaz na webové stránky** (zdroj dat FED).
- [x] **Propojení několika (2+) datových tabulek:** - Datový model v Power BI využívá relaci (1:N) mezi hlavní tabulkou faktů (`dfa-generation-levels-detail`) a dimenzní tabulkou obsahující popisky generací (`Dim_generations`).
- [x] **Použití vytvořené hierarchie:** - Je vytvořena a aplikována vlastní časová hierarchie **Dekáda -> Rok -> Kvartál**, která umožňuje uživatelům procházet data v matici do hloubky.
- [x] **Vytvoření alespoň 1 measure a 1 kalkulovaného sloupce:**
  - **Measure (Míra):** Vytvořena míra `Total_Wealth` pro dynamický výpočet a agregaci celkového majetku napříč filtry.
  - **Kalkulovaný sloupec:** Pomocí DAXu byl vytvořen sloupec `Real_Date` pro správnou klasifikaci a formátování časové osy.
- [x] **Grafická úprava a vizuálně přívětivý report:** - Vizuály byly očištěny od defaultních pozadí (průhlednost) pro čistší integraci do dashboardu, a jednodušší další potenicální úpravy.
  - Je dodržen striktní **color-coding** napříč všemi stranami (každá generace má napříč grafy přiřazenou stejnou barvu).
  - Přidány strukturované textové boxy (insighty) vysvětlující kauzalitu anomálií v datech (např. propad v roce 2022 v důsledku zásahů FEDu).
