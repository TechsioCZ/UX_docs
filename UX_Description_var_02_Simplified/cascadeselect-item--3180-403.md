# CascadeSelect/Item

Položka CascadeSelect představuje větev nebo list a odlišuje navigaci do potomků od potvrzení hodnoty.

**Vazba:** CascadeSelect. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Odlište větev od listu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě CascadeSelect. Odlište větev od listu.

## Kdy zvolit alternativu

Pro datovou hodnotu vyberte Select, Combobox či CascadeSelect podle rozsahu a hierarchie. Pro příkaz použijte Menu; vizuálně podobný obal nesmí měnit tento význam.

## Anatomie, stavy a varianty

Součást skladby **CascadeSelect**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=xs` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `type=leaf` | Pro koncový uzel bez dalšího rozbalení. |
| `type=branch` | Položka s potomky; otevírání a případný výběr rodiče jsou odlišná rozhodnutí. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=selected` | Pro skutečně potvrzenou vybranou položku. Hover ani pouhý fokus ji nenahrazují. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `dir=ltr` | Pro levopravý jazyk a odpovídající logické směry. |
| `dir=rtl` | Pro pravolevý jazyk; obrátit logické uspořádání a odpovídající směrové značky, ne význam akcí. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- U větve zpřístupnit potomky; u přípustného listu potvrdit výběr.

### Co vyvolávat nemá

- Otevřením rodiče nepotvrdit hodnotu, pokud tento režim rodiče nevybírá.

### Přechody a odpovědnost

Otevření nabídky či procházení kandidátů ještě nepotvrzuje hodnotu. Aktivace dostupné možnosti předá její identitu; zrušení procházení zachová dosavadní potvrzený výběr. Vymazání je samostatný povolený krok a povinnost se vyhodnotí ve validačním okamžiku. U vzdálených dat hostitel rozliší čekání, žádnou shodu a chybu; odpověď starého dotazu nesmí nahradit novější nabídku. PopupSurface přebírá tento model pouze od skutečného hostitele, ne podle vzhledu řádku.

### Konkrétní pravidla použití

- Odlište větev od listu.
- Otevření potomků a potvrzení hodnoty jsou různé výsledky; výběr rodiče závisí na nastavení výběru.
- Velikost položky se řídí kořenem CascadeSelect; vybraná větev je přípustná při povoleném výběru rodiče.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Návrat k rodiči zachová rozlišení mezi procházenou cestou a potvrzenou hodnotou. Výběr rodičů povolte jen v ověřeném režimu.

- **Nevhodné použití:** Otevřením rodiče nepotvrdit hodnotu, pokud tento režim rodiče nevybírá.

### ERP — účetní dimenze

**Situace a cíl:** Pracovník přiřazuje zakázku organizační jednotce ve stromu.

**Volba a varianta:** Položka potřebuje skutečný vztah rodiče a potomků; plochou sadu řeší Select/Item. V průchodu se uplatní `type=leaf`, `state=default`.

**Průchod a výsledek:** V cestě „Firma / Logistika / Sklad Brno“ otevřete rodiče a potom jeho další úroveň. Teprve dostupný vybíratelný list potvrďte do pole; otevření větve nepotvrdí rodiče.

### Web — vyhledávání služby

**Situace a cíl:** Návštěvník vybírá provozovnu podle oblasti a města.

**Volba a varianta:** Položka potřebuje skutečný vztah rodiče a potomků; plochou sadu řeší Select/Item. V průchodu se uplatní `type=leaf`, `state=selected`.

**Průchod a výsledek:** V cestě „Jižní Morava / Znojmo / Centrum“ otevřete rodiče a potom jeho další úroveň. Teprve dostupný vybíratelný list potvrďte do pole; otevření větve nepotvrdí rodiče.

### Interní systém — dokumentový portál

**Situace a cíl:** Uživatel zařazuje soubor do adresářové struktury.

**Volba a varianta:** Položka potřebuje skutečný vztah rodiče a potomků; plochou sadu řeší Select/Item. V průchodu se uplatní `type=leaf`, `state=default`.

**Průchod a výsledek:** V cestě „Projekty / Orion / Podklady“ otevřete rodiče a potom jeho další úroveň. Teprve dostupný vybíratelný list potvrďte do pole; otevření větve nepotvrdí rodiče.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy úrovní, zápis celé cesty a směrové uspořádání jazyka značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí datovou hierarchii, výběr listů či rodičů, vícenásobnost a validaci. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3180-403)
