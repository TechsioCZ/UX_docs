# FormTextarea

Formulářové víceřádkové pole spojuje delší text s popiskem a zprávou.

Cílem je zadat souvislý víceřádkový text a zachovat možnost jej přečíst a opravit.

## Kdy použít

Pro delší formulářovou odpověď se stálým názvem a místní chybovou zprávou. Obsah musí být dostupný celý i na menší ploše. Nezaměňujte Enter za odeslání ani placeholder za label.

## Kdy zvolit alternativu

Pro jednořádkový údaj použijte FormInput, pro vlastní skladbu Textarea.

## Anatomie, stavy a varianty

Pojmenovaný víceřádkový vstup se související nápovědou a validační zprávou. Rows a resize řeší prostor pro odpověď, nikoli její automatické potvrzení.

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
| `required=false` | Když lze údaj vědomě nevyplnit; absence není automaticky chyba. |
| `required=true` | Když proces skutečně vyžaduje údaj. Stejná podmínka platí ve validaci. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Psát, vkládat a upravovat delší odpověď.
- Zpřístupnit celý text při změně výšky nebo nedostatku místa.

### Co vyvolávat nemá

- Nepovažovat nový řádek za odeslání formuláře.
- Nezkracovat dlouhou odpověď bez vysvětleného datového omezení.

### Přechody a odpovědnost

Psaní mění draft, ne potvrzený záznam. Kontrolu spusťte v určeném okamžiku, například při odeslání; konkrétní odmítnutí zachová text a vysvětlí opravu u stejného pole. Po nové platné kontrole chybové sdělení zanikne nebo se nahradí aktuálním výsledkem. Zrušení formuláře musí mít určené zachování či zahození draftu. Tyto kroky řídí formulář a aplikace, nikoli samotná barva vstupu.

### Konkrétní pravidla použití

- Popisek určuje očekávaný obsah; případný limit musí být skutečný.
- U delšího textu zachovejte čitelnost a dostupnost celého obsahu.
- Chybu vysvětlete u pole.
- Readonly je popsané v kódu bez samostatné vizuální varianty; neodvozujte jeho podporu pouze z nabídky stavů Figmy.
- Počet výchozích řádků volte podle očekávané odpovědi. Povolené resize musí zachovat použitelnost okolního formuláře.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Pole má stálý přístupný název, viditelný význam a propojené instrukce i konkrétní chybu. Zachovejte rozepsané hodnoty při odmítnutí. Klávesnicové ovládání a čtení nesmí záviset jen na hoveru; delší text či jednotka nepřekrývají ovladače.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Pravidlo použití:** Nepovažovat nový řádek za odeslání formuláře.

### ERP — poznámka k zakázce

**Situace a cíl:** Pracovník doplňuje vysvětlení nestandardního průběhu zakázky.

**Volba a varianta:** Údaj „Poznámka k zakázce“ je víceřádkový popis; krátký Input by ztížil čtení celého textu. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pod názvem „Poznámka k zakázce“ vzniká draft „Dodat materiál po etapách podle dohody.“. Enter přidává řádek. Až určená kontrola může označit skutečný problém pomocí `state=error`; text zůstane celý k opravě. Po opravě a úspěšné kontrole se chyba odstraní. Uložení obsahu provádí určené potvrzení formuláře.

**Výjimka a návrat:** Po odmítnutí formuláře se neztratí dlouhá vložená poznámka.

### Web — zákaznický dotaz

**Situace a cíl:** Návštěvník popisuje potíže s konkrétním výrobkem.

**Volba a varianta:** Údaj „Popis dotazu“ je víceřádkový popis; krátký Input by ztížil čtení celého textu. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pod názvem „Popis dotazu“ vzniká draft „Výrobek po zapnutí zobrazuje přerušované světlo.“. Enter přidává řádek. Až určená kontrola může označit skutečný problém pomocí `state=error`; text zůstane celý k opravě. Po opravě a úspěšné kontrole se chyba odstraní. Uložení obsahu provádí určené potvrzení formuláře.

**Výjimka a návrat:** Je-li skutečně stanoven limit, zpráva vysvětlí překročení; samotná viditelná výška není limit znaků.

### Interní systém — ITSM incident

**Situace a cíl:** Řešitel zapisuje víceřádkový průběh řešení.

**Volba a varianta:** Údaj „Průběh řešení“ je víceřádkový popis; krátký Input by ztížil čtení celého textu. V průchodu se uplatní `state=default`, `required=false`.

**Průchod a výsledek:** Pod názvem „Průběh řešení“ vzniká draft „Ověření připojení a následný restart služby.“. Enter přidává řádek. Až určená kontrola může označit skutečný problém pomocí `state=error`; text zůstane celý k opravě. Po opravě a úspěšné kontrole se chyba odstraní. Uložení obsahu provádí určené potvrzení formuláře.

**Výjimka a návrat:** Enter vloží řádek a resize nepřekryje ukládací akci nebo sousední pole.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit tón popisků a nápověd, pravidla dlouhého textu a použití borderless a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povinnost, povolený rozsah textu, výchozí počet řádků a způsob změny rozměru. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-22805)
