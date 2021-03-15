---
title: Virkja og nota deilingu milli rása
description: Þetta efnisatriði lýsir því hvernig á að virkja og nota samnýtingareiginleika milli rása í vefsmið Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3990365dda0a0cff7adcc1d97120293d43f6e858
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973132"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Virkja og nota deilingu milli rása

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að virkja og nota samnýtingareiginleika milli rása í vefsmið Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Samnýting milli rása gerir söluaðilum kleift að endurnýta og samnýta efni á mörgum rásum svæðis. Þessi möguleiki er gagnlegur þegar rásir svæða eru með samhæft grunntungumál eða þegar þær eru með ýmislegt sameiginlegt efni.

Samnýting milli rása virkar með því að virkja sjálfgefna rás sem verður leitað að tiltæku efni í þegar útgáfa ákveðinnar rásar af umbeðnu efni finnst ekki. Efni sem fyrirhugað er að deila á milli rása er búið til í sjálfgefnu rásinni. Hægt er að staðsetja efnið á hvaða staðsetningu sem er sem notuð er á hvaða rás svæðis sem er.

## <a name="when-to-use-cross-channel-sharing"></a>Hvernig skal nota deilingu milli rása

Deiling milli rása er gagnleg þegar margar rásir á einu svæði geta deilt efni. Til dæmis getur smásali sem er með mörg vörumerki og netverslanir sem flokkað er undir einu svæði deilt sumu efni á milli sumra eða allra netverslananna. Þetta samnýtta efni getur innihaldið síður fyrir skilmála, greiðsluskilmála, afhendingarmáta og algengar spurningar.

Deiling milli rása styður einnig brot. Þess vegna er hægt að búa til efnissíðu sem inniheldur brot ákveðinna rásar sem efni milli rása. Í slíku tilfelli, þótt meirihluta efnisins verði deilt á milli rása, verða brot fyrir rásir á síðu milli rása aðeins búin til þegar óskaði er eftir þeim úr samsvarandi rás netverslunar.

Svæði sem hafa aðeins eina rás, eða svæði sem eru með margar rásir sem geta ekki deilt efni, hafa engan ávinning af deilingu milli rása.

## <a name="enable-cross-channel-sharing"></a>Virkja deilingu milli rása

Samnýting milli rása er virk á svæðisstigi. Þessi aðgerð gildir í eina átt. Með öðrum orðum, eftir að samnýting milli rása er virkjuð er ekki hægt að gera hana óvirka.

Til að virkja samnýtingu milli rása í vefsmið Commerce skal fylgja þessum skrefum.

1. Farið í **Svæðisstillingar \> Eiginleikar**.
1. Stillið valkostinn fyrir eiginleikann **Milli rása** á **Kveikt**.

    ![Kveikt á valkosti milli rása í vefsmið Commerce](./media/enabling-cross-channel-sharing.png)

Þegar deiling milli rása er virkjuð, birtast upplýsingar um millirásir í hlutanum **Rásir** í **Svæðisstillingar \> Eiginleikar** eins og dæmið í eftirfarandi mynd sýnir.

![Upplýsingar um rásir sýnilegar eftir að samnýting milli rása er virkjuð](./media/channels-cross-channel.png)

Að auki, þegar búið er að virkja samnýtingu milli rása, verður reiturinn **Rás** uppi hægra megin í vefsmið Commerce með valkostinn **Netverslun milli rása** sem hægt er að nota til að stjórna efni milli rása eins og sýnt er í eftirfarandi mynd.

