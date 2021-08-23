---
title: Úthluta Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði útskýrir hvernig á að setja upp að aðgang Microsoft Dynamics 365 Commerce matsumhverfi.
author: psimolin
ms.date: 12/17/2020
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
ms.openlocfilehash: c8241c31e82d124398189666c3a1709d25884b8acd9c8f3b1068529cbd216684
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777501"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Úthluta Dynamics 365 Commerce matsumhverfi

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp að aðgang Microsoft Dynamics 365 Commerce matsumhverfi.

Áður en þú byrjar, mælum við með að þú gríptir skjótt í gegnum þetta efni til að fá hugmynd um hvað ferlið krefst.

> [!NOTE]
> Commerce matsumhverfi er almennt ekki í boði og er veitt af samstarfsaðilum og viðskiptavinum á grundvelli beiðna. Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð ef þig vantar frekari upplýsingar.

Til að hægt sé að úthluta Commerce-matsumhverfi þarf að stofna verk sem er með ákveðið afurðarheiti og gerð. Umhverfið og Commerce Scale Unit (CSU) eru einnig með nokkrar ákveðnar færibreytur sem verður að nota þegar áætlun rafræna viðskipta er úthlutað. Leiðbeiningarnar í þessu efnisatriði lýsa öllum skrefunum sem eru nauðsynleg til að ljúka úthlutun og færibreyturnar sem þarf að nota.

Þegar búið er að úthluta Commerce-matsumhverfinu þarf að ljúka nokkrum skrefum eftir úthlutun til að gera það tilbúið fyrir notkun. Sum skref eru valkvæð, eftir þeim þáttum kerfisins þú vilt meta. Þú getur alltaf klárað valfrjálsu skrefin seinna.

Frekari upplýsingar um hvernig á að grunnstilla Commerce-matsumhverfið þegar búið er að úthluta því er að finna í [Grunnstilla Commerce-matsumhverfi](cpe-post-provisioning.md). Frekari upplýsingar um hvernig á að grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið er að finna í [Grunnstilla valfrjálsa eiginleika fyrir Commerce-matsumhverfið](cpe-optional-features.md).

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi skilyrði verða að vera til staðar áður en hægt er að úthluta matsumhverfi í Commerce:

- Þú hefur fengið aðgang að matsforritinu og fengið úthlutað afkastagetu fyrir matsumhverfi.
- Þú hefur aðgang að Microsoft Dynamics Lifecycle Services (LCS)-gáttinni.
- Þú ert fyrirliggjandi félagi eða viðskiptavinur Microsoft Dynamics 365 og getur stofnað Dynamics 365 Commerce verk.
- Þú ert með stjórnandaaðgang að Microsoft Azure-áskriftinni eða þú ert í samskiptum við umsjónaraðila áskriftar sem getur aðstoðað þig ef þörf krefur.
- Þú hefur leigjandakenni þitt fyrir Azure Active Directory (Azure AD) í boði.
- Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem kerfisstjórahóp netverslunar og þú ert með kenni hans tiltækt.
- Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem stjórnandahóp einkunna og umsagna og þú ert með kenni hans tiltækt. (Þessi öryggishópur getur verið sá sami og kerfisstjórinn fyrir netkerfi.)

Athugið að þessi listi er ekki tæmandi. Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð ef vandamál koma upp.

## <a name="provision-your-commerce-evaluation-environment"></a>Skilgreina Commerce matsumhverfi

Þessar verklagsreglur útskýra hvernig á að úthluta Commerce-matsumhverfi. Þegar búið er að ljúka þeim verður Commerce-matsumhverfið tilbúið fyrir grunnstillingu. Allar þær aðgerðir sem er lýst hér fara fram í LCS-gáttinni.

### <a name="create-a-new-project"></a>Stofna nýtt verk

Til að stofna nýtt verk í LSC skal fylgja þessum skrefum.

1. Á heimasíðu LCS velurðu plúsmerkið (**+**) til að búa til verk.
1. Fylgdu einu af þessum skrefum á hægri glugganum:

    - Ef þú ert félagi skaltu velja **Flytja, búa til lausnir og læra**.
    - Ef þú ert viðskiptavinur skaltu velja **Væntanleg forsala**.

