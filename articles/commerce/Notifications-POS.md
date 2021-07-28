---
title: Sýna pöntunartilkynningar á sölustað (POS)
description: Þetta efnisatriði lýsir því hvernig hægt er að virkja pöntunartilkynningar á sölustað og tilkynningarammann.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 57f5d23533c2fd17593648a15745fa770fc01dc4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345209"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Sýna pöntunartilkynningar á sölustað (POS)

[!include [banner](includes/banner.md)]

Starfsmönnum verslunar kann að vera úthlutað ýmsum verkum í versluninni, t.d. uppfyllingu pantana eða framkvæmd birgðamóttöku eða birgðatalningu. Biðlari sölustaðarins (POS) býður upp á eitt forrit þar sem hægt er að láta starfsmenn vita af verkum. Tilkynningaramminn á sölustað leyfir smásölum að stilla hlutverkatengdar tilkynningar. Frá og með Dynamics 365 Retail með forritsuppfærslu 5, geta þessar tilkynningar aðeins verið stilltar fyrir aðgerðir á sölustað.

Kerfið getur sýnt tilkynningar um *uppfyllingaraðgerð pöntunar* og frá og með Commerce-útgáfu 10.0.18 verður einnig hægt að sýna tilkynningar fyrir *afturköllunaraðgerð pöntunar*. En vegna þess að ramminn er hannaður til að vera teygjanlegur munu þróunaraðilar geta [skrifað tilkynningarekil](dev-itpro/extend-pos-notification.md) fyrir hvaða aðgerð sem er og birt tilkynningarnar fyrir þessa aðgerð á sölustað.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Virkja tilkynningar fyrir uppfyllingaraðgerð pöntunar eða afturköllunaraðgerð pöntunar

Til að virkja tilkynningar fyrir uppfyllingaraðgerð pöntunar eða afturköllunaraðgerð pöntunar skal fylgja þessum skrefum.

1. Farðu í **Retail og Commerce \> Uppsetningu rásar \> Uppsetning POS \> POS \> Aðgerðir**.
1. Leitið annaðhvort að aðgerðinni **Uppfylling pöntunar** eða aðgerðinni **Endurköllun pöntunar** og veljið síðan **Virkja tilkynningar** fyrir aðgerðina til að gefa til kynna að tilkynningaramminn eigi að hluta á rekilinn fyrir þessa aðgerð. Ef rekillinn er innleiddur verða tilkynningar fyrir þessa aðgerð sýndar á sölustaðnum.
1. Farðu í **Retail og Commerce \> Starfsmenn \> Starfsfólk**.
1. Veljið flipann **Commerce**, veljið starfsmannalínu og veljið því næst **Heimildir sölustaðar**. Veljið flýtiflipann **Tilkynningar** til að stækka hann og bætið síðan við aðgerðunum sem búið er að virkja tilkynningar fyrir. Ef á að stilla eina tilkynningu fyrir starfsmann skal ganga úr skugga um að gildið **Sýna röð** sé stillt á **1**. Ef fleiri en ein aðgerð er stillt skal stilla gildið **Sýna röð** til að gefa til kynna röðina sem sýna á tilkynningarnar í. 

      Tilkynningar eru aðeins sýndar fyrir aðgerðir sem er bætt við flýtiflipann **Tilkynningar**. Aðeins er hægt að bæta við aðgerðum þar ef gátreiturinn **Virkja tilkynningar** fyrir þessar aðgerðir hefur verið valinn á síðunni **Aðgerðir sölustaðar**. Að auki eru tilkynningar um aðgerð aðeins sýndar starfsfólki ef aðgerðinni er bætt við heimildir sölustaðar fyrir þetta starfsfólk.

    > [!NOTE]
    > Tilkynningum er hægt að hnekkja á notandastigi. Til að gera þetta skal opna færslu starfsmanns, velja **Heimildir sölustaðar** og síðan breyta tilkynningaáskrift notandans.

1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**. Í reitnum **Tilkynningamillibil** skal tilgreina hversu oft á að kalla fram tilkynningar. Fyrir sumar tilkynningar þarf sölustaður að hafa samband við bakvinnsluforritið í rauntíma. Þessi samskipti taka yfir reikningsgetu bakvinnsluforritsins. Þegar tilkynningamillibilið er stillt ætti því að huga að bæði viðskiptakröfum og áhrifunum af samskiptum við bakvinnsluforritið í rauntíma. Gildið **0** (núll) slekkur á tilkynningum.
1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**. Veljið áætlunina **1060** (**Starfsmenn**) til að samstilla tilkynningaáskriftir og smellið síðan á **Keyra núna**. Veljið næst áætlunina **1070** (**Stilling rásar**) til að samstilla heimildarmillibil og veljið síðan **Keyra núna**.

## <a name="view-notifications-in-the-pos"></a>Skoða tilkynningar á sölustaðnum

Eftir að þú hefur lokið ofangreindum skrefum munu starfsmenn geta skoðað tilkynningarnar á sölustaðnum. Til að skoða tilkynningar skal velja tilkynningatáknið efst í hægra horni sölustaðar. Tilkynningasvæði birtist og sýnir tilkynningar fyrir aðgerðirnar sem stilltar eru fyrir starfsmanninn. 

Fyrir **uppfyllingaraðgerð pöntunar** mun tilkynningasvæðið sýna eftirfarandi flokka:

