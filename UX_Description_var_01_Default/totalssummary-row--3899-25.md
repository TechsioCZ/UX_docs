# .TotalsSummary/Row

Interní řádek TotalsSummary spojuje název dílčí částky s její aplikací dodanou hodnotou a mírou zvýraznění.

**Vazba:** TotalsSummary. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Název a částka tvoří jeden významový řádek. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě TotalsSummary. Název a částka tvoří jeden významový řádek.

## Kdy zvolit alternativu

Pro úpravu hodnoty použijte určený vstup hostitele, ne klikací text bez role. Pro dosud neznámou hodnotu použijte odpovídající čekající či chybové vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **TotalsSummary**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `emphasis=default` | Běžný finanční řádek s jednoznačným názvem, částkou a měnou. |
| `emphasis=discount` | Zvýraznění skutečně slevového řádku; název a částku určuje aplikace. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na TotalsSummary.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Název a částka tvoří jeden významový řádek.
- Emphasis zvýrazňuje příslušnou položku; neprovádí výpočet součtu.
- Volitelná poznámka vysvětluje podmínku právě této částky; nenahrazuje její název nebo hodnotu.

## Obsah a pojmenování

Názvy údajů, částky nebo množství vztahujte ke stejné položce a jednotce. Měna či balení nezmizí při zkrácení. Ukázkové číslo z příkladu není výchozí hodnota ani limit projektu; jeho zdroj a přesnost určuje aplikace.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

### ERP — nákupní požadavek

**Situace a cíl:** Pracovník kontroluje součet připravovaných položek.

**Volba a varianta:** Jde o zobrazení hodnoty; její změna potřebuje určený vstup, nikoli klikací text bez role. V průchodu se uplatní `emphasis=default`.

**Průchod a výsledek:** Zobrazte „Položky celkem: 12 500 Kč“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

**Výjimka a návrat:** Při dlouhém znění nebo zúžení zachovejte celý rozhodující význam i bez hoveru. Změna výběru či objektu aktualizuje současně text; starý údaj nesmí zůstat u nového záznamu.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Web — košík

**Situace a cíl:** Zákazník kontroluje cenu objednávaného obsahu včetně určených nákladů.

**Volba a varianta:** Jde o zobrazení hodnoty; její změna potřebuje určený vstup, nikoli klikací text bez role. V průchodu se uplatní `emphasis=default`.

**Průchod a výsledek:** Zobrazte „Sleva: −200 Kč“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

**Výjimka a návrat:** Při dlouhém znění nebo zúžení zachovejte celý rozhodující význam i bez hoveru. Změna výběru či objektu aktualizuje současně text; starý údaj nesmí zůstat u nového záznamu.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Interní systém — objednávka služeb

**Situace a cíl:** Pracovník sleduje souhrn vybraných firemních služeb.

**Volba a varianta:** Jde o zobrazení hodnoty; její změna potřebuje určený vstup, nikoli klikací text bez role. V průchodu se uplatní `emphasis=default`.

**Průchod a výsledek:** Zobrazte „Služby celkem: 3 000 Kč“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

**Výjimka a návrat:** Při dlouhém znění nebo zúžení zachovejte celý rozhodující význam i bez hoveru. Změna výběru či objektu aktualizuje současně text; starý údaj nesmí zůstat u nového záznamu.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy finančních řádků, měnový zápis a hierarchii celku a slev a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí výpočet, měnu, zdroj částek a blokování související akce při přepočtu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3899-25)
