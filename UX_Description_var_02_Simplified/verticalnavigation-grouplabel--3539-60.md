# VerticalNavigation/GroupLabel

Název skupiny VerticalNavigation orientuje uživatele mezi souvisejícími odkazy.

**Vazba:** VerticalNavigation. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Když několik souvisejících cílů či možností tvoří jednu pojmenovanou skupinu a čtenář je má porovnávat společně. Text pojmenuje společný význam následujících cílů. Text pojmenuje společný význam následujících cílů.

## Kdy zvolit alternativu

Pokud potřebujete měnit údaj, použijte odpovídající vstupní komponentu. Pokud má text otevírat jiný cíl, použijte skutečný Link s pojmenovaným cílem.

## Anatomie, stavy a varianty

Součást skladby **VerticalNavigation**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na VerticalNavigation.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Text pojmenuje společný význam následujících cílů.
- Nezaměňujte jej za odkaz na samostatnou stránku.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Text nese význam této části bez předstírání ovladače; přechod na jiný cíl by potřeboval Link. V průchodu se uplatní `size=sm`.

- **Společné výjimky a návrat:** Při dlouhém znění nebo zúžení zachovejte celý rozhodující význam i bez hoveru. Změna výběru či objektu aktualizuje současně text; starý údaj nesmí zůstat u nového záznamu.

- **Nevhodné použití:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### ERP — navigace nákupní agendy

**Situace a cíl:** Pracovník chce z detailu objednávky přejít do přehledu dodavatelů.

**Průchod a výsledek:** Zobrazte „Nákup“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

### Web — zákaznický účet

**Situace a cíl:** Uživatel přechází mezi svými objednávkami a kontaktními údaji.

**Průchod a výsledek:** Zobrazte „Můj účet“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

### Interní systém — projektový portál

**Situace a cíl:** Člen týmu prochází sekce projektu.

**Průchod a výsledek:** Zobrazte „Projekt Orion“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit informační architekturu značky, názvy sekcí a vizuální hierarchii current/currentPath a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí cílové adresy, viditelnost podle role a zachování práce při přechodu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3539-60)
