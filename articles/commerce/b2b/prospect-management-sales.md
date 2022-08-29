---
title: Stjórna notendum viðskiptafélaga á B2B rafrænum viðskiptavefsíðum með Dynamics 365 Sales
description: Þessi grein lýsir því hvernig á að nota Microsoft Dynamics 365 Sala til að stjórna samþykki viðskiptafélaga fyrir Dynamics 365 Commerce vefsíður fyrirtækja til fyrirtækja (B2B).
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: d178e619fca7915286181aa803376cd564f60a26
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278652"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Stjórna notendum viðskiptafélaga á B2B rafrænum viðskiptavefsíðum með Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að nota Microsoft Dynamics 365 Sala til að stjórna samþykki viðskiptafélaga fyrir Dynamics 365 Commerce vefsíður fyrirtækja til fyrirtækja (B2B). Stofnanir sem hafa þegar fjárfest í Dynamics 365 Sales lausninni geta notað leiðar- og tækifærishugtök hennar fyrir samþykkisferli viðskiptafélaga í B2B rafrænum viðskiptum.

Fyrir bakgrunnsupplýsingar um samþykkisferlið B2B viðskiptafélaga, sjá [Stjórna notendum viðskiptafélaga á B2B rafrænum viðskiptavefsíðum](manage-b2b-users.md).

Hugsanlegir viðskiptafélagar geta hafið inngönguferlið á B2B rafræn viðskipti vefsíðu með því að senda inn beiðni um inngöngu í gegnum hlekk á B2B vefsíðunni. Eftir að beiðnin hefur verið lögð fram og viðkomandi störf (ss **P-0001** og **Samstilltu pantanir og rásbeiðnir**) eru keyrð í höfuðstöðvum Commerce, er inngöngubeiðnin vistuð á **Allar horfur** síðu í höfuðstöðvum Commerce. Síðan er hægt að ljúka við samþykkisferli viðskiptafélaga í sölu.

Eftir að samþætting milli sölu og viðskipta hefur verið virkjað veldur stofnun viðskiptavins í viðskiptalífinu stofnun *leiða* í sölu.

Eftirfarandi mynd sýnir dæmi um síðu til að búa til viðskiptavin fyrir tilvonandi viðskiptafélaga í sölu.

![Síða um að búa til kynningar í Dynamics 365 Sales.](../media/LeadInSales.png)

Í myndinni er **Hafðu samband** kafla sýnir manneskjuna sem sendi inn beiðni um borð og **Fyrirtæki** kafla sýnir skipulagið. Athugasemd í **Tímalína** kafla gefur til kynna að leiðin hafi verið mynduð af tvískrifa innviði. Vegna þess að það var búið til af tvískrifa innviði, mun þetta leiða ekki birtast í **Opnu leiðirnar mínar** fellilistanum. Í staðinn mun það birtast undir nýju útsýni sem er nefnt **Öll viðskipti B2B leiða**.

Samkvæmt stöðluðu ferli hæfishæfisaðila í sölu, þegar notandi "hæfir" forystunni, er an *tækifæri* skrá, a *samband* met, og an *reikning* skrá eru búin til. Tvískrifa innviðin er notuð til að skrifa tengiliðinn og reikningsskrárnar til Commerce. Tengiliðurinn er stofnaður sem viðskiptavinur *manneskju* gerð, og fyrirtækið er stofnað sem viðskiptavinur *skipulag* tegund. Ef notandi velur **Loka sem vann** fyrir tækifærið er tilboðið samþykkt í Commerce. Samþykki viðskiptavinar veldur því að stigveldi viðskiptavina er búið til.

Öll viðskiptaferli sem eftir eru eiga sér stað í Commerce. Þessi ferli fela í sér að senda tölvupóst til viðskiptafélaga, skilgreina stjórnun lánamarka fyrir notendur og bæta við fleiri notendum á B2B síðuna. Hins vegar, ef notandi hafnar forystunni eða merkir tækifærið sem glatað í stað þess að vera hæft til forystunnar, er tilvonandi í Commerce merktur sem hafnað og tölvupóstur um höfnun um borð er sendur til umsækjanda.

## <a name="enable-integration-between-sales-and-commerce"></a>Virkjaðu samþættingu milli sölu og viðskipta

Samþætting milli sölu og viðskipta byggir á tvískrifa innviði. Þess vegna ætti tvískrifað að vera virkt og virka þannig að viðskiptavinir sem eru búnir til í einu kerfinu séu skrifaðir í hitt kerfið. Fyrir frekari upplýsingar um tvískrifa innviði, sjá [Yfirlit yfir tvískrift](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Eftir að uppsetningu tvískriftar hefur verið lokið getur innleiðingaraðili farið í [Microsoft AppSource](https://appsource.microsoft.com/) og leitaðu að lausninni sem er nefnd [Tvískrifa viðskiptalausnir](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview). Settu upp pakkann með því að nota staðlaða uppsetningarhjálpina og prófaðu hann síðan með því að búa til möguleika á B2B-síðu. Eftir að tilvonandi er búinn til skaltu ganga úr skugga um að beiðnin sé sýnd á **Allar horfur** birtist í Commerce og staðfestu síðan að tilvonandi sé sýndur sem leiðandi í sölu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórna notendum samstarfsaðila á rafrænum B2B-vefsvæðum](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
