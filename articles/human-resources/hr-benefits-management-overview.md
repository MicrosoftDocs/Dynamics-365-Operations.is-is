---
title: Yfirlit fríðindastjórnunar
description: Yfirlit yfir forskoðunareiginleika stjórnunar fríðinda í Dynamics 365 Human Resources. Bjóddu starfsmönnum þínum framlengda valkosti með auðveldri notkun á netinu.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029464"
---
# <a name="benefits-management-overview"></a>Yfirlit fríðindastjórnunar

[!include [banner](includes/preview-feature.md)]

Til að vera samkeppnishæfur verður þú að bjóða upp á mikið af fríðindum til að laða að og halda bestu starfsmönnum þínum. Til viðbótar við venjulegan ávinning eins og læknisfræðilega og tannlæknaþjónustu, gætirðu líka viljað bjóða upp á stækkaða þjónustu eins og ættleiðingaraðstoð, afþreyingarforrit og fatapeninga. Forskoðunaraðgerð fríðindastjórnunar í Microsoft Dynamics 365 Human Resources veitir þér sveigjanlega lausn sem styður fjölbreytt úrval af kostum. Human Resources felur einnig í sér nothæfa reynslu starfsmanna sem sýnir framboð þitt.

- Auknar fríðindaáætlanir gera þér kleift að búa til og hafa umsjón með einstökum fríðindaáætlunum og styðja flóknar töflur um fríðindahlutfall og ívafin stig. Þú getur auðveldlega búið til fríðindaáætlanir, knippi og sjálfvirkar innritunarreglur til að auðvelda starfsmannaupplifun.

- Flex lánstraust forrit gera þér kleift að styðja við starfslok og aðra atburði í lífinu.

- Víðtækar hæfisreglur tryggja að þú gerir rétt fríðindi tiltæk réttum starfsmönnum.

- Netskráning í fríðindi veitir starfsmönnum þínum auðvelda reynslu.

- Viðurkennd vinnsla atburða á atburði í lífinu fellur saman við sjálfsafgreiðslu starfsmanna og styður einnig framtíðarviðburði.

Ef þú vilt fá aðgang að kynningargögnum þarftu að dreifa sandkassumhverfinu þínu á nýjan leik.

Þú getur veitt bein viðbrögð eða tilkynnt mál til: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Þekkt vandamál í yfirliti fríðindastjórnunar

### <a name="eligibility-processing"></a>Hæfni metin

Þegar þú keyrir á hæfi fyrir bætur sem nota 1-5X laun,% af launum og flatarmagnsupphæð, verður að stilla dagsetningu **Fríðindaupplýsinga** á **upphafsdag starfsmanns** í **Atvinnusaga**, með vinnustundum, greiðslutíðni og ársupphæð launafjárhæðar. Þú verður einnig að taka með **Vinnutíma**, **Greiðslutíðni** og **Ársupphæð launaupphæðar**. Ef starfsmaðurinn hefur fastar bætur, sláðu inn **Vinnutímar** og **Greiðslutíðni**. Árslaun upphæðin mun reikna út. Ef starfsmaðurinn er launaður þarf ekki að slá inn **vinnustundunir**. Við mælum með því að þegar nýir starfsmenn eru stofnaðir séu föst laun færð fyrst inn. Til að uppfæra upplýsingar um fríðindi skal fara á **Starfskraftur > Saga starfsmanna> Upplýsingar um atvinnumál**. Aðlagaðu dagsetninguna að upphafsdegi starfsmannsins.

### <a name="employee-self-service"></a>Sjálfsafgreiðsla starfsmanns

Ekki er verið að reikna fjárhæð starfsmanna við uppfærslu á umfjöllunarfjárhæð líftrygginga. Til dæmis þegar starfsmanni er boðið líftryggingaráætlun geta þeir valið allt að $50.000 í tryggingar á kostnað $ 0,36 á $1.000 af tryggingu.  Þegar starfsmaður uppfærir tryggingarupphæðina er tilheyrandi kostnaður starfsmannsins núll.

Fyrir fríðindaáætlun sem leyfir aðeins eitt úrval af þeirri áætlun fær notandinn villu ef þeir reyna að afsala sér áætlun eftir að hafa valið áætlun. Til dæmis velur notandi læknisáætlun og setur hana í körfuna sína. Notandinn velur síðan **Veita undanþágu** vegna annarrar læknisáætlunar. Notandinn mun fá villu.

## <a name="enable-benefits-management"></a>Virkja fríðindastjórnun

Hagur stjórnun er forsýning lögun, og er aðeins fáanleg í **Sandkassi** umhverfi. Þessar greinar lýsa því hvernig hægt er að kveikja á forskoðunaraðgerðum í Human Resources. Þeir segja einnig frá hvaða eiginleikum sem eru fyrir hendi í starfsmannamálum sem bótastjórnun kemur í stað eða er óvirk þegar þú kveikir á Fríðindastjórnun.

- [Vinna með eiginleika](hr-admin-manage-features.md)
- [Forskoðunareiginleiki: Fríðindastjórnun](hr-admin-manage-features.md?preview-feature-benefits-management)

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
- [Stofna fríðindaáætlanir starfskrafts](hr-benefits-plans-worker.md)
- [Setja upp sveigjanlegar útgjaldaáætlanir](hr-benefits-plans-flex-credit-programs.md)
- [Grunnstilla viðburði í framtíðinni](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Vinna úr fríðindaáætlunum

Þú verður að vinna úr nokkrum af breytingunum þínum til að gera þær virkar.

- [Vinna úr fríðindahæfni](hr-benefits-process-enrollment-eligibility.md)
- [Vinna úr viðburðum](hr-benefits-process-life-events.md)
- [Vinna úr breytingum á viðburðum](hr-benefits-process-life-event-changes.md)
- [Vinna úr hæfni viðburðar](hr-benefits-process-life-event-eligibility.md)
- [Vinna úr breytingum á hlutfalli](hr-benefits-process-rate-changes.md)

