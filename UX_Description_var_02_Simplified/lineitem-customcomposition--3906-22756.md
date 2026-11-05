# __LineItem/CustomComposition

Interní referenční LineItem ukazuje vlastní skladbu částí řádku položky.

**Vazba:** LineItem. Tato část je konkrétní reference, nikoli automaticky nový veřejný export.

## Kdy použít

Slouží referenční vlastní skladbě LineItem. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě LineItem. Jde o referenční či starší skladbu; její místní nastavení není univerzální veřejné pravidlo.

## Kdy zvolit alternativu

Pro provozní sestavení vyberte veřejné části rodiny LineItem. Referenční příklad nekopírujte jako nový export, pravidlo značky nebo důkaz dokončeného procesu.

## Anatomie, stavy a varianty

Součást skladby **LineItem**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Posoudit tuto konkrétní referenční skladbu před volbou veřejného řešení.

### Co vyvolávat nemá

- Nepřenést ukázková data, lokální rozměr nebo starší pojmenování jako univerzální pravidlo projektu.

### Přechody a odpovědnost

Reference slouží posouzení uvedené skladby. Přechod do provozního použití znamená volbu konkrétních veřejných částí a jejich skutečných stavů, nikoli automatickou aktivaci celého ukázkového frame. Lokální chování příkladu se nepřenáší na celou rodinu.

### Konkrétní pravidla použití

- Slouží referenční vlastní skladbě LineItem.
- Přizpůsobení zachovává identitu položky a soulad ceny, množství a akcí.

## Obsah a pojmenování

Názvy údajů, částky nebo množství vztahujte ke stejné položce a jednotce. Měna či balení nezmizí při zkrácení. Ukázkové číslo z příkladu není výchozí hodnota ani limit projektu; jeho zdroj a přesnost určuje aplikace.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Jde o konkrétní referenci, nikoli další obecný veřejný ovladač; provozní skladba musí mít určené části. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Odlišná šířka, lokální override nebo staré pojmenování se nepřenáší automaticky. Přizpůsobení zachovává identitu položky a soulad ceny, množství a akcí.

- **Nevhodné použití:** Převzít lokální rozměr nebo ukázkové chování jako univerzální pravidlo rodiny či značky.

### ERP — nákupní požadavek

**Situace a cíl:** Pracovník upravuje jeden řádek připravované objednávky materiálu.

**Průchod a výsledek:** Při návrhu oblasti „Těsnění T-40“ posuďte referenci „3 balení těsnění T-40“. Slouží referenční vlastní skladbě LineItem. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

### Web — košík

**Situace a cíl:** Zákazník chce odebrat nedostupný produkt z košíku.

**Průchod a výsledek:** Při návrhu oblasti „Vrtačka V18“ posuďte referenci „1 kus V18 s kufrem“. Slouží referenční vlastní skladbě LineItem. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

### Interní systém — portál služeb

**Situace a cíl:** Zaměstnanec čte již odeslaný požadavek v režimu readonly.

**Průchod a výsledek:** Při návrhu oblasti „Servisní sada“ posuďte referenci „2 sady příslušenství“. Slouží referenční vlastní skladbě LineItem. Ověřte vazbu názvu, obsahu a dosažitelných akcí; do projektu zvolte odpovídající skutečnou skladbu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii názvu, ceny, jednotek a řádkových akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu položky, výpočty, dostupnost a pravidla ukládání změn. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3906-22756)
