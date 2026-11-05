# Select/Item

Položka Select představuje jednu hodnotu, kterou lze potvrdit jako výběr pole.

**Vazba:** Select. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Každá položka představuje jednu hodnotu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Select. Každá položka představuje jednu hodnotu.

## Kdy zvolit alternativu

Pro datovou hodnotu vyberte Select, Combobox či CascadeSelect podle rozsahu a hierarchie. Pro příkaz použijte Menu; vizuálně podobný obal nesmí měnit tento význam.

## Anatomie, stavy a varianty

Součást skladby **Select**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=selected` | Pro skutečně potvrzenou vybranou položku. Hover ani pouhý fokus ji nenahrazují. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Potvrdit jednu dostupnou možnost pro nadřazené pole.

### Co vyvolávat nemá

- Neprovést příkaz nesouvisející s výběrem a nevybrat disabled možnost.

### Přechody a odpovědnost

Otevření nabídky či procházení kandidátů ještě nepotvrzuje hodnotu. Aktivace dostupné možnosti předá její identitu; zrušení procházení zachová dosavadní potvrzený výběr. Vymazání je samostatný povolený krok a povinnost se vyhodnotí ve validačním okamžiku. U vzdálených dat hostitel rozliší čekání, žádnou shodu a chybu; odpověď starého dotazu nesmí nahradit novější nabídku. PopupSurface přebírá tento model pouze od skutečného hostitele, ne podle vzhledu řádku.

### Konkrétní pravidla použití

- Každá položka představuje jednu hodnotu.
- Odlište selected, hover a disabled. Disabled možnost nelze nově aktivovat; dříve uloženou, nyní nedostupnou hodnotu hostitel nezamlčí a před potvrzením vysvětlí potřebnou nápravu.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Disabled možnost nelze vybrat. Zavření bez aktivace zachová původní hodnotu; navazující uložení formuláře je samostatné.

- **Pravidlo použití:** Neprovést příkaz nesouvisející s výběrem a nevybrat disabled možnost.

### ERP — zakázkový formulář

**Situace a cíl:** Pracovník přiřazuje zakázku existujícímu středisku.

**Volba a varianta:** Item potvrzuje datovou hodnotu; příkaz nad záznamem patří do Menu. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** V nabídce pole „Středisko“ aktivujte dostupnou možnost „Logistika“. Do pole se předá její identifikátor i odpovídající text; samotný fokus položku nepotvrdí.

### Web — nastavení doručení

**Situace a cíl:** Zákazník vybírá z nabízených zemí pro danou službu.

**Volba a varianta:** Item potvrzuje datovou hodnotu; příkaz nad záznamem patří do Menu. V průchodu se uplatní `state=selected`.

**Průchod a výsledek:** V nabídce pole „Země doručení“ aktivujte dostupnou možnost „Česko“. Do pole se předá její identifikátor i odpovídající text; samotný fokus položku nepotvrdí.

### Interní systém — ITSM

**Situace a cíl:** Žadatel volí prioritu z předem vysvětleného seznamu.

**Volba a varianta:** Item potvrzuje datovou hodnotu; příkaz nad záznamem patří do Menu. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** V nabídce pole „Priorita požadavku“ aktivujte dostupnou možnost „Běžná“. Do pole se předá její identifikátor i odpovídající text; samotný fokus položku nepotvrdí.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-24603)
