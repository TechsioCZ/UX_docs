# Select/Content

Obsah nabídky Select sdružuje volitelné položky vztahující se k jednomu výběrovému poli.

**Vazba:** Select. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Nabídka patří jednomu Select a obsahuje jeho možnosti nebo jejich skupiny. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Select. Nabídka patří jednomu Select a obsahuje jeho možnosti nebo jejich skupiny.

## Kdy zvolit alternativu

Pro příkazy použijte Menu, pro vyhledávání mezi hodnotami Combobox/Content. Tento obsah náleží plochému výběru Select.

## Anatomie, stavy a varianty

Součást skladby **Select**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Nabídka patří jednomu Select a obsahuje jeho možnosti nebo jejich skupiny.
- Zachovejte rozlišení zvolené, zvýrazněné a nedostupné možnosti.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Samotná oblast nepřebírá jména a akce svých ovladačů. Vnořené odkazy a tlačítka mají vlastní názvy a logické pořadí. Při menší šířce zůstává dosažitelný celý podstatný obsah, nikoli jen první viditelná část.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Nabídka patří jednomu Select a obsahuje jeho možnosti nebo jejich skupiny. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

- **Nevhodné použití:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### ERP — zakázkový formulář

**Situace a cíl:** Pracovník přiřazuje zakázku existujícímu středisku.

**Průchod a výsledek:** Sestavte oblast „Středisko“ s obsahem „Logistika“. Zachovejte rozlišení zvolené, zvýrazněné a nedostupné možnosti. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Web — nastavení doručení

**Situace a cíl:** Zákazník vybírá z nabízených zemí pro danou službu.

**Průchod a výsledek:** Sestavte oblast „Země doručení“ s obsahem „Česko“. Zachovejte rozlišení zvolené, zvýrazněné a nedostupné možnosti. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Interní systém — ITSM

**Situace a cíl:** Žadatel volí prioritu z předem vysvětleného seznamu.

**Průchod a výsledek:** Sestavte oblast „Priorita požadavku“ s obsahem „Běžná“. Zachovejte rozlišení zvolené, zvýrazněné a nedostupné možnosti. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26047)
