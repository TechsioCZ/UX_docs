# SearchForm

Vyhledávací formulář přijímá dotaz a nabízí jeho odeslání.

Cílem je zadat dotaz, vědomě spustit hledání a rozpoznat, k jakým výsledkům dotaz vedl.

## Kdy použít

Pro vědomé odeslání dotazu do pojmenovaného rozsahu výsledků. Psaní, odeslání a otevření výsledku jsou různé kroky. Pro výběr jedné hodnoty do pole použijte Combobox.

## Kdy zvolit alternativu

Pro potvrzení hodnoty z nabídky použijte Combobox, pro příkazy Command.

## Anatomie, stavy a varianty

Label, Input a odesílací Button v Control; podle potřeby také ClearButton. Ikonová a textová odesílací podoba mají stejný účel, vymazání jiný.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=input-focus` | Když je fokus ve vyhledávacím vstupu. Dotaz tím ještě není odeslán. |
| `state=button-focus` | Když je fokus na odesílacím tlačítku hledání. Samotný fokus hledání nespouští. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `gapped=false` | Pro vizuálně spojenou skladbu jednoho hledání. |
| `gapped=true` | Když jsou ovladač a odesílací tlačítko vizuálně oddělené, ale stále tvoří jedno hledání. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Odeslat aktuální dotaz pojmenovaným tlačítkem nebo odpovídajícím formulářovým ovládáním.
- Samostatně vymazat rozepsaný dotaz, pokud je vymazání nabídnuté.

### Co vyvolávat nemá

- Nezaměňovat odeslání hledání s výběrem výsledku.
- Nepředpokládat našeptávání ani filtrování při každém znaku bez určeného produktu.

### Přechody a odpovědnost

Vstup drží draft dotazu; input-focus a button-focus neodesílají. Aktivace odeslání předá dotaz aplikaci a ta odliší čekání, výsledky, nulovou shodu a selhání. Neúspěch zachová dotaz pro opakování; výsledek starého dotazu nepřepíše novější. Vymazání má určený vztah k poslednímu odeslanému hledání a neodstraňuje záznamy.

### Konkrétní pravidla použití

- Popisek vymezí rozsah hledání.
- Odlište rozepsaný a skutečně odeslaný dotaz.
- Vymazání vstupu není automaticky zrušení již provedeného hledání.
- Prázdný výsledek odlište od selhání služby.
- Našeptávání a filtrování za běhu jsou samostatná rozhodnutí, nikoli automatická součást formuláře.
- Při asynchronním hledání nesmí starší odpověď přepsat výsledky novějšího dotazu. Potvrzení dotazu musí být dostupné i z klávesnice.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nezaměňovat odeslání hledání s výběrem výsledku.

### ERP — vyhledávání dokladů

**Situace a cíl:** Pracovník hledá objednávku podle jejího identifikátoru.

**Volba a varianta:** Dotaz „O-1048“ hledá v rozsahu „Hledat v objednávkách“; nepotvrzuje identitu jako Combobox. V průchodu se uplatní `state=default`, `gapped=false`.

**Průchod a výsledek:** Pro objekt „O-1048“ použijte pojmenování „Hledat v objednávkách“. Zadání dotazu a akce „Vyhledat objednávku“ jsou dva rozlišitelné kroky. Fokus vstupu ukazuje input-focus a fokus odesílání button-focus; žádný z nich sám neprovede hledání. Po odeslání aplikace odliší výsledky, nulovou shodu a selhání; tato sada formuláře tím nezískává novou doloženou osu error.

**Výjimka a návrat:** Rozepsání O-1049 nezmění označení naposledy potvrzených výsledků, dokud není určené nové hledání.

### Web — produktový katalog

**Situace a cíl:** Návštěvník hledá konkrétní druh nářadí.

**Volba a varianta:** Dotaz „Aku vrtačka“ hledá v rozsahu „Hledat v produktech“; nepotvrzuje identitu jako Combobox. V průchodu se uplatní `state=default`, `gapped=false`.

**Průchod a výsledek:** Pro objekt „Aku vrtačka“ použijte pojmenování „Hledat v produktech“. Zadání dotazu a akce „Vyhledat produkty“ jsou dva rozlišitelné kroky. Fokus vstupu ukazuje input-focus a fokus odesílání button-focus; žádný z nich sám neprovede hledání. Po odeslání aplikace odliší výsledky, nulovou shodu a selhání; tato sada formuláře tím nezískává novou doloženou osu error.

**Výjimka a návrat:** Vymazání vstupu se nepředstírá jako zrušení už dokončeného hledání; model výsledků je určený zvlášť.

### Interní systém — znalostní báze

**Situace a cíl:** Zaměstnanec hledá návod podle popisu potíží.

**Volba a varianta:** Dotaz „Obnovení přístupu“ hledá v rozsahu „Hledat v návodech“; nepotvrzuje identitu jako Combobox. V průchodu se uplatní `state=default`, `gapped=false`.

**Průchod a výsledek:** Pro objekt „Obnovení přístupu“ použijte pojmenování „Hledat v návodech“. Zadání dotazu a akce „Vyhledat návod“ jsou dva rozlišitelné kroky. Fokus vstupu ukazuje input-focus a fokus odesílání button-focus; žádný z nich sám neprovede hledání. Po odeslání aplikace odliší výsledky, nulovou shodu a selhání; tato sada formuláře tím nezískává novou doloženou osu error.

**Výjimka a návrat:** Selhání služby není text Nenašli jsme žádný návod, protože neprokazuje nulovou shodu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit pojmenování rozsahu hledání a slovník výsledků a nulové shody a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí vyhledávací zdroj, potvrzení dotazu a chování případných asynchronních požadavků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-32835)
