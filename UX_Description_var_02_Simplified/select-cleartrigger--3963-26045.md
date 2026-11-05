# Select/ClearTrigger

Vymazání Select odstraňuje dosavadní výběr; dopad na povinné pole musí určit nadřazený formulář.

**Vazba:** Select. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Akci pojmenujte jako vymazání výběru. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Select. Akci pojmenujte jako vymazání výběru.

## Kdy zvolit alternativu

Pro datovou hodnotu vyberte Select, Combobox či CascadeSelect podle rozsahu a hierarchie. Pro příkaz použijte Menu; vizuálně podobný obal nesmí měnit tento význam.

## Anatomie, stavy a varianty

Součást skladby **Select**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Vymazat právě vybranou hodnotu, pokud je vymazání povolené.

### Co vyvolávat nemá

- Neodstranit možnost z dat ani neskrýt povinnost pole.

### Přechody a odpovědnost

Otevření nabídky či procházení kandidátů ještě nepotvrzuje hodnotu. Aktivace dostupné možnosti předá její identitu; zrušení procházení zachová dosavadní potvrzený výběr. Vymazání je samostatný povolený krok a povinnost se vyhodnotí ve validačním okamžiku. U vzdálených dat hostitel rozliší čekání, žádnou shodu a chybu; odpověď starého dotazu nesmí nahradit novější nabídku. PopupSurface přebírá tento model pouze od skutečného hostitele, ne podle vzhledu řádku.

### Konkrétní pravidla použití

- Akci pojmenujte jako vymazání výběru.
- U povinného pole zůstává po vymazání chybějící údaj, nikoli potvrzená prázdná volba.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** ClearTrigger vymaže hodnotu tohoto pole; křížek pro zavření celé vrstvy má jiný účinek. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Prázdné povinné pole vysvětlete v určeném validačním okamžiku; vymazáním se povinnost neruší. Nejde o odstranění záznamu.

- **Pravidlo použití:** Neodstranit možnost z dat ani neskrýt povinnost pole.

### ERP — zakázkový formulář

**Situace a cíl:** Pracovník přiřazuje zakázku existujícímu středisku.

**Průchod a výsledek:** Je-li v poli „Středisko“ vybráno „Logistika“ a vymazání je povolené, aktivace odstraní pouze výběr. Nabízená možnost zůstane v datech a uživatel může znovu zvolit jinou.

### Web — nastavení doručení

**Situace a cíl:** Zákazník vybírá z nabízených zemí pro danou službu.

**Průchod a výsledek:** Je-li v poli „Země doručení“ vybráno „Česko“ a vymazání je povolené, aktivace odstraní pouze výběr. Nabízená možnost zůstane v datech a uživatel může znovu zvolit jinou.

### Interní systém — ITSM

**Situace a cíl:** Žadatel volí prioritu z předem vysvětleného seznamu.

**Průchod a výsledek:** Je-li v poli „Priorita požadavku“ vybráno „Běžná“ a vymazání je povolené, aktivace odstraní pouze výběr. Nabízená možnost zůstane v datech a uživatel může znovu zvolit jinou.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26045)
