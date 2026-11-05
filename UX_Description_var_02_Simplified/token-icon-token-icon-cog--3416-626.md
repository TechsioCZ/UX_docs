# Token Icon/token-icon-cog

Glyph `token-icon-cog` představuje nastavení v odpovídajícím slotu hostitele. Samotný symbol neprovádí akci.

**Vazba:** Table. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Glyph `token-icon-cog` představuje nastavení v odpovídajícím slotu hostitele. Samotný symbol neprovádí akci. Použijte ji pouze ve slotu se stejným významem; název ovladače nebo související text tento význam zpřístupní.

## Kdy zvolit alternativu

Když má funkce jiný význam než tato kresba, použijte odpovídající glyph. U neobvyklého nebo závažného příkazu zvolte textové Button či Link; samotný symbol nesmí nahrazovat jeho vysvětlení.

## Anatomie, stavy a varianty

Součást skladby **Table**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.
Samostatnou osu error/default tento glyph nemá. Výsledek operace i význam případné změny barvy řídí skutečný hostitel; nevytvářejte neexistující varianty samotné kresby.

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- V pojmenovaném hostiteli nabídnout: Otevřít pojmenované nastavení tabulky, například viditelnost sloupců.

### Co vyvolávat nemá

- Nespustit změnu nastavení bez konkrétní volby uživatele.

### Přechody a odpovědnost

Kresbu dosazuje skutečný hostitel podle podmínky popsané níže. Změna glyphu sama nepotvrzuje výběr ani výsledek požadavku. Je-li symbol v ovladači, aktivaci, případné čekání, odmítnutí a návrat řeší tento ovladač; glyph nevytváří další fokus ani vlastní uloženou hodnotu.

### Konkrétní pravidla použití

- Vkládejte do slotu, jehož význam odpovídá symbolu.
- Pokud symbol tvoří samostatný ovladač, název akce poskytuje tento ovladač; technický název tokenu není uživatelský popisek.
- V tabulce označuje nastavení viditelnosti sloupců. Ve zdroji je vedený jako návrhové doplnění knihovny.

## Obsah a pojmenování

Technický název tohoto glyphu není text pro uživatele. Pokud je použit v samostatném ovladači, jeho název pojmenuje konkrétní výsledek a případně objekt zásahu. Dekorativní kresba neopakuje zbytečně stejné sdělení vedle již pojmenovaného obsahu.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Symbol doplňuje uvedený význam; konkrétní operaci provádí pojmenovaný hostitel, nikoli kresba. Výsledek operace řídí hostitel; kresba nevytváří další vlastní validační cyklus.

- **Pravidlo použití:** Nespustit změnu nastavení bez konkrétní volby uživatele.

- **Společné výjimky a návrat:** Při odmítnutí nebo zrušení se nesmí zobrazit falešné potvrzení; výsledek i návrat řeší hostitel.

### ERP — seznam objednávek

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „tabulka objednávek“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Průchod a výsledek:** Do skutečného ovladače u „tabulka objednávek“ vložte glyph a název „Viditelnost sloupců objednávek“. Až aktivace hostitele vyvolá tuto akci; čtení symbolu ani hover ne. Otevře se volba viditelnosti sloupců; zavření bez změny ponechá předchozí skladbu.

### Web — zákaznické objednávky

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „tabulka mých objednávek“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Průchod a výsledek:** Do skutečného ovladače u „tabulka mých objednávek“ vložte glyph a název „Viditelnost sloupců mých objednávek“. Až aktivace hostitele vyvolá tuto akci; čtení symbolu ani hover ne. Otevře se volba viditelnosti sloupců; zavření bez změny ponechá předchozí skladbu.

### Interní systém — ITSM přehled

**Situace a cíl:** V tomto projektu se řeší význam nebo ovladač u „tabulka incidentů“; je nutné odlišit samotnou kresbu od účinku hostitele.

**Průchod a výsledek:** Do skutečného ovladače u „tabulka incidentů“ vložte glyph a název „Viditelnost sloupců incidentů“. Až aktivace hostitele vyvolá tuto akci; čtení symbolu ani hover ne. Otevře se volba viditelnosti sloupců; zavření bez změny ponechá předchozí skladbu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit schválenou ikonografii, optické velikosti a sémantické barvy symbolů, v návaznosti na názvy sloupců, hustotu tabulky a vizuální hierarchii výběru a chyb a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí zdroj záznamů, filtry, řazení, rozsah výběru, oprávnění a uložení buněk. Při doplnění pravidel značky zkontrolujte zejména vazbu symbolu na název hostitele a zachování jeho skutečného významu. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=3416-626)