1. Færðu inn heiti, lýsingu og iðnað.
1. Í reitnum **Heiti afurðar** velurðu **Dynamics 365 Commerce**.
1. Í reitnum **Útgáfa afurðar** velurðu **Dynamics 365 Commerce**.
1. Í reitnum **Aðferð** velurðu **Dynamics Retail útfærsluaðferð**.
1. Valfrjálst: Hægt er að flytja inn hlutverk og notendur úr fyrirliggjandi verki.
1. Velja **Stofna**. Verksýnin birtist.

### <a name="add-the-azure-connector"></a>Bættu Azure-tengingunni við

Til að bæta Azure-tengingunni við LCS-verk skal fylgja skrefunum í [Ljúka innleiðingarferli Azure Resource Manager](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).

### <a name="deploy-the-environment"></a>Virkjaðu umhverfið

Til að virkja umhverfið skaltu fylgja þessum skrefum.

> [!NOTE]
> Þú gætir ekki þurft að klára skref 6, 7 og / eða 8 því að síðum sem hafa einn valkost er sleppt. Þegar þú ert í sýninni **Færibreytur umhverfis** skaltu staðfesta að textinn **Dynamics 365 Commerce - (Forskoðun) - Kynning (10.0.* x* með verkvangsuppfærslu *xx*)** birtist beint fyrir ofan reitinn **Heiti umhverfis**. Fyrir nánari upplýsingar, sjá myndina sem birtist eftir 8. skref.

1. Í efstu valmyndinni velurðu **Umhverfi í skýi**.
1. Veldu **Bæta við** til að bæta við umhverfi.
1. Í reitnum **Útgáfa forrits**, veldu nýjustu útgáfuna. Ef þú hefur sérstaka þörf fyrir að velja aðra forritsútgáfu en nýjustu útgáfuna skaltu ekki velja útgáfu áður **10.0.14**.
1. Í reitnum **Útgáfa verkvangs**, notarðu verkvangsútgáfuna sem er sjálfkrafa valin fyrir forritsútgáfuna sem þú valdir. 

    ![Val á forrita- og verkvangsútgáfum.](./media/project1.png)

1. Veljið **Næst**.
1. Veldu **Kynning** grannfræði umhverfis.

    ![Val á grannfræði umhverfis 1.](./media/project2.png)

1. Á síðunni **Setja upp umhverfi** slærðu inn umhverfisheiti. Hafðu ítarlegar stillingar óbreyttar.

    ![Setja upp umhverfissíðu.](./media/project4.png)

1. Stilltu VM stærð eftir þörfum. (Við mælum með VM birgðaeiningunni \[SKU\] **D13 v2**.)
1. Skoðaðu verðlagningu og leyfisskilmála og veldu síðan gátreitinn til að gefa til kynna að þú samþykki þá.
1. Veljið **Næst**.
1. Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Setja upp**. Þú munt fara aftur í gluggann **Umhverfi í skýi** og umhverfi þitt ætti að birtast á listanum.

    Umbeðið umhverfi þitt birtist í biðröð og síðan er það notað. Það tekur nokkurn tíma að klára vinnuflæði umhverfisins. Athugaðu því aftur eftir um það bil sex til níu tíma.

1. Áður en lengra er haldið skaltu ganga úr skugga um að staða umhverfisins sé **Uppsett**.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Frumstilla Commerce Scale Unit (ský)

Fylgið þessum skrefum til að ræsa CSU.

1. Í glugganum **Umhverfi í skýi** velurðu umhverfi þitt af listanum.
1. Í umhverfissýninni til hægri skaltu velja **Nánari upplýsingar**. Umhverfisupplýsingaskjárinn birtist.
1. Undir **Eiginleikar umhverfis** velurðu **Stjórna**.
1. Á flipanum **Commerce** velurðu **Frumstilla**. Skjár CSU frumstillingarifæribreyta birtist.
1. Í reitnum **Svæði** skal velja svæðið sem er það sama eða nálægt því svæði umhverfið er notað í.
1. Skildu reitinn **Útgáfa** eftir eins og hann er.
1. Veldu **Frumstilla**.
1. Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Já**. Skjárinn **Commerce-stjórnun** birtist aftur, þar sem flipinn **Commerce** er valinn. CSU þinn hefur verið í biðröð vegna úthlutunar.
1. Áður en lengra er haldið skaltu ganga úr skugga um að staða CSU sé **Tókst**. Frumstilling tekur um það bil tvær til fimm klukkustundir.

