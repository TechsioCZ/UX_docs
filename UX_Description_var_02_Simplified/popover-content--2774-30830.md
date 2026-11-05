# Popover/Content

Obsah Popover skládá titulek, vysvětlení, tělo a případné zavření lokálního panelu.

**Vazba:** Popover. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Titulek, popis, tělo a close patří témuž lokálnímu úkolu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Popover. Titulek, popis, tělo a close patří témuž lokálnímu úkolu.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v Popover a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

**Omezení konfigurace:** Popover/Content má ve zdroji duplicitní kombinace variant. Před použitím konkrétní konfigurace je nutné určit odpovídající master; podobný název sám není spolehlivý výběrový klíč.

Součást skladby **Popover**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `showTitle=true` | Když panel potřebuje viditelný titulek svého úkolu. |
| `showTitle=false` | Jen pokud je účel i přístupné pojmenování panelu zajištěné jinak. |
| `showDescription=true` | Když vysvětlení doplňuje úkol či důsledek, který titulek neobjasní. |
| `showDescription=false` | Když je význam již srozumitelný bez redundantního vysvětlení. |
| `showCloseButton=true` | Pro viditelnou a pojmenovanou možnost zavření. |
| `showCloseButton=false` | Jen pokud je nadále dostupný srozumitelný způsob ukončení; nesmí vzniknout past. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Spouštěč otevře vrstvu a předá fokus do jejího úkolu. Potvrzení je samostatná pojmenovaná akce; neúspěch ponechá potřebná data i vysvětlení. Zrušení či zavření nepotvrzuje změny a musí respektovat určenou politiku rozepsaných dat. Po zavření se fokus vrátí do logického místa; modální režim omezuje práci na pozadí, nemodální ji nesmí bezdůvodně blokovat.

### Konkrétní pravidla použití

- Titulek, popis, tělo a close patří témuž lokálnímu úkolu.
- Při skrytém titulku nebo close zachovejte pojmenování a dostupné zavření.
- Aktuální sada obsahuje duplicitní konfiguraci; nespoléhejte na jednoznačný výběr podle vlastností.
- Interaktivní obsah musí zůstat ovladatelný bez myši; přesun a návrat fokusu patří jeho konkrétnímu režimu panelu.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

U interaktivní vrstvy určete počáteční fokus, dostupné zavření a logický návrat. Modální použití drží fokus uvnitř, nemodální ho nesmí bezdůvodně uvěznit. Na malé obrazovce a při dlouhém obsahu zůstanou dosažitelné důležité akce i konec úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Titulek, popis, tělo a close patří témuž lokálnímu úkolu. V průchodu se uplatní `showTitle=true`, `showDescription=true`, `showCloseButton=true`.

- **Společné výjimky a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

- **Nevhodné použití:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### ERP — lokální filtr seznamu

**Situace a cíl:** Pracovník upravuje krátkou podmínku u konkrétního sloupce.

**Průchod a výsledek:** Sestavte oblast „Filtrovat datum dodání“ s obsahem „Podmínka termínu dodání“. Při skrytém titulku nebo close zachovejte pojmenování a dostupné zavření. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Web — informace o variantě

**Situace a cíl:** Návštěvník otevírá stručný doplněk u vybrané nabídky.

**Průchod a výsledek:** Sestavte oblast „Podrobnosti varianty“ s obsahem „Vrtačka s kufrem“. Při skrytém titulku nebo close zachovejte pojmenování a dostupné zavření. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

### Interní systém — výběr členů

**Situace a cíl:** Koordinátor doplňuje krátký výběr u pracovní položky.

**Průchod a výsledek:** Sestavte oblast „Přiřadit členy“ s obsahem „Úkol U-58“. Při skrytém titulku nebo close zachovejte pojmenování a dostupné zavření. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii nadpisu, podobu lokálních vrstev a pojmenování jejich akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí obsah úkolu, zacházení s rozepsanými změnami a chování při kolizi s okrajem. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-30830)
