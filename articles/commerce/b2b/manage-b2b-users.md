---
title: Stjórna notendum samstarfsaðila á rafrænum B2B-vefsvæðum
description: Þessi grein lýsir því hvernig á að bæta við, eyða og breyta notendum viðskiptafélaga á Microsoft Dynamics 365 Commerce viðskipti á milli fyrirtækja (B2B) netviðskiptavefsíður og í höfuðstöðvum viðskipta.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4a3d1c7bf7e7ea545590315d9e185fa525b5d5e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860296"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Stjórna notendum samstarfsaðila á rafrænum B2B-vefsvæðum

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að bæta við, eyða og breyta notendum viðskiptafélaga á Microsoft Dynamics 365 Commerce viðskipti á milli fyrirtækja (B2B) netviðskiptavefsíður og í höfuðstöðvum viðskipta.

> [!NOTE]
> - The [Stjórna B2B viðskiptafélögum með því að nota stigveldi viðskiptavina](partners-customer-hierarchies.md) grein er forsenda þessa skjals.
> - Gakktu úr skugga um að þú frumstillir einingu skjalategunda í höfuðstöðvum Commerce með því að opna **Skjalagerðir** form kl **Stjórn stofnunarinnar \> Skjalastjórnun \> Skjalagerðir**.

Rafræn B2B-vefsvæði krefjast þess að fyrirtæki skrái sig til að gerast samstarfsaðilar. Eftir að stofnun hefur sent skráningarupplýsingar á B2B rafræn viðskipti vefsíðu fer skráningarbeiðnin í gegnum hæfisferli. Ef fyrirtækið telst hæft er það tekið inn sem samstarfsaðili.

Þegar fyrirtæki hefur verið tekið inn sem samstarfsaðili verður fyrirtækisnotandinn, sem lagði fram beiðnina um að gerast samstarfsaðili, skilgreindur sem stjórnandi og fær réttindi til að taka inn fleiri heimilaða notendur af rafræna B2B-vefsvæðinu. Þessir heimiluðu notendur geta þá lagt fram pantanir fyrir hönd samstarfsaðilans.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Setja upp notanda sem stjórnanda fyrir nýjan samstarfsaðila

Hugsanlegir viðskiptafélagar geta hafið inngönguferlið á B2B rafræn viðskipti vefsíðu með því að senda inn beiðni um borð í gegnum hlekk á B2B vefsíðunni. Þeir geta síðan notað sérhannaðar eyðublaðið til að veita upplýsingarnar sem eru nauðsynlegar fyrir inngöngu og skráningu. Þegar beiðnin hefur verið send inn birtist staðfestingarsíða innsendingar. Ef innsendingin er samþykkt verður fyrirtækið sem beiðnin var send fyrir viðskiptafélagi og beiðandinn (notandinn sem hóf inngöngubeiðnina) verður stjórnandi notandi viðskiptafélaga.

Til að samþykkja beiðni viðskiptafélaga í höfuðstöðvum Commerce skaltu fylgja þessum skrefum.

1. Farið í **Upplýsingatækni smásölu og viðskipta \> Dreifingaráætlun**.
1. Keyrið vinnsluna **P-0001** til að færa allar innleiðingarbeiðnir samstarfsaðila inn í Commerce Headquarters.
1. Eftir **P-0001** starf hefur gengið vel, farðu til **Upplýsingatækni í smásölu og viðskiptum \> Viðskiptavinur**, og keyra **Samstilltu viðskiptavini og rásbeiðnir** starf. Eftir að þetta starf hefur keyrt með góðum árangri eru inngöngubeiðnirnar búnar til sem möguleikar á **B2B möguleiki** tegund í höfuðstöðvum viðskipta. 
1. Fara til **Viðskiptavinir \> Allar horfur**, og veldu færslu tilvonandi viðskiptafélaga til að opna upplýsingasíðu viðskiptavinarins.
1. Á **Almennt** flipa, veldu **Umbreyta \> Samþykkja/hafna** til að samþykkja beiðni um inngöngu. Þegar staðfestingarskilaboðin birtast skaltu staðfesta að þú viljir halda áfram með ferlið og samþykkja síðan beiðnina. Samþykkið breytir **Staða** sviði horfur skrá til **Samþykkt**. Tölvupóstur er síðan sendur á netfang beiðandans til að staðfesta að fyrirtæki hans hafi verið samþykkt sem samstarfsaðili. Einnig er stofnað stigveldi viðskiptavina þar sem beiðanda er bætt við sem stjórnanda fyrir viðskiptafélaga.

    > [!NOTE]
    > Eins og er er staðfestingarpósturinn sendur strax við samþykki. Hins vegar mun framtíðarviðskiptavirkni gera stjórnanda kleift að kveikja handvirkt á tölvupóstunum.

1. Fara til **Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**, og keyra **1010 (Viðskiptavinir)** starf til að ýta nýjum viðskiptamanna- og stigveldisskrám viðskiptavina í rásargagnagrunninn.

