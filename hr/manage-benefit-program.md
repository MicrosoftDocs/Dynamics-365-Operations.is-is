---
title: "Skilgreina og stjórna fríðindum forritið"
description: "Mannauður býður upp á verkfæri til að setja upp og viðhalda fríðindi, frádráttur og launafyrirkomulag sem fyrirtæki býður upp á eða vinnur fyrir sína starfsmenn. Þessi skrá veitir upplýsingar um hvernig setja á upp stjórna fríðindum."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Skilgreina og stjórna fríðindum forritið

Mannauður býður upp á verkfæri til að setja upp og viðhalda fríðindi, frádráttur og launafyrirkomulag sem fyrirtæki býður upp á eða vinnur fyrir sína starfsmenn. Þetta efni veitir upplýsingar um hvernig stjórna fríðindum.

<a name="benefit-setup"></a>Uppsetningu fríðinda
-------------

Áður en hægt er að skrá starfsmenn í fríðindi verður að stofna einingar fyrir hverja fríðinda. Þessar einingar sameina svipuð fríðindaáætlanir og skilgreinið sjálfgefnar stillingar, eins og frádráttuartaxta og bókhaldsupplýsingum. Margar af þessum stillingum er hægt að leiðrétta þegar starfsmenn eru skráðir síðar í fríðindi. Fyrir hverja fríðindaáætlun getur fyrirtæki bjóða nokkrar skráningavalkosti eða starfsmaður fellt niður skráningu í áætlun. 

[![Vinnsluflæði fríðinda](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Fríðindaeiningar
Áður en byrjað er stofna fríðindi og skrá starfsmenn í þær verður að skilgreina einingar sem mynda fríðindi: gerð, áætlun, og valkosti.

-   **Gerð ** – Safn áætlana fyrir tiltekin fríðindi, eins og læknisþjónusta eða bílastæði.
-   **Áætlun ** – Tiltekin fríðindi sem er fenginn samkvæmt samningi frá veitanda.
-   **Valkostur ** – Tryggingarstig, svo sem starfsmaður eingöngu eða starfsmaður og maki.

Fyrir hverja fríðindagerð, eins og sjón eða tannlæknaþjónusta, getur fyrirtæki hægt bjóða einum eða fleiri áætlunum starfsmönnum sínum. Fyrir hverja áætlun getur fyrirtækið boðið mismunandi valkostir. Starfsmenn geta til dæmis kaupa viðbótar líftryggingar sem þekja eitt, tvö eða þrisvar sinnum árleg laun þeirra. Hver samsetning áætlunar og valkosta verða fríðindi sem starfsmenn geta skrá sig í. 

[![pic fríðinda](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Hæfni
Mörgum þáttum ákvarða hæfni starfsmanns fyrir mismunandi gerðir af fríðindum sem vinnuveitandi býður uppá. Þegar fríðindi eru stofnaðar í Microsoft Dynamics 365 aðgerða er hægt að setja gerð hæfni sem á við sem fríðindin. 

Hægt er að gera fríðindi tiltæk til allra starfsmanna. Til dæmis sumum fyrirtækjum bjóða bílastæði stenst fyrir alla starfsmenn sem er jaðarfríðinda. Þegar þú stofna þessi fríðindi, stillirðu hæfniskilyrði á **allt starfsfólk eru uppfyllir hæfniskilyrði**. 

Hæfni ekki nota fyrir önnur fríðindi svo garnishments og levies skatt. Whey þessar gerðir af fríðindum er stofnuð, er að stilla á hæfni **Sniðganga mat á hæfni**. 

Loks hæfni til fríðinda er hægt að byggja. Til dæmis fyrirtæki býður upp á tvær gerðir af fríðindum líftíma tryggingar til starfsmanna. Markaðsstjóra starfsmenn eru hæfar fyrir eina líftíma tryggingar áætlun meðan allra annarra starfsmanna í fullu starfi eru hæfar fyrir aðrar líftíma tryggingar áætlun. Í Dynamics 365 aðgerða er hægt að stofna hæfnisreglu fríðinda til að finna markaðsstjóra alla starfsmenn og aðra reglu til að leita að allar aðrar starfi og eiga þessar reglur við viðeigandi fríðindi.

## <a name="enrollment"></a>Skráning
Eftir að fríðindi sem fyrirtækið býður upp hafa verið stofnuð og hæfni ákvörðuð, er hægt að skrá starfsmenn í fríðindi. Hægt er að skrá einn starfsmanns í fríðindum, eða hægt er að skrá mörgum starfsmönnum í ein eða fleiri fríðindi í einni vinnslu. 

Stundum hættir fyrirtæki að bjóða ákveðnum fríðindi. Í þessu tilfelli þarf að uppfæra fríðindin og starfsmenn sem skráðir eru í. Lokadagur fjöldafríðinda er hægt að breyta lokadegi fríðindi og innskráningu starfsmanns sem fríðinda á sama tíma. Einnig er hægt að velja marga starfsmenn sem eru skráðir í fríðindi og breyta lokadagsetningu þekju þeirra. 

Á sama hátt leyfa fjöldafríðinda þér að breyta lokadegi fríðindi og innskráningu starfsmanns fyrir þau fríðindi á sama tíma ef þú ákveður að bjóta fríðindi lengur ef þú upprunalega áætlaðir.

<a name="see-also"></a>Sjá einnig
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


