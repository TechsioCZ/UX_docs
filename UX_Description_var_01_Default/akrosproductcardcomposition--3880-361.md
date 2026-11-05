# AkrosProductCardComposition

Ukázková kompozice produktové karty kombinuje cenu, dostupnost a akci v existujícím tématu Akros.

Cílem je posoudit referenční kompozici nabídky před sestavením veřejných komponent.

## Kdy použít

Jako konkrétní referenci Akros pro porovnání identity, ceny, dostupnosti, množství a akce v jedné nabídce. Do projektu vyberte veřejné části; lokální výška ani ukázková data nejsou obecným pravidlem ProductCard.

## Kdy zvolit alternativu

Pro veřejnou stavební komponentu použijte ProductCard.

## Anatomie, stavy a varianty

Referenční story skládá cenu, dostupnost, množství a nákupní akci v tématu Akros. Její scénáře ukazují kompozici veřejných částí, nikoli nový veřejný export nebo skutečný košík.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `example=playground` | Ukázkový scénář playground; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=action-pending` | Ukázkový scénář action-pending; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=unavailable` | Ukázkový scénář unavailable; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=from` | Ukázkový scénář from; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=discounted` | Ukázkový scénář discounted; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=on-request` | Ukázkový scénář on-request; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=no-image` | Ukázkový scénář no-image; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=limited` | Ukázkový scénář limited; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=price-pending` | Ukázkový scénář price-pending; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=availability-available` | Ukázkový scénář availability-available; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=availability-limited` | Ukázkový scénář availability-limited; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=availability-preorder` | Ukázkový scénář availability-preorder; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=availability-unknown` | Ukázkový scénář availability-unknown; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=availability-pending` | Ukázkový scénář availability-pending; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=long-content` | Ukázkový scénář long-content; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=with-quantity` | Ukázkový scénář with-quantity; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=discounted-badge` | Ukázkový scénář discounted-badge; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |
| `example=recommended` | Ukázkový scénář recommended; inspirace pro návrh, nikoli nový provozní stav, veřejný export nebo univerzální výchozí nastavení. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Porovnat referenční stavy nabídky a jejich vzájemnou konzistenci.

### Co vyvolávat nemá

- Nepovažovat story za samostatný veřejný export, skutečný košík nebo pravidlo všech značek.

### Přechody a odpovědnost

Reference slouží posouzení uvedené skladby. Přechod do provozního použití znamená volbu konkrétních veřejných částí a jejich skutečných stavů, nikoli automatickou aktivaci celého ukázkového frame. Lokální chování příkladu se nepřenáší na celou rodinu.

### Konkrétní pravidla použití

- Kompozice je story, nikoli samostatný veřejný export nebo skutečný košík.
- Cena, dostupnost a nákupní akce mají oddělené odpovědnosti.
- Demonstrativní meze množství a lokální výška ovladače se nepřenášejí na celý DS.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — interní katalog materiálu

**Situace a cíl:** Pracovník vybírá konkrétní položku pro nákupní požadavek.

**Volba a varianta:** Porovnává se konkrétní reference Akros; veřejný ProductCard se musí sestavit z určených částí a jejich vlastních pravidel. V průchodu se uplatní `example=playground`.

**Průchod a výsledek:** Posuďte reference „V18 s kufrem a dvěma bateriemi“: identita produktu, množství, cena, dostupnost a případná akce musí popisovat tutéž nabídku. Následné provozní použití sestavte z veřejných částí. Ukázková lokální výška není další obecnou velikostí QuantityField.

**Výjimka a návrat:** Karta nesmí kombinovat fotografii jedné sady s cenou jiné varianty.

**Nevhodně:** Nepovažovat story za samostatný veřejný export, skutečný košík nebo pravidlo všech značek.

### Web — e-shop

**Situace a cíl:** Zákazník porovnává nabídky a přidává dostupný produkt do košíku.

**Volba a varianta:** Porovnává se konkrétní reference Akros; veřejný ProductCard se musí sestavit z určených částí a jejich vlastních pravidel. V průchodu se uplatní `example=playground`.

**Průchod a výsledek:** Posuďte reference „V18, 1 kus“: identita produktu, množství, cena, dostupnost a případná akce musí popisovat tutéž nabídku. Následné provozní použití sestavte z veřejných částí. Ukázková lokální výška není další obecnou velikostí QuantityField.

**Výjimka a návrat:** Nedostupná nabídka může umožnit čtení detailu, aniž by falešně nabízela úspěšný nákup.

**Nevhodně:** Nepovažovat story za samostatný veřejný export, skutečný košík nebo pravidlo všech značek.

### Interní systém — portál vybavení

**Situace a cíl:** Zaměstnanec vybírá zařízení ze schváleného katalogu.

**Volba a varianta:** Porovnává se konkrétní reference Akros; veřejný ProductCard se musí sestavit z určených částí a jejich vlastních pravidel. V průchodu se uplatní `example=playground`.

**Průchod a výsledek:** Posuďte reference „Monitor M27, černý“: identita produktu, množství, cena, dostupnost a případná akce musí popisovat tutéž nabídku. Následné provozní použití sestavte z veřejných částí. Ukázková lokální výška není další obecnou velikostí QuantityField.

**Výjimka a návrat:** Dlouhý název musí být celý zjistitelný a nesmí překrýt cenu či ovladač.

**Nevhodně:** Nepovažovat story za samostatný veřejný export, skutečný košík nebo pravidlo všech značek.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii produktových informací, slovník obchodních štítků a prioritu nákupních akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu nabídky, cenu, skladová data, oprávnění k nákupu a výsledek operace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3880-361)
