# StatusText

Doprovodná zpráva vysvětluje stav nebo požadavek u konkrétního prvku.

Cílem je porozumět nápovědě nebo konkrétnímu výsledku kontroly údaje a vědět, co udělat dál.

## Kdy použít

Když je třeba u konkrétního údaje sdělit instrukci, zjištěnou chybu, upozornění nebo výsledek kontroly. Zpráva musí vysvětlit následující krok. Nejde o náhradu labelu ani o mizející Toast celé transakce.

## Kdy zvolit alternativu

Pro dostupnost produktu použijte AvailabilityStatus.

## Anatomie, stavy a varianty

Text nápovědy nebo zprávy s odpovídajícím status a velikostí. Je propojený se správným údajem či úkolem; barva a symbol jsou podpůrné.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `status=default` | Běžná instrukce nebo nápověda bez tvrzení o chybě či úspěšném dokončení. |
| `status=error` | Po zjištění konkrétního opravitelného problému. Zpráva pojmenuje údaj a nápravu; rozepsaná hodnota zůstane k opravě. |
| `status=success` | Po skutečném ověření údaje v daném kontextu. Neznamená automaticky úspěšné uložení celého formuláře. |
| `status=warning` | Pro skutečnou podmínku vyžadující pozornost, při které je pokračování možné. Blokující chyba patří do error/invalid. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Vysvětlit formát, opravitelnou chybu, skutečný úspěch nebo podstatné upozornění.
- Propojit zprávu se správným polem či úkolem.

### Co vyvolávat nemá

- Nepřevádět technický výpadek služby na tvrzení, že uživatel zadal špatný údaj.
- Nevydávat barvu success za potvrzení celé transakce.

### Přechody a odpovědnost

Informace se mění podle skutečného údaje nebo stavu svého zdroje. Čtení, barva či hover neprovádí příkaz. Aplikace rozliší dosud neznámou hodnotu, známý výsledek a případnou chybu; použije jen odpovídající doložené varianty této komponenty. Obnovení dat aktualizuje text i vizuální význam společně; případnou nápravu nebo další krok poskytne samostatný pojmenovaný ovladač.

### Konkrétní pravidla použití

- Zprávu přiřaďte správnému ovladači.
- Chyba vysvětlí problém a proveditelnou opravu; úspěch popisuje skutečně dokončený výsledek.
- Barva ani ikona nenahrazují srozumitelný text.
- Samotná varianta zprávy neurčuje validaci ani její oznámení čtečce.

## Obsah a pojmenování

Zpráva pojmenuje konkrétní výsledek či problém a dostupný další krok. Úspěch se vztahuje jen ke skutečně ověřené operaci; chyba údaje se neplete s výpadkem služby. Proměnné identifikují správný objekt a jeho skutečnou hodnotu.

## Přístupnost a prostředí

Informace je srozumitelná bez samotné barvy či symbolu a bez přidávání zbytečné zastávky fokusu. Důležitá změna výsledku nesmí být dostupná pouze jako krátké vizuální probliknutí. Text, měna, jednotka či zkratka odpovídají konkrétnímu prostředí a jazyku.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nepřevádět technický výpadek služby na tvrzení, že uživatel zadal špatný údaj.

### ERP — validace dokladu

**Situace a cíl:** Pracovník odeslal formulář s chybějícím interním číslem.

**Volba a varianta:** Pro „Doplňte interní číslo dokladu“ se sděluje místní výsledek kontroly nebo oprava údaje; Toast by neměl nahradit místní zprávu. V průchodu se uplatní `status=error`.

**Průchod a výsledek:** Pro objekt „Číslo dokladu“ použijte pojmenování „Doplňte interní číslo dokladu“. Použijte status=error pouze po zjištění příslušného výsledku kontroly. Text spojte s odpovídajícím polem, popište konkrétní opravu nebo rozsah úspěchu. Nepřesouvejte chybu jiného pole či výpadek služby na správně zadanou hodnotu.

**Výjimka a návrat:** Výpadek ukládání není důvod označit správně vyplněné číslo jako neplatné.

### Web — rezervace služby

**Situace a cíl:** Návštěvník vybral termín mimo nabízený rozsah.

**Volba a varianta:** Pro „Vyberte některý z dostupných termínů“ se sděluje místní výsledek kontroly nebo oprava údaje; Toast by neměl nahradit místní zprávu. V průchodu se uplatní `status=error`.

**Průchod a výsledek:** Pro objekt „Termín rezervace“ použijte pojmenování „Vyberte některý z dostupných termínů“. Použijte status=error pouze po zjištění příslušného výsledku kontroly. Text spojte s odpovídajícím polem, popište konkrétní opravu nebo rozsah úspěchu. Nepřesouvejte chybu jiného pole či výpadek služby na správně zadanou hodnotu.

**Výjimka a návrat:** Warning se nepoužije k zakrytí blokující chyby, která nedovolí pokračovat.

### Interní systém — projektový formulář

**Situace a cíl:** Uživatel úspěšně ověřil dostupnost názvu projektu.

**Volba a varianta:** Pro „Název je dostupný“ se sděluje místní výsledek kontroly nebo oprava údaje; Toast by neměl nahradit místní zprávu. V průchodu se uplatní `status=success`.

**Průchod a výsledek:** Pro objekt „Název projektu Orion“ použijte pojmenování „Název je dostupný“. Použijte status=success pouze po zjištění příslušného výsledku kontroly. Text spojte s odpovídajícím polem, popište konkrétní opravu nebo rozsah úspěchu. Nepřesouvejte chybu jiného pole či výpadek služby na správně zadanou hodnotu.

**Výjimka a návrat:** Zpráva neznamená, že celý projekt už vznikl nebo byl uložen.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit tón nápověd, slovník chyb a sémantické tokeny zpráv a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí spouštěče validace, obsah podmínky a dostupnou cestu k nápravě. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-19238)
