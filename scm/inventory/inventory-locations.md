---
title: "Birgðastaðsetningar"
description: "Birgðastaðsetningar eru notaðar með grunnvöruhúsi (WMS I) til að ákveða hvar geyma skuli vörur og hvar vörur eru teknar til í WMS I vöruhúsi."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 6acdcfc8bbd412eaab7ac458a023b4a7f1cab445
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-locations"></a>Birgðastaðsetningar

[!include[banner](../includes/banner.md)]


Birgðastaðsetningar eru notaðar með grunnvöruhúsi (WMS I) til að ákveða hvar geyma skuli vörur og hvar vörur eru teknar til í WMS I vöruhúsi.

Athugasemd: Þetta efni á við aðgerðir í kerfiseiningu vöruhúsastjórnunar. Það á ekki við um aðgerðir í kerfiseiningu vöruhúsastjórnunar.

Hugtakið staðsetning vísar til staðurinn sem vörur eru geymdar og gefnar út úr.

Fyrir hverja staðsetningu, staðurinn þar sem varan er sett inn einnig er hægt að tilgreina. Að sjálfgefnu þær eru þær sömu. Vörur eru yfirleitt settar í og dregnar úr sömu hlið í staðsetningu, en ekki alltaf. Til dæmis vörur sem eru vistaðar í virku geymslu rekka eru sett inn úr einum gangi og gefnir út frá öðru. Aðalinntakið er frá heiti staðsetningar sem er yfirleitt ákveðin af hnitum hennar: vöruhús, gangur, rekki, hillu og körfu. Þetta heiti eða kenni er fært inn handvirkt eða myndar úr stasetningarhnitum - til dæmis 01-02-03-4 fyrir gang 1, rekki 2, hilla 3, karfa 4 í  síðunni birgðastaðsetningar.
Eiginleikar staðsetningar
-------------------

Staðsetning hefur eftirfarandi eiginleika:
-   Stærð (hæð, breidd, dýpt, og þar með rúmmál)
-   Vöruhús, rekka, hillu og körfustöðu.
-   Gerð staðsetningar (biðstaðsetningu, tiltektarstaðsetning, inn-hlið, út-hlið, staðsetning framleiðsluinntaks, eftirlitsstaðsetning eða kanban-geymslusvæði)

Ekki er hægt að notag ávísunartexta í netkerfum til að staðfesta að virknitáknið hafi valið rétta staðsetningu fyrir tilgreint vara. Þennan stýritexta er hægt að stofna handvirkt eða sjálfkrafa.

## <a name="sort-codes"></a>Raðkóðar
Notaðu röðunarkóða til að hámarka meðferð tiltektarlína, sem lýsa upplýsingunum sem er krafist fyrir tiltektarvörur úr birgðum, þar með talið tiltektarröðun. Það er hægt að tilgreina raðkóða eftir ganginum og öðrum hnitum eða með því að úthluta þeim handvirkt fyrir staðsetninguna.

## <a name="blocked-locations"></a>Lokaðar staðsetningar
Stundum gæti þurft að gefa til kynna að staðsetning verði læst um ákveðinn tíma, til dæmis til að framkvæma viðgerðir. Á öðrum tímum er hugsanlegt að læsa aðeins ílag eða aðeins frálag.
Trjáskipulag
--------------

Í síðu birgðastaðsetning er hægt að skoða útlit vöruhúss í tréskipulagi eftir hnitum birgðastaðsetninga í skilgreindu skjásniði.
Viðhalda birgðastaðsetning í skjámyndinni vöruhús
---------------------------------------------------

Mögulegt er að afrita staðsetningar úr einu vöruhúsi í annað og til að stofna staðsetningar með leiðsagnarforriti. Áður en leiðsagnarforritið keyrt skal ganga úr skugga sem um að þú hefur skilgreint heiti fyrir sjálfgefin staðsetning síðu Vöruhúss.



<a name="see-also"></a>Sjá einnig
--------

[Búa til nýtt útlit vöruhús (verkefnaleiðbeiningar](https://ax.help.dynamics.com/en/wiki/create-a-new-warehouse-layout/)




