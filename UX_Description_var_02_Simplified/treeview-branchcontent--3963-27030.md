# TreeView/BranchContent

Obsah větve TreeView nese potomky rozbaleného uzlu; sám není spouštěčem rozbalení.

**Vazba:** TreeView. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Obsahuje potomky správné větve. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě TreeView. Obsahuje potomky správné větve.

## Kdy zvolit alternativu

Pro datovou hodnotu vyberte Select, Combobox či CascadeSelect podle rozsahu a hierarchie. Pro příkaz použijte Menu; vizuálně podobný obal nesmí měnit tento význam.

## Anatomie, stavy a varianty

Součást skladby **TreeView**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Obsahuje potomky správné větve.
- Sám nenahrazuje ovladač rozbalení ani označení rodiče.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Obsahuje potomky správné větve. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

- **Nevhodné použití:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### ERP — struktura organizace

**Situace a cíl:** Pracovník prochází organizační členění před přiřazením zakázky.

**Průchod a výsledek:** Sestavte oblast „Organizační struktura“ s obsahem „Sklad Brno; Sklad Znojmo“. Sám nenahrazuje ovladač rozbalení ani označení rodiče. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Web — správa dokumentů

**Situace a cíl:** Přihlášený uživatel prochází své složky a vybírá související dokument.

**Průchod a výsledek:** Sestavte oblast „Vaše dokumenty“ s obsahem „Podklady; Výstupy“. Sám nenahrazuje ovladač rozbalení ani označení rodiče. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Interní systém — DMS archiv

**Situace a cíl:** Správce prochází projektové složky.

**Průchod a výsledek:** Sestavte oblast „Archiv projektů“ s obsahem „Smlouvy; Dodatky“. Sám nenahrazuje ovladač rozbalení ani označení rodiče. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy uzlů, ikonografii druhů položek a čitelnost hierarchie a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí datové vztahy, pravidla výběru a případné načítání potomků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-27030)
