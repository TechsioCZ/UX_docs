# AvailabilityStatus / Glyph / unavailable

Glyph dostupnosti `unavailable` vizuálně doplňuje stejnojmenný stav AvailabilityStatus; skutečnou dostupnost dodává aplikace.

**Vazba:** AvailabilityStatus. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Glyph dostupnosti `unavailable` vizuálně doplňuje stejnojmenný stav AvailabilityStatus; skutečnou dostupnost dodává aplikace. Použijte ji pouze ve slotu se stejným významem; název ovladače nebo související text tento význam zpřístupní.

## Kdy zvolit alternativu

Když má funkce jiný význam než tato kresba, použijte odpovídající glyph. U neobvyklého nebo závažného příkazu zvolte textové Button či Link; samotný symbol nesmí nahrazovat jeho vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **AvailabilityStatus**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Samostatnou osu error/default tento glyph nemá. Výsledek operace i význam případné změny barvy řídí skutečný hostitel; nevytvářejte neexistující varianty samotné kresby.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Doplnit textový stav unavailable jen ve shodě s aktuálními daty.

### Co vyvolávat nemá

- Nepotvrdit nákup, termín dodání ani jiný skladový stav pouhou kresbou.

### Přechody a odpovědnost

Kresbu dosazuje skutečný hostitel podle podmínky popsané níže. Změna glyphu sama nepotvrzuje výběr ani výsledek požadavku. Je-li symbol v ovladači, aktivaci, případné čekání, odmítnutí a návrat řeší tento ovladač; glyph nevytváří další fokus ani vlastní uloženou hodnotu.

### Konkrétní pravidla použití

- Symbol, label a skutečný stav dostupnosti musí souhlasit.
- Samotný glyph neurčuje skladová data ani oprávnění koupit.

## Obsah a pojmenování

Technický název tohoto glyphu není text pro uživatele. Pokud je použit v samostatném ovladači, jeho název pojmenuje konkrétní výsledek a případně objekt zásahu. Dekorativní kresba neopakuje zbytečně stejné sdělení vedle již pojmenovaného obsahu.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

- **Společné výjimky a návrat:** Během zjišťování použijte čekání hostitele, nikoli náhodný obchodní status. Ani potvrzená dostupnost sama negarantuje přesný den dodání.

- **Pravidlo použití:** Nepotvrdit nákup, termín dodání ani jiný skladový stav pouhou kresbou.

### ERP — nákup materiálu

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Těsnění T-40“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Průchod a výsledek:** U nabídky „Těsnění T-40“ zobrazte symbol pouze pro daty doložený stav unavailable spolu s textem „Nedostupné“. Jiná dostupnost vyžaduje odpovídající jiný symbol i text. Případné objednání provádí samostatná akce.

### Web — produktový detail

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Vrtačka V18, varianta s kufrem“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Průchod a výsledek:** U nabídky „Vrtačka V18, varianta s kufrem“ zobrazte symbol pouze pro daty doložený stav unavailable spolu s textem „Nedostupné“. Jiná dostupnost vyžaduje odpovídající jiný symbol i text. Případné objednání provádí samostatná akce.

### Interní systém — objednávání vybavení

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Monitor M27“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Průchod a výsledek:** U nabídky „Monitor M27“ zobrazte symbol pouze pro daty doložený stav unavailable spolu s textem „Nedostupné“. Jiná dostupnost vyžaduje odpovídající jiný symbol i text. Případné objednání provádí samostatná akce.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit schválenou ikonografii, optické velikosti a sémantické barvy symbolů, v návaznosti na slovník dostupnosti a význam vizuálních stavů nabídky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj skladových dat, jejich platnost, termíny a pravidla objednatelnosti. Při doplnění pravidel značky zkontrolujte zejména vazbu symbolu na název hostitele a zachování jeho skutečného významu. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3839-22)
