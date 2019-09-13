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
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887412"
---
# <a name="preferred-maintenance-workers"></a>Æskilegir viðhaldsstarfskraftar

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þú getur stofnað forgang varðandi hvaða viðhaldsstarfsmönnum er úthlutað til að ljúka verkbeiðnum við tímasetningu verkbeiðni. Notkun þessarar virkni er valkvæð, en hún getur hjálpað þér að velja fyrir hæfasta viðhaldsstarfsmanninn til að ljúka verki, byggt á færni og hæfni starfsmanna. Þess vegna er uppsetningin í **Forgangsstarfsmenn viðhalds** í verkbeiðniáætlun notuð til að ákvarða hvort tiltekinn viðhaldsstarfsmaður eða starfsmannahópur skuli áætlaðir fyrir verkbeiðni. Aðeins viðhaldsstarfsmenn sem eru tiltækir, þegar áætlun er gerð, verða áætlaðir. Ef valin uppsetning viðhaldsstarfsmanna passar við verkbeiðni við tímasetningu, en viðhaldsstarfsmanni er úthlutað til annarra starfa, verður verkbeiðnin áætluð fyrir annan tiltækan viðhaldsstarfsmann.

Áður en þú getur sett upp forgangsstarfsmenn viðhalds verður þú fyrst að setja upp viðhaldsstarfsmenn og hópa starfsmanna viðhalds sem ættu að vera tiltækir fyrir val. Sjá [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) fyrir lýsingu á hvernig setja skuli upp viðhaldsstarfsmenn og starfsmannahópa.

## <a name="set-up-preferred-workers"></a>Setja upp forgangsstarfskrafta

Forgangsviðhaldsstarfsmaður eða starfsmannahópur getur verið skyldur tilteknum

- Viðskipti  
- afbrigði viðhaldsverkgerðar  
- gerð viðhaldsverks  
- tegund viðhaldsverkgerðar  
- fastafjármunur  
- gerð eignar  

eða sambland af þessum valkostum. Því meira val sem þú gerir fyrir sömu skrá, því nákvæmari verður uppsetningin.

1. Smelltu á **Eignastjórnun** > **Uppsetning** > **Starfskraftar** > **Forgangstarfsmenn viðhalds**.

2. Smelltu á **Nýtt** til að stofna nýja færslu.

3. Byrjaðu á því að búa til „sjálfgefinn“ viðhaldsmann eða starfsmannahópsuppsetningu sem hefur engin val í reitunum sem sýndir eru í áherslulistanum hér að ofan. Þetta þýðir að þú gerir aðeins val í reitnum **Forgangshópur starfsmanna viðhalds** eða reitnum **Forgangsstarfsmaður viðhalds**. Á myndinni hér að neðan sérðu dæmi í fyrstu skránni þar sem „Beiðnir“ eru valdar sem valinn hópur starfsmanna viðhalds.

>[!NOTE]
>Þessi sjálfgefna uppsetning verður notuð við tímasetningu verkbeiðni ef engin önnur, sértækari samsetning passar við innihald verkbeiðninnar við tímasetningu verkbeiðna.

4. Endurtaktu skref 2 til að stofna nýja færslu. Taktu nauðsynlegar ákvarðanir, eftir því smáatriðastigi fyrir valinn starfsmann eða starfsmannahóp. *Dæmi:* Á myndinni hér að neðan, í sjöttu skránni, er viðhaldsstarfsmaðurinn Shawn Richardson valinn valinn starfsmaður. Hann verður sjálfkrafa valinn við tímasetningu verkbeiðni sem felur í sér eignina „CH-BP1-03-02 og viðhaldsvinnutegundin„ Aðstöðumat “, ef hann er tiltækur á tilsettum tíma.

>[!NOTE]
>Almennt þegar valinn viðhaldsstarfsmaður er valinn meðan á tímasetningu vinnu stendur fer eignastýring í gegnum allar **Forgangsstarfsmenn viðhalds** skrár til að leita að mögulegri samsvörun, athugaðu alltaf sérstaka samsetningu fyrst. Ef engin samsvörun er að finna, er „sjálfgefna“ skráin með valinu í annaðhvort reitnum **Forgangshópur starfsmanna viðhalds** eða reitnum **Forgangsstarfsmaður viðhalds** notuð.


![Mynd 1](media/02-work-order-scheduling.png)

Þú getur líka sett upp ábyrga viðhaldsstarfsmenn sem hægt er að velja þegar viðhaldsbeiðni eða verkbeiðni er búin til. Í **Öllum verkbeiðnum** og **Öllum viðhaldsbeiðnum** er hægt að breyta valinu, ef þess þarf. Sjá [Ábyrgir viðhaldsstarfsmenn](../setup-for-maintenance-requests/responsible-workers.md) fyrir meiri upplýsingar.

Við tímatökuáætlun verkbeiðni eru mismunandi stig reiknuð út til að ákvarða hvaða starfsmenn ættu að ljúka störfum sem tengjast verkbeiðni (þessi stig eru sett upp í tenglinum **Færibreytur eignastýringar** > **Tímasetningar verkbeiðni**). Ef tveir eða fleiri forgangsviðhaldsstarfsmenn eða ábyrgir starfsmenn við viðhald fá sömu einkunn við tímasetningu verkbeiðni er einn starfsmaður valinn af handahófi. Annars er það alltaf starfsmaðurinn með hæstu einkunn sem er úthlutað til að ljúka verkbeiðni.

