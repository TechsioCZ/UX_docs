# LinkButton

Odkaz ve vzhledu tlačítka zdůrazňuje přechod na konkrétní cíl.

Cílem je zvýraznit důležitý navigační přechod při zachování chování odkazu.

## Kdy použít

Pro důležitý navigační přechod, který má zůstat skutečným odkazem. Otevření formuláře ještě nevytváří záznam. Pro odeslání formuláře nebo jinou změnu dat použijte Button.

## Kdy zvolit alternativu

Pro uložení, odstranění nebo odeslání použijte Button.

## Anatomie, stavy a varianty

Odkaz s viditelnou prioritou tlačítka. Variant/theme/size vyjadřují prezentaci navigace; prvek stále slibuje konkrétní cíl, nikoli odeslání formuláře.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `variant=primary` | Pro hlavní další krok aktuálního úkolu; vizuální prioritu sladit s úrovní 2. |
| `variant=secondary` | Pro doplňující akci vedle hlavní, pokud má zůstat zřetelně dostupná. |
| `variant=tertiary` | Pro méně výraznou související akci; neskrýt její dostupný název. |
| `variant=warning` | Pro akci vyžadující zvýšenou pozornost k důsledku, který vysvětluje její text. |
| `variant=danger` | Pro destruktivní nebo jinak závažný důsledek; pojmenovat objekt a výsledek. |
| `theme=solid` | Plná podkladová plocha pro určenou vizuální prioritu podle úrovně 2; závažnost akce dále určuje její variant a text. |
| `theme=light` | Jemnější podklad pro méně intenzivní plochu při zachované čitelnosti a rozpoznatelnosti ovladače. |
| `theme=outlined` | Ohraničený ovladač při méně dominantní výplni; rámeček nesmí být jedinou informací o dostupnosti. |
| `theme=borderless` | Bez rámečku pro integrovanou či méně výraznou akci; okolní kontext musí zachovat rozpoznatelnost ovladače. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít konkrétní pojmenovaný cíl.
- Vizuálně odlišit významný navigační krok od vedlejších odkazů.

### Co vyvolávat nemá

- Neodesílat formulář ani skrytě měnit data.
- Nepřisuzovat primary automaticky význam schváleného firemního pravidla.

### Přechody a odpovědnost

Aktivace konkrétního odkazu otevře jeho pojmenovaný cíl; teprve skutečně zobrazená stránka určuje current. Otevření navigační větve nebo rámu není přechod na stránku. Zrušení panelu ponechá původní pracovní kontext a vyřeší návrat fokusu. Nedostupný cíl aplikace vysvětlí a nabídne návrat; navigace nesmí skrytě měnit obchodní data ani zahodit neuložený draft bez určeného postupu.

### Konkrétní pravidla použití

- Text vyjádří cíl, například „Přejít do košíku“.
- Zachovejte navigační význam i při tlačítkovém vzhledu.
- Nedostupnost musí řešit i skutečnou aktivaci odkazu, nejen barvu.

## Obsah a pojmenování

Název akce vyjadřuje výsledek: například „Uložit změny“ nebo „Otevřít objednávku“. U závažného kroku je rozpoznatelný i objekt zásahu. Nepoužívejte obecné „OK“, pokud z něj nelze určit následek.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — rozcestník agendy

**Situace a cíl:** Pracovník chce začít vytvářet nový požadavek.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Vytvořit požadavek“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `variant=primary`, `state=default`.

**Průchod a výsledek:** Pro objekt „Formulář nového požadavku“ použijte pojmenování „Vytvořit požadavek“. Aktivace „Otevřít formulář“ otevře odpovídající cíl bez změny obchodních dat. Hover je pouze interakční zvýraznění a dostupný odkaz zůstává ovladatelný klávesnicí. Pokud je nutné před odchodem vyřešit neuložené změny, udělá to určený průchod produktu, nikoli skrytá změna významu odkazu.

**Výjimka a návrat:** Pojmenování Potvrdit by zde slibovalo jiný výsledek než pouhou navigaci.

**Nevhodně:** Neodesílat formulář ani skrytě měnit data.

### Web — nabídka služby

**Situace a cíl:** Návštěvník chce přejít k podrobnostem vybrané nabídky.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Zjistit podrobnosti“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `variant=primary`, `state=default`.

**Průchod a výsledek:** Pro objekt „Detail služby“ použijte pojmenování „Zjistit podrobnosti“. Aktivace „Otevřít nabídku“ otevře odpovídající cíl bez změny obchodních dat. Hover je pouze interakční zvýraznění a dostupný odkaz zůstává ovladatelný klávesnicí. Pokud je nutné před odchodem vyřešit neuložené změny, udělá to určený průchod produktu, nikoli skrytá změna významu odkazu.

**Výjimka a návrat:** Stisk nesmí bez dalšího provést objednávku jen proto, že prvek vypadá jako tlačítko.

**Nevhodně:** Neodesílat formulář ani skrytě měnit data.

### Interní systém — zaměstnanecký portál

**Situace a cíl:** Zaměstnanec přechází do agendy svých žádostí.

**Volba a varianta:** Uživatel se orientuje nebo přechází přes „Moje žádosti“. Jde o navigaci na pojmenovaný cíl; Button měnící data by měl jiný význam. V průchodu se uplatní `variant=primary`, `state=default`.

**Průchod a výsledek:** Pro objekt „Přehled žádostí“ použijte pojmenování „Moje žádosti“. Aktivace „Otevřít přehled“ otevře odpovídající cíl bez změny obchodních dat. Hover je pouze interakční zvýraznění a dostupný odkaz zůstává ovladatelný klávesnicí. Pokud je nutné před odchodem vyřešit neuložené změny, udělá to určený průchod produktu, nikoli skrytá změna významu odkazu.

**Výjimka a návrat:** Disabled navigace nevyvolá přesun a důvod nedostupnosti je z kontextu zjistitelný.

**Nevhodně:** Neodesílat formulář ani skrytě měnit data.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit hierarchii navigačních výzev a vztah vzhledu odkazu k ostatním tlačítkům a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí cíl navigace a zacházení s nedokončenou prací před přechodem. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-37412)
