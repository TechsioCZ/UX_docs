# ProductCardActions

Oblast akcí ProductCard sdružuje ovladače pro práci s nabídkou a odlišuje jejich výsledky.

**Vazba:** ProductCard. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Odlište otevření detailu, košík a wishlist. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě ProductCard. Odlište otevření detailu, košík a wishlist.

## Kdy zvolit alternativu

Pokud karta jen informuje, nenabízejte falešnou akci. Pokud potřebujete jen otevřít detail, použijte odpovídající odkaz či detail podobu ProductCardButton.

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

- Odlište otevření detailu, košík a wishlist.
- Vnořené akce musí zůstat samostatně dostupné i při klikatelné kartě.
- Vnořená akce nesmí nechtěně spustit současně i navigaci celé karty.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Samotná oblast nepřebírá jména a akce svých ovladačů. Vnořené odkazy a tlačítka mají vlastní názvy a logické pořadí. Při menší šířce zůstává dosažitelný celý podstatný obsah, nikoli jen první viditelná část.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Oblast sdružuje samostatné akce; klikací obal nesmí sloučit jejich různé výsledky. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Vnořená akce se nesmí současně propadnout do navigace celé karty. Selhání změny zachová nabídku i zjistitelnou příčinu.

- **Nevhodné použití:** Spustit vedle akce potomka ještě nesouvisející operaci celého obalu.

### ERP — interní katalog materiálu

**Situace a cíl:** Pracovník vybírá konkrétní položku pro nákupní požadavek.

**Průchod a výsledek:** U nabídky „V18 s kufrem a dvěma bateriemi“ vložte samostatně pojmenovanou akci Zobrazit detail s buttonVariant=detail. Otevře se právě tato varianta.

### Web — e-shop

**Situace a cíl:** Zákazník porovnává nabídky a přidává dostupný produkt do košíku.

**Průchod a výsledek:** U nabídky „V18, 1 kus“ vložte samostatně pojmenovanou akci Přidat do košíku s buttonVariant=cart. Až potvrzení aplikace změní košík.

### Interní systém — portál vybavení

**Situace a cíl:** Zaměstnanec vybírá zařízení ze schváleného katalogu.

**Průchod a výsledek:** U nabídky „Monitor M27, černý“ vložte samostatně pojmenovanou akci Uložit do seznamu přání s buttonVariant=wishlist. Nejde o přidělení vybavení.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii produktových informací, slovník obchodních štítků a prioritu nákupních akcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí identitu nabídky, cenu, skladová data, oprávnění k nákupu a výsledek operace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-26988)
