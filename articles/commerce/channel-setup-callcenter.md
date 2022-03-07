---
title: Setja upp rás símavers
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýja rás símavers í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3b21d5e57058fee5bb77beb6731c18967ed11cacc1925e44d2f7d8cdb26d7bcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744535"
---
# <a name="set-up-a-call-center-channel"></a>Uppsetning símaversrásar


[!include [banner](includes/banner.md)]

Í þessu efnisatriði er lýst hvernig eigi að stofna nýja rás símavers í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit


Í Dynamics 365 Commerce er símaver tegund Commerce-rásar sem hægt er að skilgreina í forritinu. Að skilgreina rás fyrir símaþjónustueiningar þínar gerir kerfinu kleift að binda tiltekin gögn og sjálfgildi pöntunarvinnslu við sölupantanir. Þó fyrirtæki geti skilgreint margar símaversrásir í Commerce, er mikilvægt að hafa í huga að stakur notandi getur aðeins verið tengd einni símaversrás. 

Áður en ný rás símavers er stofnuð skaltu ganga úr skugga um að þú hafir lokið við [Skilyrði fyrir rásauppsetningu](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Stofna og stilla nýja rás símavers

Til að stofna og stilla nýja rás símavers fylgirðu þessum skrefum.

1. Í yfirlitssvæðinu ferðu í **Retail og Commerce \> Rásir \> Símaver \> Öll símaver**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitnum **Heiti** slærðu inn heiti fyrir nýju rásina.
1. Veldu viðeigandi **Lögaðila** af fellilistanum.
1. Veldu viðeigandi staðsetningu **vöruhúss** af fellilistanum. Þessi staðsetning verður notuð sem sjálfgildi í sölupöntunum sem voru stofnaðar fyrir þessa símaversrás, nema önnur sjálfgildi hafi verið skilgreind á viðskiptavinar- eða vörustigi.
1. Í reitnum **Sjálfgefinn viðskiptavinur** gefurðu upp gildan sjálfgefinn viðskiptavin. Þessi gögn eru notuð til að aðstoða við sjálfval þegar nýjar viðskiptavinafærslur eru stofnaðar. Þegar búið er til pantanir í símaverum er ekki ráðlegt að búa til pantanir fyrir sjálfgefna viðskiptavininn.
1. Í reitinn **Forstilling tilkynningar í tölvupósti** gefurðu upp gilt tilkynningarsnið fyrir tölvupóst. Þegar pantanir símavers eru búnar til og unnar er tilkynningasniðið notað til að kalla fram sjálfvirkar tilkynningar um tölvupóst til viðskiptavina með upplýsingar um stöðu pöntunar.
1. Gefa upp upplýsingakóða **verðhnekkingar**. Þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst. Þessi upplýsingakóði veitir sett af ástæðukóða sem notandinn verður beðinn um að velja úr þegar hann notar verðhækkunaraðgerðina í pöntun símavers.
1. Gefðu upp upplýsingakóðann **Biðkóði**. Þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst. Þessi upplýsingakóði veitir sett af valkvæðum ástæðukóðum sem notandinn verður beðinn um að velja úr þegar hann setur pöntun í bið.
1. Gefðu upp upplýsingakóðann **Kredit**. Þú gætir þurft að búa til upplýsingakóða fyrir þetta fyrst. Þessi upplýsingakóði veitir þann fjölda ástæðukóða sem notandinn getur valið um þegar hann notar pöntunarlánatækni í símaþjónustuver til að veita viðskiptavinum ýmsar endurgreiðslur af þjónustuástæðum.
1. Valfrjálst: setja upp fjárhagsvíddir á flýtiflipanum **Fjárhagsvíddir**. Málin sem hér eru færð inn munu sjálfkrafa vera í öllum sölupöntunum sem búnar eru til í þessari stöðvarstöð.
1. Smellt er á **Vista**.

Eftirfarandi mynd sýnir stofnun nýrrar símaversrásar.

![Ný rás símavers.](media/channel-setup-callcenter-1.png)

Eftirfarandi mynd sýnir dæmi um símaversrás.

![Dæmi um rás símavers.](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Viðbótaruppsetning grunnrásar

Viðbótarupplýsingar sem krafist er fyrir uppsetningu símaversrásar fela í sér uppsetningu á greiðslumáta og afhendingaraðferðum.

Eftirfarandi mynd sýnir uppsetningarkostina **Afhendingarmáta** og **Greiðslumáta** á flipanum **Setja upp**.

![Viðbótar uppsetningaraðgerðir símaversrásar.](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Setja upp greiðsluhætti

Fylgdu þessum skrefum til að setja upp greiðslumáta fyrir hverja greiðslugerð sem er studd á þessari rás. Notendur verða að velja úr fyrirfram skilgreindum greiðsluaðferðum til að tengja þær við símaversrásina. Áður en þú setur upp greiðslumáta símaþjónustunnar skaltu fyrst setja upp greiðslumáta þína í **Verslun og verslun \> Uppsetning rásar \> Greiðslumátar \> Greiðslumátar**.

1. Í aðgerðaglugganum velurðu flipann **Setja upp** og velur síðan **Greiðslumátar**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Veldu greiðslumáta úr fyrirfram skilgreindum greiðslum í boði á leiðsögubrautinni.
1. Stilltu allar viðbótarstillingar eins og krafist er fyrir greiðslugerð. Að því er varðar kreditkort, gjafakort eða vildarkort þarf viðbótar uppsetningu með því að velja virknina **Uppsetning korta**. 
1. Stilla rétt bókun reikninga fyrir greiðslugerðina í hlutanum **Bókun**.
1. Í aðgerðasvæðinu smellirðu á **Vista**.

Eftirfarandi mynd sýnir dæmi um greiðsluaðferð í reiðufé.

![Dæmi um greiðslumáta.](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Setja upp afhendingarmáta

Þú getur séð stillta afhendingarmáta með því að velja **Afhendingarmáta** af flipanum **Setja upp** í **Aðgerðarglugganum**.  

Fylgdu þessum skrefum til að breyta eða bæta við afhendingaraðferð sem á að tengjast símaþjónustuverinu.

1. Veldu af sendingarformi símaþjónustuvera **Hafa umsjón með afhendingaraðferðum**
1. Í aðgerðaglugganum velurðu **Nýtt** til að stofna nýjan flutningsmáta eða velur núverandi stillingu.
1. Í kaflanum **Smásölurásir** smellirðu á **Bæta við línu** til að bæta við símaversrás. Að bæta við rásum með fyrirtækjahnútum í stað þess að bæta hverri rás fyrir sig getur auðveldað að rásum sé bætt við.
1. Gakktu úr skugga um að afhendingarstíllinn hafi verið stilltur með gögnum á flýtiflipunum **Vörur** og **Heimilisföng**. Ef engar vörur eða afhendingarföng eru gild fyrir afhendingaraðferðina, þá mun það velja villur við pöntunarfærslu.
1. Þegar breytingar hafa verið gerðar á símaversstillingum afhendingarstillinga verður að keyra vinnsluna **Afhendingarmátar vinnslu** að keyra starf til að sprengja breytileika. Þetta starf er að finna með því að fara á **Retail og Commerce \> Upplýsingatækni Retail og Commerce \> Afhendingarmátar vinnslu**.

Eftirfarandi mynd sýnir dæmi um afhendingarmáta.

![Setja upp afhendingarmáta.](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Setja upp rásarnotendur

Til að búa til sölupöntun sem er tengd við símaþjónustuver rás frá höfuðstöðvum viðskiptanna verður notandinn sem býr til sölupöntunina að vera tengdur við símaþjónustuver rásarinnar. Notandinn getur ekki tengt handvirkt sölupöntun sem búin var til í Commerce Headquarters í símaversrás. Hlekkurinn er kerfisbundinn og byggist á notanda og tengslum notandans við símaversrásina. Notandi getur aðeins verið tengdur við eina símaversrás.

1. Í aðgerðaglugganum velurðu flipann **Rás** og velur síðan **Notendur rásar**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Veldu núverandi **Notandakenni** úr fellivalmyndinni til að tengja þennan notanda við símaversrásina

Þegar uppsetningu rásarnotanda er lokið og notandinn stofnar nýja sölupöntun í Commerce Headquarters verður sölupöntunin tengd við tengda rás símaþjónustuvers hans. Allar stillingar fyrir þessa rás verður beitt kerfisbundið á sölupöntunina. Notandi getur staðfest hvaða símaþjónustuver rás sölupöntunin er tengd með því að skoða tilvísun rásarheitisins á sölupöntunarhausnum.


### <a name="set-up-price-groups"></a>Setja upp verðflokka

Verðhópar eru valfrjálsir, en ef þeir eru notaðir geta þeir stjórnað því hvaða söluverð verður boðið viðskiptavinum sem setja pantanir í símaversrásina. Ef verðflokkur hefur ekki verið stilltur fyrir viðskiptavininn, eða ef ekki er beitt vöruflokkahópum á sölupöntunina (með því að nota reitinn **Kenni upprunakóða** á pöntunarhausum símaþjónustunnar), þá er verðflokkur rásarinnar notaður til að finna verð á hlutum. Ef verðlagshópur er ekki að finna á stöðvunarstöðinni, er sjálfgefið yfirverð vöru notuð. 

Til að setja upp verðflokk, gerðu eftirfarandi.

1. Í aðgerðaglugganum smellirðu á flipann **Rás** og velur síðan **Verðflokkar**.
1. Í aðgerðasvæðinu er smellt á **Nýtt**.
1. Veldu **Smásöluverðshóp** úr fellivalmyndinni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilyrði fyrir uppsetningu rásar](channels-prerequisites.md)

[Söluvirkni símavers](call-center-functionality.md)

[Uppsetning valkosta pantanavinnslu símavers](set-up-order-processing-options.md)

[Vörulistar símavers](call-center-catalogs.md)

[Setja upp og vinna með svikaviðvaranir](set-up-fraud-alerts.md)

[Setja upp samfelldniáætlanir fyrir símaver](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]