![Valkostur netverslunar milli rása í reit rásar þegar deiling milli rása hefur verið virkjuð](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Búa til og nota efni milli rása

Hægt er að búa til og nota efni milli rása á margan hátt. Til dæmis er hægt að búa til brot milli rása, búa til síður milli rása sem nota efni milli rása og efni fyrir ákveðna rás, og skrifa yfir brot milli rása með útgáfum rása fyrir brot.

### <a name="create-a-cross-channel-fragment"></a>Búa til brot milli rása

Til að búa til brot milli rása í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.
1. Í svarglugganum **Nýtt brot** skal velja eininguna **Tilboðsborði** og síðan undir **Heiti brots** skal færa inn heiti (t.d. **Borði milli rása**). Veljið síðan **Í lagi**.
1. Á eiginleikasvæðinu fyrir eininguna **Tilboðsborði** skal velja **Bæta skilaboðum við** og síðan velja **Skilaboð**.
1. Í svarglugganum **Skilaboð**, undir **Texti**, skal færa inn **Milli rása** og síðan velja **Í lagi**. 
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

Hægt er að nota þetta brot milli rása fyrir síður milli rása eða tiltekna síðu sem eru búnar til í hvaða rás svæðis sem er.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Búa til síðu milli rása sem notar efni milli rása

Hægt er að nota síður milli rása á hvaða rás sem er á svæðinu þínu. Þess vegna er hægt að búa til samnýtta efnissíðu einu sinni og gera allar uppfærslur á einum staðnum. Til dæmis er hægt að deila millirásarsíðunni **Skilmálar** sem er með vefslóðina `/toc` með öllum rásum svæðisins. Ef grunnvefslóðir fyrir rásir vefsvæðis eru `www.fabrikam.com/brand1` og `www.fabrikam.com/brand2`, sama millirásin, verður samnýtta síðan **Skilmálar** tiltæk frá báðum vefslóðum rásar vefsvæðis, á `www.fabrikam.com/brand1/toc` og `www.fabrikam.com/brand2/toc`. Ef þarf að uppfæra síðuna **Skilmálar** seinna meir, þarf aðeins að uppfæra samnýttu síðuna.

Til að búa til síðu milli rása í Commerce-vefsmið sem notar efni milli rása skal fylgja þessum skrefum.

1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í svarglugganum **Velja sniðmát** skal velja sniðmát eins og **Markaðssetning**.
1. Undir **Síðuheiti** skal færa inn heiti fyrir síðuna (til dæmis **Millirásarsíða**).
1. Undir **Vefslóð síðu** skal færa inn vefslóð síðu (t.d. **examplepage**) og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við broti**.
1. Í svarglugganum **Bæta við broti** skal velja brot milli rásar sem var áður búið til og er með tilboðsborða og velja síðan **Í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Þú ættir að sjá tilboðsborðann sem á stendur „Milli rása“.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Búa til síðu fyrir rás sem notar efni milli rása

Með því að nota efni milli rása á síðu rásar er hægt að búa til samnýtt efnisbrot í eitt skipti og síðan nota það í síðum rása. Þessi „staki gagnauppruni“ er gagnlegur fyrir samnýtt efni á borð við skilmála, greiðsluskilmála eða samskiptaupplýsingar.

Til að búa til síðu rásar í Commerce-vefsmið sem notar efni milli rása skal fylgja þessum skrefum.

1. Innan tiltekinnar rásar, t.d. **Stækkuð Fabrikam netverslun** skal fara í **Síður** og síðan velja **Ný** til að búa til nýja síðu.
1. Í svarglugganum **Velja sniðmát** skal velja sniðmát eins og **Markaðssetning**.
1. Undir **Síðuheiti** skal færa inn heiti fyrir síðuna (til dæmis **Síða rásar**).
1. Undir **Vefslóð síðu** skal færa inn vefslóð síðu (t.d. **channelspecificpage**) og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við broti**.
1. Í svarglugganum **Bæta við broti**, undir **Rás**, skal velja **Netverslun milli rása**. Brotið milli rása sem búið var til hér á undan ætti að birtast í listanum. Veljið það og veljið síðan **Í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Þú ættir að sjá tilboðsborðann sem á stendur „Milli rása“.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Búa til útgáfu tiltekinnar rásar fyrir síðu milli rása

Samnýting milli rása styður hnekkingu á efni milli rása. Til dæmis deila allar nema ein rás vefsvæðis sama efninu. Þessi rás eins vefsvæðis þarfnast annars efnis. Til að innleiða mismunandi efni fyrir hana, er millirásarefni hnekkt með efni tiltekinnar rásar með því að búa til útgáfu tiltekinnar rásar fyrir síðu millir rása.

Til að búa til útgáfu tiltekinnar rásar fyrir síðu milli rása í Commerce-vefsmið skal fylgja þessum skrefum.

1. Í reitnum **Rás** uppi hægra megin skal velja **Netverslun milli rása**.
1. Opnið síðu milli rása sem var búin til hér á undan.
1. Í reitnum **Rás** uppi hægra megin skal velja rásina sem á að vera með tiltekið efni. Síðuritillinn sýnir skilaboð sem biðja þig um að búa til nýtt síðuafbrigði.
1. Veljið **Búa til síðuafbrigði**.
1. Í hólfinu **Aðalsvæði** í síðuafbrigðinu skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Tilboðsborði** og síðan velja **Í lagi**.
1. Á eiginleikasvæðinu fyrir eininguna **Tilboðsborði** skal velja **Bæta skilaboðum við** og síðan velja **Skilaboð**.
1. Í svarglugganum **Skilaboð**, undir **Texti**, skal færa inn **Tiltekin rás** og síðan velja **Í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Þú ættir að sjá tilboðsborðann sem á stendur „Tiltekin rás“.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

Ef þú notar nú grunnvefslóð rásarinnar og ferð á vefslóð síðu milli rása á því vefsvæði, geturðu séð efni tiltekinnar rásar í stað efni milli rása.

## <a name="additional-resources"></a>Frekari upplýsingar

[Leiðir til að bæta við efni](add-manage-content.md)

[Orðalisti síðulíkans](page-elements-overview.md)

[Staða og líftími skjala](document-states-overview.md)

[Vinna með birtingarhópa](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]