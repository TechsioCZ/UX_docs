# Sidebar.PaneGroup

Skupina panelů Sidebar určuje jejich společnou skladbu a soužití v rámci rámu.

**Vazba:** Sidebar. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když několik souvisejících cílů či možností tvoří jednu pojmenovanou skupinu a čtenář je má porovnávat společně. Seskupuje panely jednoho rámu. Seskupuje panely jednoho rámu.

## Kdy zvolit alternativu

Pro samotné přechody mezi stránkami postačí VerticalNavigation. Pro dočasný kontextový úkol použijte Drawer; tato část zůstává součástí navigačního rámu.

## Anatomie, stavy a varianty

Součást skladby **Sidebar**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Seskupuje panely jednoho rámu.
- Jejich pořadí a souvislost zachovejte i při změně dostupné šířky.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

### ERP — víceagendová aplikace

**Situace a cíl:** Pracovník prochází nákup, sklad a související přehledy.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Seskupuje panely jednoho rámu. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Sestavte oblast „Objednávky“ s obsahem „Agenda Nákup / Objednávky“. Jejich pořadí a souvislost zachovejte i při změně dostupné šířky. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Web — zákaznický portál

**Situace a cíl:** Zákazník na telefonu otevírá přehled svého účtu.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Seskupuje panely jednoho rámu. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Sestavte oblast „Moje objednávky“ s obsahem „Navigace zákaznického účtu“. Jejich pořadí a souvislost zachovejte i při změně dostupné šířky. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Interní systém — projektový nástroj

**Situace a cíl:** Člen týmu přechází mezi pracovním seznamem a detaily projektu.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Seskupuje panely jednoho rámu. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Sestavte oblast „Projekt Orion“ s obsahem „Přehled / Úkoly / Dokumenty“. Jejich pořadí a souvislost zachovejte i při změně dostupné šířky. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit šířkovou a vizuální hierarchii rámu, názvy cílů a pravidla zobrazení identity značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí nabídku agend, oprávnění, zvolený režim a zachování kontextu při změně zařízení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3093-807)
