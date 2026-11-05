# AccordionSubtitle

Podtitulek Accordion doplňuje hlavní titulek o stručný kontext; zachovává jeho hlavní pojmenování.

**Vazba:** Accordion. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když hlavní název sekce potřebuje doplnit stručný kontext, přidejte tento podtitulek. Hlavní titulek zůstává nositelem názvu a odpovídá témuž obsahu. Doplňte hlavní titulek stručným kontextem.

## Kdy zvolit alternativu

Pro hlavní pojmenování sekce použijte AccordionTitle. Dlouhé vysvětlení patří do příslušného Content, nikoli do přerostlého podtitulku.

## Anatomie, stavy a varianty

Součást skladby **Accordion**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na Accordion.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Doplňte hlavní titulek stručným kontextem.
- Základní identita sekce musí zůstat srozumitelná i bez podtitulku.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Podtitulek doplní dopad sekce bez nahrazení jejího názvu; dlouhé vysvětlení patří do Content. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při dlouhém znění nebo zúžení zachovejte celý rozhodující význam i bez hoveru. Změna výběru či objektu aktualizuje současně text; starý údaj nesmí zůstat u nového záznamu.

- **Nevhodné použití:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### ERP — detail zakázky

**Situace a cíl:** Pracovník potřebuje rozbalit výpočet nákladů vedle souhrnu.

**Průchod a výsledek:** Zobrazte „Práce a materiál zvlášť“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

### Web — informace o produktu

**Situace a cíl:** Návštěvník si chce přečíst doplňující podmínky služby.

**Průchod a výsledek:** Zobrazte „Lhůta a postup podání“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

### Interní systém — HR portál

**Situace a cíl:** Zaměstnanec prochází související části žádosti o vybavení.

**Průchod a výsledek:** Zobrazte „Budova A, druhé podlaží“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit pojmenování sekcí, hierarchii titulků a vztah variant default/borderless/child a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí počet současně otevřených sekcí, výchozí otevření a případné načítání obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26466)
