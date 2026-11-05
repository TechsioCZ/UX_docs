# LineItem

Řádek položky spojuje identitu produktu, cenu, množství a dostupné akce v košíku či rekapitulaci.

Cílem je spravovat nebo přečíst jednu přesně identifikovanou položku košíku či objednávky.

## Kdy použít

Pro přečtení nebo povolenou úpravu jedné položky košíku či objednávky. Množství, cena, jednotka i chyba patří stejnému řádku. Čtení řádku neodesílá celou objednávku.

## Kdy zvolit alternativu

Pro nabídku před vložením do košíku použijte ProductCard, pro celkový součet TotalsSummary.

## Anatomie, stavy a varianty

Přesná identita jedné položky a dodané části Image, Price, Quantity, Actions a Feedback podle potřeby. ReadOnly nahradí změnovou skladbu čitelnými údaji.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `layout=default` | Vodorovná karta pro prostor, kde vedle sebe zůstanou čitelné identita, cena a akce. |
| `layout=compact` | Vodorovná karta pro prostor, kde vedle sebe zůstanou čitelné identita, cena a akce. |
| `readOnly=false` | Pro použití se skutečně dostupnými změnovými ovladači; oprávnění a uložení řídí aplikace. |
| `readOnly=true` | Pro čtení položky: množství je textové a změnové akce nejsou nabízené. |
| `pending=false` | Po dokončení příslušného přepočtu nebo před jeho zahájením; částky musí odpovídat svému potvrzenému kontextu. |
| `pending=true` | Během přepočtu: zachovat zobrazené částky, pojmenovat čekání a omezit související potvrzení. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Změnit povolené množství nebo odebrat konkrétní položku samostatnou akcí.
- Zobrazit cenu, jednotku a zpětnou vazbu ke stejné položce.

### Co vyvolávat nemá

- Nezaměňovat změnu řádku za potvrzení celé objednávky.
- Neznemožnit odebrání jen proto, že produkt už není dostupný.

### Přechody a odpovědnost

Povolená změna množství či odebrání se vztahuje jen k tomuto řádku. Aplikace oddělí draft, pending a potvrzenou změnu včetně ceny a souhrnu. Chyba ponechá rozpoznatelný původní stav a nápravu u stejné položky. ReadOnly zobrazí množství textově a nenabízí změnové akce; samotná nedostupnost zboží není důvod skrýt oprávněné odebrání.

### Konkrétní pravidla použití

- Název a varianta určují přesnou položku.
- Cena a jednotka odpovídají množství stejného řádku.
- Readonly nahrazuje vstup množství textem a skrývá akce.
- Pending zachovává zobrazené částky; výpočty a uložení řídí aplikace.
- Chybu přiřaďte dotčenému řádku. Nedostupnost produktu nemá automaticky znemožnit jeho odebrání.
- Image, Price, Quantity, Actions a Feedback jsou dodané obsahové části; jejich přeskupení zachovává identitu stejné položky.
- Pro čekání dodejte srozumitelný pendingLabel, který neprezentuje staré částky jako nově potvrzený přepočet.

## Obsah a pojmenování

Názvy údajů, částky nebo množství vztahujte ke stejné položce a jednotce. Měna či balení nezmizí při zkrácení. Ukázkové číslo z příkladu není výchozí hodnota ani limit projektu; jeho zdroj a přesnost určuje aplikace.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nezaměňovat změnu řádku za potvrzení celé objednávky.

### ERP — nákupní požadavek

**Situace a cíl:** Pracovník upravuje jeden řádek připravované objednávky materiálu.

**Volba a varianta:** Obsah „3 balení těsnění T-40“ je jedna konkrétní položka se svou jednotkou a cenou, nikoli potvrzení celé objednávky. V průchodu se uplatní `layout=default`, `readOnly=false`, `pending=false`.

**Průchod a výsledek:** Pro objekt „3 balení těsnění T-40“ použijte pojmenování „Těsnění T-40“. Množství, cena a případná zpětná vazba patří stejnému řádku. Změna množství neodesílá celou objednávku a odebrání zasahuje pouze tuto položku. Pro čisté čtení zvolte readOnly=true; v tomto režimu se nenabízí změnové akce.

**Výjimka a návrat:** Při chybě přepočtu se nezmění sousední řádek a nový součet se nepředstírá jako potvrzený.

### Web — košík

**Situace a cíl:** Zákazník chce odebrat nedostupný produkt z košíku.

**Volba a varianta:** Obsah „1 kus V18 s kufrem“ je jedna konkrétní položka se svou jednotkou a cenou, nikoli potvrzení celé objednávky. V průchodu se uplatní `layout=default`, `readOnly=false`, `pending=false`.

**Průchod a výsledek:** Pro objekt „1 kus V18 s kufrem“ použijte pojmenování „Vrtačka V18“. Množství, cena a případná zpětná vazba patří stejnému řádku. Změna množství neodesílá celou objednávku a odebrání zasahuje pouze tuto položku. Pro čisté čtení zvolte readOnly=true; v tomto režimu se nenabízí změnové akce.

**Výjimka a návrat:** Nedostupnost produktu nesmí automaticky zablokovat také možnost jeho odebrání.

### Interní systém — portál služeb

**Situace a cíl:** Zaměstnanec čte již odeslaný požadavek v režimu readonly.

**Volba a varianta:** Obsah „2 sady příslušenství“ je jedna konkrétní položka se svou jednotkou a cenou, nikoli potvrzení celé objednávky. V průchodu se uplatní `layout=default`, `readOnly=true`, `pending=false`.

**Průchod a výsledek:** Pro objekt „2 sady příslušenství“ použijte pojmenování „Servisní sada“. Množství, cena a případná zpětná vazba patří stejnému řádku. Změna množství neodesílá celou objednávku a odebrání zasahuje pouze tuto položku. Pro čisté čtení zvolte readOnly=true; v tomto režimu se nenabízí změnové akce.

**Výjimka a návrat:** Pending ponechá dříve zobrazené částky s vysvětlením; komponenta sama ceny nepřepočítává.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii názvu, ceny, jednotek a řádkových akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu položky, výpočty, dostupnost a pravidla ukládání změn. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3900-594)
