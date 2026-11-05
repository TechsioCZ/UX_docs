# TotalsSummary

Souhrn částek zobrazuje dodané položky rozpisu a celkovou nebo mezisoučtovou hodnotu.

Cílem je porozumět rozpisu částek a skutečně potvrzenému celku.

## Kdy použít

Pro související rozpis a celkovou částku dodané stejným výpočtem aplikace. Musí být zřejmé, co součet zahrnuje a co ještě čeká na přepočet. Jednu cenu nabídky zobrazuje PriceBlock.

## Kdy zvolit alternativu

Pro cenu jednoho produktu použijte PriceBlock.

## Anatomie, stavy a varianty

Pojmenované řádky částek, jejich důraz a celek. Nepovinná poznámka objasňuje řádek; pending popisuje probíhající přepočet dodávaný aplikací.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `pending=false` | Po dokončení příslušného přepočtu nebo před jeho zahájením; částky musí odpovídat svému potvrzenému kontextu. |
| `pending=true` | Během přepočtu: zachovat zobrazené částky, pojmenovat čekání a omezit související potvrzení. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zobrazit srozumitelně pojmenované řádky a součet dodaný aplikací.
- Odlišit čekání na přepočet od potvrzených částek.

### Co vyvolávat nemá

- Komponenta sama částky nepočítá.
- Neznámé náklady nesmí vypadat jako potvrzená nula.

### Přechody a odpovědnost

Změna položek vyvolá přepočet aplikace a pending=true. Dosavadní částky zůstanou rozpoznatelné jako předchozí hodnoty, související konečné potvrzení se nevydává za platné. Úspěch současně aktualizuje rozpis i celek; chyba ukončí nejasné čekání vysvětlením a možností opakování. Komponenta částky sama nepočítá.

### Konkrétní pravidla použití

- Názvy řádků jednoznačně vysvětlí částky.
- Řádky i součet dodává aplikace; komponenta je sama nepočítá.
- Neznámou dopravu nevydávejte za nulovou cenu.
- Pending zachovává zobrazené hodnoty a blokuje související akce. Zpětnou vazbu čekání pojmenujte pendingLabel.

## Obsah a pojmenování

Názvy údajů, částky nebo množství vztahujte ke stejné položce a jednotce. Měna či balení nezmizí při zkrácení. Ukázkové číslo z příkladu není výchozí hodnota ani limit projektu; jeho zdroj a přesnost určuje aplikace.

## Přístupnost a prostředí

Informace je srozumitelná bez samotné barvy či symbolu a bez přidávání zbytečné zastávky fokusu. Důležitá změna výsledku nesmí být dostupná pouze jako krátké vizuální probliknutí. Text, měna, jednotka či zkratka odpovídají konkrétnímu prostředí a jazyku.

## Omezení a příklady podle typu projektu

### ERP — nákupní požadavek

**Situace a cíl:** Pracovník kontroluje součet připravovaných položek.

**Volba a varianta:** Pro „Souhrn požadavku“ se sděluje rozpis i celek stejného výpočtu, nikoli jediná samostatná cena. V průchodu se uplatní `pending=false`.

**Průchod a výsledek:** Pro objekt „Položky a celkem“ použijte pojmenování „Souhrn požadavku“. Řádky i celek dodá stejný výpočet aplikace. Během změny přejděte na pending=true a pojmenujte čekání, zatímco zobrazené částky nejsou nové potvrzené údaje. Po výsledku vyjasněte platný součet nebo chybu; samotná komponenta přepočet neprovádí.

**Výjimka a návrat:** Při přepočtu pending nezaměňuje staré zobrazené částky za hotový nový celek.

**Nevhodně:** Komponenta sama částky nepočítá.

### Web — košík

**Situace a cíl:** Zákazník kontroluje cenu objednávaného obsahu včetně určených nákladů.

**Volba a varianta:** Pro „Souhrn košíku“ se sděluje rozpis i celek stejného výpočtu, nikoli jediná samostatná cena. V průchodu se uplatní `pending=false`.

**Průchod a výsledek:** Pro objekt „Zboží / Doprava / Celkem“ použijte pojmenování „Souhrn košíku“. Řádky i celek dodá stejný výpočet aplikace. Během změny přejděte na pending=true a pojmenujte čekání, zatímco zobrazené částky nejsou nové potvrzené údaje. Po výsledku vyjasněte platný součet nebo chybu; samotná komponenta přepočet neprovádí.

**Výjimka a návrat:** Dosud neurčená doprava nesmí tvrdit Doprava zdarma jen prázdnou nebo nulovou hodnotou.

**Nevhodně:** Komponenta sama částky nepočítá.

### Interní systém — objednávka služeb

**Situace a cíl:** Pracovník sleduje souhrn vybraných firemních služeb.

**Volba a varianta:** Pro „Rozpis služeb“ se sděluje rozpis i celek stejného výpočtu, nikoli jediná samostatná cena. V průchodu se uplatní `pending=false`.

**Průchod a výsledek:** Pro objekt „Služby / Úprava ceny / Celkem“ použijte pojmenování „Rozpis služeb“. Řádky i celek dodá stejný výpočet aplikace. Během změny přejděte na pending=true a pojmenujte čekání, zatímco zobrazené částky nejsou nové potvrzené údaje. Po výsledku vyjasněte platný součet nebo chybu; samotná komponenta přepočet neprovádí.

**Výjimka a návrat:** Zvýraznění discount nezavádí samostatný výpočet a při pending zůstane důvod omezení akce dostupný.

**Nevhodně:** Komponenta sama částky nepočítá.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy finančních řádků, měnový zápis a hierarchii celku a slev a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí výpočet, měnu, zdroj částek a blokování související akce při přepočtu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3899-92)
