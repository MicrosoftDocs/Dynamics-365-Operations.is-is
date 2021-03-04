---
title: Sýna afslátt í POS
description: Þetta efni útskýrir hvernig Microsoft Dynamics 365 Commerce hjálpar söluaðilum að fræðast um kynningar og hvernig hægt er að nota þær til að selja og viðbótarselja áætlanir.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 7531e250580019a1e9892d22fc7761770227c61f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413163"
---
# <a name="show-discounts-in-pos"></a>Sýna afslátt í POS

[!include [banner](includes/banner.md)]

Kynningar gegna mikilvægu hlutverki við að hvetja viðskiptavini sem taka ákvarðanir um kaup. Sem dæmi má nefna að frí geta framleitt mesta sölu fyrir smásala, vegna þess að allur smásölumarkaðurinn fyllist af lokkandi kynningum og afslætti. Ef verslunaraðilar vita um og skilja kynningarnar sem eru í boði geta þeir auðveldlega nýtt sér þessar kynningar til að krossselja og viðbótarselja vörur. Þetta efni útskýrir hvernig Microsoft Dynamics 365 Commerce hjálpar söluaðilum að fræðast um kynningar og hvernig hægt er að nota þær til að selja og viðbótarselja áætlanir.

## <a name="learn-about-store-discounts"></a>Lærðu um afslátt í verslun

Commerce felur í sér aðgerð sem ber nafnið „Skoða alla afslætti.“ Þessi aðgerð sýnir alla afslættina sem eru í gangi í verslun. Aðgerðina „Skoða alla afslætti“ er hægt að kortleggja á hnapp í sölustað (POS) og hægt er að bæta þeim hnapp við síðuna **Velkomin** eða síðuna **Færsla**. Eftirfarandi mynd sýnir dæmi um síðuna **Allir afslættir** sem opnast.

![Síðan Allir afslættir](./media/View_all_discounts.png "Síðan Allir afslættir")

Til að sýna afslætti leitar kerfið eftir öllum afsláttum sem passa við eitt eða fleiri af eftirfarandi skilyrðum:

- Verðflokkur afsláttarins samsvarar verðflokki verslunarinnar.
- Verðlagshóp afsláttarins er varpað í hlutdeildar- eða vildarkerfi.
- Verðflokki afsláttarins er varpað í vörulista sem er tengd versluninni.

Síðan **Allir afslættir** sýnir aðeins nokkra afsláttarmiða sem byggir á afsláttarmiða, vegna þess að smásalar búa venjulega til þúsund afsláttarmiða og samsvarandi afslætti fyrir einstaka viðskiptavini og þessari síðu er ekki ætlað að sýna sérstökum afslætti viðskiptavina. Afsláttarmiðatengdur afsláttur er aðeins sýndur ef kveikt er á valkostinum **Sækja um án afsláttarmiðakóða** í hverjum afsláttarmiðahaus. Í því tilfelli geta gjaldkerar beitt afsláttarmiða án þess að þurfa að slá inn eða skanna afsláttarmiða eða strikamerki.

Þegar kveikt er á valkostinum **Sækja um án afsláttarmiðakóða** verða ýmsar sviðsmyndir tiltækar. Til dæmis geta gjaldkerar veitt viðskiptavinum viðbótarafslátt vegna viðskiptavinarins eða vegna vörugalla. Prentuðum afsláttarmiða eða strikamerkjum þarf ekki að dreifa til gjaldkera. Í staðinn geta gjaldkerar valið hnappinn **Nota afsláttarmiða**. Afsláttarmiða er síðan sjálfkrafa beitt á færsluna. Ef margar afsláttarmiðar eru til fyrir afsláttarmiðahaus velur kerfið sjálfkrafa fyrsta virka afsláttarmiðann í færslunni.

Á síðunni **Allir afslættir** geta söluaðilar einnig leitað að afslætti eftir lykilorðum. Leitarorðaleitin er í reitunum sem innihalda afsláttarheitið og afsláttarlýsinguna. Söluaðilar geta einnig síað afslátt út frá því hvort afsláttur krefst afsláttarmiðakóða.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Krossselja og selja upp með því að nota afslátt

