# __LineItem/ItemError

Interní chybová část LineItem zpřístupňuje problém konkrétní položky.

**Vazba:** LineItem. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Zprávu přiřaďte pouze dotčené položce. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě LineItem. Zprávu přiřaďte pouze dotčené položce.

## Kdy zvolit alternativu

Pro časově omezené oznámení celé operace zvažte Toast. Chyba jednoho pole má zůstat u tohoto pole; nepotvrzuje ani neblokuje jiný údaj.

## Anatomie, stavy a varianty

Součást skladby **LineItem**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na LineItem.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Zprávu přiřaďte pouze dotčené položce.
- Vysvětlete problém a dostupnou opravu bez dojmu, že selhaly všechny řádky.
- Ve výchozí ukázce následuje StatusText za Controls, aby oprava zůstala v souvislosti s ovladači položky.

## Obsah a pojmenování

Názvy údajů, částky nebo množství vztahujte ke stejné položce a jednotce. Měna či balení nezmizí při zkrácení. Ukázkové číslo z příkladu není výchozí hodnota ani limit projektu; jeho zdroj a přesnost určuje aplikace.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Místní zpráva umožní opravu u řádku; samotný Toast by mohl zmizet bez dohledatelné příčiny. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Chyba jedné položky nesmí vyprázdnit ostatní řádky ani zrušit celý návrh. Zpráva zmizí až po opravě nebo novém potvrzeném výsledku.

- **Nevhodné použití:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### ERP — nákupní požadavek

**Situace a cíl:** Pracovník upravuje jeden řádek připravované objednávky materiálu.

**Průchod a výsledek:** U právě dotčené položky zobrazte „Požadované množství není dostupné. Upravte počet balení.“ za jejími Controls. Uživatel upraví počet balení v dostupném QuantityField a znovu jej potvrdí.

### Web — košík

**Situace a cíl:** Zákazník chce odebrat nedostupný produkt z košíku.

**Průchod a výsledek:** U právě dotčené položky zobrazte „Změnu množství se nepodařilo uložit. Zkuste to znovu.“ za jejími Controls. Uživatel může opakovat aktualizaci až po vyjasnění skutečného uloženého množství; ostatní položky zůstávají beze změny.

### Interní systém — portál služeb

**Situace a cíl:** Zaměstnanec čte již odeslaný požadavek v režimu readonly.

**Průchod a výsledek:** U právě dotčené položky zobrazte „Tuto konfiguraci již nelze nově objednat.“ za jejími Controls. Uživatel může otevřít platnou nabídku nebo tuto položku oprávněně odebrat; nedostupnost nesmí znemožnit odebrání.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii názvu, ceny, jednotek a řádkových akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu položky, výpočty, dostupnost a pravidla ukládání změn. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3909-884)
