---
title: Úthluta forskoðunarumhverfi fyrir Commerce
description: Þetta efni útskýrir hvernig á að úthluta forskoðunarumhverfi Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934749"
---
# <a name="provision-a-commerce-preview-environment"></a>Úthluta forskoðunarumhverfi fyrir Commerce

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að úthluta forskoðunarumhverfi Microsoft Dynamics 365 Commerce.

Áður en þú byrjar, mælum við með að þú rennir að minnsta kosti í gegnum allt efnið til að fá hugmynd um hvað ferlið felur í sér og hvað efnið inniheldur.

> [!NOTE]
> Ef þér hefur ekki verið veittur aðgangur að forskoðun Dynamics 365 Commerce ennþá geturðu beðið um forsýningaraðgang af [Vefsíðu Commerce](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Yfirlit

Til að úthluta forskoðunarumhverfi Commerce með góðum árangri verður þú að búa til verk sem hefur tiltekið vöruheiti og tegund. Umhverfið og Retail Cloud Scale Unit (RCSU) hafa einnig nokkrar sérstakar færibreytur sem þú þarft að nota við úthlutun rafrænna viðskipta síðar. Leiðbeiningarnar í þessu efni lýsa öllum nauðsynlegum skrefum sem þú verður að ljúka og breytunum sem þú verður að nota.

Eftir árangursríka úthlutun á forskoðunarumhverfi Commerce þarf að ljúka nokkrum eftirúthlutunarskrefum til að undirbúa það. Sum skref eru valkvæð, eftir þeim þáttum kerfisins þú vilt meta. Þú getur alltaf klárað valfrjálsu skrefin seinna.

Fyrir upplýsingar um hvernig skuli stilla þér forskoðunarumhverfi Commerce eftir að því hefur verið úthlutað skal sjá [Stilla forskoðunarumhverfi Commerce](cpe-post-provisioning.md). Upplýsingar um hvernig eigi að stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce er að finna í [Stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce](cpe-optional-features.md).

Láttu Microsoft vita ef þú hefur einhverjar spurningar um ráðstöfunarskrefin eða lendir í einhverjum vandræðum í [Microsoft Dynamics 365 Commerce forskoða Yammer hóp](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Forkröfur

Eftirfarandi forsendur verða að vera til áður en þú getur veitt forskoðunarumhverfi Commerce:

- Þú hefur aðgang að Microsoft Dynamics Lifecycle Services (LCS)-gáttinni.
- Þú fékkst samþykkt inn í Dynamics 365 Commerce Forskoða kerfi.
- Þú hefur nauðsynlegar heimildir til að búa til verk fyrir **Væntanlegar forsölur** eða **Flytja, búa til lausnir og læra**.
- Þú ert meðlimur í hlutverkinu **Umhverfisstjóri** eða **Eigandi verks** í verkinu þar sem þú munt að sjá um umhverfið
- Þú hefur stjórnandaaðgang að Microsoft Azure-áskriftinni þinni eða ert í sambandi við áskriftarstjórann sem getur lokið skrefunum tveimur sem krefjast stjórnunarheimilda fyrir þína hönd.
- Þú hefur leigjandakenni þitt fyrir Azure Active Directory (Azure AD) í boði.
- Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem kerfisstjórahóp netverslunar og þú ert með kenni hans tiltækt.
- Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem stjórnandahóp einkunna og umsagna og þú ert með kenni hans tiltækt. (Þessi öryggishópur getur verið sá sami og kerfisstjórinn fyrir netkerfi.)

### <a name="find-your-azure-ad-tenant-id"></a>Finndu Azure AD-leigjandakenni þitt

Leigjandakenni þitt fyrir Azure AD er alþjóðlegt auðkenni (GUID) sem líkist þessu dæmi: **72f988bf-86f1-41af-91ab-2d7cd011db47**.

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a>Finndu Azure AD-leigjandakenni þitt með því að nota Azure-gáttina

1. Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).
1. Gangið úr skugga um að rétt skráasafn sé valið.
1. Á valmyndinni til vinstri velurðu **Azure Active Directory**.
1. Undir **Stjórna** velurðu **Eiginleika**. Leigjandakenni þitt fyrir Azure AD birtist undir **Skráasafnskenni**.

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a>Finndu leigjandakenni þitt fyrir Azure AD með því að nota OpenID Connect-lýsigögn

Búðu til OpenID-slóð með því að skipta út **\{YOUR\_DOMAIN\}** með léninu þínu, eins og `microsoft.com`. Til dæmis, mun `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` verða `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.

1. Farðu á OpenID-slóðina sem inniheldur lénið þitt.

    Hægt er að finna leigjandakenni Azure AD í mörgum eiginleikagildum.

1. Finndu **authorization\_endpoint** og dragðu út GUID sem birtist strax á eftir `login.microsoftonline.com/`.

### <a name="find-your-azure-ad-security-group-id"></a>Finndu þitt Azure AD-kenni öryggishóps

Kenni þitt fyrir Azure AD-öryggishóp er GUID sem líkist þessu dæmi: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.

Þessi aðferð gerir ráð fyrir að þú sért meðlimur í hópnum sem þú ert að reyna að finna kenni fyrir.

1. Opnaðu [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).
1. Veldu **Skráðu inn með Microsoft** og skráðu þig inn með skilríkjum þínum.
1. Vinstra megin velurðu **sýna fleiri sýni**.
1. Í hægri glugganum virkjarðu **Hópar**.
1. Lokaðu hægri glugganum.
1. Veldu **alla hópa sem ég tilheyri**.
1. Í reitnum **Forskoðun svara** skaltu finna hópinn þinn. Kenni öryggishópsins birtist undir eiginleikanum **kenni**.

## <a name="provision-your-commerce-preview-environment"></a>Úthluta forskoðunarumhverfi þínu fyrir Commerce

Þessar aðferðir útskýra hvernig á að bjóða upp á forskoðunarumhverfi Commerce. Þegar þú hefur lokið við þau er forskoðunarumhverfi Commerce tilbúið til uppsetningar. Allar þær aðgerðir sem er lýst hér fara fram í LCS-gáttinni.

> [!IMPORTANT]
> Forskoðunaraðgangur er bundinn við LCS-reikninginn og -stofnunina sem þú tilgreindir í forskoðunarforritinu. Þú verður að nota sama reikning til að veita forskoðunarumhverfi Commerce. Ef þú verður að nota annan LCS-reikning eða -leigjanda fyrir forskoðunarumhverfi Commerce verður þú að láta Microsoft í té þessar upplýsingar. Sjá upplýsingar um tengilið í kaflanum [Stuðningur við forskoðunarumhverfi í Commerce](#commerce-preview-environment-support) síðar í þessu efni.

### <a name="grant-access-to-e-commerce-applications"></a>Veita aðgang að forritum með rafræn viðskipti

> [!IMPORTANT]
> Sá sem skráir sig inn verður að vera Azure AD-leigjandastjóri sem hefur Azure AD-kenni leigjanda. Ef þessu skrefi er ekki lokið án villu munu eftirstandandi úthlutunarskrefi ekki takast.

Fylgdu þessum skrefum til að heimila forritum rafrænna viðskipta að fá aðgang að Azure-áskriftinni.

1. Settu saman vefslóð á eftirfarandi sniði:

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. Afritaðu og límdu slóðina í vafrann eða textaritilinn og settu í staðinn **\{AAD\_TENANT\_ID\}** með Azure AD-kenni leigjanda. Opnaðu síðan slóðina.
1. Í valmyndinni Azure AD skráirðu þig inn í og staðfestir að þú viljir veita **Dynamics 365 Commerce (Forskoðun)** aðgang að áskrift þinni. Þér verður beint á síðu sem segir hvort aðgerðin hafi tekist.

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
> Þú gætir ekki þurft að klára skref 6, 7 og / eða 8 því að síðum sem hafa einn valkost er sleppt. Þegar þú ert í sýninni **Færibreytur umhverfis** skaltu staðfesta að textinn **Dynamics 365 Commerce (Forskoðun) - Demo (10.0.6 með verkvangsuppfærslu 30)** birtist beint fyrir ofan reitinn **Heiti umhverfis**. Sjá myndina sem birtist eftir 8. skref.

1. Í efstu valmyndinni velurðu **Umhverfi í skýi**.
1. Veldu **Bæta við** til að bæta við umhverfi.
1. Í reitnum **Útgáfa forrits** velurðu **10.0.6**.
1. Í reitnum **Útgáfa verkvangs** velurðu **Uppfærsla verkvangs 30**.

    ![Val á forrita- og verkvangsútgáfum](./media/project1.png)

1. Veljið **Næst**.
1. Veldu **Kynning** grannfræði umhverfis.

    ![Val á grannfræði umhverfis 1](./media/project2.png)

1. Veldu **Dynamics 365 Commerce (Forskoðun) - Kynning** sem grannfræði umhverfis. Ef þú stilltir upp eitt Azure-tengi áður verður það notað fyrir þetta umhverfi. Ef þú stilltir mörg Azure-tengi geturðu valið hvaða tengi á að nota: **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**. (Til að fá bestan heildarárangur mælum við með að þú veljir **Vestur-BNA 2**.)

    ![Val á grannfræði umhverfis 2](./media/project3.png)

1. Á síðunni **Setja upp umhverfi** slærðu inn umhverfisheiti. Hafðu ítarlegar stillingar óbreyttar.

    ![Setja upp umhverfissíðu](./media/project4.png)

1. Stilltu VM stærð eftir þörfum. (Við mælum með VM birgðaeiningunni \[SKU\] **D13 v2**.)
1. Skoðaðu verðlagningu og leyfisskilmála og veldu síðan gátreitinn til að gefa til kynna að þú samþykki þá.
1. Veljið **Næst**.
1. Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Setja upp**. Þú munt fara aftur í gluggann **Umhverfi í skýi** og umhverfi þitt ætti að birtast á listanum.

    Umbeðið umhverfi þitt birtist í biðröð og síðan er það notað. Það tekur nokkurn tíma að klára vinnuflæði umhverfisins. Athugaðu því aftur eftir um það bil sex til níu tíma.

1. Áður en lengra er haldið skaltu ganga úr skugga um að staða umhverfisins sé **Uppsett**.

### <a name="initialize-rcsu"></a>Frumstilla RCSU

Fylgið eftirfarandi skrefum til að hefja tilboðsbeiðnina.

1. Í glugganum **Umhverfi í skýi** velurðu umhverfi þitt af listanum.
1. Í umhverfissýninni til hægri skaltu velja **Nánari upplýsingar**. Umhverfisupplýsingaskjárinn birtist.
1. Undir **Eiginleikar umhverfis** velurðu **Stjórna**.
1. Á flipanum **Retail** velurðu **Frumstilla**. Skjár RCSU frumstillingarifæribreyta birtist.
1. Í reitnum **Svæði** velurðu **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.
1. Í reitnum **Útgáfa** velurðu **Tilgreina útgáfu** á listanum og tilgreinir síðan **9.16.19262.5** í reitnum sem birtist. Vertu viss um að tilgreina nákvæma útgáfu sem er tilgreind hér. Annars verður þú að uppfæra RCSU í réttri útgáfu síðar.
1. Kveiktu á valkostinum **Nota viðbót**.
1. Á listanum yfir viðbætur velurðu **Grunnviðbótin Forskoðunarsýnishorn af Commerce**.
1. Veldu **Frumstilla**.
1. Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Já**. Þér er snúið aftur á skjáinn **Smásölustjórnun** þar sem flipinn **Retail** er valinn. RCSU þinn hefur verið í biðröð vegna úthlutunar.
1. Áður en lengra er haldið skaltu ganga úr skugga um að staða RCSU sé **Tókst**. Frumstilling tekur um það bil tvær til fimm klukkustundir.

### <a name="initialize-e-commerce"></a>Frumstilla rafræn viðskipti

Fylgið eftirfarandi skrefum til að frumstilla e-Commerce.

1. Á flipanum **e-Commerce (forskoðun)** skoðarðu samþykki fyrir forskoðun og velir síðan **Uppsetning**.
1. Í reitnum **Leigjandaheiti í e-Commerce** færirðu inn heiti. Hafðu þó í huga að þetta heiti mun birtast í sumum slóðum sem vísa til netverslunartilviksins.
1. Í reitnum **Heiti Retail Cloud Scale Unit** velurðu þitt RCSU á listanum. (Listinn ætti aðeins að hafa einn valkost.)

    Reiturinn **Landafræði rafrænna viðskipta** er stilltur sjálfkrafa og ekki er hægt að breyta gildinu.

1. Veldu **Næst** til að halda áfram.
1. Í reitnum **Studd hýsilheiti** slærðu inn gilt lén, eins og `www.fabrikam.com`.
1.  Í reitnum **AAD-öryggishópur fyrir kerfisstjóra** slærðu inn fyrstu stafina í nafni öryggishópsins sem þú vilt nota. Veldu stækkunarglerstáknið til að birta leitarniðurstöður. Velja öryggisflokk af listanum.
2.  Í reitnum **AAD-öryggishópur stjórnanda fyrir einkunnir og umsagnir** slærðu inn fyrstu stafina í nafni öryggishópsins sem þú vilt nota. Veldu stækkunarglerstáknið til að birta leitarniðurstöður. Velja öryggisflokk af listanum.
1. Hafðu kveikt á valkostinum **Virkja einkunna- og umsagnaþjónustu**.
1. Ef þú hefur þegar lokið Microsoft Azure Active Directory (Azure AD) samþykkisskref eins og lýst er í hlutanum „Veita aðgang að forritum með rafræn viðskipti“ skaltu velja gátreitinn til að staðfesta samþykki þitt. Ef þú hefur ekki enn lokið þessu skrefi þarftu að gera það áður en þú heldur áfram með frumstillinguna. Veldu tengilinn í textanum við hliðina á gátreitnum til að opna samþykkisgluggann og ljúka skrefinu.
1. Veldu **Frumstilla**. Þér er snúið aftur á skjáinn **Smásölustjórnun** þar sem flipinn **rafræn viðskipti (forsýning)** er valinn. Frumstilling rafrænna viðskipta er hafin.
1. Áður en lengra er haldið skaltu bíða þar til staða frumstillingar í netverslun er **Frumstilling tókst**.
1. Undir **Krækjur** neðst til hægri, skrifaðu vefslóðirnar fyrir eftirfarandi tengla:

    * **rafræn viðskipti síða** - Hlekkurinn á rótina á netverslunarsíðunni þinni.
    * **stjórnunartæki fyrir e-verslun** - Hlekkurinn að stjórnunartólinu.

## <a name="commerce-preview-environment-support"></a>Stuðningur við forskoðunarumhverfi fyrir Commerce

Ef þú lendir í vandræðum meðan þú lýkur úthlutunarskrefunum skaltu fara á [Microsoft Dynamics 365 Commerce Forskoðun Yammer hópur](https://aka.ms/Dynamics365CommercePreviewYammer) fyrir aðstoð.

Ef þú lendir í vandamálum þegar þú reynir að fá aðgang að Yammer-hóp geturðu haft samband við Microsoft með tölvupósti á <Dynamics365Commerce@microsoft.com>. Ekki er fylgst með þessu netfangi með virkum hætti. Því má búast við seinkun á viðbrögðum.

## <a name="next-steps"></a>Næstu skref

Til að halda áfram úthlutunar- og stillingarferli forskoðunarumhverfis Commerce eftir að því hefur verið úthlutað skal sjá [Stilla forskoðunarumhverfi Commerce](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir forskoðunarumhverfi Commerce](cpe-overview.md)

[Skilgreina forskoðunarumhverfi Commerce](cpe-post-provisioning.md)

[Stilltu valfrjálsa eiginleika fyrir forsýningarumhverfi Commerce](cpe-optional-features.md)

[Algengar spurningar um forskoðunarumhverfi Commerce](cpe-faq.md)

[Microsoft Dynamics Lifecycle Services (LSC)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-gátt](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce vefsvæði](https://aka.ms/Dynamics365CommerceWebsite)

[Hjálpartilföng fyrir Dynamics 365 Retail](../retail/index.md)
