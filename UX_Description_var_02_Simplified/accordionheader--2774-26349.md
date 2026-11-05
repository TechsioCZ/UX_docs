# AccordionHeader

Záhlaví Accordion pojmenovává jednu sekci a poskytuje její rozbalovací ovládání.

**Vazba:** Accordion. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Záhlaví ovládá odpovídající AccordionContent. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Accordion. Záhlaví ovládá odpovídající AccordionContent.

## Kdy zvolit alternativu

Pokud musí být obsah čtený bez rozbalení, zobrazte jej trvale. Pro přepínání rovnocenných panelů zvažte Tabs, pro navigaci skutečný Link.

## Anatomie, stavy a varianty

Součást skladby **Accordion**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=collapsed` | Když přiřazený rozbalovací obsah není otevřený. Text spouštěče dál identifikuje stejný obsah. |
| `state=expanded` | Když je přiřazený obsah skutečně otevřený. Spouštěč, indikátor a obsah se nesmějí rozcházet. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Rozbalit nebo sbalit obsah jedné přiřazené sekce.

### Co vyvolávat nemá

- Neodeslat formulář, nepotvrdit souhlas ani otevřít nesouvisející stránku.

### Přechody a odpovědnost

Záhlaví, indikátor a viditelnost obsahu se shodují. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Záhlaví ovládá odpovídající AccordionContent.
- Titulek a indikátor musí popisovat stejnou položku a její skutečné otevření.
- Rozbalení musí jít aktivovat také klávesnicí; dostupný název a oznámení otevření patří stejnému záhlaví.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Zrušení ani neúspěch nesmí předstírat potvrzený výsledek. Neodeslat formulář, nepotvrdit souhlas ani otevřít nesouvisející stránku. Před skrytím obsahu vyřešte fokus uvnitř tak, aby zůstal na dosažitelném místě.

- **Pravidlo použití:** Neodeslat formulář, nepotvrdit souhlas ani otevřít nesouvisející stránku.

### ERP — detail zakázky

**Situace a cíl:** Pracovník potřebuje rozbalit výpočet nákladů vedle souhrnu.

**Volba a varianta:** Tento díl provádí právě místní krok hostitele; jeho obal ani dekorativní glyph jej nenahrazují. V průchodu se uplatní `state=collapsed`.

**Průchod a výsledek:** U „Práce a použitý materiál“: Rozbalit nebo sbalit obsah jedné přiřazené sekce. Záhlaví, indikátor a viditelnost obsahu se shodují. Aktivace musí změnit jen přiřazenou sekci, panel nebo rám; fokus není potvrzením jiných údajů.

### Web — informace o produktu

**Situace a cíl:** Návštěvník si chce přečíst doplňující podmínky služby.

**Volba a varianta:** Tento díl provádí právě místní krok hostitele; jeho obal ani dekorativní glyph jej nenahrazují. V průchodu se uplatní `state=expanded`.

**Průchod a výsledek:** U „Vrácení zboží z internetového obchodu“: Rozbalit nebo sbalit obsah jedné přiřazené sekce. Záhlaví, indikátor a viditelnost obsahu se shodují. Aktivace musí změnit jen přiřazenou sekci, panel nebo rám; fokus není potvrzením jiných údajů.

### Interní systém — HR portál

**Situace a cíl:** Zaměstnanec prochází související části žádosti o vybavení.

**Volba a varianta:** Tento díl provádí právě místní krok hostitele; jeho obal ani dekorativní glyph jej nenahrazují. V průchodu se uplatní `state=collapsed`.

**Průchod a výsledek:** U „Budova A, druhé podlaží“: Rozbalit nebo sbalit obsah jedné přiřazené sekce. Záhlaví, indikátor a viditelnost obsahu se shodují. Aktivace musí změnit jen přiřazenou sekci, panel nebo rám; fokus není potvrzením jiných údajů.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit pojmenování sekcí, hierarchii titulků a vztah variant default/borderless/child a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí počet současně otevřených sekcí, výchozí otevření a případné načítání obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-26349)
