# FileUpload/Dropzone

Přijímací plocha FileUpload nabízí přetažení místního souboru i systémový výběr přílohy.

**Vazba:** FileUpload. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Přetažení doplňte systémovým výběrem souboru. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě FileUpload. Přetažení doplňte systémovým výběrem souboru.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v FileUpload a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **FileUpload**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=hover` | Při najetí ukazatelem na dostupný prvek. Zvýraznění nepotvrzuje hodnotu ani nespouští operaci. |
| `state=focus` | Při skutečném klávesnicovém fokusu. Poloha fokusu zůstává odlišitelná od vybrané hodnoty a aktivace. |
| `state=dragging` | Když uživatel skutečně přetahuje soubory nad příslušnou plochou. Neznamená přijetí ani úspěšný upload. |
| `state=invalid` | Když kontrola odhalí neplatný údaj nebo výběr. Vysvětlení určí opravu; samotná barva nestačí. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Otevřít výběr souborů a doplňkově přijmout přetažené soubory.

### Co vyvolávat nemá

- Nevydávat přijetí do lokální sady za dokončený přenos na server.

### Přechody a odpovědnost

Výběr nejprve vytvoří lokální sadu. Kontrola podmínek rozliší accepted a rejected s konkrétním důvodem; accepted ještě neznamená upload. Pokud projekt přenáší soubory, musí aplikace oddělit průběh, úspěch a opakování po chybě. Zrušení výběru nepřidá nový soubor; odebrání lokální přílohy nesmaže již uložený dokument.

### Konkrétní pravidla použití

- Přetažení doplňte systémovým výběrem souboru.
- Uveďte skutečné podmínky přijetí; aktivní plocha neslibuje dokončený serverový upload.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — příloha dodavatelského dokladu

**Situace a cíl:** Pracovník přidává podklad k právě upravované faktuře.

**Volba a varianta:** Dropzone nabízí výběr a doplňkové tažení; Image pouze zobrazuje obsah. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** U přílohy „Příloha faktury“ otevřete pojmenovaný výběr a zvolte „dodaci-list-1048.pdf“. Stejný výsledek může nabídnout tažení; kontrola vytvoří accepted nebo rejected s důvodem.

**Výjimka a návrat:** Zrušení systémového výběru nic nepřidá. Přijatý soubor je zatím v lokální sadě; přenos a jeho chybu musí aplikace oddělit.

**Nevhodně:** Nevydávat přijetí do lokální sady za dokončený přenos na server.

### Web — zákaznický požadavek

**Situace a cíl:** Návštěvník přikládá fotografii k dotazu na produkt.

**Volba a varianta:** Dropzone nabízí výběr a doplňkové tažení; Image pouze zobrazuje obsah. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** U přílohy „Fotografie k požadavku“ otevřete pojmenovaný výběr a zvolte „detail-vady.jpg“. Stejný výsledek může nabídnout tažení; kontrola vytvoří accepted nebo rejected s důvodem.

**Výjimka a návrat:** Zrušení systémového výběru nic nepřidá. Přijatý soubor je zatím v lokální sadě; přenos a jeho chybu musí aplikace oddělit.

**Nevhodně:** Nevydávat přijetí do lokální sady za dokončený přenos na server.

### Interní systém — dokumentový portál

**Situace a cíl:** Zaměstnanec připravuje více souborů k pracovnímu úkolu.

**Volba a varianta:** Dropzone nabízí výběr a doplňkové tažení; Image pouze zobrazuje obsah. V průchodu se uplatní `state=default`.

**Průchod a výsledek:** U přílohy „Podklady k úkolu“ otevřete pojmenovaný výběr a zvolte „zadani-orion.pdf“. Stejný výsledek může nabídnout tažení; kontrola vytvoří accepted nebo rejected s důvodem.

**Výjimka a návrat:** Zrušení systémového výběru nic nepřidá. Přijatý soubor je zatím v lokální sadě; přenos a jeho chybu musí aplikace oddělit.

**Nevhodně:** Nevydávat přijetí do lokální sady za dokončený přenos na server.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník příloh, prezentaci omezení a tón chybových zpráv a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené typy, velikosti, počty, způsob přenosu a skutečný stav serverového uložení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2938-32)
