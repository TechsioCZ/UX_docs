# ProductCardStock

Skladová část ProductCard sděluje dostupnost zboží podle vlastního třívariantního modelu.

**Vazba:** ProductCard. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Text dostupnosti patří ke správné variantě produktu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě ProductCard. Text dostupnosti patří ke správné variantě produktu.

## Kdy zvolit alternativu

Pro časově omezené oznámení celé operace zvažte Toast. Chyba jednoho pole má zůstat u tohoto pole; nepotvrzuje ani neblokuje jiný údaj.

## Anatomie, stavy a varianty

Součást skladby **ProductCard**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `status=in-stock` | Pro potvrzenou dostupnost nabídky této karty. Tříhodnotový ProductCardStock není automatický převod všech stavů AvailabilityStatus. |
| `status=limited-stock` | Pro doloženou omezenou dostupnost této nabídky; popis objasní relevantní omezení. |
| `status=out-of-stock` | Pro aktuálně nedostupnou nabídku. Čtení detailu může zůstat možné i bez nákupní akce. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na ProductCard.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Text dostupnosti patří ke správné variantě produktu.
- Tři stavy této části nejsou automatickým mapováním všech stavů AvailabilityStatus.
- Skladová informace sama nepovoluje nákup.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

### ERP — interní katalog materiálu

**Situace a cíl:** Pracovník vybírá konkrétní položku pro nákupní požadavek.

**Volba a varianta:** Zpráva patří stejnému údaji či řádku; mizející Toast by ztížil místní opravu. V průchodu se uplatní `status=limited-stock`.

**Průchod a výsledek:** Zobrazte „Omezená dostupnost“ v místě této části a zachovejte spojení s jejím objektem. Po skutečně zjištěné podmínce uživatel u stejného objektu pozná problém nebo výsledek a pokračuje uvedenou opravou či samostatnou akcí.

**Výjimka a návrat:** Pro unknown či předobjednávku nevymýšlejte další variantu tohoto tříhodnotového dílu; potřebný význam řešte odpovídající skladbou AvailabilityStatus.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Web — e-shop

**Situace a cíl:** Zákazník porovnává nabídky a přidává dostupný produkt do košíku.

**Volba a varianta:** Zpráva patří stejnému údaji či řádku; mizející Toast by ztížil místní opravu. V průchodu se uplatní `status=in-stock`.

**Průchod a výsledek:** Zobrazte „Skladem“ v místě této části a zachovejte spojení s jejím objektem. Po skutečně zjištěné podmínce uživatel u stejného objektu pozná problém nebo výsledek a pokračuje uvedenou opravou či samostatnou akcí.

**Výjimka a návrat:** Pro unknown či předobjednávku nevymýšlejte další variantu tohoto tříhodnotového dílu; potřebný význam řešte odpovídající skladbou AvailabilityStatus.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Interní systém — portál vybavení

**Situace a cíl:** Zaměstnanec vybírá zařízení ze schváleného katalogu.

**Volba a varianta:** Zpráva patří stejnému údaji či řádku; mizející Toast by ztížil místní opravu. V průchodu se uplatní `status=out-of-stock`.

**Průchod a výsledek:** Zobrazte „Není skladem“ v místě této části a zachovejte spojení s jejím objektem. Po skutečně zjištěné podmínce uživatel u stejného objektu pozná problém nebo výsledek a pokračuje uvedenou opravou či samostatnou akcí.

**Výjimka a návrat:** Pro unknown či předobjednávku nevymýšlejte další variantu tohoto tříhodnotového dílu; potřebný význam řešte odpovídající skladbou AvailabilityStatus.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii produktových informací, slovník obchodních štítků a prioritu nákupních akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu nabídky, cenu, skladová data, oprávnění k nákupu a výsledek operace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-36114)