> [!NOTE]
> Til að tryggja að nýju viðskiptamannafærslurnar séu sendar í rásargagnagrunninn ætti að minnsta kosti ein af heimilisfangabókunum sem eru tengdar viðskiptavininum að vera með í heimilisfangaskrá viðskiptavinarins sem tengist netversluninni. Hægt er að gera þetta ferli sjálfvirkt með því að stilla heimilisfangaskrána á sjálfgefna viðskiptavinum netverslunarinnar þannig að kerfið afritar gildi heimilisfangabókar til hvers nýs viðskiptamanns.

Eftir að stigveldisskrár viðskiptavina hafa verið samstilltar við rásargagnagrunninn getur umsækjandinn skráð sig inn á B2B rafræn viðskipti vefsíðu með því að nota netfangið sem hann gaf upp þegar þeir sendu inn beiðni um inngöngu. Notendur geta notað nýskráningarferlið til að stilla aðgangsorð fyrir reikninginn. Fyrir upplýsingar um hvernig á að virkja Azure Active Directory (Azure AD) Skráning B2C auðkennisveitu til að tengja við B2B viðskiptamannaskrána sem var búin til við samþykki viðskiptavinar, sjá [Virkja sjálfvirka tengingu](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Tilkynna B2B-viðföngum þegar þau eru samþykkt eða þeim hafnað

Þegar þú samþykkir eða hafnar beiðni um inngöngu í B2B tilvonandi um borð, er hægt að senda tölvupósttilkynningu sjálfkrafa til viðskiptavinarins.

Til að setja upp tölvupósttilkynningar í höfuðstöðvum Commerce fyrir viðburði í **B2B tilboð samþykkt** eða **B2B tilboði hafnað** tegund tilkynninga skaltu fylgja þessum skrefum.

1. Búðu til tölvupóstsniðmát fyrir tölvupóst sem verða send til viðskiptavina þegar annað hvort **B2B tilboð samþykkt** eða **B2B tilboði hafnað** tegund tilkynninga er ræst. Fyrir upplýsingar um staðgengla sem þessar tilkynningagerðir styðja, sjá [Tegundir tilkynninga](../email-templates-transactions.md#notification-types). Frekari upplýsingar um hvernig á að búa til sniðmát fyrir tölvupóst skal skoða [Stofna sniðmát fyrir tölvupóst](../email-templates-transactions.md#create-an-email-template).
1. Bætið við **B2B tilboð samþykkt** og **B2B tilboði hafnað** tilkynningategundir yfir á tilkynningasniðið í tölvupósti og varpa þeim síðan við tölvupóstsniðmátin sem þú bjóst til. Frekari upplýsingar um forstillingar tilkynninga er að finna í [Setja upp forstillingu tilkynningar í tölvupósti](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Fleiri notendur samstarfsaðila teknir inn

Notandi samstarfsaðila sem er stjórnandi getur tekið fleiri notendur samstarfsaðila inn á rafrænt B2B-vefsvæðið eftir þörfum.

Til að taka fleiri notendur samstarfsaðila inn á rafrænt B2B-vefsvæðið skal fylgja þessum skrefum.

1. Skráðu þig inn á rafræna B2B-vefsvæðið sem stjórnandi.
1. Farið í **Reikningurinn minn \> Notendur fyrirtækis \> Skoða upplýsingar** og veljið **Bæta við notanda**.
1. Færið inn nauðsynlegar upplýsingar og veljið **Vista**. Staða nýja notandans er stillt á **Í bið**.

Eftir **P-0001** og **Samstilltu viðskiptavini og rásbeiðnir** störf hafa verið keyrð, viðskiptavinur skrá yfir **Persóna** gerð er búin til fyrir nýja notandann í höfuðstöðvum Commerce. Þessi viðskiptavinafærsla tengist einnig viðeigandi stigveldisfærslu viðskiptavinar fyrir samstarfsaðilann. Auk þess er tölvupóstur sendur á netfang nýja notandans til að tilkynna honum að honum hafi verið bætt við sem notanda samstarfsaðilafyrirtækisins og geti nú skráð sig inn á rafræna B2B-vefsvæðið.

Næst skaltu keyra **1010 (Viðskiptavinir)** starf til að samstilla nýja viðskiptafélaga notandann við rásargagnagrunninn.

Eftir að viðskiptamannaskráin er samstillt er staða notandans á B2B rafrænum verslunarvefnum stillt á **Virkur**, og nýi notandinn getur skráð sig inn á B2B rafræn viðskipti vefsíðu með því að nota netfangið sitt. Notendur geta notað nýskráningarferlið til að stilla aðgangsorð fyrir reikninginn. Fyrir upplýsingar um hvernig á að virkja Azure AD Skráning B2C auðkennisveitu sem á að tengja við B2B viðskiptamannaskrá sem var búin til í höfuðstöðvum Commerce, sjá [Virkja sjálfvirka tengingu](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Breyta notandaupplýsingum samstarfsaðila

Til að breyta upplýsingum um notendur samstarfsaðila skal fylgja þessum skrefum.

1. Skráðu þig inn á rafræna B2B-vefsvæðið sem stjórnandi.
1. Farið í **Reikningurinn minn \> Notendur fyrirtækis \> Skoða upplýsingar**, veljið hnappinn **Breyta** (blýantstákn), gerið nauðsynlegar breytingar og veljið síðan **Vista**. Breytingarnar taka aðeins gildi eftir að **P-0001**, **viðskiptavini og rásbeiðnir**, og **1010 (Viðskiptavinir)** störf hafa verið rekin.

## <a name="remove-a-business-partner-user"></a>Fjarlægja notanda samstarfsaðila

Eins og þörf krefur getur stjórnandi fjarlægt núverandi notendur samstarfsaðilafyrirtækis af listanum yfir notendur sem hafa aðgang að rafræna B2B-vefsvæðinu.
Til að fjarlægja notanda samstarfsaðila skal fylgja þessum skrefum.
- Skráðu þig inn á rafræna B2B-vefsvæðið sem stjórnandi.
- Fara til **Reikningurinn minn > Notendur stofnunar \> Skoða smáatriði**, og veldu **Fjarlægja** hnappinn ("X" tákn). Þegar staðfestingarboð birtist skal staðfesta að ætlunin sé að fjarlægja notandann. Breytingin tekur aðeins gildi eftir að **P-0001**, **viðskiptavini og rásbeiðnir**, og **1010 (Viðskiptavinir)** störf hafa verið rekin.

> [!NOTE]
> Þegar notandi er fjarlægður af listanum yfir notendur sem hafa aðgang að rafræna B2B-vefsvæðinu, er samsvarandi viðskiptavinafærsla fjarlægð úr stigveldisfærslu viðskiptavinar fyrir samstarfsaðilann. Hins vegar er færslu viðskiptavinar ekki eytt úr Commerce Headquarters.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Um borð í núverandi viðskiptavinum sem viðskiptafélagar á vef B2B rafrænna viðskipta

Stjórnendur geta tekið samstarfsaðila og notendur beint inn Commerce Headquarters. Þessi möguleiki er gagnlegur til að setja núverandi viðskiptafélaga þína um borð á B2B rafræn viðskipti vefsíðu.

Til að taka inn samstarfsaðila og notendur í Commerce Headquarters skal fylgja þessum skrefum.

1. Búðu til eða veldu viðskiptavin í **Skipulag** tegund til að bæta við sem viðskiptafélaga.
1. Búðu til eða veldu viðskiptavin í **Persóna** tegund til að bæta við sem stjórnanda eða notanda fyrir viðskiptafélaga. Gakktu úr skugga um að aðalnetföng séu tengd viðskiptavinum. Þessi netföng eru notuð til að skrá þig inn á vefsíðuna. 

    > [!NOTE]
    > Kerfið verður að geta fundið einstakt viðskiptavinaskrá fyrir notendur sem ættu að geta skráð sig inn á vefsíðuna. Ef kerfið finnur fleiri en einn viðskiptavin sem hefur sama aðalnetfangið í lögaðilanum mun notandinn ekki geta skráð sig inn á vefsíðuna.

1. Stofnið stigveldisauðkenni viðskiptavinar.
1. Færið inn lýsandi nafn í reitinn **Heiti**.
1. Í reitinn **Fyrirtæki** skal færa inn viðskiptavin samstarfsaðilafyrirtækisins.
1. Á **Stigveldi** Flýtiflipi, veldu **Bæta við**.
1. Í **Nafn** reit, veldu viðskiptavin í **Persóna** tegund.
1. Veldu **Admin** hlutverk fyrir viðskiptavininn sem ætti að vera tilnefndur sem stjórnandi.
1. Endurtaktu þetta ferli til að bæta fleiri viðskiptavinum við stigveldið.

## <a name="additional-information"></a>Viðbótarupplýsingar

- Hægt er að stilla öll störf sem nefnd eru í þessari grein til að keyra á áætlun í runusniði. Búist er við að samstarfsaðilar muni skilgreina runuvinnslur eftir þörfum.
- Sem stendur getur aðeins einn notandi/viðskiptavinafærsla verið stjórnandi og aðeins er hægt að breyta hlutverkinu í Commerce Headquarters. Enginn stuðningur er fyrir sjálfsafgreiðslumöguleika sem gerir samstarfsaðilum kleift að velja marga stjórnendur eða breyta stjórnendum úr rafrænum B2B-vefsvæðum.
- Þótt hægt sé að skilgreina eyðsluþak fyrir notendur, hefur framfylgni eyðsluþaks í ferli pöntunarfærslunnar ekki enn verið innleidd.
- Allur viðskiptagrunnur og villuleit fyrir upplifun notanda á rafrænu B2B-vefsvæði byggist á skilgreiningu viðskiptavinafærslunnar sem er varpað á notandann í Commerce Headquarters.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2B-svæði fyrir rafræn viðskipti](set-up-b2b-site.md)

[Stjórna B2B-viðskiptafélögum með því að nota stigveldi viðskiptavina](partners-customer-hierarchies.md)

[Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti](payment-method.md)

[Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði](quantity-limits.md)

[Yfirlit númeraraða](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
