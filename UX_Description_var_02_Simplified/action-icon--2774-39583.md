# Action Icon

Ikonový ovladač s pevným křížkem zavírá jednu konkrétní vrstvu nebo lokální zobrazení.

Cílem je nabídnout jednu opakovanou akci tam, kde její symbol uživatel rozpozná a úplný název zůstane dostupný.

## Kdy použít

Pro zavření právě otevřené vrstvy nebo zrušení lokálního zobrazení, kde je křížek jednoznačný. Tento master má pevný křížek; není to univerzální ovladač pro libovolný glyph. Pro uložení, úpravu či odstranění zvolte textové Button nebo skutečně zaměnitelný ikonový ovladač.

## Kdy zvolit alternativu

Pro uložení, úpravu nebo odstranění použijte odpovídající Button, případně skutečně zaměnitelný ikonový ovladač. Table.IconButton má vlastní zaměnitelný slot; není aliasem tohoto pevného křížku.

## Anatomie, stavy a varianty

Pojmenovaný ovladač s jednou ikonou. Vzhled size/tone/state doplňuje akci; nenahrazuje její název ani vyjasnění objektu zásahu.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `tone=neutral` | Pro běžnou akci bez destruktivního významu; její dostupnost a výsledek zůstávají samostatné. |
| `tone=danger` | Pro skutečně závažnou akci, jejíž důsledek vysvětluje text; konkrétní tokeny určí úroveň 2. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zavřít právě pojmenovanou vrstvu nebo náhled.
- Před zavřením předat řešení rozepsaných údajů hostitelskému panelu.

### Co vyvolávat nemá

- Neukládat, neupravovat ani neodstraňovat záznam pomocí pevného křížku.
- Nepředstírat loading či disabled variantu, kterou tato sada neobsahuje.

### Přechody a odpovědnost

Default přechází do hover jen najetím. Aktivace křížku zavírá určenou vrstvu; neukládá a neodstraňuje záznam. Hostitelská vrstva řeší neuložený draft i návrat fokusu. Master nemá vlastní loading, error ani disabled osu; případnou nedostupnost nelze vyřešit pouhým přejmenováním varianty.

### Konkrétní pravidla použití

- Aktuální master používá pevnou ikonu křížku a nabízí default a hover. Pro jiný symbol zvolte vhodný ikonový ovladač.
- Ovladač pojmenujte podle výsledku, například „Zavřít detail“. Tooltip nemá nahrazovat jeho přístupný název.

## Obsah a pojmenování

Název vyjádří zavření konkrétní vrstvy, například „Zavřít detail dodavatele D-208“. Samotné „Křížek“ nepopisuje výsledek. Tooltip doplňuje orientaci, nenahrazuje přístupný název. Odstranění položky musí mít jiný skutečně určený ovladač.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Jsou-li v panelu rozepsané údaje, produkt před odchodem vyřeší jejich zachování nebo výslovné zahození; křížek sám neukládá.

- **Pravidlo použití:** Neukládat, neupravovat ani neodstraňovat záznam pomocí pevného křížku.

### ERP — detail dodavatele

**Situace a cíl:** Uživatel dokončil prohlížení a chce zavřít detail dodavatele D-208.

**Volba a varianta:** Zavírá se pouze „detail dodavatele D-208“; pevný křížek tomuto výsledku odpovídá, textové Uložit by slibovalo jinou akci. V průchodu se uplatní `tone=neutral`, `state=default`.

**Průchod a výsledek:** Použijte pevný křížek s názvem „Zavřít detail dodavatele D-208“, například tone=neutral a state=default. Hover jen zvýrazní tentýž ovladač. Aktivací se zavře tento náhled či detail a vrátí se kontext původního seznamu; upravit nebo smazat záznam tím nelze.

### Web — redakční systém CMS

**Situace a cíl:** Uživatel dokončil prohlížení a chce zavřít náhled konceptu článku Č-24.

**Volba a varianta:** Zavírá se pouze „náhled konceptu článku Č-24“; pevný křížek tomuto výsledku odpovídá, textové Uložit by slibovalo jinou akci. V průchodu se uplatní `tone=neutral`, `state=default`.

**Průchod a výsledek:** Použijte pevný křížek s názvem „Zavřít náhled konceptu článku Č-24“, například tone=neutral a state=default. Hover jen zvýrazní tentýž ovladač. Aktivací se zavře tento náhled či detail a vrátí se kontext původního seznamu; upravit nebo smazat záznam tím nelze.

### Interní systém — ITSM

**Situace a cíl:** Uživatel dokončil prohlížení a chce zavřít detail incidentu INC-142.

**Volba a varianta:** Zavírá se pouze „detail incidentu INC-142“; pevný křížek tomuto výsledku odpovídá, textové Uložit by slibovalo jinou akci. V průchodu se uplatní `tone=neutral`, `state=default`.

**Průchod a výsledek:** Použijte pevný křížek s názvem „Zavřít detail incidentu INC-142“, například tone=neutral a state=default. Hover jen zvýrazní tentýž ovladač. Aktivací se zavře tento náhled či detail a vrátí se kontext původního seznamu; upravit nebo smazat záznam tím nelze.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník názvů ikonových akcí, vzhled neutral/danger a vztah k textovým tlačítkům a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí oprávnění k akci, potvrzení nevratného zásahu a způsob obnovy. Při doplnění pravidel značky zkontrolujte zejména zavírací význam pevného křížku, jeho pojmenování a kontrast vůči okolní vrstvě. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-39583)
