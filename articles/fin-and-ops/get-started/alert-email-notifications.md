---
title: Viðvörunartilkynning biðlara með tölvupósti
description: Þetta efnisatriði veitir upplýsingar um hvernig á að setja upp reglur sem senda tilkynningar í tölvupósti þegar fyrirfram skilgreindir viðburðir eiga sér stað.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2019
ms.locfileid: "373784"
---
# <a name="client-alert-notifications-by-email"></a>Viðvörunartilkynning biðlara með tölvupósti

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Í Microsoft Dynamics 365 for Finance and Operations er hægt að skilgreina sérsniðar viðvörunarreglur sem fylgjast með síuðum yfirlitum á gögnum og senda sjálfkrafa tilkynningar í tölvupósti þegar fyrirfram skilgreindir viðburðir gerast. Möguleikinn til að senda tilkynningar í tölvupósti er tiltækur fyrir allar studdar gerðir viðvörunar og einnig er hægt að kveikja á honum fyrir núverandi viðvörunarreglur.

Hægt er að nota innbyggðar stýringar til að búa til viðvörunarreglur sem fylgjast með síuðum yfirlitum á runuvinnslum kerfis. Með því að fylgjast með svæðinu **Staða** er einnig hægt að skilgreina viðvörunarreglur sem senda tölvupóst þegar runuvinnsla mistekst. Eftir að þessar viðvörunarreglur eru búnar til þarf ekki lengur að athuga skýrslur út af breytingum á viðskiptagögnum. Í staðinn er hægt að láta snjallþjónustu breytingagreininga Finance and Operations fylgjast með.

Viðvaranir biðlara eru háðar undirkerfi tölvupósts sem er veitt í gegnum samþættingu við Microsoft Office. Við mælum með því að þú notir veituna fyrir SMTP-samskiptaregluna, þannig að dreifing á tölvupósti þarf ekki að treysta á staðbundinn póstþjón.

Til að senda tilkynningar með tölvupósti verða viðskiptavinir að skilgreina samþættar tölvupóstsþjónustur. Tilkynningar í tölvupósti eru sendar viðtakendum af hálfu eigenda tilkynningar.

Frekari upplýsingar um hvernig á að skilgrein tölvupóst í Finance and Operations er að finna í [Stilling og sending tölvupósts](../organization-administration/configure-email.md).

Eftirfarandi mynd sýnir svargluggann **Stofna viðvörunarreglu** sem er nú með valkostinn **Senda tölvupóst**.

[![Stofna svarglugga viðvörunarreglu þar sem valkosturinn „Senda tölvupóst“ er stilltur á Já](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Þegar valkosturinn **Senda tölvupóst** er stilltur á **Já** verður haldið áfram að senda viðvörunartilkynningar úr Aðgerðamiðstöðinni.

## <a name="alert-notification-email-templates"></a>Sniðmát fyrir viðvörunartilkynningar í tölvupósti

Þjónustan sendir tilkynningar í tölvupósti með því að nota fyrirfram skilgreind sniðmát tölvupósts sem afhenda grunnupplýsingar um viðvörunartilkynninguna. Þessar upplýsingar innihalda beinan tengil á síðuna þar sem viðvörunarreglan var skilgreind.

Eftirfarandi mynd sýnir uppbyggingu á viðvörunartilkynningum þegar þær eru mótteknar með tölvupósti.

[![Viðvörunartilkynningar sem byggjast á sniðmáti fyrir stofnun á færslu, breytingar á svæði og eyðingu á sniðmáti](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)