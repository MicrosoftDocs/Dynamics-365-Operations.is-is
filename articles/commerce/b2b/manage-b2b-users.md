---
title: Stjórna notendum samstarfsaðila á rafrænum B2B-vefsvæðum
description: Þetta efnisatriði lýsir því hvernig stjórnendur geta bætt við, breytt og eytt notendum samstarfsaðila á rafrænum B2B-vefsvæðum.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96b76a08206b8c1bc5029acdfd385fda2870ca85
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035923"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Stjórna notendum samstarfsaðila á rafrænum B2B-vefsvæðum

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig stjórnendur geta bætt við, breytt og eytt notendum samstarfsaðila á rafrænum B2B-vefsvæðum.

Rafræn B2B-vefsvæði krefjast þess að fyrirtæki skrái sig til að gerast samstarfsaðilar. Þegar fyrirtæki sendir inn skráningarupplýsingar til rafræns B2B-vefsvæðið fer það í gegnum hæfnisferli. Ef fyrirtækið telst hæft er það tekið inn sem samstarfsaðili.

Þegar fyrirtæki hefur verið tekið inn sem samstarfsaðili verður fyrirtækisnotandinn, sem lagði fram beiðnina um að gerast samstarfsaðili, skilgreindur sem stjórnandi og fær réttindi til að taka inn fleiri heimilaða notendur af rafræna B2B-vefsvæðinu. Þessir heimiluðu notendur geta þá lagt fram pantanir fyrir hönd samstarfsaðilans.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>Kveikja á eiginleika rafrænna B2B-viðskiptamöguleika í Commerce Headquarters

Eiginleiki rafrænna B2B-viðskiptamöguleika í Commerce Headquarters gerir fyrirtækjum kleift að taka inn samstarfsaðila og skilgreina notendur sem stjórnendur. Þessi eiginleiki gerir stjórnendum einnig kleift að búa til og stjórna notendum og teymum samstarfsaðila og úthluta þeim ákveðnum hlutverkum. Að lokum gerir það notendum samstarfsaðila kleift að búa til pöntunarsniðmát og nota fyrirliggjandi pantanir til að endurpanta afurðir.

Til að kveikja á eiginleika rafrænna B2B-viðskiptamöguleika í Commerce Headquarters skal fylgja þessum skrefum.

