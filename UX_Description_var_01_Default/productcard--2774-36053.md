# ProductCard

Produktová karta shrnuje jednu nabídku a poskytuje odpovídající další akci.

Cílem je porovnat konkrétní nabídku a přejít k jasně oddělené akci nad touto nabídkou.

## Kdy použít

Pro porovnání jedné konkrétní nabídky a rozpoznatelný přechod k jejímu detailu, košíku nebo wishlistu. Identita, cena, dostupnost i akce musí patřit téže variantě. Srovnatelná data mnoha řádků mohou lépe obsloužit Table.

## Kdy zvolit alternativu

Pro položku košíku použijte LineItem.

## Anatomie, stavy a varianty

ProductCardImage, Name a relevantní Price, Badges, Rating, Stock a Actions či Button. Každá část představuje stejnou konkrétní nabídku; rozložení column/row nemění její identitu.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `layout=column` | Svislá karta při omezené šířce nebo katalogové mřížce. |
| `layout=row` | Vodorovná karta pro prostor, kde vedle sebe zůstanou čitelné identita, cena a akce. |
| `buttonVariant=cart` | Pro reálnou akci přidání příslušné nabídky do košíku; oznámit výsledek požadavku. |
| `buttonVariant=detail` | Pro otevření detailu stejného produktu; nemění košík. |
| `buttonVariant=wishlist` | Pro uložení či změnu zájmu o stejný produkt; neznamená nákup. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít detail produktu nebo spustit určenou akci cart či wishlist.
- Udržet identitu obrázku, názvu, ceny, dostupnosti a akcí.

### Co vyvolávat nemá

- Nepřidávat do košíku kliknutím na libovolný text bez zřejmé výzvy.
- Nepřevádět automaticky stavy samostatného AvailabilityStatus na tříhodnotový ProductCardStock.

### Přechody a odpovědnost

Pro objekt „V18 s kufrem a dvěma bateriemi“ použijte pojmenování „Aku vrtačka V18“. Pro uvedený úkol je v tomto příkladu buttonVariant=detail. Název, obrázek, cena i dostupnost ukazují tutéž nabídku. Aktivace tohoto tlačítka se nesloučí s jiným odkazem celé karty; potvrzení změny musí vycházet z výsledku aplikace. Odpovědnost za skutečný výsledek a případné odmítnutí má aplikace hostící tuto komponentu.

### Konkrétní pravidla použití

- Název, obrázek, cena a dostupnost patří ke stejné variantě produktu.
- Odlište otevření detailu, vložení do košíku a wishlist.
- Kliknutí na celou kartu nesmí zastínit samostatné vnořené akce.
- Dostupnost sama neurčuje oprávnění koupit.
- Dlouhý název nesmí překrýt cenu ani hlavní akci.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — interní katalog materiálu

**Situace a cíl:** Pracovník vybírá konkrétní položku pro nákupní požadavek.

**Volba a varianta:** Nabídka „V18 s kufrem a dvěma bateriemi“ potřebuje souvislou identitu, cenu a dostupnost před samostatnou akcí; pouhý obrázek by rozhodnutí nevysvětlil. V průchodu se uplatní `layout=column`, `buttonVariant=detail`.

**Průchod a výsledek:** Pro objekt „V18 s kufrem a dvěma bateriemi“ použijte pojmenování „Aku vrtačka V18“. Pro uvedený úkol je v tomto příkladu buttonVariant=detail. Název, obrázek, cena i dostupnost ukazují tutéž nabídku. Aktivace tohoto tlačítka se nesloučí s jiným odkazem celé karty; potvrzení změny musí vycházet z výsledku aplikace.

**Výjimka a návrat:** Karta nesmí kombinovat fotografii jedné sady s cenou jiné varianty.

**Nevhodně:** Nepřidávat do košíku kliknutím na libovolný text bez zřejmé výzvy.

### Web — e-shop

**Situace a cíl:** Zákazník porovnává nabídky a přidává dostupný produkt do košíku.

**Volba a varianta:** Nabídka „V18, 1 kus“ potřebuje souvislou identitu, cenu a dostupnost před samostatnou akcí; pouhý obrázek by rozhodnutí nevysvětlil. V průchodu se uplatní `layout=column`, `buttonVariant=cart`.

**Průchod a výsledek:** Pro objekt „V18, 1 kus“ použijte pojmenování „Aku vrtačka V18“. Pro uvedený úkol je v tomto příkladu buttonVariant=cart. Název, obrázek, cena i dostupnost ukazují tutéž nabídku. Aktivace tohoto tlačítka se nesloučí s jiným odkazem celé karty; potvrzení změny musí vycházet z výsledku aplikace.

**Výjimka a návrat:** Nedostupná nabídka může umožnit čtení detailu, aniž by falešně nabízela úspěšný nákup.

**Nevhodně:** Nepřidávat do košíku kliknutím na libovolný text bez zřejmé výzvy.

### Interní systém — portál vybavení

**Situace a cíl:** Zaměstnanec vybírá zařízení ze schváleného katalogu.

**Volba a varianta:** Nabídka „Monitor M27, černý“ potřebuje souvislou identitu, cenu a dostupnost před samostatnou akcí; pouhý obrázek by rozhodnutí nevysvětlil. V průchodu se uplatní `layout=column`, `buttonVariant=wishlist`.

**Průchod a výsledek:** Pro objekt „Monitor M27, černý“ použijte pojmenování „Monitor M27“. Pro uvedený úkol je v tomto příkladu buttonVariant=wishlist. Název, obrázek, cena i dostupnost ukazují tutéž nabídku. Aktivace tohoto tlačítka se nesloučí s jiným odkazem celé karty; potvrzení změny musí vycházet z výsledku aplikace.

**Výjimka a návrat:** Dlouhý název musí být celý zjistitelný a nesmí překrýt cenu či ovladač.

**Nevhodně:** Nepřidávat do košíku kliknutím na libovolný text bez zřejmé výzvy.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii produktových informací, slovník obchodních štítků a prioritu nákupních akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu nabídky, cenu, skladová data, oprávnění k nákupu a výsledek operace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-36053)
