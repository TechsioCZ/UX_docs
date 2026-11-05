# NumericInput

Číselný vstup umožňuje zadat hodnotu a upravit ji krokovými ovladači.

Cílem je zadat přesné číslo s jasnou jednotkou, mezemi a chováním krokových ovladačů.

## Kdy použít

Pro skutečnou číselnou veličinu s jednotkou, přesností a případnými mezemi. Psaní musí připustit dočasný draft před kontrolou. Telefon, kód dokladu a identifikátor s úvodními nulami nejsou číselný výpočet.

## Kdy zvolit alternativu

Pro telefon použijte PhoneInput, pro produktové množství QuantityField a pro hotové pole s popiskem FormNumericInput.

## Anatomie, stavy a varianty

Číselný draft a případné krokové ovladače. Jednotka, meze a způsob potvrzení patří skutečnému použití; prázdný draft není automaticky nula.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=error` | Po zjištění konkrétního opravitelného problému. Zpráva pojmenuje údaj a nápravu; rozepsaná hodnota zůstane k opravě. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `state=readonly` | Když má být existující hodnota čitelná, ale není dovoleno ji měnit. Nezaměňovat za disabled ani za prázdnou hodnotu. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Psát číselný draft a podle nastavení měnit hodnotu krokem.
- Vysvětlit nepřípustnou hodnotu a umožnit opravu.

### Co vyvolávat nemá

- Nenahrazovat dočasně prázdný draft automaticky nulou nebo minimem.
- Nepoužívat na identifikátory, u kterých je nutné zachovat počáteční nuly.

### Přechody a odpovědnost

Psaní mění draft, ne potvrzený záznam. Kontrolu spusťte v určeném okamžiku, například při odeslání; konkrétní odmítnutí zachová text a vysvětlí opravu u stejného pole. Po nové platné kontrole chybové sdělení zanikne nebo se nahradí aktuálním výsledkem. Zrušení formuláře musí mít určené zachování či zahození draftu. Tyto kroky řídí formulář a aplikace, nikoli samotná barva vstupu.

### Konkrétní pravidla použití

- Jednotku a omezení uveďte, pokud nejsou z kontextu zřejmá.
- Rozlišujte prázdný draft, nulu a neplatné číslo.
- Readonly ponechává hodnotu ke čtení; disabled vyjadřuje nedostupnost ovladače.
- Číselný formát, validaci a uložení určuje aplikace.
- Na dosažené mezi zamezte kroku dále mimo povolený rozsah; ručně rozepsanou neplatnou hodnotu odlište od potvrzeného čísla.

## Obsah a pojmenování

Názvy údajů, částky nebo množství vztahujte ke stejné položce a jednotce. Měna či balení nezmizí při zkrácení. Ukázkové číslo z příkladu není výchozí hodnota ani limit projektu; jeho zdroj a přesnost určuje aplikace.

## Přístupnost a prostředí

Pole má stálý přístupný název, viditelný význam a propojené instrukce i konkrétní chybu. Zachovejte rozepsané hodnoty při odmítnutí. Klávesnicové ovládání a čtení nesmí záviset jen na hoveru; delší text či jednotka nepřekrývají ovladače.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nenahrazovat dočasně prázdný draft automaticky nulou nebo minimem.

### ERP — množství materiálu

**Situace a cíl:** Pracovník zadává požadovanou délku materiálu.

**Volba a varianta:** Údaj „Délka v metrech“ je číselná veličina s jednotkou; běžný text ani telefon by nevyjádřil meze a krok. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** Pro objekt „12,5 m“ použijte pojmenování „Délka v metrech“. Začněte state=default a dovolte rozepsání i opravu. Konkrétní chybu ukažte po určené smysluplné kontrole, například při odeslání; error se zobrazí se zprávou u téhož pole a zachová draft. Úspěšná kontrola údaje nepotvrzuje uložení celého formuláře. Prázdné dosud nevyplňované pole nezbarvujte chybově hned při otevření.

**Výjimka a návrat:** Neplatný draft zůstane čitelný a vysvětlení ukáže, jaký rozsah lze zadat.

### Web — konfigurátor služby

**Situace a cíl:** Návštěvník stanovuje počet účastníků nabídky.

**Volba a varianta:** Údaj „Počet účastníků“ je číselná veličina s jednotkou; běžný text ani telefon by nevyjádřil meze a krok. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** Pro objekt „3 osoby“ použijte pojmenování „Počet účastníků“. Začněte state=default a dovolte rozepsání i opravu. Konkrétní chybu ukažte po určené smysluplné kontrole, například při odeslání; error se zobrazí se zprávou u téhož pole a zachová draft. Úspěšná kontrola údaje nepotvrzuje uložení celého formuláře. Prázdné dosud nevyplňované pole nezbarvujte chybově hned při otevření.

**Výjimka a návrat:** Rozpracované vymazání hodnoty se nesmí ihned vrátit na předchozí číslo a znemožnit nové zadání.

### Interní systém — plánování kapacity

**Situace a cíl:** Vedoucí zadává plánovaný počet pracovních hodin.

**Volba a varianta:** Údaj „Plánovaná kapacita“ je číselná veličina s jednotkou; běžný text ani telefon by nevyjádřil meze a krok. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** Pro objekt „7,5 hodiny“ použijte pojmenování „Plánovaná kapacita“. Začněte state=default a dovolte rozepsání i opravu. Konkrétní chybu ukažte po určené smysluplné kontrole, například při odeslání; error se zobrazí se zprávou u téhož pole a zachová draft. Úspěšná kontrola údaje nepotvrzuje uložení celého formuláře. Prázdné dosud nevyplňované pole nezbarvujte chybově hned při otevření.

**Výjimka a návrat:** Readonly ponechá hodnotu dostupnou; disabled nesmí vypadat jako potvrzená nula.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit zápis čísel, jednotek a vzhled krokových ovladačů a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí meze, krok, desetinnou přesnost, pravidla zaokrouhlení a potvrzení hodnoty. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-14143)
