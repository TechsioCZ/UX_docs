# Table.EmptyState

Prázdný stav tabulky vysvětluje absenci řádků; podle zdroje nahrazuje tělo a ponechává záhlaví.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Nahrazuje tělo tabulky; záhlaví zůstává viditelné. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Nahrazuje tělo tabulky; záhlaví zůstává viditelné.

## Kdy zvolit alternativu

Pro časově omezené oznámení celé operace zvažte Toast. Chyba jednoho pole má zůstat u tohoto pole; nepotvrzuje ani neblokuje jiný údaj.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na Table.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Nahrazuje tělo tabulky; záhlaví zůstává viditelné.
- Text odliší prázdná data, nulovou shodu filtru a selhání načtení.
- Nabídněte jen skutečně dostupný další krok.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Volba a varianta:** EmptyState vysvětlí známý prázdný výsledek; Skeleton pouze čekání a chyba služby potřebuje vlastní vysvětlení. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pro výsledek „Žádné objednávky neodpovídají filtru.“ ponechte záhlaví a kontext tabulky. Nabídněte Zrušit filtry pro obnovení širšího seznamu objednávek.

**Výjimka a návrat:** Při selhání načtení zobrazte skutečnou chybu a Opakovat načtení; nevydávejte ji za nulový počet záznamů. Zrušení filtru nic nemaže.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Volba a varianta:** EmptyState vysvětlí známý prázdný výsledek; Skeleton pouze čekání a chyba služby potřebuje vlastní vysvětlení. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pro výsledek „Zatím nemáte žádné objednávky.“ ponechte záhlaví a kontext tabulky. Nabídněte Přejít do katalogu pro zahájení nákupu, pokud je katalog skutečně dostupný.

**Výjimka a návrat:** Při selhání načtení zobrazte skutečnou chybu a Opakovat načtení; nevydávejte ji za nulový počet záznamů. Zrušení filtru nic nemaže.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Volba a varianta:** EmptyState vysvětlí známý prázdný výsledek; Skeleton pouze čekání a chyba služby potřebuje vlastní vysvětlení. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pro výsledek „Žádné požadavky v této kategorii.“ ponechte záhlaví a kontext tabulky. Nabídněte Zobrazit všechny kategorie pro rozšíření přehledu požadavků.

**Výjimka a návrat:** Při selhání načtení zobrazte skutečnou chybu a Opakovat načtení; nevydávejte ji za nulový počet záznamů. Zrušení filtru nic nemaže.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3390-47)
