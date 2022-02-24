---
title: upplýsingar notaðar í uppskriftaútreikningum með staðalkostnaði
description: Uppskriftarútreikningar (BOM) nota gögn frá nokkrum upprunum til að reikna út staðalkostnað framleiddrar vöru. Uppruninn felur í sér upplýsingar um vörur, leiðir víxla, óbeinan kostnað útreikningsformúla og útgáfu kostnaðarútreiknings.
author: AndersGirke
manager: tfehr
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbc7e4105d085e2af0e8e6e574244f5083d08c15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430311"
---
# <a name="information-used-in-bom-calculations-with-standard-costs"></a>upplýsingar notaðar í uppskriftaútreikningum með staðalkostnaði

[!include [banner](../includes/banner.md)]

Uppskriftarútreikningar (BOM) nota gögn frá nokkrum upprunum til að reikna út staðalkostnað framleiddrar vöru. Uppruninn felur í sér upplýsingar um vörur, leiðir víxla, óbeinan kostnað útreikningsformúla og útgáfu kostnaðarútreiknings.

Upplýsingar keyptu vörunnar sem eru notaðar í uppskriftarútreikningi staðalkostnaðar felur í sér eftirfarandi:
-   Kostnað − Kostnaði keyptrar vöru er viðhaldið sem kostnaðarfærslum tengdar ákveðnum stað í kostnaðarútgáfa fyrir staðalkostnaður. Hver kostnaðarfærsla hefur gilda dagsetningu og dagsetning uppskriftarútreikningsins ákvarðar það hvaða kostnaðarfærslur eru notaðar. Til dæmis gæti uppskriftarútreikningur með útreikningsdagsetningu í framtíðinni notað kostnaðarfærslu í biðstöðu með gilda dagsetningu í framtíðinni.
-   Kostnaðarflokkur − Kostnaðarflokkurinn sem er úthlutaður keyptri vöru býður upp á grundvöllinn fyrir hlutun kostnaðar í útreiknuðum kostnaði framleiddrar vöru.
-   Viðvörunarskilyrði sem eru innfelld í uppskriftarútreikningsflokki vörunnar gera uppskriftarútreikningnum kleift að finna möguleg vandamál. Þetta getur verið þegar keypta varan hefur kostnaðinn núll, magnið núll í Uppskrift eða úrelta kostnaðarfærslu. Hægt er að hnekkja viðvörunarskilyrðum þegar verið er að hefja uppskriftarútreikning.

Upplýsingar framleiddu vörunnar sem eru notaðar í uppskriftarútreikningi staðalkostnaðar felur í sér eftirfarandi:
-   Staðlað pöntunarmagn fyrir birgðir − Staðlað pöntunarmagn vöru (fyrir birgðir) virkar sem sjálfgefna lotustærð bókhalds fyrir afborganir fasts kostnaðar í uppskriftarútreikningi. Lotustærð bókhaldsins mun einnig endurspegla margfeldi pöntunarmagns ef það er tilgreint.
-   Viðvörunarskilyrði sem eru innfelld í uppskriftarútreikningsflokki vörunnar gera uppskriftarútreikningnum kleift að finna möguleg vandamál. Einn dæmi gæti verið að framleidd vara hefur ekki Uppskrift eða leið. Hægt er að hnekkja viðvörunarskilyrðum þegar verið er að hefja uppskriftarútreikning.

