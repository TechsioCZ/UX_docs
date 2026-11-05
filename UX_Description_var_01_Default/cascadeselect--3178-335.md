# CascadeSelect

Hierarchický výběr umožňuje postupně projít větve a vybrat hodnotu z jejich kontextu.

Cílem je potvrdit hodnotu se znalostí jejího místa ve víceúrovňové hierarchii.

## Kdy použít

Pro výběr hodnoty, jejíž význam závisí na rodičovské cestě. Musí existovat skutečná hierarchie a určené vybíratelné úrovně. Pro plochý seznam použijte Select; pro navigaci mezi stránkami VerticalNavigation.

## Kdy zvolit alternativu

Pro plochý seznam použijte Select, pro hledání v možnostech Combobox, pro průzkum stromu TreeView.

## Anatomie, stavy a varianty

Pojmenované pole, obsahové panely jednotlivých úrovní a položky branch/leaf. Zobrazená cesta odlišuje výběr od pouhého otevření rodiče.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=xs` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=readonly` | Když má být existující hodnota čitelná, ale není dovoleno ji měnit. Nezaměňovat za disabled ani za prázdnou hodnotu. |
| `state=error` | Po zjištění konkrétního opravitelného problému. Zpráva pojmenuje údaj a nápravu; rozepsaná hodnota zůstane k opravě. |
| `state=success` | Po skutečném ověření údaje v daném kontextu. Neznamená automaticky úspěšné uložení celého formuláře. |
| `state=warning` | Pro skutečnou podmínku vyžadující pozornost, při které je pokračování možné. Blokující chyba patří do error/invalid. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=focus` | Při skutečném klávesnicovém fokusu. Poloha fokusu zůstává odlišitelná od vybrané hodnoty a aktivace. |
| `required=false` | Když lze údaj vědomě nevyplnit; absence není automaticky chyba. |
| `required=true` | Když proces skutečně vyžaduje údaj. Stejná podmínka platí ve validaci. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít potomky větve, vrátit se k rodiči a potvrdit dostupný list.
- Výběr rodičů nebo více hodnot povolit jen v určeném režimu.

### Co vyvolávat nemá

- Nezaměňovat otevření větve s potvrzením hodnoty.
- Neodvozovat strom z pouhého řazení textů bez skutečných vztahů.

### Přechody a odpovědnost

Otevření nabídky či procházení kandidátů ještě nepotvrzuje hodnotu. Aktivace dostupné možnosti předá její identitu; zrušení procházení zachová dosavadní potvrzený výběr. Vymazání je samostatný povolený krok a povinnost se vyhodnotí ve validačním okamžiku. U vzdálených dat hostitel rozliší čekání, žádnou shodu a chybu; odpověď starého dotazu nesmí nahradit novější nabídku. PopupSurface přebírá tento model pouze od skutečného hostitele, ne podle vzhledu řádku.

### Konkrétní pravidla použití

- Odlište otevření větve od potvrzení uzlu.
- U jedné hodnoty zachovejte význam celé cesty. U více hodnot rozlište stejně pojmenované listy v různých větvích.
- Výběr rodiče používejte podle nastavení daného výběru.
- Depth v ukázkách vyjadřuje otevřenou cestu, nikoli další samostatný parametr.
- Zachovejte celou vybranou cestu ve stavu formuláře. V uvedeném modelu šipky procházejí hierarchii, Enter vybírá list a Escape zavírá nabídku.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — účetní dimenze

**Situace a cíl:** Pracovník přiřazuje zakázku organizační jednotce ve stromu.

**Volba a varianta:** Do pole „Organizační jednotka“ se vybírá konkrétní identita „Firma / Logistika / Sklad Brno“. Její cesta vyžaduje průchod rodiči; plochý Select by ji nevysvětlil. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „Firma / Logistika / Sklad Brno“ použijte pojmenování „Organizační jednotka“. Otevřete příslušné úrovně a odlište rodiče od potvrzovaného listu. Potvrďte „Firma / Logistika / Sklad Brno“ až aktivací příslušné položky. Při chybě povinného výběru použijte error se zprávou u pole, nikoli výběr první možnosti bez souhlasu. Samostatné uložení produktu se řídí jeho určenou potvrzovací akcí.

**Výjimka a návrat:** Otevření Logistika nepotvrdí rodiče, pokud je povolený jen výběr koncové jednotky.

**Nevhodně:** Nezaměňovat otevření větve s potvrzením hodnoty.

### Web — vyhledávání služby

**Situace a cíl:** Návštěvník vybírá provozovnu podle oblasti a města.

**Volba a varianta:** Do pole „Provozovna“ se vybírá konkrétní identita „Jižní Morava / Znojmo / Centrum“. Její cesta vyžaduje průchod rodiči; plochý Select by ji nevysvětlil. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „Jižní Morava / Znojmo / Centrum“ použijte pojmenování „Provozovna“. Otevřete příslušné úrovně a odlište rodiče od potvrzovaného listu. Potvrďte „Jižní Morava / Znojmo / Centrum“ až aktivací příslušné položky. Při chybě povinného výběru použijte error se zprávou u pole, nikoli výběr první možnosti bez souhlasu. Samostatné uložení produktu se řídí jeho určenou potvrzovací akcí.

**Výjimka a návrat:** Nedostupná pobočka nevypadá jako platně potvrzená volba a návrat k rodiči nesmaže potichu předchozí hodnotu.

**Nevhodně:** Nezaměňovat otevření větve s potvrzením hodnoty.

### Interní systém — dokumentový portál

**Situace a cíl:** Uživatel zařazuje soubor do adresářové struktury.

**Volba a varianta:** Do pole „Cílová složka“ se vybírá konkrétní identita „Projekty / Orion / Podklady“. Její cesta vyžaduje průchod rodiči; plochý Select by ji nevysvětlil. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „Projekty / Orion / Podklady“ použijte pojmenování „Cílová složka“. Otevřete příslušné úrovně a odlište rodiče od potvrzovaného listu. Potvrďte „Projekty / Orion / Podklady“ až aktivací příslušné položky. Při chybě povinného výběru použijte error se zprávou u pole, nikoli výběr první možnosti bez souhlasu. Samostatné uložení produktu se řídí jeho určenou potvrzovací akcí.

**Výjimka a návrat:** RTL upraví směry otevírání a značky; význam rodiče a potomka zůstává stejný.

**Nevhodně:** Nezaměňovat otevření větve s potvrzením hodnoty.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy úrovní, zápis celé cesty a směrové uspořádání jazyka značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí datovou hierarchii, výběr listů či rodičů, vícenásobnost a validaci. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3178-335)
