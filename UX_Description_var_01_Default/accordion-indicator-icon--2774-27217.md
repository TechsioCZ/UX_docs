# Accordion Indicator Icon

Interní ikona Accordion Indicator Icon vizuálně doplňuje směr rozbalení sekce; aktivaci zajišťuje její záhlaví.

**Vazba:** Accordion Internal. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Interní ikona Accordion Indicator Icon vizuálně doplňuje směr rozbalení sekce; aktivaci zajišťuje její záhlaví. Použijte ji pouze ve slotu se stejným významem; název ovladače nebo související text tento význam zpřístupní.

## Kdy zvolit alternativu

Když má funkce jiný význam než tato kresba, použijte odpovídající glyph. U neobvyklého nebo závažného příkazu zvolte textové Button či Link; samotný symbol nesmí nahrazovat jeho vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **Accordion Internal**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=collapsed` | Když přiřazený rozbalovací obsah není otevřený. Text spouštěče dál identifikuje stejný obsah. |
| `state=expanded` | Když je přiřazený obsah skutečně otevřený. Spouštěč, indikátor a obsah se nesmějí rozcházet. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Vizuálně doplnit význam popsaný v definici této ikony a jeho správný stav.

### Co vyvolávat nemá

- Nepřidat samostatnou aktivaci jen kresbě a neoznámit jiný stav než její textový hostitel.

### Přechody a odpovědnost

Kresbu dosazuje skutečný hostitel podle podmínky popsané níže. Změna glyphu sama nepotvrzuje výběr ani výsledek požadavku. Je-li symbol v ovladači, aktivaci, případné čekání, odmítnutí a návrat řeší tento ovladač; glyph nevytváří další fokus ani vlastní uloženou hodnotu.

### Konkrétní pravidla použití

- Značka odpovídá rozbalení příslušné položky.
- Aktivaci poskytuje záhlaví Accordion, nikoli samotná ikona.

## Obsah a pojmenování

Technický název tohoto glyphu není text pro uživatele. Pokud je použit v samostatném ovladači, jeho název pojmenuje konkrétní výsledek a případně objekt zásahu. Dekorativní kresba neopakuje zbytečně stejné sdělení vedle již pojmenovaného obsahu.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

### ERP — detail zakázky

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Rozpis nákladů“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. V průchodu se uplatní `state=collapsed`. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** U „Rozpis nákladů“ kresba vizuálně označí skutečné otevření příslušné sekce. Aktivaci, klávesnici i alternativu k gestu poskytuje hostitelský ovladač; kresba nepřidává druhý fokus.

**Výjimka a návrat:** Při zavření se společně změní obsah i indikátor; fokus není expanded.

**Nevhodně:** Z kresby samotné odvodit funkční resize či potvrzení údajů.

### Web — informace o produktu

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Podmínky vrácení“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. V průchodu se uplatní `state=expanded`. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** U „Podmínky vrácení“ kresba vizuálně označí skutečné otevření příslušné sekce. Aktivaci, klávesnici i alternativu k gestu poskytuje hostitelský ovladač; kresba nepřidává druhý fokus.

**Výjimka a návrat:** Při zavření se společně změní obsah i indikátor; fokus není expanded.

**Nevhodně:** Z kresby samotné odvodit funkční resize či potvrzení údajů.

### Interní systém — HR portál

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Podrobnosti pracoviště“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. V průchodu se uplatní `state=collapsed`. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** U „Podrobnosti pracoviště“ kresba vizuálně označí skutečné otevření příslušné sekce. Aktivaci, klávesnici i alternativu k gestu poskytuje hostitelský ovladač; kresba nepřidává druhý fokus.

**Výjimka a návrat:** Při zavření se společně změní obsah i indikátor; fokus není expanded.

**Nevhodně:** Z kresby samotné odvodit funkční resize či potvrzení údajů.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit schválenou ikonografii, optické velikosti a sémantické barvy symbolů, v návaznosti na pojmenování sekcí, hierarchii titulků a vztah variant default/borderless/child a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí počet současně otevřených sekcí, výchozí otevření a případné načítání obsahu. Při doplnění pravidel značky zkontrolujte zejména vazbu symbolu na název hostitele a zachování jeho skutečného významu. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-27217)
