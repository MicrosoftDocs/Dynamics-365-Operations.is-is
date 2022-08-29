---
title: Setja upp forstillingu tilkynningar í tölvupósti
description: Þessi grein lýsir því hvernig á að búa til tilkynningaprófíl í tölvupósti í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292136"
---
# <a name="set-up-an-email-notification-profile"></a>Setja upp forstillingu tilkynningar í tölvupósti

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til tilkynningaprófíl í tölvupósti í Microsoft Dynamics 365 Commerce.

Þegar rásir eru búnar til er hægt að setja upp forstillingu tilkynningar í tölvupósti. Tilkynningasniðið í tölvupósti skilgreinir atburði sölufærslu (eins og pöntun búin til, pöntun pakkað og pöntun reikningsfærð atburðir) sem þú munt senda tilkynningar um til viðskiptavina þinna. 

Frekari upplýsingar um hvernig á að skilgreina tölvupóst er að finna í [Stilling og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).



## <a name="create-an-email-template"></a>Stofna sniðmát fyrir tölvupóst

Áður en hægt er að virkja tegund tölvupósttilkynninga verður þú að búa til tölvupóstsniðmát fyrir fyrirtæki í höfuðstöðvum Commerce fyrir hverja tegund tilkynninga sem þú vilt styðja. Þetta sniðmát skilgreinir efni tölvupósts, sendanda, sjálfgefið tungumál og meginmál tölvupósts fyrir hvert studd tungumál.

Til að stofna tölvupóstsniðmát, skal fylgja eftirfarandi skrefum.

1. Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitinn **Kenni tölvupósts** slærðu inn kenni til að auðkenna þetta sniðmát.
1. Í reitnum **Nafn sendanda** skal færa inn heiti sendanda.
1. Í reitnum **Lýsing tölvupósts** skal færa inn auðskiljanlega lýsingu.
1. Í **Netfang sendanda** slærðu inn netfang sendanda.
1. Í hlutanum **Almennt** skal velja sjálfgefið tungumál fyrir sniðmát tölvupóstsins. Sjálfgefið tungumál verður notað þegar ekkert staðbundið sniðmát er til fyrir tilgreint tungumál.
1. Stækkaðu hlutann **Efni tölvupóstskilaboða** og veldu **Nýtt** til að búa til sniðmátsinnihald. Veldu tungumál fyrir hvern efnislið og gefðu upp efnislínu tölvupóstsins. Ef tölvupósturinn verður með meginmál skal passa að hakað sé í reitinn **Hefur meginmál**.
1. Í aðgerðaglugganum velurðu **Tölvupóstskeyti** til að gefa upp meginmálssnið tölvupósts.

Eftirfarandi mynd sýnir nokkur dæmi um sniðmátsstillingar tölvupósts.

![Stillingar fyrir sniðmát tölvupósts.](media/email-template.png)

Fyrir frekari upplýsingar um að búa til tölvupóstsniðmát, sjá [Búðu til tölvupóstsniðmát fyrir viðskiptaviðburði](email-templates-transactions.md). 

## <a name="create-an-email-notification-profile"></a>Stofna forstillingu tilkynningar í tölvupósti

Til að búa til tilkynningaprófíl í tölvupósti í höfuðstöðvum skaltu fylgja þessum skrefum.

1. Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitinn **Tilkynning um tölvupóst** slærðu inn heiti til að bera kennsl á forstillinguna.
1. Í reitnum **Lýsing** skal færa inn viðeigandi lýsingu.
1. Stilltu rofann **Virkur** á **Já**.

## <a name="add-a-notification-type"></a>Bættu við tegund tilkynninga

Til að stofna tölvupóststilvik, skal fylgja eftirfarandi skrefum.

1. Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.
1. Undir **Stillingar fyrir tölvupósttilkynningar í smásölu**, veldu **Nýtt**.
1. Veldu viðeigandi **Gerð tilkynningar í tölvupósti** af fellilistanum.
1. Veldu tölvupóstsniðmátið sem þú bjóst til hér að ofan úr **Netfang** fellilistanum.
1. Veldu **Virkur** gátreit.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir nokkur dæmi um stillingar tilkynningar tilviks.

![Tilkynningastillingar tilvika.](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>Tímasettu endurtekið tilkynningaferli í tölvupósti

Til að senda út tölvupósttilkynningar verður þú að hafa **Vinnsla smásölupöntunar í tölvupósti** starf í gangi.

Til að setja upp runuvinnu í höfuðstöðvum til að senda viðskiptatölvupóst skaltu fylgja þessum skrefum.

1. Fara til **Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Tölvupóstur og tilkynningar \> Sendu tilkynningu í tölvupósti**.
1. Í **Vinnsla smásölupöntunar í tölvupósti** valmynd, veldu **Endurkoma**.
1. Í **Skilgreindu endurtekningu** valmynd, veldu **Engin lokadagsetning**.
1. Undir **Endurtekningarmynstur**, veldu **Fundargerð**, og stilltu síðan **Telja** sviði til **1**. Þessar stillingar munu tryggja að tölvupósttilkynningar séu unnar eins fljótt og auðið er.
1. Veldu **Allt í lagi** að fara aftur til **Vinnsla smásölupöntunar í tölvupósti** valmynd.
1. Veldu **Allt í lagi** til að ljúka uppsetningu verksins.

## <a name="next-steps"></a>Næstu skref

Áður en hægt er að senda tölvupóst verður þú að stilla útsendan póstþjónustu. Nánari upplýsingar er að finna í [Skilgreina og senda tölvupóst](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreining og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Yfirlit rása](channels-overview.md)

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)

[Yfirlit yfir fyrirtæki og fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
