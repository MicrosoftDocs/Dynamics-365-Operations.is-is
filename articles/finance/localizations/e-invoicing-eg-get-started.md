---
title: Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Egyptaland
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Egyptaland í Finance and Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592599"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a>Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Egyptaland

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Egyptaland. Efnisatriðið leiðir þig í gegnum skilgreiningarskrefi sem eru landsmiðuð í Regulatory Configuration Services (RCS) og bætast ofan á skrefin sem lýst er í [Hafist handa með viðbót rafrænnar reikningsfærslu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landsbundin skilgreining fyrir eiginleika rafrænnar reikningsfærslu fyrir rafrænan reikning í Egyptalandi (EG)

Til að skilgreina eiginleika rafrænnar reikningsfærslu fyrir rafræna reikninga í Egyptalandi (EG) þarf að ljúka nokkrum skrefum. Sumar færibreyturnar úr skilgreiningunum eru birtar með sjálfgefnum gildum og því verður að yfirfara þær og uppfæra svo þær henti betur fyrir viðskiptaaðgerðum þínum.

### <a name="prerequisites"></a>Forkröfur

Áður en ferlið er klárað í þessum hluta þarf að:

- Búa til leynilykil stafræns vottorðs eins og lýst er í hlutanum **Búa til leynilykil stafræns vottorðs** í [Hafist handa með þjónustuveitu viðbótar rafrænnar reikningsfærslu](e-invoicing-get-started-service-administration.md). Í prófunartilgangi veita egypsk skattyfirvöld ákveðnar prufur af stafrænum vottorðum sem þarf aðeins að nota við prófun og staðfestingu lausnar. Til að fá frekari upplýsingar skal skoða vefsvæði egypskra skattyfirvalda með tenglinum sem gefinn er upp í [SDK rafræn reikningsfærsla í Egyptalandi](https://sdk.sit.invoicing.eta.gov.eg/faq/).
- Búið til eiginleika rafrænnar reikningsfærslu fyrir egypskan rafrænan reikning (EG) fyrir fyrirtækið eins og lýst er í hlutanum **Stofna eiginleika rafrænnar reikningsfærslu undir þjónustuveitu fyrirtækisins** í [Hafist handa með viðbót rafrænnar reikningsfærslu](e-invoicing-get-started.md).

1. Í RCS, í hlutanum **Eiginleikar** á vinnusvæðinu **Altækur eiginleiki**, skal velja reitinn **Viðbót rafrænnar reikningsfærslu**.
2. Á síðunni **Eiginleikar viðbótar fyrir rafræna reikningsfærslu** skal staðfesta að rafræni reikningsfærslueiginleikinn **Egypskur rafrænn reikningur (EG)** sem var stofnaður sé valinn.
3. Í flipanum **Útgáfur** skal staðfesta að útgáfan **Drög** sé valin.
4. Í flipanum **Uppsetningar**, í hnitanetinu, skal velja eiginleikauppsetningu **Sölureiknings**.
5. Veljið **Breyta** og í flipanum **Aðgerðir**, í reitahópnum **Aðgerðir**, skal velja **Skrifa undir json-skjal fyrir egypsk skattyfirvöld**.
6. Í reitahópnum **Færibreytur** skal velja færibreytuna, **Heiti vottorðs** og velja heiti stafræna vottorðsins sem er stofnað til að nota eiginleika rafrænnar reikningsfærslu.
7. Í reitahópnum **Aðgerðir** skal velja **Samþætta við egypska ETA-þjónustu**. Endurtakið þetta skref fyrir tvö tilvik þessarar aðgerðar.
8. Í reitahópnum **Færibreytur** skal velja **Vefslóð þjónustu** og **Skrá inn vefslóð þjónustu** og, ef þörf krefur, fara yfir færibreytur vefslóðar. Skoða skal vefsvæði egypskra skattyfirvalda til að fá vefslóð prófunar og framleiðslu með því að nota tengilinn sem gefinn er upp í [SDK rafrænnar reikningsfærslu fyrir Egyptaland](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Veljið **Vista** og lokið síðunni.
10. Til að skilgreina uppsetningu forritsins skal sjá [Hafist handa með viðbót rafrænnar reikningsfærslu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landsbundin skilgreining forritsuppsetningar fyrir eiginleika rafrænnar reikningsfærslu fyrir rafrænan reikning í Egyptalandi (EG)

Skilgreining á uppsetningu forrits fyrir rafræna reikningsfærslueiginleikann **Rafrænn reikningur Egyptalands (EG)** krefst þess að tiltekin skref verði kláruð. Ljúka þarf þessum skrefum áður en settur er upp eiginleiki rafrænnar reikningsfærslu í þjónustuumhverfi viðbótar rafrænnar reikningsfærslu.

### <a name="prerequisites"></a>Forkröfur

Áður en þú klárar ferlið í þessum hluta skaltu stofna og setja af stað rafræna reikningsfærslueiginleikann **Egypskur rafrænn reikningur (EG)** til að skilgreina uppsetningu forritsins fyrir rafrænan reikningsfærslueiginleikann **Egypskur rafrænn reikningur (EG)** eins og lýst er í hlutanum **Skilgreina uppsetningu forrits** í efnisatriðinu [Hafist handa með viðbót rafrænnar reikningsfærslu](e-invoicing-get-started.md).

1. Í RCS, í hlutanum **Eiginleikar** á vinnusvæðinu **Altækur eiginleiki**, skal velja reitinn **Viðbót rafrænnar reikningsfærslu**.
2. Á síðunni **Eiginleikar viðbótar fyrir rafræna reikningsfærslu** skal staðfesta að rafræni reikningsfærslueiginleikinn **Egypskur rafrænn reikningur (EG)** sé valinn.
3. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
4. Í flipanum **Uppsetningar** skal velja **Uppsetning forrits** og í reitnum **Tengt forrit** skal velja forritið þar sem á að setja upp.
5. Í reitnum **Töfluheiti** skal staðfesta að reikningabók viðskiptavinar sé valin.
6. Veljið **Svargerðir** og veljið síðan **Ný**.
7. Í reitinn **Svargerð** skal færa inn „Svar“ og í reitinn **Lýsing** skal færa inn „Lýsing“.
8. Í reitnum **Staða sendingar** skal velja **Í bið**.
9. Í reitnum **Líkanavörpun** skal velja **Líkanavörpun úr svarskilaboðum** með **(Forútgáfa) Innflutningssnið svarskilaboða** og síðan velja **Vista**.
10. Veljið **Ný** og í reitinn **Svargerð** skal færa inn „ResponseData“ sem fast gildi. Í reitinn **Lýsing** skal færa inn „Lýsing“.
11. Í reitnum **Staða sendingar** skal velja **Í bið**.
12. Í reitnum **Heiti gagnaeiningar** skal velja **Sölureikningshausar V2**.
13. Í reitinn **Líkanavörpun** skal velja **Gagnainnflutningur á egypsku svari** með **(Forútgáfa) Gagnainnflutningur á egypsku svari** og veljið síðan **Vista**.
14. Til að nota eiginleika rafrænnar reikningsfærslu skal skoða [Hafist handa með viðbót rafrænnar reikningsfærslu](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Til að virkja eiginleikann **Egypskur rafrænn reikningur (EG)** þarf hugsanlega að senda takmörkuð gögn, þ.m.t. skattskráningarkenni fyrirtækisins. Þessi gögn verða send til stofnana þriðja aðila sem skattyfirvöld heimila að megi senda rafræna reikninga til þessara skattyfirvalda á fyrirframskilgreindu sniði sem þarf fyrir samþættingu við vefþjónustu yfirvalda. Stjórnandi getur kveikt og slökkt á eiginleikanum með því að fara í **Fyrirtækisstjórnun** > **Uppsetning** > **Færibreytur rafrænna skjala**. Í flipanum **Eiginleikar** skal velja línuna sem inniheldur eiginleikann **Egypskur rafrænn reikningur (EG)** og síðan velja viðeigandi atriði. Gögn sem eru flutt inn úr þessum ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132). Frekari upplýsingar er að finna í köflunum um persónuverndaryfirlýsingu í fylgiskjölum um eiginleika eftir löndum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit innbótar rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með viðbót rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með innbót rafrænna reikninga](e-invoicing-get-started.md)
- [Rafrænir reikningar viðskiptavinar í Egyptalandi](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