- **Afhending í verslun** - Þessi flokkur sýnir fjölda stakra pöntunarlína sem áætlað er að verði sóttar úr núverandi verslun. Hægt er að velja númerið á flokknum til að opna aðgerðina **Uppfylling pöntunar** með síu þannig að hún sýni aðeins virkar pöntunarlínur sem eru settar upp að verða sóttar úr núverandi verslun.
- **Senda úr verslun** – Þessi flokkur sýnir talningu stakra pöntunarlína sem hafa verið skilgreindar til senda frá núverandi verslun notandans. Hægt er að velja númerið á flokknum til að opna aðgerðina **Uppfylling pöntunar** með síuðu yfirliti þannig að það sýni aðeins virkar pöntunarlínur sem eru settar upp að verða sendar úr núverandi verslun.

Fyrir **endurköllunaraðgerð pöntunar** mun tilkynningasvæðið sýna eftirfarandi flokka:

- **Pantanir sem á að uppfylla** – Þessi flokkur sýnir talningu pantana sem eru skilgreindar annaðhvort til að vera sóttar eða sendar fyrir núverandi verslun notanda. Hægt er að velja númerið á flokknum til að opna aðgerðina **Endurköllun pöntunar** með síuðu yfirliti sem sýnir aðeins opnu pantanirnar sem núverandi verslun notanda þarf að uppfylla fyrir annaðhvort að verða sótt úr verslun eða sent úr verslun.
- **Pantanir sem þarf að sækja** - Þessi flokkur sýnir fjölda pantana sem áætlað er að verði sóttar úr núverandi verslun. Hægt er að velja númerið á flokknum til að opna aðgerðina **Endurköllun pöntunar** með síuðu yfirliti sem sýnir aðeins opnar pantanir sem núverandi verslun notanda þarf að uppfylla fyrir annaðhvort að verða sótt úr verslun eða sent úr verslun.
- **Pantanir sem þarf að senda** – Þessi hópur sýnir fjölda pantana sem á að senda úr núverandi verslun notanda. Hægt er að velja númerið á flokknum til að opna aðgerðina **Endurköllun pöntunar** með síuðu yfirliti sem sýnir aðeins opnar pantanir sem núverandi verslun notanda þarf að uppfylla sendingu fyrir.

Fyrir bæði tilkynningar um uppfyllingu pöntunar og endurköllun pöntunar, þar sem nýjar pantanir eru sóttar af ferlinu, breytist tilkynningatáknið til að gefa til kynna að nýjar tilkynningar og talning fyrir viðeigandi flokka sé uppfært. Þótt flokkarnir séu uppfærðir með reglulegu millibili, geta notendur sölustaðar uppfært flokkana handvirkt hvenær sem er með því að velja **Uppfæra** við hliðina á flokknum. Að lokum, ef hópur hefur nýtt atriði, sem núverandi starfsmaður hefur ekki skoðað, þá sýnir hópurinn sprengitákn sem gefur til kynna nýtt efni.

## <a name="enable-live-content-on-pos-buttons"></a>Virkja beint efni á hnöppum sölustaðar

Hnappar sölustaðar geta nú sýnt fjölda til að auðvelda starfsmönnum að ákvarða hvaða verk krefjast strax athygli. Til að sýna þetta númer á hnappi sölustaðar verður að ljúka tilkynningastillingunni sem lýst er fyrr í þessu efni (þ.e.a.s. þú verður að virkja tilkynningar fyrir aðgerð, setja upp tilkynningamillibil og uppfæra heimildaflokk sölustaðar fyrir starfsmanninn). Að auki verður þú að opna hnappahnit hönnuðar, skoða eiginleika hnappsins og velja gátreitinn **Virkja beint efni**. Í reitnum **Jöfnun efnis** getur þú valið hvort talningin birtist í efra hægra horninu á hnappinn (**Efst til hægri**) eða í miðjunni (**Miðja**).

> [!NOTE]
> Beint efni getur aðeins verið virkjað fyrir aðgerðir ef gátreiturinn **Virkja tilkynningar** hefur verið valinn á síðunni **Aðgerðir sölustaðar** eins og lýst er hér að ofan í þessu efnisatriði.

Eftirfarandi skýringarmynd sýnir stillingar á beinu efni í hnappahniti hönnuðar.

![Stillingar fyrir lifandi efni í hönnuður hnappatafla.](./media/ButtonGridDesigner.png "Stillingar fyrir lifandi efni í hönnuður hnappatafla")

Til að sýna talningu tilkynningar á hnappi þarf að tryggja að verið sé að uppfæra rétt skjáútlit. Til að ákvarða skjáútlitið sem sölustaður er að nota skal velja táknið **Stillingar** efst í hægra horninu og taka niður **Auðkenni skjáútlits** og **Upplausn útlits**. Nú skaltu nota Edge-vafra, opna síðuna **Skjáútlit**, finna **Auðkenni skjáútlits** og **Upplausn útlits** sem er tilgreint efst og velja gátreitinn **Gera lifandi efni virkt**. Farið í **Retail og Commerce \> Upplýsingatækni Retail og Commerce \> Dreifingaráætlun** og keyrið 1090 (afgreiðslukassar) verk til að samstilla breytingar á útliti.

![Finndu skjáinn sem POS notar.](./media/Choose_screen_layout.png "Finndu skjáútlitið")

Eftirfarandi skýringarmynd sýnir áhrif þess að velja **Efst til hægri** á móti **Miðju** í reitnum **Jöfnun efnis** fyrir hnappa af ýmsum stærðum.

![Beint efni á hnöppum sölustaðar.](./media/ButtonsWithLiveContent.png "Beint efni á hnöppum sölustaðar")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
