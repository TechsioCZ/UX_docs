# VerticalNavigation/Branch

Větev VerticalNavigation zpřístupňuje vnořené navigační cíle; otevření větve nemusí měnit stránku.

**Vazba:** VerticalNavigation. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Otevírá vnořené cíle. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě VerticalNavigation. Otevírá vnořené cíle.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v VerticalNavigation a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **VerticalNavigation**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `open=false` | Když je uzavřená; při zavření zůstává logická návaznost na spouštěč. |
| `open=true` | Když je panel či větev skutečně otevřená. |
| `state=base` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=focus` | Při skutečném klávesnicovém fokusu. Poloha fokusu zůstává odlišitelná od vybrané hodnoty a aktivace. |
| `state=currentPath` | Pro předka skutečně aktuální stránky. Samotné rozbalení větve z ní currentPath neudělá. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít nebo zavřít nabídku podřízených navigačních cílů.

### Co vyvolávat nemá

- Nesloučit rozbalení s nepojmenovanou změnou stránky.

### Přechody a odpovědnost

CurrentPath zůstává údaj o předkovi skutečné stránky a nezávisí pouze na otevření. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Otevírá vnořené cíle.
- Otevření větve samo nemusí změnit stránku; currentPath a current jsou rozdílné informace.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Branch ovládá viditelnost potomků; Link přechází na konkrétní stránku. V průchodu se uplatní `open=false`, `state=base`.

- **Společné výjimky a návrat:** Sbalení nesmí uvěznit fokus v neviditelném odkazu. Samostatný přechod na stránku rodiče potřebuje odlišený pojmenovaný cíl.

- **Pravidlo použití:** Nesloučit rozbalení s nepojmenovanou změnou stránky.

### ERP — navigace nákupní agendy

**Situace a cíl:** Pracovník chce z detailu objednávky přejít do přehledu dodavatelů.

**Průchod a výsledek:** U navigační oblasti „Nákup / Dodavatelé“ otevřete potomky větve. Aktuální stránka se tím nezmění; její předek může nést currentPath nezávisle na otevření.

### Web — zákaznický účet

**Situace a cíl:** Uživatel přechází mezi svými objednávkami a kontaktními údaji.

**Průchod a výsledek:** U navigační oblasti „Můj účet / Objednávky“ otevřete potomky větve. Aktuální stránka se tím nezmění; její předek může nést currentPath nezávisle na otevření.

### Interní systém — projektový portál

**Situace a cíl:** Člen týmu prochází sekce projektu.

**Průchod a výsledek:** U navigační oblasti „Projekt Orion / Dokumenty“ otevřete potomky větve. Aktuální stránka se tím nezmění; její předek může nést currentPath nezávisle na otevření.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit informační architekturu značky, názvy sekcí a vizuální hierarchii current/currentPath a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí cílové adresy, viditelnost podle role a zachování práce při přechodu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3538-167)
