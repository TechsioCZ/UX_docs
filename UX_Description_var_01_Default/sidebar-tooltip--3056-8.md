# Sidebar.Tooltip

Nápověda Sidebar zpřístupňuje název navigačního cíle při jeho vizuálním skrytí ve sbalení.

**Vazba:** Sidebar. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Text odpovídá skutečnému názvu cíle. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Sidebar. Text odpovídá skutečnému názvu cíle.

## Kdy zvolit alternativu

Pokud potřebujete měnit údaj, použijte odpovídající vstupní komponentu. Pokud má text otevírat jiný cíl, použijte skutečný Link s pojmenovaným cílem.

## Anatomie, stavy a varianty

Součást skladby **Sidebar**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `placement=right` | Polohu right volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=left` | Polohu left volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na Sidebar.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Text odpovídá skutečnému názvu cíle.
- Doplňuje sbalenou položku a neznamená další samostatný navigační cíl.
- Nápovědu zpřístupněte i fokusem položky; při přesunu ukazatele do bubliny ji neschovávejte jen kvůli opuštění ikony.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

### ERP — víceagendová aplikace

**Situace a cíl:** Pracovník prochází nákup, sklad a související přehledy.

**Volba a varianta:** Text nese význam této části bez předstírání ovladače; přechod na jiný cíl by potřeboval Link. V průchodu se uplatní `placement=right`.

**Průchod a výsledek:** Zobrazte „Objednávky“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

**Výjimka a návrat:** Tooltip není jediným přístupným názvem navigační položky. Při rozbalení zbytečně neopakuje stejný viditelný label; na dotyku zůstává cíl rozpoznatelný.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Web — zákaznický účet na desktopu

**Situace a cíl:** Zákazník na větší obrazovce potřebuje dosáhnout navigace svého účtu i při sbaleném bočním rámci.

**Volba a varianta:** Text nese význam této části bez předstírání ovladače; přechod na jiný cíl by potřeboval Link. V průchodu se uplatní `placement=right`.

**Průchod a výsledek:** Zobrazte „Moje objednávky“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

**Výjimka a návrat:** Tooltip není jediným přístupným názvem navigační položky. Při rozbalení zbytečně neopakuje stejný viditelný label; na dotyku zůstává cíl rozpoznatelný.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### Interní systém — projektový nástroj

**Situace a cíl:** Člen týmu přechází mezi pracovním seznamem a detaily projektu.

**Volba a varianta:** Text nese význam této části bez předstírání ovladače; přechod na jiný cíl by potřeboval Link. V průchodu se uplatní `placement=right`.

**Průchod a výsledek:** Zobrazte „Dokumenty projektu Orion“ v místě této části a zachovejte spojení s jejím objektem. Uživatel podle tohoto obsahu rozpozná správnou oblast nebo údaj a pokračuje jejím skutečným ovladačem; čtení nic neukládá.

**Výjimka a návrat:** Tooltip není jediným přístupným názvem navigační položky. Při rozbalení zbytečně neopakuje stejný viditelný label; na dotyku zůstává cíl rozpoznatelný.

**Nevhodně:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit šířkovou a vizuální hierarchii rámu, názvy cílů a pravidla zobrazení identity značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí nabídku agend, oprávnění, zvolený režim a zachování kontextu při změně zařízení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3056-8)
