# Select/StatusText

Stavová zpráva Select vysvětluje nápovědu, chybu, úspěch nebo upozornění související s výběrem.

**Vazba:** Select. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Default používá nápovědu, error vysvětluje neplatný výběr, success potvrzuje výsledek a warning upozorňuje na podmínku. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Select. Default používá nápovědu, error vysvětluje neplatný výběr, success potvrzuje výsledek a warning upozorňuje na podmínku.

## Kdy zvolit alternativu

Pro časově omezené oznámení celé operace zvažte Toast. Chyba jednoho pole má zůstat u tohoto pole; nepotvrzuje ani neblokuje jiný údaj.

## Anatomie, stavy a varianty

Součást skladby **Select**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `status=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `status=error` | Po zjištění konkrétního opravitelného problému. Zpráva pojmenuje údaj a nápravu; rozepsaná hodnota zůstane k opravě. |
| `status=success` | Po skutečném ověření údaje v daném kontextu. Neznamená automaticky úspěšné uložení celého formuláře. |
| `status=warning` | Pro skutečnou podmínku vyžadující pozornost, při které je pokračování možné. Blokující chyba patří do error/invalid. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Předat konkrétní informaci uvedenou v definici této části ve správné vazbě na Select.

### Co vyvolávat nemá

- Nepřidávat automaticky vlastní navigaci, uložení nebo jinou aktivaci pouhým kliknutím na text.

### Přechody a odpovědnost

Obsah či označení se aktualizuje až se změnou odpovídajícího údaje nebo stavu hostitele. Čtení, fokus okolního prvku ani zkrácení textu neprovádí obchodní akci. Chybějící nebo neaktuální údaj nesmí být nahrazen falešnou potvrzenou hodnotou; aplikace zachová kontext a nabídne nápravu v samostatném ovladači, pokud je možná.

### Konkrétní pravidla použití

- Default používá nápovědu, error vysvětluje neplatný výběr, success potvrzuje výsledek a warning upozorňuje na podmínku.
- Zprávu propojte se správným polem; nenahrazuje jeho popisek.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Text přiřaďte ke správnému objektu nebo ovladači. Nezavádějte samostatný fokus jen kvůli stylování. Při zkrácení zachovejte přístup k celému důležitému významu a při lokalizaci prostor pro delší znění.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Zpráva patří stejnému údaji či řádku; mizející Toast by ztížil místní opravu. V průchodu se uplatní `status=error`.

- **Společné výjimky a návrat:** Prázdné dosud nevyplňované pole není chybou hned při otevření. Odmítnutí zachová ostatní údaje a umožní vrátit se k výběru.

- **Nevhodné použití:** Přidat samotnému textu nepojmenované ukládání, odstranění nebo přesměrování.

### ERP — zakázkový formulář

**Situace a cíl:** Uživatel odeslal formulář, ale povinné pole „Středisko“ zůstalo bez výběru.

**Průchod a výsledek:** Při odeslání povinného pole „Středisko“ bez výběru zobrazte „Vyberte středisko.“ ve status=error. Zpráva patří tomuto poli; po potvrzení dostupné hodnoty „Logistika“ a platné kontrole chybové sdělení odstraňte.

### Web — nastavení doručení

**Situace a cíl:** Uživatel odeslal formulář, ale povinné pole „Země doručení“ zůstalo bez výběru.

**Průchod a výsledek:** Při odeslání povinného pole „Země doručení“ bez výběru zobrazte „Vyberte zemi doručení.“ ve status=error. Zpráva patří tomuto poli; po potvrzení dostupné hodnoty „Česko“ a platné kontrole chybové sdělení odstraňte.

### Interní systém — ITSM

**Situace a cíl:** Uživatel odeslal formulář, ale povinné pole „Priorita požadavku“ zůstalo bez výběru.

**Průchod a výsledek:** Při odeslání povinného pole „Priorita požadavku“ bez výběru zobrazte „Vyberte prioritu požadavku.“ ve status=error. Zpráva patří tomuto poli; po potvrzení dostupné hodnoty „Běžná“ a platné kontrole chybové sdělení odstraňte.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník popisků a možností, vizuální styl polí a způsob značení povinnosti a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené hodnoty, výchozí volbu, povinnost údaje a okamžik validace. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-24629)
