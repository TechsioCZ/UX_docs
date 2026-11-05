# Table.ExpandToggle

Ovladač detailu řádku rozbaluje jeho doplňující panel nezávisle na výběru řádku.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Ovládá detail právě jednoho řádku. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Ovládá detail právě jednoho řádku.

## Kdy zvolit alternativu

Pro samostatný rozsáhlý úkol otevřete konkrétní detail. Pro čtení bez koordinovaných nástrojů postačí Table; další interakce nepřidávejte pouze kvůli dostupnému vizuálnímu slotu.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=collapsed` | Když přiřazený rozbalovací obsah není otevřený. Text spouštěče dál identifikuje stejný obsah. |
| `state=expanded` | Když je přiřazený obsah skutečně otevřený. Spouštěč, indikátor a obsah se nesmějí rozcházet. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Rozbalit nebo sbalit detail stejného řádku a sdělit jeho expanded stav.

### Co vyvolávat nemá

- Neodstranit řádek a nepoužít křížek jako označení rozbalení.

### Přechody a odpovědnost

Detail je pod správným rodičovským záznamem. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Ovládá detail právě jednoho řádku.
- Rozbalení se nesmí zaměnit za výběr řádku nebo jinou řádkovou akci.
- Použijte rozbalovací chevron, nikoli zavírací křížek. Oznámené expanded musí odpovídat viditelnosti detailu.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Zachovejte čitelné přiřazení záhlaví a buněk, jednotky a identitu řádku. Odkazy a ovladače v tabulce jsou pojmenované a dostupné klávesnicí. Samotný název DataTable nedokládá vzor ARIA grid; nepřidávejte neověřené buněčné ovládání šipkami.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Zrušení ani neúspěch nesmí předstírat potvrzený výsledek. Neodstranit řádek a nepoužít křížek jako označení rozbalení. Před skrytím obsahu vyřešte fokus uvnitř tak, aby zůstal na dosažitelném místě.

- **Pravidlo použití:** Neodstranit řádek a nepoužít křížek jako označení rozbalení.

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Volba a varianta:** Tento díl provádí právě místní krok hostitele; jeho obal ani dekorativní glyph jej nenahrazují. V průchodu se uplatní `state=collapsed`.

**Průchod a výsledek:** U „Objednávka O-1048“: Rozbalit nebo sbalit detail stejného řádku a sdělit jeho expanded stav. Detail je pod správným rodičovským záznamem. Aktivace musí změnit jen přiřazenou sekci, panel nebo rám; fokus není potvrzením jiných údajů.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Volba a varianta:** Tento díl provádí právě místní krok hostitele; jeho obal ani dekorativní glyph jej nenahrazují. V průchodu se uplatní `state=expanded`.

**Průchod a výsledek:** U „Objednávka W-248“: Rozbalit nebo sbalit detail stejného řádku a sdělit jeho expanded stav. Detail je pod správným rodičovským záznamem. Aktivace musí změnit jen přiřazenou sekci, panel nebo rám; fokus není potvrzením jiných údajů.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Volba a varianta:** Tento díl provádí právě místní krok hostitele; jeho obal ani dekorativní glyph jej nenahrazují. V průchodu se uplatní `state=collapsed`.

**Průchod a výsledek:** U „Incident INC-142“: Rozbalit nebo sbalit detail stejného řádku a sdělit jeho expanded stav. Detail je pod správným rodičovským záznamem. Aktivace musí změnit jen přiřazenou sekci, panel nebo rám; fokus není potvrzením jiných údajů.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3395-95)
