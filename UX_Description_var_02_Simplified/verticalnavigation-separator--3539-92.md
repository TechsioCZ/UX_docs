# VerticalNavigation/Separator

Oddělovač VerticalNavigation vizuálně rozděluje skupiny navigačních cílů.

**Vazba:** VerticalNavigation. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když vedle sebe existují dvě významové skupiny, které je třeba odlišit i vizuálně. Odděluje přítomné navigační skupiny. Odděluje přítomné navigační skupiny.

## Kdy zvolit alternativu

Pokud je třeba vysvětlit význam skupiny, přidejte její skutečný titulek. Oddělovač sám skupinu nepojmenuje a nevytváří další akci.

## Anatomie, stavy a varianty

Součást skladby **VerticalNavigation**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Oddělit skutečně přítomné související skupiny či úrovně dané skladby.

### Co vyvolávat nemá

- Nespouštět akci a nevytvářet dojem dalšího vybraného nebo chybového objektu.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Odděluje přítomné navigační skupiny.
- Bez navazující skupiny nemá zůstávat osamoceným prvkem.

## Obsah a pojmenování

Tato vizuální část nepřidává vlastní produktový údaj. Případný popis stavu poskytuje příslušný hostitel; symbol, počet značek nebo zástupná délka se nevydávají za dosud neznámá data.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Oddělují se již pojmenované skupiny; další Button ani samostatný nadpis by význam čáry nenahradil. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při skrytí prázdné skupiny odstraňte i osiřelý oddělovač. Na malé šířce čára nesmí nahradit chybějící názvy oblastí.

- **Nevhodné použití:** Dát čáře vlastní fokus nebo z ní udělat nepojmenovaný přepínač.

### ERP — navigace nákupní agendy

**Situace a cíl:** Pracovník chce z detailu objednávky přejít do přehledu dodavatelů.

**Průchod a výsledek:** V oblasti „Nákup / Dodavatelé“ oddělte sousední významové skupiny, nikoli položky jednoho nečleněného úkolu. Pořadí i názvy zůstávají srozumitelné bez dekorativní čáry.

### Web — zákaznický účet

**Situace a cíl:** Uživatel přechází mezi svými objednávkami a kontaktními údaji.

**Průchod a výsledek:** V oblasti „Můj účet / Objednávky“ oddělte sousední významové skupiny, nikoli položky jednoho nečleněného úkolu. Pořadí i názvy zůstávají srozumitelné bez dekorativní čáry.

### Interní systém — projektový portál

**Situace a cíl:** Člen týmu prochází sekce projektu.

**Průchod a výsledek:** V oblasti „Projekt Orion / Dokumenty“ oddělte sousední významové skupiny, nikoli položky jednoho nečleněného úkolu. Pořadí i názvy zůstávají srozumitelné bez dekorativní čáry.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit informační architekturu značky, názvy sekcí a vizuální hierarchii current/currentPath a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí cílové adresy, viditelnost podle role a zachování práce při přechodu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3539-92)
