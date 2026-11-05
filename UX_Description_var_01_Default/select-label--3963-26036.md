# Select/Label

Popisek Select pojmenovává údaj, který má uživatel vybrat z nabídky.

**Vazba:** Select. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když uživatel zadává nebo vybírá údaj, ponechte jeho název čitelný před vyplněním i po něm. Pojmenujte vybíraný údaj a propojte popisek s odpovídajícím polem. Pojmenujte vybíraný údaj a propojte popisek s odpovídajícím polem.

## Kdy zvolit alternativu

Instrukci nebo chybu sdělte navázanou nápovědou či StatusText; trvalý název pole tím nenahrazujte. Pro akci použijte odpovídající tlačítko.

## Anatomie, stavy a varianty

Součást skladby **Select**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na Select.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Pojmenujte vybíraný údaj a propojte popisek s odpovídajícím polem.
- Popisek zůstává srozumitelný před výběrem i po něm.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

### ERP — zakázkový formulář

**Situace a cíl:** Pracovník přiřazuje zakázku existujícímu středisku.

**Volba a varianta:** Stálý název zůstává čitelný po vyplnění; placeholder ani chybová zpráva jej nenahradí. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Zobrazte „Středisko“ v místě této části a zachovejte spojení s jejím objektem. Před zadáním uživatel rozpozná požadovaný údaj; programové přiřazení vede na správný ovladač, nikoli na sousední pole.

**Výjimka a návrat:** Při dlouhém znění nebo zúžení zachovejte celý rozhodující význam i bez hoveru. Změna výběru či objektu aktualizuje současně text; starý údaj nesmí zůstat u nového záznamu.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Web — nastavení doručení

**Situace a cíl:** Zákazník vybírá z nabízených zemí pro danou službu.

**Volba a varianta:** Stálý název zůstává čitelný po vyplnění; placeholder ani chybová zpráva jej nenahradí. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Zobrazte „Země doručení“ v místě této části a zachovejte spojení s jejím objektem. Před zadáním uživatel rozpozná požadovaný údaj; programové přiřazení vede na správný ovladač, nikoli na sousední pole.

**Výjimka a návrat:** Při dlouhém znění nebo zúžení zachovejte celý rozhodující význam i bez hoveru. Změna výběru či objektu aktualizuje současně text; starý údaj nesmí zůstat u nového záznamu.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Interní systém — ITSM

**Situace a cíl:** Žadatel volí prioritu z předem vysvětleného seznamu.

**Volba a varianta:** Stálý název zůstává čitelný po vyplnění; placeholder ani chybová zpráva jej nenahradí. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Zobrazte „Priorita požadavku“ v místě této části a zachovejte spojení s jejím objektem. Před zadáním uživatel rozpozná požadovaný údaj; programové přiřazení vede na správný ovladač, nikoli na sousední pole.

**Výjimka a návrat:** Při dlouhém znění nebo zúžení zachovejte celý rozhodující význam i bez hoveru. Změna výběru či objektu aktualizuje současně text; starý údaj nesmí zůstat u nového záznamu.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26036)
