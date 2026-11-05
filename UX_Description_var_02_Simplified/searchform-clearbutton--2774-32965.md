# SearchForm.ClearButton

Vymazávací tlačítko SearchForm odstraňuje rozepsaný dotaz; změna již zobrazených výsledků je samostatné rozhodnutí.

**Vazba:** SearchForm. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Vymazání odstraňuje zadaný dotaz. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě SearchForm. Vymazání odstraňuje zadaný dotaz.

## Kdy zvolit alternativu

Pro výběr konkrétní hodnoty s hledáním použijte Combobox, pro příkazy Command. Tato část zůstává součástí zadání a odeslání dotazu.

## Anatomie, stavy a varianty

Součást skladby **SearchForm**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Vymazat rozepsaný dotaz v příslušném hledání.

### Co vyvolávat nemá

- Nevydávat vymazání za odstranění výsledků z databáze ani zrušení hotového požadavku.

### Přechody a odpovědnost

Prázdný vstup je odlišený od posledního potvrzeného hledání podle modelu produktu. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Vymazání odstraňuje zadaný dotaz.
- Dopad na již zobrazené výsledky určuje vyhledávání; vymazání se nesmí vydávat za zrušení dokončené operace.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Vymazání dotazu má jiný účel než odeslání hledání nebo zavření panelu. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Produkt musí odlišit prázdný draft od posledního odeslaného dotazu a určit, kdy zobrazí výchozí výsledky. Vymazání samo negarantuje zrušení běžícího požadavku.

- **Pravidlo použití:** Nevydávat vymazání za odstranění výsledků z databáze ani zrušení hotového požadavku.

### ERP — vyhledávání dokladů

**Situace a cíl:** Pracovník hledá objednávku podle jejího identifikátoru.

**Průchod a výsledek:** U hledání „Hledat v objednávkách“ vymažte rozepsaný dotaz „O-1048“. Fokus zůstane v použitelném hledání; záznamy se neodstraňují.

### Web — produktový katalog

**Situace a cíl:** Návštěvník hledá konkrétní druh nářadí.

**Průchod a výsledek:** U hledání „Hledat v produktech“ vymažte rozepsaný dotaz „Aku vrtačka“. Fokus zůstane v použitelném hledání; záznamy se neodstraňují.

### Interní systém — znalostní báze

**Situace a cíl:** Zaměstnanec hledá návod podle popisu potíží.

**Průchod a výsledek:** U hledání „Hledat v návodech“ vymažte rozepsaný dotaz „Obnovení přístupu“. Fokus zůstane v použitelném hledání; záznamy se neodstraňují.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit pojmenování rozsahu hledání a slovník výsledků a nulové shody a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí vyhledávací zdroj, potvrzení dotazu a chování případných asynchronních požadavků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-32965)
