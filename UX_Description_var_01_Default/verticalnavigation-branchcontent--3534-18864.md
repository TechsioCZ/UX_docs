# VerticalNavigation/BranchContent

Obsah větve VerticalNavigation nese vnořené odkazy s vlastním tónem, odsazením a případným vodítkem.

**Vazba:** VerticalNavigation. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Obsahuje odkazy správné nadřazené větve. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě VerticalNavigation. Obsahuje odkazy správné nadřazené větve.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v VerticalNavigation a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **VerticalNavigation**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `tone=plain` | Když strukturu skupiny objasňuje nadpis a rozložení bez potřeby dalšího výrazného podkladu. |
| `tone=subtle` | Když je třeba jemně odlišit skupinu od okolí, aniž by převzala prioritu hlavního cíle. |
| `tone=accent` | Pro záměrně zvýrazněnou oblast podle pravidel značky; tón nesmí předstírat current, selected nebo chybu. |
| `variant=primary` | Vizuální provedení primary podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `variant=secondary` | Vizuální provedení secondary podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `indent=true` | Když odsazení odpovídá skutečné hierarchii. |
| `indent=false` | Pro skladbu, jejíž vztahy zůstávají čitelné bez tohoto odsazení. |
| `showGuide=false` | Bez čáry; vztah rodiče a potomků musí zůstat srozumitelný. |
| `showGuide=true` | Pro pomocné zobrazení hierarchické vodicí čáry. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Sestavit části této oblasti podle konkrétních pravidel níže; vlastní ovladače obsahu zůstávají oddělené.

### Co vyvolávat nemá

- Nepřevzít aktivaci vnořeného ovladače jako další nesouvisející akci celého obalu.

### Přechody a odpovědnost

Změnu vyvolává konkrétní vnořený ovladač nebo změna dat hostitele. Obal zachová vztah názvu, obsahu a daného objektu; neprovádí další skrytou akci při události potomka. Po zavření či skrytí nesmí uvnitř zůstat nedosažitelný fokus ani jediná cesta k dokončení úkolu.

### Konkrétní pravidla použití

- Obsahuje odkazy správné nadřazené větve.
- Tone, odsazení a guide pomáhají číst hierarchii; neurčují aktuální stránku.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

### ERP — navigace nákupní agendy

**Situace a cíl:** Pracovník chce z detailu objednávky přejít do přehledu dodavatelů.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Obsahuje odkazy správné nadřazené větve. V průchodu se uplatní `tone=plain`, `variant=primary`, `indent=true`, `showGuide=false`.

**Průchod a výsledek:** Sestavte oblast „Nákup / Dodavatelé“ s obsahem „Přehled; Otevřené objednávky“. Tone, odsazení a guide pomáhají číst hierarchii; neurčují aktuální stránku. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Web — zákaznický účet

**Situace a cíl:** Uživatel přechází mezi svými objednávkami a kontaktními údaji.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Obsahuje odkazy správné nadřazené větve. V průchodu se uplatní `tone=plain`, `variant=primary`, `indent=true`, `showGuide=false`.

**Průchod a výsledek:** Sestavte oblast „Můj účet / Objednávky“ s obsahem „Aktivní; Archivované objednávky“. Tone, odsazení a guide pomáhají číst hierarchii; neurčují aktuální stránku. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### Interní systém — projektový portál

**Situace a cíl:** Člen týmu prochází sekce projektu.

**Volba a varianta:** Je potřeba zachovat skladbu této oblasti, nikoli přidat její další klikací kopii. Obsahuje odkazy správné nadřazené větve. V průchodu se uplatní `tone=plain`, `variant=primary`, `indent=true`, `showGuide=false`.

**Průchod a výsledek:** Sestavte oblast „Projekt Orion / Dokumenty“ s obsahem „Podklady; Smlouvy“. Tone, odsazení a guide pomáhají číst hierarchii; neurčují aktuální stránku. Každou změnu nebo přechod provádí konkrétní pojmenovaný ovladač uvnitř.

**Výjimka a návrat:** Při zúžení či delším obsahu zachovejte přístup ke všem důležitým částem. Skrytí oblasti nesmí ponechat fokus v neviditelném obsahu nebo odstranit jedinou cestu zpět.

**Nevhodně:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit informační architekturu značky, názvy sekcí a vizuální hierarchii current/currentPath a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí cílové adresy, viditelnost podle role a zachování práce při přechodu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3534-18864)
