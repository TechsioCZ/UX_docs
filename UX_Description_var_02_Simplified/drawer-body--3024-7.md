# Drawer.Body

Tělo Drawer nese pracovní obsah panelu a zachovává dosažitelnost delšího úkolu.

**Vazba:** Drawer. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Obsahuje vlastní pracovní úkol. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Drawer. Obsahuje vlastní pracovní úkol.

## Kdy zvolit alternativu

Titulek patří do Title/Header a závěrečné akce do Footer. Rozsáhlý úkol, který nelze udržet čitelný v panelu, otevřete na samostatné stránce.

## Anatomie, stavy a varianty

Součást skladby **Drawer**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Obsahuje vlastní pracovní úkol.
- Dlouhý obsah nesmí znemožnit přístup k závěrečným akcím, včetně snížené snap polohy.
- Jde o posouvanou obsahovou oblast; při vložení mobilního Sidebar počítejte s jeho vlastní skladbou bez dodatečného vnitřního odsazení.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

U interaktivní vrstvy určete počáteční fokus, dostupné zavření a logický návrat. Modální použití drží fokus uvnitř, nemodální ho nesmí bezdůvodně uvěznit. Na malé obrazovce a při dlouhém obsahu zůstanou dosažitelné důležité akce i konec úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Obsahuje vlastní pracovní úkol. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

- **Nevhodné použití:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### ERP — související detail objednávky

**Situace a cíl:** Pracovník potřebuje upravit údaje vybraného řádku a vidět kontext přehledu.

**Průchod a výsledek:** Sestavte oblast „Upravit objednávku O-1048“ s obsahem „Objednávka O-1048“. Dlouhý obsah nesmí znemožnit přístup k závěrečným akcím, včetně snížené snap polohy. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Web — mobilní filtrování katalogu

**Situace a cíl:** Návštěvník nastavuje filtry v panelu od okraje obrazovky.

**Průchod a výsledek:** Sestavte oblast „Filtrovat produkty“ s obsahem „Dostupnost a cenové rozpětí“. Dlouhý obsah nesmí znemožnit přístup k závěrečným akcím, včetně snížené snap polohy. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Interní systém — pracovní detail incidentu

**Situace a cíl:** Řešitel otevře z přehledu vedlejší úkol k incidentu.

**Průchod a výsledek:** Sestavte oblast „Incident INC-142“ s obsahem „Podrobnosti incidentu“. Dlouhý obsah nesmí znemožnit přístup k závěrečným akcím, včetně snížené snap polohy. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit logickou stranu panelu, hierarchii jeho textů a prioritu závěrečných akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí modalitu konkrétního použití, ukládání, výchozí velikost a zachování rozpracovaného obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3024-7)
