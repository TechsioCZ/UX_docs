# .SidebarTooltipDock

Interní .SidebarTooltipDock poskytuje referenční ukotvení nápovědy Sidebar.

**Vazba:** Sidebar. Tato část je konkrétní reference, nikoli automaticky nový veřejný export.

## Kdy použít

Ukotvuje nápovědu ke správné položce Sidebar. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Sidebar. Jde o referenční či starší skladbu; její místní nastavení není univerzální veřejné pravidlo.

## Kdy zvolit alternativu

Pro provozní sestavení vyberte veřejné části rodiny Sidebar. Referenční příklad nekopírujte jako nový export, pravidlo značky nebo důkaz dokončeného procesu.

## Anatomie, stavy a varianty

Součást skladby **Sidebar**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `placement=right` | Polohu right volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=left` | Polohu left volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Posoudit tuto konkrétní referenční skladbu před volbou veřejného řešení.

### Co vyvolávat nemá

- Nepřenést ukázková data, lokální rozměr nebo starší pojmenování jako univerzální pravidlo projektu.

### Přechody a odpovědnost

Reference slouží posouzení uvedené skladby. Přechod do provozního použití znamená volbu konkrétních veřejných částí a jejich skutečných stavů, nikoli automatickou aktivaci celého ukázkového frame. Lokální chování příkladu se nepřenáší na celou rodinu.

### Konkrétní pravidla použití

- Ukotvuje nápovědu ke správné položce Sidebar.
- Obsah tooltipu musí odpovídat názvu jejího cíle.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Jde o konkrétní referenci, nikoli další obecný veřejný ovladač; provozní skladba musí mít určené části. V průchodu se uplatní `placement=right`.

- **Společné výjimky a návrat:** Odlišná šířka, lokální override nebo staré pojmenování se nepřenáší automaticky. Obsah tooltipu musí odpovídat názvu jejího cíle.

- **Nevhodné použití:** Převzít lokální rozměr nebo ukázkové chování jako univerzální pravidlo rodiny či značky.

### ERP — víceagendová aplikace

**Situace a cíl:** Pracovník prochází nákup, sklad a související přehledy.

**Průchod a výsledek:** Při návrhu oblasti „Objednávky“ posuďte referenci „Agenda Nákup / Objednávky“. Ukotvuje nápovědu ke správné položce Sidebar. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

### Web — zákaznický účet na desktopu

**Situace a cíl:** Zákazník na větší obrazovce potřebuje dosáhnout navigace svého účtu i při sbaleném bočním rámci.

**Průchod a výsledek:** Při návrhu oblasti „Moje objednávky“ posuďte referenci „Navigace zákaznického účtu“. Ukotvuje nápovědu ke správné položce Sidebar. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

### Interní systém — projektový nástroj

**Situace a cíl:** Člen týmu přechází mezi pracovním seznamem a detaily projektu.

**Průchod a výsledek:** Při návrhu oblasti „Projekt Orion“ posuďte referenci „Přehled / Úkoly / Dokumenty“. Ukotvuje nápovědu ke správné položce Sidebar. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit šířkovou a vizuální hierarchii rámu, názvy cílů a pravidla zobrazení identity značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí nabídku agend, oprávnění, zvolený režim a zachování kontextu při změně zařízení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3084-233)
