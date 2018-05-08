---
title: "Setja upp öryggisbúnað fyrir Power BI-efni greiningar á kostnaðarbókhaldi"
description: "Í þessu efnisatriði er útskýrt hvernig hægt er að yfirfæra aðgang á færslustigi í kostnaðarbókhaldi í línu á færslustigi í Microsoft Power BI. Þessi virkni hjálpar til við að tryggja að notendur sjá aðeins Power BI-gögn sem þeir fá aðgang að."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0c0faf0b12368273decacfae88c57707b350bf4
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Setja upp öryggisbúnað fyrir Power BI-efni greiningar á kostnaðarbókhaldi

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig hægt er að yfirfæra aðgang á færslustigi í kostnaðarbókhaldi í línu á færslustigi í Microsoft Power BI. Þessi virkni hjálpar til við að tryggja að notendur sjá aðeins Power BI-gögn sem þeir fá aðgang að.

<a name="overview"></a>Yfirlit
--------

Í **Greiningu á kostnaðarbókhaldi** notar Microsoft Power BI öryggi á línustigi til að takmarka aðgang notenda. Öryggi er byggt á aðgangsstigi stigveldis fyrirtækis sem eru sett upp í færibreytum kostnaðarbókhalds. Nánari upplýsingar um **Greiningu á kostnaðarbókhaldi** Power BI innihald er að finna í [Power BI-efni greiningar á kostnaðarbókhaldi](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Uppsetning
Til að yfirfæra öryggi á aðgangsstigi til Power BI þarf eigandi Power BI að fylgja eftirfarandi skrefum. **Athugasemd:** Notandinn sem gefur út Power BI-efni **Greiningar á kostnaðarbókhaldi** verður sjálfvirkt eigandi. Aðeins eigandi getur sett upp öryggi í Power BI. Þar að auki, þar til að eigandi bætir við öðrum notendum á PowerBI.com getur enginn nema eigandinn séð hvaða gögn í Power BI-efni **Greiningar á kostnaðarbókhaldi**.

1.  Birta Power BI í skilgreiningarskránni.
2.  Skráðu þig inn á PowerBI.com.
3.  Finna gagnamengi fyrir Power BI-efni **Greiningar á kostnaðarbókhaldi**
4.  Opnaðu öryggissíðuna. 

    ![Opna öryggissíðuna](./media/CA-picture-1.png)

5.  Hlutverkið **Stjórnborð kostnaðarhlutar** er þegar stofnað. Bæta við öðrum aðilum sem eru hluti af stigveldisskipan aðgangsstigs kostnaðarbókhalds. 

    ![Bæta við meðlimum](./media/CA-picture-2.png)

Notendur sem er bætt við hlutverkið **Stjórnborð kostnaðarhlutar** sjá aðeins gögnin sem þeir hafa heimild til að sjá, samkvæmt skilgreiningu í stigveldisskipan aðgangsstigs kostnaðarbókhalds. **Athugasemd:** Öryggi á línustigi gildir í reitum og skýrslum í Microsoft Dynamics 365 for Finance and Operations sem eru innfelld úr Power BI.

## <a name="updating-security"></a>Uppfæri öryggi
Ef uppfærslur eru gerðar á öryggi á aðgangsstigi í kostnaðarbókhaldi, og þú vilt að Power BI endurspegli þessar uppfærslur, þarf að uppfæra einingaverslun fyrir Power BI-efni **Greiningar á kostnaðarbókhaldi**. Eftir að þú lýkur uppfærslu á einingaverslun úr Finance and Operations verður að uppfæra gervinga á PowerBI.com. Nánari upplýsingar um hvernig á að gera uppfærslu á einingaverslun í [Uppfærsla einingaverslun](power-bi-integration-entity-store.md#update-entity-store). Eigandi Power BI-efnis **Greining kostnaðarbókhalds** verður einnig að gera uppfærslu einingaverslunar ef nýir notendur fá aðgang að stigveldisskipan. Þar að auki verður eigandi að bæta við nýjum notendum við hlutverk **Stjórnborð kostnaðarhlutar** á PowerBI.com, svo að öryggi á línustigi sé notað fyrir þá.

## <a name="disabling-security"></a>Afvirkjun öryggis
Gerum ráð fyrir að fyrirtækið vilji takmarka gagnaaðgengi. Ef af einhverri ástæðu, öryggi færibreyturnar verður óvirkt þegar kostnaðarbókhald er keyrt, eigandinn verður að bæta notendum við í hlutverkið **Kostnaðarbókari** í Power BI í staðinn. Ef öryggislyklinum er breytt úr virkri stöðu í óvirka stöðu, er góð hugmynd að fjarlægja notendur úr hlutverkinu **Stjórnborð kostnaðarhlutar**. Og öfugt ef þú endurvirkjar öryggisstillingar. Notendur geta tilheyrt báðum hlutverkum. Sameiginlegar aðgangur er sameining beggja hlutverka. Í tilfelli Power BI-efnis **Greining á kostnaðarbókhaldi** hafa notendur með sameiginlegan aðgang óheftan gagnaaðgang. Ef markmiðið er að nota takmarkaðan aðgang verður að úthluta notendum eingöngu á hlutverk **Stjórnborð kostnaðarhlutar**. Þessar uppfærslur á öryggi á línustigi taka strax gildi. Notendur sem verða fyrir áhrifum ættu að endurræsa vafra sína.

## <a name="additional-resources"></a>Frekari upplýsingar
Til að fræðast nánar um öryggi á línustigi Power BI, sjá [Stjórna öryggi líkansins í Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).




