# Token Icon/token-icon-pagination-ellipsis

Glyph `token-icon-pagination-ellipsis` představuje vynechané stránky v odpovídajícím slotu hostitele. Samotný symbol neprovádí akci.

**Vazba:** Pagination. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Glyph `token-icon-pagination-ellipsis` představuje vynechané stránky v odpovídajícím slotu hostitele. Samotný symbol neprovádí akci. Použijte ji pouze ve slotu se stejným významem; název ovladače nebo související text tento význam zpřístupní.

## Kdy zvolit alternativu

Když má funkce jiný význam než tato kresba, použijte odpovídající glyph. U neobvyklého nebo závažného příkazu zvolte textové Button či Link; samotný symbol nesmí nahrazovat jeho vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **Pagination**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Samostatnou osu error/default tento glyph nemá. Výsledek operace i význam případné změny barvy řídí skutečný hostitel; nevytvářejte neexistující varianty samotné kresby.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Vizuálně doplnit význam popsaný v definici této ikony a jeho správný stav.

### Co vyvolávat nemá

- Nepřidat samostatnou aktivaci jen kresbě a neoznámit jiný stav než její textový hostitel.

### Přechody a odpovědnost

Kresbu dosazuje skutečný hostitel podle podmínky popsané níže. Změna glyphu sama nepotvrzuje výběr ani výsledek požadavku. Je-li symbol v ovladači, aktivaci, případné čekání, odmítnutí a návrat řeší tento ovladač; glyph nevytváří další fokus ani vlastní uloženou hodnotu.

### Konkrétní pravidla použití

- Vkládejte do slotu, jehož význam odpovídá symbolu.
- Pokud symbol tvoří samostatný ovladač, název akce poskytuje tento ovladač; technický název tokenu není uživatelský popisek.

## Obsah a pojmenování

Technický název tohoto glyphu není text pro uživatele. Pokud je použit v samostatném ovladači, jeho název pojmenuje konkrétní výsledek a případně objekt zásahu. Dekorativní kresba neopakuje zbytečně stejné sdělení vedle již pojmenovaného obsahu.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

- **Společné výjimky a návrat:** Po změně počtu výsledků opravte rozsah i výpustky. Bez doloženého hostitele neslibujte jejich aktivací nabídku skrytých stránek.

- **Nevhodné použití:** Považovat výpustku za označení načítání nebo počtu vybraných záznamů.

### ERP — přehled objednávek

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „1 … 4 5 6 … 12“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Průchod a výsledek:** V posloupnosti „1 … 4 5 6 … 12“ označte vynechané stránky. Čísla dostupných stránek a předchozí/další ovladač zůstávají pojmenované; samotná výpustka není neurčená stránka.

### Web — katalog článků

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „1 … 3 4 5 … 8“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Průchod a výsledek:** V posloupnosti „1 … 3 4 5 … 8“ označte vynechané stránky. Čísla dostupných stránek a předchozí/další ovladač zůstávají pojmenované; samotná výpustka není neurčená stránka.

### Interní systém — správa uživatelů

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „1 … 6 7 8 … 20“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Průchod a výsledek:** V posloupnosti „1 … 6 7 8 … 20“ označte vynechané stránky. Čísla dostupných stránek a předchozí/další ovladač zůstávají pojmenované; samotná výpustka není neurčená stránka.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit schválenou ikonografii, optické velikosti a sémantické barvy symbolů, v návaznosti na vzhled stránkování a pojmenování navigačních ovladačů a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí velikost stránky, celkový počet výsledků a vazbu na filtry a řazení. Při doplnění pravidel značky zkontrolujte zejména vazbu symbolu na název hostitele a zachování jeho skutečného významu. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-22735)
