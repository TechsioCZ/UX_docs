# Drawer/Side

Starší boční Drawer na stránce Dialog kombinuje fyzické left/right, velikost a modal/modeless.

**Vazba:** Dialog. Tato část je konkrétní reference, nikoli automaticky nový veřejný export.

## Kdy použít

Používá fyzické left/right, velikosti a modal/modeless původního Dialog API. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Dialog. Jde o referenční či starší skladbu; její místní nastavení není univerzální veřejné pravidlo.

## Kdy zvolit alternativu

Pro nový boční kontextový panel zvažte Drawer.Side. Starší fyzické left/right a nové logické start/end nepovažujte za automaticky zaměnitelné konfigurace.

## Anatomie, stavy a varianty

**Omezení konfigurace:** Starší Drawer/Side má ve zdroji duplicitní kombinace variant. Před použitím musí být určena konkrétní instance; fyzické left/right nelze automaticky přepsat na logické start/end nového Drawer.Side.

Součást skladby **Dialog**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `placement=left` | Polohu left volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=right` | Polohu right volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `size=xs` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `size=xl` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `size=full` | Pro využití dostupné plochy s čitelným obsahem; neznamená automatický responzivní breakpoint. |
| `behavior=modal` | Pro modální použití s řízeným fokusem a omezenou prací na pozadí. |
| `behavior=modeless` | Pouze v konfiguraci, která skutečně dovoluje současnou práci mimo panel; neodvozovat podporu z jiného masteru. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Posoudit tuto konkrétní referenční skladbu před volbou veřejného řešení.

### Co vyvolávat nemá

- Nepřenést ukázková data, lokální rozměr nebo starší pojmenování jako univerzální pravidlo projektu.

### Přechody a odpovědnost

Reference slouží posouzení uvedené skladby. Přechod do provozního použití znamená volbu konkrétních veřejných částí a jejich skutečných stavů, nikoli automatickou aktivaci celého ukázkového frame. Lokální chování příkladu se nepřenáší na celou rodinu.

### Konkrétní pravidla použití

- Používá fyzické left/right, velikosti a modal/modeless původního Dialog API.
- Sada má duplicitní kombinace; aktuální konfiguraci nelze jednoznačně určit jen podle názvu varianty.
- Nepovažujte ji automaticky za alias nového Drawer.Side.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

U interaktivní vrstvy určete počáteční fokus, dostupné zavření a logický návrat. Modální použití drží fokus uvnitř, nemodální ho nesmí bezdůvodně uvěznit. Na malé obrazovce a při dlouhém obsahu zůstanou dosažitelné důležité akce i konec úkolu.

## Omezení a příklady podle typu projektu

### ERP — odstranění konceptu

**Situace a cíl:** Pracovník chce odstranit přesně určený rozpracovaný doklad.

**Volba a varianta:** Jde o konkrétní referenci, nikoli další obecný veřejný ovladač; provozní skladba musí mít určené části. V průchodu se uplatní `placement=left`, `behavior=modal`.

**Průchod a výsledek:** Při návrhu oblasti „Odstranit koncept O-1048“ posuďte referenci „Koncept objednávky O-1048“. Používá fyzické left/right, velikosti a modal/modeless původního Dialog API. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

**Výjimka a návrat:** Odlišná šířka, lokální override nebo staré pojmenování se nepřenáší automaticky. Sada má duplicitní kombinace; aktuální konfiguraci nelze jednoznačně určit jen podle názvu varianty.

**Nevhodně:** Převzít lokální rozměr nebo ukázkové chování jako univerzální pravidlo rodiny či značky.

### Web — nastavení zákazníka

**Situace a cíl:** Uživatel upravuje krátkou skupinu kontaktních údajů.

**Volba a varianta:** Jde o konkrétní referenci, nikoli další obecný veřejný ovladač; provozní skladba musí mít určené části. V průchodu se uplatní `placement=left`, `behavior=modal`.

**Průchod a výsledek:** Při návrhu oblasti „Upravit kontakt“ posuďte referenci „Kontaktní e-mail“. Používá fyzické left/right, velikosti a modal/modeless původního Dialog API. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

**Výjimka a návrat:** Odlišná šířka, lokální override nebo staré pojmenování se nepřenáší automaticky. Sada má duplicitní kombinace; aktuální konfiguraci nelze jednoznačně určit jen podle názvu varianty.

**Nevhodně:** Převzít lokální rozměr nebo ukázkové chování jako univerzální pravidlo rodiny či značky.

### Interní systém — rozhodnutí o požadavku

**Situace a cíl:** Vedoucí rozhoduje o konkrétním požadavku.

**Volba a varianta:** Jde o konkrétní referenci, nikoli další obecný veřejný ovladač; provozní skladba musí mít určené části. V průchodu se uplatní `placement=left`, `behavior=modal`.

**Průchod a výsledek:** Při návrhu oblasti „Vrátit k doplnění“ posuďte referenci „Požadavek P-58“. Používá fyzické left/right, velikosti a modal/modeless původního Dialog API. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

**Výjimka a návrat:** Odlišná šířka, lokální override nebo staré pojmenování se nepřenáší automaticky. Sada má duplicitní kombinace; aktuální konfiguraci nelze jednoznačně určit jen podle názvu varianty.

**Nevhodně:** Převzít lokální rozměr nebo ukázkové chování jako univerzální pravidlo rodiny či značky.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit tón rozhodovacích textů, prioritu akcí a vzhled modalit a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí důsledky potvrzení, zacházení s rozepsanými daty a bezpečný návrat. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-29341)
