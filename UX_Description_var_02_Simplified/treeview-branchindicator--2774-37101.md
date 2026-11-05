# TreeView/BranchIndicator

Indikátor větve TreeView vizuálně rozlišuje její otevření a zavření.

**Vazba:** TreeView. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když je třeba vizuálně rozlišit skutečný stav položky či polohu v sekvenci. Značka odpovídá skutečnému rozbalení větve. Značka odpovídá skutečnému rozbalení větve.

## Kdy zvolit alternativu

Pokud potřebujete měnit stav, použijte pojmenovaný spouštěč či ovladač hostitele. Samotná značka má označovat skutečný stav a nemá vytvářet jeho druhou nezávislou kopii.

## Anatomie, stavy a varianty

Součást skladby **TreeView**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=closed` | Při skutečně zavřené větvi. Značka neříká nic o výběru jejího uzlu. |
| `state=open` | Při skutečně otevřené větvi či panelu. Otevření nepotvrzuje jinou hodnotu. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Označit skutečný stav vlastní položky nebo jejího ovladače.

### Co vyvolávat nemá

- Nevytvářet druhé nezávislé ovládání, pokud jej nepopisuje skutečný hostitel.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Značka odpovídá skutečnému rozbalení větve.
- Nesmí vydávat vybranou položku za otevřenou větev.

## Obsah a pojmenování

Tato vizuální část nepřidává vlastní produktový údaj. Případný popis stavu poskytuje příslušný hostitel; symbol, počet značek nebo zástupná délka se nevydávají za dosud neznámá data.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Značka pouze potvrzuje skutečný stav hostitele; jeho trigger zajišťuje změnu bez druhého ovladače. V průchodu se uplatní `state=closed`.

- **Společné výjimky a návrat:** Při zrušení výběru nebo zavření se změní i značka. Hover a fokus nezmění potvrzený výběr; disabled neznamená nevybraný.

- **Nevhodné použití:** Použít značku jako druhou samostatnou akci nebo jí oznámit uložení celého formuláře.

### ERP — struktura organizace

**Situace a cíl:** Pracovník prochází organizační členění před přiřazením zakázky.

**Průchod a výsledek:** V oblasti „Organizační struktura“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Značka odpovídá skutečnému rozbalení větve. Hostitel současně ukazuje stejný obsah či vybranou identitu.

### Web — správa dokumentů

**Situace a cíl:** Přihlášený uživatel prochází své složky a vybírá související dokument.

**Průchod a výsledek:** V oblasti „Vaše dokumenty“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Značka odpovídá skutečnému rozbalení větve. Hostitel současně ukazuje stejný obsah či vybranou identitu.

### Interní systém — DMS archiv

**Situace a cíl:** Správce prochází projektové složky.

**Průchod a výsledek:** V oblasti „Archiv projektů“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Značka odpovídá skutečnému rozbalení větve. Hostitel současně ukazuje stejný obsah či vybranou identitu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy uzlů, ikonografii druhů položek a čitelnost hierarchie a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí datové vztahy, pravidla výběru a případné načítání potomků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-37101)
