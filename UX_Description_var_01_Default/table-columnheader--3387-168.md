# Table.ColumnHeader

Záhlaví sloupce pojmenovává srovnávaný údaj a případně ukazuje směr řazení.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Text vysvětlí údaj ve sloupci. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Text vysvětlí údaj ve sloupci.

## Kdy zvolit alternativu

Pro samostatný rozsáhlý úkol otevřete konkrétní detail. Pro čtení bez koordinovaných nástrojů postačí Table; další interakce nepřidávejte pouze kvůli dostupnému vizuálnímu slotu.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `align=start` | Pro běžný text na logickém začátku řádku. |
| `align=center` | Pro krátké srovnatelné symboly či hodnoty, pokud zůstává čitelné přiřazení ke sloupci. |
| `align=end` | Pro srovnávání číselných hodnot a jednotek na logickém konci. |
| `sort=none` | Řazení ještě neurčuje asc ani desc; ovladač může být nadále řaditelný. |
| `sort=asc` | Aktuální vzestupné pořadí podle skutečné hodnoty sloupce; vysvětlit význam u nečíselných dat. |
| `sort=desc` | Aktuální sestupné pořadí stejného sloupce; směr musí souhlasit s načtenými záznamy. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Pojmenovat sloupec a při skutečně zapojeném řazení měnit jeho pořadí asc/desc.

### Co vyvolávat nemá

- Nezaměnit sort=none za zákaz řazení ani přetažení sloupce za změnu dat.

### Přechody a odpovědnost

None označuje řaditelný, dosud neseřazený sloupec. Až aktivace zapojeného ovladače vyžádá asc či desc a výsledné pořadí musí souhlasit s indikací. Pouhý hover či přesun fokusu neřadí. Při selhání načtení aplikace nesmí ukazovat nový směr jako úspěšně aplikovaný nad starým pořadím.

### Konkrétní pravidla použití

- Text vysvětlí údaj ve sloupci.
- None, asc a desc odpovídají skutečnému řazení.
- Nabídka řazení nesmí zaměnit označení směru za právě fokusovaný stav.
- None znamená dosud neseřazený, ale řaditelný sloupec. Při změně pořadí nebo šířky nabídněte dosažitelnou alternativu k tažení a samotnému hoveru.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Zachovejte čitelné přiřazení záhlaví a buněk, jednotky a identitu řádku. Odkazy a ovladače v tabulce jsou pojmenované a dostupné klávesnicí. Samotný název DataTable nedokládá vzor ARIA grid; nepřidávejte neověřené buněčné ovládání šipkami.

## Omezení a příklady podle typu projektu

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Volba a varianta:** Záhlaví řídí význam a případné řazení sloupce, nikoli výběr celého řádku. V průchodu se uplatní `sort=none`.

**Průchod a výsledek:** U sloupce „Datum dodání“ rozlišujte sort=none, asc a desc podle skutečného pořadí. Aktivace zapojeného ovladače vyžádá změnu směru a aplikace sjednotí indikaci s výsledky.

**Výjimka a návrat:** Hover neřadí. Při chybě požadavku nezobrazujte staré pořadí jako nově seřazené; změna šířky či polohy sloupce nesmí měnit data.

**Nevhodně:** Nezaměnit sort=none za zákaz řazení ani přetažení sloupce za změnu dat.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Volba a varianta:** Záhlaví řídí význam a případné řazení sloupce, nikoli výběr celého řádku. V průchodu se uplatní `sort=asc`.

**Průchod a výsledek:** U sloupce „Datum objednání“ rozlišujte sort=none, asc a desc podle skutečného pořadí. Aktivace zapojeného ovladače vyžádá změnu směru a aplikace sjednotí indikaci s výsledky.

**Výjimka a návrat:** Hover neřadí. Při chybě požadavku nezobrazujte staré pořadí jako nově seřazené; změna šířky či polohy sloupce nesmí měnit data.

**Nevhodně:** Nezaměnit sort=none za zákaz řazení ani přetažení sloupce za změnu dat.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Volba a varianta:** Záhlaví řídí význam a případné řazení sloupce, nikoli výběr celého řádku. V průchodu se uplatní `sort=desc`.

**Průchod a výsledek:** U sloupce „Priorita“ rozlišujte sort=none, asc a desc podle skutečného pořadí. Aktivace zapojeného ovladače vyžádá změnu směru a aplikace sjednotí indikaci s výsledky.

**Výjimka a návrat:** Hover neřadí. Při chybě požadavku nezobrazujte staré pořadí jako nově seřazené; změna šířky či polohy sloupce nesmí měnit data.

**Nevhodně:** Nezaměnit sort=none za zákaz řazení ani přetažení sloupce za změnu dat.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3387-168)
