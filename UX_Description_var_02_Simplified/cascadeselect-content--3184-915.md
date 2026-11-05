# CascadeSelect/Content

Panel CascadeSelect nese nabídku uzlů jedné otevřené úrovně hierarchie.

**Vazba:** CascadeSelect. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Jeden panel zobrazuje uzly příslušné otevřené úrovně. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě CascadeSelect. Jeden panel zobrazuje uzly příslušné otevřené úrovně.

## Kdy zvolit alternativu

Pro datovou hodnotu vyberte Select, Combobox či CascadeSelect podle rozsahu a hierarchie. Pro příkaz použijte Menu; vizuálně podobný obal nesmí měnit tento význam.

## Anatomie, stavy a varianty

Součást skladby **CascadeSelect**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=xs` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `depth=1` | Referenční hloubka panelu 1 musí odpovídat skutečné rodičovské větvi; číslo varianty neurčuje maximální hloubku dat. |
| `depth=2` | Referenční hloubka panelu 2 musí odpovídat skutečné rodičovské větvi; číslo varianty neurčuje maximální hloubku dat. |
| `depth=3` | Referenční hloubka panelu 3 musí odpovídat skutečné rodičovské větvi; číslo varianty neurčuje maximální hloubku dat. |
| `dir=ltr` | Pro levopravý jazyk a odpovídající logické směry. |
| `dir=rtl` | Pro pravolevý jazyk; obrátit logické uspořádání a odpovídající směrové značky, ne význam akcí. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Jeden panel zobrazuje uzly příslušné otevřené úrovně.
- Zachovejte vztah k rodičovské větvi i při současném zobrazení více úrovní.
- Pořadí sloupců a směr otevření odpovídají dir. Depth je ukázka rozbalené cesty, nikoli další údaj formulářové hodnoty.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Samotná oblast nepřebírá jména a akce svých ovladačů. Vnořené odkazy a tlačítka mají vlastní názvy a logické pořadí. Při menší šířce zůstává dosažitelný celý podstatný obsah, nikoli jen první viditelná část.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Jeden panel zobrazuje uzly příslušné otevřené úrovně. V průchodu se uplatní `depth=1`.

- **Společné výjimky a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

- **Nevhodné použití:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### ERP — účetní dimenze

**Situace a cíl:** Pracovník přiřazuje zakázku organizační jednotce ve stromu.

**Průchod a výsledek:** Sestavte oblast „Organizační jednotka“ s obsahem „Firma / Logistika / Sklad Brno“. Zachovejte vztah k rodičovské větvi i při současném zobrazení více úrovní. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Web — vyhledávání služby

**Situace a cíl:** Návštěvník vybírá provozovnu podle oblasti a města.

**Průchod a výsledek:** Sestavte oblast „Provozovna“ s obsahem „Jižní Morava / Znojmo / Centrum“. Zachovejte vztah k rodičovské větvi i při současném zobrazení více úrovní. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Interní systém — dokumentový portál

**Situace a cíl:** Uživatel zařazuje soubor do adresářové struktury.

**Průchod a výsledek:** Sestavte oblast „Cílová složka“ s obsahem „Projekty / Orion / Podklady“. Zachovejte vztah k rodičovské větvi i při současném zobrazení více úrovní. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy úrovní, zápis celé cesty a směrové uspořádání jazyka značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí datovou hierarchii, výběr listů či rodičů, vícenásobnost a validaci. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3184-915)
