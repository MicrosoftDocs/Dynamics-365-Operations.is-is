---
title: Stjórnaðu notendum viðskiptafélaga á B2B rafrænum viðskiptavefsíðum með því að nota Dynamics 365 Sales
description: Þetta efni lýsir því hvernig á að nota Microsoft Dynamics 365 Sala til að stjórna samþykki viðskiptafélaga fyrir Dynamics 365 Commerce fyrirtæki til fyrirtækja (B2B) vefsíður.
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c6ac5409de5101c91b9348de800e3eaea9895c23
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312133"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Stjórnaðu notendum viðskiptafélaga á B2B rafrænum viðskiptavefsíðum með því að nota Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Þetta efni lýsir því hvernig á að nota Microsoft Dynamics 365 Sala til að stjórna samþykki viðskiptafélaga fyrir Dynamics 365 Commerce fyrirtæki til fyrirtækja (B2B) vefsíður. Stofnanir sem þegar hafa fjárfest í Dynamics 365 Sales lausninni geta notað leiðar- og tækifærishugtök hennar fyrir samþykkisferli viðskiptafélaga í B2B rafrænum viðskiptum.

Fyrir bakgrunnsupplýsingar um samþykkisferlið B2B viðskiptafélaga, sjá [Stjórna notendum viðskiptafélaga á B2B rafrænum viðskiptavefsíðum](manage-b2b-users.md).

Hugsanlegir viðskiptafélagar geta hafið inngönguferlið á B2B rafræn viðskipti vefsíðu með því að senda inn beiðni um borð í gegnum hlekk á B2B vefsíðunni. Eftir að beiðnin hefur verið lögð fram og viðkomandi störf (ss **P-0001** og **Samstilltu pantanir og rásbeiðnir**) eru keyrð í höfuðstöðvum Commerce, er inngöngubeiðnin vistuð á **Allar horfur** síðu í höfuðstöðvum Commerce. Síðan er hægt að ljúka við samþykkisferli viðskiptafélaga í sölu.

Eftir að samþætting á milli sölu og viðskipta hefur verið virkjuð veldur stofnun viðskiptafélaga í Commerce því að *leiða* í sölu.

Eftirfarandi mynd sýnir dæmi um síðu til að búa til viðskiptavin fyrir tilvonandi viðskiptafélaga í sölu.

![Síða um að búa til kynningar í Dynamics 365 Sales.](../media/LeadInSales.png)

Í myndinni er **Hafðu samband** kafla sýnir manneskjuna sem sendi inn beiðni um borð og **Fyrirtæki** kafla sýnir skipulagið. Athugasemd í **Tímalína** kafla gefur til kynna að leiðin hafi verið mynduð af tvískrifa innviði. Vegna þess að það var búið til af tvískrifa innviði, mun þetta leiða ekki birtast í **Opnu leiðirnar mínar** fellilistanum. Í staðinn mun það birtast undir nýju útsýni sem er nefnt **Öll viðskipti B2B leiða**.

Samkvæmt stöðluðu ferli hæfishæfisenda í sölu, þegar notandi „hæfir“ forystuna, er an *tækifæri* skrá, a *samband* met, og an *reikning* skrár eru búnar til. Tvískrifa innviðirnir eru notaðir til að skrifa tengiliðinn og reikningsskrárnar til Commerce. Tengiliðurinn er stofnaður sem viðskiptavinur *manneskju* gerð, og fyrirtækið er stofnað sem viðskiptavinur *skipulag* tegund. Ef notandi velur **Loka sem vann** fyrir tækifærið er tilboðið samþykkt í Commerce. Samþykki viðskiptavinar veldur því að stigveldi viðskiptavina er búið til.

Öll viðskiptaferli sem eftir eru eiga sér stað í Commerce. Þessi ferli fela í sér að senda tölvupóst til viðskiptafélaga, skilgreina stjórnun lánamarka fyrir notendur og bæta við fleiri notendum á B2B síðuna. Hins vegar, ef notandi hafnar forystunni eða merkir tækifærið sem glatað í stað þess að vera hæft til forystunnar, er tilvonandi í Commerce merktur sem hafnað og tölvupóstur um höfnun um borð er sendur til umsækjanda.

## <a name="enable-integration-between-sales-and-commerce"></a>Virkjaðu samþættingu milli sölu og viðskipta

Samþætting milli sölu og viðskipta byggir á tvískrifa innviði. Þess vegna ætti tvískrifað að vera virkt og virka þannig að viðskiptavinir sem eru búnir til í einu kerfinu séu skrifaðir í hitt kerfið. Fyrir frekari upplýsingar um tvískrifa innviði, sjá [Tvöföld skrif yfirlit](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Eftir að uppsetningu tvískrifa hefur verið lokið getur innleiðingaraðili farið í [Microsoft AppSource](https://appsource.microsoft.com/) og leitaðu að lausninni sem er nefnd [Tvískrifa viðskiptalausnir](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview). Settu upp pakkann með því að nota staðlaða uppsetningarhjálpina og prófaðu hann síðan með því að búa til möguleika á B2B síðu. Eftir að tilvonandi er búinn til skaltu ganga úr skugga um að beiðnin sé sýnd á **Allar horfur** birtist í Commerce og staðfestu síðan að tilvonandi sé sýndur sem leiðandi í sölu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórna notendum samstarfsaðila á rafrænum B2B-vefsvæðum](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
