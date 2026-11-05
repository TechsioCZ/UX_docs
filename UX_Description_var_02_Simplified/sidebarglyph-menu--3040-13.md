# .SidebarGlyph/menu

Interní glyph Sidebar `menu` vizuálně představuje nabídku navigace; skutečný název a cílovou stránku určuje hostitelská položka.

**Vazba:** Sidebar. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Interní glyph Sidebar `menu` vizuálně představuje nabídku navigace; skutečný název a cílovou stránku určuje hostitelská položka. Použijte ji pouze ve slotu se stejným významem; název ovladače nebo související text tento význam zpřístupní.

## Kdy zvolit alternativu

Když má funkce jiný význam než tato kresba, použijte odpovídající glyph. U neobvyklého nebo závažného příkazu zvolte textové Button či Link; samotný symbol nesmí nahrazovat jeho vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **Sidebar**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Samostatnou osu error/default tento glyph nemá. Výsledek operace i význam případné změny barvy řídí skutečný hostitel; nevytvářejte neexistující varianty samotné kresby.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Doplnit pojmenovaný spouštěč otevření navigace.

### Co vyvolávat nemá

- Nepovažovat otevření rámu za změnu stránky nebo odhlášení.

### Přechody a odpovědnost

Kresbu dosazuje skutečný hostitel podle podmínky popsané níže. Změna glyphu sama nepotvrzuje výběr ani výsledek požadavku. Je-li symbol v ovladači, aktivaci, případné čekání, odmítnutí a návrat řeší tento ovladač; glyph nevytváří další fokus ani vlastní uloženou hodnotu.

### Konkrétní pravidla použití

- Používejte vedle odpovídajícího navigačního cíle.
- Ve sbalení musí název cíle zůstat dostupný; samotný symbol cílovou stránku neurčuje.

## Obsah a pojmenování

Technický název tohoto glyphu není text pro uživatele. Pokud je použit v samostatném ovladači, jeho název pojmenuje konkrétní výsledek a případně objekt zásahu. Dekorativní kresba neopakuje zbytečně stejné sdělení vedle již pojmenovaného obsahu.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společný cíl:** V tomto projektu se řeší význam nebo ovladač u „Otevřít navigaci“; je nutné odlišit samotnou kresbu od účinku hostitele.

- **Společná volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

- **Společné výjimky a návrat:** Při jiné informační architektuře zvolte jinou kresbu či název cíle. Disabled odkaz nesmí zůstat účinný pouhou vizuální úpravou.

- **Pravidlo použití:** Nepovažovat otevření rámu za změnu stránky nebo odhlášení.

### ERP — navigace nákupu

**Průchod a výsledek:** V navigaci pojmenujte hostitele „Otevřít navigaci“ pouze tehdy, když takový cíl nebo ovladač skutečně existuje. Ve sbaleném rámci poskytuje stejný název i tooltip; symbol se nevydává za vlastní odkaz. Otevření nabídky nemění právě zobrazenou stránku. V tomto příkladu jde o oblast navigace nákupu.

### Web — zákaznický účet

**Průchod a výsledek:** V navigaci pojmenujte hostitele „Otevřít navigaci“ pouze tehdy, když takový cíl nebo ovladač skutečně existuje. Ve sbaleném rámci poskytuje stejný název i tooltip; symbol se nevydává za vlastní odkaz. Otevření nabídky nemění právě zobrazenou stránku. V tomto příkladu jde o oblast zákaznický účet.

### Interní systém — pracovní portál

**Průchod a výsledek:** V navigaci pojmenujte hostitele „Otevřít navigaci“ pouze tehdy, když takový cíl nebo ovladač skutečně existuje. Ve sbaleném rámci poskytuje stejný název i tooltip; symbol se nevydává za vlastní odkaz. Otevření nabídky nemění právě zobrazenou stránku. V tomto příkladu jde o oblast pracovní portál.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit schválenou ikonografii, optické velikosti a sémantické barvy symbolů, v návaznosti na šířkovou a vizuální hierarchii rámu, názvy cílů a pravidla zobrazení identity značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí nabídku agend, oprávnění, zvolený režim a zachování kontextu při změně zařízení. Při doplnění pravidel značky zkontrolujte zejména vazbu symbolu na název hostitele a zachování jeho skutečného významu. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3040-13)
