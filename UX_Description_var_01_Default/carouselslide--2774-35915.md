# CarouselSlide

Snímek Carousel nese jednu položku sekvence a určuje způsob přizpůsobení obrázku své ploše.

**Vazba:** Carousel. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Jeden snímek představuje jednu položku sekvence. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Carousel. Jeden snímek představuje jednu položku sekvence.

## Kdy zvolit alternativu

Pro více souvisejících pohledů zvažte Gallery. Pro souvislý popis informací použijte text; obrázek není náhradou všech instrukcí.

## Anatomie, stavy a varianty

Součást skladby **Carousel**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `objectFit=cover` | Vyplnit plochu s možným ořezem; zachovat informace rozhodující pro identifikaci. |
| `objectFit=contain` | Ukázat celý obraz v ploše i za cenu volného místa. |
| `objectFit=fill` | Roztáhnout do plochy jen pokud deformace neznehodnotí informaci. |
| `objectFit=none` | Ponechat přirozený rozměr a posoudit ořez i dostupnost obsahu v určeném kontejneru. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zobrazit obraz stejné položky jako ostatní obsah hostitele.

### Co vyvolávat nemá

- Bez určeného ovladače nepřidávat zoom, navigaci či změnu nabídky.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Jeden snímek představuje jednu položku sekvence.
- ObjectFit volte tak, aby ořez zachoval důležitý obsah.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Obraz má alternativu podle své skutečné úlohy; stejná identita je čitelná i při nenačtení. Ořez zachová podstatnou informaci. Klikací použití potřebuje samostatně definovaný, pojmenovaný a klávesnicově dostupný hostitel.

## Omezení a příklady podle typu projektu

### ERP — katalog zařízení

**Situace a cíl:** Pracovník porovnává pohledy na vybírané zařízení.

**Volba a varianta:** Obraz pomáhá rozpoznat právě zobrazený objekt; více volitelných pohledů by vyžadovalo Gallery nebo Carousel. V průchodu se uplatní `objectFit=cover`.

**Průchod a výsledek:** Zobrazte obraz „Zařízení Z-22, boční pohled“ se shodnou textovou identitou. Ořez zachová rozhodující vlastnosti; pouze skutečně definovaný odkaz či ovladač může navázat detail nebo změnu snímku.

**Výjimka a návrat:** Při chybě obrazu ponechte název a textovou identitu objektu. Změna varianty musí aktualizovat i obraz; stará fotografie se nevydává za novou nabídku.

**Nevhodně:** Přidat nepojmenované přidání do košíku, upload nebo zoom samotné ploše obrázku.

### Web — produktová prezentace

**Situace a cíl:** Návštěvník chce vidět více situací použití produktu.

**Volba a varianta:** Obraz pomáhá rozpoznat právě zobrazený objekt; více volitelných pohledů by vyžadovalo Gallery nebo Carousel. V průchodu se uplatní `objectFit=cover`.

**Průchod a výsledek:** Zobrazte obraz „Vrtačka při práci v dílně“ se shodnou textovou identitou. Ořez zachová rozhodující vlastnosti; pouze skutečně definovaný odkaz či ovladač může navázat detail nebo změnu snímku.

**Výjimka a návrat:** Při chybě obrazu ponechte název a textovou identitu objektu. Změna varianty musí aktualizovat i obraz; stará fotografie se nevydává za novou nabídku.

**Nevhodně:** Přidat nepojmenované přidání do košíku, upload nebo zoom samotné ploše obrázku.

### Interní systém — výuková knihovna

**Situace a cíl:** Pracovník prochází související obrázkové instrukce.

**Volba a varianta:** Obraz pomáhá rozpoznat právě zobrazený objekt; více volitelných pohledů by vyžadovalo Gallery nebo Carousel. V průchodu se uplatní `objectFit=cover`.

**Průchod a výsledek:** Zobrazte obraz „Nastavení pracovního panelu“ se shodnou textovou identitou. Ořez zachová rozhodující vlastnosti; pouze skutečně definovaný odkaz či ovladač může navázat detail nebo změnu snímku.

**Výjimka a návrat:** Při chybě obrazu ponechte název a textovou identitu objektu. Změna varianty musí aktualizovat i obraz; stará fotografie se nevydává za novou nabídku.

**Nevhodně:** Přidat nepojmenované přidání do košíku, upload nebo zoom samotné ploše obrázku.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit povolený styl prezentace, práci s pohybem a význam případného zvýraznění obsahu a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí pořadí snímků, krajní chování sekvence a případné přehrávání. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-35915)
