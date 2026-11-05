# TreeView/BranchTrigger

Spouštěč větve TreeView mění rozbalení jejích potomků; výběr uzlu je odlišná operace.

**Vazba:** TreeView. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Ovladač mění otevření právě své větve. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě TreeView. Ovladač mění otevření právě své větve.

## Kdy zvolit alternativu

Pro datovou hodnotu vyberte Select, Combobox či CascadeSelect podle rozsahu a hierarchie. Pro příkaz použijte Menu; vizuálně podobný obal nesmí měnit tento význam.

## Anatomie, stavy a varianty

Součást skladby **TreeView**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Zdroj této části neuvádí samostatnou variantní osu. Použijte ji ve správném kontextu hostitele; nepřidávejte odhadem vlastní error, success nebo loading.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Rozbalit a sbalit potomky právě této větve.

### Co vyvolávat nemá

- Nezměnit automaticky vybraný uzel ani neprovést navigaci.

### Přechody a odpovědnost

Vztah rodiče a potomků zůstává čitelný a indikátor odpovídá otevření. Neúspěšná nebo zrušená aktivace nesmí předstírat potvrzený výsledek; způsob návratu řídí příslušný hostitel.

### Konkrétní pravidla použití

- Ovladač mění otevření právě své větve.
- Odlište jeho aktivaci od výběru uzlu nebo navigace.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Odlište fokus, otevření, výběr a aktuální cíl podle role tohoto prvku. Ovládání funguje klávesnicí a zachovává pojmenování i při sbalení. Při zúžení, delším jménu a jiném směru jazyka zůstávají obsah i ovladače dostupné.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Trigger pouze otevírá potomky, datový výběr nebo navigace jsou jiné operace. Tato část nemá vlastní variantní osu; uvedená situace je stavem dat nebo hostitele.

- **Společné výjimky a návrat:** Při sbalení s fokusem uvnitř potomků přesuňte fokus na dosažitelnou větev. Prázdný list nevydávejte za další rozbalitelnou větev.

- **Pravidlo použití:** Nezměnit automaticky vybraný uzel ani neprovést navigaci.

### ERP — struktura organizace

**Situace a cíl:** Pracovník prochází organizační členění před přiřazením zakázky.

**Průchod a výsledek:** U větve v oblasti „Organizační struktura“ aktivujte otevření potomků. BranchContent i indikátor se sjednotí s expanded; potvrzený datový výběr zůstane beze změny.

### Web — správa dokumentů

**Situace a cíl:** Přihlášený uživatel prochází své složky a vybírá související dokument.

**Průchod a výsledek:** U větve v oblasti „Vaše dokumenty“ aktivujte otevření potomků. BranchContent i indikátor se sjednotí s expanded; potvrzený datový výběr zůstane beze změny.

### Interní systém — DMS archiv

**Situace a cíl:** Správce prochází projektové složky.

**Průchod a výsledek:** U větve v oblasti „Archiv projektů“ aktivujte otevření potomků. BranchContent i indikátor se sjednotí s expanded; potvrzený datový výběr zůstane beze změny.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit názvy uzlů, ikonografii druhů položek a čitelnost hierarchie a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí datové vztahy, pravidla výběru a případné načítání potomků. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3963-27022)
