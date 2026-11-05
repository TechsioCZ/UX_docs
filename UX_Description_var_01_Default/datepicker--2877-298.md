# DatePicker

Datumové pole umožňuje zvolit datum či čas a jejich interval.

Cílem je zadat jednoznačné datum nebo interval s odpovídajícím časovým upřesněním.

## Kdy použít

Pro datum nebo interval, kde kalendář pomůže ověřit den a souvislosti. Proces určí dostupné termíny, přesnost a případné časové pásmo. Samotná změna zobrazeného měsíce nepotvrzuje termín.

## Kdy zvolit alternativu

Nezaměňovat dnešek se zvoleným dnem. Nepotvrzovat neúplný interval nebo nedostupné datum jen změnou zobrazeného měsíce.

## Anatomie, stavy a varianty

Vstup hodnoty a kalendářní Content s CalendarDay; PeriodView se otevírá z hlavičky. Při časovém použití TimeControl patří konkrétnímu datu nebo hranici intervalu.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=error` | Po zjištění konkrétního opravitelného problému. Zpráva pojmenuje údaj a nápravu; rozepsaná hodnota zůstane k opravě. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=readonly` | Když má být existující hodnota čitelná, ale není dovoleno ji měnit. Nezaměňovat za disabled ani za prázdnou hodnotu. |
| `selectionMode=single` | Pro výběr jednoho data; neprezentovat jej jako celý interval. |
| `selectionMode=range` | Pro interval se zřetelným začátkem a koncem; neúplnost se vyhodnotí podle procesu. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Vybrat dostupný den nebo hranice intervalu.
- Při časovém použití upravit odpovídající čas, aniž se ztratí příslušné datum.

### Co vyvolávat nemá

- Nezaměňovat dnešek se zvoleným dnem.
- Nepotvrzovat neúplný interval nebo nedostupné datum jen změnou zobrazeného měsíce.

### Přechody a odpovědnost

Procházení měsíce či roku pouze mění pohled. Potvrzení dostupného dne nebo hranice intervalu mění draft termínu; today není selected. Neúplný či nepřípustný interval zůstane rozpoznatelný k opravě. Čas patří správné hranici a požadované přesnosti. Zrušení nepotvrdí rozpracovaný nový termín; uložení celého úkolu řídí formulář.

### Konkrétní pravidla použití

- Režim single odděluje jednu hodnotu od range se začátkem a koncem.
- Datum bez času se podle modelu DS potvrzuje ihned. Časové hodnoty zůstávají rozpracované do Confirm; Cancel je ruší.
- Formát, časové pásmo a meze určete podle konkrétního použití.
- Dnešní datum, vybrané datum a nedostupný den mají rozdílný význam.
- Readonly neumožňuje změnu ani vymazání hodnoty.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — plánování dodávky

**Situace a cíl:** Pracovník mění termín dodání konkrétní objednávky.

**Volba a varianta:** Termín „12. 11. 2026, 08:30“ vyžaduje kalendářní souvislost a jeden den s časem. V průchodu se uplatní `state=default`, `selectionMode=single`.

**Průchod a výsledek:** Pro objekt „12. 11. 2026, 08:30“ použijte pojmenování „Termín dodání“. Použijte selectionMode=single pro jeden termín. Potřebnou časovou přesnost doplňte příslušným TimeControl. Změna měsíce nebo roku jen zpřístupní volbu; dnešek není automaticky vybrán. Odmítnutou hodnotu označte error a objasněte opravu, neúplný interval se nepotvrdí jako hotový.

**Výjimka a návrat:** Při odmítnutí termínu se vysvětlí dostupná možnost a rozepsaná hodnota zůstane k opravě.

**Nevhodně:** Nezaměňovat dnešek se zvoleným dnem.

### Web — rezervace služby

**Situace a cíl:** Návštěvník vybírá začátek a konec rezervace.

**Volba a varianta:** Termín „12.–14. 11. 2026“ vyžaduje kalendářní souvislost a jednoznačný začátek i konec intervalu. V průchodu se uplatní `state=default`, `selectionMode=range`.

**Průchod a výsledek:** Pro objekt „12.–14. 11. 2026“ použijte pojmenování „Termín rezervace“. Použijte selectionMode=range s rozpoznatelným začátkem a koncem. Změna měsíce nebo roku jen zpřístupní volbu; dnešek není automaticky vybrán. Odmítnutou hodnotu označte error a objasněte opravu, neúplný interval se nepotvrdí jako hotový.

**Výjimka a návrat:** Nedostupný den uvnitř intervalu se posuzuje podle pravidel služby, ne jen podle barvy jeho buňky.

**Nevhodně:** Nezaměňovat dnešek se zvoleným dnem.

### Interní systém — směnový plán

**Situace a cíl:** Koordinátor upravuje časový úsek směny.

**Volba a varianta:** Termín „12. 11. 2026, 08:30–16:00“ vyžaduje kalendářní souvislost a jednoznačný začátek i konec intervalu. V průchodu se uplatní `state=default`, `selectionMode=range`.

**Průchod a výsledek:** Pro objekt „12. 11. 2026, 08:30–16:00“ použijte pojmenování „Čas směny“. Použijte selectionMode=range s rozpoznatelným začátkem a koncem. Potřebnou časovou přesnost doplňte příslušným TimeControl. Změna měsíce nebo roku jen zpřístupní volbu; dnešek není automaticky vybrán. Odmítnutou hodnotu označte error a objasněte opravu, neúplný interval se nepotvrdí jako hotový.

**Výjimka a návrat:** Přechod přes půlnoc se dovolí jen při takovém zadání procesu a s viditelným datem konce.

**Nevhodně:** Nezaměňovat dnešek se zvoleným dnem.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit formát data a času, názvy období a jazyk vysvětlení omezení a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené termíny, časové pásmo, přesnost a pravidla intervalu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2877-298)
