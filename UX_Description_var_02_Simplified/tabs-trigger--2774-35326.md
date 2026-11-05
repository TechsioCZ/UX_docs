# Tabs.Trigger

Záložka Tabs vybírá související obsahový panel a odlišuje jeho aktivní stav od pouhého fokusu.

**Vazba:** Tabs. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Záložka vybírá svůj odpovídající panel. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Tabs. Záložka vybírá svůj odpovídající panel.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v Tabs a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **Tabs**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `variant=default` | Vizuální provedení default podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `variant=line` | Vizuální provedení line podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `variant=solid` | Vizuální provedení solid podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `variant=outline` | Vizuální provedení outline podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=selected` | Pro skutečně potvrzenou vybranou položku. Hover ani pouhý fokus ji nenahrazují. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Aktivovat přiřazený panel podle jednotného modelu celé sady.

### Co vyvolávat nemá

- Nespouštět nevratnou operaci, neaktivovat disabled panel a nezaměnit fokus za selected.

### Přechody a odpovědnost

Vybraná záložka a viditelný panel souhlasí. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Záložka vybírá svůj odpovídající panel.
- Fokus není automaticky potvrzený výběr; selected musí souhlasit se zobrazeným obsahem.
- Při potvrzovaném způsobu aktivace přepněte panel až potvrzením, nikoli jen přesunem fokusu; pravidlo musí být stejné v celé skupině.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Celá sada používá jeden doložený model klávesnice. Při prodlevě načítání upřednostněte výslovnou aktivaci místo změny při každém fokusu; draft panelu se tiše nezahazuje.

- **Pravidlo použití:** Nespouštět nevratnou operaci, neaktivovat disabled panel a nezaměnit fokus za selected.

### ERP — detail zakázky

**Situace a cíl:** Pracovník přepíná mezi údaji stejné zakázky.

**Volba a varianta:** Trigger mění rovnocenný panel; pořadí povinných etap vyjadřuje Steps. V průchodu se uplatní `variant=default`, `state=default`.

**Průchod a výsledek:** U sady „Zakázka — Údaje / Položky“ aktivujte záložku jejího panelu. Selected a Tabs.Content se společně přepnou; změna pohledu nemění údaje objektu.

### Web — detail produktu

**Situace a cíl:** Návštěvník porovnává popis a technické parametry.

**Volba a varianta:** Trigger mění rovnocenný panel; pořadí povinných etap vyjadřuje Steps. V průchodu se uplatní `variant=default`, `state=selected`.

**Průchod a výsledek:** U sady „Popis / Parametry“ aktivujte záložku jejího panelu. Selected a Tabs.Content se společně přepnou; změna pohledu nemění údaje objektu.

### Interní systém — profil pracovníka

**Situace a cíl:** Uživatel prochází přehled různých druhů údajů o stejné osobě.

**Volba a varianta:** Trigger mění rovnocenný panel; pořadí povinných etap vyjadřuje Steps. V průchodu se uplatní `variant=default`, `state=default`.

**Průchod a výsledek:** U sady „Profil / Oprávnění“ aktivujte záložku jejího panelu. Selected a Tabs.Content se společně přepnou; změna pohledu nemění údaje objektu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy panelů, vizuální vzhled záložek a hierarchii vybraného stavu a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí uchování rozepsaných hodnot, načítání a automatickou či potvrzovanou aktivaci. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-35326)
