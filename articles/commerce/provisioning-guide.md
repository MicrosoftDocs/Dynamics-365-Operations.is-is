---
title: Ákvæði a Dynamics 365 Commerce sandkassa umhverfi
description: Þessi grein útskýrir hvernig á að kveða á um a Microsoft Dynamics 365 Commerce sandkassaumhverfi fyrir kynningu eða sandkassanotkun með innbyggðum kynningargögnum.
author: psimolin
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3ada30fc9d86d236b71d018ef77f2ae8573f2285
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013135"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Ákvæði a Dynamics 365 Commerce sandkassa umhverfi

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að kveða á um a Microsoft Dynamics 365 Commerce sandkassaumhverfi fyrir kynningarnotkun með innbyggðum kynningargögnum. Ferlið við að setja upp framleiðsluumhverfi er svipað en flóknara þar sem margar af forsendum sandkassaumhverfisins eru þegar gefnar upp í kynningargögnunum.

Áður en þú byrjar mælum við með því að þú skoðir þessa grein fljótlega til að fá hugmynd um hvað ferlið krefst.

Til að útvega Commerce sandkassaumhverfi með góðum árangri verður þú að tilgreina nokkrar færibreytur fyrir umhverfið og Commerce Scale Unit (CSU) sem verður notað þegar þú útvegar Commerce síðar. Leiðbeiningarnar í þessari grein lýsa öllum skrefum sem þarf til að ljúka úthlutun og færibreytum sem þú verður að nota.

Eftir að þú hefur útvegað viðskiptaumhverfið þitt verður þú að ljúka nokkrum skrefum eftir úthlutun til að undirbúa það fyrir notkun. Sum skref eru valfrjáls, allt eftir þeim þáttum kerfisins sem þú vilt nota. Þú getur alltaf klárað valfrjálsu skrefin seinna.

Fyrir upplýsingar um hvernig á að stilla viðskiptaumhverfið þitt eftir að þú útvegar það, sjá [Stilltu Commerce sandkassaumhverfi](cpe-post-provisioning.md). Fyrir upplýsingar um hvernig á að stilla valfrjálsa eiginleika fyrir viðskiptaumhverfið þitt, sjá [Stilltu valfrjálsa eiginleika fyrir Commerce sandkassaumhverfi](cpe-optional-features.md).

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi forsendur verða að vera til staðar áður en þú getur útvegað viðskiptaumhverfið þitt:

