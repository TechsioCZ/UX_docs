# Token Icon/token-icon-select-indicator-open

Glyph `token-icon-select-indicator-open` představuje otevřenou nabídku Select v odpovídajícím slotu hostitele. Samotný symbol neprovádí akci.

**Vazba:** Select. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Glyph `token-icon-select-indicator-open` představuje otevřenou nabídku Select v odpovídajícím slotu hostitele. Samotný symbol neprovádí akci. Použijte ji pouze ve slotu se stejným významem; název ovladače nebo související text tento význam zpřístupní.

## Kdy zvolit alternativu

Když má funkce jiný význam než tato kresba, použijte odpovídající glyph. U neobvyklého nebo závažného příkazu zvolte textové Button či Link; samotný symbol nesmí nahrazovat jeho vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **Select**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Samostatnou osu error/default tento glyph nemá. Výsledek operace i význam případné změny barvy řídí skutečný hostitel; nevytvářejte neexistující varianty samotné kresby.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- V pojmenovaném hostiteli nabídnout: Doplnit skutečně otevřenou nabídku výběru.

### Co vyvolávat nemá

- Nevytvářet druhý nezávislý spouštěč bez názvu.

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

### ERP — zakázkový formulář

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Logistika“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** Do skutečného ovladače u „Logistika“ vložte glyph a název „Doplnit skutečně otevřenou nabídku výběru“. Až aktivace hostitele vyvolá tuto akci; čtení symbolu ani hover ne. Výsledek určuje skutečný ovladač a aplikace. Samotný glyph tuto operaci neprovádí.

**Výjimka a návrat:** Nevytvářet druhý nezávislý spouštěč bez názvu. Při odmítnutí nebo zrušení se nesmí zobrazit falešné potvrzení; výsledek i návrat řeší hostitel.

**Nevhodně:** Nevytvářet druhý nezávislý spouštěč bez názvu.

### Web — nastavení doručení

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Česko“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** Do skutečného ovladače u „Česko“ vložte glyph a název „Doplnit skutečně otevřenou nabídku výběru“. Až aktivace hostitele vyvolá tuto akci; čtení symbolu ani hover ne. Výsledek určuje skutečný ovladač a aplikace. Samotný glyph tuto operaci neprovádí.

**Výjimka a návrat:** Nevytvářet druhý nezávislý spouštěč bez názvu. Při odmítnutí nebo zrušení se nesmí zobrazit falešné potvrzení; výsledek i návrat řeší hostitel.

**Nevhodně:** Nevytvářet druhý nezávislý spouštěč bez názvu.

### Interní systém — ITSM

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Běžná“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** Do skutečného ovladače u „Běžná“ vložte glyph a název „Doplnit skutečně otevřenou nabídku výběru“. Až aktivace hostitele vyvolá tuto akci; čtení symbolu ani hover ne. Výsledek určuje skutečný ovladač a aplikace. Samotný glyph tuto operaci neprovádí.

**Výjimka a návrat:** Nevytvářet druhý nezávislý spouštěč bez názvu. Při odmítnutí nebo zrušení se nesmí zobrazit falešné potvrzení; výsledek i návrat řeší hostitel.

**Nevhodně:** Nevytvářet druhý nezávislý spouštěč bez názvu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit schválenou ikonografii, optické velikosti a sémantické barvy symbolů, v návaznosti na slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména vazbu symbolu na název hostitele a zachování jeho skutečného významu. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-22755)
