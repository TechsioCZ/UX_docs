# DatePicker/Content

Kalendářní panel DatePicker nese výběr data a podle režimu související časové ovládání.

**Vazba:** DatePicker. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Panel patří příslušnému datumovému poli. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě DatePicker. Panel patří příslušnému datumovému poli.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v DatePicker a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **DatePicker**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `selectionMode=single` | Pro výběr jednoho data; neprezentovat jej jako celý interval. |
| `selectionMode=range` | Pro interval se zřetelným začátkem a koncem; neúplnost se vyhodnotí podle procesu. |
| `granularity=day` | Když uživatelský úkol potřebuje datum bez časové přesnosti. |
| `granularity=minute` | Když uživatelský úkol vyžaduje minuty při zachovaném datu. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Panel patří příslušnému datumovému poli.
- Rozložení odpovídá single/range a zvolené přesnosti; při časovém režimu zachovejte potvrzení a zrušení draftu.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Samotná oblast nepřebírá jména a akce svých ovladačů. Vnořené odkazy a tlačítka mají vlastní názvy a logické pořadí. Při menší šířce zůstává dosažitelný celý podstatný obsah, nikoli jen první viditelná část.

## Omezení a příklady podle typu projektu

### ERP — plánování dodávky

**Situace a cíl:** Pracovník mění termín dodání konkrétní objednávky.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Panel patří příslušnému datumovému poli. V průchodu se uplatní `selectionMode=single`, `granularity=minute`.

**Průchod a výsledek:** Sestavte oblast „Termín dodání“ s obsahem „12. 11. 2026, 08:30“. Rozložení odpovídá single/range a zvolené přesnosti; při časovém režimu zachovejte potvrzení a zrušení draftu. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Web — rezervace služby

**Situace a cíl:** Návštěvník vybírá začátek a konec rezervace.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Panel patří příslušnému datumovému poli. V průchodu se uplatní `selectionMode=range`, `granularity=day`.

**Průchod a výsledek:** Sestavte oblast „Termín rezervace“ s obsahem „12.–14. 11. 2026“. Rozložení odpovídá single/range a zvolené přesnosti; při časovém režimu zachovejte potvrzení a zrušení draftu. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Interní systém — směnový plán

**Situace a cíl:** Koordinátor upravuje časový úsek směny.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Panel patří příslušnému datumovému poli. V průchodu se uplatní `selectionMode=range`, `granularity=minute`.

**Průchod a výsledek:** Sestavte oblast „Čas směny“ s obsahem „12. 11. 2026, 08:30–16:00“. Rozložení odpovídá single/range a zvolené přesnosti; při časovém režimu zachovejte potvrzení a zrušení draftu. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit formát data a času, názvy období a jazyk vysvětlení omezení a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené termíny, časové pásmo, přesnost a pravidla intervalu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2879-792)
