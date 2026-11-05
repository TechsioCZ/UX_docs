# FileUpload

Výběr souborů umožňuje získat a zkontrolovat místní soubory před dalším zpracováním.

Cílem je vybrat soubory pro určený účel a zjistit, zda byly přijaty a případně skutečně přeneseny.

## Kdy použít

Pro přidání souborů k přesně pojmenovanému účelu. Před výběrem musí být známé podmínky přijetí a rozdíl mezi lokální přílohou a serverovým uložením. Dostupná musí být cesta bez tažení.

## Kdy zvolit alternativu

Neoznačovat místně přijatý soubor za úspěšně nahraný. Neodstranit již uložený dokument pouhým odebráním nové lokální přílohy.

## Anatomie, stavy a varianty

Dropzone zpřístupňuje výběr i přetažení; jednotlivé Item ukazují přijaté či odmítnuté soubory a jejich typ. Lokální přijetí a skutečný serverový přenos jsou oddělené kroky.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=invalid` | Když kontrola odhalí neplatný údaj nebo výběr. Vysvětlení určí opravu; samotná barva nestačí. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=readonly` | Když má být existující hodnota čitelná, ale není dovoleno ji měnit. Nezaměňovat za disabled ani za prázdnou hodnotu. |
| `required=false` | Když lze údaj vědomě nevyplnit; absence není automaticky chyba. |
| `required=true` | Když proces skutečně vyžaduje údaj. Stejná podmínka platí ve validaci. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít výběr souboru, přidat soubor nebo jej odebrat z připravované sady.
- Povolit tažení jako doplňkovou cestu ke stejnému výběru.

### Co vyvolávat nemá

- Neoznačovat místně přijatý soubor za úspěšně nahraný.
- Neodstranit již uložený dokument pouhým odebráním nové lokální přílohy.

### Přechody a odpovědnost

Výběr nejprve vytvoří lokální sadu. Kontrola podmínek rozliší accepted a rejected s konkrétním důvodem; accepted ještě neznamená upload. Pokud projekt přenáší soubory, musí aplikace oddělit průběh, úspěch a opakování po chybě. Zrušení výběru nepřidá nový soubor; odebrání lokální přílohy nesmaže již uložený dokument.

### Konkrétní pravidla použití

- Uveďte skutečně povolené typy, velikosti a další limity.
- Přetažení doplňte systémovým výběrem souboru.
- Odmítnutí vysvětlete u konkrétní přílohy.
- Accepted znamená přijetí místního File objektu, nikoli dokončené nahrání na server. Transport, průběh a serverové chyby řídí aplikace.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — příloha dodavatelského dokladu

**Situace a cíl:** Pracovník přidává podklad k právě upravované faktuře.

**Volba a varianta:** Soubor „dodaci-list-1048.pdf“ má být přílohou tohoto úkolu; pouhý Image by nezajistil výběr ani podmínky přijetí. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „dodaci-list-1048.pdf“ použijte pojmenování „Příloha faktury“. Akce „Vybrat soubor“ zpřístupní výběr i bez tažení. Přijatý soubor má type=accepted a odmítnutý type=rejected s konkrétním důvodem. Přijetí do seznamu ještě neznamená serverové uložení; průběh a výsledek přenosu musí být určeny odděleně.

**Výjimka a návrat:** Odmítnutý typ vysvětlí konkrétní omezení a neodstraní jiné již vybrané platné soubory.

**Nevhodně:** Neoznačovat místně přijatý soubor za úspěšně nahraný.

### Web — zákaznický požadavek

**Situace a cíl:** Návštěvník přikládá fotografii k dotazu na produkt.

**Volba a varianta:** Soubor „detail-vady.jpg“ má být přílohou tohoto úkolu; pouhý Image by nezajistil výběr ani podmínky přijetí. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „detail-vady.jpg“ použijte pojmenování „Fotografie k požadavku“. Akce „Přidat fotografii“ zpřístupní výběr i bez tažení. Přijatý soubor má type=accepted a odmítnutý type=rejected s konkrétním důvodem. Přijetí do seznamu ještě neznamená serverové uložení; průběh a výsledek přenosu musí být určeny odděleně.

**Výjimka a návrat:** Odebrání nové fotografie neznamená smazání celého požadavku a dotykový uživatel má cestu bez drag-and-drop.

**Nevhodně:** Neoznačovat místně přijatý soubor za úspěšně nahraný.

### Interní systém — dokumentový portál

**Situace a cíl:** Zaměstnanec připravuje více souborů k pracovnímu úkolu.

**Volba a varianta:** Soubor „zadani-orion.pdf“ má být přílohou tohoto úkolu; pouhý Image by nezajistil výběr ani podmínky přijetí. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „zadani-orion.pdf“ použijte pojmenování „Podklady k úkolu“. Akce „Přidat podklady“ zpřístupní výběr i bez tažení. Přijatý soubor má type=accepted a odmítnutý type=rejected s konkrétním důvodem. Přijetí do seznamu ještě neznamená serverové uložení; průběh a výsledek přenosu musí být určeny odděleně.

**Výjimka a návrat:** Souhrnné invalid nenahrazuje určení, který soubor a proč nebyl přijat.

**Nevhodně:** Neoznačovat místně přijatý soubor za úspěšně nahraný.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník příloh, prezentaci omezení a tón chybových zpráv a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené typy, velikosti, počty, způsob přenosu a skutečný stav serverového uložení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2956-157)
