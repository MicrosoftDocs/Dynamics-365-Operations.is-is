---
title: Ábyrgir viðhaldsstarfskraftar
description: Þetta efni útskýrir hvernig á að setja upp gerðir ábyrgðaraðila viðhaldsstarfskrafta í eignastjórnun.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d68c9e6de6e9d62d1dea95c747b17900d343e7324857dcfc083d48e5c1006b0e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731296"
---
# <a name="responsible-maintenance-workers"></a>Ábyrgir viðhaldsstarfskraftar

[!include [banner](../../includes/banner.md)]

 

Ábyrgir starfsmenn viðhalds geta tengst eignategundum, eignum, starfrænum stöðum, tegundum viðhaldsstétta, viðhaldsstörfum, afbrigði af viðhaldsstörfum og viðskiptum. Hægt er að nota þær í vinnupöntunum og viðhaldsbeiðnum til að gefa til kynna val á viðhaldsstarfsmönnunum sem ættu að vera ábyrgir fyrir verkbeiðninni. (Samt sem áður eru þessir viðhaldsstarfsmenn ekki endilega sömu starfsmenn og áætlað er að framkvæma verkbeiðnina.) Notkun þessarar aðgerðar er valkvæð. Til dæmis er hægt að nota það til að velja ábyrga starfsmenn eða starfsmannahópa fyrir ákveðnar vinnutegundir eða vinnusvæði.

Meðan á líftíma verkbeiðni stendur eða líftíma viðhaldsbeiðni er hægt að breyta eða uppfæra ábyrga starfsmenn viðhalds. Þessi breyting eða uppfærsla gæti tengst til dæmis breytingu á líftíma viðhaldsbeiðni eða líftíma verkbeiðni.

Uppsetningin á **Ábyrgir starfsmenn viðhalds** síðu er *ekki* notuð við tímasetningar verkbeiðni.

> [!NOTE]
> Í eignastjórnun geturðu einnig sett upp *valinn* viðhaldsstarfsmenn sem gætu verið úthlutaðir til vinnupantana við tímasetningar verkbeiðni.

Áður en þú getur sett upp ábyrga starfsmenn viðhalds verður þú að setja upp starfsmenn og hópa starfsmanna viðhalds sem ættu að vera tiltækir fyrir val. (Sjá upplýsingar um hvernig á að setja upp starfskrafta og viðhaldsstarfsmannahóps [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) .)

## <a name="set-up-responsible-maintenance-workers"></a>Setja upp ábyrga viðhaldsstarfskrafta

1. Veldu **Eignastýring** \> **Uppsetning** \> **Starfskraftar** \> **Ábyrgir starfsmenn viðhalds**.
2. Veljið **Ný** til að stofna nýja skrá.
3. Búðu fyrst til sjálfgefinn viðhaldsstarfsmann eða skipulag ábyrgan viðhaldsstarfsmannahóp þar sem þú stillir aðeins **Ábyrgur hópur viðhaldsstarfsmanna** reit og/eða retiinn **Ábyrgðarmaður**. Skildu reitina sem eftir eru auðir. Þessi sjálfgefna uppsetning verður notuð við tímasetningu verkbeiðni ef engin önnur, sértækari samsetning passar við innihald verkbeiðninnar.

    > [!NOTE]
    > Þegar stofnað er til viðhaldsbeiðni, þegar ábyrgur viðhaldsstarfsmaður eða ábyrgur viðhaldsstarfsmannahópur er gerður tiltækur fyrir val á **Allar viðhaldsbeiðnir** síðu, Eignastjórn fer í gegnum allar ábyrgar skrár starfsmanna viðhalds til að athuga hvort mögulegt sé samsvörun. Það athugar alltaf sértækustu samsetninguna fyrst. Með öðrum orðum, Eignastjórnun kannar fyrst hvort samsvörun finnist fyrir reitinn **Viðskipti**. Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Afbrigði af viðhaldsstörfum**. Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Afbrigði af viðhaldsstörfum** og svo framvegis. Eins og þú sérð á skipulagi síðunnar þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá hefur Eignastýring athugað hverja skrá frá hægri til vinstri fyrir leik (fyrst **Viðskipti**, síðan **Afbrigði af viðhaldsstörfum**, síðan **Tegund viðhalds**, síðan **Flokkur um viðhaldsstörf**, síðan **Virk staðsetning**, síðan **Eignir**, og að lokum **Tegund eigna**). Ef engin samsvörun er notuð er sjálfgefna skráin sem hefur ekkert val í þeim sjö reitum notuð.

Eftirfarandi mynd sýnir dæmi um listasíðuna **Ábyrgir viðhaldsstarfsmenn**.

![Síðan fyrir ábyrga viðhaldsstarfsmenn.](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]