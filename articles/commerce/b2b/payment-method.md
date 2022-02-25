---
title: Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti
description: Þetta efnisatriði lýsir því hvernig á að stilla greiðslumáta viðskiptavinareiknings í Microsoft Dynamics 365 Commerce. Það lýsir einnig hvernig lánamörk hafa áhrif á greiðsluupptöku á reikningi á netviðskiptasíðum fyrirtækja til fyrirtækja (B2B).
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0366f7b51ac138cc7305f98d5607c554440e6d34
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323356"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að stilla greiðslumáta viðskiptavinareiknings í Microsoft Dynamics 365 Commerce. Það lýsir einnig hvernig lánamörk hafa áhrif á greiðsluupptöku á reikningi á netviðskiptasíðum fyrirtækja til fyrirtækja (B2B).

Smásalar geta tekið við ýmsum gerðum af greiðslum í staðinn fyrir afurðir og þjónustu sem þeir selja í rás rafrænna viðskipta. Hver greiðslugerð sem smásali samþykkir verður að vera skilgreind í Dynamics 365 Commerce þegar kerfið er sett upp. Greiðslumáti viðskiptavinareiknings (eða „á reikning“) verður að vera studdur á B2B rafrænum viðskiptasíðum. 

## <a name="prerequisites"></a>Forkröfur

1. Bætið greiðslumáta viðskiptavinalykils við Commerce Headquarters.
2. Tengið greiðslumáta viðskiptavinalykils við rás rafrænna viðskipta.
3. Gakktu úr skugga um að **Leyfa á reikningi** eign er virkjuð fyrir viðskiptavini á **Verslun og verslun \> Viðskiptavinir \> Allir viðskiptavinir \> Vanskil greiðslur** í höfuðstöðvum viðskipta.

    > [!NOTE]
    > Ef allir viðskiptavinir ættu að hafa leyfi til að hafa greiðslumáta á reikningi virkan geturðu stillt **Leyfa á reikningi** eign til **Já** fyrir sjálfgefinn viðskiptavin rásarinnar sem tengist B2B síðunni. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Virkja greiðslumáta fyrir viðskiptavinalykil í Commerce Site Builder 

Til að virkja greiðslumáta fyrir viðskiptavinalykil í Commerce Site Builder skal fylgja þessum skrefum.

1. Farið í **Svæðisstillingar \> Viðbætur**.
1. Stillið eiginleikann **Virkja greiðslur viðskiptavinalykils** á **Virkjað fyrir B2B-viðskiptavini**. 
1. Veldur **Vista og birta**.

