---
title: "Fyrirtæki og stigveldi fyrirtækis (grundvallaratriði viðskipta)"
description: "Grundvallaratriði viðskipta hefur þrjár gerðir af samstæðufyrirtæki sem er hægt að skilgreina sem hjálpa fyrirtæki að framkvæma viðskiptaferli eða ná markmiði."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 93711977ad8d861ca75ba80ee542ee112c8ddd2f
ms.lasthandoff: 03/31/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Fyrirtæki og stigveldi fyrirtækis (grundvallaratriði viðskipta)

[!include[banner](includes/banner.md)]


Grundvallaratriði viðskipta hefur þrjár gerðir af samstæðufyrirtæki sem er hægt að skilgreina sem hjálpa fyrirtæki að framkvæma viðskiptaferli eða ná markmiði. 

Fyrirtæki er hópur af fólki sem vinna saman að því að framkvæma viðskiptaferli eða ná markmiði. Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækiseininga sem mynda fyrirtæki þitt.

## <a name="organizations"></a>Fyrirtæki
Í   Commerce essentials (grundvallaratriði viðskipta)  er hægt að skilgreina eftirfarandi þrjár gerðir samstæðufyrirtæki: lögaðila, rekstrareiningar, og hópa. Í Microsoft Dynamics AX eru öll innri fyrirtæki gerðir af einingunni Aðili. Notið þess vegna þessum fyrirtækjum í aðsetursbók til að geyma aðsetur og aðrar tengslaupplýsingar. Aðila getur verið annað hvort einstaklingur eða fyrirtæki, og geta tilheyrt einni eða fleiri aðsetursbækur.
### <a name="legal-entities"></a>Lögaðilar

Lögaðili er fyrirtæki sem hefur skráð ögfest lagalega uppbyggingu. Lögaðila er hægt að færa inn í samninga og eru þeir krafnir um að útbúa yfirlit sem segir til um frammistöðu þeirra. Fyrirtæki aðeins gerð af lögaðila Í Microsoft Dynamics AX, og sérhver lögaðili tengist auðkenni fyrirtækis. Þessi tenging til staðar þar sem Fyrirtækiskenni eða DataAreaId, er notaður í sumum gagnalíkön þar sem fyrirtækin eru notaðar sem jaðar fyrir gagnaöryggi. Notendur geta nálgast gögn aðeins fyrir fyrirtæki sem eru skráðir inn í.

### <a name="operating-units"></a>Rekstrareiningar

Rekstrareining er fyrirtæki sem er notað til að skipta stýringu verðmæta og rekstrarferlis í viðskiptum. Fólk í rekstrareiningu hefur skyldu til að hámarka notkun takmarkaðra auðlinda, bæta ferli og bera ábyrgð á afköstum sínum. Í Commerce essentials, innihalda tegundir rekstrareininga kostnaðarstaði, viðskiptaeiningar, deildir og virðisstraumar og smásölurásir. Eftirfarandi tafla veitir frekari upplýsingar um hverja tegund rekstrareiningar.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Gerð rekstrareiningar** | **Lýsing**                                                                         | **Tilgangur**                                                                                                                                 |
| Viðskiptaeining           | Er hálf-sjálfstæð rekstrareining sem er stofnuð til að uppfylla viðskiptamarkmið áætlunar. | Notaðu viðskiptaeiningar við fjárhagsskýrslugerð sem byggir á iðngeirum eða afurðalínum sem fyrirtækið þjónar á milli lögaðila. |
| Smásölurás          | Rekstrareiningu sem táknar verslunarhúsnæði.                             | Notið til að stjórna og stýra eina eða fleiri verslanir innan eða á milli lögaðila.                                                               |

