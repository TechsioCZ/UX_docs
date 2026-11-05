# FooterLink

Odkaz Footer vede na konkrétní cíl z doplňující navigace v patičce.

**Vazba:** Footer. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Text pojmenuje skutečný cíl odkazu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Footer. Text pojmenuje skutečný cíl odkazu.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v Footer a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **Footer**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Přejít na skutečný pojmenovaný cíl odpovídající skupině patičky.

### Co vyvolávat nemá

- Neprovést změnu dat pouhým kliknutím na doplňující navigaci.

### Přechody a odpovědnost

Uživatel se dostane k informaci, kterou název odkazu slíbil. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Text pojmenuje skutečný cíl odkazu.
- Odkaz zařaďte do významově správné skupiny patičky.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Samotná oblast nepřebírá jména a akce svých ovladačů. Vnořené odkazy a tlačítka mají vlastní názvy a logické pořadí. Při menší šířce zůstává dosažitelný celý podstatný obsah, nikoli jen první viditelná část.

## Omezení a příklady podle typu projektu

### ERP — pracovní aplikace

**Situace a cíl:** Pracovník hledá doplňující informace o používaném systému.

**Volba a varianta:** Link slibuje konkrétní obsah; Button by byl vhodný pro příkaz, nikoli pro doplňující navigaci. V průchodu se uplatní `size=sm`.

**Průchod a výsledek:** Odkaz „Postup založení požadavku“ otevře přímo odpovídající návod nebo podmínky. Text předem objasňuje obsah cíle; samotná navigace neodesílá požadavek ani nemění objednávku.

**Výjimka a návrat:** Nedostupný cíl musí mít dostupné vysvětlení a návrat. Účet ani rozepsaná práce se nesmějí změnit pouhou aktivací doplňujícího odkazu.

**Nevhodně:** Neprovést změnu dat pouhým kliknutím na doplňující navigaci.

### Web — veřejná prezentace

**Situace a cíl:** Návštěvník hledá kontakty a doplňující informace.

**Volba a varianta:** Link slibuje konkrétní obsah; Button by byl vhodný pro příkaz, nikoli pro doplňující navigaci. V průchodu se uplatní `size=sm`.

**Průchod a výsledek:** Odkaz „Podmínky doručení“ otevře přímo odpovídající návod nebo podmínky. Text předem objasňuje obsah cíle; samotná navigace neodesílá požadavek ani nemění objednávku.

**Výjimka a návrat:** Nedostupný cíl musí mít dostupné vysvětlení a návrat. Účet ani rozepsaná práce se nesmějí změnit pouhou aktivací doplňujícího odkazu.

**Nevhodně:** Neprovést změnu dat pouhým kliknutím na doplňující navigaci.

### Interní systém — zaměstnanecký portál

**Situace a cíl:** Zaměstnanec chce otevřít návod k používání portálu.

**Volba a varianta:** Link slibuje konkrétní obsah; Button by byl vhodný pro příkaz, nikoli pro doplňující navigaci. V průchodu se uplatní `size=sm`.

**Průchod a výsledek:** Odkaz „Postup obnovení přístupu“ otevře přímo odpovídající návod nebo podmínky. Text předem objasňuje obsah cíle; samotná navigace neodesílá požadavek ani nemění objednávku.

**Výjimka a návrat:** Nedostupný cíl musí mít dostupné vysvětlení a návrat. Účet ani rozepsaná práce se nesmějí změnit pouhou aktivací doplňujícího odkazu.

**Nevhodně:** Neprovést změnu dat pouhým kliknutím na doplňující navigaci.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit skupiny doplňující navigace, povinné značkové informace a textovou identitu a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí aktuální cíle, kontaktní údaje a obsah potřebný pro daný produkt. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-38773)
