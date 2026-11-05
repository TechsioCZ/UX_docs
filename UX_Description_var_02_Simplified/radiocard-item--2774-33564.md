# RadioCard.Item

Výběrová karta představuje jednu možnost ze vzájemně se vylučující skupiny.

Cílem je vybrat právě jednu z několika vzájemně se vylučujících možností s potřebným vysvětlením.

## Kdy použít

Pro právě jednu z možností, jejichž dopady potřebují vedle názvu i vysvětlení. Celá sada má jednu otázku. Stručné alternativy řeší RadioGroup; nezávislé volby Checkbox.

## Kdy zvolit alternativu

Pro stručné možnosti použijte RadioGroup, pro nezávislé výběry Checkbox.

## Anatomie, stavy a varianty

Jedna možnost pojmenované skupiny s titulkem a potřebným vysvětlením. Checked označuje jedinou vybranou alternativu dané skupiny.

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

- Vybrat jednu možnost společné pojmenované skupiny.
- Zpřístupnit doplňující text možnosti jako součást rozhodování.

### Co vyvolávat nemá

- Neumožnit několik současných odpovědí tam, kde je pravidlem právě jedna.
- Nezaměňovat výběr karty za dokončenou objednávku.

### Přechody a odpovědnost

Dostupná aktivace mění hodnotu podle modelu ovladače; disabled ji nemění. Hodnota formuláře se uloží až jeho potvrzením, pokud není předem určené a srozumitelné okamžité ukládání. Při selhání okamžitého uložení aplikace vysvětlí stav a obnoví potvrzenou hodnotu nebo výslovně zachová neuložený návrh. Nelze ponechat zdánlivě uloženou změnu bez vysvětlení.

### Konkrétní pravidla použití

- Položky tvoří jednu pojmenovanou skupinu.
- Titulek a popis vysvětlí rozdíl mezi nabídkami.
- Výběr se liší od fokusu, chyby i nedostupnosti.
- Případná doplňující akce nesmí nejasně měnit vybranou možnost.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Neumožnit několik současných odpovědí tam, kde je pravidlem právě jedna.

### ERP — způsob dodání

**Situace a cíl:** Pracovník volí jediný způsob převzetí materiálu.

**Volba a varianta:** Pro „Způsob převzetí“ je třeba jedna z výlučných možností; několik nezávislých Checkbox by dovolilo rozporné odpovědi. V průchodu se uplatní `variant=solid`, `state=default`.

**Průchod a výsledek:** Pro objekt „Vyzvednutí ve skladu“ použijte pojmenování „Způsob převzetí“. Pojmenujte společnou otázku a po aktivaci možnosti „Vyzvednutí ve skladu“ označte checked právě tuto alternativu. Při volbě jiné se původní odznačí. Invalid použijte pro skutečně chybějící či nepřípustný výběr v určeném validačním okamžiku, nikoli jako běžné počáteční zvýraznění skupiny.

**Výjimka a návrat:** Povinný nevyplněný výběr se vyhodnotí až při určené kontrole, nikoli jen otevřením stránky.

### Web — nabídka služby

**Situace a cíl:** Návštěvník porovnává několik vzájemně alternativních balíčků.

**Volba a varianta:** Pro „Balíček služby“ je třeba jedna z výlučných možností; několik nezávislých Checkbox by dovolilo rozporné odpovědi. V průchodu se uplatní `variant=solid`, `state=checked`.

**Průchod a výsledek:** Pro objekt „Rozšířená podpora“ použijte pojmenování „Balíček služby“. Pojmenujte společnou otázku a po aktivaci možnosti „Rozšířená podpora“ označte checked právě tuto alternativu. Při volbě jiné se původní odznačí. Invalid použijte pro skutečně chybějící či nepřípustný výběr v určeném validačním okamžiku, nikoli jako běžné počáteční zvýraznění skupiny.

**Výjimka a návrat:** Disabled nabídka zůstane vysvětlená a nelze ji potvrdit jen kliknutím na její text.

### Interní systém — HR požadavek

**Situace a cíl:** Zaměstnanec vybírá variantu vybavení pracoviště.

**Volba a varianta:** Pro „Sada vybavení“ je třeba jedna z výlučných možností; několik nezávislých Checkbox by dovolilo rozporné odpovědi. V průchodu se uplatní `variant=solid`, `state=default`.

**Průchod a výsledek:** Pro objekt „Mobilní pracoviště“ použijte pojmenování „Sada vybavení“. Pojmenujte společnou otázku a po aktivaci možnosti „Mobilní pracoviště“ označte checked právě tuto alternativu. Při volbě jiné se původní odznačí. Invalid použijte pro skutečně chybějící či nepřípustný výběr v určeném validačním okamžiku, nikoli jako běžné počáteční zvýraznění skupiny.

**Výjimka a návrat:** Má-li být možné sestavit více nezávislých položek, použije se odpovídající vícevolbový vzor.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii textů voleb a vzhled variant outline/subtle/solid a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené možnosti, povinnost skupiny a případný výchozí výběr. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-33564)
