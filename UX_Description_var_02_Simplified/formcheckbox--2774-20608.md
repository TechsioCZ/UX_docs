# FormCheckbox

Formulářové zaškrtávací pole spojuje volbu s popiskem a doprovodnou zprávou.

Cílem je zvolit nezávislou možnost nebo srozumitelně vyjádřit výběr více položek.

## Kdy použít

Pro formulářovou skladbu nezávislé volby včetně názvu a souvisejícího vysvětlení. Samotné označení neodesílá celý formulář. Pouhý výběr datových řádků může použít Checkbox bez další formulářové skladby.

## Kdy zvolit alternativu

Pro jednu možnost ze skupiny použijte RadioGroup; pro samotný stavební ovladač Checkbox.

## Anatomie, stavy a varianty

Checkbox propojený s významem otázky, povinností a případnou zprávou. DisabledChecked zachovává vybranou hodnotu v nedostupném ovladači.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `state=default` | Výchozí nezvolená nebo vypnutá hodnota podle významu ovladače. Neznamená chybu ani potvrzené uložení. |
| `state=checked` | Pro aktuálně zvolenou možnost. Značka vyjadřuje hodnotu, nikoli sama úspěch jejího serverového uložení. |
| `state=indeterminate` | Když je ve skupině vybrána jen část položek. Nejde o třetí odpověď namísto ano/ne. |
| `state=error` | Po zjištění konkrétního opravitelného problému. Zpráva pojmenuje údaj a nápravu; rozepsaná hodnota zůstane k opravě. |
| `state=success` | Po skutečném ověření údaje v daném kontextu. Neznamená automaticky úspěšné uložení celého formuláře. |
| `state=warning` | Pro skutečnou podmínku vyžadující pozornost, při které je pokračování možné. Blokující chyba patří do error/invalid. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=disabledChecked` | Pro již vybranou možnost, kterou nyní nelze měnit. Vybraná hodnota má zůstat rozpoznatelná. |
| `required=false` | Když lze údaj vědomě nevyplnit; absence není automaticky chyba. |
| `required=true` | Když proces skutečně vyžaduje údaj. Stejná podmínka platí ve validaci. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zaškrtnout a zrušit jednotlivou volbu.
- U hromadného výběru rozlišit žádné, některé a všechny položky.

### Co vyvolávat nemá

- Nezaměňovat indeterminate za třetí uživatelskou odpověď.
- Neodesílat celý formulář jen změnou zaškrtnutí, pokud to není předem zřetelný vzor.

### Přechody a odpovědnost

Dostupná aktivace mění hodnotu podle modelu ovladače; disabled ji nemění. Hodnota formuláře se uloží až jeho potvrzením, pokud není předem určené a srozumitelné okamžité ukládání. Při selhání okamžitého uložení aplikace vysvětlí stav a obnoví potvrzenou hodnotu nebo výslovně zachová neuložený návrh. Nelze ponechat zdánlivě uloženou změnu bez vysvětlení.

### Konkrétní pravidla použití

- Text jasně popisuje volbu a její případný důsledek.
- Checked, indeterminate, chyba a nedostupnost jsou rozdílné významy.
- Required neurčuje sám výsledek validace.
- Chybovou zprávu přiřaďte konkrétní volbě; nepředpokládejte libovolné kombinace stavů mimo připravené varianty.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nezaměňovat indeterminate za třetí uživatelskou odpověď.

### ERP — seznam objednávek

**Situace a cíl:** Pracovník vybírá objednávky pro následný společný export.

**Volba a varianta:** Pro „Vybrat objednávku O-1048“ je třeba jedna nezávislá volba, nikoli jediná odpověď vzájemně výlučné RadioGroup. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „Objednávka O-1048“ použijte pojmenování „Vybrat objednávku O-1048“. Výběr řádku přepne jeho hodnotu z nezvolené na checked. Pokud ovladač řídí skupinu, indeterminate použijte jen pro část vybraných položek. Samotné zaškrtnutí neprovede následný export, přiřazení ani odeslání; ty mají samostatnou pojmenovanou akci.

**Výjimka a návrat:** Výběr všech na stránce se nesmí bez vysvětlení vydávat za výběr celé databáze.

### Web — objednávkový formulář

**Situace a cíl:** Zákazník volí nepovinné zasílání zpráv o objednávce.

**Volba a varianta:** Pro „Posílat oznámení e-mailem“ je třeba jedna nezávislá volba, nikoli jediná odpověď vzájemně výlučné RadioGroup. V průchodu se uplatní `state=checked`, `required=false`.

**Průchod a výsledek:** Pro objekt „Oznámení o objednávce“ použijte pojmenování „Posílat oznámení e-mailem“. Výběr řádku přepne jeho hodnotu z nezvolené na checked. Pokud ovladač řídí skupinu, indeterminate použijte jen pro část vybraných položek. Samotné zaškrtnutí neprovede následný export, přiřazení ani odeslání; ty mají samostatnou pojmenovanou akci.

**Výjimka a návrat:** Nepovinná volba není předem vynucená chybovým stavem a neznamená souhlas s jiným účelem.

### Interní systém — správa týmu

**Situace a cíl:** Vedoucí vybírá několik členů pro přiřazení školení.

**Volba a varianta:** Pro „Vybrat člena týmu“ je třeba jedna nezávislá volba, nikoli jediná odpověď vzájemně výlučné RadioGroup. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „Členové týmu Logistika“ použijte pojmenování „Vybrat člena týmu“. Výběr řádku přepne jeho hodnotu z nezvolené na checked. Pokud ovladač řídí skupinu, indeterminate použijte jen pro část vybraných položek. Samotné zaškrtnutí neprovede následný export, přiřazení ani odeslání; ty mají samostatnou pojmenovanou akci.

**Výjimka a návrat:** Zrušení výběru nemaže člena ani jeho dosavadní školení.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit značení povinnosti, slovník souhlasů a vzhled vybraných či chybových voleb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí rozsah výběru, pravidla povinné volby a okamžik uložení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-20608)
