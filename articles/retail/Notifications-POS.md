---
title: "Sýna pöntunartilkynningar á sölustað (POS)"
description: "Þetta efnisatriði lýsir því hvernig hægt er að virkja pöntunartilkynningar á sölustað og tilkynningarammann. Á endanum munu þróunaraðilar geta útfært þessar tilkynningar á fleiri aðgerðir en pöntunaruppfyllingaraðgerðir."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 41f16d13051f6095bdb04af1586ec06fe0ce93f6
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Sýna pöntunartilkynningar á sölustað (POS)

[!include [banner](includes/banner.md)]

Í nútíma smásöluumhverfi eru verslunarstarfsmönnum úthlutað ýmsum verkum, svo sem að aðstoða viðskiptavini, færa inn færslur, framkvæma birgðatalningu og taka á móti pöntunum í verslun. Biðlari sölustaðarins (POS) gerir starfsmönnum kleift að framkvæma öll þessi verk og mörg önnur í einu forriti. Þar sem þarf að framkvæma ýmis verk yfir daginn, gætu starfsmenn þurft að fá tilkynningu þegar eitthvað krefst athygli þeirra. Tilkynningaramminn á sölustað leyfir smásölum að stilla hlutverkatengdar tilkynningar. Með Microsoft Dynamics 365 for Retail með forritsuppfærslu 5, geta þessar tilkynningar aðeins verið stilltar fyrir aðgerðir á sölustað.

Eins og er getur kerfið aðeins sýnt tilkynningar fyrir pöntunaruppfyllingaraðgerðir. En vegna þess að ramminn er hannaður til að vera teygjanlegur munu þróunaraðilar á endanum geta skrifað tilkynningarekil fyrir hvaða aðgerð sem er og birt tilkynningarnar fyrir þessa aðgerð á sölustað.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Virkja tilkynningar fyrir pöntunaruppfyllingaraðgerðir

Til að virkja tilkynningar fyrir pöntunaruppfyllingaraðgerðir skal fylgja þessum skrefum.

1. Farið í **Retail** &gt; **Uppsetning rásar** &gt; **Uppsetning** &gt; **Sölustaður** &gt; **Aðgerðir**.
2. Leitið að aðgerðinni **Pöntunaruppfylling** og veljið gátreitinn **Virkja tilkynningar** svo tilkynningaramminn hlusti á rekilinn fyrir þessa aðgerð. Ef rekillinn er innleiddur verða tilkynningar fyrir þessa aðgerð sýndar á sölustaðnum.
3. Farið í **Retail** &gt; **Starfsmenn** &gt; **Starfsfólk** &gt;, undir smásöluflipanum, opnið heimildir sölustaðar sem tengjast starfsmanninum. Stækkið flýtiflipann **Tilkynningar**, bætið við aðgerðinni **Pöntunaruppfylling** og stillið reitinn **Birtingarröð** á **1**. Ef fleiri en ein tilkynning er skilgreind er þessi reitur notaður til að raða tilkynningunum. Tilkynningar sem hafa lægra gildi á **Birtingarröð** birtast fyrir ofan tilkynningar sem hafa hærra gildi. Tilkynningar sem hafa gildi **Birtingarraðar** á **1** eru efst.

    Tilkynningar eru aðeins sýndar fyrir aðgerðir sem er bætt við á flýtiflipanum **Tilkynningar** og aðeins er hægt að bæta við aðgerðum þar ef gátreiturinn **Virkja tilkynningar** fyrir þessar aðgerðir hefur verið valinn á síðunni **Aðgerðir sölustaðar**. Að auki eru tilkynningar um aðgerð aðeins sýndar starfsfólki ef aðgerðinni er bætt við heimildir sölustaðar fyrir þetta starfsfólk.

    > [!NOTE]
    > Tilkynningum er hægt að hnekkja á notandastigi. Opnið færslur starfsmanns, veljið **Heimildir sölustaðar** og breytið síðan tilkynningaáskrift notandans.

