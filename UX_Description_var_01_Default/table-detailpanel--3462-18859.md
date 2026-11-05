# Table.DetailPanel

Detailový panel tabulky nese rozšířené informace jednoho záznamu a zachovává jeho identitu.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Rozšířené údaje patří stejnému záznamu jako nadřazený řádek. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Rozšířené údaje patří stejnému záznamu jako nadřazený řádek.

## Kdy zvolit alternativu

Pro rozsáhlý samostatný úkol otevřete detail přes Link nebo použijte Drawer. DetailPanel slouží obsahu přiřazenému konkrétnímu řádku.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Rozšířené údaje patří stejnému záznamu jako nadřazený řádek.
- Panel nesmí působit jako nový samostatný záznam.
- Panel se rozprostírá pod příslušným řádkem přes šířku tabulky; rozbalení nesmí ztratit vazbu na původní záznam.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Zachovejte čitelné přiřazení záhlaví a buněk, jednotky a identitu řádku. Odkazy a ovladače v tabulce jsou pojmenované a dostupné klávesnicí. Samotný název DataTable nedokládá vzor ARIA grid; nepřidávejte neověřené buněčné ovládání šipkami.

## Omezení a příklady podle typu projektu

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Volba a varianta:** DetailPanel zachová kontext řádku; rozsáhlý samostatný formulář otevřete v detailu nebo Drawer. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pod správným rodičovským řádkem zobrazte „Dodací adresa a položky O-1048“ přes šířku tabulky. Otevření vyvolal jeho ExpandToggle; panel se nesmí tvářit jako nový samostatný záznam.

**Výjimka a návrat:** Při sbalení přesuňte případný fokus z detailu na dosažitelné místo u téhož řádku. Načítání či chyba detailu nesmí přepsat data sousedních řádků.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Volba a varianta:** DetailPanel zachová kontext řádku; rozsáhlý samostatný formulář otevřete v detailu nebo Drawer. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pod správným rodičovským řádkem zobrazte „Průběh doručení W-248“ přes šířku tabulky. Otevření vyvolal jeho ExpandToggle; panel se nesmí tvářit jako nový samostatný záznam.

**Výjimka a návrat:** Při sbalení přesuňte případný fokus z detailu na dosažitelné místo u téhož řádku. Načítání či chyba detailu nesmí přepsat data sousedních řádků.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Volba a varianta:** DetailPanel zachová kontext řádku; rozsáhlý samostatný formulář otevřete v detailu nebo Drawer. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pod správným rodičovským řádkem zobrazte „Historie změn INC-142“ přes šířku tabulky. Otevření vyvolal jeho ExpandToggle; panel se nesmí tvářit jako nový samostatný záznam.

**Výjimka a návrat:** Při sbalení přesuňte případný fokus z detailu na dosažitelné místo u téhož řádku. Načítání či chyba detailu nesmí přepsat data sousedních řádků.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3462-18859)
