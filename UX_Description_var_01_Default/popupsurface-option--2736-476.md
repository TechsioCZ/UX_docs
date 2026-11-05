# PopupSurface/Option

Interní řádek PopupSurface nese možnost nabídky a rezervované místo jejího indikátoru.

**Vazba:** PopupSurface. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Hostitel určuje, zda jde o formulářovou hodnotu nebo příkaz. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě PopupSurface. Hostitel určuje, zda jde o formulářovou hodnotu nebo příkaz.

## Kdy zvolit alternativu

Pro datovou hodnotu vyberte Select, Combobox či CascadeSelect podle rozsahu a hierarchie. Pro příkaz použijte Menu; vizuálně podobný obal nesmí měnit tento význam.

## Anatomie, stavy a varianty

Součást skladby **PopupSurface**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=selected` | Pro skutečně potvrzenou vybranou položku. Hover ani pouhý fokus ji nenahrazují. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat aktivaci právě hostiteli: výběr hodnoty pro Select/Combobox nebo příkaz pro Menu.

### Co vyvolávat nemá

- Neurčit obchodní akci jen podle vizuálně selected stavu řádku.

### Přechody a odpovědnost

Otevření nabídky či procházení kandidátů ještě nepotvrzuje hodnotu. Aktivace dostupné možnosti předá její identitu; zrušení procházení zachová dosavadní potvrzený výběr. Vymazání je samostatný povolený krok a povinnost se vyhodnotí ve validačním okamžiku. U vzdálených dat hostitel rozliší čekání, žádnou shodu a chybu; odpověď starého dotazu nesmí nahradit novější nabídku. PopupSurface přebírá tento model pouze od skutečného hostitele, ne podle vzhledu řádku.

### Konkrétní pravidla použití

- Hostitel určuje, zda jde o formulářovou hodnotu nebo příkaz.
- Místo indikátoru zůstává rezervované i při jeho skrytí.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — zakázkový formulář

**Situace a cíl:** Pracovník přiřazuje zakázku existujícímu středisku.

**Volba a varianta:** Sdílí se vizuální řádek, nikoli význam: Menu provádí příkaz, Select nebo Combobox potvrzuje hodnotu. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** U pole „Středisko“ aktivace možnosti „Logistika“ předá hodnotu Select či Combobox; hostitel určí potvrzenou identitu.

**Výjimka a návrat:** Zavření bez aktivace ponechá předchozí stav. Disabled možnost nelze provést; hostitel zachová svůj model klávesnice a návratu.

**Nevhodně:** Neurčit obchodní akci jen podle vizuálně selected stavu řádku.

### Web — nastavení doručení

**Situace a cíl:** Zákazník vybírá z nabízených zemí pro danou službu.

**Volba a varianta:** Sdílí se vizuální řádek, nikoli význam: Menu provádí příkaz, Select nebo Combobox potvrzuje hodnotu. V průchodu se uplatní `state=selected`.

**Průchod a výsledek:** U pole „Země doručení“ aktivace možnosti „Česko“ předá hodnotu Select či Combobox; hostitel určí potvrzenou identitu.

**Výjimka a návrat:** Zavření bez aktivace ponechá předchozí stav. Disabled možnost nelze provést; hostitel zachová svůj model klávesnice a návratu.

**Nevhodně:** Neurčit obchodní akci jen podle vizuálně selected stavu řádku.

### Interní systém — projektové úkoly

**Situace a cíl:** Koordinátor vybírá nástroj u konkrétního úkolu.

**Volba a varianta:** Sdílí se vizuální řádek, nikoli význam: Menu provádí příkaz, Select nebo Combobox potvrzuje hodnotu. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** U příkazu v nabídce úkolu U-58 aktivace provede pouze jeho pojmenovanou akci; vizuální selected samo nespouští obchodní operaci.

**Výjimka a návrat:** Zavření bez aktivace ponechá předchozí stav. Disabled možnost nelze provést; hostitel zachová svůj model klávesnice a návratu.

**Nevhodně:** Neurčit obchodní akci jen podle vizuálně selected stavu řádku.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2736-476)
