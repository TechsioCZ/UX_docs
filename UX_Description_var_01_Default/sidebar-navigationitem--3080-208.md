# Sidebar.NavigationItem

Navigační položka Sidebar vede na pojmenovanou stránku a zachovává její identitu i ve sbaleném rámu.

**Vazba:** Sidebar. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Název, ikona a cíl popisují tutéž stránku. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Sidebar. Název, ikona a cíl popisují tutéž stránku.

## Kdy zvolit alternativu

Pro samotné přechody mezi stránkami postačí VerticalNavigation. Pro dočasný kontextový úkol použijte Drawer; tato část zůstává součástí navigačního rámu.

## Anatomie, stavy a varianty

Součást skladby **Sidebar**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `collapsed=false` | Pro plnou čitelnou podobu položky. |
| `collapsed=true` | Pro sbalenou podobu se zachovaným názvem cíle. |
| `active=false` | Pro ostatní cíle; hover ani fokus nepřepínají tento údaj. |
| `active=true` | Jen pro skutečně aktuální navigační cíl. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=active` | Při probíhající aktivaci ovladače. Nezaměňovat tento interakční stav za trvalou vybranou hodnotu nebo active=true navigačního cíle. |
| `state=focus` | Při skutečném klávesnicovém fokusu. Poloha fokusu zůstává odlišitelná od vybrané hodnoty a aktivace. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít pojmenovaný navigační cíl; ve sbalení ponechat jeho název dostupný.

### Co vyvolávat nemá

- Nezaměnit aktivní vzhled za nezávislé schválení nebo dokončení úkolu.

### Přechody a odpovědnost

Obsah stránky, aktivní položka, viditelný label a tooltip souhlasí. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Název, ikona a cíl popisují tutéž stránku.
- Ve sbalení zachovejte dostupný název a shodný tooltip.
- Aktuální master překrývá Overview a Button; používejte jediný zdroj viditelného názvu.
- Disabled odkaz musí skutečně zamezit navigaci; současný podklad nemá zvláštní disabled barevné ošetření, proto se na barvu nespoléhejte.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

### ERP — víceagendová aplikace

**Situace a cíl:** Pracovník prochází nákup, sklad a související přehledy.

**Volba a varianta:** Položka naviguje, zatímco Sidebar.Trigger mění rám bez přechodu na jinou stránku. V průchodu se uplatní `collapsed=false`, `active=false`, `state=default`.

**Průchod a výsledek:** Položku „Objednávky“ pojmenujte podle skutečného cíle. Aktivací otevřete danou agendu a active sjednoťte se zobrazenou stránkou; v ikonovém sbalení zůstává stejný název i tooltip.

**Výjimka a návrat:** Zdrojové překrytí textových vrstev nesmí být vykládáno jako dva různé cíle. Disabled odkaz potřebuje skutečnou ochranu aktivace; pouhá barva nestačí.

**Nevhodně:** Nezaměnit aktivní vzhled za nezávislé schválení nebo dokončení úkolu.

### Web — zákaznický portál

**Situace a cíl:** Zákazník na telefonu otevírá přehled svého účtu.

**Volba a varianta:** Položka naviguje, zatímco Sidebar.Trigger mění rám bez přechodu na jinou stránku. V průchodu se uplatní `collapsed=false`, `active=false`, `state=default`.

**Průchod a výsledek:** Položku „Moje objednávky“ pojmenujte podle skutečného cíle. Aktivací otevřete danou agendu a active sjednoťte se zobrazenou stránkou; v ikonovém sbalení zůstává stejný název i tooltip.

**Výjimka a návrat:** Zdrojové překrytí textových vrstev nesmí být vykládáno jako dva různé cíle. Disabled odkaz potřebuje skutečnou ochranu aktivace; pouhá barva nestačí.

**Nevhodně:** Nezaměnit aktivní vzhled za nezávislé schválení nebo dokončení úkolu.

### Interní systém — projektový nástroj

**Situace a cíl:** Člen týmu přechází mezi pracovním seznamem a detaily projektu.

**Volba a varianta:** Položka naviguje, zatímco Sidebar.Trigger mění rám bez přechodu na jinou stránku. V průchodu se uplatní `collapsed=false`, `active=false`, `state=default`.

**Průchod a výsledek:** Položku „Projekt Orion“ pojmenujte podle skutečného cíle. Aktivací otevřete danou agendu a active sjednoťte se zobrazenou stránkou; v ikonovém sbalení zůstává stejný název i tooltip.

**Výjimka a návrat:** Zdrojové překrytí textových vrstev nesmí být vykládáno jako dva různé cíle. Disabled odkaz potřebuje skutečnou ochranu aktivace; pouhá barva nestačí.

**Nevhodně:** Nezaměnit aktivní vzhled za nezávislé schválení nebo dokončení úkolu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit šířkovou a vizuální hierarchii rámu, názvy cílů a pravidla zobrazení identity značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí nabídku agend, oprávnění, zvolený režim a zachování kontextu při změně zařízení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3080-208)
