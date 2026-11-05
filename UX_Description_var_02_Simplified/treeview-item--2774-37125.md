# TreeView/Item

Položka TreeView reprezentuje koncový uzel hierarchie bez vlastní rozbalované větve.

**Vazba:** TreeView. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Představuje koncový uzel, nikoli obal potomků. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě TreeView. Představuje koncový uzel, nikoli obal potomků.

## Kdy zvolit alternativu

Pro datovou hodnotu vyberte Select, Combobox či CascadeSelect podle rozsahu a hierarchie. Pro příkaz použijte Menu; vizuálně podobný obal nesmí měnit tento význam.

## Anatomie, stavy a varianty

Součást skladby **TreeView**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=selected` | Pro skutečně potvrzenou vybranou položku. Hover ani pouhý fokus ji nenahrazují. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Vybrat koncový uzel, pokud jej dovoluje režim stromu.

### Co vyvolávat nemá

- Nerozbalovat neexistující potomky ani nepovažovat fokus za potvrzení.

### Přechody a odpovědnost

Výběr identifikuje konkrétní list v jeho celé cestě. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Představuje koncový uzel, nikoli obal potomků.
- Odlište jeho výběr od fokusu a od otevření okolní větve.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společné výjimky a návrat:** Stejně pojmenované listy odlište cestou. Disabled list nelze potvrdit; zrušení výběrového úkolu nesmí provést navazující obchodní akci.

- **Pravidlo použití:** Nerozbalovat neexistující potomky ani nepovažovat fokus za potvrzení.

### ERP — struktura organizace

**Situace a cíl:** Pracovník prochází organizační členění před přiřazením zakázky.

**Volba a varianta:** List potvrzuje datový uzel; BranchTrigger prozkoumává větev a VerticalNavigation otevírá stránky. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** V cestě „Logistika / Sklad Brno“ aktivujte dostupný koncový uzel. Potvrzený výběr předá identitu tohoto listu; pouhý fokus ji nenahradí a neexistující potomci se nerozbalují.

### Web — správa dokumentů

**Situace a cíl:** Přihlášený uživatel prochází své složky a vybírá související dokument.

**Volba a varianta:** List potvrzuje datový uzel; BranchTrigger prozkoumává větev a VerticalNavigation otevírá stránky. V průchodu se uplatní `state=selected`.

**Průchod a výsledek:** V cestě „Projekt Orion / Podklady“ aktivujte dostupný koncový uzel. Potvrzený výběr předá identitu tohoto listu; pouhý fokus ji nenahradí a neexistující potomci se nerozbalují.

### Interní systém — DMS archiv

**Situace a cíl:** Správce prochází projektové složky.

**Volba a varianta:** List potvrzuje datový uzel; BranchTrigger prozkoumává větev a VerticalNavigation otevírá stránky. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** V cestě „Orion / Smlouvy“ aktivujte dostupný koncový uzel. Potvrzený výběr předá identitu tohoto listu; pouhý fokus ji nenahradí a neexistující potomci se nerozbalují.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy uzlů, ikonografii druhů položek a čitelnost hierarchie a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí datové vztahy, pravidla výběru a případné načítání potomků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-37125)
