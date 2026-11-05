# DataTable

DataTable uspořádává záznamy a propojuje je s nástroji pro hledání, filtrování a další práci s daty.

Cílem je porovnat stejné atributy záznamů a podle skutečné skladby nad nimi provést odlišené datové operace.

## Kdy použít

Pro srovnávání stejných atributů více záznamů v řádcích a sloupcích. Table je základ čtení; DataTable koordinuje skutečně vložené nástroje, výběr a datové operace. Karta je vhodnější, když údaje nelze rozumně srovnat po sloupcích.

## Kdy zvolit alternativu

Pro čtení a porovnání údajů bez této koordinace nástrojů použijte Table.

## Anatomie, stavy a varianty

Základní tabulka propojuje Row, ColumnHeader a Cell. DataTable přidává koordinaci Toolbar, FilterRow, PaginationBar a dalších skutečně zapojených nástrojů; ExpandToggle a DetailPanel patří témuž rodičovskému řádku.
Kořen nemá vystavenou vlastní variantní osu. Konkrétní stavy buněk, řazení a nástrojů patří příslušným částem Table; jejich podporu nepřisuzujte automaticky kořeni.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Číst odpovídající hodnoty v řádcích a sloupcích.
- V DataTable samostatně hledat, filtrovat, řadit, vybírat a aktivovat konkrétní řádkové akce.

### Co vyvolávat nemá

- Nepovažovat každý klik v řádku za výběr i otevření detailu zároveň.
- Nezaměňovat prázdnou databázi, nulovou shodu a chybu načtení.

### Přechody a odpovědnost

Základní Table zobrazuje dodaná data a nevytváří automaticky editaci či filtry. V DataTable řídí aplikace společný dotaz, filtry, řazení a stránkování. Po výsledku se sjednotí řádky, rozsah i indikace; při chybě zůstane předchozí stav rozpoznatelný a je dostupná náprava. Výběr či editace patří konkrétním řádkům a Table.Cell, nikoli domnělé variantě kořene error.

### Konkrétní pravidla použití

- Hledání, filtry, výběr a řádkové akce mají odlišné účely a musí pracovat nad správnými záznamy.
- Editovaná hodnota, potvrzená hodnota a chyba musí patřit správnému řádku a sloupci.
- Změna filtru se promítne do výsledků i stránkování.
- Nulovou shodu odlište od prázdné databáze a chyby načtení.
- Název data grid sám neurčuje buněčné klávesnicové ovládání.
- Podpora velikostí je v současné dokumentaci rozporná; složené části výslovně uvádějí md.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Zachovejte čitelné přiřazení záhlaví a buněk, jednotky a identitu řádku. Odkazy a ovladače v tabulce jsou pojmenované a dostupné klávesnicí. Samotný název DataTable nedokládá vzor ARIA grid; nepřidávejte neověřené buněčné ovládání šipkami.

## Omezení a příklady podle typu projektu

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Volba a varianta:** Záznam „Objednávka O-1048“ se porovnává podle stejných atributů jako sousední řádky; volná karta by ztížila srovnání po sloupcích. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pro objekt „Objednávka O-1048“ použijte pojmenování „Přehled objednávek“. Rozsah hledání a filtrů určete nad jedním souborem dat. Změna filtru aktualizuje také stránkování a řazení; vybrané řádky mají vlastní rozsah. Editace používá stavy příslušné Table.Cell, ne domnělou jednotnou error variantu celého kořene.

**Výjimka a návrat:** Neúspěšná editace buňky zachová draft a neoznačí sousední buňku jako chybnou.

**Nevhodně:** Nepovažovat každý klik v řádku za výběr i otevření detailu zároveň.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Volba a varianta:** Záznam „Objednávka W-248“ se porovnává podle stejných atributů jako sousední řádky; volná karta by ztížila srovnání po sloupcích. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pro objekt „Objednávka W-248“ použijte pojmenování „Moje objednávky“. Rozsah hledání a filtrů určete nad jedním souborem dat. Změna filtru aktualizuje také stránkování a řazení; vybrané řádky mají vlastní rozsah. Editace používá stavy příslušné Table.Cell, ne domnělou jednotnou error variantu celého kořene.

**Výjimka a návrat:** Pro nulový výsledek filtru nabídne aplikace změnu filtru, ne falešné tvrzení o neexistenci objednávek.

**Nevhodně:** Nepovažovat každý klik v řádku za výběr i otevření detailu zároveň.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Volba a varianta:** Záznam „Incident INC-142“ se porovnává podle stejných atributů jako sousední řádky; volná karta by ztížila srovnání po sloupcích. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pro objekt „Incident INC-142“ použijte pojmenování „Požadavky podpory“. Rozsah hledání a filtrů určete nad jedním souborem dat. Změna filtru aktualizuje také stránkování a řazení; vybrané řádky mají vlastní rozsah. Editace používá stavy příslušné Table.Cell, ne domnělou jednotnou error variantu celého kořene.

**Výjimka a návrat:** Serverové stránkování potřebuje skutečný celkový rowCount; název data grid nezavádí automaticky buněčné klávesnicové ovládání.

**Nevhodně:** Nepovažovat každý klik v řádku za výběr i otevření detailu zároveň.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3399-330)
