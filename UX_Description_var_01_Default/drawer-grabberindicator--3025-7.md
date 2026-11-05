# Drawer.GrabberIndicator

Vizuální úchyt Drawer naznačuje možnost tažení; jeho orientace odpovídá umístění panelu.

**Vazba:** Drawer. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Vizuální úchyt Drawer naznačuje možnost tažení; jeho orientace odpovídá umístění panelu. Použijte ji pouze ve slotu se stejným významem; název ovladače nebo související text tento význam zpřístupní.

## Kdy zvolit alternativu

Když má funkce jiný význam než tato kresba, použijte odpovídající glyph. U neobvyklého nebo závažného příkazu zvolte textové Button či Link; samotný symbol nesmí nahrazovat jeho vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **Drawer**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `orientation=horizontal` | Vodorovná kresba úchytu odpovídající hornímu či dolnímu panelu. Neurčuje uspořádání obsahu ani sama nezajišťuje resize. |
| `orientation=vertical` | Svislá kresba úchytu odpovídající bočnímu panelu. Aktivní oblast a pohyb řídí Drawer.Grabber, nikoli tato čára. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Vizuálně doplnit význam popsaný v definici této ikony a jeho správný stav.

### Co vyvolávat nemá

- Nepřidat samostatnou aktivaci jen kresbě a neoznámit jiný stav než její textový hostitel.

### Přechody a odpovědnost

Kresbu dosazuje skutečný hostitel podle podmínky popsané níže. Změna glyphu sama nepotvrzuje výběr ani výsledek požadavku. Je-li symbol v ovladači, aktivaci, případné čekání, odmítnutí a návrat řeší tento ovladač; glyph nevytváří další fokus ani vlastní uloženou hodnotu.

### Konkrétní pravidla použití

- Orientace značky odpovídá umístění Drawer.
- Jde o vizuální úchyt; skutečné gesto patří ovládací oblasti a panelu.

## Obsah a pojmenování

Technický název tohoto glyphu není text pro uživatele. Pokud je použit v samostatném ovladači, jeho název pojmenuje konkrétní výsledek a případně objekt zásahu. Dekorativní kresba neopakuje zbytečně stejné sdělení vedle již pojmenovaného obsahu.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

### ERP — související detail objednávky

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Upravit objednávku O-1048“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. V průchodu se uplatní `orientation=vertical`. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** U „Upravit objednávku O-1048“ kresba vizuálně označí úchyt povoleného pohybu panelu. Aktivaci, klávesnici i alternativu k gestu poskytuje hostitelský ovladač; kresba nepřidává druhý fokus.

**Výjimka a návrat:** Změna polohy panelu není uložení jeho obsahu.

**Nevhodně:** Z kresby samotné odvodit funkční resize či potvrzení údajů.

### Web — mobilní filtrování katalogu

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Filtrovat produkty“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. V průchodu se uplatní `orientation=horizontal`. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** U „Filtrovat produkty“ kresba vizuálně označí úchyt povoleného pohybu panelu. Aktivaci, klávesnici i alternativu k gestu poskytuje hostitelský ovladač; kresba nepřidává druhý fokus.

**Výjimka a návrat:** Změna polohy panelu není uložení jeho obsahu.

**Nevhodně:** Z kresby samotné odvodit funkční resize či potvrzení údajů.

### Interní systém — pracovní detail incidentu

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „Incident INC-142“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. V průchodu se uplatní `orientation=vertical`. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

**Průchod a výsledek:** U „Incident INC-142“ kresba vizuálně označí úchyt povoleného pohybu panelu. Aktivaci, klávesnici i alternativu k gestu poskytuje hostitelský ovladač; kresba nepřidává druhý fokus.

**Výjimka a návrat:** Změna polohy panelu není uložení jeho obsahu.

**Nevhodně:** Z kresby samotné odvodit funkční resize či potvrzení údajů.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit schválenou ikonografii, optické velikosti a sémantické barvy symbolů, v návaznosti na logickou stranu panelu, hierarchii jeho textů a prioritu závěrečných akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí modalitu konkrétního použití, ukládání, výchozí velikost a zachování rozpracovaného obsahu. Při doplnění pravidel značky zkontrolujte zejména vazbu symbolu na název hostitele a zachování jeho skutečného významu. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3025-7)
