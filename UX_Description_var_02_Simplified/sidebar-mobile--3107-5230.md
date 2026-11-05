# Sidebar.Mobile

Mobilní boční rám zpřístupňuje navigaci v dočasném panelu Drawer; otevření a návrat musí zachovat kontext uživatele.

Cílem je orientovat se v aplikačním rámci na desktopu i mobilu a dosáhnout stejné navigace.

## Kdy použít

Pro dočasnou navigaci na úzké ploše, kde má hlavní pracovní obsah dostat vlastní prostor. Open řídí otevření panelu; nejde o desktopové expanded nebo ikonový rail. Pro trvalý desktopový rám použijte Sidebar.Desktop. Konkrétní bod přepnutí určí projekt.

## Kdy zvolit alternativu

Pro samotný navigační seznam použijte VerticalNavigation, pro dočasný kontextový obsah Drawer.

## Anatomie, stavy a varianty

Desktop a Mobile skladba rámu s navigací, záhlavím, obsahem a případnou patičkou. Trigger a Rail se vztahují ke skutečnému collapsible režimu; Pane a Inset řeší vztah k hlavnímu obsahu.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `side=start` | Polohu start volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `side=end` | Polohu end volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `dir=ltr` | Pro levopravý jazyk a odpovídající logické směry. |
| `dir=rtl` | Pro pravolevý jazyk; obrátit logické uspořádání a odpovídající směrové značky, ne význam akcí. |
| `open=true` | Když je panel či větev skutečně otevřená. |
| `open=false` | Když je uzavřená; při zavření zůstává logická návaznost na spouštěč. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít navigační cíl a podle režimu rozbalit, sbalit či zavřít rám.
- V mobilní podobě nabídnout odpovídající dočasný Drawer.

### Co vyvolávat nemá

- Nezaměňovat sbalení s odhlášením nebo změnou stránky.
- Nepovažovat none za další typ sbaleného railu.

### Přechody a odpovědnost

Aktivace konkrétního odkazu otevře jeho pojmenovaný cíl; teprve skutečně zobrazená stránka určuje current. Otevření navigační větve nebo rámu není přechod na stránku. Zrušení panelu ponechá původní pracovní kontext a vyřeší návrat fokusu. Nedostupný cíl aplikace vysvětlí a nabídne návrat; navigace nesmí skrytě měnit obchodní data ani zahodit neuložený draft bez určeného postupu.

### Konkrétní pravidla použití

- Mobilní skladba používá Drawer.
- Otevření, zavření a návrat zachovávají kontext hlavního obsahu.
- Navigační položky mají stejné názvy a cíle jako odpovídající navigace aplikace.
- Dlouhý seznam nesmí znemožnit přístup k poslední položce nebo zavření.
- U modálního mobilního panelu udržte fokus uvnitř, po zavření jej vraťte ke spouštěči nebo navazujícímu cíli.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nezaměňovat sbalení s odhlášením nebo změnou stránky.

### ERP — víceagendová aplikace

**Situace a cíl:** Na úzké obrazovce uživatel otevře dočasnou navigaci pro oblast „Objednávky“ a po výběru či zavření pokračuje v hlavním obsahu.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Objednávky“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `side=start`, `open=true`.

**Průchod a výsledek:** Pro objekt „Agenda Nákup / Objednávky“ použijte pojmenování „Objednávky“. Rozbalení větve nebo rámu nemění samo stránku. Aktuální cíl označte podle skutečně zobrazeného obsahu; jména zůstanou dostupná i při sbalení. Na mobilu použijte určený navigační panel a po jeho zavření zachovejte hlavní pracovní kontext.

**Výjimka a návrat:** Icon zachová dostupné názvy, zatímco none zůstává rozbalené bez předstíraného railu.

### Web — zákaznický portál

**Situace a cíl:** Na úzké obrazovce uživatel otevře dočasnou navigaci pro oblast „Moje objednávky“ a po výběru či zavření pokračuje v hlavním obsahu.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Moje objednávky“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `side=start`, `open=true`.

**Průchod a výsledek:** Pro objekt „Navigace zákaznického účtu“ použijte pojmenování „Moje objednávky“. Rozbalení větve nebo rámu nemění samo stránku. Aktuální cíl označte podle skutečně zobrazeného obsahu; jména zůstanou dostupná i při sbalení. Na mobilu použijte určený navigační panel a po jeho zavření zachovejte hlavní pracovní kontext.

**Výjimka a návrat:** Dlouhý seznam nesmí zablokovat zavření nebo přístup k poslednímu cíli.

### Interní systém — projektový nástroj

**Situace a cíl:** Na úzké obrazovce uživatel otevře dočasnou navigaci pro oblast „Projekt Orion“ a po výběru či zavření pokračuje v hlavním obsahu.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Projekt Orion“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `side=start`, `open=true`.

**Průchod a výsledek:** Pro objekt „Přehled / Úkoly / Dokumenty“ použijte pojmenování „Projekt Orion“. Rozbalení větve nebo rámu nemění samo stránku. Aktuální cíl označte podle skutečně zobrazeného obsahu; jména zůstanou dostupná i při sbalení. Na mobilu použijte určený navigační panel a po jeho zavření zachovejte hlavní pracovní kontext.

**Výjimka a návrat:** Sticky záhlaví nesmí způsobit přesah důležité spodní části mimo dostupnou výšku.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit šířkovou a vizuální hierarchii rámu, názvy cílů a pravidla zobrazení identity značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí nabídku agend, oprávnění, zvolený režim a zachování kontextu při změně zařízení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3107-5230)