1. Opna skal **Vinnusvæði \> Eiginleikastjórnun**.
1. Í flipanum **Allt** skal sía reitinn **Eining** með því að nota heitið **Smásala og viðskipti**.
1. Finnið og veljið eiginleikann sem kallast **Virkja notkun á rafrænum viðskiptamöguleikum milli fyrirtækja (B2B)** og veljið síðan **Virkja núna**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Búa til númeraröð og bæta henni við samnýttar viðskiptafæribreytur

Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kennimerki fyrir skýrslur aðalgagna og færslur sem krefjast kennimerkja. Nánari upplýsingar um númeraraðir er að finna í [Yfirlit númeraraða](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Til að búa til númeraröð og bæta henni við samnýttar viðskiptafæribreytur í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Númeraraðir \> Númeraraðir** og búið til númeraröð.
1. Opnið **Smásala og viðskipti \> Uppsetning höfuðstöðva \> Færibreytur \> Samnýttar viðskiptafæribreytur** og bætið nýju númeraröðinni við tilvísunina **Stigveldisauðkenni viðskiptavinar**.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Setja upp notanda sem stjórnanda fyrir nýjan samstarfsaðila

Mögulegir samstarfsaðilar geta hafið innleiðingarferlið í rafrænt B2B-vefsvæðið með því að senda inn beiðni um innleiðingu í gegnum tengil á svæðinu. Eftir að mögulegur notandi samstarfsaðila velur tengilinn getur hann gefið upp upplýsingarnar sem þarf til að vera tekinn inn og geta nýskráð sig. Þegar beiðnin hefur verið send inn birtist staðfestingarsíða innsendingar. Ef innsendingin er samþykkt verður beiðandinn (þ.e. notandinn sem hóf innleiðingarbeiðnina) að stjórnendanotanda samstarfsaðila.

Til að samþykkja og setja upp stjórnendanotanda samstarfsaðila í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Upplýsingatækni smásölu og viðskipta \> Dreifingaráætlun**.
1. Keyrið vinnsluna **P-0001** til að færa allar innleiðingarbeiðnir samstarfsaðila inn í Commerce Headquarters.
1. Þegar keyrslu vinnslunnar **P-0001** er lokið skal fara í **Upplýsingatækni smásölu og viðskipta \> Viðskiptavinur** og keyra vinnsluna **Samstilla viðskiptavini og viðskiptafélaga úr async-stillingu**. Þegar þessari vinnslu lýkur eru innleiðingarbeiðnirnar búnar til sem viðfangafærslur í Commerce Headquarters. Reiturinn **Kenni tegundar** fyrir þessar færslur er stiltlur á **B2B-viðföng**.
1. Farið í **Viðskiptavinir \> Öll viðföng** og opnið viðfangasíðuna.
1. Veljið viðfangafærslu nýja samstarfsaðilans til að opna upplýsingasíðu viðfangs.
1. Í flipanum **Almennt** skal velja **Breyta \> Samþykkja/hafna** til að samþykkja eða hafna innleiðingarbeiðninni. Þegar staðfestingarboð birtast skal staðfesta að halda eigi áfram með ferlið og samþykkja beiðnina. Tölvupóstur er síðan sendur á netfang beiðandans til að staðfesta að fyrirtæki hans hafi verið samþykkt sem samstarfsaðili.

    Þegar beiðnin er samþykkt er reiturinn **Staða** í viðfangafærslunni stilltur á **Samþykkt**. Auk þess eru tvær nýjar viðskiptavinafærslur stofnaðar í kerfinu: Viðskiptavinafærsla af **Gerð: Fyrirtæki** fyrir fyrirtæki samstarfsaðila og viðskiptavinafærsla af **Gerð: Einstaklingur** fyrir beiðandann. Stigveldisfærsla viðskiptavinar fyrir samstarfsaðilann er einnig stofnuð. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Farið í **Upplýsingatækni smásölu og viðskipta \> Dreifingaráætlun** og keyrið vinnsluna **1010** (**Viðskiptavinir**) til að færa nýlega stofnaða viðskiptavinafærslu og stigveldisfærslu viðskiptavinar í gagnagrunn rásarinnar.

Þegar beiðnin er samþykkt og viðskiptavinafærslan og stigveldisfærsla viðskiptavinar eru samstilltar við gagnagrunnsrásina, getur beiðandinn skráð sig inn á rafræna B2B-vefsvæðið með netfanginu sem hann gaf upp þegar hann sendin inn beiðnina. Notendur geta notað nýskráningarferlið til að stilla aðgangsorð fyrir reikninginn.

## <a name="onboard-additional-business-partner-users"></a>Fleiri notendur samstarfsaðila teknir inn

Notandi samstarfsaðila sem er stjórnandi getur tekið fleiri notendur samstarfsaðila inn á rafrænt B2B-vefsvæðið eftir þörfum.

Til að taka fleiri notendur samstarfsaðila inn á rafrænt B2B-vefsvæðið skal fylgja þessum skrefum.

1. Skráðu þig inn á rafræna B2B-vefsvæðið sem stjórnandi.
1. Farið í **Reikningurinn minn \> Notendur fyrirtækis \> Skoða upplýsingar** og veljið **Bæta við notanda**.
1. Færið inn nauðsynlegar upplýsingar og veljið **Vista**. Staða nýja notandans er stillt á **Í bið**.

    Þegar vinnslurnar **P-0001** og **Samstilla viðskiptavini og viðskiptafélaga úr async-stillingu** hafa verið keyrðar er viðskiptavinafærslan **Gerð: Einstaklingur** fyrir nýja notandann stofnuð í Commerce Headquarters. Þessi viðskiptavinafærsla tengist einnig viðeigandi stigveldisfærslu viðskiptavinar fyrir samstarfsaðilann. Auk þess er tölvupóstur sendur á netfang nýja notandans til að tilkynna honum að honum hafi verið bætt við sem notanda samstarfsaðilafyrirtækisins og geti nú skráð sig inn á rafræna B2B-vefsvæðið.

1. Keyrið vinnsluna **1010** (**Viðskiptavinir**) til að samstilla nýjan notanda samstarfsaðila við gagnagrunnsrásina.

Þegar færsla viðskiptavinar er samstillt er staða notandans á rafræna B2B-vefsvæðinu stillt á **Virkur** og nýi notandinn getur skráð sig inn á rafræna B2B-vefsvæðið með netfanginu sínu. Notendur geta notað nýskráningarferlið til að stilla aðgangsorð fyrir reikninginn.

## <a name="edit-business-partner-user-details"></a>Breyta notandaupplýsingum samstarfsaðila

Til að breyta upplýsingum um notendur samstarfsaðila skal fylgja þessum skrefum.

1. Skráðu þig inn á rafræna B2B-vefsvæðið sem stjórnandi.
1. Farið í **Reikningurinn minn \> Notendur fyrirtækis \> Skoða upplýsingar**, veljið hnappinn **Breyta** (blýantstákn), gerið nauðsynlegar breytingar og veljið síðan **Vista**. Breytingarnar taka aðeins gildi eftir að búið er að keyra verkin **P-0001**, **Samstilla viðskiptavini og viðskiptafélaga úr async-stillingu** og **1010** (**Viðskiptavinir**).

## <a name="remove-a-business-partner-user"></a>Fjarlægja notanda samstarfsaðila

Eins og þörf krefur getur stjórnandi fjarlægt núverandi notendur samstarfsaðilafyrirtækis af listanum yfir notendur sem hafa aðgang að rafræna B2B-vefsvæðinu.

Til að fjarlægja notanda samstarfsaðila skal fylgja þessum skrefum.

1. Skráðu þig inn á rafræna B2B-vefsvæðið sem stjórnandi.
1. Farið í **Reikningurinn minn \> Notendur fyrirtækis \> Skoða upplýsingar** og veljið hnappinn **Fjarlægja** („X“-táknið). Þegar staðfestingarboð birtist skal staðfesta að ætlunin sé að fjarlægja notandann. Breytingin tekur aðeins gildi eftir að búið er að keyra verkin **P-0001**, **Samstilla viðskiptavini og viðskiptafélaga úr async-stillingu** og **1010** (**Viðskiptavinir**).

> [!NOTE]
> Þegar notandi er fjarlægður af listanum yfir notendur sem hafa aðgang að rafræna B2B-vefsvæðinu, er samsvarandi viðskiptavinafærsla fjarlægð úr stigveldisfærslu viðskiptavinar fyrir samstarfsaðilann. Hins vegar er færslu viðskiptavinar ekki eytt úr Commerce Headquarters.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Taka inn samstarfsaðila og notendur í Commerce Headquarters

Stjórnendur geta tekið samstarfsaðila og notendur beint inn Commerce Headquarters.

Til að taka inn samstarfsaðila og notendur í Commerce Headquarters skal fylgja þessum skrefum.

1. Stofnið viðskiptavinafærsluna **Gerð: Fyrirtæki** fyrir fyrirtæki samstarfsaðilans.
1. Stofnið viðskiptavinafærslurnar **Gerð: Einstaklingur** fyrir notendur samstarfsaðilans. Gangið úr skugga um að aðalnetfang sé tilgreint fyrir hvern viðskiptavin.
1. Fyrir hverja viðskiptavinafærslu af **Gerð: Einstaklingur** sem þarf að gera að stjórnanda samstarfsaðilafyrirtækisins, í flýtiflipanum **Smásala**, skal stilla valkostinn **B2B-stjórnandi** á **Já**.
1. Stofnið stigveldisauðkenni viðskiptavinar. Færið inn lýsandi nafn í reitinn **Heiti**.
1. Í reitinn **Fyrirtæki** skal færa inn viðskiptavin samstarfsaðilafyrirtækisins.
1. Veljið **Bæta við** og veljið síðan viðskiptavin í reitnum **Heiti**.
1. Endurtakið þetta ferli til að bæta fleiri viðskiptavinum við stigveldið.

## <a name="additional-information"></a>Frekari upplýsingar

- Hægt er að skilgreina öll verk sem eru nefnd eru í þessu efnisatriði til að keyra áætlun á runusniði. Búist er við að samstarfsaðilar muni skilgreina runuvinnslur eftir þörfum.
- Sem stendur getur aðeins einn notandi/viðskiptavinafærsla verið stjórnandi og aðeins er hægt að breyta hlutverkinu í Commerce Headquarters. Enginn stuðningur er fyrir sjálfsafgreiðslumöguleika sem gerir samstarfsaðilum kleift að velja marga stjórnendur eða breyta stjórnendum úr rafrænum B2B-vefsvæðum.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Þótt hægt sé að skilgreina eyðsluþak fyrir notendur, hefur framfylgni eyðsluþaks í ferli pöntunarfærslunnar ekki enn verið innleidd.
- Allur viðskiptagrunnur og villuleit fyrir upplifun notanda á rafrænu B2B-vefsvæði byggist á skilgreiningu viðskiptavinafærslunnar sem er varpað á notandann í Commerce Headquarters.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2B-svæði fyrir rafræn viðskipti](set-up-b2b-site.md)

[Stofna líkanastigveldi fyrir B2B-fyrirtæki](org-model.md)

[Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti](payment-method.md)

[Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði](quantity-limits.md)

[Yfirlit númeraraða](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)
