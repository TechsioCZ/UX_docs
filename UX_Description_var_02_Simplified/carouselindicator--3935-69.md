# CarouselIndicator

Pojmenovaný indikátor Carousel umožňuje zvolit jeden konkrétní snímek a označuje právě zobrazenou pozici.

**Vazba:** Carousel. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Pro přímý přechod na konkrétní existující snímek v Carousel. Zdroj definuje ovládací plochu 24 × 24 px kolem tečky 8 px; tento díl není jen dekorativní značka. Indikátor patří konkrétnímu existujícímu snímku.

## Kdy zvolit alternativu

Pro postup o jeden snímek použijte CarouselControl. Pokud nelze jednotlivé pozice smysluplně zpřístupnit, neslibujte pouhou dekorativní tečkou možnost přímé volby.

## Anatomie, stavy a varianty

Součást skladby **Carousel**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=active` | Označuje skutečně zobrazený snímek Carousel. |

Tečka je uvnitř jednoho klávesnicově dosažitelného, pojmenovaného ovladače. Rozměr masteru je popis zdroje; vhodnost cílové plochy je nutné posoudit v konkrétním prostředí. Význam active je aktuální snímek, nikoli fokus.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zobrazit konkrétní existující snímek aktivací jeho pojmenovaného indikátoru.

### Co vyvolávat nemá

- Nezaměnit hover za aktuální snímek a neprovést jinou akci nad produktem.

### Přechody a odpovědnost

Aktivace pojmenovaného bodu požádá Carousel o zobrazení jeho snímku. Active se přepne spolu se skutečně zobrazeným snímkem; hover ani fokus jej nepřepínají. Na stejném bodu nesmí vzniknout druhý ovladač uvnitř tlačítka. Změnu indexu řídí Carousel, ne samostatná kresba tečky.

### Konkrétní pravidla použití

- Indikátor patří konkrétnímu existujícímu snímku.
- Aktuální značka musí odpovídat zobrazené položce, nikoli pouze fokusu.
- Viditelná tečka a plocha pro její aktivaci mají různou velikost; malý symbol nemá zmenšit ovládací cíl.

## Obsah a pojmenování

Každý bod pojmenujte cílovou pozicí a skutečným počtem, například „Zobrazit snímek 2 z 5“. Je-li užitečný význam snímku, doplňte jej, například „Detail štítku“. Aktuální pozice je dostupná i bez rozlišení barvy.

## Přístupnost a prostředí

Přímý výběr snímku funguje klávesnicí i ukazatelem a má viditelný fokus. Samotná tečka nepřidává druhou zastávku uvnitř téhož ovladače. Změna snímku nevytrhne fokus z aktivovaného bodu a neprovede jiný příkaz. Při delších názvech či změně počtu snímků zůstává pořadí srozumitelné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Bod slouží přímé volbě konkrétního snímku; předchozí/další řeší CarouselControl. V průchodu se uplatní `state=default`.

- **Společné výjimky a návrat:** Počet 5 je modelový, musí souhlasit se skutečným počtem snímků. Při odstranění snímku upravte pořadí i názvy; bez aktivace nepřepínejte snímek.

- **Nevhodné použití:** Vytvořit jen dekorativní tečku bez dostupného tlačítka nebo dvě fokusovatelné vrstvy pro tentýž bod.

### ERP — katalog zařízení

**Situace a cíl:** Pracovník porovnává pohledy na vybírané zařízení.

**Průchod a výsledek:** U sekvence „Fotografie zařízení“ pojmenujte bod například „Zobrazit snímek 2 z 5“. Aktivace ovladače zobrazí druhý snímek a společně aktualizuje active; přechod fokusu jen zpřístupní ovládání.

### Web — produktová prezentace

**Situace a cíl:** Návštěvník chce vidět více situací použití produktu.

**Průchod a výsledek:** U sekvence „Ukázky použití“ pojmenujte bod například „Zobrazit snímek 2 z 5“. Aktivace ovladače zobrazí druhý snímek a společně aktualizuje active; přechod fokusu jen zpřístupní ovládání.

### Interní systém — výuková knihovna

**Situace a cíl:** Pracovník prochází související obrázkové instrukce.

**Průchod a výsledek:** U sekvence „Ukázky nastavení“ pojmenujte bod například „Zobrazit snímek 2 z 5“. Aktivace ovladače zobrazí druhý snímek a společně aktualizuje active; přechod fokusu jen zpřístupní ovládání.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit povolený styl prezentace, práci s pohybem a význam případného zvýraznění obsahu a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí pořadí snímků, krajní chování sekvence a případné přehrávání. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3935-69)
