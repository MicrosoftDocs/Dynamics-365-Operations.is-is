---
title: Yfirlit
description: Í Dynamics 365 Human Resources veitir vinnusvæðið Leyfi og fjarvera sveigjanlegan ramma til að stofna nýjar orlofsáætlanir, verkflæði til að stjórna beiðnum og innsæi sjálfsþjónustusíða þar sem starfsmenn geta beðið um frí.
author: andreabichsel
manager: AnnBe
ms.date: 04/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f7ba32b31a67d81ee5be568b0e64842f343f96b
ms.sourcegitcommit: 9940ca772807d3c4e1ff3bf47f45b7251c4469ac
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/04/2020
ms.locfileid: "3226231"
---
# <a name="overview"></a>Yfirlit

Dynamics 365 Human Resources hjálpar þér að veita starfsmönnum þínum mikinn orlof. Vinnusvæðið **Leyfi og fjarvera** býður upp á sveigjanlegan ramma til að búa til ný orlofsáætlun, verkflæði til að stjórna beiðnum og innsæi sjálfsþjónustusíða þar sem starfsmenn geta beðið um frí. Greining hjálpar fyrirtækinu þínu að mæla og fylgjast með orlofshlutfalli og notkun vegna orlofssókna.

## <a name="set-up-leave-and-absence"></a>Setja upp leyfi og fjarvistir

Áður en þú stofnar orlof fyrir starfsmenn þína þarftu að gera nokkur uppsetningarskref:

- [Grunnstilla færibreytur leyfis og fjarvista](hr-leave-and-absence-parameters.md)
- [Búa til dagatal fyrir vinnutíma](hr-leave-and-absence-working-time-calendar.md)
- [Stofna verkflæði fyrir beiðni um leyfi](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Stofnun og umsjón með orlofsáætlunum

Áður en þú býrð til orlofsáætlun fyrir starfsmenn þína þarftu að búa til orlofs- og fjarverutegundir. Eftir að þú hefur búið til orlofssamninga geturðu síðan skráð starfsmenn í áætlunina. Þú getur einnig keyrt uppsöfnunarferlið, búið til viðvaranir og skoðað greiningar fyrir áætlanir þínar.

- [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md)
- [Búa til leyfis- og fjarvistaáætlun](hr-leave-and-absence-plans.md)
- [Úthluta starfsmönnum á leyfisáætlun](hr-leave-and-absence-enroll.md)
- [Uppsöfnunaráætlanir fyrir leyfi og fjarvistir](hr-leave-and-absence-accrue.md)
- [Skoða greiningu á leyfum og fjarvistum](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Biðja um frí og hafa umsjón með beiðnum

Starfsmenn þínir geta sent inn beiðnir um frí og þú getur stjórnað þeim í **Sjálfsafgreiðsla starfsmanna** vinnusvæði.

- [Biðja um frí](hr-employee-self-service-request-time-off.md)
- [Vinna með beiðnir um leyfi og fjarvistir](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Þekkt mál vegna leyfis og fjarvista

### <a name="rounding-precision"></a>Sléttunarnákvæmni

Þú getur ekki stillt **Sléttunarnákvæmni** þegar þú stillir **Gerð sléttunar**. Þú getur aðeins stillt **Sléttunarnákvæmni** með því að nota eininguna **Gerð leyfis og fjarvistar**. 

1. Úr **Gerðir leyfis og fjarvista** velurðu **Opna í Excel** til að opna eininguna **Gerð leyfis og fjarvista**.

2. Þegar skráin hefur opnast og er virkjuð skaltu velja **Hönnun**.

3. Á töflunni **Gerð leyfis og fjarvista** velurðu blýantsvalkostinn til að breyta.

4. Veldu **RoundingPrecision** og **RoundingType** og veldu síðan **Bæta við** til að bæta við lista yfir reiti.

5. Veldu **Uppfæra** og síðan **Lokið**.

6. Sláðu inn eða veldu **Gerð sléttunar** fyrir hverja leyfisgerð ef þær hafa ekki verið stilltar nú þegar. 

7. Sláðu inn **Sléttunarnákvæmni** fyrir viðeigandi gerðir.

8. Veldu **Birta** til að ýta breytingunum yfir í Human Resources.

## <a name="leave-and-absence-preview-features"></a>Forskoðunareiginleikar leyfis og fjarveru

Þú getur prófað nýja forskoðunareiginleika leyfis og fjarveru í **Sandkassi** umhverfi. Upplýsingar um stillingu forútgáfueiginleika er að finna í [Vinna með eiginleika](hr-admin-manage-features.md). Forskoðunareiginleikar eru:

- **Frestun leyfis** - Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann. Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir. Ef frestunin á sér stað eftir að uppsöfnun er unnin skapar frestun leyfis hlutfallslega leiðréttingu á leyfisstöðu starfsmanns. 

- **Yfirfærslureglur** - Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar. Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga. 