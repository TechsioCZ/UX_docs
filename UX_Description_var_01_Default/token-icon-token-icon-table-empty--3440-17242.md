# Token Icon/token-icon-table-empty

Glyph `token-icon-table-empty` představuje prázdnou tabulku v odpovídajícím slotu hostitele. Samotný symbol neprovádí akci.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Glyph `token-icon-table-empty` představuje prázdnou tabulku v odpovídajícím slotu hostitele. Samotný symbol neprovádí akci. Použijte ji pouze ve slotu se stejným významem; název ovladače nebo související text tento význam zpřístupní.

## Kdy zvolit alternativu

Když má funkce jiný význam než tato kresba, použijte odpovídající glyph. U neobvyklého nebo závažného příkazu zvolte textové Button či Link; samotný symbol nesmí nahrazovat jeho vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
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

### ERP — seznam objednávek

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Žádné objednávky neodpovídají filtru.“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** Doplňte Table.EmptyState textem „Žádné objednávky neodpovídají filtru.“. Nadále zůstává čitelný kontext a záhlaví; další krok poskytne pojmenované zrušení filtru či skutečně dostupné založení záznamu.

**Výjimka a návrat:** Při výpadku načtení zobrazte chybu a opakování, nikoli pravdivostně chybnou prázdnou databázi.

**Nevhodně:** Skrýt chybu služby za symbol prázdné tabulky.

### Web — zákaznické objednávky

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Zatím nemáte objednávky.“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** Doplňte Table.EmptyState textem „Zatím nemáte objednávky.“. Nadále zůstává čitelný kontext a záhlaví; další krok poskytne pojmenované zrušení filtru či skutečně dostupné založení záznamu.

**Výjimka a návrat:** Při výpadku načtení zobrazte chybu a opakování, nikoli pravdivostně chybnou prázdnou databázi.

**Nevhodně:** Skrýt chybu služby za symbol prázdné tabulky.

### Interní systém — ITSM přehled

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Žádné incidenty v této kategorii.“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** Doplňte Table.EmptyState textem „Žádné incidenty v této kategorii.“. Nadále zůstává čitelný kontext a záhlaví; další krok poskytne pojmenované zrušení filtru či skutečně dostupné založení záznamu.

**Výjimka a návrat:** Při výpadku načtení zobrazte chybu a opakování, nikoli pravdivostně chybnou prázdnou databázi.

**Nevhodně:** Skrýt chybu služby za symbol prázdné tabulky.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit schválenou ikonografii, optické velikosti a sémantické barvy symbolů, v návaznosti na názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména vazbu symbolu na název hostitele a zachování jeho skutečného významu. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3440-17242)
