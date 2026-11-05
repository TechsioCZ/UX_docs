# Skeleton / Rectangle

Obdélníkový Skeleton rezervuje plochu dosud načítaného obsahového bloku.

**Vazba:** Skeleton. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Pouze po dobu, kdy aplikace skutečně získává příslušný obsah a ještě nezná jeho konečný výsledek. Tvar přibližte budoucímu bloku, například obrázku nebo kartě. Tvar přibližte budoucímu bloku, například obrázku nebo kartě.

## Kdy zvolit alternativu

Jakmile je výsledek známý, použijte skutečný obsah nebo vysvětlení prázdného či chybového výsledku. Placeholder není náhradou hlášení o trvalé nedostupnosti.

## Anatomie, stavy a varianty

Součást skladby **Skeleton**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `variant=primary` | Vizuální provedení primary podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `variant=secondary` | Vizuální provedení secondary podle pravidel značky a stejné role ve skladbě. Samotný styl nemění stav dat, počet voleb ani oprávnění. |
| `speed=slow` | Vizuální tempo pulzování slow; není odhadem doby načtení. Respektovat omezený pohyb. |
| `speed=normal` | Vizuální tempo pulzování normal; není odhadem doby načtení. Respektovat omezený pohyb. |
| `speed=fast` | Vizuální tempo pulzování fast; není odhadem doby načtení. Respektovat omezený pohyb. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zastoupit příslušný dosud nedostupný obsah po skutečnou dobu čekání.

### Co vyvolávat nemá

- Nespouštět vlastní akci ani nevydávat zástupnou plochu za známou hodnotu.

### Přechody a odpovědnost

Vstupem je skutečné čekání na tento obsah. Po odpovědi aplikace placeholder odstraní a ukáže data, vysvětlené prázdno nebo chybu s dostupnou nápravou. Při opakování se znovu čeká jen na chybějící oblast; již potvrzené okolní údaje se nevynulují.

### Konkrétní pravidla použití

- Tvar přibližte budoucímu bloku, například obrázku nebo kartě.
- Po dokončení načítání jej nahraďte skutečným obsahem nebo odpovídajícím prázdným či chybovým stavem.
- Pokud se používá pulzování, respektujte nastavení omezeného pohybu; animace nemá být jediným signálem čekání.

## Obsah a pojmenování

Tato vizuální část nepřidává vlastní produktový údaj. Případný popis stavu poskytuje příslušný hostitel; symbol, počet značek nebo zástupná délka se nevydávají za dosud neznámá data.

## Přístupnost a prostředí

Vizuální část sama nevyžaduje další zastávku fokusu. Název a případnou aktivaci poskytuje její skutečný hostitel. Význam zůstává dostupný také textově nebo strukturou; samotná barva či poloha značky jej nenahrazuje.

## Omezení a příklady podle typu projektu

**Společné pro všechny tři následující příklady:**

- **Společná volba a varianta:** Známá je struktura budoucího obsahu, jeho výsledek ještě ne; falešná hodnota ani nekonečný spinner by jej nevysvětlily. V průchodu se uplatní `variant=primary`, `speed=slow`.

- **Společné výjimky a návrat:** Prázdný či chybný výsledek ukončí čekání vysvětlením a případnou akcí opakování; placeholder nesmí běžet trvale. Případnou pulzaci potlačte podle nastavení omezeného pohybu.

- **Nevhodné použití:** Ukázat zástupný tvar jako skutečnou cenu, dostupnost nebo text záznamu.

### ERP — profil dodavatele

**Situace a cíl:** Aplikace načítá základní profil vybrané firmy.

**Průchod a výsledek:** Během skutečného získávání dat rezervujte místo pro fotografii zařízení. Po odpovědi nahraďte placeholder právě tímto obsahem, nikoli dříve přijatou hodnotou jiného objektu.

### Web — zákaznický účet

**Situace a cíl:** Po otevření účtu se načítá jeho obsahová karta.

**Průchod a výsledek:** Během skutečného získávání dat rezervujte místo pro produktový obraz. Po odpovědi nahraďte placeholder právě tímto obsahem, nikoli dříve přijatou hodnotou jiného objektu.

### Interní systém — týmový adresář

**Situace a cíl:** Pracovník otevírá kartu kolegy.

**Průchod a výsledek:** Během skutečného získávání dat rezervujte místo pro náhled výukového obsahu. Po odpovědi nahraďte placeholder právě tímto obsahem, nikoli dříve přijatou hodnotou jiného objektu.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit vizuální intenzitu placeholderů a pravidla omezeného pohybu a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí začátek a konec načítání i následný stav obsahu. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2774-16670)
