---
title: Hafist handa með rafrænar reikningsfærslur fyrir Egyptaland
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með rafrænni reikningsfærslu fyrir Egyptaland í Finance and Supply Chain Management.
author: gionoder
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b25a3489d009a02b45d66d4c3a0271a56a92f5ac
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985626"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>Hafist handa með rafrænar reikningsfærslur fyrir Egyptaland

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Egyptaland. Efnisatriðið leiðir þig í gegnum skilgreiningarskrefi sem eru landsmiðuð í Regulatory Configuration Services (RCS) og bætast ofan á skrefin sem lýst er í [Hafist handa með rafrænni reikningsfærslu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landsbundin skilgreining fyrir eiginleika rafrænnar reikningsfærslu fyrir rafrænan reikning í Egyptalandi (EG)

Sumar færibreyturnar úr **rafræna reikningseiginleikanum fyrir Egypskan rafrænan reikning (EG)** eru birtar með sjálfgefnum gildum. Farið yfir gildin og, ef þörf krefur, uppfærið gildin svo þau endurspegli betur fyrirtækjareksturinn áður en rafræni reikningseiginleikinn er notaður í þjónustuumhverfinu.

Þessi hluti tengist **Landsbundin skilgreining fyrir eiginleika rafrænnar reikningsfærslu** hlutanum í efnisatriðinu [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

### <a name="prerequisites"></a>Forkröfur

Áður en ferlið er klárað í þessum hluta þarf að:

- Búa til leynilykil stafræns vottorðs eins og lýst er í hlutanum **Búa til leynilykil stafræns vottorðs** í [Hafist handa með stjórnun þjónustu rafrænna reikninga](e-invoicing-get-started-service-administration.md). Í prófunartilgangi veita egypsk skattyfirvöld ákveðnar prufur af stafrænum vottorðum sem þarf aðeins að nota við prófun og staðfestingu lausnar. Til að fá frekari upplýsingar skal skoða vefsvæði egypskra skattyfirvalda með tenglinum sem gefinn er upp í [SDK rafræn reikningsfærsla í Egyptalandi](https://sdk.sit.invoicing.eta.gov.eg/faq/).

1. Í RCS, í hlutanum **Eiginleikar** á vinnusvæðinu **Altækur eiginleiki**, skal velja reitinn **Rafræn reikningsfærsla**.
2. Á síðunni **Eiginleikar fyrir rafræna reikningsfærslu** skal staðfesta að rafræni reikningsfærslueiginleikinn **Egypskur rafrænn reikningur (EG)** sem var stofnaður sé valinn.
3. Í flipanum **Útgáfur** skal staðfesta að útgáfan **Drög** sé valin.
4. Í flipanum **Uppsetningar**, í hnitanetinu, skal velja eiginleikauppsetningu **Sölureiknings**.
5. Veljið **Breyta** og í flipanum **Aðgerðir**, í reitahópnum **Aðgerðir**, skal velja **Skrifa undir json-skjal fyrir egypsk skattyfirvöld**.
6. Í reitahópnum **Færibreytur** skal velja færibreytuna, **Heiti vottorðs** og velja heiti stafræna vottorðsins sem er stofnað til að nota eiginleika rafrænnar reikningsfærslu.
7. Í reitahópnum **Aðgerðir** skal velja **Samþætta við egypska ETA-þjónustu**. Endurtakið þetta skref fyrir tvö tilvik þessarar aðgerðar.
8. Í reitahópnum **Færibreytur** skal velja **Vefslóð þjónustu** og **Skrá inn vefslóð þjónustu** og, ef þörf krefur, fara yfir færibreytur vefslóðar. Skoða skal vefsvæði egypskra skattyfirvalda til að fá vefslóð prófunar og framleiðslu með því að nota tengilinn sem gefinn er upp í [SDK rafrænnar reikningsfærslu fyrir Egyptaland](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Veljið **Vista** og lokið síðunni.
10. Til að nota eiginleika rafrænnar reikningsfærslu skal skoða [Hafist handa með rafrænni reikningsfærslu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landsbundin skilgreining forritsuppsetningar fyrir eiginleika rafrænnar reikningsfærslu fyrir rafrænan reikning í Egyptalandi (EG)

Ljúkið þessum skrefum áður en uppsetning forritsins er virkjuð í forriti sem er tengt við Finance eða Supply Chain Management.

Þessi hluti tengist **Landsháð grunnstilling á uppsetningu forrits** hlutanum í efnisatriðinu [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

1. Í RCS, í hlutanum **Eiginleikar** á vinnusvæðinu **Altækur eiginleiki**, skal velja reitinn **Rafræn reikningsfærsla**.
2. Á síðunni **Eiginleikar fyrir rafræna reikningsfærslu** skal staðfesta að rafræni reikningsfærslueiginleikinn **Egypskur rafrænn reikningur (EG)** sé valinn.
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
14. Til að virkja uppsetningu forritsins í Finance eða Supply Chain Management tengd forrit skal skoða [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Til að virkja eiginleikann **Egypskur rafrænn reikningur (EG)** þarf hugsanlega að senda takmörkuð gögn, þ.m.t. skattskráningarkenni fyrirtækisins. Þessi gögn verða send til stofnana þriðja aðila sem skattyfirvöld heimila að megi senda rafræna reikninga til þessara skattyfirvalda á fyrirframskilgreindu sniði sem þarf fyrir samþættingu við vefþjónustu yfirvalda. Stjórnandi getur kveikt og slökkt á eiginleikanum með því að fara í **Fyrirtækisstjórnun** > **Uppsetning** > **Færibreytur rafrænna skjala**. Í flipanum **Eiginleikar** skal velja línuna sem inniheldur eiginleikann **Egypskur rafrænn reikningur (EG)** og síðan velja viðeigandi atriði. Gögn sem eru flutt inn úr þessum ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132). Frekari upplýsingar er að finna í köflunum um persónuverndaryfirlýsingu í fylgiskjölum um eiginleika eftir löndum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md)
- [Rafrænir reikningar viðskiptavinar í Egyptalandi](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
