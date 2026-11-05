# CarouselControl

Směrový ovladač Carousel zpřístupňuje pohyb k předchozí nebo další položce.

**Vazba:** Carousel. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Ovladač pojmenujte podle směru: předchozí nebo další snímek. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Carousel. Ovladač pojmenujte podle směru: předchozí nebo další snímek.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v Carousel a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **Carousel**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zobrazit předchozí či další existující snímek odpovídajícím ovladačem.

### Co vyvolávat nemá

- Neměnit produkt, objednávku či výběr jiného ovladače.

### Přechody a odpovědnost

Hlavní snímek a indikátor ukazují stejnou novou pozici. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Ovladač pojmenujte podle směru: předchozí nebo další snímek.
- Na krajích sekvence musí dostupnost odpovídat skutečným možnostem procházení.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Dvojice mění pozici o jeden snímek; přímý skok na určenou pozici řeší CarouselIndicator. V průchodu se uplatní `size=sm`.

- **Společné výjimky a návrat:** Na posledním snímku nevymýšlejte cyklení, pokud není skutečně určeno. Přepnutí nemění produkt ani nepotvrzuje formulář.

- **Pravidlo použití:** Neměnit produkt, objednávku či výběr jiného ovladače.

### ERP — katalog zařízení

**Situace a cíl:** Pracovník porovnává pohledy na vybírané zařízení.

**Průchod a výsledek:** U sekvence „Fotografie zařízení“ pojmenujte ovladače Předchozí snímek a Další snímek. Aktivace dostupného Další zobrazí následující existující snímek a současně přepne odpovídající indikátor.

### Web — produktová prezentace

**Situace a cíl:** Návštěvník chce vidět více situací použití produktu.

**Průchod a výsledek:** U sekvence „Ukázky použití“ pojmenujte ovladače Předchozí snímek a Další snímek. Aktivace dostupného Další zobrazí následující existující snímek a současně přepne odpovídající indikátor.

### Interní systém — výuková knihovna

**Situace a cíl:** Pracovník prochází související obrázkové instrukce.

**Průchod a výsledek:** U sekvence „Ukázky nastavení“ pojmenujte ovladače Předchozí snímek a Další snímek. Aktivace dostupného Další zobrazí následující existující snímek a současně přepne odpovídající indikátor.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit povolený styl prezentace, práci s pohybem a význam případného zvýraznění obsahu a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí pořadí snímků, krajní chování sekvence a případné přehrávání. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3935-122)
