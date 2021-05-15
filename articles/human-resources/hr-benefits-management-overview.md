---
title: Yfirlit fríðindastjórnunar
description: Yfirlit yfir eiginleika stjórnunar fríðinda í Dynamics 365 Human Resources. Bjóddu starfsmönnum þínum framlengda valkosti með auðveldri notkun á netinu.
author: andreabichsel
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4ad94d81d7e8bedd3622b3e073e431bc4abaafff
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924231"
---
# <a name="benefits-management-overview"></a>Yfirlit fríðindastjórnunar

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Til að vera samkeppnishæfur verður þú að bjóða upp á mikið af fríðindum til að laða að og halda bestu starfsmönnum þínum. Til viðbótar við venjulegan ávinning eins og læknisfræðilega og tannlæknaþjónustu, gætirðu líka viljað bjóða upp á stækkaða þjónustu eins og ættleiðingaraðstoð, afþreyingarforrit og fatapeninga. Fríðindastjórnun í Microsoft Dynamics 365 Human Resources veitir þér sveigjanlega lausn sem styður fjölbreytt úrval af kostum. Human Resources felur einnig í sér nothæfa reynslu starfsmanna sem sýnir framboð þitt.

- Auknar fríðindaáætlanir gera þér kleift að búa til og hafa umsjón með einstökum fríðindaáætlunum og styðja flóknar töflur um fríðindahlutfall og ívafin stig. Þú getur auðveldlega búið til fríðindaáætlanir, knippi og sjálfvirkar innritunarreglur til að auðvelda starfsmannaupplifun.

- Flex lánstraust forrit gera þér kleift að styðja við starfslok og aðra atburði í lífinu.

- Víðtækar hæfisreglur tryggja að þú gerir rétt fríðindi tiltæk réttum starfsmönnum.

- Netskráning í fríðindi veitir starfsmönnum þínum auðvelda reynslu.

- Hæf vinnsla á atburði í lífinu styður framtíðarviðburði.

Ef þú vilt fá aðgang að kynningargögnum þarftu að dreifa sandkassumhverfinu þínu á nýjan leik.

>[!NOTE]
>Nú er hægt að sérsníða skjámyndir fríðindastjórnunar. Nú er hægt að bæta sérstilltum reitum sem tengjast tryggingarhlutföllum í skjámyndinni **Tryggingarvalkostur** fyrir fríðindaáætlanir. Frekari upplýsingar um hvernig unnið er með sérstillta reiti er að finna í [Sérstilltir reitir](hr-developer-custom-fields.md).
>![Sérstilltir reitir fríðindastjórnunar](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Virkja fríðindastjórnun

Þetta efnisatriði lýsir því hvernig á að kveikja á eiginleikum í Human Resources. Hún segir einnig frá hvaða eiginleikum sem eru fyrir hendi í starfsmannamálum sem bótastjórnun kemur í stað eða er óvirk þegar þú kveikir á Fríðindastjórnun.

> [!IMPORTANT]
> ÞEgar þú hefur virkjað fríðindastjórnun í umhverfi **Framleiðslu** er ekki hægt að afvirkja hana. Við mælum með að virkja og prófa ávinning stjórnunar í umhverfinu **Sandkassi** áður en það er gert kleift í umhverfi **Framleiðslu**. Það er verulegur munur á gamall fríðindavirkni og nýrrar virkni stjórnunar fríðinda sem krefst viðbótaruppsetningar og ætti að prófa áður en þeir eru settir í framleiðslu.

- [Vinna með eiginleika](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Stilla starfsmannaupplýsingum

Áður en þú getur skráð starfsmenn í fríðindi verður þú að veita nauðsynlegar upplýsingar. Þú verður að skrá starfsmann í **Áætlun fastra launa** á upphafsdegi hans og þú verður að velja **Greiðslutíðni fríðinda** í **Atvinnuupplýsingar** í glugganum **Starfskraftur**.

Ef um er að ræða starfsmann sem fær viðbótarlaun líkt og þóknanir er hægt að bæta við **Árleg launatengd fríðindi** upphæð úr starfsmannafærslu. Human Resources notar **Árleg launatengd fríðindi** upphæð við ákvörðun tryggingaupphæðar, í stað árlega upphæð fastra launa. **Árleg launatengd fríðindi** verða að vera gild frá upphafsdagsetningu starfsmanns eða frá upphaf fríðindatímabilsins, hvort sem er síðar. Ef bæði föst laun og upphæð árlegra launatengdra fríðinda eru skráð fyrir starfsmann verða árleg launatengd fríðindi notuð við ákvörðun á tryggingaupphæðum.

Þegar þú býrð til bótaáætlun þar sem notast er við tíðni sem byggist á kyni eða aldri, verður þú að færa inn fæðingardag og kyn starfsmanns til að reikna út fríðindakostnaðinn.

## <a name="configure-benefits-management"></a>Grunnstilla fríðindastjórnun

Áður en þú getur búið til fríðindaáætlun fyrir starfsmenn þína þarftu að stilla valkosti fyrir áætlanirnar.

- [Stilla færibreytur fríðindastjórnunar](hr-benefits-setup-parameters.md)
- [Grunnstilla hæfnireglur og valkosti](hr-benefits-setup-eligibility-rules.md)
- [Grunnstilla hæfnisvalkosti persónulegs tengiliðar](hr-benefits-setup-contact-eligibility-options.md)
- [Stofna tryggingarvalkosti](hr-benefits-setup-coverage-options.md)
- [Setja upp greiðslutíðni](hr-benefits-setup-payment-frequencies.md)
- [Grunnstilla gerðir viðburða](hr-benefits-setup-life-event-types.md)
- [Stofna gerðir áætlana](hr-benefits-setup-plan-types.md)
- [Setja upp ástæðukóða](hr-benefits-setup-reason-codes.md)
- [Setja upp kóða fyrir lög](hr-benefits-setup-tier-codes.md)
- [Grunnstilla taxta](hr-benefits-setup-rates.md)
- [Grunnstilla frádrætti](hr-benefits-setup-deductions.md)
- [Grunnstilla biðdaga](hr-benefits-setup-waiting-days.md)
- [Grunnstilla biðtímabil](hr-benefits-setup-waiting-periods.md)
- [Setja upp sléttunarreglur](hr-benefits-setup-rounding-rules.md)
- [Stofna atvinnuflokka](hr-benefits-setup-employment-categories.md)
- [Setja upp ráðningargerðir](hr-benefits-setup-employment-types.md)
- [Grunnstilla sjálfsafgreiðslu starfsmanns](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Stofna fríðindaáætlanir

Þessar greinar sýna hvernig á að búa til fríðindaáætlun, þar með talið knippi og flex kredit forrit.

- [Uppsetning fríðindaáætlana](hr-benefits-plans-setup.md)
- [Setja upp sveigjanlegar útgjaldaáætlanir](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Vinna úr fríðindaáætlunum

Þú verður að vinna úr nokkrum af breytingunum þínum til að gera þær virkar.

- [Vinna úr fríðindahæfni](hr-benefits-process-enrollment-eligibility.md)
- [Vinna úr viðburðum](hr-benefits-process-life-events.md)
- [Vinna úr breytingum á viðburðum](hr-benefits-process-life-event-changes.md)
- [Vinna úr hæfni viðburðar](hr-benefits-process-life-event-eligibility.md)
- [Vinna úr breytingum á hlutfalli](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]