---
title: Uppsetning öryggis fyrir kostnaðarbókhaldsgreiningar Power BI efni
description: Í þessu efnisatriði er útskýrt hvernig hægt er að yfirfæra aðgang á færslustigi í kostnaðarbókhaldi í línu á færslustigi í Microsoft Power BI. Þessi virkni hjálpar til við að tryggja að notendur sjá aðeins Power BI gögn sem þeir fá aðgang að.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d1cd378a58d4a4fe4388238f97e84a8e2b07937b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551461"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Uppsetning öryggis fyrir kostnaðarbókhaldsgreiningar Power BI efni

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig hægt er að yfirfæra aðgang á færslustigi í kostnaðarbókhaldi í línu á færslustigi í Microsoft Power BI. Þessi virkni hjálpar til við að tryggja að notendur sjá aðeins Power BI gögn sem þeir fá aðgang að.

## <a name="overview"></a>Yfirlit

**Greining á kostnaðarbókhaldi** Microsoft Power BI efni notar Power BI öryggi á línustigi til að takmarka aðgang notenda. Öryggi er byggt á aðgangsstigi stigveldis fyrirtækis sem eru sett upp í færibreytum kostnaðarbókhalds. Nánari upplýsingar um **Greiningu á kostnaðarbókhaldi** Power BI innihald er að finna í [Power BI-efni greiningar á kostnaðarbókhaldi](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Uppsetning
Til að yfirfæra öryggi á aðgangsstigi til Power BI þarf eigandi Power BI efnis að fylgja eftirfarandi skrefum.

> [!NOTE]
> Notandinn sem gefur út **Greiningar á kostnaðarbókhaldi** Power BI-efni verður sjálfvirkt eigandi. Aðeins eigandi getur sett upp öryggi í Power BI. Þar að auki, þar til að eigandi bætir við öðrum notendum á PowerBI.com getur enginn nema eigandinn séð hvaða gögn í **Greiningar á kostnaðarbókhaldi** Power BI efni.

1. Birta Power BI í skilgreiningarskránni.
2. Skráðu þig inn á PowerBI.com.
3. Finna gagnamengi fyrir **Greiningar á kostnaðarbókhaldi** Power BI efni.
4. Opnaðu öryggissíðuna.

    ![Opna öryggissíðuna](./media/CA-picture-1.png)

5. Hlutverkið **Stjórnborð kostnaðarhlutar** er þegar stofnað. Bæta við öðrum aðilum sem eru hluti af stigveldisskipan aðgangsstigs kostnaðarbókhalds.

    ![Bæta við meðlimum](./media/CA-picture-2.png)

Notendur sem er bætt við hlutverkið **Stjórnborð kostnaðarhlutar** sjá aðeins gögnin sem þeir hafa heimild til að sjá, samkvæmt skilgreiningu í stigveldisskipan aðgangsstigs kostnaðarbókhalds.

> [!NOTE]
> Athugasemd: Öryggi á línustigi gildir í reitum og skýrslum í Microsoft Dynamics 365 for Finance and Operations sem eru innfelld úr Power BI.

## <a name="updating-security"></a>Uppfæri öryggi
Ef uppfærslur eru gerðar á öryggi á aðgangsstigi í kostnaðarbókhaldi, og þú vilt að Power BI endurspegli þessar uppfærslur, þarf að uppfæra einingaverslun fyrir **Greiningar á kostnaðarbókhaldi** Power BI efni. Eftir að þú lýkur uppfærslu á einingaverslun úr Finance and Operations verður að uppfæra gervingar á PowerBI.com. Nánari upplýsingar um hvernig á að gera uppfærslu á einingaverslun í [Uppfærsla einingaverslun](power-bi-integration-entity-store.md#update-entity-store). Eigandi **Greining kostnaðarbókhalds** Power BI-efnis verður einnig að gera uppfærslu einingaverslunar ef nýir notendur fá aðgang að stigveldisskipan. Þar að auki verður eigandi að bæta við nýjum notendum við hlutverk **Stjórnborð kostnaðarhlutar** á PowerBI.com, svo að öryggi á línustigi sé notað fyrir þá.

## <a name="disabling-security"></a>Afvirkjun öryggis
Gerum ráð fyrir að fyrirtækið vilji takmarka gagnaaðgengi. Ef af einhverri ástæðu, öryggi færibreyturnar verður óvirkt þegar kostnaðarbókhald er keyrt, verður eigandinn að bæta notendum við í hlutverkið **Kostnaðarbókari** í Power BI í staðinn. Ef öryggislyklinum er breytt úr virkri stöðu í óvirka stöðu, er góð hugmynd að fjarlægja notendur úr hlutverkinu **Stjórnborð kostnaðarhlutar**. Og öfugt ef þú endurvirkjar öryggisstillingar. Notendur geta tilheyrt báðum hlutverkum. Sameiginlegar aðgangur er sameining beggja hlutverka. Í tilfelli **Greining á kostnaðarbókhaldi** Power BI efnis hafa notendur með sameiginlegan aðgang óheftan gagnaaðgang. Ef markmiðið er að nota takmarkaðan aðgang verður að úthluta notendum eingöngu á hlutverk **Stjórnborð kostnaðarhlutar**. Þessar uppfærslur á öryggi á línustigi taka strax gildi. Notendur sem verða fyrir áhrifum ættu að endurræsa vafra sína.

## <a name="additional-resources"></a>Frekari upplýsingar
Til að fræðast nánar um Power BI öryggi á línustigi, sjá [Stjórna öryggi líkansins í Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).
