# VerticalNavigation

Svislá navigace zpřístupňuje cílové stránky a jejich hierarchii.

Cílem je přejít na správnou stránku v hierarchii a rozpoznat současné místo.

## Kdy použít

Pro pojmenované cíle uspořádané do skupin nebo větví. Aktuální cesta odpovídá zobrazené stránce, nikoli poslednímu hoveru. Výběr datové položky v hierarchii řeší TreeView.

## Kdy zvolit alternativu

Pro výběr dat použijte TreeView nebo CascadeSelect; pro celý responzivní rám Sidebar.

## Anatomie, stavy a varianty

Group a GroupLabel sdružují Link nebo rozbalovací Branch s BranchContent; Separator odděluje přítomné skupiny. Current a currentPath označují různé vztahy ke stránce.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít pojmenovaný navigační cíl nebo rozbalit skupinu jeho potomků.
- Zobrazit current pro stránku a currentPath pro její předky.

### Co vyvolávat nemá

- Nezaměňovat otevření větve za změnu stránky.
- Nepoužívat navigační položku pro skrytou změnu či odstranění dat.

### Přechody a odpovědnost

Aktivace konkrétního odkazu otevře jeho pojmenovaný cíl; teprve skutečně zobrazená stránka určuje current. Otevření navigační větve nebo rámu není přechod na stránku. Zrušení panelu ponechá původní pracovní kontext a vyřeší návrat fokusu. Nedostupný cíl aplikace vysvětlí a nabídne návrat; navigace nesmí skrytě měnit obchodní data ani zahodit neuložený draft bez určeného postupu.

### Konkrétní pravidla použití

- Current označuje aktuální stránku, currentPath cestu k ní.
- Otevřená větev nemusí být aktuálním cílem.
- Názvy skupin nejsou automaticky odkazy.
- Odsazení pomáhá číst vztahy; hluboké zanoření nesmí připravit cíl o dostupný název.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

### ERP — navigace nákupní agendy

**Situace a cíl:** Pracovník chce z detailu objednávky přejít do přehledu dodavatelů.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Nákup / Dodavatelé“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `size=sm`.

**Průchod a výsledek:** Pro objekt „Stránka Dodavatelé“ použijte pojmenování „Nákup / Dodavatelé“. Rozbalení větve nebo rámu nemění samo stránku. Aktuální cíl označte podle skutečně zobrazeného obsahu; jména zůstanou dostupná i při sbalení. Na mobilu použijte určený navigační panel a po jeho zavření zachovejte hlavní pracovní kontext.

**Výjimka a návrat:** Rozbalení Nákup neoznačí automaticky jeho první podstránku za aktuální.

**Nevhodně:** Nezaměňovat otevření větve za změnu stránky.

### Web — zákaznický účet

**Situace a cíl:** Uživatel přechází mezi svými objednávkami a kontaktními údaji.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Můj účet / Objednávky“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `size=sm`.

**Průchod a výsledek:** Pro objekt „Moje objednávky“ použijte pojmenování „Můj účet / Objednávky“. Rozbalení větve nebo rámu nemění samo stránku. Aktuální cíl označte podle skutečně zobrazeného obsahu; jména zůstanou dostupná i při sbalení. Na mobilu použijte určený navigační panel a po jeho zavření zachovejte hlavní pracovní kontext.

**Výjimka a návrat:** Dlouhý název nebo úzká šířka nesmí znemožnit rozpoznání cíle.

**Nevhodně:** Nezaměňovat otevření větve za změnu stránky.

### Interní systém — projektový portál

**Situace a cíl:** Člen týmu prochází sekce projektu.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Projekt Orion / Dokumenty“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `size=sm`.

**Průchod a výsledek:** Pro objekt „Dokumenty projektu“ použijte pojmenování „Projekt Orion / Dokumenty“. Rozbalení větve nebo rámu nemění samo stránku. Aktuální cíl označte podle skutečně zobrazeného obsahu; jména zůstanou dostupná i při sbalení. Na mobilu použijte určený navigační panel a po jeho zavření zachovejte hlavní pracovní kontext.

**Výjimka a návrat:** CurrentPath neznamená schválení dokumentů a deaktivovaná položka nesmí vykonat navigaci.

**Nevhodně:** Nezaměňovat otevření větve za změnu stránky.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit informační architekturu značky, názvy sekcí a vizuální hierarchii current/currentPath a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí cílové adresy, viditelnost podle role a zachování práce při přechodu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3539-102)
