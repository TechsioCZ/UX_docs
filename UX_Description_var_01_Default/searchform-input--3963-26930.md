# SearchForm.Input

Vstup SearchForm přijímá rozepsaný vyhledávací dotaz, který se odlišuje od již odeslaného hledání.

**Vazba:** SearchForm. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Odlište právě rozepsaný dotaz od naposledy odeslaného. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě SearchForm. Odlište právě rozepsaný dotaz od naposledy odeslaného.

## Kdy zvolit alternativu

Pro výběr konkrétní hodnoty s hledáním použijte Combobox, pro příkazy Command. Tato část zůstává součástí zadání a odeslání dotazu.

## Anatomie, stavy a varianty

Součást skladby **SearchForm**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Přijmout rozepsaný vyhledávací dotaz a umožnit jeho opravu.

### Co vyvolávat nemá

- Samotným psaním nepotvrdit nalezený objekt ani neprohlásit nové výsledky za načtené.

### Přechody a odpovědnost

Psaní mění draft, ne potvrzený záznam. Kontrolu spusťte v určeném okamžiku, například při odeslání; konkrétní odmítnutí zachová text a vysvětlí opravu u stejného pole. Po nové platné kontrole chybové sdělení zanikne nebo se nahradí aktuálním výsledkem. Zrušení formuláře musí mít určené zachování či zahození draftu. Tyto kroky řídí formulář a aplikace, nikoli samotná barva vstupu.

### Konkrétní pravidla použití

- Odlište právě rozepsaný dotaz od naposledy odeslaného.
- Popisek vymezí, v jakém obsahu se hledá; placeholder jej nenahrazuje.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Pole má stálý přístupný název, viditelný význam a propojené instrukce i konkrétní chybu. Zachovejte rozepsané hodnoty při odmítnutí. Klávesnicové ovládání a čtení nesmí záviset jen na hoveru; delší text či jednotka nepřekrývají ovladače.

## Omezení a příklady podle typu projektu

### ERP — vyhledávání dokladů

**Situace a cíl:** Pracovník hledá objednávku podle jejího identifikátoru.

**Volba a varianta:** Vstup sbírá dotaz pro hledání; výběr existující identity do formuláře řeší Combobox. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pod názvem „Hledat v objednávkách“ napište „O-1048“. Dotaz zůstane draftem do aktivace odeslání; samotné psaní ani input-focus nejsou potvrzeným hledáním.

**Výjimka a návrat:** Vymazání či změna draftu se nesmí vydávat za nový načtený výsledek. Starší síťová odpověď nesmí přepsat výsledky novějšího dotazu.

**Nevhodně:** Samotným psaním nepotvrdit nalezený objekt ani neprohlásit nové výsledky za načtené.

### Web — produktový katalog

**Situace a cíl:** Návštěvník hledá konkrétní druh nářadí.

**Volba a varianta:** Vstup sbírá dotaz pro hledání; výběr existující identity do formuláře řeší Combobox. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pod názvem „Hledat v produktech“ napište „Aku vrtačka“. Dotaz zůstane draftem do aktivace odeslání; samotné psaní ani input-focus nejsou potvrzeným hledáním.

**Výjimka a návrat:** Vymazání či změna draftu se nesmí vydávat za nový načtený výsledek. Starší síťová odpověď nesmí přepsat výsledky novějšího dotazu.

**Nevhodně:** Samotným psaním nepotvrdit nalezený objekt ani neprohlásit nové výsledky za načtené.

### Interní systém — znalostní báze

**Situace a cíl:** Zaměstnanec hledá návod podle popisu potíží.

**Volba a varianta:** Vstup sbírá dotaz pro hledání; výběr existující identity do formuláře řeší Combobox. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Pod názvem „Hledat v návodech“ napište „Obnovení přístupu“. Dotaz zůstane draftem do aktivace odeslání; samotné psaní ani input-focus nejsou potvrzeným hledáním.

**Výjimka a návrat:** Vymazání či změna draftu se nesmí vydávat za nový načtený výsledek. Starší síťová odpověď nesmí přepsat výsledky novějšího dotazu.

**Nevhodně:** Samotným psaním nepotvrdit nalezený objekt ani neprohlásit nové výsledky za načtené.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit pojmenování rozsahu hledání a slovník výsledků a nulové shody a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí vyhledávací zdroj, potvrzení dotazu a chování případných asynchronních požadavků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26930)
