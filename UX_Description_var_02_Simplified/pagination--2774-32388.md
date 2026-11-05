# Pagination

Stránkování umožňuje procházet rozdělený seznam výsledků.

Cílem je procházet stránky jednoho stabilně vymezeného souboru výsledků.

## Kdy použít

Pro stránky stejného souboru výsledků se zachováním dotazu, filtrů a řazení. Produkt musí určit skutečný rozsah a celkový počet. Pracovní proces nerozdělujte stránkováním místo Steps.

## Kdy zvolit alternativu

Pro sekvenci snímků použijte Carousel, pro etapy úkolu Steps.

## Anatomie, stavy a varianty

Ovladače dostupných stránek a aktuální pozice v jednom souboru výsledků. Rozsah dat, velikost stránky a vyhodnocení filtrů řídí aplikace.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `variant=filled` | Vizuální provedení filled podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `variant=outlined` | Vizuální provedení outlined podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `variant=minimal` | Vizuální provedení minimal podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Přejít na dostupnou předchozí, další nebo konkrétní stránku.
- Aktualizovat aktuální stránku podle skutečně načtených výsledků.

### Co vyvolávat nemá

- Nedělit bezdůvodně jeden formulář nebo lineární pracovní proces.
- Nezaměňovat pořadové číslo stránky za počet vybraných záznamů.

### Přechody a odpovědnost

Pro objekt „Záznamy 51–100 z 240“ použijte pojmenování „Stránka objednávek“. Přechod na dostupnou stránku zachová dotaz, filtry a řazení. Aktuální pozice se sjednotí se skutečným výsledkem načtení a po změně rozsahu se opraví neexistující stránka. Vzhled filled/outlined/minimal tuto datovou logiku nemění. Odpovědnost za skutečný výsledek a případné odmítnutí má aplikace hostící tuto komponentu.

### Konkrétní pravidla použití

- Aktuální stránka musí odpovídat zobrazeným datům.
- První a poslední stránka mají správně omezené krajní ovladače.
- Při změně filtru upravte rozsah a dostupné stránky podle nových výsledků.
- Výpustka není skutečná stránka. Načítání a počet výsledků řídí aplikace.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nedělit bezdůvodně jeden formulář nebo lineární pracovní proces.

### ERP — přehled objednávek

**Situace a cíl:** Pracovník prochází filtrovaný seznam objednávek.

**Volba a varianta:** Stránky mění část týchž výsledků „Stránka objednávek“; Steps by nesprávně naznačovalo etapy vyplňování. V průchodu se uplatní `variant=filled`.

**Průchod a výsledek:** Pro objekt „Záznamy 51–100 z 240“ použijte pojmenování „Stránka objednávek“. Přechod na dostupnou stránku zachová dotaz, filtry a řazení. Aktuální pozice se sjednotí se skutečným výsledkem načtení a po změně rozsahu se opraví neexistující stránka. Vzhled filled/outlined/minimal tuto datovou logiku nemění.

**Výjimka a návrat:** Po změně filtru se aktuální stránka upraví na existující rozsah, místo prázdné neexistující stránky.

### Web — katalog článků

**Situace a cíl:** Návštěvník pokračuje v přehledu starších článků.

**Volba a varianta:** Stránky mění část týchž výsledků „Další stránka článků“; Steps by nesprávně naznačovalo etapy vyplňování. V průchodu se uplatní `variant=filled`.

**Průchod a výsledek:** Pro objekt „Stránka 2 z 8“ použijte pojmenování „Další stránka článků“. Přechod na dostupnou stránku zachová dotaz, filtry a řazení. Aktuální pozice se sjednotí se skutečným výsledkem načtení a po změně rozsahu se opraví neexistující stránka. Vzhled filled/outlined/minimal tuto datovou logiku nemění.

**Výjimka a návrat:** Na poslední stránce nemá Další slibovat existující obsah, který už nenásleduje.

### Interní systém — správa uživatelů

**Situace a cíl:** Správce čte seznam uživatelů po částech.

**Volba a varianta:** Stránky mění část týchž výsledků „Stránkování uživatelů“; Steps by nesprávně naznačovalo etapy vyplňování. V průchodu se uplatní `variant=filled`.

**Průchod a výsledek:** Pro objekt „Uživatelé 21–40“ použijte pojmenování „Stránkování uživatelů“. Přechod na dostupnou stránku zachová dotaz, filtry a řazení. Aktuální pozice se sjednotí se skutečným výsledkem načtení a po změně rozsahu se opraví neexistující stránka. Vzhled filled/outlined/minimal tuto datovou logiku nemění.

**Výjimka a návrat:** Případný výběr napříč stránkami má jasně vymezený rozsah mimo samotnou Pagination.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit vzhled stránkování a pojmenování navigačních ovladačů a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí velikost stránky, celkový počet výsledků a vazbu na filtry a řazení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-32388)
