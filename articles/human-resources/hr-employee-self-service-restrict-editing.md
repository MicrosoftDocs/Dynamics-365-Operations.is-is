---
title: Takmörkun á breytingu persónuupplýsinga
description: Takmarka getu starfsmanna til að breyta tengiliðaupplýsingum í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e10db35996d31dc6c40a4253a324139c346be8c9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070753"
---
# <a name="restrict-editing-of-personal-information"></a>Takmörkun á breytingu persónuupplýsinga


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Þetta efnisatriði lýsir því hvernig á að takmarka getu starfsmanna til að breyta tengiliðaupplýsingum í Dynamics 365 Human Resources. Þú gætir viljað koma í veg fyrir að starfsmenn geti breytt ákvenum samskiptaupplýsingum á borð við staðsetningu fyrirtækis þeirra eða netfang.

> [!NOTE]
> Til að nota þennan möguleika þarf fyrist að virkja **(Forskoðun) Takmarka möguleika starfsmanna á að bæta við eða breyta aðsetri og tengiliðaupplýsingum í völdum tilgangi.** í eiginleikastjórnun. Frekari upplýsingar um hvernig forskoðunareiginleikar eru virkjaðir er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).<br><br>![Virkja forskoðunareiginleika.](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Velja upplýsingarnar sem starfsmaður getur bætt við eða breytt

1. Í mannauði, veljið **Starfsmannastjórnun**, veljið **Tenglar** og veljið svo **Færibreytur mannauðs**.

   ![Opna færibreytur Human Resources.](./media/hr-employee-self-service-human-resources-parameters.png)

2. Á síðunni **Færibreytur mannauðs** skal velja flipann **Sjálfsafgreiðsla starfsmanns**.

   ![Veljið Sjálfsafgreiðsla starfsmanna.](./media/hr-employee-self-service-tab.png)

3. Í flipanum **Sjálfsafgreiðsla starfsmanna** skal afhaka allar upplýsingar í hlutanum **Aðseturs og tengiliðaupplýsingar** sem starfsmenn eiga ekki að fá að bæta við eða breyta. Í þessu dæmi höfum við ekki afhakað tengiliðaupplýsingarnar **Fyrirtæki**.

   ![Takmarka breytingar á tengiliðaupplýsingum fyrirtækis.](./media/hr-employee-self-service-restrict-business.png)

4. Veldu **Vista**.

   ![Vista breytingar.](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Reynsla starfsmanns

Þegar búið er að takmarka starfsmenn frá því að bæta við eða breyta tengiliðaupplýsingum geta þeir séð upplýsingar en ekki breytt þeim.

Í þessu dæmi, þar sem starfsmönnum er meinað að breyta tengiliðaupplýsingunum **Fyrirtæki**, geta þeir samt séð upplýsingarnar í **Sjálfsafgreiðslu starfsmanna**:

![Skoða upplýsingar tengiliðar.](./media/hr-employee-self-service-restrict-view.png)

Hins vegar, þegar þeir velja tengiliðaupplýsingar fyrirtækisins, birtist svæðið **Breyta aðsetri** sem skrifvarið og þeir geta ekki breytt neinum reitanna.

![Upplýsingar um viðskiptatengiliði birtast skrifvarðir.](./media/hr-employee-self-service-restrict-read-only.png)

Þar að auki, ef þeir velja **Bæta við** til að bæta við nýju aðsetri, geta þeir ekki valið **Fyrirtæki** úr felliglugganum **Tilgangur**.

![Starfsmaður getur ekki bætt við heimilisfangi fyrirtækis.](./media/hr-employee-self-service-restrict-add.png)

Starfsmenn fá sömu upplifun þegar þeir velja **Tengiliðaupplýsingar** á síðunni **Persónulegar upplýsingar** og bæta við nýju aðsetri. Felliglugginn **Tilgangur** sýnir aðeins hvers konar upplýsingum hægt er að bæta við. 

![Starfsmaður getur ekki valið fyrirtæki í felliglugga fyrir tilgang.](./media/hr-employee-self-service-restrict-purpose.png)

**Tengiliðaupplýsingar** sýna nú **Tilgang** í hnitanetinu.

![Tilgangur birtist í hnitaneti tengiliðaupplýsinga.](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Sjá einnig

[Yfirlit yfir sjálfsafgreiðslu starfsmanns og stjórnanda](hr-employee-manager-self-service-overview.md)<br>
[Grunnstilla færibreytur Human Resources](hr-setup-parameters.md)<br>
[Breyta persónuupplýsingum](hr-employee-manager-self-service-edit-personal-information.md)
