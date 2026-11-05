# ProductCardPrice

Cenová část ProductCard zobrazuje cenu nabídky dodanou aplikací; její rozsah nemusí odpovídat celému PriceBlock.

**Vazba:** ProductCard. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Cena patří ke stejné nabídce jako ostatní údaje karty. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě ProductCard. Cena patří ke stejné nabídce jako ostatní údaje karty.

## Kdy zvolit alternativu

Pro úpravu hodnoty použijte určený vstup hostitele, ne klikací text bez role. Pro dosud neznámou hodnotu použijte odpovídající čekající či chybové vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **ProductCard**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na ProductCard.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Cena patří ke stejné nabídce jako ostatní údaje karty.
- Měna a případná jednotka mají být jednoznačné; částky dodává aplikace.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

### ERP — interní katalog materiálu

**Situace a cíl:** Uživatel potřebuje v daném projektu přečíst „12 500 Kč za sadu“ ve správném kontextu.

**Volba a varianta:** Jde o zobrazení hodnoty; její změna potřebuje určený vstup, nikoli klikací text bez role. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Zobrazte „12 500 Kč za sadu“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

**Výjimka a návrat:** Chybějící cenu neukazujte jako 0 Kč. Cena na dotaz musí mít pravdivý důvod; čekání řeší PriceBlock, nikoli vymyšlená cena.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Web — e-shop

**Situace a cíl:** Uživatel potřebuje v daném projektu přečíst „1 490 Kč za kus“ ve správném kontextu.

**Volba a varianta:** Jde o zobrazení hodnoty; její změna potřebuje určený vstup, nikoli klikací text bez role. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Zobrazte „1 490 Kč za kus“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

**Výjimka a návrat:** Chybějící cenu neukazujte jako 0 Kč. Cena na dotaz musí mít pravdivý důvod; čekání řeší PriceBlock, nikoli vymyšlená cena.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Interní systém — portál vybavení

**Situace a cíl:** Uživatel potřebuje v daném projektu přečíst „Cena na dotaz“ ve správném kontextu.

**Volba a varianta:** Jde o zobrazení hodnoty; její změna potřebuje určený vstup, nikoli klikací text bez role. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Zobrazte „Cena na dotaz“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

**Výjimka a návrat:** Chybějící cenu neukazujte jako 0 Kč. Cena na dotaz musí mít pravdivý důvod; čekání řeší PriceBlock, nikoli vymyšlená cena.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii produktových informací, slovník obchodních štítků a prioritu nákupních akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu nabídky, cenu, skladová data, oprávnění k nákupu a výsledek operace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26971)
