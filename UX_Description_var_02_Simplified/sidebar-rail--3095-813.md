# Sidebar.Rail

Okrajový ovládací pás Sidebar poskytuje prostor pro změnu stavu bočního rámu.

**Vazba:** Sidebar. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Pás zůstává součástí ovládání příslušného rámu. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě Sidebar. Pás zůstává součástí ovládání příslušného rámu.

## Kdy zvolit alternativu

Pro samotné přechody mezi stránkami postačí VerticalNavigation. Pro dočasný kontextový úkol použijte Drawer; tato část zůstává součástí navigačního rámu.

## Anatomie, stavy a varianty

Součást skladby **Sidebar**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `side=start` | Polohu start volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `side=end` | Polohu end volte vůči skutečnému spouštěči či okraji. Start/end jsou logické směry podle jazyka; samotná varianta nedokládá automatické řešení kolizí. |
| `dir=ltr` | Pro levopravý jazyk a odpovídající logické směry. |
| `dir=rtl` | Pro pravolevý jazyk; obrátit logické uspořádání a odpovídající směrové značky, ne význam akcí. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=focus` | Při skutečném klávesnicovém fokusu. Poloha fokusu zůstává odlišitelná od vybrané hodnoty a aktivace. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Nabídnout ovládání povoleného režimu rámu klávesnicí i ukazatelem.

### Co vyvolávat nemá

- Nevynucovat přesné tažení a nevytvářet rail v režimu none.

### Přechody a odpovědnost

Změna rámu zachová dosažitelnost cílů i hlavního obsahu. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Pás zůstává součástí ovládání příslušného rámu.
- Změna stavu nesmí vyžadovat pouze přesný zásah myší nebo tažení.
- Režim none rail nevykresluje; jeho ovládání není samostatnou funkcí mimo podporovaný rám.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Rail je doplňkové ovládání desktopového rámu; mobilní panel má vlastní spouštěč a zavření. V průchodu se uplatní `side=start`, `state=default`.

- **Společné výjimky a návrat:** Stejný výsledek musí být dosažitelný klávesnicí a bez přesného gesta. Režim none rail nemá; mobilní otevření řeší Sidebar.Trigger, nikoli předstíraný desktopový rail.

- **Pravidlo použití:** Nevynucovat přesné tažení a nevytvářet rail v režimu none.

### ERP — víceagendová aplikace

**Situace a cíl:** Pracovník prochází nákup, sklad a související přehledy.

**Průchod a výsledek:** V oblasti „Objednávky“ použijte rail jen u podporovaného desktopového režimu. Aktivace dostupným ovladačem změní sbalení rámu a zachová aktuální stránku i její data.

### Web — zákaznický účet na desktopu

**Situace a cíl:** Zákazník na větší obrazovce potřebuje dosáhnout navigace svého účtu i při sbaleném bočním rámci.

**Průchod a výsledek:** V oblasti „Moje objednávky“ použijte rail jen u podporovaného desktopového režimu. Aktivace dostupným ovladačem změní sbalení rámu a zachová aktuální stránku i její data.

### Interní systém — projektový nástroj

**Situace a cíl:** Člen týmu přechází mezi pracovním seznamem a detaily projektu.

**Průchod a výsledek:** V oblasti „Projekt Orion“ použijte rail jen u podporovaného desktopového režimu. Aktivace dostupným ovladačem změní sbalení rámu a zachová aktuální stránku i její data.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit šířkovou a vizuální hierarchii rámu, názvy cílů a pravidla zobrazení identity značky a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí nabídku agend, oprávnění, zvolený režim a zachování kontextu při změně zařízení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3095-813)
