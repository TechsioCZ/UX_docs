# ProductCardImage

Obrazová část ProductCard představuje konkrétní produkt a zachovává vazbu na jeho název.

**Vazba:** ProductCard. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Obrázek představuje stejnou variantu jako název a cena karty. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě ProductCard. Obrázek představuje stejnou variantu jako název a cena karty.

## Kdy zvolit alternativu

Pro více souvisejících pohledů zvažte Gallery. Pro souvislý popis informací použijte text; obrázek není náhradou všech instrukcí.

## Anatomie, stavy a varianty

Součást skladby **ProductCard**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zobrazit obraz stejné položky jako ostatní obsah hostitele.

### Co vyvolávat nemá

- Bez určeného ovladače nepřidávat zoom, navigaci či změnu nabídky.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Obrázek představuje stejnou variantu jako název a cena karty.
- Ořez a alternativní text musí umožnit rozpoznat produkt.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Obraz má alternativu podle své skutečné úlohy; stejná identita je čitelná i při nenačtení. Ořez zachová podstatnou informaci. Klikací použití potřebuje samostatně definovaný, pojmenovaný a klávesnicově dostupný hostitel.

## Omezení a příklady podle typu projektu

### ERP — interní katalog materiálu

**Situace a cíl:** Pracovník vybírá konkrétní položku pro nákupní požadavek.

**Volba a varianta:** Obraz pomáhá rozpoznat právě zobrazený objekt; více volitelných pohledů by vyžadovalo Gallery nebo Carousel. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Zobrazte obraz „V18 s kufrem a dvěma bateriemi“ se shodnou textovou identitou. Ořez zachová rozhodující vlastnosti; pouze skutečně definovaný odkaz či ovladač může navázat detail nebo změnu snímku.

**Výjimka a návrat:** Při chybě obrazu ponechte název a textovou identitu objektu. Změna varianty musí aktualizovat i obraz; stará fotografie se nevydává za novou nabídku.

**Nevhodně:** Přidat nepojmenované přidání do košíku, upload nebo zoom samotné ploše obrázku.

### Web — e-shop

**Situace a cíl:** Zákazník porovnává nabídky a přidává dostupný produkt do košíku.

**Volba a varianta:** Obraz pomáhá rozpoznat právě zobrazený objekt; více volitelných pohledů by vyžadovalo Gallery nebo Carousel. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Zobrazte obraz „V18, 1 kus“ se shodnou textovou identitou. Ořez zachová rozhodující vlastnosti; pouze skutečně definovaný odkaz či ovladač může navázat detail nebo změnu snímku.

**Výjimka a návrat:** Při chybě obrazu ponechte název a textovou identitu objektu. Změna varianty musí aktualizovat i obraz; stará fotografie se nevydává za novou nabídku.

**Nevhodně:** Přidat nepojmenované přidání do košíku, upload nebo zoom samotné ploše obrázku.

### Interní systém — portál vybavení

**Situace a cíl:** Zaměstnanec vybírá zařízení ze schváleného katalogu.

**Volba a varianta:** Obraz pomáhá rozpoznat právě zobrazený objekt; více volitelných pohledů by vyžadovalo Gallery nebo Carousel. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

**Průchod a výsledek:** Zobrazte obraz „Monitor M27, černý“ se shodnou textovou identitou. Ořez zachová rozhodující vlastnosti; pouze skutečně definovaný odkaz či ovladač může navázat detail nebo změnu snímku.

**Výjimka a návrat:** Při chybě obrazu ponechte název a textovou identitu objektu. Změna varianty musí aktualizovat i obraz; stará fotografie se nevydává za novou nabídku.

**Nevhodně:** Přidat nepojmenované přidání do košíku, upload nebo zoom samotné ploše obrázku.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii produktových informací, slovník obchodních štítků a prioritu nákupních akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu nabídky, cenu, skladová data, oprávnění k nákupu a výsledek operace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26967)
