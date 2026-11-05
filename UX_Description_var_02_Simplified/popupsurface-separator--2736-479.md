# PopupSurface/Separator

Interní oddělovač PopupSurface rozděluje skupiny nabídky a již zahrnuje doložené vnitřní mezery.

**Vazba:** PopupSurface. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když vedle sebe existují dvě významové skupiny, které je třeba odlišit i vizuálně. Rozděluje související skupiny nabídky. Rozděluje související skupiny nabídky.

## Kdy zvolit alternativu

Pokud je třeba vysvětlit význam skupiny, přidejte její skutečný titulek. Oddělovač sám skupinu nepojmenuje a nevytváří další akci.

## Anatomie, stavy a varianty

Součást skladby **PopupSurface**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Oddělit skutečně přítomné související skupiny či úrovně dané skladby.

### Co vyvolávat nemá

- Nespouštět akci a nevytvářet dojem dalšího vybraného nebo chybového objektu.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Rozděluje související skupiny nabídky.
- Vnitřní mezery jsou již součástí oddělovače; další padding nepřičítejte automaticky.

## Obsah a pojmenování

Tato vizuální část nepřidává vlastní produktový údaj. Případný popis stavu poskytuje příslušný hostitel; symbol, počet značek nebo zástupná délka se nevydávají za dosud neznámá data.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Oddělují se již pojmenované skupiny; další Button ani samostatný nadpis by význam čáry nenahradil. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při skrytí prázdné skupiny odstraňte i osiřelý oddělovač. Vnitřní mezery jsou součástí tohoto dílu, nepřičítejte je podruhé.

- **Nevhodné použití:** Dát čáře vlastní fokus nebo z ní udělat nepojmenovaný přepínač.

### ERP — zakázkový formulář

**Situace a cíl:** Pracovník přiřazuje zakázku existujícímu středisku.

**Průchod a výsledek:** V oblasti „Středisko“ oddělte sousední významové skupiny, nikoli položky jednoho nečleněného úkolu. Pořadí i názvy zůstávají srozumitelné bez dekorativní čáry.

### Web — nastavení doručení

**Situace a cíl:** Zákazník vybírá z nabízených zemí pro danou službu.

**Průchod a výsledek:** V oblasti „Země doručení“ oddělte sousední významové skupiny, nikoli položky jednoho nečleněného úkolu. Pořadí i názvy zůstávají srozumitelné bez dekorativní čáry.

### Interní systém — projektové úkoly

**Situace a cíl:** Koordinátor vybírá nástroj u konkrétního úkolu.

**Průchod a výsledek:** V oblasti „Akce úkolu U-58“ oddělte sousední významové skupiny, nikoli položky jednoho nečleněného úkolu. Pořadí i názvy zůstávají srozumitelné bez dekorativní čáry.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2736-479)
