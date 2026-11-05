# ProductCardButton

Akční část ProductCard rozlišuje vložení do košíku, otevření detailu a práci s wishlistem.

**Vazba:** ProductCard. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Varianta cart, detail nebo wishlist musí odpovídat skutečné akci. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě ProductCard. Varianta cart, detail nebo wishlist musí odpovídat skutečné akci.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v ProductCard a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **ProductCard**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `buttonVariant=cart` | Pro reálnou akci přidání příslušné nabídky do košíku; oznámit výsledek požadavku. |
| `buttonVariant=detail` | Pro otevření detailu stejného produktu; nemění košík. |
| `buttonVariant=wishlist` | Pro uložení či změnu zájmu o stejný produkt; neznamená nákup. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Podle buttonVariant otevřít detail, požádat o přidání do košíku nebo změnit wishlist.

### Co vyvolávat nemá

- Nepřidat produkt, když akce slibuje pouze detail; neaktivovat zároveň jiný odkaz karty.

### Přechody a odpovědnost

Výsledek odpovídá konkrétní variantě akce nad stejnou nabídkou. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Varianta cart, detail nebo wishlist musí odpovídat skutečné akci.
- Název a symbol mají vyjadřovat tentýž výsledek; navigaci na detail nezaměňujte za změnu košíku.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — interní katalog materiálu

**Situace a cíl:** Pracovník vybírá konkrétní položku pro nákupní požadavek.

**Volba a varianta:** Samostatná akce odděluje detail, nákupní požadavek a wishlist; klikací obal je nesmí sloučit. V průchodu se uplatní `buttonVariant=detail`.

**Průchod a výsledek:** Pro nabídku „V18 s kufrem a dvěma bateriemi“ zvolte buttonVariant=detail. Aktivace otevře detail této varianty bez změny košíku.

**Výjimka a návrat:** Selhání změny ponechá nabídku dostupnou a sdělí skutečný výsledek. Událost nesmí současně aktivovat odkaz celé karty.

**Nevhodně:** Nepřidat produkt, když akce slibuje pouze detail; neaktivovat zároveň jiný odkaz karty.

### Web — e-shop

**Situace a cíl:** Zákazník porovnává nabídky a přidává dostupný produkt do košíku.

**Volba a varianta:** Samostatná akce odděluje detail, nákupní požadavek a wishlist; klikací obal je nesmí sloučit. V průchodu se uplatní `buttonVariant=cart`.

**Průchod a výsledek:** Pro nabídku „V18, 1 kus“ zvolte buttonVariant=cart. Aktivace požádá o přidání; až potvrzený výsledek změní stav košíku.

**Výjimka a návrat:** Selhání změny ponechá nabídku dostupnou a sdělí skutečný výsledek. Událost nesmí současně aktivovat odkaz celé karty.

**Nevhodně:** Nepřidat produkt, když akce slibuje pouze detail; neaktivovat zároveň jiný odkaz karty.

### Interní systém — portál vybavení

**Situace a cíl:** Zaměstnanec vybírá zařízení ze schváleného katalogu.

**Volba a varianta:** Samostatná akce odděluje detail, nákupní požadavek a wishlist; klikací obal je nesmí sloučit. V průchodu se uplatní `buttonVariant=wishlist`.

**Průchod a výsledek:** Pro nabídku „Monitor M27, černý“ zvolte buttonVariant=wishlist. Aktivace změní zájem o tentýž produkt; nejde o přidělení vybavení.

**Výjimka a návrat:** Selhání změny ponechá nabídku dostupnou a sdělí skutečný výsledek. Událost nesmí současně aktivovat odkaz celé karty.

**Nevhodně:** Nepřidat produkt, když akce slibuje pouze detail; neaktivovat zároveň jiný odkaz karty.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii produktových informací, slovník obchodních štítků a prioritu nákupních akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu nabídky, cenu, skladová data, oprávnění k nákupu a výsledek operace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-36138)
