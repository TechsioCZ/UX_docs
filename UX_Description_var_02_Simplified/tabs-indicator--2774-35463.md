# Tabs.Indicator

Indikátor Tabs vizuálně označuje aktivní záložku a souhlasí s právě zobrazeným panelem.

**Vazba:** Tabs. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když je třeba vizuálně rozlišit skutečný stav položky či polohu v sekvenci. Značka označuje aktivní záložku. Značka označuje aktivní záložku.

## Kdy zvolit alternativu

Pokud potřebujete měnit stav, použijte pojmenovaný spouštěč či ovladač hostitele. Samotná značka má označovat skutečný stav a nemá vytvářet jeho druhou nezávislou kopii.

## Anatomie, stavy a varianty

Součást skladby **Tabs**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Označit skutečný stav vlastní položky nebo jejího ovladače.

### Co vyvolávat nemá

- Nevytvářet druhé nezávislé ovládání, pokud jej nepopisuje skutečný hostitel.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Značka označuje aktivní záložku.
- Nesmí se přesunout jen podle hover nebo fokusu, pokud se odpovídající panel nezměnil.

## Obsah a pojmenování

Tato vizuální část nepřidává vlastní produktový údaj. Případný popis stavu poskytuje příslušný hostitel; symbol, počet značek nebo zástupná délka se nevydávají za dosud neznámá data.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Značka pouze potvrzuje skutečný stav hostitele; jeho trigger zajišťuje změnu bez druhého ovladače. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při zrušení výběru nebo zavření se změní i značka. Hover a fokus nezmění potvrzený výběr; disabled neznamená nevybraný.

- **Nevhodné použití:** Použít značku jako druhou samostatnou akci nebo jí oznámit uložení celého formuláře.

### ERP — detail zakázky

**Situace a cíl:** Pracovník přepíná mezi údaji stejné zakázky.

**Průchod a výsledek:** V oblasti „Zakázka — Údaje / Položky“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Značka označuje aktivní záložku. Hostitel současně ukazuje stejný obsah či vybranou identitu.

### Web — detail produktu

**Situace a cíl:** Návštěvník porovnává popis a technické parametry.

**Průchod a výsledek:** V oblasti „Popis / Parametry“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Značka označuje aktivní záložku. Hostitel současně ukazuje stejný obsah či vybranou identitu.

### Interní systém — profil pracovníka

**Situace a cíl:** Uživatel prochází přehled různých druhů údajů o stejné osobě.

**Průchod a výsledek:** V oblasti „Profil / Oprávnění“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Značka označuje aktivní záložku. Hostitel současně ukazuje stejný obsah či vybranou identitu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy panelů, vizuální vzhled záložek a hierarchii vybraného stavu a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí uchování rozepsaných hodnot, načítání a automatickou či potvrzovanou aktivaci. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-35463)
