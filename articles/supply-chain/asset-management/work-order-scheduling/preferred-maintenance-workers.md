---
title: Setja upp æskilega viðhaldsstarfskrafta
description: Þetta efni útskýrir hvernig á að setja upp forgangsviðhaldsstarfskrafta í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3501cb49cbc8b3060da03b3d2e9badc949910a48
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652196"
---
# <a name="set-up-preferred-maintenance-workers"></a>Setja upp æskilega viðhaldsstarfskrafta

[!include [banner](../../includes/banner.md)]

 

Við tímasetningu verkbeiðni er hægt að stofna forgang varðandi hvaða viðhaldsstarfsmanni eða starfsmannahóp er úthlutað til að ljúka verkbeiðninni. Notkun þessarar virkni er valkvæð, en hún getur hjálpað þér að velja fyrir hæfasta viðhaldsstarfsmanninn til að ljúka verki, byggt á færni og hæfni starfsmanna. Aðeins viðhaldsstarfsmenn sem eru tiltækir, þegar áætlun er gerð, verða áætlaðir. Ef valin uppsetning viðhaldsstarfsmanna passar við verkbeiðni við tímasetningu, en viðhaldsstarfsmanni er úthlutað til annarra starfa, verður verkbeiðnin áætluð fyrir annan tiltækan viðhaldsstarfsmann.

Áður en þú getur sett upp valda viðhaldsstarfsmenn verður þú fyrst að setja upp viðhaldsstarfsmenn og starfsmannahópa. Fyrir lýsingu á hvernig setja skuli upp viðhaldsstarfsmenn og starfsmannahópa skals sjá [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Setja upp forgangsstarfskrafta

Forgangsviðhaldsstarfsmaður eða starfsmannahópur getur verið skyldur einum eða fleiri af eftirfarandi:

- Viðskipti  
- afbrigði viðhaldsverkgerðar  
- gerð viðhaldsverks  
- tegund viðhaldsverkgerðar  
- fastafjármunur  
- gerð eignar  

Því meira val sem þú gerir fyrir sömu skrá, því nákvæmari verður uppsetningin.

1. Smelltu á **Eignastjórnun** > **Uppsetning** > **Starfskraftar** > **Forgangstarfsmenn viðhalds**.

2. Smelltu á **Nýtt** til að stofna nýja færslu.

3. Byrjaðu á því að búa til „sjálfgefinn“ viðhaldsstarfsmann eða starfsmannahóp. Þetta þýðir að þú gerir aðeins val í reitnum **Forgangshópur starfsmanna viðhalds** eða reitnum **Forgangsstarfsmaður viðhalds**. Á skjámyndinni hér að neðan sérðu dæmi í fyrstu skránni þar sem „Beiðnir“ eru valdar sem **Valinn hópur starfsmanna viðhalds**.

    [!NOTE] Þessi sjálfgefna uppsetning verður notuð við tímasetningu verkbeiðni ef engin önnur, sértækari samsetning passar við innihald verkbeiðninnar.

4. Endurtaktu skref 2 til að stofna nýja færslu. Taktu nauðsynlegar ákvarðanir, eftir því smáatriðastigi fyrir valinn starfsmann eða starfsmannahóp. 

    *Dæmi:* Á skjámyndinni hér að neðan, í sjöttu skránni, er viðhaldsstarfsmaðurinn Shawn Richardson valinn valinn starfsmaður. Hann verður sjálfkrafa valinn við tímasetningu verkbeiðni sem felur í sér eignina „CH-BP1-03-02 og gerð viðhaldsverks „Aðstöðumat“, ef hann er tiltækur á tilsettum tíma.

    [!NOTE] Almennt þegar valinn viðhaldsstarfsmaður er valinn meðan á tímasetningu vinnu stendur fer eignastýring í gegnum allar **Forgangsstarfsmenn viðhalds** skrár til að leita að mögulegri samsvörun, athugaðu alltaf sérstaka samsetningu fyrst. Ef engin samsvörun er að finna, er „sjálfgefna“ skráin með valinu í annaðhvort reitnum **Forgangshópur starfsmanna viðhalds** eða reitnum **Forgangsstarfsmaður viðhalds** notuð.

![Mynd 1](media/02-work-order-scheduling.png)

Þú getur líka sett upp *ábyrga* viðhaldsstarfsmenn sem hægt er að velja þegar viðhaldsbeiðni eða verkbeiðni er búin til. Hægt er að breyta valinu í **Öllum verkbeiðnum** og **Öllum viðhaldsbeiðnum**, ef þess þarf. Nánari upplýsingar er að finna í [Ábyrgir viðhaldsstarfsmenn](../setup-for-maintenance-requests/responsible-workers.md).

Við tímatökuáætlun verkbeiðni eru mismunandi stig reiknuð út til að ákvarða hvaða starfsmenn ættu að ljúka störfum sem tengjast verkbeiðni (þessi stig eru sett upp í tenglinum **Færibreytur eignastýringar** > **Tímasetningar verkbeiðni**). Ef tveir eða fleiri forgangsviðhaldsstarfsmenn eða ábyrgir starfsmenn við viðhald fá sömu einkunn við tímasetningu verkbeiðni er einn starfsmaður valinn af handahófi. Annars er það alltaf starfsmaðurinn með hæstu einkunn sem er úthlutað til að ljúka verkbeiðni.

