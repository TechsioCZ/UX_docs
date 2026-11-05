# Select/ItemIndicator

Indikátor položky Select vizuálně označuje vybranou možnost v nabídce.

**Vazba:** Select. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když je třeba vizuálně rozlišit skutečný stav položky či polohu v sekvenci. Značka odpovídá skutečně vybrané možnosti. Značka odpovídá skutečně vybrané možnosti.

## Kdy zvolit alternativu

Pokud potřebujete měnit stav, použijte pojmenovaný spouštěč či ovladač hostitele. Samotná značka má označovat skutečný stav a nemá vytvářet jeho druhou nezávislou kopii.

## Anatomie, stavy a varianty

Součást skladby **Select**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Označit skutečný stav vlastní položky nebo jejího ovladače.

### Co vyvolávat nemá

- Nevytvářet druhé nezávislé ovládání, pokud jej nepopisuje skutečný hostitel.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Značka odpovídá skutečně vybrané možnosti.
- Hover ani fokus samy neznamenají potvrzený výběr.

## Obsah a pojmenování

Tato vizuální část nepřidává vlastní produktový údaj. Případný popis stavu poskytuje příslušný hostitel; symbol, počet značek nebo zástupná délka se nevydávají za dosud neznámá data.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Značka pouze potvrzuje skutečný stav hostitele; jeho trigger zajišťuje změnu bez druhého ovladače. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při zrušení výběru nebo zavření se změní i značka. Hover a fokus nezmění potvrzený výběr; disabled neznamená nevybraný.

- **Nevhodné použití:** Použít značku jako druhou samostatnou akci nebo jí oznámit uložení celého formuláře.

### ERP — zakázkový formulář

**Situace a cíl:** Pracovník přiřazuje zakázku existujícímu středisku.

**Průchod a výsledek:** V oblasti „Středisko“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Značka odpovídá skutečně vybrané možnosti. Hostitel současně ukazuje stejný obsah či vybranou identitu.

### Web — nastavení doručení

**Situace a cíl:** Zákazník vybírá z nabízených zemí pro danou službu.

**Průchod a výsledek:** V oblasti „Země doručení“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Značka odpovídá skutečně vybrané možnosti. Hostitel současně ukazuje stejný obsah či vybranou identitu.

### Interní systém — ITSM

**Situace a cíl:** Žadatel volí prioritu z předem vysvětleného seznamu.

**Průchod a výsledek:** V oblasti „Priorita požadavku“ ukažte označení až při odpovídajícím vybraném nebo otevřeném stavu. Značka odpovídá skutečně vybrané možnosti. Hostitel současně ukazuje stejný obsah či vybranou identitu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26068)
