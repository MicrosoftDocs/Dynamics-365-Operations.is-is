---
title: Setja upp forstillingu tilkynningar í tölvupósti
description: Þetta efnisatriði lýsir hvernig á að stofna forstillingu tilkynningar í tölvupósti í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/01/2021
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
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792658"
---
# <a name="set-up-an-email-notification-profile"></a>Setja upp forstillingu tilkynningar í tölvupósti

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að stofna forstillingu tilkynningar í tölvupósti í Microsoft Dynamics 365 Commerce.

Þegar rásir eru búnar til er hægt að setja upp forstillingu tilkynningar í tölvupósti. Á þann hátt er hægt að senda viðskiptavinum tölvupósta vegna ýmissa færslutilvika á borð við stofnun pöntunar, sendingarstöðu pöntunar og greiðsluvillu.

Frekari upplýsingar um hvernig á að skilgreina tölvupóst er að finna í [Stilling og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Stofna forstillingu tilkynningar í tölvupósti

Fylgdu þessum skrefum til að búa til tilkynningar um tölvupóst.

1. Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.
1. Í aðgerðasvæðinu er smellt á **Nýtt**.
1. Í reitinn **Tilkynning um tölvupóst** slærðu inn heiti til að bera kennsl á forstillinguna.
1. Í reitnum **Lýsing** skal færa inn viðeigandi lýsingu.
1. Stilltu rofann **Virkur** á **Já**.

### <a name="create-an-email-template"></a>Stofna sniðmát fyrir tölvupóst

Áður en hægt er að virkja gerð tölvupóststilkynningar þarf að stofna tölvupóstssniðmát fyrirtækis í Commerce Headquarters. Þetta sniðmát skilgreinir viðfangsefni tölvupóstsins, sjálfgefið tungumál hans og meginmál fyrir öll tungumálin sem á að styðja við.

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

![Stillingar fyrir sniðmát tölvupósts](media/email-template.png)

### <a name="create-an-email-event"></a>Stofna tilvik fyrir tölvupóst

Til að stofna tölvupóststilvik, skal fylgja eftirfarandi skrefum.

1. Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir. 
1. Velja tölvupóstssniðmát af fellislistanum **Tölvupóstskenni**.
1. Veldu viðeigandi **Gerð tilkynningar í tölvupósti** af fellilistanum.
1. Velja skal gátreitinn **Virkt** .
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir nokkur dæmi um stillingar tilkynningar tilviks.

![Tilkynningastillingar tilvika](media/email-notification-profile.png)

### <a name="next-steps"></a>Næstu skref

Áður en þú getur sent tölvupóst verður þú að stilla póstþjónustu póst á útleið og setja upp runuvinnslu. Nánari upplýsingar er að finna í [Skilgreina og senda tölvupóst](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).


## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreining og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Yfirlit rása](channels-overview.md)

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)

[Yfirlit yfir fyrirtæki og fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
