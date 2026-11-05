# Sidebar.Desktop

Desktopový boční rám organizuje navigaci a podporuje stanovený režim sbalení; hlavní obsah s ním musí sdílet dostupný prostor.

Cílem je orientovat se v aplikačním rámci na desktopu i mobilu a dosáhnout stejné navigace.

## Kdy použít

Pro desktopový aplikační rám s trvale dosažitelnou navigací a hlavním pracovním obsahem. Zvolte skutečný režim icon, offcanvas nebo none; poslední se nesbaluje. Dočasnou navigaci na úzké ploše řeší Sidebar.Mobile. Konkrétní bod přepnutí určí projekt, ne samotná šířka masteru.

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
| `collapsible=icon` | Při sbalení zůstává ikonová navigace s dostupnými názvy a odpovídajícím tooltipem. |
| `collapsible=offcanvas` | Sbalením se panel skryje mimo plochu; zůstane dosažitelný ovladač návratu. |
| `collapsible=none` | Rám zůstává rozbalený; neslibovat sbalení a nepřidávat k němu samostatný rail. |
| `expanded=true` | Pro rozbalený rám nebo obsah. |
| `expanded=false` | Pro sbalený povolený režim; u Sidebar collapsible=none nepředstírat sbalení. |

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

- Icon, offcanvas a none mají odlišný režim sbalení. None zůstává rozbalené.
- Ve sbaleném režimu zachovejte dostupné názvy cílů a tooltip odpovídající labelu.
- Navigační cíl, aktivní stránka a otevřená větev se nesmějí zaměňovat.
- Se sticky záhlavím zohledněte zbývající výšku.
- NavigationItem má v aktuálním masteru překryté popisky; zachovejte jediný čitelný název.
- Režim none nezobrazuje rail; nabízet neúčinný ovladač sbalení by bylo zavádějící.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nezaměňovat sbalení s odhlášením nebo změnou stránky.

### ERP — víceagendová aplikace

**Situace a cíl:** Pracovník prochází nákup, sklad a související přehledy.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Objednávky“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `side=start`, `collapsible=icon`, `expanded=true`.

**Průchod a výsledek:** Pro objekt „Agenda Nákup / Objednávky“ použijte pojmenování „Objednávky“. Rozbalení větve nebo rámu nemění samo stránku. Aktuální cíl označte podle skutečně zobrazeného obsahu; jména zůstanou dostupná i při sbalení. Na mobilu použijte určený navigační panel a po jeho zavření zachovejte hlavní pracovní kontext.

**Výjimka a návrat:** Icon zachová dostupné názvy, zatímco none zůstává rozbalené bez předstíraného railu.

### Web — zákaznický účet na desktopu

**Situace a cíl:** Zákazník na větší obrazovce potřebuje dosáhnout navigace svého účtu i při sbaleném bočním rámci.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Moje objednávky“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `side=start`, `collapsible=icon`, `expanded=true`.

**Průchod a výsledek:** Pro objekt „Navigace zákaznického účtu“ použijte pojmenování „Moje objednávky“. Rozbalení větve nebo rámu nemění samo stránku. Aktuální cíl označte podle skutečně zobrazeného obsahu; jména zůstanou dostupná i při sbalení. Na mobilu použijte určený navigační panel a po jeho zavření zachovejte hlavní pracovní kontext.

**Výjimka a návrat:** Dlouhý seznam nesmí zablokovat zavření nebo přístup k poslednímu cíli.

### Interní systém — projektový nástroj

**Situace a cíl:** Člen týmu přechází mezi pracovním seznamem a detaily projektu.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Projekt Orion“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `side=start`, `collapsible=icon`, `expanded=true`.

**Průchod a výsledek:** Pro objekt „Přehled / Úkoly / Dokumenty“ použijte pojmenování „Projekt Orion“. Rozbalení větve nebo rámu nemění samo stránku. Aktuální cíl označte podle skutečně zobrazeného obsahu; jména zůstanou dostupná i při sbalení. Na mobilu použijte určený navigační panel a po jeho zavření zachovejte hlavní pracovní kontext.

**Výjimka a návrat:** Sticky záhlaví nesmí způsobit přesah důležité spodní části mimo dostupnou výšku.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit šířkovou a vizuální hierarchii rámu, názvy cílů a pravidla zobrazení identity značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí nabídku agend, oprávnění, zvolený režim a zachování kontextu při změně zařízení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3100-5255)