4. Smellið á **Retail** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Forstillingar sölustaðar** &gt; **Virknireglur**. Í reitnum **Tilkynningamillibil** skal tilgreina hversu oft á að kalla fram tilkynningar. Fyrir sumar tilkynningar þarf sölustaður að hafa samband við bakvinnsluforritið í rauntíma. Þessi samskipti taka yfir reikningsgetu bakvinnsluforritsins. Þegar tilkynningamillibilið er stillt ætti því að huga að bæði viðskiptakröfum og áhrifunum af samskiptum við bakvinnsluforritið í rauntíma. Gildið **0** (núll) slekkur á tilkynningum.
5. Farðu í **Smásala** &gt; **Upplýsingatækni smásölu** &gt; **Dreifingaráætlun**. Veljið áætlunina **1060** (**Starfsmenn**) til að samstilla tilkynningaáskriftir og smellið síðan á **Keyra núna**. Veljið næst áætlunina **1070** (**Stilling rásar**) til að samstilla heimildarmillibil og veljið síðan **Keyra núna**.

## <a name="view-notifications-in-the-pos"></a>Skoða tilkynningar á sölustaðnum

Eftir að þú hefur lokið ofangreindum skrefum munu starfsmenn geta skoðað tilkynningarnar á sölustaðnum. Til að skoða tilkynningar skal smella á tilkynningatáknið efst í hægra horni sölustaðar. Við það birtist tilkynningamiðstöð með tilkynningum fyrir pöntunaruppfyllingaraðgerðina. Tilkynningamiðstöðin ætti að birta eftirfarandi hópa innan pöntunaruppfyllingaraðgerðarinnar:

- **Afhending í verslun** - Þessi hópur sýnir fjölda pantana sem hafa afhendingarstillinguna **Afhending** og afhendingin er áætlaðu frá núverandi verslun. Hægt er að smella á númerið á hópnum til að opna síðuna **Pöntunaruppfylling**. Í þessu tilfelli verður síðan síuð þannig að hún sýnir aðeins virku pantanirnar sem eru settar upp fyrir afhendingu frá núverandi verslun.
- **Senda frá verslun** - Þessi hópur sýnir fjölda pantana sem hafa afhendingarstillinguna **Sending** og sendingin er áætluð frá núverandi verslun. Hægt er að smella á númerið á hópnum til að opna síðuna **Pöntunaruppfylling**. Í þessu tilviki verður síðan síuð þannig að hún sýnir aðeins virku pantanirnar sem eru settar upp fyrir sendingu frá núverandi verslun.

Þegar nýjum pöntunum er úthlutað í búðina til uppfyllingar þá breytist tilkynningartáknið til að gefa til kynna nýjar tilkynningar og fjöldi viðeigandi hópa verður uppfærður. Þótt hóparnir séu uppfærðir með reglulegu millibili, geta notendur sölustaðar uppfært hópana handvirkt hvenær sem er með því að velja hnappinn **Uppfæra** við hliðina á hópnum. Að lokum, ef hópur hefur nýtt atriði, sem núverandi starfsmaður hefur ekki skoðað, þá sýnir hópurinn sprengitákn sem gefur til kynna nýtt efni.

## <a name="enable-live-content-on-pos-buttons"></a>Virkja beint efni á hnöppum sölustaðar

Hnappar sölustaðar geta nú sýnt fjölda til að auðvelda starfsmönnum að ákvarða hvaða verk krefjast strax athygli. Til að sýna þetta númer á hnappi sölustaðar verður að ljúka tilkynningastillingunni sem lýst er fyrr í þessu efni (þ.e.a.s. þú verður að virkja tilkynningar fyrir aðgerð, setja upp tilkynningamillibil og uppfæra heimildaflokk sölustaðar fyrir starfsmanninn). Að auki verður þú að opna hnappahnit hönnuðar, skoða eiginleika hnappsins og velja gátreitinn **Virkja beint efni**. Í reitnum **Jöfnun efnis** getur þú valið hvort talningin birtist í efra hægra horninu á hnappinn (**Efst til hægri**) eða í miðjunni (**Miðja**).

> [!NOTE]
> Beint efni getur aðeins verið virkjað fyrir aðgerðir ef gátreiturinn **Virkja tilkynningar** hefur verið valinn á síðunni **Aðgerðir sölustaðar** eins og lýst er hér að ofan í þessu efnisatriði.

Eftirfarandi skýringarmynd sýnir stillingar á beinu efni í hnappahniti hönnuðar.

![Stillingar á beinu efni í hnappahniti hönnuðar](./media/ButtonGridDesigner.png "Stillingar á beinu efni í hnappahniti hönnuðar")

Eftirfarandi skýringarmynd sýnir áhrif þess að velja **Efst til hægri** á móti **Miðju** í reitnum **Jöfnun efnis** fyrir hnappa af ýmsum stærðum.

![Beint efni á hnöppum sölustaðar](./media/ButtonsWithLiveContent.png "Beint efni á hnöppum sölustaðar")