Uppskriftarupplýsingarnar sem eru notaðar í uppskriftarútreikningi staðalkostnaðar eru eftirfarandi:
-   Uppskriftarútgáfa − Uppskriftarútgáfan sem er úthlutuð framleiddu vörunni hefur gildar dagsetningar frá og til og stöðu fyrir samþykkt og virkt. Uppskriftarútgáfan getur átt við um allt fyrirtækið eða eitt setur og getur líka endurspeglað magnrofsstaði.
-   Vörumagn uppskriftarlínu − Íhlutur hefur yfirleitt breytilegar magnkröfur en þær geta verið fastar. Íhlutamagnið er yfirleitt tilgreint fyrir framleiðslu einnar yfirvöru en það getur verið tilgreint fyrir hvert 100 eða hvert 1000 til að aðstoða við nákvæmni tugabrota. Íhlutamagnið er líka hægt að reikna út á grundvelli mælinga.
-   Rýrnun uppskriftarlínuvöru − Íhlutur getur haft breytilegt eða fast magn fyrir áætlaða rýrnum.
-   Gildar dagsetningar uppskriftarlínuvöru − Íhlutur getur haft gildar dagsetningar frá og til.
-   Framleiðslugerð uppskriftarlínuvöru − Lotustærð kostnaðarútreiknings fyrir afborganir af föstum kostnaði mun endurspegla magn uppskriftarútreikningsins og niðurbrotsham eftir pöntun af því að uppskriftarútreikningurinn gerir ráð fyrir því að framleiddi íhluturinn verði framleiddur í nákvæma magninu frekar en stöðluðu pöntunarmagni sínu.
-   Undiruppskrift framleidds íhlutar − Framleiddur íhlutur getur haft tiltekna uppskriftarútgáfu sem væri notuð í staðinn fyrir núverandi virka uppskriftarútgáfu vörunnar í uppskriftarútreikningi.
-   Undirleið framleidds íhlutar - Framleiddur íhlutur getur haft tiltekna uppskriftarútgáfu sem væri notuð í staðinn fyrir núverandi virka leiðarútgáfu vörunnar í uppskriftarútreikningi.
-   Aðgerðarnúmer og áhrif prósenta aðgerðarrýrnunar − Aðgerðarnúmerið tengir íhlut við tiltekna aðgerð og aðgerðir geta haft rýrnunarprósentu. Tengingin gerir uppskriftarútreikningum kleift að gera grein fyrir rýrnunarprósentum og heildarrýrnunarprósentum yfir margar aðgerðir af nauðsynlegu magni íhlutarins.
-   Hundsa uppskriftarlínuvöru í kostnaðarútreikningum − Hægt er að hundsa íhlut fyrir uppskriftarútreikning.

Upplýsingar rekstrartilfanga sem eru notaðar í uppskriftarútreikningi staðalkostnaðar fela í sér:
-   Tímakostnaður − Tímakostnaðurinn sem eru tengdar við rekstrartilföng er tilgreindur sem kostnaðartegundum sem eru úthlutaðar á uppsetningartíma og keyrslutíma. Þessar kostnaðartegundir ættu vera auðkenndar fyrir tilfangaflokka og rekstrartilföng. Tímakostnaðurinn sem er tengdur við kostnaðartegund getur átt við um eitt setur eða allt fyrirtækið.
-   Kostnaður á einingu − Sum framleiðsluumhverfi úthluta kostnaði rekstrartilfanga á úttakseiningu, sem myndi vera tilgreint sem mismunandi kostnaðartegund fyrir magn. Til dæmis getur magntengdur kostnaður endurspeglað stykkjataxta fyrir vinnu eða þá að málningarframleiðandi gæti úthlutað kostnaði rekstrartilfanga fyrir hvert úttaks-gallon.
-   Hnekking upplýsinga rekstrartilfanga á leiðaraðgerðum − upplýsingar rekstrartilfanga um kostnaðartegundir erfast frá aðgerðum þar sem hægt er að hnekkja þeim. Uppskriftarútreikningar nota kostnaðartegundarupplýsingar sem er tilgreint í leiðaraðgerðunum.
-   Kostnaðarflokkur fyrir kostnaðartegund − Kostnaðarflokkur sem er úthlutað kostnaðartegund býður upp á hlutun kostnaðar í útreiknuðum kostnaði framleiddrar vöru. Til dæmis gætu mismunandi kostnaðarflokkar verið notaðir til að hluta útreiknaða kostnaðinn sem er tengdur við vélar og vinnu eða við uppsetningar- og keyrslutíma.

