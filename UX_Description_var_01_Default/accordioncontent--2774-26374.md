# AccordionContent

Obsah položky Accordion nese informace příslušné sekce, dostupné po jejím rozbalení.

**Vazba:** Accordion. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Zobrazujte obsah přiřazený správnému záhlaví. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Accordion. Zobrazujte obsah přiřazený správnému záhlaví.

## Kdy zvolit alternativu

Pokud musí být obsah čtený bez rozbalení, zobrazte jej trvale. Pro přepínání rovnocenných panelů zvažte Tabs, pro navigaci skutečný Link.

## Anatomie, stavy a varianty

Součást skladby **Accordion**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=collapsed` | Když přiřazený rozbalovací obsah není otevřený. Text spouštěče dál identifikuje stejný obsah. |
| `state=expanded` | Když je přiřazený obsah skutečně otevřený. Spouštěč, indikátor a obsah se nesmějí rozcházet. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Zobrazujte obsah přiřazený správnému záhlaví.
- Nepřenášejte sem informace jiné položky nebo jedinou instrukci nutnou před rozbalením.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

### ERP — detail zakázky

**Situace a cíl:** Pracovník potřebuje rozbalit výpočet nákladů vedle souhrnu.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Zobrazujte obsah přiřazený správnému záhlaví. V průchodu se uplatní `state=collapsed`.

**Průchod a výsledek:** Sestavte oblast „Rozpis nákladů“ s obsahem „Práce a použitý materiál“. Nepřenášejte sem informace jiné položky nebo jedinou instrukci nutnou před rozbalením. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Web — informace o produktu

**Situace a cíl:** Návštěvník si chce přečíst doplňující podmínky služby.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Zobrazujte obsah přiřazený správnému záhlaví. V průchodu se uplatní `state=expanded`.

**Průchod a výsledek:** Sestavte oblast „Podmínky vrácení“ s obsahem „Vrácení zboží z internetového obchodu“. Nepřenášejte sem informace jiné položky nebo jedinou instrukci nutnou před rozbalením. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Interní systém — HR portál

**Situace a cíl:** Zaměstnanec prochází související části žádosti o vybavení.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Zobrazujte obsah přiřazený správnému záhlaví. V průchodu se uplatní `state=collapsed`.

**Průchod a výsledek:** Sestavte oblast „Podrobnosti pracoviště“ s obsahem „Budova A, druhé podlaží“. Nepřenášejte sem informace jiné položky nebo jedinou instrukci nutnou před rozbalením. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit pojmenování sekcí, hierarchii titulků a vztah variant default/borderless/child a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí počet současně otevřených sekcí, výchozí otevření a případné načítání obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-26374)
