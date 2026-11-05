# QuantityField

Pole množství spojuje číselný draft s jednotkou a informací o aktualizaci.

Cílem je změnit požadované množství položky, rozpoznat jednotku a zjistit výsledek aktualizace.

## Kdy použít

Pro úpravu množství konkrétní položky v její jednotce. Musí být určené meze, krok a okamžik potvrzení či přepočtu. Prostý číselný údaj bez položkového průchodu patří do NumericInput.

## Kdy zvolit alternativu

Pro obecné číslo použijte FormNumericInput.

## Anatomie, stavy a varianty

Pojmenované množství, jednotka a krokové ovladače se zpětnou vazbou aktualizace. HideLabel může skrýt viditelný název, nikoli odstranit jeho přístupnou vazbu.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=error` | Když je odmítnuté množství nebo selže jeho aktualizace. Vysvětlit skutečnou příčinu a zachovat návrh k opravě; nejde samo o stav skladu. |
| `state=pending` | Během skutečně probíhajícího načítání nebo aktualizace. Zobrazený návrh není sám potvrzeným výsledkem. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=readonly` | Když má být existující hodnota čitelná, ale není dovoleno ji měnit. Nezaměňovat za disabled ani za prázdnou hodnotu. |
| `hideLabel=false` | Pro běžnou viditelně pojmenovanou hodnotu množství. |
| `hideLabel=true` | Pouze pokud význam objasní okolní kontext a pole má stále přístupný název. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zadat množství přímo nebo jej měnit krokovými ovladači.
- Při potvrzení jasně odlišit draft, probíhající změnu a uloženou hodnotu.

### Co vyvolávat nemá

- Nepovažovat skladovou nedostupnost za stejnou chybu jako neúspěšné uložení množství.
- Nenechat starší odpověď přepsat novější záměr.

### Přechody a odpovědnost

Z potvrzeného množství vznikne draft; po určeném potvrzení a platné kontrole začne pending. Úspěch sjednotí množství i související přepočet se skutečným výsledkem; error ponechá návrh a důvod odmítnutí. Zrušení před odesláním vrátí potvrzené množství. Aplikace sváže odpověď s položkou a požadavkem, aby starší odpověď nepřepsala novější záměr.

### Konkrétní pravidla použití

- Jednotka odpovídá skutečnému balení.
- Zachovejte editovatelný prázdný i odmítnutý draft. Neopravujte jej tiše na minimum.
- Meze omezují příslušné krokové ovladače.
- Validaci a uložení řídí aplikace; pending a chyba se týkají aktualizace množství, nikoli skladové dostupnosti.
- Při hideLabel zachovejte přístupný název pole. U souběžných aktualizací nesmí starší odpověď přepsat novější zamýšlené množství.

## Obsah a pojmenování

Názvy údajů, částky nebo množství vztahujte ke stejné položce a jednotce. Měna či balení nezmizí při zkrácení. Ukázkové číslo z příkladu není výchozí hodnota ani limit projektu; jeho zdroj a přesnost určuje aplikace.

## Přístupnost a prostředí

Pole má stálý přístupný název, viditelný význam a propojené instrukce i konkrétní chybu. Zachovejte rozepsané hodnoty při odmítnutí. Klávesnicové ovládání a čtení nesmí záviset jen na hoveru; delší text či jednotka nepřekrývají ovladače.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nepovažovat skladovou nedostupnost za stejnou chybu jako neúspěšné uložení množství.

### ERP — nákupní požadavek

**Situace a cíl:** Pracovník opravuje množství materiálu na konkrétním řádku.

**Volba a varianta:** Množství „3 balení“ patří konkrétní položce a jejímu přepočtu; prosté NumericInput samo nevyřeší položkovou aktualizaci. V průchodu se uplatní `state=default`, `hideLabel=false`.

**Průchod a výsledek:** Pro objekt „3 balení“ použijte pojmenování „Počet balení“. Při úpravě zůstává návrh editovatelný. Po zahájení aktualizace se pending vztahuje na množství tohoto řádku. Při úspěchu se zobrazení sjednotí s poslední potvrzenou hodnotou; error ponechá návrh a konkrétní příčinu. Odpověď na starší požadavek nesmí přepsat novější záměr.

**Výjimka a návrat:** Při odmítnutí meze zůstane návrh čitelný a pole vysvětlí povolený rozsah.

### Web — košík

**Situace a cíl:** Zákazník mění počet kusů vloženého produktu.

**Volba a varianta:** Množství „2 kusy“ patří konkrétní položce a jejímu přepočtu; prosté NumericInput samo nevyřeší položkovou aktualizaci. V průchodu se uplatní `state=default`, `hideLabel=false`.

**Průchod a výsledek:** Pro objekt „2 kusy“ použijte pojmenování „Množství“. Při úpravě zůstává návrh editovatelný. Po zahájení aktualizace se pending vztahuje na množství tohoto řádku. Při úspěchu se zobrazení sjednotí s poslední potvrzenou hodnotou; error ponechá návrh a konkrétní příčinu. Odpověď na starší požadavek nesmí přepsat novější záměr.

**Výjimka a návrat:** Nula nesmí bez předem jasného modelu potichu znamenat nevratné odstranění položky.

### Interní systém — objednávání spotřebního materiálu

**Situace a cíl:** Zaměstnanec objednává materiál prodávaný v dlouze pojmenované jednotce.

**Volba a varianta:** Množství „2 sady po 10 kusech“ patří konkrétní položce a jejímu přepočtu; prosté NumericInput samo nevyřeší položkovou aktualizaci. V průchodu se uplatní `state=default`, `hideLabel=false`.

**Průchod a výsledek:** Pro objekt „2 sady po 10 kusech“ použijte pojmenování „Počet sad“. Při úpravě zůstává návrh editovatelný. Po zahájení aktualizace se pending vztahuje na množství tohoto řádku. Při úspěchu se zobrazení sjednotí s poslední potvrzenou hodnotou; error ponechá návrh a konkrétní příčinu. Odpověď na starší požadavek nesmí přepsat novější záměr.

**Výjimka a návrat:** Souběžné rychlé změny nezpůsobí návrat na hodnotu starší síťové odpovědi.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit zápis jednotek, popisky množství a styl zpráv o aktualizaci a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí meze, krok, dostupné balení, okamžik přepočtu a rozhodnutí o nulovém množství. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3861-1334)
