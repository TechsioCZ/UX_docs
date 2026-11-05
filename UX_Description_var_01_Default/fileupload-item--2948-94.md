# FileUpload/Item

Položka FileUpload ukazuje přijatý nebo odmítnutý místní soubor a jeho dostupné akce.

**Vazba:** FileUpload. Rozsah použití se týká tohoto dílu; úplný pracovní průchod řídí jeho hostitel.

## Kdy použít

Zobrazujte název a lokální přijetí nebo odmítnutí konkrétního souboru. Výsledek se vztahuje jen ke správnému obsahu či objektu této části ve skladbě FileUpload. Zobrazujte název a lokální přijetí nebo odmítnutí konkrétního souboru.

## Kdy zvolit alternativu

Pro prostý navigační přechod použijte Link, pro operaci Button. Tuto obsahovou část ponechte její vymezené roli v FileUpload a neslučujte ji s nepojmenovanou akcí celého obalu.

## Anatomie, stavy a varianty

Součást skladby **FileUpload**. Varianty níže popisují tento konkrétní díl; ostatní části mohou mít vlastní odlišné osy a odpovědnosti.

| Volba ve zdroji | Kdy ji použít a co znamená |
|---|---|
| `type=accepted` | Soubor prošel místními podmínkami přijetí; neznamená automaticky dokončený serverový přenos. |
| `type=rejected` | Soubor nebyl přijat podle určených pravidel; uvést konkrétní důvod a možnost nápravy. |
| `state=default` | Běžný stav bez právě indikované interakce nebo známého problému. Není důkazem, že již proběhla validace či uložení. |
| `state=disabled` | Když uživatel nyní nemůže prvek použít z určeného důvodu. Aktivace se neprovede; podmínka dostupnosti má být zjistitelná. |
| `preview=document` | Zobrazit document jen ve shodě se skutečným typem nebo účelem přílohy; ikona není potvrzením úspěšného přenosu. |
| `preview=image` | Zobrazit image jen ve shodě se skutečným typem nebo účelem přílohy; ikona není potvrzením úspěšného přenosu. |

## Chování a akce

### Co může vyvolat nebo zprostředkovat

- Zobrazit jeden přijatý nebo odmítnutý soubor a nabídnout jen určené řádkové operace.

### Co vyvolávat nemá

- Nesmazat uložený dokument místo odebrání nové lokální přílohy.

### Přechody a odpovědnost

Výběr nejprve vytvoří lokální sadu. Kontrola podmínek rozliší accepted a rejected s konkrétním důvodem; accepted ještě neznamená upload. Pokud projekt přenáší soubory, musí aplikace oddělit průběh, úspěch a opakování po chybě. Zrušení výběru nepřidá nový soubor; odebrání lokální přílohy nesmaže již uložený dokument.

### Konkrétní pravidla použití

- Zobrazujte název a lokální přijetí nebo odmítnutí konkrétního souboru.
- Odmítnutí vysvětlete u této přílohy.
- Accepted není potvrzení úspěšného nahrání na server.

## Obsah a pojmenování

Použijte konkrétní názvy odpovídající skutečným objektům projektu. Popisek, hodnota, nápověda a chyba mají různé účely; placeholder nenahrazuje trvalý název. Dlouhý obsah ani lokalizace nesmějí změnit nebo skrýt rozhodující význam této části.

## Přístupnost a prostředí

Dostupné akce lze provést klávesnicí a jejich názvy popisují výsledek. Fokus se neplete s potvrzenou hodnotou. Význam i dostupnost zůstávají rozpoznatelné bez samotné barvy; menší plocha neodstraní jedinou cestu k dokončení úkolu.

## Omezení a příklady podle typu projektu

### ERP — příloha dodavatelského dokladu

**Situace a cíl:** Pracovník přidává podklad k právě upravované faktuře.

**Volba a varianta:** Item drží stav jednoho souboru; Dropzone zpřístupňuje přidání dalších. V průchodu se uplatní `type=accepted`, `state=default`, `preview=document`.

**Průchod a výsledek:** Řádek „dodaci-list-1048.pdf“ ukáže název, stav místního přijetí a případný důvod odmítnutí. Pojmenované Odebrat odstraní právě tuto novou lokální přílohu ze sady.

**Výjimka a návrat:** Neúspěšný přenos není úspěšně uložený dokument. Opakování či zrušení přenosu nabídněte pouze se skutečnou podporou aplikace; lokální odebrání nesmí smazat uložený originál.

**Nevhodně:** Nesmazat uložený dokument místo odebrání nové lokální přílohy.

### Web — zákaznický požadavek

**Situace a cíl:** Návštěvník přikládá fotografii k dotazu na produkt.

**Volba a varianta:** Item drží stav jednoho souboru; Dropzone zpřístupňuje přidání dalších. V průchodu se uplatní `type=accepted`, `state=default`, `preview=document`.

**Průchod a výsledek:** Řádek „detail-vady.jpg“ ukáže název, stav místního přijetí a případný důvod odmítnutí. Pojmenované Odebrat odstraní právě tuto novou lokální přílohu ze sady.

**Výjimka a návrat:** Neúspěšný přenos není úspěšně uložený dokument. Opakování či zrušení přenosu nabídněte pouze se skutečnou podporou aplikace; lokální odebrání nesmí smazat uložený originál.

**Nevhodně:** Nesmazat uložený dokument místo odebrání nové lokální přílohy.

### Interní systém — dokumentový portál

**Situace a cíl:** Zaměstnanec připravuje více souborů k pracovnímu úkolu.

**Volba a varianta:** Item drží stav jednoho souboru; Dropzone zpřístupňuje přidání dalších. V průchodu se uplatní `type=accepted`, `state=default`, `preview=document`.

**Průchod a výsledek:** Řádek „zadani-orion.pdf“ ukáže název, stav místního přijetí a případný důvod odmítnutí. Pojmenované Odebrat odstraní právě tuto novou lokální přílohu ze sady.

**Výjimka a návrat:** Neúspěšný přenos není úspěšně uložený dokument. Opakování či zrušení přenosu nabídněte pouze se skutečnou podporou aplikace; lokální odebrání nesmí smazat uložený originál.

**Nevhodně:** Nesmazat uložený dokument místo odebrání nové lokální přílohy.

## Související pravidla a vazba na úroveň 2

Tato dokumentace patří do **úrovně 3 — komponenty**. Nadřazená **úroveň 2 — pravidla značky** má určit slovník příloh, prezentaci omezení a tón chybových zpráv a respektuje korporátní úroveň 1. Konkrétní pravidla úrovně 2 zatím nejsou dodaná; ukázková barva, téma nebo text je nenahrazují.

Produkt dále určí povolené typy, velikosti, počty, způsob přenosu a skutečný stav serverového uložení. Při doplnění pravidel značky zkontrolujte zejména pojmenování a varianty této konkrétní komponenty proti jejímu úkolu a povoleným akcím. Konflikt se neřeší tichým přejmenováním stavu nebo přidáním nedoložené funkce.

[Komponenta ve Figmě](https://www.figma.com/design/gi5GUSWwAeXknaKEeLqK5w/New-Design-System?node-id=2948-94)
