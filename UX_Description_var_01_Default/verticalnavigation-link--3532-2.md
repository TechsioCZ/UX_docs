# VerticalNavigation/Link

Odkaz VerticalNavigation vede na konkrétní stránku a odlišuje aktuální cíl.

**Vazba:** VerticalNavigation. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Pojmenujte skutečný navigační cíl. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě VerticalNavigation. Pojmenujte skutečný navigační cíl.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v VerticalNavigation a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **VerticalNavigation**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `state=base` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=focus` | Při skutečném klávesnicovém fokusu. Poloha fokusu zůstává odlišitelná od vybrané hodnoty a aktivace. |
| `state=current` | Pouze pro právě zobrazený navigační cíl. Neoznačuje navštívení v minulosti ani dokončený úkol. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít konkrétní pojmenovanou stránku a označit skutečný aktuální cíl.

### Co vyvolávat nemá

- Nepovažovat pouhé otevření rodičovské větve za návštěvu cíle.

### Přechody a odpovědnost

Aktuální stránka odpovídá current, nikoli jen poslednímu hoveru. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Pojmenujte skutečný navigační cíl.
- Current znamená aktuální stránku, nikoli pouze otevřenou nadřazenou větev.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

### ERP — navigace nákupní agendy

**Situace a cíl:** Pracovník chce z detailu objednávky přejít do přehledu dodavatelů.

**Volba a varianta:** Link otevírá stránku; Branch pouze zpřístupní potomky a TreeView vybírá data. V průchodu se uplatní `state=base`.

**Průchod a výsledek:** Odkaz v cestě „Nákup / Dodavatelé“ otevře odpovídající pojmenovanou stránku. Current se řídí skutečně zobrazeným cílem; otevření nadřazené větve není jeho aktivací.

**Výjimka a návrat:** Při nedostupném cíli vysvětlete problém a zachovejte cestu zpět. Disabled nesmí zůstat účinným odkazem jen s jinou barvou.

**Nevhodně:** Nepovažovat pouhé otevření rodičovské větve za návštěvu cíle.

### Web — zákaznický účet

**Situace a cíl:** Uživatel přechází mezi svými objednávkami a kontaktními údaji.

**Volba a varianta:** Link otevírá stránku; Branch pouze zpřístupní potomky a TreeView vybírá data. V průchodu se uplatní `state=base`.

**Průchod a výsledek:** Odkaz v cestě „Můj účet / Objednávky“ otevře odpovídající pojmenovanou stránku. Current se řídí skutečně zobrazeným cílem; otevření nadřazené větve není jeho aktivací.

**Výjimka a návrat:** Při nedostupném cíli vysvětlete problém a zachovejte cestu zpět. Disabled nesmí zůstat účinným odkazem jen s jinou barvou.

**Nevhodně:** Nepovažovat pouhé otevření rodičovské větve za návštěvu cíle.

### Interní systém — projektový portál

**Situace a cíl:** Člen týmu prochází sekce projektu.

**Volba a varianta:** Link otevírá stránku; Branch pouze zpřístupní potomky a TreeView vybírá data. V průchodu se uplatní `state=base`.

**Průchod a výsledek:** Odkaz v cestě „Projekt Orion / Dokumenty“ otevře odpovídající pojmenovanou stránku. Current se řídí skutečně zobrazeným cílem; otevření nadřazené větve není jeho aktivací.

**Výjimka a návrat:** Při nedostupném cíli vysvětlete problém a zachovejte cestu zpět. Disabled nesmí zůstat účinným odkazem jen s jinou barvou.

**Nevhodně:** Nepovažovat pouhé otevření rodičovské větve za návštěvu cíle.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit informační architekturu značky, názvy sekcí a vizuální hierarchii current/currentPath a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí cílové adresy, viditelnost podle role a zachování práce při přechodu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3532-2)
