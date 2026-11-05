# AvailabilityStatus / SkeletonLine

Zástupný řádek AvailabilityStatus rezervuje prostor pro dosud načítanou informaci o dostupnosti.

**Vazba:** AvailabilityStatus. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Pouze po dobu, kdy aplikace skutečně získává příslušný obsah a ještě nezná jeho konečný výsledek. Používejte po dobu čekání na dostupnost. Používejte po dobu čekání na dostupnost.

## Kdy zvolit alternativu

Jakmile je výsledek známý, použijte skutečný obsah nebo vysvětlení prázdného či chybového výsledku. Placeholder není náhradou hlášení o trvalé nedostupnosti.

## Anatomie, stavy a varianty

Součást skladby **AvailabilityStatus**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zastoupit příslušný dosud nedostupný obsah po skutečnou dobu čekání.

### Co vyvolávat nemá

- Nespouštět vlastní akci ani nevydávat zástupnou plochu za známou hodnotu.

### Přechody a odpovědnost

Vstupem je skutečné čekání na tento obsah. Po odpovědi aplikace placeholder odstraní a ukáže data, vysvětlené prázdno nebo chybu s dostupnou nápravou. Při opakování se znovu čeká jen na chybějící oblast; již potvrzené okolní údaje se nevynulují.

### Konkrétní pravidla použití

- Používejte po dobu čekání na dostupnost.
- Zástupný řádek nepředstavuje stav unavailable ani unknown.

## Obsah a pojmenování

Tato vizuální část nepřidává vlastní produktový údaj. Případný popis stavu poskytuje příslušný hostitel; symbol, počet značek nebo zástupná délka se nevydávají za dosud neznámá data.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Známá je struktura budoucího obsahu, jeho výsledek ještě ne; falešná hodnota ani nekonečný spinner by jej nevysvětlily. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Prázdný či chybný výsledek ukončí čekání vysvětlením a případnou akcí opakování; placeholder nesmí běžet trvale. Tato SkeletonLine je statická; nepřebírá pulzaci obecného Skeleton.

- **Nevhodné použití:** Ukázat zástupný tvar jako skutečnou cenu, dostupnost nebo text záznamu.

### ERP — nákup materiálu

**Situace a cíl:** Aplikace ještě získává údaj pro oblast „Dostupnost materiálu“ a jeho výsledek není potvrzený.

**Průchod a výsledek:** Během skutečného získávání dat rezervujte místo pro dostupnost materiálu. Po odpovědi nahraďte placeholder právě tímto obsahem, nikoli dříve přijatou hodnotou jiného objektu.

### Web — produktový detail

**Situace a cíl:** Aplikace ještě získává údaj pro oblast „Dostupnost vybrané varianty“ a jeho výsledek není potvrzený.

**Průchod a výsledek:** Během skutečného získávání dat rezervujte místo pro dostupnost vybrané varianty. Po odpovědi nahraďte placeholder právě tímto obsahem, nikoli dříve přijatou hodnotou jiného objektu.

### Interní systém — objednávání vybavení

**Situace a cíl:** Aplikace ještě získává údaj pro oblast „Dostupnost vybavení“ a jeho výsledek není potvrzený.

**Průchod a výsledek:** Během skutečného získávání dat rezervujte místo pro dostupnost vybavení. Po odpovědi nahraďte placeholder právě tímto obsahem, nikoli dříve přijatou hodnotou jiného objektu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník dostupnosti a význam vizuálních stavů nabídky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj skladových dat, jejich platnost, termíny a pravidla objednatelnosti. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3844-200)
