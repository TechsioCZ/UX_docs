# Table.Row

Řádek tabulky spojuje hodnoty jednoho záznamu a odlišuje výběr od hover i střídavého pozadí.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Spojuje hodnoty jednoho záznamu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Spojuje hodnoty jednoho záznamu.

## Kdy zvolit alternativu

Pro samostatný rozsáhlý úkol otevřete konkrétní detail. Pro čtení bez koordinovaných nástrojů postačí Table; další interakce nepřidávejte pouze kvůli dostupnému vizuálnímu slotu.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=base` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=selected` | Pro skutečně potvrzenou vybranou položku. Hover ani pouhý fokus ji nenahrazují. |
| `striped=false` | Bez střídání podkladu; význam selected zůstává samostatný. |
| `striped=true` | Pro střídání vizuálního podkladu řádků, které není výběrem ani stavem chyby. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Spojuje hodnoty jednoho záznamu.
- Selected, hover a striped mají odlišný význam.
- Při akcích zachovejte jednoznačnou identitu řádku.
- Při povoleném přesouvání řádků nabídněte alternativu k tažení. Nested je zvýraznění hloubky, které může soužít se striped; není další výběrový stav.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Zachovejte čitelné přiřazení záhlaví a buněk, jednotky a identitu řádku. Odkazy a ovladače v tabulce jsou pojmenované a dostupné klávesnicí. Samotný název DataTable nedokládá vzor ARIA grid; nepřidávejte neověřené buněčné ovládání šipkami.

## Omezení a příklady podle typu projektu

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Spojuje hodnoty jednoho záznamu. V průchodu se uplatní `state=base`, `striped=false`.

**Průchod a výsledek:** Sestavte oblast „Přehled objednávek“ s obsahem „O-1048; 12 500 Kč; Čeká“. Selected, hover a striped mají odlišný význam. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Spojuje hodnoty jednoho záznamu. V průchodu se uplatní `state=selected`, `striped=false`.

**Průchod a výsledek:** Sestavte oblast „Moje objednávky“ s obsahem „W-248; 1 490 Kč; Doručeno“. Selected, hover a striped mají odlišný význam. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Spojuje hodnoty jednoho záznamu. V průchodu se uplatní `state=base`, `striped=false`.

**Průchod a výsledek:** Sestavte oblast „Požadavky podpory“ s obsahem „INC-142; Běžná priorita; Jana Nováková“. Selected, hover a striped mají odlišný význam. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3386-62)
