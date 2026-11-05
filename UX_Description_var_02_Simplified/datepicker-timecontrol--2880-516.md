# DatePicker/TimeControl

Časové ovládání DatePicker upravuje hodiny, minuty či sekundy; v rozsahu má oddělenou skupinu začátku a konce.

**Vazba:** DatePicker. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Granularity určuje pole pro hodiny, minuty nebo sekundy. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě DatePicker. Granularity určuje pole pro hodiny, minuty nebo sekundy.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v DatePicker a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **DatePicker**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `selectionMode=single` | Pro výběr jednoho data; neprezentovat jej jako celý interval. |
| `selectionMode=range` | Pro interval se zřetelným začátkem a koncem; neúplnost se vyhodnotí podle procesu. |
| `granularity=hour` | Když stačí hodinová přesnost a produkt určil její pravidla. |
| `granularity=minute` | Když uživatelský úkol vyžaduje minuty při zachovaném datu. |
| `granularity=second` | Jen pokud proces skutečně vyžaduje sekundovou přesnost; nevynucovat ji pro běžný termín. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=readonly` | Když má být existující hodnota čitelná, ale není dovoleno ji měnit. Nezaměňovat za disabled ani za prázdnou hodnotu. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Upravit odpovídající časový údaj zvoleného data či hranice intervalu.

### Co vyvolávat nemá

- Nezaměnit začátek a konec ani neodvodit přesnost z pouhé vizuální velikosti.

### Přechody a odpovědnost

Procházení měsíce či roku pouze mění pohled. Potvrzení dostupného dne nebo hranice intervalu mění draft termínu; today není selected. Neúplný či nepřípustný interval zůstane rozpoznatelný k opravě. Čas patří správné hranici a požadované přesnosti. Zrušení nepotvrdí rozpracovaný nový termín; uložení celého úkolu řídí formulář.

### Konkrétní pravidla použití

- Granularity určuje pole pro hodiny, minuty nebo sekundy.
- V range oddělte a pojmenujte začátek a konec.
- Čas zůstává draftem do Confirm; Cancel jej ruší podle modelu DatePicker.
- Pásmo, meze a pravidla platného intervalu dodává konkrétní použití.
- Neúplný čas nebo obrácený interval nepovažujte za potvrzený výsledek. Přechod přes půlnoc musí vycházet i z datumového kontextu, ne jen z pořadí hodin.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Pole má stálý přístupný název, viditelný význam a propojené instrukce i konkrétní chybu. Zachovejte rozepsané hodnoty při odmítnutí. Klávesnicové ovládání a čtení nesmí záviset jen na hoveru; delší text či jednotka nepřekrývají ovladače.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Odmítnutý čas zůstane k opravě u správné hranice. Produkt určí časové pásmo a pravidla intervalu; změna času nepotvrdí jiný den.

- **Pravidlo použití:** Nezaměnit začátek a konec ani neodvodit přesnost z pouhé vizuální velikosti.

### ERP — plánování dodávky

**Situace a cíl:** Pracovník mění termín dodání konkrétní objednávky.

**Volba a varianta:** Časový údaj doplňuje vybrané datum, samotný CalendarDay jej nezadá. V průchodu se uplatní `selectionMode=single`, `granularity=minute`, `state=default`.

**Průchod a výsledek:** Pro odpovídající hranici termínu nastavte „08:30“. Pole pojmenujte Začátek či Konec, pokud jsou přítomné obě hranice; datum a požadovaná přesnost zůstávají součástí hodnoty.

### Web — rezervace služby s časem

**Situace a cíl:** Zákazník vybírá službu s určeným časem příjezdu, nejen celé dny rezervace.

**Volba a varianta:** Časový údaj doplňuje vybrané datum, samotný CalendarDay jej nezadá. V průchodu se uplatní `selectionMode=range`, `granularity=hour`, `state=default`.

**Průchod a výsledek:** Pro odpovídající hranici termínu nastavte „Začátek 12. 11. v 10:00, konec 14. 11. v 16:00“. Pole pojmenujte Začátek či Konec, pokud jsou přítomné obě hranice; datum a požadovaná přesnost zůstávají součástí hodnoty.

### Interní systém — směnový plán

**Situace a cíl:** Koordinátor upravuje časový úsek směny.

**Volba a varianta:** Časový údaj doplňuje vybrané datum, samotný CalendarDay jej nezadá. V průchodu se uplatní `selectionMode=range`, `granularity=minute`, `state=default`.

**Průchod a výsledek:** Pro odpovídající hranici termínu nastavte „Začátek 08:30, konec 16:00“. Pole pojmenujte Začátek či Konec, pokud jsou přítomné obě hranice; datum a požadovaná přesnost zůstávají součástí hodnoty.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit formát data a času, názvy období a jazyk vysvětlení omezení a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené termíny, časové pásmo, přesnost a pravidla intervalu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2880-516)
