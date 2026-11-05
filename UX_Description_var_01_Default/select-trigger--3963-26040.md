# Select/Trigger

Spouštěč Select zpřístupňuje nabídku možností pro pojmenované pole.

**Vazba:** Select. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Spouštěč ovládá právě svou nabídku. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Select. Spouštěč ovládá právě svou nabídku.

## Kdy zvolit alternativu

Pro datovou hodnotu vyberte Select, Combobox či CascadeSelect podle rozsahu a hierarchie. Pro příkaz použijte Menu; vizuálně podobný obal nesmí měnit tento význam.

## Anatomie, stavy a varianty

Součást skladby **Select**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít a zavřít nabídku konkrétního pole; vrátit se bez změny potvrzené hodnoty.

### Co vyvolávat nemá

- Nepotvrdit první možnost pouhým otevřením.

### Přechody a odpovědnost

Otevření nabídky či procházení kandidátů ještě nepotvrzuje hodnotu. Aktivace dostupné možnosti předá její identitu; zrušení procházení zachová dosavadní potvrzený výběr. Vymazání je samostatný povolený krok a povinnost se vyhodnotí ve validačním okamžiku. U vzdálených dat hostitel rozliší čekání, žádnou shodu a chybu; odpověď starého dotazu nesmí nahradit novější nabídku. PopupSurface přebírá tento model pouze od skutečného hostitele, ne podle vzhledu řádku.

### Konkrétní pravidla použití

- Spouštěč ovládá právě svou nabídku.
- Otevření samo nemění potvrzenou hodnotu; stav otevření musí odpovídat zobrazenému obsahu.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — zakázkový formulář

**Situace a cíl:** Pracovník přiřazuje zakázku existujícímu středisku.

**Volba a varianta:** Trigger zpřístupňuje plochý výběr; datové hledání by potřebovalo Combobox. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** U pole „Středisko“ aktivace otevře jeho volby, například „Logistika“. Opětovné zavření bez výběru zachová dosavadní hodnotu; otevření ji nenahradí první položkou.

**Výjimka a návrat:** Po zavření se fokus vrátí ke stejnému spouštěči. Disabled nabídku neotevře; důvod nedostupnosti je zjistitelný.

**Nevhodně:** Nepotvrdit první možnost pouhým otevřením.

### Web — nastavení doručení

**Situace a cíl:** Zákazník vybírá z nabízených zemí pro danou službu.

**Volba a varianta:** Trigger zpřístupňuje plochý výběr; datové hledání by potřebovalo Combobox. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** U pole „Země doručení“ aktivace otevře jeho volby, například „Česko“. Opětovné zavření bez výběru zachová dosavadní hodnotu; otevření ji nenahradí první položkou.

**Výjimka a návrat:** Po zavření se fokus vrátí ke stejnému spouštěči. Disabled nabídku neotevře; důvod nedostupnosti je zjistitelný.

**Nevhodně:** Nepotvrdit první možnost pouhým otevřením.

### Interní systém — ITSM

**Situace a cíl:** Žadatel volí prioritu z předem vysvětleného seznamu.

**Volba a varianta:** Trigger zpřístupňuje plochý výběr; datové hledání by potřebovalo Combobox. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** U pole „Priorita požadavku“ aktivace otevře jeho volby, například „Běžná“. Opětovné zavření bez výběru zachová dosavadní hodnotu; otevření ji nenahradí první položkou.

**Výjimka a návrat:** Po zavření se fokus vrátí ke stejnému spouštěči. Disabled nabídku neotevře; důvod nedostupnosti je zjistitelný.

**Nevhodně:** Nepotvrdit první možnost pouhým otevřením.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26040)
