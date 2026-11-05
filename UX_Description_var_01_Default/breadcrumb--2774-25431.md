# Breadcrumb

Drobečková navigace ukazuje polohu stránky v hierarchii a cestu k nadřazeným místům.

Cílem je porozumět poloze stránky v hierarchii a vrátit se k nadřazenému obsahu.

## Kdy použít

Pro polohu stránky ve skutečné hierarchii a návrat k jejím předkům. Aktuální místo zůstává rozpoznatelné i při zkrácení. Historii návštěv řeší Zpět; pracovní etapy Steps.

## Kdy zvolit alternativu

Pro postup etapami úkolu použijte Steps.

## Anatomie, stavy a varianty

Posloupnost předků a aktuálního místa, oddělovače a při zkrácení také ovladač skrytých úrovní. Oddělovač není navigační cíl.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít skutečného předka aktuální stránky.
- Při zkrácení cesty zpřístupnit vynechané části určeným ovladačem.

### Co vyvolávat nemá

- Nenahrazovat historii tlačítka Zpět ani průběh rozpracovaného procesu.
- Neskrývat současně počátek i aktuální místo.

### Přechody a odpovědnost

Aktivace konkrétního odkazu otevře jeho pojmenovaný cíl; teprve skutečně zobrazená stránka určuje current. Otevření navigační větve nebo rámu není přechod na stránku. Zrušení panelu ponechá původní pracovní kontext a vyřeší návrat fokusu. Nedostupný cíl aplikace vysvětlí a nabídne návrat; navigace nesmí skrytě měnit obchodní data ani zahodit neuložený draft bez určeného postupu.

### Konkrétní pravidla použití

- Názvy odpovídají skutečným cílům.
- Aktuální stránku odlište od odkazů na nadřazené úrovně.
- Při zkrácení cesty zachovejte přístup ke skrytým úrovním.
- Výpustka představuje vynechané úrovně, nikoli další stránku.
- MaxItems zachovává první a závěrečné položky cesty; výpustka zastupuje vynechané prostřední úrovně.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — detail objednávky

**Situace a cíl:** Pracovník otevřel objednávku z oddělení nákupu.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Nákup / Objednávky / O-1048“. Cesta ukazuje skutečné předky, nikoli historii Zpět. V průchodu se uplatní `size=sm`.

**Průchod a výsledek:** Pro objekt „Objednávka O-1048“ použijte pojmenování „Nákup / Objednávky / O-1048“. Předkové jsou skutečné pojmenované cíle a poslední položka určuje nynější místo. Při zkrácení zůstane počátek a konec cesty dostupný; zkracovací ovladač zpřístupní vynechané předky. Nejde o tlačítko systémové historie.

**Výjimka a návrat:** Stejný záznam otevřený z hledání nemění své předky jen podle posledního kliknutí.

**Nevhodně:** Nenahrazovat historii tlačítka Zpět ani průběh rozpracovaného procesu.

### Web — produktový katalog

**Situace a cíl:** Návštěvník potřebuje širší kategorii než aktuální detail.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Nářadí / Vrtačky / V18“. Cesta ukazuje skutečné předky, nikoli historii Zpět. V průchodu se uplatní `size=sm`.

**Průchod a výsledek:** Pro objekt „Aku vrtačka V18“ použijte pojmenování „Nářadí / Vrtačky / V18“. Předkové jsou skutečné pojmenované cíle a poslední položka určuje nynější místo. Při zkrácení zůstane počátek a konec cesty dostupný; zkracovací ovladač zpřístupní vynechané předky. Nejde o tlačítko systémové historie.

**Výjimka a návrat:** Dlouhá cesta se zkrátí při zachování začátku a koncových položek; vynechané části zůstávají dostupné.

**Nevhodně:** Nenahrazovat historii tlačítka Zpět ani průběh rozpracovaného procesu.

### Interní systém — dokumentový archiv DMS

**Situace a cíl:** Uživatel se orientuje v několika úrovních složek.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Projekty / Orion / Smlouvy“. Cesta ukazuje skutečné předky, nikoli historii Zpět. V průchodu se uplatní `size=sm`.

**Průchod a výsledek:** Pro objekt „Smlouvy projektu Orion“ použijte pojmenování „Projekty / Orion / Smlouvy“. Předkové jsou skutečné pojmenované cíle a poslední položka určuje nynější místo. Při zkrácení zůstane počátek a konec cesty dostupný; zkracovací ovladač zpřístupní vynechané předky. Nejde o tlačítko systémové historie.

**Výjimka a návrat:** Breadcrumb nesmí tvrdit, že rozpracovaná smlouva byla uložená nebo schválená.

**Nevhodně:** Nenahrazovat historii tlačítka Zpět ani průběh rozpracovaného procesu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy úrovní a způsob zkracování dlouhé navigační cesty a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí skutečnou hierarchii, cílové adresy a zachování rozpracovaných dat při přechodu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-25431)
