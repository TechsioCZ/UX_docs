# Drawer.Sheet

Horní nebo dolní výsuvný panel zpřístupňuje související obsah; výškové režimy a snap musí zachovat dostupnost akcí.

Cílem je provést kontextový úkol v okrajovém panelu při zachování vztahu k hlavnímu obsahu.

## Kdy použít

Pro související detail nebo vedlejší pracovní úkol se zachovaným kontextem hlavní stránky. Boční panel řeší Drawer.Side, horní či dolní Drawer.Sheet. Dlouhý samostatný proces otevřete na vlastní stránce.

## Kdy zvolit alternativu

Pro trvalý navigační rám použijte Sidebar, pro samostatné soustředěné rozhodnutí Dialog.

## Anatomie, stavy a varianty

Side nebo Sheet určují osu a okraj panelu. Header obsahuje Title a případný Description, Body pracovní obsah a Footer závěrečné akce; Grabber a GrabberIndicator se používají jen pro odpovídající polohování.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `placement=bottom` | Polohu bottom volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `placement=top` | Polohu top volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=xs` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `size=xl` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `size=full` | Plný dostupný rozměr příslušné osy: u Drawer.Side šířka, u Drawer.Sheet výška; důležité ovladače zůstanou dosažitelné. |
| `dir=ltr` | Pro levopravý jazyk a odpovídající logické směry. |
| `dir=rtl` | Pro pravolevý jazyk; obrátit logické uspořádání a odpovídající směrové značky, ne význam akcí. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít související detail nebo formulář, upravit obsah a panel určeným způsobem zavřít.
- U pohyblivého panelu nabídnout alternativu k tažení.

### Co vyvolávat nemá

- Nezaměňovat posun panelu za uložení obsahu.
- Nepřebírat starší Drawer/Side a Drawer/Edge jako automatické aliasy nových komponent.

### Přechody a odpovědnost

Spouštěč otevře vrstvu a předá fokus do jejího úkolu. Potvrzení je samostatná pojmenovaná akce; neúspěch ponechá potřebná data i vysvětlení. Zrušení či zavření nepotvrzuje změny a musí respektovat určenou politiku rozepsaných dat. Po zavření se fokus vrátí do logického místa; modální režim omezuje práci na pozadí, nemodální ji nesmí bezdůvodně blokovat.

### Konkrétní pravidla použití

- Snap mění polohu panelu; obsah se automaticky nepřepočítává do menší výšky.
- I při snížené poloze zachovejte dosažitelnost důležitých akcí.
- Tažení doplňte dostupným způsobem stejného výsledku.
- Starší Drawer/Edge není automatickým aliasem této komponenty.
- U modálního použití omezte práci na pozadí a udržte fokus v panelu; po zavření jej obnovte v odpovídajícím místě.
- Full vyplní dostupnou výšku. Snížená snap poloha sama nepřisune patičku do viditelné oblasti.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

U interaktivní vrstvy určete počáteční fokus, dostupné zavření a logický návrat. Modální použití drží fokus uvnitř, nemodální ho nesmí bezdůvodně uvěznit. Na malé obrazovce a při dlouhém obsahu zůstanou dosažitelné důležité akce i konec úkolu.

## Omezení a příklady podle typu projektu

### ERP — související detail objednávky

**Situace a cíl:** Pracovník potřebuje upravit údaje vybraného řádku a vidět kontext přehledu.

**Volba a varianta:** Úkol „Upravit objednávku O-1048“ potřebuje pracovní detail při zachování vztahu k hlavní stránce; samostatná stránka by změnila tento způsob práce. V průchodu se uplatní `placement=bottom`.

**Průchod a výsledek:** Pro objekt „Objednávka O-1048“ použijte pojmenování „Upravit objednávku O-1048“. Krok „Uložit změny v panelu“ má vlastní potvrzovací ovladač; zavření vrstvy je samostatný výsledek. Určete počáteční fokus a dostupnou cestu zpět. U modálního použití nepřipusťte ovládání překrytého pozadí; při neúspěchu ponechte potřebný obsah k opravě a nepředstírejte hotový výsledek.

**Výjimka a návrat:** Zavření panelu se změněnými údaji nesmí působit jako úspěšné uložení, pokud nic uloženo nebylo. Přepnutí či zavření samo neukládá rozepsaný formulář; návrat a zachování dat musí odpovídat určenému průchodu.

**Nevhodně:** Nezaměňovat posun panelu za uložení obsahu.

### Web — mobilní filtrování katalogu

**Situace a cíl:** Návštěvník nastavuje filtry v panelu od okraje obrazovky.

**Volba a varianta:** Úkol „Filtrovat produkty“ potřebuje pracovní detail při zachování vztahu k hlavní stránce; samostatná stránka by změnila tento způsob práce. V průchodu se uplatní `placement=bottom`.

**Průchod a výsledek:** Pro objekt „Dostupnost a cenové rozpětí“ použijte pojmenování „Filtrovat produkty“. Krok „Použít filtry“ má vlastní potvrzovací ovladač; zavření vrstvy je samostatný výsledek. Určete počáteční fokus a dostupnou cestu zpět. U modálního použití nepřipusťte ovládání překrytého pozadí; při neúspěchu ponechte potřebný obsah k opravě a nepředstírejte hotový výsledek.

**Výjimka a návrat:** Ani snížený snap nesmí znemožnit dosažení akce Použít a zavření panelu. Přepnutí či zavření samo neukládá rozepsaný formulář; návrat a zachování dat musí odpovídat určenému průchodu.

**Nevhodně:** Nezaměňovat posun panelu za uložení obsahu.

### Interní systém — pracovní detail incidentu

**Situace a cíl:** Řešitel otevře z přehledu vedlejší úkol k incidentu.

**Volba a varianta:** Úkol „Incident INC-142“ potřebuje pracovní detail při zachování vztahu k hlavní stránce; samostatná stránka by změnila tento způsob práce. V průchodu se uplatní `placement=bottom`.

**Průchod a výsledek:** Pro objekt „Podrobnosti incidentu“ použijte pojmenování „Incident INC-142“. Krok „Aktualizovat incident“ má vlastní potvrzovací ovladač; zavření vrstvy je samostatný výsledek. Určete počáteční fokus a dostupnou cestu zpět. U modálního použití nepřipusťte ovládání překrytého pozadí; při neúspěchu ponechte potřebný obsah k opravě a nepředstírejte hotový výsledek.

**Výjimka a návrat:** Je-li použit modálně, fokus nesmí zůstat v překrytém seznamu; nemodální režim se určí samostatně. Přepnutí či zavření samo neukládá rozepsaný formulář; návrat a zachování dat musí odpovídat určenému průchodu.

**Nevhodně:** Nezaměňovat posun panelu za uložení obsahu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit logickou stranu panelu, hierarchii jeho textů a prioritu závěrečných akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí modalitu konkrétního použití, ukládání, výchozí velikost a zachování rozpracovaného obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3039-604)