Fjölskiptur afsláttur, svo sem magnafsláttur, blanda-og-passa afsláttur og þröskuldafsláttur, er frábær leið til að hvetja viðskiptavini til að kaupa fleiri vörur til að fá stærri afslátt. Þess vegna hjálpa þeir einnig við að auka stærð körfu viðskiptavina og tekjur smásala. Hægt er að birta þessa afslætti á vefsíðum í netverslun, á samfélagsmiðlum og á borðum í versluninni.

En jafnvel þegar allar þessar kynningaraðferðir eru notaðar gætu viðskiptavinir misst af tækifærinu til að nýta sér kynningar. Til að auðvelda söluaðilum að fá upplýsingar um það hvaða tilboð hægt er að nota fyrir valda línu, eða jafnvel alla körfuna, geta smásalar bætt við hnappnum fyrir aðgerðina **„Skoða afslætti sem eru í boði“** á hnappahnitinu á síðunni **Færsla**. Þar af leiðandi getur sölutengiliður valið færslulínu og síðan valið hnappinn til að sýna alla afslætti sem eru í boði fyrir völdu línuna. Sölumaðurinn getur einnig valið annan flipa til að sýna afslætti sem eiga við um alla færsluna. Mikilvægt er að hafa í huga að **Skoða afslætti sem eru í boði** sýnir ekki afslættina sem þegar eru notaðir í sölulínunni vegna þess að afsláttarupplýsingarnar eru þegar sýndar í sölulínunni. Tilgangurinn með þessari atburðarás er aðeins sá að sýna afslættina sem hafa ekki enn verið notaðir. Undantekningin á þessu eru afslættirnir sem eru notaðir út frá afsláttarmiða sem merktur er sem „Nota án kóða afsláttarmiða“. Þetta auðveldar söluaðila að fjarlægja á einfaldan hátt afsláttarmiðann sem hann hefur notað.

Síðan **Allir afslættir** sýna aðeins afslætti sem ekki keppa við þá afslætti sem eru notaðir. Þessi hegðun hjálpar til við að tryggja að ef söluaðili upplýsir viðskiptavin um afslátt og viðskiptavinurinn grípur til nauðsynlegra aðgerða (til dæmis kaupir viðskiptavinurinn einn hlut til viðbótar til að fá 10 prósent afslátt), þá er afslátturinn notaður á færsluna. Afslættir sem byggjast á afsláttarmiðum eru aðeins birtir þegar kveikt er á valkostinum **Nota án kóða afsláttarmiða**.

Í einföldri atburðarás þar sem allir afslættir hafa sama forgang er afsláttur með samhæði **Samsett**, og er jafnvægisstýring á afslætti stillt á **Besta verð og blanda innan forgangs, aldrei blandað yfir forgangsröðun**, síðan **Allir afslættir** sýnir alla tiltæka afslætti fyrir vöru, vegna þess að allir afslættir eru samsettir og keppa ekki hver við annan.

Eftirfarandi myndir sýna rökfræði sem ákvarðar hvaða afsláttur er sýndur í háþróaðri atburðarás, svo sem atburðarás þar sem afsláttur samhliða háttur er **Besta verðið** eða **Sértilboð**, og tvö eða fleiri forgangsröð eru notuð. Í þessum tilfellum hefur frekari áhrif á afsláttina sem eru sýndir byggð á því hvort eftirlit með samhliða afslætti er stillt á **Besta verð og blanda innan forgangs, aldrei blandað yfir forgangsröðun** eða **Besta verðið aðeins innan forgangs, alltaf samsett yfir forgang**.

Eftirfarandi mynd sýnir rökfræði sem er notuð þegar stýringu á samhliða afslætti er stillt á **Besta verð og blanda innan forgangs, aldrei blandað yfir forgangsröðun**.

![Rökfræði fyrir besta verðið og efnasamband í forgangi, aldrei blandað yfir forgangsröðun](./media/Model_1.png "Rökfræði fyrir besta verðið og efnasamband í forgangi, aldrei blandað yfir forgangsröðun").

Eftirfarandi mynd sýnir rökfræði sem er notuð þegar stýringu á samhliða afslætti er stillt á **Besta verð aðeins innan forgangs, alltaf blandað yfir forgangsröðun**.

![Rökfræði fyrir besta verðið aðeins í forgangi, alltaf blandað yfir forgangsröðun](./media/Model_2.png "Rökfræði fyrir besta verðið aðeins í forgangi, alltaf blandað yfir forgangsröðun").


[!INCLUDE[footer-include](../includes/footer-banner.md)]