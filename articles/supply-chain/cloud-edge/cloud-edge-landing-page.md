---
title: Einingarkvarðar fyrir ský og jaðra fyrir vinnuálag framleiðslu og vöruhúsakerfis
description: Þetta efnisatriði veitir upplýsingar um einingarkvarðar fyrir ský og jaðra fyrir vinnuálag framleiðslu og vöruhúsakerfis
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 28301cdfb86d00ea6f04e996fe7fb1485e83b2d4
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104965"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Einingarkvarðar fyrir ský og jaðra fyrir vinnuálag framleiðslu og vöruhúsakerfis

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Einingarkvarðar fyrir ský gerir kleift að dreifa vinnuálagi í vinnusal og vöruhúsi í mismunandi umhverfum. Þessi virkni getur hjálpað til við að auka afköst, koma í veg fyrir truflun á þjónustu og hámarkað uppitíma. Hún er veitt af eftirfarandi viðbótum:

- Viðbót Cloud Scale Unit fyrir Dynamics 365 Supply Chain Management
- Viðbót Edge Scale Unit fyrir Dynamics 365 Supply Chain Management

Fyrirtæki sem vinna með framleiðslu og dreifingu verða að geta keyrt helstu viðskiptaferla allan sólarhringinn án truflana og á eðlilegum hraða. Cloud and edge scale units gerir fyrirtækjum kleift að keyra mikilvægustu framleiðslu- og vöruhúsaferla án truflana, jafnvel þegar koma upp stöku vandamál tengd nettengingu eða biðtíma.

## <a name="public-preview-information"></a>Upplýsingar um forútgáfu

Forútgáfan býður upp á eitt umhverfi sem virkar sem miðstöð í skýi fyrir Dynamics 365 Supply Chain Management-umhverfið og eitt umhverfi sem virkar sem skýjaeiningarkvörðun.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Skoða stöðu

Forútgáfan fyrir cloud og edge scale units verður aðgengileg fyrir fyrirliggjandi viðskiptavini Supply Chain Management í október 2020.

