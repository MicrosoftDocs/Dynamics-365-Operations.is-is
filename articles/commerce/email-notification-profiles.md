---
title: Setja upp forstillingu tilkynningar í tölvupósti
description: Þetta efnisatriði lýsir hvernig á að stofna forstillingu tilkynningar í tölvupósti í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 02/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7a7d796a173a6f9dfcd62e1f73e078cac614145e
ms.sourcegitcommit: 2aca3a95d42403c7f5d80dcd5e3ee958dca5c894
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2022
ms.locfileid: "8087868"
---
# <a name="set-up-an-email-notification-profile"></a>Setja upp forstillingu tilkynningar í tölvupósti

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að stofna forstillingu tilkynningar í tölvupósti í Microsoft Dynamics 365 Commerce.

Þegar rásir eru búnar til er hægt að setja upp forstillingu tilkynningar í tölvupósti. Tilkynningasniðið í tölvupósti skilgreinir atburði sölufærslu (eins og pöntun búin til, pöntun pakkað og pöntun reikningsfærð atburðir) sem þú munt senda tilkynningar til viðskiptavina þinna. 

Frekari upplýsingar um hvernig á að skilgreina tölvupóst er að finna í [Stilling og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Stofna forstillingu tilkynningar í tölvupósti

Fylgdu þessum skrefum til að búa til tilkynningar um tölvupóst.

1. Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.
1. Í aðgerðasvæðinu er smellt á **Nýtt**.
1. Í reitinn **Tilkynning um tölvupóst** slærðu inn heiti til að bera kennsl á forstillinguna.
1. Í reitnum **Lýsing** skal færa inn viðeigandi lýsingu.
1. Stilltu rofann **Virkur** á **Já**.

### <a name="create-an-email-template"></a>Stofna sniðmát fyrir tölvupóst

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

### <a name="create-an-email-event"></a>Stofna tilvik fyrir tölvupóst

Til að stofna tölvupóststilvik, skal fylgja eftirfarandi skrefum.

1. Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir. 
1. Velja tölvupóstssniðmát af fellislistanum **Tölvupóstskenni**.
1. Veldu viðeigandi **Gerð tilkynningar í tölvupósti** af fellilistanum.
1. Velja skal gátreitinn **Virkt** .
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir nokkur dæmi um stillingar tilkynningar tilviks.

![Tilkynningastillingar tilvika.](media/email-notification-profile.png)

> [!NOTE]
> Tilkynningagerðin sem viðskiptavinurinn hefur búið til krefst að sérsniðin sé innleidd áður en hægt er að senda tilkynningu í tölvupósti.

### <a name="next-steps"></a>Næstu skref

Áður en þú getur sent tölvupóst verður þú að stilla póstþjónustu póst á útleið og setja upp runuvinnslu. Nánari upplýsingar er að finna í [Skilgreina og senda tölvupóst](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreining og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Yfirlit rása](channels-overview.md)

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)

[Yfirlit yfir fyrirtæki og fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
