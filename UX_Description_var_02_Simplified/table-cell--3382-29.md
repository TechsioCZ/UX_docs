# Table.Cell

Buňka tabulky zobrazuje nebo upravuje jednu hodnotu záznamu ve správném sloupci.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Hodnota patří správnému řádku a sloupci. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Hodnota patří správnému řádku a sloupci.

## Kdy zvolit alternativu

Pokud údaj nelze upravovat, ponechte čitelnou buňku bez editing. Pokud je třeba celý formulář s více souvisejícími údaji, otevřete určený detail nebo Drawer.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `align=start` | Pro běžný text na logickém začátku řádku. |
| `align=center` | Pro krátké srovnatelné symboly či hodnoty, pokud zůstává čitelné přiřazení ke sloupci. |
| `align=end` | Pro srovnávání číselných hodnot a jednotek na logickém konci. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=editing` | Když uživatel upravuje draft této buňky. Potvrzení a zrušení změny musí mít určený výsledek. |
| `state=error` | Když byl odmítnut draft této buňky nebo jeho uložení. Ponechat návrh a konkrétní chybu u stejného řádku a sloupce. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zobrazit hodnotu stejného sloupce a při povolené editaci přijmout její draft.

### Co vyvolávat nemá

- Neuložit jinou buňku a nevydávat pouhý přechod do editing za potvrzenou hodnotu.

### Přechody a odpovědnost

Čtení → výslovné zahájení editace → lokální draft → potvrzení. Úspěšné uložení nahradí hodnotu stejné buňky; odmítnutí přejde do jejího error a zachová návrh. Zrušení před potvrzením obnoví poslední uloženou hodnotu. Způsob potvrzení i případný konflikt souběžných změn určí aplikace; změna fokusu nesmí skrytě potvrdit jiný řádek.

### Konkrétní pravidla použití

- Hodnota patří správnému řádku a sloupci.
- V editačním režimu odlište draft, potvrzení a chybu konkrétní buňky.
- Chyba jedné hodnoty nesmí působit jako neplatnost jiného řádku.
- Zkrácenou hodnotu potřebnou pro rozhodnutí zpřístupněte celou i bez hoveru. Pinned chrání pevný sloupec před prosvítáním posouvaných buněk.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Pole má stálý přístupný název, viditelný význam a propojené instrukce i konkrétní chybu. Zachovejte rozepsané hodnoty při odmítnutí. Klávesnicové ovládání a čtení nesmí záviset jen na hoveru; delší text či jednotka nepřekrývají ovladače.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Buňka řeší jeden atribut záznamu; složitější úpravy otevřete v detailu nebo Drawer. V průchodu se uplatní `state=default`.

- **Společné výjimky a návrat:** Odmítnutí ponechá draft a error v této buňce; zrušení před potvrzením vrátí původní hodnotu. Dlouhý důležitý údaj zůstává dostupný celý i bez hoveru.

- **Pravidlo použití:** Neuložit jinou buňku a nevydávat pouhý přechod do editing za potvrzenou hodnotu.

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Průchod a výsledek:** U správného řádku zobrazte „12 500 Kč“. Pokud je zde skutečně povolená editace, uživatel ji výslovně zahájí, upraví draft a potvrdí. Teprve úspěšná odpověď nahradí uloženou hodnotu.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Průchod a výsledek:** U správného řádku zobrazte „1 490 Kč“. Pokud je zde skutečně povolená editace, uživatel ji výslovně zahájí, upraví draft a potvrdí. Teprve úspěšná odpověď nahradí uloženou hodnotu.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Průchod a výsledek:** U správného řádku zobrazte „Běžná priorita“. Pokud je zde skutečně povolená editace, uživatel ji výslovně zahájí, upraví draft a potvrdí. Teprve úspěšná odpověď nahradí uloženou hodnotu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3382-29)
