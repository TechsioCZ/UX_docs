# Hotkeys

Nápověda klávesových zkratek zobrazuje kombinaci kláves v zápisu vhodném pro platformu.

Cílem je pomoci zkušenému uživateli najít a použít skutečně dostupnou klávesovou zkratku.

## Kdy použít

Jako doplněk skutečně dostupného příkazu pro opakovanou práci. Zkratka se zobrazí u stejného příkazu, kterému je přiřazena; dostupný zůstává i pojmenovaný ovladač. Nápověda zkratky sama příkaz neregistruje.

## Kdy zvolit alternativu

Běžné pojmenované tlačítko nebo odkaz ponechte jako dostupnou cestu bez znalosti zkratky.

## Anatomie, stavy a varianty

Jedna klávesa nebo kombinace s platformním zápisem. Jde o prezentaci skutečné zkratky; registraci a spuštění příkazu řeší aplikace.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `type=single` | Pro jedinou klávesu bez kombinace. |
| `type=compound` | Pro skutečnou kombinaci kláves vykonávající jednu určenou akci. |
| `platform=auto` | Zápis odpovídající skutečně registrované zkratce pro platformu auto; auto neznamená automatickou registraci a custom potřebuje skutečné mapování. |
| `platform=mac` | Zápis odpovídající skutečně registrované zkratce pro platformu mac; auto neznamená automatickou registraci a custom potřebuje skutečné mapování. |
| `platform=windows` | Zápis odpovídající skutečně registrované zkratce pro platformu windows; auto neznamená automatickou registraci a custom potřebuje skutečné mapování. |
| `platform=linux` | Zápis odpovídající skutečně registrované zkratce pro platformu linux; auto neznamená automatickou registraci a custom potřebuje skutečné mapování. |
| `platform=custom` | Zápis odpovídající skutečně registrované zkratce pro platformu custom; auto neznamená automatickou registraci a custom potřebuje skutečné mapování. |

**Dostupné kombinace:** Zachycená reference má single s platform=auto/mac/windows/linux a compound pouze s platform=custom. Osy type a platform nelze libovolně násobit; compound+auto není doložený master. Zkratky v příkladech jsou podmíněné modely produktu, nikoli výchozí registrace DS.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zobrazit odpovídající kombinaci pro prostředí uživatele.
- Ponechat běžný ovladač stejné akce dostupný bez znalosti zkratky.

### Co vyvolávat nemá

- Neslibovat zkratku, která není registrovaná.
- Nezobrazovat systémově konfliktní kombinaci jako jedinou cestu k operaci.

### Přechody a odpovědnost

Informace se mění podle skutečného údaje nebo stavu svého zdroje. Čtení, barva či hover neprovádí příkaz. Aplikace rozliší dosud neznámou hodnotu, známý výsledek a případnou chybu; použije jen odpovídající doložené varianty této komponenty. Obnovení dat aktualizuje text i vizuální význam společně; případnou nápravu nebo další krok poskytne samostatný pojmenovaný ovladač.

### Konkrétní pravidla použití

- Zápis kombinace přizpůsobte platformě.
- Zkratka musí odpovídat skutečné akci a kontextu, ve kterém funguje.
- Komponenta pouze zobrazuje kombinaci; její registraci, konflikty a dostupnost řídí aplikace.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Informace je srozumitelná bez samotné barvy či symbolu a bez přidávání zbytečné zastávky fokusu. Důležitá změna výsledku nesmí být dostupná pouze jako krátké vizuální probliknutí. Text, měna, jednotka či zkratka odpovídají konkrétnímu prostředí a jazyku.

## Omezení a příklady podle typu projektu

### ERP — práce s doklady

**Situace a cíl:** Operátor často vyhledává doklad z horního panelu.

**Volba a varianta:** Pro „Vyhledat doklad“ se sděluje zkratka existujícího příkazu vedle dostupného ovladače. V průchodu se uplatní `type=compound`, `platform=custom`.

**Průchod a výsledek:** Příklad předpokládá, že projekt k příkazu „Vyhledat doklad“ skutečně přiřadil Ctrl+K. Použijte type=compound, platform=custom a zobrazte odpovídající kombinaci u stejného viditelného ovladače. Registraci, platný rozsah a případné kolize řeší aplikace. Aktivace zkratky má stejný výsledek jako tento ovladač; samotná nápověda jej nevyvolává.

**Výjimka a návrat:** V textovém poli se zkratka nesmí plést s běžným zadáváním nebo přepsat rozepsaný doklad.

**Nevhodně:** Neslibovat zkratku, která není registrovaná.

### Web — editor obsahu

**Situace a cíl:** Redaktor chce rychle uložit koncept článku.

**Volba a varianta:** Pro „Uložit koncept“ se sděluje zkratka existujícího příkazu vedle dostupného ovladače. V průchodu se uplatní `type=compound`, `platform=custom`.

**Průchod a výsledek:** Příklad předpokládá, že projekt k příkazu „Uložit koncept“ skutečně přiřadil Ctrl+S. Použijte type=compound, platform=custom a zobrazte odpovídající kombinaci u stejného viditelného ovladače. Registraci, platný rozsah a případné kolize řeší aplikace. Aktivace zkratky má stejný výsledek jako tento ovladač; samotná nápověda jej nevyvolává.

**Výjimka a návrat:** Zobrazení kláves neznamená automatické uložení; selhání musí zůstat viditelné.

**Nevhodně:** Neslibovat zkratku, která není registrovaná.

### Interní systém — projektový nástroj

**Situace a cíl:** Uživatel otevírá paletu příkazů v prostředí Windows nebo macOS.

**Volba a varianta:** Pro „Otevřít příkazy“ se sděluje zkratka existujícího příkazu vedle dostupného ovladače. V průchodu se uplatní `type=compound`, `platform=custom`.

**Průchod a výsledek:** Příklad předpokládá, že projekt k příkazu „Otevřít příkazy“ skutečně přiřadil Ctrl+K ve Windows nebo ⌘+K v macOS. Použijte type=compound, platform=custom a zobrazte odpovídající kombinaci u stejného viditelného ovladače. Registraci, platný rozsah a případné kolize řeší aplikace. Aktivace zkratky má stejný výsledek jako tento ovladač; samotná nápověda jej nevyvolává.

**Výjimka a návrat:** Custom použijte jen s reálným mapováním; pouhá změna textu nevytvoří novou zkratku.

**Nevhodně:** Neslibovat zkratku, která není registrovaná.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit způsob zápisu kláves, názvy systémových kláves a jednotný styl nápovědy a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí mapování kláves, dostupnost v konkrétním prostředí a ochranu rozepsaného textu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3320-2)
