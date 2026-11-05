# DatePicker/PeriodView

Přehled období DatePicker umožňuje vybrat měsíc nebo rok pro další kalendářní navigaci.

**Vazba:** DatePicker. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Month a year mění úroveň kalendářní navigace. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě DatePicker. Month a year mění úroveň kalendářní navigace.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v DatePicker a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **DatePicker**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `view=month` | Výběr měsíce z hlavičky kalendáře; nejde o nový samostatný veřejný DatePicker. |
| `view=year` | Výběr roku z hlavičky kalendáře; potvrzený den není automaticky změněn jen otevřením tohoto pohledu. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Změnit zobrazené období výběrem měsíce či roku z rozbalené hlavičky.

### Co vyvolávat nemá

- Samotnou změnou období neodeslat formulář ani automaticky nepotvrdit den.

### Přechody a odpovědnost

Procházení měsíce či roku pouze mění pohled. Potvrzení dostupného dne nebo hranice intervalu mění draft termínu; today není selected. Neúplný či nepřípustný interval zůstane rozpoznatelný k opravě. Čas patří správné hranici a požadované přesnosti. Zrušení nepotvrdí rozpracovaný nový termín; uložení celého úkolu řídí formulář.

### Konkrétní pravidla použití

- Month a year mění úroveň kalendářní navigace.
- Zobrazené období není automaticky potvrzená hodnota pole.
- Pohled se otevírá přes nadpis kalendáře; nejde o samostatný veřejný kořen DatePicker.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — plánování dodávky

**Situace a cíl:** Pracovník mění termín dodání konkrétní objednávky.

**Volba a varianta:** PeriodView zrychluje změnu období; sám nepotvrzuje celý den jako CalendarDay. V průchodu se uplatní `view=month`.

**Průchod a výsledek:** Z hlavičky otevřete odpovídající přehled a zvolte „listopad 2026“. Kalendář přejde do vybraného období, kde uživatel teprve volí den.

**Výjimka a návrat:** Zrušení přehledu nepotvrdí nový termín. Vybrané datum se nesmí zaměnit s rokem nebo měsícem, který má právě fokus.

**Nevhodně:** Samotnou změnou období neodeslat formulář ani automaticky nepotvrdit den.

### Web — rezervace služby

**Situace a cíl:** Návštěvník vybírá začátek a konec rezervace.

**Volba a varianta:** PeriodView zrychluje změnu období; sám nepotvrzuje celý den jako CalendarDay. V průchodu se uplatní `view=month`.

**Průchod a výsledek:** Z hlavičky otevřete odpovídající přehled a zvolte „listopad 2026“. Kalendář přejde do vybraného období, kde uživatel teprve volí den.

**Výjimka a návrat:** Zrušení přehledu nepotvrdí nový termín. Vybrané datum se nesmí zaměnit s rokem nebo měsícem, který má právě fokus.

**Nevhodně:** Samotnou změnou období neodeslat formulář ani automaticky nepotvrdit den.

### Interní systém — směnový plán

**Situace a cíl:** Koordinátor upravuje časový úsek směny.

**Volba a varianta:** PeriodView zrychluje změnu období; sám nepotvrzuje celý den jako CalendarDay. V průchodu se uplatní `view=year`.

**Průchod a výsledek:** Z hlavičky otevřete odpovídající přehled a zvolte „rok 2026“. Kalendář přejde do vybraného období, kde uživatel teprve volí den.

**Výjimka a návrat:** Zrušení přehledu nepotvrdí nový termín. Vybrané datum se nesmí zaměnit s rokem nebo měsícem, který má právě fokus.

**Nevhodně:** Samotnou změnou období neodeslat formulář ani automaticky nepotvrdit den.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit formát data a času, názvy období a jazyk vysvětlení omezení a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené termíny, časové pásmo, přesnost a pravidla intervalu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2878-113)
