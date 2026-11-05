# ProductCardBadges

Skupina štítků ProductCard doplňuje krátké vlastnosti konkrétní nabídky.

**Vazba:** ProductCard. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Štítky vyjadřují vlastnosti právě zobrazené nabídky. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě ProductCard. Štítky vyjadřují vlastnosti právě zobrazené nabídky.

## Kdy zvolit alternativu

Pro jednu jednoduchou vlastnost lze použít samotný Badge. Pro cenu či dostupnost použijte jejich vlastní části; další štítek je nenahrazuje.

## Anatomie, stavy a varianty

Součást skladby **ProductCard**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Štítky vyjadřují vlastnosti právě zobrazené nabídky.
- Držte je stručné a nezaměňujte je s hlavní nákupní akcí.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Samotná oblast nepřebírá jména a akce svých ovladačů. Vnořené odkazy a tlačítka mají vlastní názvy a logické pořadí. Při menší šířce zůstává dosažitelný celý podstatný obsah, nikoli jen první viditelná část.

## Omezení a příklady podle typu projektu

### ERP — interní katalog materiálu

**Situace a cíl:** Pracovník vybírá konkrétní položku pro nákupní požadavek.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Štítky vyjadřují vlastnosti právě zobrazené nabídky. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Sestavte oblast „Aku vrtačka V18“ s obsahem „Novinka; pouze celá balení“. Držte je stručné a nezaměňujte je s hlavní nákupní akcí. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Web — e-shop

**Situace a cíl:** Zákazník porovnává nabídky a přidává dostupný produkt do košíku.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Štítky vyjadřují vlastnosti právě zobrazené nabídky. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Sestavte oblast „Aku vrtačka V18“ s obsahem „Novinka“. Držte je stručné a nezaměňujte je s hlavní nákupní akcí. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Interní systém — portál vybavení

**Situace a cíl:** Zaměstnanec vybírá zařízení ze schváleného katalogu.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Štítky vyjadřují vlastnosti právě zobrazené nabídky. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Sestavte oblast „Monitor M27“ s obsahem „Doporučené vybavení“. Držte je stručné a nezaměňujte je s hlavní nákupní akcí. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii produktových informací, slovník obchodních štítků a prioritu nákupních akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu nabídky, cenu, skladová data, oprávnění k nákupu a výsledek operace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26973)
