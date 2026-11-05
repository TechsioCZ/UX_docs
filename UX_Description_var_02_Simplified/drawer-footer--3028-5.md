# Drawer.Footer

Patička Drawer seskupuje závěrečné akce konkrétního úkolu.

**Vazba:** Drawer. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Seskupuje závěrečné akce právě otevřeného úkolu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Drawer. Seskupuje závěrečné akce právě otevřeného úkolu.

## Kdy zvolit alternativu

Pro průběžné informace v úkolu použijte Body, pro identifikaci Header. Footer ponechte závěrečným akcím téhož panelu.

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

- Seskupuje závěrečné akce právě otevřeného úkolu.
- Potvrzení a zrušení mají odlišné názvy i důsledky; patička zůstává dosažitelná při dlouhém obsahu.
- Výchozí skladba obsahuje zavírací tlačítko Drawer.CloseTrigger; vlastní potvrzovací akce dodává obsah patičky.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

U interaktivní vrstvy určete počáteční fokus, dostupné zavření a logický návrat. Modální použití drží fokus uvnitř, nemodální ho nesmí bezdůvodně uvěznit. Na malé obrazovce a při dlouhém obsahu zůstanou dosažitelné důležité akce i konec úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Footer soustředí závěrečné akce téhož panelu; delší instrukce patří do Body. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při odmítnutí potvrzení ponechte data v Body a ukažte příčinu. Patička zůstane dosažitelná i při dlouhém obsahu či nižší snap poloze.

- **Nevhodné použití:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### ERP — související detail objednávky

**Situace a cíl:** Pracovník potřebuje upravit údaje vybraného řádku a vidět kontext přehledu.

**Průchod a výsledek:** Pro úkol „Upravit objednávku O-1048“ rozlište vlastní obsah potvrzovací akce „Uložit změny v panelu“ a samostatné zavření či Zrušit. Výchozí CloseTrigger se nesmí vydávat za uložení.

### Web — mobilní filtrování katalogu

**Situace a cíl:** Návštěvník nastavuje filtry v panelu od okraje obrazovky.

**Průchod a výsledek:** Pro úkol „Filtrovat produkty“ rozlište vlastní obsah potvrzovací akce „Použít filtry“ a samostatné zavření či Zrušit. Výchozí CloseTrigger se nesmí vydávat za uložení.

### Interní systém — pracovní detail incidentu

**Situace a cíl:** Řešitel otevře z přehledu vedlejší úkol k incidentu.

**Průchod a výsledek:** Pro úkol „Incident INC-142“ rozlište vlastní obsah potvrzovací akce „Aktualizovat incident“ a samostatné zavření či Zrušit. Výchozí CloseTrigger se nesmí vydávat za uložení.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit logickou stranu panelu, hierarchii jeho textů a prioritu závěrečných akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí modalitu konkrétního použití, ukládání, výchozí velikost a zachování rozpracovaného obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3028-5)
