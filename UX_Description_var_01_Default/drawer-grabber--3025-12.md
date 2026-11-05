# Drawer.Grabber

Oblast úchytu Drawer poskytuje místo pro ovládání tažení; jeho dostupnou alternativu zajišťuje celá kompozice.

**Vazba:** Drawer. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Gesto musí vést ke skutečně podporované změně polohy. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Drawer. Gesto musí vést ke skutečně podporované změně polohy.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v Drawer a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **Drawer**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `orientation=horizontal` | Vodorovné uspořádání, když dovolí čitelné pořadí a celý obsah. |
| `orientation=vertical` | Svislé uspořádání pro dostupný prostor a souvislou orientaci; nemění pořadí významů. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Změnit povolenou pozici či velikost příslušného panelu, pokud to použití nabízí.

### Co vyvolávat nemá

- Neukládat obsah tažením a nevyžadovat gesto jako jedinou cestu k výsledku.

### Přechody a odpovědnost

Panel zůstane použitelný a má dosažitelné důležité akce. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Gesto musí vést ke skutečně podporované změně polohy.
- Zajistěte jiný dostupný způsob stejného výsledku než tažení.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

U interaktivní vrstvy určete počáteční fokus, dostupné zavření a logický návrat. Modální použití drží fokus uvnitř, nemodální ho nesmí bezdůvodně uvěznit. Na malé obrazovce a při dlouhém obsahu zůstanou dosažitelné důležité akce i konec úkolu.

## Omezení a příklady podle typu projektu

### ERP — související detail objednávky

**Situace a cíl:** Pracovník potřebuje upravit údaje vybraného řádku a vidět kontext přehledu.

**Volba a varianta:** Grabber je ovladač povoleného pohybu; GrabberIndicator je pouze jeho kresba. V průchodu se uplatní `orientation=horizontal`.

**Průchod a výsledek:** U panelu „Upravit objednávku O-1048“ lze úchytem změnit pouze skutečně povolenou polohu či velikost. Tentýž výsledek musí mít dostupnou cestu bez přesného tažení; data uvnitř se tím nepotvrzují.

**Výjimka a návrat:** Změna snap polohy sama nedokládá resize obsahu. Po posunu zůstanou dosažitelné závěrečné akce a dlouhý obsah; neexistující pohyb nesmí úchyt slibovat.

**Nevhodně:** Neukládat obsah tažením a nevyžadovat gesto jako jedinou cestu k výsledku.

### Web — mobilní filtrování katalogu

**Situace a cíl:** Návštěvník nastavuje filtry v panelu od okraje obrazovky.

**Volba a varianta:** Grabber je ovladač povoleného pohybu; GrabberIndicator je pouze jeho kresba. V průchodu se uplatní `orientation=horizontal`.

**Průchod a výsledek:** U panelu „Filtrovat produkty“ lze úchytem změnit pouze skutečně povolenou polohu či velikost. Tentýž výsledek musí mít dostupnou cestu bez přesného tažení; data uvnitř se tím nepotvrzují.

**Výjimka a návrat:** Změna snap polohy sama nedokládá resize obsahu. Po posunu zůstanou dosažitelné závěrečné akce a dlouhý obsah; neexistující pohyb nesmí úchyt slibovat.

**Nevhodně:** Neukládat obsah tažením a nevyžadovat gesto jako jedinou cestu k výsledku.

### Interní systém — pracovní detail incidentu

**Situace a cíl:** Řešitel otevře z přehledu vedlejší úkol k incidentu.

**Volba a varianta:** Grabber je ovladač povoleného pohybu; GrabberIndicator je pouze jeho kresba. V průchodu se uplatní `orientation=horizontal`.

**Průchod a výsledek:** U panelu „Incident INC-142“ lze úchytem změnit pouze skutečně povolenou polohu či velikost. Tentýž výsledek musí mít dostupnou cestu bez přesného tažení; data uvnitř se tím nepotvrzují.

**Výjimka a návrat:** Změna snap polohy sama nedokládá resize obsahu. Po posunu zůstanou dosažitelné závěrečné akce a dlouhý obsah; neexistující pohyb nesmí úchyt slibovat.

**Nevhodně:** Neukládat obsah tažením a nevyžadovat gesto jako jedinou cestu k výsledku.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit logickou stranu panelu, hierarchii jeho textů a prioritu závěrečných akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí modalitu konkrétního použití, ukládání, výchozí velikost a zachování rozpracovaného obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3025-12)
