# Table.Toolbar

Nástrojový pruh DataTable sdružuje hledání a akce nad správnou množinou záznamů.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Hledání a akce pracují nad jasně určenými záznamy. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Hledání a akce pracují nad jasně určenými záznamy.

## Kdy zvolit alternativu

Pro samotné čtení údajů postačí Table bez této nástrojové vrstvy. Akce jednoho řádku nezaměňujte za nástroje celého přehledu.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Hledání a akce pracují nad jasně určenými záznamy.
- Hromadné akce odpovídají skutečnému výběru.
- Přeplněný pruh rozdělte podle priority nebo využijte nabídku dalších akcí.
- Upřednostněte nejvýše tři vlastní hlavní akce; další přesuňte do nabídky. Jde o doporučení pro přehlednost, nikoli technický zákaz vykreslení.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Zachovejte čitelné přiřazení záhlaví a buněk, jednotky a identitu řádku. Odkazy a ovladače v tabulce jsou pojmenované a dostupné klávesnicí. Samotný název DataTable nedokládá vzor ARIA grid; nepřidávejte neověřené buněčné ovládání šipkami.

## Omezení a příklady podle typu projektu

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Volba a varianta:** Toolbar slouží celému přehledu nebo pojmenovanému výběru; místní operace jednoho řádku se nemá tvářit jako hromadná. V průchodu se uplatní `size=md`.

**Průchod a výsledek:** V přehledu použijte „Vybrány 2 objednávky; Exportovat výběr“. Exportovat výběr se vztahuje právě ke dvěma skutečně označeným objednávkám; rozsah je viditelný před aktivací.

**Výjimka a návrat:** Po změně filtru nebo stránky musí být zřejmé, zda výběr zahrnuje i neviditelné řádky. Selhání hromadné akce nesmí předstírat úspěch všech záznamů.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Volba a varianta:** Toolbar slouží celému přehledu nebo pojmenovanému výběru; místní operace jednoho řádku se nemá tvářit jako hromadná. V průchodu se uplatní `size=md`.

**Průchod a výsledek:** V přehledu použijte „Hledat v mých objednávkách“. Odeslaný dotaz hledá pouze v objednávkách tohoto zákazníka; nezmění jejich obsah.

**Výjimka a návrat:** Po změně filtru nebo stránky musí být zřejmé, zda výběr zahrnuje i neviditelné řádky. Selhání hromadné akce nesmí předstírat úspěch všech záznamů.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Volba a varianta:** Toolbar slouží celému přehledu nebo pojmenovanému výběru; místní operace jednoho řádku se nemá tvářit jako hromadná. V průchodu se uplatní `size=md`.

**Průchod a výsledek:** V přehledu použijte „Vybrány 3 incidenty; Přiřadit řešitele“. Přiřadit řešitele otevře volbu pro tři označené incidenty; samotný výběr řádků přiřazení neprovede.

**Výjimka a návrat:** Po změně filtru nebo stránky musí být zřejmé, zda výběr zahrnuje i neviditelné řádky. Selhání hromadné akce nesmí předstírat úspěch všech záznamů.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3396-2080)
