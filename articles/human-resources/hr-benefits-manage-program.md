---
title: Skilgreina og stjórna fríðindaáætlun
description: Mannauður býður upp á verkfæri til að setja upp og viðhalda fríðindi, frádráttur og launafyrirkomulag sem fyrirtæki býður upp á eða vinnur fyrir sína starfsmenn. Þessi skrá veitir upplýsingar um hvernig setja á upp og stjórna fríðindum.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 08b80f4f90ce6b4a286120cd6329a45a4ebd3f71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877802"
---
# <a name="define-and-manage-a-benefits-program"></a>Skilgreina og stjórna fríðindaáætlun


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Human Resources býður upp á verkfæri til að setja upp og viðhalda fríðindi, frádráttur og launafyrirkomulag sem fyrirtæki býður upp á eða vinnur fyrir sína starfsmenn. Þessi skrá veitir upplýsingar um hvernig setja á upp og stjórna fríðindum.

## <a name="benefit-setup"></a>Uppsetning á fríðindum

Áður en hægt er að skrá starfsmenn í fríðindi verður að stofna einingar fyrir hverja fríðinda. Þessar einingar sameina svipuð fríðindaáætlanir og skilgreinið sjálfgefnar stillingar, eins og frádráttuartaxta og bókhaldsupplýsingum. Margar af þessum stillingum er hægt að leiðrétta þegar starfsmenn eru skráðir síðar í fríðindi. Fyrir hverja fríðindaáætlun getur fyrirtæki bjóða nokkrar skráningavalkosti eða starfsmaður fellt niður skráningu í áætlun. 

[![Flæði fríðindaferla.](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Fríðindaeiningar

Áður en byrjað er stofna fríðindi og skrá starfsmenn í þau verður að skilgreina einingar sem mynda fríðindi: gerð, áætlun, og valkosti.

-   **Gerð** – Safn áætlana fyrir tiltekin fríðindi, eins og læknisþjónusta eða bílastæði.
-   **Áætlun** – Tiltekin fríðindi sem er fenginn samkvæmt samningi frá veitanda.
-   **Valkostur** – Tryggingarstig, svo sem starfsmaður eingöngu eða starfsmaður og maki.

Fyrir hverja fríðindagerð, eins og sjón eða tannlæknaþjónusta, getur fyrirtæki hægt bjóða einum eða fleiri áætlunum starfsmönnum sínum. Fyrir hverja áætlun getur fyrirtækið boðið mismunandi valkostir. Starfsmenn geta til dæmis kaupa viðbótar líftryggingar sem þekja eitt, tvö eða þrisvar sinnum árleg laun þeirra. Hver samsetning áætlunar og valkosta verða fríðindi sem starfsmenn geta skrá sig í. 

[![fríðindamynd.](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Hæfi
Mörgum þáttum ákvarða hæfni starfsmanns fyrir mismunandi gerðir af fríðindum sem vinnuveitandi býður uppá. Þegar fríðindi eru stofnuð í Dynamics 365 Human Resources er hægt að stilla hæfnigerð sem á við um fríðindin. 

Hægt er að gera fríðindi tiltæk til allra starfsmanna. Til dæmis bjóða sum fyrirtækjum bílastæðapassa fyrir alla starfsmenn sem er hliðarfríðindi. Þegar þú stofna þessi fríðindi, stillirðu hæfniskilyrði á **allt starfsfólk eru uppfyllir hæfniskilyrði**. 

Fyrir önnur fríðindi, svo sem frádráttur frá launum og skattheimtu, á hæfni ekki við. Þegar þú búa til þessar tegundir af fríðindum, stillirðu hæfni til að **fara framhjá hæfniferli** 

Að lokum, fríðindahæfni getur byggt á reglum. Til dæmis býður fyrirtæki upp á tvær gerðir af fríðindum fyrir líftryggingar til starfsmanna. Yfirmenn á meðan starfsmanna eru hæfar fyrir eina líftryggingaáætlun á meðan allir aðrir starfsmanna í fullu starfi eru hæfar fyrir aðra líftryggingaráætlun. Í Human Resources er hægt að stofna hæfnisreglu fríðinda til að finna alla yfirmenn og aðrar reglur til að finna aðra starfsmenn í fullu starfi og svo nota þær reglur fyrir viðeigandi fríðindi.

## <a name="enrollment"></a>Skráning
Eftir að fríðindi sem fyrirtækið býður upp hafa verið stofnuð og hæfni ákvörðuð, er hægt að skrá starfsmenn í fríðindi. Hægt er að skrá einn starfsmanns í fríðindum, eða hægt er að skrá mörgum starfsmönnum í ein eða fleiri fríðindi í einni vinnslu. 

Stundum hættir fyrirtæki að bjóða ákveðnum fríðindi. Í þessu tilfelli þarf að uppfæra fríðindin og starfsmenn sem skráðir eru í þau. Lokadagur fjöldafríðinda leyfir þér að breyta lokadegi fríðindi og innskráningu starfsmanns fyrir þau fríðindi á sama tíma. Einnig er hægt að velja marga starfsmenn sem eru skráðir í fríðindi og breyta lokadagsetningu þekju þeirra. 

Á sama hátt leyfa fjöldafríðinda þér að breyta lokadegi fríðindi og innskráningu starfsmanns fyrir þau fríðindi á sama tíma ef þú ákveður að bjóta fríðindi lengur ef þú upprunalega áætlaðir.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
