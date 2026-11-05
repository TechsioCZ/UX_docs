# AccordionIndicator

Indikátor Accordion vizuálně rozlišuje sbalenou a rozbalenou položku.

**Vazba:** Accordion. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když je třeba vizuálně rozlišit skutečný stav položky či polohu v sekvenci. Směr nebo podoba značky odpovídá skutečnému otevření položky. Směr nebo podoba značky odpovídá skutečnému otevření položky.

## Kdy zvolit alternativu

Pokud potřebujete měnit stav, použijte pojmenovaný spouštěč či ovladač hostitele. Samotná značka má označovat skutečný stav a nemá vytvářet jeho druhou nezávislou kopii.

## Anatomie, stavy a varianty

Součást skladby **Accordion**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=collapsed` | Když přiřazený rozbalovací obsah není otevřený. Text spouštěče dál identifikuje stejný obsah. |
| `state=expanded` | Když je přiřazený obsah skutečně otevřený. Spouštěč, indikátor a obsah se nesmějí rozcházet. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Označit skutečný stav vlastní položky nebo jejího ovladače.

### Co vyvolávat nemá

- Nevytvářet druhé nezávislé ovládání, pokud jej nepopisuje skutečný hostitel.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Směr nebo podoba značky odpovídá skutečnému otevření položky.
- Samotná značka nenahrazuje srozumitelný název záhlaví.

## Obsah a pojmenování

Tato vizuální část nepřidává vlastní produktový údaj. Případný popis stavu poskytuje příslušný hostitel; symbol, počet značek nebo zástupná délka se nevydávají za dosud neznámá data.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Při zrušení výběru nebo zavření se změní i značka. Hover a fokus nezmění potvrzený výběr; disabled neznamená nevybraný.

- **Nevhodné použití:** Použít značku jako druhou samostatnou akci nebo jí oznámit uložení celého formuláře.

### ERP — detail zakázky

**Situace a cíl:** Pracovník potřebuje rozbalit výpočet nákladů vedle souhrnu.

**Volba a varianta:** Značka pouze potvrzuje skutečný stav hostitele; jeho trigger zajišťuje změnu bez druhého ovladače. V průchodu se uplatní `state=collapsed`.

**Průchod a výsledek:** V oblasti „Rozpis nákladů“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Směr nebo podoba značky odpovídá skutečnému otevření položky. Hostitel současně ukazuje stejný obsah či vybranou identitu.

### Web — informace o produktu

**Situace a cíl:** Návštěvník si chce přečíst doplňující podmínky služby.

**Volba a varianta:** Značka pouze potvrzuje skutečný stav hostitele; jeho trigger zajišťuje změnu bez druhého ovladače. V průchodu se uplatní `state=expanded`.

**Průchod a výsledek:** V oblasti „Podmínky vrácení“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Směr nebo podoba značky odpovídá skutečnému otevření položky. Hostitel současně ukazuje stejný obsah či vybranou identitu.

### Interní systém — HR portál

**Situace a cíl:** Zaměstnanec prochází související části žádosti o vybavení.

**Volba a varianta:** Značka pouze potvrzuje skutečný stav hostitele; jeho trigger zajišťuje změnu bez druhého ovladače. V průchodu se uplatní `state=collapsed`.

**Průchod a výsledek:** V oblasti „Podrobnosti pracoviště“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Směr nebo podoba značky odpovídá skutečnému otevření položky. Hostitel současně ukazuje stejný obsah či vybranou identitu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit pojmenování sekcí, hierarchii titulků a vztah variant default/borderless/child a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí počet současně otevřených sekcí, výchozí otevření a případné načítání obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-26344)
