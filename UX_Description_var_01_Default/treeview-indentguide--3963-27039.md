# TreeView/IndentGuide

Vodicí čára TreeView vizuálně podporuje vztah rodič–potomek v zanořeném obsahu.

**Vazba:** TreeView. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když vedle sebe existují dvě významové skupiny, které je třeba odlišit i vizuálně. Čára podporuje čtení vztahu rodič–potomek. Čára podporuje čtení vztahu rodič–potomek.

## Kdy zvolit alternativu

Pokud je třeba vysvětlit význam skupiny, přidejte její skutečný titulek. Oddělovač sám skupinu nepojmenuje a nevytváří další akci.

## Anatomie, stavy a varianty

Součást skladby **TreeView**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Oddělit skutečně přítomné související skupiny či úrovně dané skladby.

### Co vyvolávat nemá

- Nespouštět akci a nevytvářet dojem dalšího vybraného nebo chybového objektu.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Čára podporuje čtení vztahu rodič–potomek.
- Hierarchie musí být srozumitelná i z názvů a uspořádání, ne pouze z čáry.

## Obsah a pojmenování

Tato vizuální část nepřidává vlastní produktový údaj. Případný popis stavu poskytuje příslušný hostitel; symbol, počet značek nebo zástupná délka se nevydávají za dosud neznámá data.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

### ERP — struktura organizace

**Situace a cíl:** Pracovník prochází organizační členění před přiřazením zakázky.

**Volba a varianta:** Oddělují se již pojmenované skupiny; další Button ani samostatný nadpis by význam čáry nenahradil. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** V oblasti „Organizační struktura“ oddělte sousední významové skupiny, nikoli položky jednoho nečleněného úkolu. Pořadí i názvy zůstávají srozumitelné bez dekorativní čáry.

**Výjimka a návrat:** Při skrytí prázdné skupiny odstraňte i osiřelý oddělovač. Na malé šířce čára nesmí nahradit chybějící názvy oblastí.

**Nevhodně:** Dát čáře vlastní fokus nebo z ní udělat nepojmenovaný přepínač.

### Web — správa dokumentů

**Situace a cíl:** Přihlášený uživatel prochází své složky a vybírá související dokument.

**Volba a varianta:** Oddělují se již pojmenované skupiny; další Button ani samostatný nadpis by význam čáry nenahradil. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** V oblasti „Vaše dokumenty“ oddělte sousední významové skupiny, nikoli položky jednoho nečleněného úkolu. Pořadí i názvy zůstávají srozumitelné bez dekorativní čáry.

**Výjimka a návrat:** Při skrytí prázdné skupiny odstraňte i osiřelý oddělovač. Na malé šířce čára nesmí nahradit chybějící názvy oblastí.

**Nevhodně:** Dát čáře vlastní fokus nebo z ní udělat nepojmenovaný přepínač.

### Interní systém — DMS archiv

**Situace a cíl:** Správce prochází projektové složky.

**Volba a varianta:** Oddělují se již pojmenované skupiny; další Button ani samostatný nadpis by význam čáry nenahradil. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** V oblasti „Archiv projektů“ oddělte sousední významové skupiny, nikoli položky jednoho nečleněného úkolu. Pořadí i názvy zůstávají srozumitelné bez dekorativní čáry.

**Výjimka a návrat:** Při skrytí prázdné skupiny odstraňte i osiřelý oddělovač. Na malé šířce čára nesmí nahradit chybějící názvy oblastí.

**Nevhodně:** Dát čáře vlastní fokus nebo z ní udělat nepojmenovaný přepínač.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy uzlů, ikonografii druhů položek a čitelnost hierarchie a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí datové vztahy, pravidla výběru a případné načítání potomků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-27039)