Ef þú finnur ekki tengilinn **Stjórna** í upplýsingayfirliti umhverfis skal hafa samband við tengiliðann hjá Microsoft til að fá aðstoð.

Þú gætir fengið eftirfarandi villuboð við uppsetningarferlið:

> Mat (prufu-/prófunarumhverfi) þarf að skrá inn tengiforrit \<application ID\> í höfuðstöðvum.

Ef ræsing CSU mistekst og þessi villuboð birtast skal skrá forritskennið, altækt einkvæmt kennimerki (GUID), og fylgja svo skrefunum í næsta hluta til að skrá CSU-uppsetningarforrit í Commerce Headquarters.

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a>Skrá CSU-uppsetningarforrit í Commerce Headquarters (ef þess er krafist)

Til að skrá CSU-uppsetningarforritið í Commerce Headquarters skal fylgja þessum skrefum.

1. Í Commerce Headquarters skal opna **Kerfisstjórnun \> Uppsetning \> Azure Active Directory forrita**.
1. Í **Kenni biðlara** dálkinum skal slá inn kenni forrits úr villuboðum í CSU-frumstillingarboðum sem voru móttekin.
1. Í dálknum **Heiti** skal færa inn lýsandi texta (til dæmis **CSU-viðtæki**).
1. Í dálkinn **Notandakenni** skal slá inn **RetailServiceAccount**.
1. Reynið aftur ræsingu á CSU og uppsetningu úr LCS.

### <a name="initialize-e-commerce"></a>Frumstilla rafræn viðskipti

Fylgið eftirfarandi skrefum til að frumstilla e-Commerce.

1. Í flipanum **e-Commerce** skal fara yfir matssamþykki og velja svo **Uppsetning**.
1. Í reitinn **Heiti e-Commerce-umhverfis** skal færa inn heiti. Hafa skal í huga að þetta heiti mun birtast á sumum vefslóðum sem benda á tilvik þitt af rafrænum viðskiptum.
1. Í reitnum **Heiti Commerce Scale Unit** skal velja CSU í listanum. (Listinn ætti aðeins að hafa einn valkost.)

    Reiturinn **Svæði rafrænna viðskipta** er stillt sjálfkrafa.

1. Veldu **Næst** til að halda áfram.
1. Í reitnum **Studd hýsilheiti** slærðu inn gilt lén, eins og `www.fabrikam.com`.
1. Í reitinn **AAD-öryggisflokkur fyrir kerfisstjóra** skal færa inn fyrstu stafina í heiti öryggisflokksins sem á að nota og síðan velja stækkunarglerið til að skoða leitarniðurstöðurnar. Veljið réttan öryggisflokk í listanum.
1.  Í reitinn **AAD-öryggisflokkur fyrir ritstjóra einkunna og umsagna** skal færa inn fyrstu stafina í heiti öryggisflokksins sem á að nota og síðan velja stækkunarglerið til að skoða leitarniðurstöðurnar. Veljið réttan öryggisflokk í listanum.
1. Haldið valkostinum **Virkja þjónustu einkunna og umsagna** á **Já**.
1. Veldu **Frumstilla**. Skjárinn **Commerce-stjórnun** birtist aftur, þar sem flipinn **e-Commerce** er valinn. Frumstilling rafrænna viðskipta er hafin.
1. Áður en lengra er haldið skaltu bíða þar til staða frumstillingar í netverslun er **Frumstilling tókst**.
1. Undir **Krækjur** neðst til hægri, skrifaðu vefslóðirnar fyrir eftirfarandi tengla:

    * **rafræn viðskipti síða** - Hlekkurinn á rótina á netverslunarsíðunni þinni.
    * **Commerce-vefssmiður** - Tengillinn á verkfæri svæðisstjórnunar.

## <a name="next-steps"></a>Næstu skref

Til að halda áfram að úthluta og grunnstilla Commerce-matsumhverfið skal skoða [Grunnstilla Commerce-matsumhverfi](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi](cpe-overview.md)

[Stilla Dynamics 365 Commerce matsumhverfi](cpe-post-provisioning.md)

[Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi](cpe-bopis.md)

[Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi](cpe-optional-features.md)

[algengar spurningar um Dynamics 365 Commerce matsumhverfi](cpe-faq.md)

[Microsoft Dynamics Lifecycle Services (LSC)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (ský)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]