Til að fá aðgang að forútgáfu 10.0.15/verkvangsuppfærslu 39 fyrir uppsetningu í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) umhverfinu, þarftu að vera hluti af forskoðun snemmbúins aðgangs (einnig þekkt sem PEAP) fyrir Supply Chain Management. Hægt er að taka þátt í PEAP ef þú ert þegar meðlimur stærra [Dynamics Insider Program](https://experience.dynamics.com/insider). Veljið einfaldlega forritið sem heitir „Finance & Operations: Forskoða snemmbúinn aðgang (PEAP).“

> [!IMPORTANT]
> Möguleiki einingarkvarða fyrir Supply Chain Management er aðeins í boði ef þú samþykkir [Cloud + Edge forútgáfa fyrir Finance and Operations skilmála](https://Aka.ms/SCMCnETerms).

### <a name="data-processing-for-the-preview"></a>Gagnavinnsla fyrir forútgáfuna

Meðan opin forútgáfa stendur yfir verða sumar umsjónarþjónustur hýstar í Bandaríkjunum. Hins vegar, þegar eiginleikinn verður almennt í boði verða þessar umsjónarþjónustur í boði á öllum svæðum sem Supply Chain Management styður. Þetta hefur áhrif á flutning og geymslu stjórnunarupplýsinga sem stjórnandi einingarkvörðunar notar, þ.m.t.:

- Heiti og auðkenni leigjenda
- LCS-verkkenni
- Tölvupóstur stjórnanda sem er notað fyrir innskráningu
- Umhverfiskenni fyrir miðstöð og kvörðunareiningar
- Skilgreiningar vinnuálags
- Safnaðar mælingar (t.d. biðtími og gegnumstreymi) sem eru sýndar á greiningarsíðu vörpunar

Gögnum sem flutt eru í og geymd í gagnamiðstöðvum Bandaríkjanna verður eytt þegar notkun á umhverfum forútgáfa er hætt.

### <a name="sign-up-for-the-preview"></a>Skráðu þig fyrir forskoðun

Til að skrá sig fyrir forútgáfu cloud og edge fyrir Supply Chain Management, verður fyrirtækið þitt að vera með lifandi skýjaumhverfi Supply Chain Management.

Möguleikar einingarkvörðunar eru sem stendur í opinni forútgáfu. Þegar þú skráir þig, verður þú að nota notandareikning í tilteknum leigjanda. Einnig þarf að vera verkeigandi eða stjórnandi umhverfis í LCS fyrir virkt LCS-verk Dynamics 365 í þeim leigjanda.

Þegar þú skráir þig fyrir forútgáfuna, velurðu leigjanda og ferð í gegnum innskráningarferlið. Um leið og Microsoft getur úthlutað forútgáfunni, færðu tölvupóst frá okkur með úthlutunarupplýsingum og kynningarkóðum fyrir tvö umhverfi (miðstöð og einingarkvarða) fyrir viðeigandi LCS-verk. Þá er hægt að setja upp umhverfin tvö sem 2 laga sandkassaumhverfi. Þessi umhverfi gilda í 60 daga frá stofndegi kynningarkóðans. Ekki ætti að nota umhverfin fyrr en skrefið sem lýst er í næstu efnisgrein er lokið.

Þegar búið er að staðfesta hjá Microsoft að umhverfin tvö hafi verið sett upp með því að nota kynningarkóðana, verður annað umhverfanna skilgreint sem miðstöð og hitt skilgreint sem einingarkvarði. Síðan er hægt að skilgreina einingarkvarðana og setja upp vinnuálag valins vöruhúsakerfi og framleiðslu með því að nota [Gátt Scale Unit Manager](https://aka.ms/SCMSUM).

Umhverfum forútgáfu verður eytt sjálfkrafa eftir 60 daga. Hins vegar gæti þeim verið eytt fyrr ef svo virðist sem þau séu ekki notuð. Þegar umhverfum forútgáfu hefur verið eytt, geturðu skráð þig og beðið eftir nýrri uppsetningu forútgáfu.

Til að skrá sig fyrir forskoðuninni skaltu fara í [Gátt Scale Unit Manager](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Takmarkanir sem gilda meðan á forskoðunartímabilinu stendur

> [!IMPORTANT]
> Á upphafsstigi forskoðunaráætlunarinnar fyrir þennan eiginleika, styður Microsoft aðeins miðstöðvar sem eru með einingarkvarða í skýi, ekki miðstöðvar sem eru með einingarkvarða í edge. Edge-einingarkvarðar eru uppsettir á staðnum og verða væntanlega aðgengilegir á næsta stigi áætlunarinnar.

Vegna þess að einingarkvarðar í skýi og edge eru forskoðunareiginleikar, er framboð á þjónustum þeim tengdum í boði í takmörkuðum löndum og svæðum. Með því að virkja einingarkvarða fyrir ský og edge, staðfestir þú að þú skiljir að sum gögn sem tengjast skilgreiningu og úrvinnslu einingarkvarða í skýi og edge kunni að vera geymd í gagnamiðstöðvum sem eru staðsettar í Bandaríkjunum. Með því að virkja einingarkvarða í skýi og edge, samþykkir þú einnig [Forskoðun skýs + Edge fyrir Finance and Operations skilmála](https://Aka.ms/SCMCnETerms). Frekari upplýsingar um einingarkvarða í skýi og edge er að finna í [fylgiskjöl](https://aka.ms/scmcne).

Persónuvernd þín skiptir Microsoft máli. Til að fá nánari upplýsingar skaltu lesa [yfirlýsingu okkar um persónuvernd](https://aka.ms/privacy).

> [!IMPORTANT]
> Einhver viðskiptavirkni er ekki studd að fullu í opinni forútgáfu þegar vinnuálag er notað í einingarkvörðum. Frekari upplýsingar um hagnýtt vinnuálag er að finna í hlutunum síðar í þessu efnisatriði.

## <a name="scale-units-and-dedicated-workloads"></a>Einingarkvarðar og úthlutað vinnuálag

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 með einingarkvörðum":::

Einingarkvarðar stækka umhverfi Supply Chain Management miðstöðvarinnar með því að bæta við úthlutaðri úrvinnslugetu. Hægt er að keyra einingarkvarða í skýinu. Að öðrum kosti er hægt að keyra þá á staðbundinni starfsstöð. Hægt er að aftengja einingarkvarða tímabundið frá miðstöðvarumhverfinu. Þegar þeir eru tengdir fá einingarkvarðarnir allar upplýsingarnar sem þarf til að keyra úthlutaða úrvinnslu fyrir úthlutað vinnuálag.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Valkostir einingarkvarða í opinni forútgáfu":::

Fyrir opna forútgáfu er hægt að skilgreina umhverfi miðstöðvar með valið vinnuálag í einingarkvarða í skýinu með því að nota gátt Scale Unit Manager. Þátttakendur forskoðunar sem eru með aðgang að staðbundnum viðskiptagögnum (LBD) í umhverfi á staðnum geta einnig skilgreint LBD-umhverfið sem einingarkvarða edge.

Vinnuálag er skilgreint safn viðskiptavirkni sem hægt er að taka til greina og úthluta til einingarkvarða. Sem stendur er til tvenns konar vinnuálag í forskoðun:

- Framkvæmd framleiðslu
- Vöruhúsakerfi

Hægt er að úthluta einu fyrir hvora gerð vinnuálags á hvern einingarkvarða. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Úthlutað vinnuálag fyrir framkvæmd framleiðslu í einingarkvarða

Fyrir framkvæmd framleiðslu, bjóða einingarkvarðar edge upp á eftirfarandi möguleika, jafnvel þegar edge-einingarnar eru ekki tengdar við skýið:

- Stjórnandi véla og eftirlitsmenn vinnusalar fá aðgang að framleiðsluáætlun.
- Stjórnendur vél geta uppfært áætlunina með því að keyra afmarkað og verk framleiðsluferlis.
- Umsjónarmaður vinnusalar getur breytt starfsáætluninni.
- Starfskraftar geta opnað tíma og viðveru til innstimplunar og útstimplunar á jaðrinum til að tryggja réttan útreikning launa starfsmanna.

Frekari upplýsingar eru í [upplýsingar um vinnuálag einingarkvarða í framleiðslu](cloud-edge-workload-manufacturing.md).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Úthlutaðir möguleikar vinnuálags í vöruhúsakerfi í einingarkvarða

Fyrir vöruhúsakerfi, bjóða einingarkvarðar edge upp á eftirfarandi möguleika, jafnvel þegar edge-einingarnar eru ekki tengdar við skýið:

- Úrvinnsla á völdum bylgjuaðferðum er virkjuð fyrir sölupantanir og eftirspurnaráfyllingu.
- Starfskraftar í vöruhúsi geta keyrt vöruhúsavinnu sölu og eftirspurnaráfyllingar með vöruhúsaforritinu.
- Starfskraftar í vöruhúsi geta spurst fyrir um lagerbirgðir með vöruhúsaforritinu.
- Starfskraftar í vöruhúsi geta stofnað og keyrt birgðahreyfingar með vöruhúsaforritinu.
- Starfskraftar í vöruhúsi geta skráð innkaupapantanir og sinnt frágangsvinnu með vöruhúsaforritinu.

Frekari upplýsingar er að finna í [upplýsingar um vinnuálag einingarkvarða í vöruhúsi](cloud-edge-workload-warehousing.md).

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Innleiða einingarkvarða fyrir umhverfi Supply Chain Management

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Setja upp forútgáfu fyrir einingarkvarða í skýi og edge

Eftirfarandi mynd sýnir skráningu og flæði úthlutunar fyrir opna forútgáfu fyrir einingarkvarða í skýi.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Skráningarferli forútgáfu":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>Veljið LCS-verk leigjandans og ítarlegt forskoðunarferli

Í opnu forútgáfunni sýnir [Gátt Scale Unit Manager](https://aka.ms/SCMSUM) lista yfir leigjendur sem reikningurinn þinn er hluti af, og hvar þú ert eigandi eða stjórnandi umhverfis fyrir LCS-verk.

Ef leigjandinn sem leitað er að er ekki á þessum lista skaltu fara í [LCS](https://lcs.dynamics.com/v2) og ganga úr skugga um að þú sért annaðhvort stjórnandi umhverfis eða verkeigandi LCS-verks fyrir þann leigjanda. Athugið að aðeins Azure Active Directory (Azure AD) reikningar frá völdum leigjanda mega ljúka skráningarferlinu.

> [!NOTE]
> Þegar búið er að gera breytingarnar á LCS, getur það tekið allt að 30 mínútur fyrir listann yfir leigjendur að sýna breytingarnar.

Listinn sýnir skráningarstöðuna fyrir hvern leigjanda.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Nýskráningarvalkostur fyrir leigjanda":::

Veljið tengilinn **Smellið hér til að skrá sig** til að skrá LCS-leigjandann til þátttöku í forútgáfunni. Samþykkja verður skilmálana. Einnig þarf að gefa upp tölvupóstfang fyrirtækis þar sem Microsoft getur sent samskipti sem tengjast skráningarferli forskoðunar.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Innsending nýskráningar fyrir leigjanda":::

Microsoft mun fara yfir beiðnina og tilkynna um næstu skref með því að senda tölvupóst á netfangið sem gefið var upp á nýskráningareyðublaðinu.

Þegar búið er að veita aðgang að forskoðunaráætluninni, færðu tvo kynningarkóða fyrir LCS-verkið þitt. Nú er hægt að nota þessa kynningarkóða il að setja upp tvö umhverfi í LCS. Umhverfin verða að nota PEAP-útgáfu 10.0.15 eða nýrri. Þegar búið er að nota kynningarkóðana skal láta Microsoft vita (í samræmi við leiðbeiningar) þannig að hægt sé að ljúka virkjun umhverfisins fyrir forskoðunareiginleikana. Microsoft lætur vita þegar þessu skilgreiningarskrefi er lokið.

Nú er hægt að hefja skilgreiningu á einingarkvörðum og vinnuálagi í forskoðunarumhverfinu.

> [!IMPORTANT]
> Þegar einingarkvarðar í skýi eru skilgreindir er hægt að [gera öll áskilin skref í gátt Scale Unit Manager](#scale-unit-manager-portal).
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Stjórna einingarkvörðum í skýi og vinnuálagi með gátt Scale Unit Manager

Farið í [Gátt Scale Unit Manager](https://aka.ms/SCMSUM) og skráið ykkur inn með leigjandareikningnum. Á síðunni **Skilgreina einingarkvarða** er hægt að bæta við umhverfi miðstöðvar ef það er ekki þegar í boði. Síðan er hægt að velja miðstöðina sem á að skilgreina með einingarkvörðum og vinnuálagi.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Stjórnun einingarkvarða og vinnuálags":::

Til að bæta við einum eða fleiri einingarkvörðum sem eru í boði í þínu nærumhverfi, skal velja **Bæta við einingarkvörðum**. Í forskoðuninni ætti að birtast einingarkvarði í skýi sem þú settir upp fyrir einn af kynningarkóðunum sem þú fékkst sem hluti af áætlun forskoðunar.

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

Í flipanum **Skilgreint vinnuálag** skal nota hnappinn **Stofna vinnuálag** til að bæta vöruhúsakerfi eða vinnuálagi framleiðslu við einn einingarkvarðann. Fyrir hvert vinnuálag þarf að tilgreina samhengi ferlanna sem vinnuálagið verður í. Fyrir vinnuálag vöruhúsakerfis er samhengið tiltekið vöruhús á tilteknu svæði og lögaðila. Fyrir vinnuálag framkvæmdar í framleiðslu er samhengið tiltekið svæði í lögaðila.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Stofnun vinnuálags":::

> [!IMPORTANT]
> Gátt Scale Unit Manager í forskoðun leyfir þér ekki að fjarlægja vinnuálag úr einingarkvörðum eða taka úthlutun á einingarkvarða til baka úr miðstöð þegar búið er að úthluta. Ef nauðsynlegt er að fjarlægja úthlutun skal hafa samband við tengiliðinn sem sér um áætlun forskoðunar.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]