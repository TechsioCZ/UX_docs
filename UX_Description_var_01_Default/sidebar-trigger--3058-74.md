# Sidebar.Trigger

Spouštěč Sidebar mění otevření nebo sbalení konkrétního bočního rámu.

**Vazba:** Sidebar. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Ovládá právě příslušný rám. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Sidebar. Ovládá právě příslušný rám.

## Kdy zvolit alternativu

Pro samotné přechody mezi stránkami postačí VerticalNavigation. Pro dočasný kontextový úkol použijte Drawer; tato část zůstává součástí navigačního rámu.

## Anatomie, stavy a varianty

Součást skladby **Sidebar**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `size=md` | Pro běžnou hustotu a vztah k sousedním prvkům stejné skladby. |
| `size=sm` | Pro husté rozložení a krátký obsah; nezmenšit dostupnou aktivní plochu nebo čitelnost pod potřeby použití. |
| `size=lg` | Pro výraznější obsah nebo volnější rozložení; větší varianta nemění význam, oprávnění ani stav. |
| `tone=neutral` | Pro běžnou akci bez destruktivního významu; její dostupnost a výsledek zůstávají samostatné. |
| `tone=danger` | Pro skutečně závažnou akci, jejíž důsledek vysvětluje text; konkrétní tokeny určí úroveň 2. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=active` | Při probíhající aktivaci ovladače. Nezaměňovat tento interakční stav za trvalou vybranou hodnotu nebo active=true navigačního cíle. |
| `state=focus` | Při skutečném klávesnicovém fokusu. Poloha fokusu zůstává odlišitelná od vybrané hodnoty a aktivace. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít, zavřít nebo sbalit příslušný rám podle podporovaného režimu.

### Co vyvolávat nemá

- Neodhlásit uživatele, nezměnit agendu a neslibovat sbalení u režimu none.

### Přechody a odpovědnost

Obsah stránky zůstane zachovaný a název ovladače odpovídá dalšímu možnému kroku. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Ovládá právě příslušný rám.
- Název vyjádří otevření nebo sbalení podle skutečného stavu a dostupného režimu.
- Nabízejte jen změnu, kterou dovoluje zvolený režim Sidebar; v none se rám nesbaluje.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

### ERP — víceagendová aplikace

**Situace a cíl:** Pracovník prochází nákup, sklad a související přehledy.

**Volba a varianta:** Trigger mění otevření nebo sbalení rámu; NavigationItem přechází na stránku. V průchodu se uplatní `tone=neutral`, `state=default`.

**Průchod a výsledek:** V desktopové agendě Nákup zvolte u hostitele collapsible=icon. Ovladač Sbalit navigaci změní expanded=true na false, zachová aktuální Objednávky a zpřístupní jména ikon; pro opačný krok změní název na Rozbalit navigaci.

**Výjimka a návrat:** V režimu none se ovládání sbalení nenabízí. Režim rámu je vlastností hostitele, nikoli novou variantou tohoto triggeru.

**Nevhodně:** Neodhlásit uživatele, nezměnit agendu a neslibovat sbalení u režimu none.

### Web — zákaznický portál

**Situace a cíl:** Zákazník na telefonu otevírá přehled svého účtu.

**Volba a varianta:** Trigger mění otevření nebo sbalení rámu; NavigationItem přechází na stránku. V průchodu se uplatní `tone=neutral`, `state=default`.

**Průchod a výsledek:** Na úzké obrazovce zákaznického účtu ovladač Otevřít navigaci přepne hostitelský Sidebar.Mobile z open=false na true. Otevření samo nepřejde na jinou stránku; zavření vrátí kontext i logický fokus.

**Výjimka a návrat:** V režimu none se ovládání sbalení nenabízí. Režim rámu je vlastností hostitele, nikoli novou variantou tohoto triggeru.

**Nevhodně:** Neodhlásit uživatele, nezměnit agendu a neslibovat sbalení u režimu none.

### Interní systém — projektový nástroj

**Situace a cíl:** Člen týmu přechází mezi pracovním seznamem a detaily projektu.

**Volba a varianta:** Trigger mění otevření nebo sbalení rámu; NavigationItem přechází na stránku. V průchodu se uplatní `tone=neutral`, `state=default`.

**Průchod a výsledek:** V pracovním prostoru Orion může hostitel použít offcanvas. Skrytí rámu zachová aktuální pracovní obsah a ponechá dosažitelný spouštěč pro nové otevření mimo skrytou oblast.

**Výjimka a návrat:** V režimu none se ovládání sbalení nenabízí. Režim rámu je vlastností hostitele, nikoli novou variantou tohoto triggeru.

**Nevhodně:** Neodhlásit uživatele, nezměnit agendu a neslibovat sbalení u režimu none.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit šířkovou a vizuální hierarchii rámu, názvy cílů a pravidla zobrazení identity značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí nabídku agend, oprávnění, zvolený režim a zachování kontextu při změně zařízení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3058-74)
