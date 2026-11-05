# Table.IconButton

Ikonové tlačítko Table.IconButton poskytuje pojmenované ovládání viditelnosti sloupců nebo nabídky operátorů filtru.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Vnořenou ikonu lze vyměnit: ozubené kolo pro sloupce, filtr pro nabídku podmínek. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Vnořenou ikonu lze vyměnit: ozubené kolo pro sloupce, filtr pro nabídku podmínek.

## Kdy zvolit alternativu

Pro samostatný rozsáhlý úkol otevřete konkrétní detail. Pro čtení bez koordinovaných nástrojů postačí Table; další interakce nepřidávejte pouze kvůli dostupnému vizuálnímu slotu.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít pojmenovanou nabídku viditelnosti sloupců nebo operátorů filtru podle vloženého glyphu.

### Co vyvolávat nemá

- Nevydávat ovladač za ActionIcon s pevnou ikonou křížku ani za univerzální editaci řádku.

### Přechody a odpovědnost

Uživatel ovládá právě deklarovanou oblast tabulky. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Vnořenou ikonu lze vyměnit: ozubené kolo pro sloupce, filtr pro nabídku podmínek.
- Každý ovladač má přístupný název odpovídající výsledku; samotný glyph nestačí.
- Nezaměňujte jej automaticky za ActionIcon s pevnou ikonou křížku.
- Referenční tabulka používá glyphy md (20 px); current je ve Figmě staticky 16 px a nesrovnává se automaticky s velikostí v kódu.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Zachovejte čitelné přiřazení záhlaví a buněk, jednotky a identitu řádku. Odkazy a ovladače v tabulce jsou pojmenované a dostupné klávesnicí. Samotný název DataTable nedokládá vzor ARIA grid; nepřidávejte neověřené buněčné ovládání šipkami.

## Omezení a příklady podle typu projektu

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Volba a varianta:** Má zaměnitelný slot; pevný křížek ActionIcon by zde sliboval zavření místo nastavení. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** Ovladač pojmenujte „Viditelnost sloupců“. S ozubeným kolem otevře volbu viditelnosti sloupců, s filtrem nabídku podmínek; konkrétní změna nastane až volbou v této nabídce.

**Výjimka a návrat:** Zavření nabídky bez volby nezmění nastavení. Název musí odpovídat vloženému glyphu a po zavření se fokus logicky vrátí na ovladač.

**Nevhodně:** Nevydávat ovladač za ActionIcon s pevnou ikonou křížku ani za univerzální editaci řádku.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Volba a varianta:** Má zaměnitelný slot; pevný křížek ActionIcon by zde sliboval zavření místo nastavení. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** Ovladač pojmenujte „Podmínky filtru“. S ozubeným kolem otevře volbu viditelnosti sloupců, s filtrem nabídku podmínek; konkrétní změna nastane až volbou v této nabídce.

**Výjimka a návrat:** Zavření nabídky bez volby nezmění nastavení. Název musí odpovídat vloženému glyphu a po zavření se fokus logicky vrátí na ovladač.

**Nevhodně:** Nevydávat ovladač za ActionIcon s pevnou ikonou křížku ani za univerzální editaci řádku.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Volba a varianta:** Má zaměnitelný slot; pevný křížek ActionIcon by zde sliboval zavření místo nastavení. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** Ovladač pojmenujte „Viditelnost sloupců“. S ozubeným kolem otevře volbu viditelnosti sloupců, s filtrem nabídku podmínek; konkrétní změna nastane až volbou v této nabídce.

**Výjimka a návrat:** Zavření nabídky bez volby nezmění nastavení. Název musí odpovídat vloženému glyphu a po zavření se fokus logicky vrátí na ovladač.

**Nevhodně:** Nevydávat ovladač za ActionIcon s pevnou ikonou křížku ani za univerzální editaci řádku.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3424-613)