- Þú hefur aðgang að Microsoft Dynamics Lifecycle Services (LCS)-gáttinni.
- Þú ert núverandi Microsoft Dynamics 365 samstarfsaðila eða viðskiptavinur og hafa innleiðingarverkefni þegar búið til og hægt að nota í LCS.  
- Þú hefur búið til Azure Active Directory (Azure AD) öryggishópur sem hægt er að nota sem viðskiptakerfisstjórahóp og þú hefur auðkenni hans tiltækt.
- Þú hefur búið til Azure AD öryggishópur sem hægt er að nota sem stjórnendahóp fyrir einkunnir og umsagnir og þú hefur auðkenni hans tiltækt. (Þessi öryggishópur getur verið sá sami og Commerce kerfisstjórahópurinn.)
- Þú hefur sett upp höfuðstöðvartilvik innan LCS. Fyrir frekari upplýsingar, sjá [Settu upp nýtt umhverfi](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Athugið að þessi listi er ekki tæmandi. Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð ef vandamál koma upp.

## <a name="provision-your-commerce-environment"></a>Útvegaðu viðskiptaumhverfið þitt

Eftirfarandi aðferðir útskýra hvernig á að útvega viðskiptaumhverfi. Eftir að þú hefur lokið þessum skrefum verður viðskiptaumhverfið þitt tilbúið til uppsetningar. Öll skrefin sem lýst er hér að neðan fara fram í LCS gáttinni.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Frumstilla Commerce Scale Unit (ský)

Fylgið þessum skrefum til að ræsa CSU.

1. Í LCS skaltu velja umhverfi þitt af listanum.
1. Í **UMHVERFI** skoða til hægri, veldu **Allar upplýsingar**. Umhverfisupplýsingaskjárinn birtist.
1. Í **Stjórna umhverfi** kafla undir **UMHVERFISEIGINLEIKAR**, veldu **Stjórna**.
1. Á **Commerce Scale Units** flipa, veldu **Frumstilla**. The **Bættu við mælieiningu** útsýni birtist.
1. Í **SVÆÐI** reit, veldu svæðið sem er það sama eða nálægt svæðinu sem þú sendir umhverfið á.
1. Í **Útgáfa** fellilistanum, veldu nýjustu útgáfuna sem til er.
1. Veldu **Frumstilla**.
1. Í viðvörunarglugganum sem biður þig um að staðfesta frumstillingu Commerce Scale Unit skaltu velja **Já**. CSU hefur nú verið í biðröð fyrir úthlutun.
1. Áður en þú heldur áfram skaltu ganga úr skugga um að staða CSU þíns sé **ÁRANGUR**. Frumstilling tekur um það bil tvær til fimm klukkustundir.

Ef þú finnur ekki tengilinn **Stjórna** í upplýsingayfirliti umhverfis skal hafa samband við tengiliðann hjá Microsoft til að fá aðstoð.

### <a name="initialize-e-commerce"></a>Frumstilla rafræn viðskipti

Fylgdu þessum skrefum til að frumstilla Commerce.

1. Á flipanum **rafræn viðskipti**, veldu **Uppsetning**.
1. Í reitinn **Heiti e-Commerce-umhverfis** skal færa inn heiti. Hafa skal í huga að þetta heiti mun birtast á sumum vefslóðum sem benda á tilvik þitt af rafrænum viðskiptum.
1. Í reitnum **Heiti Commerce Scale Unit** skal velja CSU í listanum. (Listinn ætti aðeins að hafa einn valkost.)

    Reiturinn **Svæði rafrænna viðskipta** er stillt sjálfkrafa.

1. Veldu **Næst** til að halda áfram.
1. Í reitnum **Studd hýsilheiti** slærðu inn gilt lén, eins og `www.fabrikam.com`.
1. Í reitinn **AAD-öryggisflokkur fyrir kerfisstjóra** skal færa inn fyrstu stafina í heiti öryggisflokksins sem á að nota og síðan velja stækkunarglerið til að skoða leitarniðurstöðurnar. Veljið réttan öryggisflokk í listanum.
1.  Í reitinn **AAD-öryggisflokkur fyrir ritstjóra einkunna og umsagna** skal færa inn fyrstu stafina í heiti öryggisflokksins sem á að nota og síðan velja stækkunarglerið til að skoða leitarniðurstöðurnar. Veljið réttan öryggisflokk í listanum.
1. Haldið valkostinum **Virkja þjónustu einkunna og umsagna** á **Já**.
1. Veldu **Frumstilla**. Skjárinn **Commerce-stjórnun** birtist aftur, þar sem flipinn **e-Commerce** er valinn. Frumstilling rafrænna viðskipta er hafin.
1. Áður en þú heldur áfram skaltu bíða þar til staða Commerce frumstillingar er **FRÁHÆFING TEKST**.
1. Undir **Krækjur** neðst til hægri, skrifaðu vefslóðirnar fyrir eftirfarandi tengla:

    * **rafræn viðskipti síða** - Hlekkurinn á rótina á netverslunarsíðunni þinni.
    * **Commerce-vefssmiður** - Tengillinn á verkfæri svæðisstjórnunar.

## <a name="next-steps"></a>Næstu skref

Til að halda áfram ferlinu við að útvega og stilla viðskiptaumhverfið þitt, sjá [Stilltu Commerce sandkassaumhverfi](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Stilla a Dynamics 365 Commerce sandkassa umhverfi](cpe-post-provisioning.md)

[Stilltu BOPIS í a Dynamics 365 Commerce sandkassa umhverfi](cpe-bopis.md)

[Stilltu valfrjálsa eiginleika fyrir a Dynamics 365 Commerce sandkassa umhverfi](cpe-optional-features.md)

[Microsoft Dynamics Lifecycle Services (LSC)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (ský)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
