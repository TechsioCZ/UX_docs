# Table.PaginationBar

Pruh stránkování DataTable ukazuje rozsah a ovládání stránek skutečných výsledků.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Rozsah, počet stránek a aktuální stránka odpovídají výsledkům tabulky. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Rozsah, počet stránek a aktuální stránka odpovídají výsledkům tabulky.

## Kdy zvolit alternativu

Pro samostatný rozsáhlý úkol otevřete konkrétní detail. Pro čtení bez koordinovaných nástrojů postačí Table; další interakce nepřidávejte pouze kvůli dostupnému vizuálnímu slotu.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Změnit stránku nebo nabízený počet řádků na stránku při zachování aktuálních podmínek.

### Co vyvolávat nemá

- Nepočítat celkový počet z délky právě načtené serverové stránky a neměnit filtr skrytě.

### Přechody a odpovědnost

Aktivace dostupné stránky nebo změna velikosti stránky vyžádá odpovídající rozsah se stejnými podmínkami. Nový rozsah se potvrdí společně s daty. Při selhání zůstane předchozí výsledek rozpoznatelný a lze opakovat; ovladač nepředstírá úspěšný přechod. Změny rowCount přepočítají i existenci poslední stránky.

### Konkrétní pravidla použití

- Rozsah, počet stránek a aktuální stránka odpovídají výsledkům tabulky.
- Při změně filtru aktualizujte i dostupné stránky.
- Volba počtu řádků na stránku potřebuje přístupný název i bez viditelného labelu. Při serverovém stránkování vycházejte z celkového rowCount, nikoli jen z délky aktuální stránky.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Zachovejte čitelné přiřazení záhlaví a buněk, jednotky a identitu řádku. Odkazy a ovladače v tabulce jsou pojmenované a dostupné klávesnicí. Samotný název DataTable nedokládá vzor ARIA grid; nepřidávejte neověřené buněčné ovládání šipkami.

## Omezení a příklady podle typu projektu

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Volba a varianta:** Tento pruh koordinuje rozsah dat tabulky; Steps by neprávem naznačovalo pracovní etapy. V průchodu se uplatní `size=md`.

**Průchod a výsledek:** Pro rozsah „Záznamy 51–100 z 240“ zobrazte skutečný rowCount i pojmenovanou velikost stránky. Aktivace další existující stránky zachová filtry a řazení, po načtení se současně změní data i rozsah.

**Výjimka a návrat:** Při selhání ponechte předchozí výsledek rozpoznatelný a nabídněte opakování. Po zmenšení výsledku opravte neexistující aktuální stránku.

**Nevhodně:** Nepočítat celkový počet z délky právě načtené serverové stránky a neměnit filtr skrytě.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Volba a varianta:** Tento pruh koordinuje rozsah dat tabulky; Steps by neprávem naznačovalo pracovní etapy. V průchodu se uplatní `size=md`.

**Průchod a výsledek:** Pro rozsah „Objednávky 11–20 z 36“ zobrazte skutečný rowCount i pojmenovanou velikost stránky. Aktivace další existující stránky zachová filtry a řazení, po načtení se současně změní data i rozsah.

**Výjimka a návrat:** Při selhání ponechte předchozí výsledek rozpoznatelný a nabídněte opakování. Po zmenšení výsledku opravte neexistující aktuální stránku.

**Nevhodně:** Nepočítat celkový počet z délky právě načtené serverové stránky a neměnit filtr skrytě.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Volba a varianta:** Tento pruh koordinuje rozsah dat tabulky; Steps by neprávem naznačovalo pracovní etapy. V průchodu se uplatní `size=md`.

**Průchod a výsledek:** Pro rozsah „Požadavky 21–40 z 85“ zobrazte skutečný rowCount i pojmenovanou velikost stránky. Aktivace další existující stránky zachová filtry a řazení, po načtení se současně změní data i rozsah.

**Výjimka a návrat:** Při selhání ponechte předchozí výsledek rozpoznatelný a nabídněte opakování. Po zmenšení výsledku opravte neexistující aktuální stránku.

**Nevhodně:** Nepočítat celkový počet z délky právě načtené serverové stránky a neměnit filtr skrytě.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3397-666)
