# SearchForm.Button (icon)

Ikonová podoba odesílacího tlačítka SearchForm spouští hledání a potřebuje rozpoznatelný přístupný název.

**Vazba:** SearchForm. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Ikona má přístupný název vysvětlující odeslání hledání. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě SearchForm. Ikona má přístupný název vysvětlující odeslání hledání.

## Kdy zvolit alternativu

Pro výběr konkrétní hodnoty s hledáním použijte Combobox, pro příkazy Command. Tato část zůstává součástí zadání a odeslání dotazu.

## Anatomie, stavy a varianty

Součást skladby **SearchForm**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Spustit stejné hledání jako textové odesílací tlačítko; název vysvětlí rozsah.

### Co vyvolávat nemá

- Nezaměnit ikonu hledání s vymazáním nebo zavřením.

### Přechody a odpovědnost

Dotaz se považuje za odeslaný, nikoli za již vybraný záznam. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Ikona má přístupný název vysvětlující odeslání hledání.
- Nezaměňujte ji s vymazáním dotazu nebo zavřením nabídky.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Tento ovladač odesílá hledání; ClearButton pouze maže draft. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Nulová shoda je platný výsledek s možností upravit dotaz; selhání služby nabídne opakování a zachová dotaz.

- **Pravidlo použití:** Nezaměnit ikonu hledání s vymazáním nebo zavřením.

### ERP — vyhledávání dokladů

**Situace a cíl:** Pracovník hledá objednávku podle jejího identifikátoru.

**Průchod a výsledek:** Aktivace „Hledat v objednávkách“ odešle právě dotaz „O-1048“. Aplikace teprve po odpovědi zobrazí výsledky stejného dotazu; žádný výsledek se tím nevybere.

### Web — produktový katalog

**Situace a cíl:** Návštěvník hledá konkrétní druh nářadí.

**Průchod a výsledek:** Aktivace „Hledat v produktech“ odešle právě dotaz „Aku vrtačka“. Aplikace teprve po odpovědi zobrazí výsledky stejného dotazu; žádný výsledek se tím nevybere.

### Interní systém — znalostní báze

**Situace a cíl:** Zaměstnanec hledá návod podle popisu potíží.

**Průchod a výsledek:** Aktivace „Hledat v návodech“ odešle právě dotaz „Obnovení přístupu“. Aplikace teprve po odpovědi zobrazí výsledky stejného dotazu; žádný výsledek se tím nevybere.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit pojmenování rozsahu hledání a slovník výsledků a nulové shody a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí vyhledávací zdroj, potvrzení dotazu a chování případných asynchronních požadavků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-32963)
