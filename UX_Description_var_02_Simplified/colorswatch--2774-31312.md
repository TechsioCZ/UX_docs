# ColorSwatch

Barevný vzorek představuje jednu volitelnou barvu.

Cílem je vybrat konkrétní nabízenou barvu bez závislosti na jejím vizuálním rozlišení.

## Kdy použít

Pro výběr konkrétní nabízené barvy s textovým názvem. Uživatel musí vědět, zda vybírá produktovou variantu nebo vizuální nastavení. Barva sama nevyjadřuje sklad, cenu ani dokončení uložení.

## Kdy zvolit alternativu

Samotným barevným vzorkem nesdělujte stav, který potřebuje textové vysvětlení.

## Anatomie, stavy a varianty

ColorSwatch prezentuje jednu barevnou možnost a stav jejího výběru či dostupnosti. Jeho textový název a vazbu na skutečnou variantu dodává okolní výběrová skladba.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `radius=sm` | Vizuální provedení sm podle pravidel úrovně 2 a zřetelného oddělení obsahu; nemění význam ani akce. |
| `radius=md` | Vizuální provedení md podle pravidel úrovně 2 a zřetelného oddělení obsahu; nemění význam ani akce. |
| `radius=lg` | Vizuální provedení lg podle pravidel úrovně 2 a zřetelného oddělení obsahu; nemění význam ani akce. |
| `radius=full` | Vizuální provedení full podle pravidel úrovně 2 a zřetelného oddělení obsahu; nemění význam ani akce. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=selected` | Pro skutečně potvrzenou vybranou položku. Hover ani pouhý fokus ji nenahrazují. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=focus` | Při skutečném klávesnicovém fokusu. Poloha fokusu zůstává odlišitelná od vybrané hodnoty a aktivace. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zvolit dostupný vzorek a textově potvrdit jeho název.
- Odlišit fokus od již vybrané barvy.

### Co vyvolávat nemá

- Nepoužívat barvu jako jediný identifikátor nabídky.
- Neodvozovat skladovou dostupnost nebo úspěch uložení z barevného vzorku.

### Přechody a odpovědnost

Fokus a hover pouze zpřístupňují vzorek. Až aktivace dostupné barvy potvrdí selected a její textový název; disabled nelze vybrat. Aplikace současně aktualizuje údaje stejné produktové varianty. Při selhání navazujícího načtení se neprezentuje stará fotografie či cena jako potvrzená nová nabídka.

### Konkrétní pravidla použití

- Každý vzorek má srozumitelný název.
- Vybranou a nedostupnou barvu odlište i jinak než odstínem.
- Světlé a podobné barvy musí zůstat rozpoznatelné vůči pozadí.
- Počet současně vybraných barev určuje celá výběrová kompozice.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nepoužívat barvu jako jediný identifikátor nabídky.

### ERP — katalog materiálů

**Situace a cíl:** Pracovník vybírá barevné provedení evidované položky.

**Volba a varianta:** Pro „Barva materiálu“ je třeba pojmenovaný barevný vzorek; samotný barevný kruh bez názvu nestačí. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** Pro objekt „Antracit“ použijte pojmenování „Barva materiálu“. Před volbou je vzorek default a po potvrzení správné barvy selected. Fokus či hover nejsou potvrzením. Název vybrané barvy i související obrázek či údaj odpovídají stejné variantě; disabled volbu nelze potvrdit.

**Výjimka a návrat:** Dvě podobné šedé potřebují rozlišitelné názvy; samotný odstín nestačí.

### Web — konfigurátor produktu

**Situace a cíl:** Zákazník porovnává dostupné barevné varianty.

**Volba a varianta:** Pro „Barva výrobku“ je třeba pojmenovaný barevný vzorek; samotný barevný kruh bez názvu nestačí. V průchodu se uplatní `state=selected`.

**Průchod a výsledek:** Pro objekt „Modrá“ použijte pojmenování „Barva výrobku“. Před volbou je vzorek default a po potvrzení správné barvy selected. Fokus či hover nejsou potvrzením. Název vybrané barvy i související obrázek či údaj odpovídají stejné variantě; disabled volbu nelze potvrdit.

**Výjimka a návrat:** Disabled barva není objednatelná a její hover nesmí změnit potvrzený produkt.

### Interní systém — konfigurace pracovních týmů

**Situace a cíl:** Správce vybírá značku týmu z omezené schválené palety.

**Volba a varianta:** Pro „Barva týmu“ je třeba pojmenovaný barevný vzorek; samotný barevný kruh bez názvu nestačí. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** Pro objekt „Tým Logistika, zelená“ použijte pojmenování „Barva týmu“. Před volbou je vzorek default a po potvrzení správné barvy selected. Fokus či hover nejsou potvrzením. Název vybrané barvy i související obrázek či údaj odpovídají stejné variantě; disabled volbu nelze potvrdit.

**Výjimka a návrat:** Tým není identifikovaný pouze zeleným kroužkem v jinak nepojmenovaném seznamu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit schválené názvy barev, prezentaci vzorků a tokeny vybraného stavu a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí seznam nabízených barev, jejich identity a případné vazby na variantu produktu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-31312)
