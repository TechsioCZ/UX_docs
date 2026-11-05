# PriceBlock

Cenový blok zpřístupňuje dodanou cenu, její podmínky a případnou původní cenu.

Cílem je rozpoznat cenu jedné nabídky včetně jejího rozsahu nebo důvodu, proč ještě není známá.

## Kdy použít

Pro cenu jedné nabídky včetně měny, jednotky a rozsahu platnosti. Cena od, sleva, cena na dotaz a čekání mají odlišný význam. Samotná cena není tlačítkem k nákupu.

## Kdy zvolit alternativu

Pro rozpis a celkovou částku použijte TotalsSummary.

## Anatomie, stavy a varianty

Aktuální částka s měnou a jednotkou; podle state také význam ceny od, původní cena nebo cena na dotaz. OriginalSrLabel a pendingLabel doplňují informace čtečkám.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=known` | Pro konkrétní známou cenu aktuální nabídky s odpovídající měnou a jednotkou. |
| `state=from` | Když částka představuje spodní cenu nabízeného rozsahu, nikoli pevnou cenu všech konfigurací. |
| `state=discounted` | Pro doloženou novou a původní cenu stejné nabídky. Obě částky musí být významově odlišitelné. |
| `state=on-request` | Když cena vyžaduje navazující poptávku. Nejde o nulovou cenu. |
| `state=pending` | Během skutečně probíhajícího načítání nebo aktualizace. Zobrazený návrh není sám potvrzeným výsledkem. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zobrazit cenu, cenu od, doloženou slevu, cenu na dotaz nebo čekání.
- Při změně nabídky aktualizovat částku, měnu a jednotku společně.

### Co vyvolávat nemá

- Neodvozovat cenu z dostupnosti ani prezentovat neznámou cenu jako nulu.
- Samotné zobrazení ceny nevytváří nákupní operaci.

### Přechody a odpovědnost

Informace se mění podle skutečného údaje nebo stavu svého zdroje. Čtení, barva či hover neprovádí příkaz. Aplikace rozliší dosud neznámou hodnotu, známý výsledek a případnou chybu; použije jen odpovídající doložené varianty této komponenty. Obnovení dat aktualizuje text i vizuální význam společně; případnou nápravu nebo další krok poskytne samostatný pojmenovaný ovladač.

### Konkrétní pravidla použití

- Odlište pevnou cenu, cenu od, slevu, cenu na dotaz a čekání na cenu.
- Měnu, jednotku a daňový údaj uveďte jednoznačně.
- Původní a zlevněná cena musí patřit stejné nabídce.
- Částky, výpočty a formátované texty dodává aplikace. Pending není nulová cena.
- Po skrytí údaje nesmí zůstat osamocený oddělovač.
- Původní cenu při slevě pojmenujte pomocí originalSrLabel a čekání pomocí pendingLabel; oba texty patří čtečkám, nikoli nové viditelné vrstvě.

## Obsah a pojmenování

Názvy údajů, částky nebo množství vztahujte ke stejné položce a jednotce. Měna či balení nezmizí při zkrácení. Ukázkové číslo z příkladu není výchozí hodnota ani limit projektu; jeho zdroj a přesnost určuje aplikace.

## Přístupnost a prostředí

Informace je srozumitelná bez samotné barvy či symbolu a bez přidávání zbytečné zastávky fokusu. Důležitá změna výsledku nesmí být dostupná pouze jako krátké vizuální probliknutí. Text, měna, jednotka či zkratka odpovídají konkrétnímu prostředí a jazyku.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Neodvozovat cenu z dostupnosti ani prezentovat neznámou cenu jako nulu.

### ERP — nákupní katalog

**Situace a cíl:** Nákupčí porovnává cenu konkrétního balení materiálu.

**Volba a varianta:** Pro „Cena balení“ se sděluje cena téže nabídky včetně jednotky, nikoli její dostupnost. V průchodu se uplatní `state=known`.

**Průchod a výsledek:** Pro objekt „1 250 Kč za balení“ použijte pojmenování „Cena balení“. Pro tento příklad zvolte state=known. Zobrazte skutečnou částku s jednotkou. Pending použijte jen po dobu získávání ceny a výsledek neslibujte změnou dostupnosti produktu.

**Výjimka a návrat:** Cena od se nezobrazuje jako pevná cena každé možné konfigurace.

### Web — produktový detail

**Situace a cíl:** Zákazník vybírá mezi běžnou a zlevněnou nabídkou.

**Volba a varianta:** Pro „Cena vybrané varianty“ se sděluje cena téže nabídky včetně jednotky, nikoli její dostupnost. V průchodu se uplatní `state=discounted`.

**Průchod a výsledek:** Pro objekt „1 490 Kč, původně 1 790 Kč“ použijte pojmenování „Cena vybrané varianty“. Pro tento příklad zvolte state=discounted. Novou i původní částku odlište a původní cenu pojmenujte také originalSrLabel. Pending použijte jen po dobu získávání ceny a výsledek neslibujte změnou dostupnosti produktu.

**Výjimka a návrat:** Při pending se nepřepne nabídka na zdarma a popis čekání je dostupný čtečkám.

### Interní systém — objednávání služeb

**Situace a cíl:** Pracovník vybírá službu oceňovanou individuálně.

**Volba a varianta:** Pro „Cena služby“ se sděluje cena téže nabídky včetně jednotky, nikoli její dostupnost. V průchodu se uplatní `state=on-request`.

**Průchod a výsledek:** Pro objekt „Cena na dotaz“ použijte pojmenování „Cena služby“. Pro tento příklad zvolte state=on-request. Text Cena na dotaz předá uživatele k samostatně pojmenované poptávkové akci; částka není nula. Pending použijte jen po dobu získávání ceny a výsledek neslibujte změnou dostupnosti produktu.

**Výjimka a návrat:** OriginalSrLabel ani pendingLabel nejsou další viditelné cenové řádky.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit zápis měny a jednotek, hierarchii původní a nové ceny a pojmenování ceny na dotaz a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí cenová data, rozsah nabídky, platnost slevy a dokončení přepočtu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3838-68)