> [!NOTE]
> Nýjar svæðisstillingar taka gildi aðeins eftir að búið er að uppfæra skrána app.settings.json. Frekari upplýsingar er að finna í [Uppfærslur á SDK og einingasafni](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Virkja greiðslumáta fyrir viðskiptavinalykil á greiðslusíðu fyrir B2B-svæði rafrænna viðskipta

Til að virkja greiðslumáta viðskiptavinalykils á greiðslusíðunni fyrir B2B-svæði rafrænna viðskipta skal fylgja þessum skrefum.

1. Í Commerce Site Builder skal finna og breyta greiðslusíðunni eða brotinu sem inniheldur greiðslueininguna fyrir B2B-svæði rafrænna viðskipta.
1. Í raufinni **Hólf greiðsluferlishluta** skal velja **Bæta við einingu** og síðan bæta við einingu **Greiðsla með viðskiptavinalykli**.
1. Staðsetjið eininguna **Greiðsla með viðskiptavinalykli** með því að velja úrfellingarmerkið (**...**) og veljið síðan **Færa upp** eða **Færa niður** eftir þörfum.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Staðfesta að greiðslumáti viðskiptavinalykils hafi verið virkjaður og gefin út

Til að staðfesta að greiðslumáti viðskiptavinalykils hafi verið gerður virkur skal fylgja þessum skrefum.

1. Skráðu þig inn á svæði rafrænna viðskipta.
1. Bætið afurð við körfuna.
1. Farið á síðu greiðsluferlis. Þar ætti að sjást nýi greiðslumáti **Viðskiptavinalykils**.

## <a name="work-with-credit-limits"></a>Vinna með lánamörk

Þegar möguleiki fyrir greiðslur viðskiptavinareikninga er virkjaður á B2B-síðunni, vilja stofnanir venjulega sýna upplýsingar um lánamörk og inneignir á lánamörkum meðan á pöntunartökuferlinu stendur. Lánsfjármörk viðskiptavina eru skilgreind af **Lánamörk** eign á **Inneign og innheimtur** Flýtiflipi viðskiptavinaskrár í höfuðstöðvum Commerce. Hins vegar, í B2B atburðarás, ætti pöntun sem viðskiptavinur setur oft að vera reikningsfærð á reikning fyrirtækisins sem viðskiptavinurinn tilheyrir. Þess vegna verður þú að stilla **Reikningsreikningur** eign á **Reikningur og afhending** Flýtiflipi viðskiptavinaskrárinnar yfir á auðkenni viðskiptavinareiknings fyrirtækisins. Síðan, þegar viðskiptavinurinn leggur inn pöntun á B2B síðunni, verður pöntunin reikningsfærð til fyrirtækisins. B2B-síðan mun einnig nota lánsfjárhámark stofnunarinnar í stað lánsfjárhámarksins sem er skilgreint á viðskiptaskrá.

Útreikningur á lánamörkum og stöðu sem sýnd er á B2B vefsíðunni fer eftir stillingu **Tegund lánahámarks** eign í höfuðstöðvum Commerce. Staðsetning þessarar eignar er mismunandi eftir því hvort **Útlánastjórnun** eiginleiki er virkur í **Eiginleikastjórnun** vinnusvæði:

- Ef **Útlánastjórnun** eiginleiki er virkur, eignin er staðsett á **Lánamörk** Hraðflipi kl **Inneign og innheimtur \> Uppsetning \> Inneign og innheimtufæribreytur \> Inneign**. 
- Ef **Útlánastjórnun** eiginleiki er óvirkur, eignin er staðsett undir **Lánshæfismat** kl **Reikningur fáanlegur \> Uppsetning \> Færibreytur viðskiptakrafna \> Lánshæfismat**.

Gildin sem **Tegund lánahámarks** eignastoðir eru **Enginn**, **·**, **+ fylgiseðill eða vörukvittun**, og **Jafnvægi + Allt**. Fyrir frekari upplýsingar um þessi gildi, sjá [Tegundargildi lánamarka](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Við mælum með að þú stillir **Tegund lánahámarks** eign til **Staða + fylgiseðill eða vöruseðill**, þannig að opnar sölupantanir leggi ekki sitt af mörkum til útreiknings á stöðunni. Síðan, ef viðskiptavinir þínir leggja inn framtíðarpantanir, þurfa þeir ekki að hafa áhyggjur af því að þessar pantanir hafi áhrif á núverandi stöðu þeirra.

Önnur eign sem hefur áhrif á pöntun á reikningi er **Lögboðið lánamörk** eign, sem er staðsett á **Inneign og innheimtur** Flýtiflipi viðskiptavinaskrárinnar. Með því að stilla þessa eign á **Já** fyrir tiltekna viðskiptavini, getur þú þvingað kerfið til að athuga lánshæfismat þeirra, jafnvel þótt **Tegund lánahámarks** eign hefur verið stillt á **Enginn** til að tilgreina að ekki skuli athuga lánamörk fyrir neinn viðskiptavin.

Eins og er, B2B síður þar sem **Lögboðið lánamörk** eign er virkjuð hafa viðbótarvirkni. Ef eignin er virkjuð á viðskiptaskrá, þegar viðskiptavinurinn leggur inn pöntun, kemur B2B síðan í veg fyrir að hann noti greiðslumáta á reikningi til að greiða meira en eftirstöðvar inneignar. Til dæmis, ef eftirstandandi inneign viðskiptavinarins er $1,000, en pöntunin er virði $1,200, getur viðskiptavinurinn aðeins greitt $1,000 með því að nota inneignaraðferðina. Þeir verða að nota einhvern annan greiðslumáta til að greiða eftirstöðvarnar. Ef **Lögboðið lánamörk** eign er óvirk á skrá viðskiptavinar getur viðskiptavinurinn greitt hvaða upphæð sem er með því að nota inneignargreiðslumáta. Hins vegar, jafnvel þó að viðskiptavinur geti lagt inn pantanir, mun kerfið ekki leyfa þessum pöntunum að vera uppfylltar ef þær fara yfir lánahámarkið. Ef þú verður að athuga lánamörk allra viðskiptavina sem eiga rétt á greiðslum á reikningi, mælum við með að þú stillir **Tegund lánahámarks** eign til **Staða + fylgiseðill eða vöruseðill** og **Lögboðið lánahámark** eign til **Nei**.

The **Inneign og innheimtur** mát hefur nýja möguleika á lánastjórnun. Til að kveikja á þessum eiginleikum skaltu virkja **Útlánastjórnun** eiginleiki í **Eiginleikastjórnun** vinnurými. Einn af nýju möguleikunum gerir kleift að setja sölupantanir í bið á grundvelli blokkunarreglna. Persóna lánastjórans getur síðan sleppt eða hafnað pöntunum eftir frekari greiningu. Hins vegar, möguleikinn til að setja sölupantanir í bið á ekki við um viðskiptapantanir, vegna þess að sölupantanir eru oft með fyrirframgreiðslu og **Útlánastjórnun** eiginleiki styður ekki alveg fyrirframgreiðsluaðstæður. 

Burtséð frá því hvort **Útlánastjórnun** eiginleiki er virkjaður, ef inneign viðskiptavina fer yfir lánsfjárhámarkið meðan á pöntun stendur, fara sölupantanir ekki í bið. Þess í stað mun Commerce búa til annað hvort viðvörunarskilaboð eða villuboð, allt eftir gildi **Skilaboð þegar farið er yfir lánamörk** sviði á **Lánamörk** Flýtiflipi.

The **Útiloka frá lánastýringu** eign sem kemur í veg fyrir að Commerce sölupantanir haldist í bið er staðsett á sölupöntunarhaus (**Verslun og verslun \> Viðskiptavinir \> Allar sölupantanir**). Ef þessi eign er stillt á **Já** (sjálfgefið gildi) fyrir Commerce sölupantanir, pantanir verða útilokaðar frá biðvinnuflæði lánastýringar. Athugið að þó að eignin sé nefnd **Útiloka frá lánastýringu**, skilgreint lánsfjárhámark verður enn notað meðan á pöntun stendur. Pantanir fara bara ekki í bið.

Möguleikinn á að setja Commerce sölupantanir í bið á grundvelli blokkunarreglna er fyrirhuguð fyrir Commerce útgáfur í framtíðinni. Þangað til það er stutt, ef þú verður að þvinga Commerce sölupantanir til að fara í gegnum nýju lánastýringarflæðið, geturðu sérsniðið eftirfarandi XML skrár í Visual Studio lausn. Í skránum skaltu breyta rökfræðinni þannig að **CredManExcludeSalesOrder** fáninn er stilltur á **Nei**. Á þennan hátt er **Útiloka frá lánastýringu** eign verður stillt á **Nei** sjálfgefið fyrir Commerce sölupantanir.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

Athugaðu að ef **CredManExcludeSalesOrder** fáninn er stilltur á **Nei**, og B2B viðskiptavinur getur keypt í verslunum með því að nota sölustað (POS) forritið, bókun á reiðufé og flutningsfærslum gæti mistekist. Til dæmis er lokunarregla á tegund reiðufjárgreiðslu og viðskiptavinur B2B keypti suma hluti í versluninni með því að nota reiðufé. Í þessu tilviki verður sölupöntunin sem myndast ekki reikningsfærð vegna þess að hún verður í biðstöðu. Þess vegna mun pósturinn mistakast. Af þessum sökum mælum við með því að þú gerir end-to-end prófun eftir að þú hefur innleitt þessa aðlögun.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2B-svæði fyrir rafræn viðskipti](set-up-b2b-site.md)

[Stjórna B2B viðskiptafélögum með því að nota stigveldi viðskiptavina](partners-customer-hierarchies.md)

[Stjórna notendum viðskiptafélaga á B2B svæði fyrir rafræn viðskipti](manage-b2b-users.md)

[Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði](quantity-limits.md)

[Uppfærslur á SDK og kjarnasafni](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
