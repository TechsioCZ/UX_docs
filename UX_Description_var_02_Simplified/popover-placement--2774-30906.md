# Popover/Placement

Referenční sada Popover/Placement ukazuje polohu panelu vůči spouštěči.

**Vazba:** Popover. Tato část je konkrétní reference, nikoli automaticky nový veřejný export.

## Kdy použít

Ukazuje polohy vůči spouštěči. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Popover. Jde o referenční či starší skladbu; její místní nastavení není univerzální veřejné pravidlo.

## Kdy zvolit alternativu

Pro provozní sestavení vyberte veřejné části rodiny Popover. Referenční příklad nekopírujte jako nový export, pravidlo značky nebo důkaz dokončeného procesu.

## Anatomie, stavy a varianty

Součást skladby **Popover**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `placement=top` | Polohu top volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=top-start` | Polohu top-start volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=top-end` | Polohu top-end volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=right` | Polohu right volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=right-start` | Polohu right-start volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=right-end` | Polohu right-end volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=bottom` | Polohu bottom volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=bottom-start` | Polohu bottom-start volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=bottom-end` | Polohu bottom-end volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=left` | Polohu left volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=left-start` | Polohu left-start volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=left-end` | Polohu left-end volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Posoudit tuto konkrétní referenční skladbu před volbou veřejného řešení.

### Co vyvolávat nemá

- Nepřenést ukázková data, lokální rozměr nebo starší pojmenování jako univerzální pravidlo projektu.

### Přechody a odpovědnost

Reference slouží posouzení uvedené skladby. Přechod do provozního použití znamená volbu konkrétních veřejných částí a jejich skutečných stavů, nikoli automatickou aktivaci celého ukázkového frame. Lokální chování příkladu se nepřenáší na celou rodinu.

### Konkrétní pravidla použití

- Ukazuje polohy vůči spouštěči.
- Jde o referenci umístění, nikoli potvrzení automatického přepozicování při kolizi.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

U interaktivní vrstvy určete počáteční fokus, dostupné zavření a logický návrat. Modální použití drží fokus uvnitř, nemodální ho nesmí bezdůvodně uvěznit. Na malé obrazovce a při dlouhém obsahu zůstanou dosažitelné důležité akce i konec úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Jde o konkrétní referenci, nikoli další obecný veřejný ovladač; provozní skladba musí mít určené části. V průchodu se uplatní `placement=top`.

- **Společné výjimky a návrat:** Odlišná šířka, lokální override nebo staré pojmenování se nepřenáší automaticky. Jde o referenci umístění, nikoli potvrzení automatického přepozicování při kolizi.

- **Nevhodné použití:** Převzít lokální rozměr nebo ukázkové chování jako univerzální pravidlo rodiny či značky.

### ERP — lokální filtr seznamu

**Situace a cíl:** Pracovník upravuje krátkou podmínku u konkrétního sloupce.

**Průchod a výsledek:** Při návrhu oblasti „Filtrovat datum dodání“ posuďte referenci „Podmínka termínu dodání“. Ukazuje polohy vůči spouštěči. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

### Web — informace o variantě

**Situace a cíl:** Návštěvník otevírá stručný doplněk u vybrané nabídky.

**Průchod a výsledek:** Při návrhu oblasti „Podrobnosti varianty“ posuďte referenci „Vrtačka s kufrem“. Ukazuje polohy vůči spouštěči. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

### Interní systém — výběr členů

**Situace a cíl:** Koordinátor doplňuje krátký výběr u pracovní položky.

**Průchod a výsledek:** Při návrhu oblasti „Přiřadit členy“ posuďte referenci „Úkol U-58“. Ukazuje polohy vůči spouštěči. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii nadpisu, podobu lokálních vrstev a pojmenování jejich akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí obsah úkolu, zacházení s rozepsanými změnami a chování při kolizi s okrajem. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-30906)
