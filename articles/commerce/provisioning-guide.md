---
title: Úthluta forskoðunarumhverfi fyrir Dynamics 365 Commerce
description: Þetta efni útskýrir hvernig á að úthluta forskoðunarumhverfi Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426466"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>Úthluta forskoðunarumhverfi fyrir Dynamics 365 Commerce


[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að úthluta forskoðunarumhverfi Dynamics 365 Commerce.

Áður en þú byrjar, mælum við með að þú gríptir skjótt í gegnum þetta efni til að fá hugmynd um hvað ferlið krefst.

> [!NOTE]
> Ef þér hefur ekki verið veittur aðgangur að forskoðun Dynamics 365 Commerce ennþá geturðu beðið um forsýningaraðgang af vefsíðunni [Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Yfirlit

Til að úthluta forskoðunarumhverfi Commerce með góðum árangri verður þú að búa til verk sem hefur tiltekið vöruheiti og tegund. Umhverfið og Commerce Scale Unit (CSU) eru einnig með nokkrar ákveðnar færibreytur sem verður að nota þegar rafrænum viðskiptum er úthlutað. Leiðbeiningarnar í þessu efni lýsa öllum nauðsynlegum skrefum sem þarf til að ljúka úthlutun og breytunum sem þú verður að nota.

Eftir árangursríka úthlutun á forskoðunarumhverfi Commerce þarf að ljúka nokkrum eftirúthlutunarskrefum til að undirbúa það. Sum skref eru valkvæð, eftir þeim þáttum kerfisins þú vilt meta. Þú getur alltaf klárað valfrjálsu skrefin seinna.

Fyrir upplýsingar um hvernig skuli stilla þér forskoðunarumhverfi Commerce eftir að því hefur verið úthlutað skal sjá [Stilla forskoðunarumhverfi Commerce](cpe-post-provisioning.md). Upplýsingar um hvernig eigi að stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce er að finna í [Stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce](cpe-optional-features.md).

Láttu Microsoft vita ef þú hefur einhverjar spurningar um ráðstöfunarskrefin eða lendir í einhverjum vandræðum í [Microsoft Dynamics 365 Commerce forskoða Yammer hóp](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi forsendur verða að vera til áður en þú getur veitt forskoðunarumhverfi Commerce:

- Þú hefur aðgang að Microsoft Dynamics Lifecycle Services (LCS)-gáttinni.
- Þú ert fyrirliggjandi félagi eða viðskiptavinur Microsoft Dynamics 365 og getur stofnað Dynamics 365 Commerce verk.
- Þú fékkst samþykkt inn í Dynamics 365 Commerce Forskoða kerfi.
- Þú hefur nauðsynlegar heimildir til að búa til verk fyrir **Flytja, búa til lausnir og læra**.
- Þú ert meðlimur í hlutverkinu **Umhverfisstjóri** eða **Eigandi verks** í verkinu þar sem þú munt að sjá um umhverfið
- Þú hefur stjórnandaaðgang að Microsoft Azure-áskriftinni þinni eða ert í sambandi við áskriftarstjórann sem getur lokið skrefunum tveimur sem krefjast stjórnunarheimilda fyrir þína hönd.
- Þú hefur leigjandakenni þitt fyrir Azure Active Directory (Azure AD) í boði.
- Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem kerfisstjórahóp netverslunar og þú ert með kenni hans tiltækt.
- Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem stjórnandahóp einkunna og umsagna og þú ert með kenni hans tiltækt. (Þessi öryggishópur getur verið sá sami og kerfisstjórinn fyrir netkerfi.)

## <a name="provision-your-commerce-preview-environment"></a>Úthluta forskoðunarumhverfi þínu fyrir Commerce

Þessar aðferðir útskýra hvernig á að bjóða upp á forskoðunarumhverfi Commerce. Þegar þú hefur lokið við þau er forskoðunarumhverfi Commerce tilbúið til uppsetningar. Allar þær aðgerðir sem er lýst hér fara fram í LCS-gáttinni.

> [!IMPORTANT]
> Forskoðunaraðgangur er bundinn við LCS-reikninginn og -fyrirtækið sem þú tilgreindir í forskoðunarforriti Commerce. Þú verður að nota sama reikning til að veita forskoðunarumhverfi Commerce. Ef þú þarft að nota annan LCS-reikning eða -leigjanda fyrir forskoðunarumhverfi Commerce verður þú að láta Microsoft í té þessar upplýsingar. Sjá upplýsingar um tengilið í kaflanum [Stuðningur við forskoðunarumhverfi í Commerce](#commerce-preview-environment-support) síðar í þessu efni.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Staðfestu að forskoðunaraðgerðir séu tiltækar og virkjaðar í LCS

Til að staðfesta að forskoðunaraðgerðir séu tiltækar og virkjaðar í LCS skal fylgja þessum skrefum.

1. Skráðu þig inn í [LCS-gáttina](https://lcs.dynamics.com) með því að nota sama LCS-reikning og þú notaðir til að biðja um aðgang að forskoðuninni.
1. Flettu alla leið til hægri á heimasíðu LCS og veldu reitinn **Forskoðun aðgerðastjórnunar**.

    ![Stjórnun forskoðunarreits](./media/preview1.png)

1. Skrunaðu niður að **Einkaforskoðunareiginleikar** og staðfestu að eftirfarandi aðgerðir séu tiltækar og virkjaðar:

    - Mat á rafrænum viðskipta
    - Forritsumhverfi forskoðunar á Commerce

    ![Einkaforskoðunareiginleikar](./media/preview2.png)

1. Ef þessir eiginleikar birtast ekki á listanum skaltu hafa samband við Microsoft og gefa upp vinnupóstfang þitt, LCS reikning og upplýsingar um leigjanda. Sjá upplýsingar um tengilið í kaflanum [Stuðningur við forskoðunarumhverfi í Commerce](#commerce-preview-environment-support).

### <a name="create-a-new-project"></a>Stofna nýtt verk

Til að stofna nýtt verk í LSC skal fylgja þessum skrefum.

1. Á heimasíðu LCS velurðu plúsmerkið (**+**) til að búa til verk.
1. Fylgdu einu af þessum skrefum á hægri glugganum:

    - Ef þú ert félagi skaltu velja **Flytja, búa til lausnir og læra**.
    - Ef þú ert viðskiptavinur skaltu velja **Væntanleg forsala**.

1. Færðu inn heiti, lýsingu og iðnað.
1. Í reitnum **Heiti afurðar** velurðu **Dynamics 365 Retail**.
1. Í reitnum **Útgáfa afurðar** velurðu **Dynamics 365 Retail**.
1. Í reitnum **Aðferð** velurðu **Dynamics Retail útfærsluaðferð**.
1. Valfrjálst: Hægt er að flytja inn hlutverk og notendur úr fyrirliggjandi verki.
1. Velja **Stofna**. Verksýnin birtist.

### <a name="add-the-azure-connector"></a>Bættu Azure-tengingunni við

Fylgdu þessum skrefum til að bæta Azure Connector við LCS-verkið.

1. Fylgið einu af eftirfarandi skrefum:

    - Ef þú ert félagi skaltu velja reitinn **Stillingar verks** lengst til hægri.
    - Ef þú ert viðskiptavinur velurðu **Stillingar verks** í efstu valmyndinni.

1. Velja **Azure-tengingar**.
1. Veldu **Bæta við** til að bæta við Azure-tengingu.
1. Færið inn heiti.
1. Sláðu inn Azure-áskriftarkenni þitt.
1. Kveiktu á valkostinum **Skilgreina að nota Azure Resource Manager (ARM)**.
1. Staðfestu að gildið **Azure áskrift AAD leigjandaléns (eða kenni)** sé rétt. Hafðu samband við Azure áskriftarstjórann þinn, eftir þörfum.
1. Veljið **Næst**.
1. Fylgdu leiðbeiningunum á síðunni til að veita nauðsynlegum forritum aðgang að áskriftinni þinni. Hafðu samband við Azure áskriftarstjórann þinn, eftir þörfum.

    1. Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).
    1. Gakktu úr skugga um að rétt skráarsafn sé valið og síðan, í valmyndinni til vinstri, velurðu **Áskrift**.
    1. Finndu rétta áskrift á listanum og veldu hana. Notaðu leitina eftir þörfum.
    1. Í valmyndinni velurðu **Aðgangsstýring (IAM)**.
    1. Til hægri, undir **Bæta við hlutverkaúthlutun** velurðu **Bæta við**. Glugginn **Bæta við hlutverki** birtist.
    1. Á svæðinu **Hlutverk**, veljið **Þátttakandi**.
    1. Í reitnum **Úthluta aðgangi að** notarðu sjálfgefið gildi, **Azure AD notandi, hópur eða þjónustustjóri**.
    1. Undir **Velja** slærðu inn **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Veldu **Virkjunarþjónusta Dynamics \[wsfed-enabled\]** í listanum.
    1. Veljið **Vista**.

1. Veljið **Næst**.
1. Fylgdu leiðbeiningunum á síðunni til að veita nauðsynlegum forritum aðgang að áskriftinni þinni. Hafðu samband við Azure áskriftarstjórann þinn, eftir þörfum.
1. Veljið **Næst**.
1. Í reitnum **Azure-svæðið** velurðu **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.
1. Veldu **Tengjast**. Azure tengið þitt ætti að birtast á listanum.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Flytjið inn grunnviðbótina Forskoðunarsýnishorn af Commerce

Fylgdu þessum skrefum til að flytja grunnviðbótina Forskoðunarsýnishorn Commerce inn í verkið.

1. Opnaðu heimasíðu fyrir verkefnið með því að velja heiti verkefnis efst.
1. Fylgið einu af eftirfarandi skrefum:

    - Ef þú ert félagi skaltu velja reitinn **Eignasafn** lengst til hægri.
    - Ef þú ert viðskiptavinur velurðu **Eignasafn** í efstu valmyndinni.

1. Í listanum til vinstri skaltu velja **Virkjanlegur hugbúnaðarpakki**.
1. Velja **Innflutningur**.
1. Undir **Samnýtt eignasafn** velurðu **Grunnviðbótin Forskoðunarsýnishorn af Commerce** af eignalistanum.
1. Veldu **Tína til**. Þér verður beint aftur í eignasafnið og þú ættir að sjá viðbótina á listanum.

Eftirfarandi mynd sýnir aðgerðir sem þarf að grípa til á LCS-síðunni **Eignasafn**.

![Innflutningur á grunnviðbótinni Forskoðunarsýnishorn af Commerce](./media/import.png)

### <a name="deploy-the-environment"></a>Virkjaðu umhverfið

Til að virkja umhverfið skaltu fylgja þessum skrefum.

> [!NOTE]
> Þú gætir ekki þurft að klára skref 6, 7 og / eða 8 því að síðum sem hafa einn valkost er sleppt. Þegar þú ert í sýninni **Færibreytur umhverfis** skaltu staðfesta að textinn **Dynamics 365 Commerce - (Forskoðun) - Kynning (10.0.* x* með verkvangsuppfærslu *xx*)** birtist beint fyrir ofan reitinn **Heiti umhverfis**. Fyrir nánari upplýsingar, sjá myndina sem birtist eftir 8. skref.

1. Í efstu valmyndinni velurðu **Umhverfi í skýi**.
1. Veldu **Bæta við** til að bæta við umhverfi.
1. Í reitnum **Útgáfa forrits**, veldu nýjustu útgáfuna. Ef þú hefur sérstaka þörf fyrir að velja aðra forritsútgáfu en nýjustu útgáfuna skaltu ekki velja útgáfu áður **10.0.8**.
1. Í reitnum **Útgáfa verkvangs**, notarðu verkvangsútgáfuna sem er sjálfkrafa valin fyrir forritsútgáfuna sem þú valdir. 

    ![Val á forrita- og verkvangsútgáfum](./media/project1.png)

1. Veljið **Næst**.
1. Veldu **Kynning** grannfræði umhverfis.

    ![Val á grannfræði umhverfis 1](./media/project2.png)

1. Veldu **Dynamics 365 Commerce - Kynning** sem grannfræði umhverfis. Ef þú stilltir upp eitt Azure-tengi áður verður það notað fyrir þetta umhverfi. Ef þú stilltir mörg Azure-tengi geturðu valið hvaða tengi á að nota: **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**. (Til að fá bestan heildarárangur mælum við með að þú veljir **Vestur-BNA 2**.)

    ![Val á grannfræði umhverfis 2](./media/project3.png)

1. Á síðunni **Setja upp umhverfi** slærðu inn umhverfisheiti. Hafðu ítarlegar stillingar óbreyttar.

    ![Setja upp umhverfissíðu](./media/project4.png)

1. Stilltu VM stærð eftir þörfum. (Við mælum með VM birgðaeiningunni \[SKU\] **D13 v2**.)
1. Skoðaðu verðlagningu og leyfisskilmála og veldu síðan gátreitinn til að gefa til kynna að þú samþykki þá.
1. Veljið **Næst**.
1. Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Setja upp**. Þú munt fara aftur í gluggann **Umhverfi í skýi** og umhverfi þitt ætti að birtast á listanum.

    Umbeðið umhverfi þitt birtist í biðröð og síðan er það notað. Það tekur nokkurn tíma að klára vinnuflæði umhverfisins. Athugaðu því aftur eftir um það bil sex til níu tíma.

1. Áður en lengra er haldið skaltu ganga úr skugga um að staða umhverfisins sé **Uppsett**.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Frumstilla Commerce Scale Unit (ský)

Fylgið eftirfarandi skrefum til að hefja CSU.

1. Í glugganum **Umhverfi í skýi** velurðu umhverfi þitt af listanum.
1. Í umhverfissýninni til hægri skaltu velja **Nánari upplýsingar**. Umhverfisupplýsingaskjárinn birtist.
1. Undir **Eiginleikar umhverfis** velurðu **Stjórna**.
1. Á flipanum **Commerce** velurðu **Frumstilla**. Skjár CSU frumstillingarifæribreyta birtist.
1. Í reitnum **Svæði** velurðu **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.
1. Í reitnum **Útgáfa** velurðu **Tilgreina útgáfu** á listanum og tilgreinir síðan **9.18.20014.4** í reitnum sem birtist. Vertu viss um að tilgreina nákvæma útgáfu sem er tilgreind hér. Annars verður þú að uppfæra RCSU í réttri útgáfu síðar.
1. Kveiktu á valkostinum **Nota viðbót**.
1. Á listanum yfir viðbætur velurðu **Grunnviðbótin Forskoðunarsýnishorn af Commerce**.
1. Veldu **Frumstilla**.
1. Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Já**. Skjárinn **Commerce-stjórnun** birtist aftur, þar sem flipinn **Commerce** er valinn. CSU þinn hefur verið í biðröð vegna úthlutunar.
1. Áður en lengra er haldið skaltu ganga úr skugga um að staða CSU sé **Tókst**. Frumstilling tekur um það bil tvær til fimm klukkustundir.

### <a name="initialize-e-commerce"></a>Frumstilla rafræn viðskipti

Fylgið eftirfarandi skrefum til að frumstilla e-Commerce.

1. Á flipanum **e-Commerce** skoðarðu samþykki fyrir forskoðun og velir síðan **Uppsetning**.
1. Í reitnum **Leigjandaheiti í e-Commerce** færirðu inn heiti. Hafðu þó í huga að þetta heiti mun birtast í sumum slóðum sem vísa til netverslunartilviksins.
1. Í reitnum **Heiti Commerce Scale Unit** skal velja CSU í listanum. (Listinn ætti aðeins að hafa einn valkost.)

    Reiturinn **Landafræði rafrænna viðskipta** er stilltur sjálfkrafa og ekki er hægt að breyta gildinu.

1. Veldu **Næst** til að halda áfram.
1. Í reitnum **Studd hýsilheiti** slærðu inn gilt lén, eins og `www.fabrikam.com`.
1.  Í reitnum **AAD-öryggishópur fyrir kerfisstjóra** slærðu inn fyrstu stafina í nafni öryggishópsins sem þú vilt nota. Veldu stækkunarglerstáknið til að birta leitarniðurstöður. Velja réttan öryggisflokk af listanum.
2.  Í reitnum **AAD-öryggishópur stjórnanda fyrir einkunnir og umsagnir** slærðu inn fyrstu stafina í nafni öryggishópsins sem þú vilt nota. Veldu stækkunarglerstáknið til að birta leitarniðurstöður. Velja réttan öryggisflokk af listanum.
1. Hafðu kveikt á valkostinum **Virkja einkunna- og umsagnaþjónustu**.
1. Veldu **Frumstilla**. Skjárinn **Commerce-stjórnun** birtist aftur, þar sem flipinn **e-Commerce** er valinn. Frumstilling rafrænna viðskipta er hafin.
1. Áður en lengra er haldið skaltu bíða þar til staða frumstillingar í netverslun er **Frumstilling tókst**.
1. Undir **Krækjur** neðst til hægri, skrifaðu vefslóðirnar fyrir eftirfarandi tengla:

    * **rafræn viðskipti síða** - Hlekkurinn á rótina á netverslunarsíðunni þinni.
    * **stjórnunartæki fyrir e-verslun** - Hlekkurinn að stjórnunartólinu.

## <a name="commerce-preview-environment-support"></a>Stuðningur við forskoðunarumhverfi fyrir Commerce

Ef þú lendir í vandræðum meðan þú lýkur úthlutunarskrefunum skaltu fara á [Microsoft Dynamics 365 Commerce Forskoðun Yammer hópur](https://aka.ms/Dynamics365CommercePreviewYammer) fyrir aðstoð.

## <a name="next-steps"></a>Næstu skref

Til að halda áfram úthlutunar- og stillingarferli forskoðunarumhverfis Commerce eftir að því hefur verið úthlutað skal sjá [Stilla forskoðunarumhverfi Commerce](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi](cpe-overview.md)

[Skilgreina Dynamics 365 Commerce forskoðunarumhverfi](cpe-post-provisioning.md)

[Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce forskoðunarumhverfi](cpe-optional-features.md)

[Dynamics 365 Commerce yfirlitsumhverfi algengra spurninga](cpe-faq.md)

[Microsoft Dynamics Lifecycle Services (LSC)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (ský)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)

