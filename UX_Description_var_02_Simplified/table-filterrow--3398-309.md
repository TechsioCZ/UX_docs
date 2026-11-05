# Table.FilterRow

Řádek filtrů DataTable omezuje výsledky podle datového typu a významu jednotlivých sloupců.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Typ ovladače a operátor odpovídají datům daného sloupce. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Table. Typ ovladače a operátor odpovídají datům daného sloupce.

## Kdy zvolit alternativu

Pokud tabulka slouží pouze ke čtení, nepřidávejte zbytečně filtrovací řádek. Globální dotaz patří do nástroje hledání; podmínka konkrétního sloupce sem.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zadat podmínku ve správném sloupci a odpovídajícím datovém typu; změnu vztáhnout na stejný soubor výsledků.

### Co vyvolávat nemá

- Neodstranit nevyhovující záznamy a nevyžadovat hodnotu pro operátor je prázdné či není prázdné.

### Přechody a odpovědnost

Po změně podmínky aplikace přepočítá nebo znovu načte tentýž soubor výsledků a opraví neexistující aktuální stránku. Čekání, nulová shoda a selhání jsou různé výsledky. Zrušení rozepsané podmínky ji nepoužije; odstranění aktivního filtru obnoví příslušný širší rozsah bez odstranění dat.

### Konkrétní pravidla použití

- Typ ovladače a operátor odpovídají datům daného sloupce.
- Výsledek filtru a stránkování musí zůstat vzájemně konzistentní.
- Nulovou shodu nevydávejte za chybu načtení.
- Booleovský filtr používá třístavový výběr, výčet Select a vícenásobný výčet Combobox; všechny sloupce nepřevádějte na obyčejný textový vstup.
- Operátor patří do nabídky podmínek. Pro „je prázdné“ a „není prázdné“ se hodnota nezadává; ovladač musí pojmenovat aktivní podmínku.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Pole má stálý přístupný název, viditelný význam a propojené instrukce i konkrétní chybu. Zachovejte rozepsané hodnoty při odmítnutí. Klávesnicové ovládání a čtení nesmí záviset jen na hoveru; delší text či jednotka nepřekrývají ovladače.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Jde o podmínku konkrétního sloupce; globální dotaz patří do hledání Toolbar. V průchodu se uplatní `size=md`.

- **Společné výjimky a návrat:** Pro je prázdné se nezadává hodnota. Nulová shoda nabídne úpravu či zrušení filtru, chyba služby opakování; záznamy se neodstraňují.

- **Pravidlo použití:** Neodstranit nevyhovující záznamy a nevyžadovat hodnotu pro operátor je prázdné či není prázdné.

### ERP — seznam objednávek

**Situace a cíl:** Pracovník porovnává termíny, stav a částky objednávek.

**Průchod a výsledek:** Nastavte podmínku „Stav je Čeká na vyřízení“ v příslušném sloupci. Typ ovladače odpovídá typu dat; po použití se aktualizují výsledky i platný rozsah stránek.

### Web — zákaznické objednávky

**Situace a cíl:** Zákazník porovnává své již vytvořené objednávky.

**Průchod a výsledek:** Nastavte podmínku „Stav je Doručeno“ v příslušném sloupci. Typ ovladače odpovídá typu dat; po použití se aktualizují výsledky i platný rozsah stránek.

### Interní systém — ITSM přehled

**Situace a cíl:** Koordinátor třídí a porovnává požadavky podpory.

**Průchod a výsledek:** Nastavte podmínku „Řešitel je Jana Nováková“ v příslušném sloupci. Typ ovladače odpovídá typu dat; po použití se aktualizují výsledky i platný rozsah stránek.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3398-309)