Leiðarupplýsingarnar sem eru notaðar í uppskriftarútreikningi staðalkostnaðar fela í sér:
-   Leiðarútgáfa - Leiðarútgáfan sem er úthlutuð framleiddu vörunni hefur gildar dagsetningar frá og til og stöðu fyrir samþykkt og virkt. Leiðarútgáfan verður að eiga við um eitt setur og getur líka endurspeglað magnrofsstaði.
-   Leiðaraðgerðartími − Hægt er að tilgreina tímann fyrir keyrslutíma og uppsetningartíma. Tíminn á klukkustund er yfirleitt tilgreindur fyrir framleiðslu einnar yfirvöru en hann getur verið tilgreindur fyrir hvert 100 eða hvert 1000 til að aðstoða við nákvæmni tugabrota.
-   Leiðaraðgerðatími fyrir aukatilföng − Aukatilföng hafa sama aðgerðarnúmer og aðaltilföngin og þau hafa sama leiðaraðgerðatíma. Til dæmis gæti aðgerð útheimt vél sem aðaltilföngin og vinnu og verkfæri sem aukatilföng.
-   Rýrnunarprósenta leiðaraðgerðar - uppskriftarútreikningar gera grein fyrir rýrnunarprósentum og heildarrýrnunarprósentum yfir margar aðgerðir. Þetta á við nauðsynlegum tíma fyrir leiðaraðgerðir og nauðsynlegu magni fyrir íhluti sem eru tengdar við aðgerðarnúmer.
-   Kostnaðartegundir fyrir leiðaraðgerð − Upplýsingar rekstrartilfanga um kostnaðartegundir erfast til aðgerða þar sem hægt verður að hnekkja þeim. Uppskriftarútreikningar nota kostnaðartegundarupplýsingar sem er tilgreint í leiðaraðgerðinni.

Upplýsingarnar um framleiðslurekstrarkostnað sem eru notaðar í uppskriftarútreikningi staðalkostnaðar fela í sér:
-   Álag − Útreikningsformúla álags endurspeglar prósentu virðis eins og 100 % sem er bundin við tiltekinn kostnaðarflokk eins og vinnu.
-   Taxti − Útreikningsformúla taxta endurspeglar upphæð á einingu eins og 10,00 USD á klukkustund sem er bundið við tiltekinn kostnaðarflokk eins og vinnu.
-   Tímagrundvallaður á móti efnisgrundvölluðum rekstrarkostnaði − Framleiðslurekstrarkostnaðinn er hægt að binda við leiðaraðgerðirnar eða efnisíhlutina.

Upplýsingarnar um útgáfu kostnaðarútreiknings sem eru notaðar í uppskriftarútreikningi staðalkostnaðar fela í sér:
-   Gerð kostnaðarútreiknings − Útgáfa kostnaðarútreikningsins þarf að innihalda staðalkostnað. Nokkrar takmarkanir eiga við um uppskriftarútreikninga sem nota staðalkostnað. Til dæmis tilgreina þessar takmarkanir að hafa þurfi gjöld með í einingarkostnaði og að niðurbrotshamur uppskriftarútreikningsins þurfi að vera einstiga.
-   Skylduvararegla − Útgáfa kostnaðarútreiknings getur gefið fyrirmæli um notkun varareglu eins og að nota tiltekna útgáfu kostnaðarútreiknings eða virku kostnaðarfærslnanna. Skylduvarareglan á yfirleitt við um útgáfu kostnaðarútreiknings sem stendur fyrir stigvaxandi uppfærslurnar í tveggja-útgáfu nálgun fyrir kostnaðaruppfærslur.
-   Lokunarmerking fyrir kostnað í bið − Lokunarmerking getur komið í veg fyrir uppskriftarútreikninga á kostnaðinum í bið fyrir framleiddar vörur.
-   Tiltekin dagsetning frá − Tiltekna dagsetningin frá mun virka sem sjálfgefna útreikningsdagsetningin fyrir alla uppskriftarútreikninga sem fela í sér útgáfu kostnaðarútreikningsins.
-   Tiltekið setur − Tiltekið setur mun takmarka uppskriftarútreikninga við eitt setur.
-   Innihald kostnaðarútgáfunnar verður að fela í sér kostnað − Innihaldið verður að fela í sér kostnað. Það má fela í sér söluverð til að reikna út söluverð sem lagt er til fyrir framleiddar vörur.

Hægt er að tilgreina nokkra uppruna upplýsinga þegar verið er að hefja uppskriftarútreikning. Þetta felur í sér setrið, útreikningsdagsetninguna og útgáfu kostnaðarútreikningsins.





