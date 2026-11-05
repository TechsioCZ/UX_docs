# AvailabilityStatus

Informace o dostupnosti vysvětluje stav produktu a případné podmínky získání.

Cílem je rozpoznat aktuálně doloženou dostupnost konkrétního produktu a její omezení.

## Kdy použít

Pro sdělení dostupnosti jedné přesně určené nabídky podle aktuálních dat. Odlište neznámou informaci, čekání, nedostupnost a předobjednávku. Samotný stav neurčuje právo nakoupit ani termín dodání.

## Kdy zvolit alternativu

Pro obecnou zprávu pole použijte StatusText.

## Anatomie, stavy a varianty

Stav, label a doplňující detail téže nabídky. Glyph doplňuje text; při pending je běžný obsah nahrazen zástupnou linkou a pendingLabel poskytuje textovou informaci čtečkám.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `status=available` | Pro dostupnost potvrzenou aktuálním zdrojem aplikace; neznamená automaticky konkrétní termín dodání. |
| `status=limited` | Pro skutečně omezenou dostupnost s odpovídajícím vysvětlením; nevymýšlet počet kusů z barvy. |
| `status=preorder` | Pro nabídku v režimu předobjednávky s vysvětlenými podmínkami; neprezentovat jako okamžitou dostupnost. |
| `status=unavailable` | Pro potvrzenou nedostupnost nabídky. Neznamená neznámou informaci ani automatický zákaz všech souvisejících akcí. |
| `status=unknown` | Když dostupnost není potvrzená. Nezaměňovat za unavailable ani za pending. |
| `status=pending` | Během skutečně probíhajícího načítání nebo aktualizace. Zobrazený návrh není sám potvrzeným výsledkem. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Prezentovat údaj dodaný aplikací s vysvětlením jeho významu.
- Při čekání odlišit načítání od neznámého či nedostupného zboží.

### Co vyvolávat nemá

- Samotný stav nepovoluje nákup ani neslibuje datum dodání.
- Unknown se nesmí převést na unavailable a pending na available.

### Přechody a odpovědnost

Informace se mění podle skutečného údaje nebo stavu svého zdroje. Čtení, barva či hover neprovádí příkaz. Aplikace rozliší dosud neznámou hodnotu, známý výsledek a případnou chybu; použije jen odpovídající doložené varianty této komponenty. Obnovení dat aktualizuje text i vizuální význam společně; případnou nápravu nebo další krok poskytne samostatný pojmenovaný ovladač.

### Konkrétní pravidla použití

- Stav, label a detail dodává aplikace.
- Rozlišujte available, limited, preorder, unavailable, unknown a pending. Neznámá dostupnost není potvrzená nedostupnost.
- Pending skrývá běžný label a detail; `pendingLabel` je text pro čtečky, nikoli viditelný popisek.
- Dostupnost sama neurčuje oprávnění koupit ani vypočtený termín doručení.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Informace je srozumitelná bez samotné barvy či symbolu a bez přidávání zbytečné zastávky fokusu. Důležitá změna výsledku nesmí být dostupná pouze jako krátké vizuální probliknutí. Text, měna, jednotka či zkratka odpovídají konkrétnímu prostředí a jazyku.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Nevhodné použití:** Samotný stav nepovoluje nákup ani neslibuje datum dodání.

### ERP — nákup materiálu

**Situace a cíl:** Nákupčí porovnává dostupnost položky před vytvořením požadavku.

**Volba a varianta:** Pro „Dostupnost materiálu“ se sděluje potvrzená či výslovně neznámá dostupnost, nikoli příslib nákupu. V průchodu se uplatní `status=limited`.

**Průchod a výsledek:** Pro objekt „Těsnění T-40“ použijte pojmenování „Dostupnost materiálu“. Ukázkový status=limited zobrazte pouze při odpovídajících datech. Pro skutečně omezenou dostupnost s odpovídajícím vysvětlením; nevymýšlet počet kusů z barvy. Při čekání přejděte na pending, nikoli na jiný obchodní stav. Nákup nebo přidělení zařízení je samostatná operace.

**Výjimka a návrat:** Při nedostupné službě se nezobrazí Skladem jen podle dřívější barvy komponenty.

### Web — produktový detail

**Situace a cíl:** Zákazník rozhoduje mezi dostupnou a předobjednávanou variantou.

**Volba a varianta:** Pro „Dostupnost vybrané varianty“ se sděluje potvrzená či výslovně neznámá dostupnost, nikoli příslib nákupu. V průchodu se uplatní `status=preorder`.

**Průchod a výsledek:** Pro objekt „Vrtačka V18, varianta s kufrem“ použijte pojmenování „Dostupnost vybrané varianty“. Ukázkový status=preorder zobrazte pouze při odpovídajících datech. Pro nabídku v režimu předobjednávky s vysvětlenými podmínkami; neprezentovat jako okamžitou dostupnost. Při čekání přejděte na pending, nikoli na jiný obchodní stav. Nákup nebo přidělení zařízení je samostatná operace.

**Výjimka a návrat:** Samotné Skladem neslibuje doručení zítra, pokud takový termín produkt nepotvrdil.

### Interní systém — objednávání vybavení

**Situace a cíl:** Zaměstnanec zjišťuje možnost získat konkrétní zařízení.

**Volba a varianta:** Pro „Dostupnost vybavení“ se sděluje potvrzená či výslovně neznámá dostupnost, nikoli příslib nákupu. V průchodu se uplatní `status=unknown`.

**Průchod a výsledek:** Pro objekt „Monitor M27“ použijte pojmenování „Dostupnost vybavení“. Ukázkový status=unknown zobrazte pouze při odpovídajících datech. Když dostupnost není potvrzená. Nezaměňovat za unavailable ani za pending. Při čekání přejděte na pending, nikoli na jiný obchodní stav. Nákup nebo přidělení zařízení je samostatná operace.

**Výjimka a návrat:** Při pending zůstává zpětná vazba dostupná čtečkám prostřednictvím pendingLabel.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník dostupnosti a význam vizuálních stavů nabídky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj skladových dat, jejich platnost, termíny a pravidla objednatelnosti. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3839-105)
