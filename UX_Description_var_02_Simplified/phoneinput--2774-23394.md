# PhoneInput

Telefonní pole spojuje předvolbu země s telefonním číslem.

Cílem je zadat telefon s jednoznačným mezinárodním významem a případně jej opravit.

## Kdy použít

Pro telefon s jasným zemským kontextem a účelem kontaktování. Formátová kontrola není ověření dosažitelnosti. Číselník země nesmí při opravě tiše změnit význam celého čísla.

## Kdy zvolit alternativu

Pro obecné číselné hodnoty použijte NumericInput.

## Anatomie, stavy a varianty

Telefonní vstup se zemským kontextem a s ním spojeným popiskem a zprávou. Kontrola formátu není ověření dosažitelnosti kontaktu.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=error` | Po zjištění konkrétního opravitelného problému. Zpráva pojmenuje údaj a nápravu; rozepsaná hodnota zůstane k opravě. |
| `state=success` | Po skutečném ověření údaje v daném kontextu. Neznamená automaticky úspěšné uložení celého formuláře. |
| `state=warning` | Pro skutečnou podmínku vyžadující pozornost, při které je pokračování možné. Blokující chyba patří do error/invalid. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=readonly` | Když má být existující hodnota čitelná, ale není dovoleno ji měnit. Nezaměňovat za disabled ani za prázdnou hodnotu. |
| `required=false` | Když lze údaj vědomě nevyplnit; absence není automaticky chyba. |
| `required=true` | Když proces skutečně vyžaduje údaj. Stejná podmínka platí ve validaci. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Vybrat odpovídající zemský kontext a upravit telefonní číslo.
- Odlišit kontrolu formátu od skutečného ověření dosažitelnosti.

### Co vyvolávat nemá

- Nezaměňovat správný formát za ověřený kontakt.
- Nepřepisovat smysl čísla automatickou změnou země bez rozpoznatelného výsledku.

### Přechody a odpovědnost

Psaní mění draft, ne potvrzený záznam. Kontrolu spusťte v určeném okamžiku, například při odeslání; konkrétní odmítnutí zachová text a vysvětlí opravu u stejného pole. Po nové platné kontrole chybové sdělení zanikne nebo se nahradí aktuálním výsledkem. Zrušení formuláře musí mít určené zachování či zahození draftu. Tyto kroky řídí formulář a aplikace, nikoli samotná barva vstupu.

### Konkrétní pravidla použití

- Zemi identifikujte názvem a předvolbou, nikoli pouze vlajkou.
- Přijměte vložení celého čísla bez nechtěné ztráty předvolby.
- Změna země nemá tiše odstranit uživatelem zadanou hodnotu.
- Formátová platnost neznamená ověření vlastnictví čísla.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Pole má stálý přístupný název, viditelný význam a propojené instrukce i konkrétní chybu. Zachovejte rozepsané hodnoty při odmítnutí. Klávesnicové ovládání a čtení nesmí záviset jen na hoveru; delší text či jednotka nepřekrývají ovladače.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nezaměňovat správný formát za ověřený kontakt.

### ERP — kontaktní osoba dodavatele

**Situace a cíl:** Pracovník zadává telefon kontaktní osoby v zahraničí.

**Volba a varianta:** Údaj „Telefon kontaktní osoby“ je telefon se zemským kontextem; NumericInput by mohl ztratit jeho význam. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „+420 777 123 456“ použijte pojmenování „Telefon kontaktní osoby“. Začněte state=default a dovolte rozepsání i opravu. Konkrétní chybu ukažte po určené smysluplné kontrole, například při odeslání; error se zobrazí se zprávou u téhož pole a zachová draft. Úspěšná kontrola údaje nepotvrzuje uložení celého formuláře. Prázdné dosud nevyplňované pole nezbarvujte chybově hned při otevření.

**Výjimka a návrat:** Lokálně platné číslo bez potřebného kontextu se nevydává za ověřenou mezinárodní adresu.

### Web — rezervace služby

**Situace a cíl:** Návštěvník zadává kontakt pro změnu termínu.

**Volba a varianta:** Údaj „Kontaktní telefon“ je telefon se zemským kontextem; NumericInput by mohl ztratit jeho význam. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „+420 777 123 456“ použijte pojmenování „Kontaktní telefon“. Začněte state=default a dovolte rozepsání i opravu. Konkrétní chybu ukažte po určené smysluplné kontrole, například při odeslání; error se zobrazí se zprávou u téhož pole a zachová draft. Úspěšná kontrola údaje nepotvrzuje uložení celého formuláře. Prázdné dosud nevyplňované pole nezbarvujte chybově hned při otevření.

**Výjimka a návrat:** Success formátu neznamená, že už proběhlo potvrzení zprávou nebo telefonátem.

### Interní systém — zaměstnanecký adresář

**Situace a cíl:** Zaměstnanec mění pracovní telefon.

**Volba a varianta:** Údaj „Pracovní telefon“ je telefon se zemským kontextem; NumericInput by mohl ztratit jeho význam. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pro objekt „+420 777 123 456“ použijte pojmenování „Pracovní telefon“. Začněte state=default a dovolte rozepsání i opravu. Konkrétní chybu ukažte po určené smysluplné kontrole, například při odeslání; error se zobrazí se zprávou u téhož pole a zachová draft. Úspěšná kontrola údaje nepotvrzuje uložení celého formuláře. Prázdné dosud nevyplňované pole nezbarvujte chybově hned při otevření.

**Výjimka a návrat:** Při odmítnutí zůstane zadaný kontakt k opravě a není tiše nahrazen dřívějším.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit zápis názvů zemí, formát zobrazeného telefonu a tón instrukcí a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povinnost kontaktu, povolené země, validaci a případné skutečné ověření. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-23394)
