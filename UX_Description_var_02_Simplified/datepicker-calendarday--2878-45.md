# DatePicker/CalendarDay

Kalendářní den DatePicker reprezentuje konkrétní datum s odlišením výběru, dostupnosti a případné pozice v intervalu.

**Vazba:** DatePicker. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Odlište dnešní datum, vybrané datum, nedostupný den a pozici v intervalu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě DatePicker. Odlište dnešní datum, vybrané datum, nedostupný den a pozici v intervalu.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v DatePicker a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **DatePicker**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `density=regular` | Pro běžné zobrazení kalendářních dnů bez předstírané časové přesnosti. |
| `density=timed` | Pro skladbu kalendáře s časovým ovládáním; hustota neurčuje dostupnost dne. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=today` | Pro aktuální den v určeném časovém kontextu. Today nesmí být zaměněno se selected. |
| `state=selected` | Pro skutečně potvrzenou vybranou položku. Hover ani pouhý fokus ji nenahrazují. |
| `state=in-range` | Pro dny uvnitř zvoleného intervalu; hranice mají vlastní označení. |
| `state=range-start` | Pro skutečný začátek vybíraného nebo vybraného intervalu. |
| `state=range-end` | Pro skutečný konec intervalu; nezaměnit jej za počátek nebo pouhý hover. |
| `state=unavailable` | Pro den, který nelze podle pravidel procesu vybrat. Odlišit od dneška a od sousedního měsíce. |
| `state=outside` | Pro den mimo právě zobrazený měsíc. Samotné outside neurčuje jeho obchodní dostupnost. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Potvrdit dostupný den nebo určenou hranici intervalu.

### Co vyvolávat nemá

- Nezaměnit today za selected a nevybrat disabled či unavailable den.

### Přechody a odpovědnost

Procházení měsíce či roku pouze mění pohled. Potvrzení dostupného dne nebo hranice intervalu mění draft termínu; today není selected. Neúplný či nepřípustný interval zůstane rozpoznatelný k opravě. Čas patří správné hranici a požadované přesnosti. Zrušení nepotvrdí rozpracovaný nový termín; uložení celého úkolu řídí formulář.

### Konkrétní pravidla použití

- Odlište dnešní datum, vybrané datum, nedostupný den a pozici v intervalu.
- Vizuální označení nesmí zaměnit začátek a konec rozsahu.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Nedostupný den nelze potvrdit. U intervalu nejprve zvolte obě přípustné hranice; změna zobrazeného měsíce není potvrzením.

- **Pravidlo použití:** Nezaměnit today za selected a nevybrat disabled či unavailable den.

### ERP — plánování dodávky

**Situace a cíl:** Pracovník mění termín dodání konkrétní objednávky.

**Volba a varianta:** Den potvrzuje konkrétní termín; přehled měsíců a roků zajišťuje PeriodView. V průchodu se uplatní `density=regular`, `state=selected`.

**Průchod a výsledek:** V kalendáři vyhledejte „12. listopadu 2026“. Aktivace dostupného dne upraví termín nebo určenou hranici intervalu; dnešek není automaticky selected.

### Web — rezervace služby

**Situace a cíl:** Návštěvník vybírá začátek a konec rezervace.

**Volba a varianta:** Den potvrzuje konkrétní termín; přehled měsíců a roků zajišťuje PeriodView. V průchodu se uplatní `density=regular`, `state=range-start`.

**Průchod a výsledek:** V kalendáři vyhledejte „12. listopadu 2026 — začátek rezervace“. Aktivace dostupného dne upraví termín nebo určenou hranici intervalu; dnešek není automaticky selected.

### Interní systém — směnový plán

**Situace a cíl:** Koordinátor upravuje časový úsek směny.

**Volba a varianta:** Den potvrzuje konkrétní termín; přehled měsíců a roků zajišťuje PeriodView. V průchodu se uplatní `density=regular`, `state=range-start`.

**Průchod a výsledek:** V kalendáři vyhledejte „12. listopadu 2026 — začátek směny“. Aktivace dostupného dne upraví termín nebo určenou hranici intervalu; dnešek není automaticky selected.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit formát data a času, názvy období a jazyk vysvětlení omezení a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené termíny, časové pásmo, přesnost a pravidla intervalu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2878-45)
