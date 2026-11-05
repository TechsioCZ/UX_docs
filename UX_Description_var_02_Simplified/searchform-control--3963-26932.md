# SearchForm.Control

Ovládací oblast SearchForm skládá textový vstup a související ovladače jednoho hledání.

**Vazba:** SearchForm. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Spojte vstup, odeslání a případné vymazání jednoho dotazu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě SearchForm. Spojte vstup, odeslání a případné vymazání jednoho dotazu.

## Kdy zvolit alternativu

Pro výběr konkrétní hodnoty s hledáním použijte Combobox, pro příkazy Command. Tato část zůstává součástí zadání a odeslání dotazu.

## Anatomie, stavy a varianty

Součást skladby **SearchForm**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Spojte vstup, odeslání a případné vymazání jednoho dotazu.
- Každý ovladač má rozpoznatelný výsledek a nesmí překrývat zadaný text.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Samotná oblast nepřebírá jména a akce svých ovladačů. Vnořené odkazy a tlačítka mají vlastní názvy a logické pořadí. Při menší šířce zůstává dosažitelný celý podstatný obsah, nikoli jen první viditelná část.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Spojte vstup, odeslání a případné vymazání jednoho dotazu. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

- **Nevhodné použití:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### ERP — vyhledávání dokladů

**Situace a cíl:** Pracovník hledá objednávku podle jejího identifikátoru.

**Průchod a výsledek:** Sestavte oblast „Hledat v objednávkách“ s obsahem „O-1048“. Každý ovladač má rozpoznatelný výsledek a nesmí překrývat zadaný text. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Web — produktový katalog

**Situace a cíl:** Návštěvník hledá konkrétní druh nářadí.

**Průchod a výsledek:** Sestavte oblast „Hledat v produktech“ s obsahem „Aku vrtačka“. Každý ovladač má rozpoznatelný výsledek a nesmí překrývat zadaný text. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Interní systém — znalostní báze

**Situace a cíl:** Zaměstnanec hledá návod podle popisu potíží.

**Průchod a výsledek:** Sestavte oblast „Hledat v návodech“ s obsahem „Obnovení přístupu“. Každý ovladač má rozpoznatelný výsledek a nesmí překrývat zadaný text. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit pojmenování rozsahu hledání a slovník výsledků a nulové shody a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí vyhledávací zdroj, potvrzení dotazu a chování případných asynchronních požadavků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26932)