## <a name="organizational-hierarchies"></a>Stigveldi fyrirtækja
Í Grunnþættir viðskipta (Commerce essentials), hefur hvert stigveldi úthluta málefni. Tilgangur stigveldis ákvarðar gerðir fyrirtæki sem má hafa með í stigveldi. Tilgangur skilgreinir einnig hvaða forrit aðstæður sem hægt er að nota í stigveldinu. Til dæmis er hægt að nota smásölustigveldi til að kaupa og selja afurðir í smásöluverslun. Fyrirtæki í stigveldi geta samnýtt færibreytur reglur og færslur. Fyrirtæki getur erft eða hunsað færibreytur móðurfélags þess. Hins vegar samnýtt aðalgögn, eins og afurðir og aðsetursbækur, gildir fyrir allt fyrirtækið og ekki er hægt að hnekkja verði fyrir einstök fyrirtæki.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Bestu framkvæmd við að setja upp fyrirtækis í stigveldi 

Íhugið eftirfarandi bestu venjur þegar komið stigveldi fyrirtækis:
-   Stofna deild til að tilgreina skurðpunkta á milli lögaðila og viðskiptaeiningar. Þú getur þá tekið saman gögn frá deild til lögaðila fyrir lögbundin skýrslugerð, og frá deild til viðskiptaeiningu fyrir innri skýrslugjöf.
-   Í einum lögaðila, ekki setja upp mörgum stigveldum fyrir sama málefni stigveldis.
-   Stofnaðu ekki stigveldi fyrir hvert málefni. Vanalega er aðeins hægt að nota eitt stigveldi fyrir margan tilgang. Til dæmis er hægt að úthluta einu stigveldi rekstrareiningar á allar reglur sem tengjast tilgangi.
-   Stofna samhæft stigveldi. Í stigveldi, öllum hnútum sem eru í sama fjarlægð úr rótarhnút eru skilgreindar sem stig. Í samhæfðu stigveldi, aðeins ein gerð rekstrareiningar getur átt sér stað á hverju stigi, og fjarlægð úr rótarhnút í hvert stig er samræmd. Ef undirskipuð stig er milli deild og lögaðila eða viðskiptaeiningar sem eru frátakara fyrirtæki getur verið nauðsynlegt til að stofna samhæft stigveldi.
-   Settu ekki upp líkan af sérstöku stigveldi rekstrareiningar ef skipulag lögaðila sem er einnig rekstrarskipulag þitt. Blandað stigveldi lögaðila og rekstrareiningar getur þjónað tilgangi beggja.
-   Áður en þú setur upp helstu atburðarásir endurskipulagningar þarf að nota öruggar gildisdagsetningar stigveldisins til að framkvæma áhrifagreiningu og staðfestingarpróf.
-   Vista stigveldi sem drög ef gæti þurft að breyta stigveldi áður en hægt að gefa hana út.
-   Takmarka fjölda fólks sem hefur leyfi til að bæta við eða fjarlægja stofnanir frá stigveldi í framleiðsluumhverfi. Lægri tala minnkar hættuna sem á dýrum mistökum og gera verður leiðréttingar.

## <a name="retail-store-management"></a>Stjórnun smásöluverslunar
Eftirfarandi tafla lýsir aðstæðum Commerce essentials þar sem hægt er að nota stigveldi fyrirtækis.
| Verkefni                                                                           | Lýsing                                                                                                                                                                                                                                                                                                | Tilgangur stigveldis    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Stjórna smásöluúrvali                                                      | Auðkennið vörurnar sem eru tiltækar í hverri smásöluverslun .                                                                                                                                                                                                                                             | Smásöluúrval    |
| Stjórna áfyllingu í smásölu                                                    | Flokkur geymir til að fylla á birgðum á grundvelli áfyllingarreglur.                                                                                                                                                                                                                                          | Áfylling í smásölu |
| Tilkynna gögn fyrir verslanir.                                                         | Verslunarflokkar fyrir skýrslugerð.                                                                                                                                                                                                                                                                                | Skýrslugerð smásölu     |
| Bóka birgðir, reikna uppgjör eða bóka uppgjör fyrir verslunarflokk | Stofna verslanir sem má tengja við runuvinnslu. Þegar runuvinnsla er skilgreind til að bóka í birgðir, reikna uppgjör eða bóka uppgjör, er hægt að tilgreina hvaða stigveldi vinnslan á við. Þegar verslunum er bætt við eða fjarlægt úr stigveldinu þarf ekki að breyta runuvinnslu. | Retail POS skráning   |






