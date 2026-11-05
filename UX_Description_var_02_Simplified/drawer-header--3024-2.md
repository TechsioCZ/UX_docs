# Drawer.Header

Záhlaví Drawer seskupuje jeho název a případné úvodní informace nebo zavření.

**Vazba:** Drawer. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Seskupuje titulek a případné úvodní vysvětlení či zavření panelu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Drawer. Seskupuje titulek a případné úvodní vysvětlení či zavření panelu.

## Kdy zvolit alternativu

Pro delší pracovní obsah použijte Body; Header nemá nahrazovat formulář nebo závěrečné akce Footer.

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

- Seskupuje titulek a případné úvodní vysvětlení či zavření panelu.
- Zavření musí zůstat rozpoznatelnou akcí, oddělenou od potvrzení úkolu.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

U interaktivní vrstvy určete počáteční fokus, dostupné zavření a logický návrat. Modální použití drží fokus uvnitř, nemodální ho nesmí bezdůvodně uvěznit. Na malé obrazovce a při dlouhém obsahu zůstanou dosažitelné důležité akce i konec úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Header identifikuje úkol; formulář patří do Body a závěrečné potvrzení do Footer. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Zavření není Uložit. Dlouhé jméno nesmí vytlačit zavírací ovladač mimo dosažitelnou plochu; draft řeší hostitelský panel.

- **Nevhodné použití:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### ERP — související detail objednávky

**Situace a cíl:** Pracovník potřebuje upravit údaje vybraného řádku a vidět kontext přehledu.

**Průchod a výsledek:** V záhlaví použijte Drawer.Title „Upravit objednávku O-1048“, případné stručné vysvětlení a pojmenované zavření. Tělo i závěrečné akce se vztahují k témuž objektu.

### Web — mobilní filtrování katalogu

**Situace a cíl:** Návštěvník nastavuje filtry v panelu od okraje obrazovky.

**Průchod a výsledek:** V záhlaví použijte Drawer.Title „Filtrovat produkty“, případné stručné vysvětlení a pojmenované zavření. Tělo i závěrečné akce se vztahují k témuž objektu.

### Interní systém — pracovní detail incidentu

**Situace a cíl:** Řešitel otevře z přehledu vedlejší úkol k incidentu.

**Průchod a výsledek:** V záhlaví použijte Drawer.Title „Incident INC-142“, případné stručné vysvětlení a pojmenované zavření. Tělo i závěrečné akce se vztahují k témuž objektu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit logickou stranu panelu, hierarchii jeho textů a prioritu závěrečných akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí modalitu konkrétního použití, ukládání, výchozí velikost a zachování rozpracovaného obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3024-2)
