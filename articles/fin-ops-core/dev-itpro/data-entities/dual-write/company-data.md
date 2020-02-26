---
title: Fyrirtækishugtak í Common Data Service
description: Þetta efni lýsir samþættingu fyrirtækjaupplýsinga milli Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 20a3f89821af56cb4c3969c89301d4a8a32ab848
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019845"
---
# <a name="company-concept-in-common-data-service"></a>Fyrirtækishugtak í Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Í Finance and Operations er hugtakið a *fyrirtæki* bæði lögleg smíð og viðskiptasmíð. Það er einnig öryggis- og sýnileikamörk fyrir gögn. Notendur vinna alltaf í samhengi við eitt fyrirtæki og flest gögnin eru röndótt af fyrirtækinu.

Common Data Service er ekki með sambærilegt hugtak. Næsta hugtakið er *rekstrareining*, sem er fyrst og fremst öryggis- og sýnileikamörk fyrir notendagögn. Þetta hugtak hefur ekki sömu lagalegu eða viðskiptalegu afleiðingar og hugtakið fyrirtæki.

Vegna þess að rekstrareining og fyrirtæki eru ekki sambærileg hugtök er ekki mögulegt að þvinga kortlagningu á milli þeirra (1: 1) í þeim tilgangi að samþætta Common Data Service. Hins vegar vegna þess að notendur verða sjálfgefið að geta séð sömu skrár í forritinu og Common Data Service, hefur Microsoft kynnt nýja einingu í Common Data Service sem heitir cdm\_Fyrirtæki. Þessi eining jafngildir fyrirtækinu í forritinu. Til að hjálpa til við að tryggja að sýnileiki gagna sé jafnstór milli forritsins og Common Data Service úr kassanum, mælum við með eftirfarandi uppsetningu fyrir gögn í Common Data Service:

+ Fyrir hverja færslu fyrirtækis Finance and Operations sem er virk fyrir tvískiptingu, er tilheyrandi cdm\_Fyrirtækjaskrá búin til.
+ Þegar cdm\_Fyrirtækjaskrá er búin til og virkjuð fyrir tvískipt skrif, er sjálfgefin rekstrareining búin til með sama nafn. Þó að sjálfgefið teymi sé sjálfkrafa búið til fyrir þá rekstrareiningu er rekstrareiningin ekki notuð.
+ Sérstakt eigendateymi er búið til sem hefur sama nafn. Það er líka tengt rekstrareiningunni.
+ Sjálfgefið að eigandi skrár sem er búinn til og tvískrifaður til Common Data Service er stillt á „DW Owner“ teymið sem er tengt tilheyrandi rekstrareiningum.

Eftirfarandi skýringarmynd sýnir dæmi um þessa gagnauppsetningu í Common Data Service.

![Uppsetning gagna í Common Data Service](media/dual-write-company-1.png)

Vegna þessarar stillingar verða allar skrár sem tengjast USMF fyrirtækinu í eigu teymis sem er tengt USMF viðskiptareiningunni í Common Data Service. Þess vegna getur hver notandi sem hefur aðgang að þeirri rekstrareiningu með öryggishlutverki sem er stillt á sýnileika rekstrareininga, nú séð þessar skrár. Eftirfarandi dæmi sýnir hvernig hægt er að nota teymi til að veita réttan aðgang að þeim skrám.

+ Hlutverkinu „Sölustjóri“ er úthlutað til meðlima „USMF sölu“ teymisins.
+ Notendur sem hafa hlutverk „sölustjóra“ geta fengið aðgang að öllum reikningsgögnum sem eru aðilar að sömu viðskiptareiningunni og þeir eru aðilar að.
+ "USMF Sales" teymið er tengt við USMF viðskiptadeildina sem áður var nefnd.
+ Þess vegna geta meðlimir í "USMF sölu" teyminu séð hvaða reikning sem er í eigu "USMF DW" notandans, sem hefði komið frá USMF fyrirtækinu í Finance and Operations.

![Hvernig hægt er að nota teymi](media/dual-write-company-2.png)

Eins og myndin hér að ofan sýnir er þessi 1:1 kortlagning milli rekstrareiningar, fyrirtækis og teymis aðeins upphafspunktur. Í þessu dæmi er ný „eining“ í Evrópu búin til handvirkt í Common Data Service sem yfireining bæði fyrir DEMF og ESMF. Þessi nýja rótarviðskiptaeining er ekki skyld tvöföldum skrifum. Hins vegar er hægt að nota hana til að veita meðlimum „EUR Sales“ teymisins aðgang að reikningsgögnum bæði í DEMF og ESMF með því að stilla sýnileika gagna á **Yfir-/undir-BU** í tilheyrandi öryggishlutverki.

Lokaumræðan sem þarf að ræða er hvernig tvískipt skrifa ákvarðar hvaða eigendateymi það ætti að úthluta skrám til. Þessari hegðun er stjórnað af reitnum **Sjálfgefið eigendateymi** á cdm\_Fyrirtækjaskrá. Þegar cdm\_Fyrirtækjaskrá er virk fyrir tvískipta skrifun, stofna viðbætur sjálfkrafa tilheyrandi viðskiptaeiningu og eigendateymi (ef það er ekki þegar til) og stillir reitinn **Sjálfgefið eigendateymi**. Stjórnandi getur breytt þessum reit í annað gildi. Stjórnandi getur þó ekki hreinsað reitinn svo framarlega sem einingin er virk fyrir tvískipta skrifun.

> [!div class="mx-imgBorder"]
![Reiturinn Sjálfgefið eigendateymi](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Fyrirtækjaskrár og ræsibönd

Common Data Service-samþætting færir fyrirtækjajöfnun með því að nota auðkenni fyrirtækisins til að randa gögn. Eins og eftirfarandi mynd sýnir, eru allar fyrirtækjasértækar einingar útvíkkaðar þannig að þær hafa mörg-til-einn (N: 1) vensl við cdm\_Fyrirtækjaeining.

> [!div class="mx-imgBorder"]
![N:1 vensl milli fyrirtækjasértakrar einingar og einingarinnar cdm_Company](media/dual-write-bootstrapping.png)

+ Fyrir skrár, eftir að fyrirtæki er bætt við og vistað, verður gildið aðeins lesanlegt. Þess vegna ættu notendur að gæta þess að þeir velja rétt fyrirtæki.
+ Aðeins skrár sem hafa fyrirtækjagögn eru gjaldgengar fyrir tvískiptingu milli forritsins og Common Data Service.
+ Fyrir núverandi gögn Common Data Service mun stjórnandaleidd ræsibandareynsla brátt verða tiltæk.
