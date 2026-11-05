# RadioGroup.Item

Položka rádiové skupiny představuje jednu z navzájem výlučných voleb.

Cílem je vybrat jednu stručně pojmenovanou hodnotu ze vzájemně se vylučujících odpovědí.

## Kdy použít

Pro právě jednu stručnou odpověď v pojmenované skupině. Výběr musí jít změnit bez nevratného vedlejšího účinku. Více nezávislých odpovědí patří do Checkbox; rozsáhlé alternativy do RadioCard.

## Kdy zvolit alternativu

Pro bohatší vysvětlení možností použijte RadioCard, pro dlouhý seznam Select a pro nezávislé volby Checkbox.

## Anatomie, stavy a varianty

Jednotlivé RadioGroup.Item s názvy a společným významem otázky. Skupina má jednu vybranou odpověď; styl outline/subtle/solid nemění počet povolených voleb.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `variant=outline` | Vizuální provedení outline podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `variant=subtle` | Vizuální provedení subtle podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `variant=solid` | Vizuální provedení solid podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `state=default` | Výchozí nezvolená nebo vypnutá hodnota podle významu ovladače. Neznamená chybu ani potvrzené uložení. |
| `state=checked` | Pro aktuálně zvolenou možnost. Značka vyjadřuje hodnotu, nikoli sama úspěch jejího serverového uložení. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=invalid` | Když kontrola odhalí neplatný údaj nebo výběr. Vysvětlení určí opravu; samotná barva nestačí. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Změnit výběr v jedné skupině.
- Ponechat pojmenování celé otázky i jednotlivých odpovědí rozpoznatelné.

### Co vyvolávat nemá

- Nepoužívat na několik nezávislých zapnutí.
- Neprovádět navazující nevratnou operaci pouhou změnou označené odpovědi.

### Přechody a odpovědnost

Dostupná aktivace mění hodnotu podle modelu ovladače; disabled ji nemění. Hodnota formuláře se uloží až jeho potvrzením, pokud není předem určené a srozumitelné okamžité ukládání. Při selhání okamžitého uložení aplikace vysvětlí stav a obnoví potvrzenou hodnotu nebo výslovně zachová neuložený návrh. Nelze ponechat zdánlivě uloženou změnu bez vysvětlení.

### Konkrétní pravidla použití

- Pojmenujte skupinu i jednotlivé volby.
- Udržujte jednu společnou hodnotu výběru.
- Checked se liší od pouhého fokusu a invalid od disabled.
- Pořadí možností musí být srozumitelné bez barevného rozlišení.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nepoužívat na několik nezávislých zapnutí.

### ERP — forma úhrady

**Situace a cíl:** Pracovník vybírá jednu z nabízených forem úhrady dokladu.

**Volba a varianta:** Pro „Forma úhrady“ je třeba jedna z výlučných možností; několik nezávislých Checkbox by dovolilo rozporné odpovědi. V průchodu se uplatní `variant=solid`, `state=default`.

**Průchod a výsledek:** Pro objekt „Převodem“ použijte pojmenování „Forma úhrady“. Pojmenujte společnou otázku a po aktivaci možnosti „Převodem“ označte checked právě tuto alternativu. Při volbě jiné se původní odznačí. Invalid použijte pro skutečně chybějící či nepřípustný výběr v určeném validačním okamžiku, nikoli jako běžné počáteční zvýraznění skupiny.

**Výjimka a návrat:** Individuální nedostupná odpověď se liší od chybějícího povinného výběru.

### Web — způsob kontaktu

**Situace a cíl:** Návštěvník určuje preferovaný kanál odpovědi.

**Volba a varianta:** Pro „Jak vás máme kontaktovat“ je třeba jedna z výlučných možností; několik nezávislých Checkbox by dovolilo rozporné odpovědi. V průchodu se uplatní `variant=solid`, `state=checked`.

**Průchod a výsledek:** Pro objekt „E-mailem“ použijte pojmenování „Jak vás máme kontaktovat“. Pojmenujte společnou otázku a po aktivaci možnosti „E-mailem“ označte checked právě tuto alternativu. Při volbě jiné se původní odznačí. Invalid použijte pro skutečně chybějící či nepřípustný výběr v určeném validačním okamžiku, nikoli jako běžné počáteční zvýraznění skupiny.

**Výjimka a návrat:** Dlouhý seznam možností může vyžadovat Select, místo přehlcené skupiny.

### Interní systém — ITSM

**Situace a cíl:** Žadatel určuje, zda se potíž týká jedné osoby nebo celého týmu.

**Volba a varianta:** Pro „Rozsah potíží“ je třeba jedna z výlučných možností; několik nezávislých Checkbox by dovolilo rozporné odpovědi. V průchodu se uplatní `variant=solid`, `state=default`.

**Průchod a výsledek:** Pro objekt „Celý tým“ použijte pojmenování „Rozsah potíží“. Pojmenujte společnou otázku a po aktivaci možnosti „Celý tým“ označte checked právě tuto alternativu. Při volbě jiné se původní odznačí. Invalid použijte pro skutečně chybějící či nepřípustný výběr v určeném validačním okamžiku, nikoli jako běžné počáteční zvýraznění skupiny.

**Výjimka a návrat:** Invalid neoznačuje konkrétní osobu či tým za chybný, ale problém s vyplněním skupiny.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník odpovědí, jejich pořadí a vzhled výběru a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povinnost skupiny, dostupné odpovědi a okamžik potvrzení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-33126)
