# Combobox/Content

Obsah Combobox zobrazuje možnosti odpovídající dotazu nebo doložený prázdný výsledek.

**Vazba:** Combobox. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Zobrazujte možnosti odpovídající aktuálnímu dotazu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Combobox. Zobrazujte možnosti odpovídající aktuálnímu dotazu.

## Kdy zvolit alternativu

Pokud seznam nevyžaduje hledání, postačí Select. Pro příkazy použijte Command či Menu, nikoli potvrzování datové hodnoty.

## Anatomie, stavy a varianty

Součást skladby **Combobox**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=options` | Když jsou pro aktuální dotaz dostupné odpovídající možnosti. Jejich zobrazení ještě nepotvrzuje hodnotu. |
| `state=empty` | Při úspěšném získání možností či výsledků bez shody. Selhání služby vyžaduje jiné vysvětlení. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Zobrazujte možnosti odpovídající aktuálnímu dotazu.
- Nulová shoda má jiný význam než chyba získání dat; nabídka sama nepotvrzuje hodnotu.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Samotná oblast nepřebírá jména a akce svých ovladačů. Vnořené odkazy a tlačítka mají vlastní názvy a logické pořadí. Při menší šířce zůstává dosažitelný celý podstatný obsah, nikoli jen první viditelná část.

## Omezení a příklady podle typu projektu

### ERP — výběr dodavatele

**Situace a cíl:** Pracovník hledá existujícího dodavatele podle části názvu.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Zobrazujte možnosti odpovídající aktuálnímu dotazu. V průchodu se uplatní `state=options`.

**Průchod a výsledek:** Sestavte oblast „Dodavatel“ s obsahem „Technika Znojmo, D-208“. Nulová shoda má jiný význam než chyba získání dat; nabídka sama nepotvrzuje hodnotu. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Web — výběr výdejního místa

**Situace a cíl:** Zákazník hledá místo zadáním města.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Zobrazujte možnosti odpovídající aktuálnímu dotazu. V průchodu se uplatní `state=options`.

**Průchod a výsledek:** Sestavte oblast „Výdejní místo“ s obsahem „Znojmo, Centrum“. Nulová shoda má jiný význam než chyba získání dat; nabídka sama nepotvrzuje hodnotu. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Interní systém — přiřazení řešitele

**Situace a cíl:** Koordinátor vyhledává člena týmu pro incident.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Zobrazujte možnosti odpovídající aktuálnímu dotazu. V průchodu se uplatní `state=options`.

**Průchod a výsledek:** Sestavte oblast „Řešitel“ s obsahem „Jana Nováková, tým Podpora“. Nulová shoda má jiný význam než chyba získání dat; nabídka sama nepotvrzuje hodnotu. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník hledání, zápis výsledků a styl validační zpětné vazby a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj možností, povinnost údaje a pravidla případného vzdáleného hledání. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-36544)
