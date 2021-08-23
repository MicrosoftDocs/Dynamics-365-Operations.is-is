---
title: Gera greiðslutillögur lánardrottins sjálfvirkar
description: Þetta efnisatriði útskýrir hvernig fyrirtæki sem greiða lánardrottnum með reglulegu millibili geta gert ferlið sjálfvirkt sem býr til greiðslutillögur lánardrottins.
author: kweekley
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 483621a5de2980212926ac1011c16f1b82e4a3d075bbe9bcbbe6a0e35f06e5bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749103"
---
# <a name="automate-vendor-payment-proposals"></a>Gera greiðslutillögur lánardrottins sjálfvirkar

[!include [banner](../includes/banner.md)]

Fyrirtæki sem greiða lánardrottnum með reglulegu millibili geta nú gert ferlið sjálfvirkt sem býr til greiðslutillögur lánardrottins. Sjálfvirkar greiðslutillögur lánardrottins skilgreina eftirfarandi atriði:

- Þegar greiðslutillögur eru keyrðar
- Hvaða skilyrði eru notuð til að velja þá reikninga sem á að greiða
- Hvaða greiðslubók lánardrottins er notuð til að vista viðeigandi greiðslur

Sjálfvirkar greiðslutillögur bóka ekki sjálfkrafa greiðslurnar. Þess vegna er hægt að halda áfram að nota alla staðfestingar- og verkflæðisferla sem eru þegar notaðir til að samþykkja greiðslurnar sem eru stofnaðar.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Skilgreina tilfelli greiðslutillagna lánardrottins

Sjálfvirkar greiðslutillögur lánardrottins nota ramma sjálfvirkniferlis. Mismunandi viðskiptaferli nota þennan ramma til að skilgreina endurtekningu á völdu ferli. Fyrir greiðslutillögur lánardrottins er hægt að nálgast sjálfvirkni á **Viðskiptaskuldir \> Greiðsluuppsetning \> Sjálfvirkniferli**.

Fyrst skal nota sjálfvirknivalkostinn **Búa til nýtt ferli** og velja **Greiðslutillaga lánardrottins**. Leiðsagnarforrit leiðir notandann í gegnum ferlið þegar verið er að setja upp greiðslutillögu lánardrottins.

## <a name="general-page"></a>Almenna síðan

Á síðunni **Almennt** í leiðsögninni skal slá inn heiti greiðslutillögu lánardrottins sem verið er að búa til. Ef öllum innlendum lánardrottnum er greitt með ávísun á mánudegi, skal færa inn lýsandi heiti á borð við **Innlend\_Ávísun**. Heitið sem fært er inn er sýnt í vikulegu yfirliti sjálfvirkniferlisins á vinnusvæðinu **Greiðslur lánardrottins**.

Næst skal skilgreina eiganda greiðslubókarinnar sem er stofnuð. Eigandinn er yfirleitt starfsmaður viðskiptaskulda (AP) sem er ábyrgur fyrir greiðslubók eftir að hún hefur verið stofnuð.

Eftirstandandi stillingar á síðunni eru almennar og eru notaðar til að skilgreina endurtekningarmynstur þessarar útgáfu af greiðslutillögu lánardrottins. Til dæmis, ef tilfelli er fyrir ávísanagreiðslur á mánudegi er hægt að skilgreina það þannig að það keyri vikulega og hægt er að velja mánudag sem þann dag vikunnar þegar það er keyrt. Einnig er hægt að færa inn snemmbúna tímaáætlun, t.d. 02:00, þannig að sjálfvirkniferlinu verði lokið fyrir upphaf næsta viðskiptadags.

Mikilvægt er að þú skiljir að þú sért að nota leiðsagnarforritið til að skilgreina hvenær unnið er úr greiðslutillögu lánardrottins. Ekki er hægt að skilgreina hvenær lánardrottnagreiðslur eru myndaðar, prentaðar og bókaðar. Í vikulegu yfirliti er sjálfvirkniferlið fyrir greiðslutillögur lánardrottins birt á þeim dögum sem valdir eru í endurtekningarmynstrinu.

Frekari upplýsingar um aðra reiti á síðunni **Almennt** er að finna í fylgiskjölum sjálfvirkniferlisins.

## <a name="vendor-payment-proposal-page"></a>Greiðslutillögusíða lánardrottins

Næsta síða í leiðsagnarforritinu er **Greiðslutillaga lánardrottins**. Það er notað til að skilgreina skilyrðin fyrir vali á lánardrottnareikningum sem á að greiða. Almennt finnast sömu valmöguleikar í greiðslutillögunni í greiðslubók lánardrottins. Hinsvegar eru nokkrar undantekningar. Til dæmis verður að skilgreina allar dagsetningar á þessari síðu sem tengdar dagsetningar því að dagsetning greiðslutillögunnar breytist í hvert skipti sem tillagan er keyrð.

### <a name="journal-name"></a>Heiti færslubókar

Reiturinn **Heiti færslubókar** skilgreinir færslubókarheitið sem lánardrottnagreiðslurnar eru stofnaðar í. Sjálfvirkni á greiðslutillögu lánardrottins býr til greiðslur í skilgreindu færslubókinni, en færslubókin er ekki bókuð.

### <a name="from-date-and-to-date"></a>Dagsetning til og frá

Í stað þess að skilgreina „frá“ dagsetningu og „til“ dagsetningu til að velja reikninga á grundvelli gjalddaga eða dagsetningar staðgreiðsluafsláttar verður að nota valkostinn **Skilgreina skilyrði til dagsetningar** og reitinn **Stilltur dagafjöldi fyrir „til“ dagsetningu** til að skilgreina „til“ dagsetninguna. Ekki er til staðar hugtak fyrir „frá“ dagsetningu í sjálfvirkni greiðslutillaga.

Valkosturinn **Skilgreina skilyrði til dagsetningar** er sjálfgefið stilltur á **Nei**. Ef þetta sjálfgildi er notað mun ferlið velja alla reikninga fyrir greiðslu þegar ferlið er keyrt vegna þess að engin „til“ dagsetning hefur verið skilgreind.

Ef valkosturinn **Skilgreina skilyrði „til“ dagsetningar** er stilltur á **Já** skal nota reitinn **Stilltur dagafjöldi fyrir „til“ dagsetningu** til að skilgreina dagsetninguna þegar reikningar eru valdir sem tilgreindan fjölda daga á undan eða eftir dagsetningunni þegar ferlið er keyrt. Talan getur verið jákvæð, neikvæð, eða 0 (núll). Kerfið mun fyrir vikið greiða reikninga þar sem gjalddagar eða dagsetningar staðgreiðsluafsláttar eru innan tilgreinds dagafjölda á undan eða eftir dagsetningunni þegar ferlið er keyrt. Til dæmis, fyrir alla reikninga sem eru á gjalddaga á eða fyrir föstudag, stofnar greiðsluröðin greiðslur til allra lánardrottna með ávísun á miðvikudegi. Í þessu tilfelli skal stilla reitinn **Stilltur dagafjöldi fyrir „til“ dagsetningu** á **2**. Þegar tilfelli greiðslutillögunnar er keyrt miðvikudaginn 25. mars verða allir reikningar með gjalddaga eða dagsetningu staðgreiðsluafsláttar þann 27. mars eða fyrr valdir til greiðslu.

### <a name="minimum-payment-date"></a>Dagsetning lágmarksgreiðslu

Lágmarksgreiðsludagsetning skilgreinir fyrstu dagsetningu sem er notuð þegar greiðslur eru stofnaðar. Fyrst þarf að stilla valkostinn **Skilgreina skilyrði fyrstu greiðsludagsetningar** á **Já**. Þessi stilling gerir þér kleift að nota virkni fyrstu greiðsludagsetningar. Ef þessi valkostur er stilltur á **Já** skal nota reitinn **Stilltur dagafjöldi fyrir fyrstu greiðsludagsetningu** til að skilgreina fyrstu greiðsludagsetningu sem tilgreindan fjölda daga fyrir eða eftir daginn sem ferlið er keyrt. Talan getur verið jákvæð, neikvæð, eða 0 (núll). Til dæmis myndar greiðsluröðin greiðslur á miðvikudegi til að taka með allar greiðslur sem eru með lágmarksgreiðsludagsetningu á mánudeginum á undan. Í þessu tilfelli skal stilla **Stilltur dagafjöldi fyrir fyrstu greiðsludagsetningu** reitinn á **-2**.

Hér er dæmi sem sýnir hvernig reitirnir fyrir „til“ dagsetninguna og fyrstu greiðsludagsetninguna vinna saman. Sjálfvirk greiðslutillaga er sett upp til að keyra á miðvikudegi. Reiturinn **Stilltur dagafjöldi fyrir „til“ dagsetningu** er stilltur á **1** til að skilgreina „til“ dagsetninguna á grunni gjalddagans. Reiturinn **Stilltur dagafjöldi fyrir fyrstu greiðsludagsetningu** er stilltur á **-2**. Ef sjálfvirkt greiðsluferli hefst miðvikudaginn 25. mars verða allir reikningar sem eru á gjalddaga 26. mars eða fyrr teknir með í greiðslutillögunni. Greiðslutillögur verða myndaðar á eftirfarandi hátt:

- Allir reikningar sem eru á gjalddaga fyrir 23. mars verða með greiðsludag 23. mars.
- Reikningar sem eru á gjalddaga 24. mars verða með greiðsludagsetningu 24. mars.
- Reikningar sem eru á gjalddaga 25. mars verða með greiðsludagsetningu 25. mars.
- Reikningar sem eru á gjalddaga 26. mars verða með greiðsludagsetningu 26. mars.

### <a name="summarized-payment-date"></a>Samantekin greiðsludagsetning

Samantekin greiðsludagsetning er aðeins notuð þegar reiturinn **Tímabil** er stilltur á **Samtals** fyrir greiðslumáta reikninganna. Ef reiturinn **Tímabil** er stilltur á **Samtals** fyrir greiðslumáta þarf að stilla valkostinn **Skilgreina skilyrði samantekinnar greiðsludagsetningar** á **Já**. Ef þessi valkostur er stilltur á **Já** skal nota reitinn **Stilltur dagafjöldi fyrir samantekna greiðsludagsetningu** til að skilgreina samantekna greiðsludagsetningu sem tilgreindan fjölda daga fyrir eða eftir daginn sem ferlið er keyrt. Talan getur verið jákvæð, neikvæð eða 0 (núll). Sem dæmi, röðin býr til greiðslur á miðvikudegi og fyrirtækið vill búa til samantekna greiðslu á miðvikudegi. Í þessu tilfelli skal stilla **Stilltur dagafjöldi fyrir samantekna greiðsludagsetningu** reitinn á **0**.

### <a name="records-to-include"></a>Færslur til að taka með

Enn er hægt að skilgreina síuvalkosti fyrir greiðslutillöguna. Ef sía er skilgreind eru síuskilyrðin ekki birt á síðu leiðsagnarforritsins. Hins vegar er hægt að skoða þau með því að opna síuna aftur.

Eftirstandandi reitir fyrir tillöguna virka á sama hátt og þeir gera fyrir greiðslutillöguna í greiðslubók lánardrottins. Frekari upplýsingar um hina reitina er að finna í [Stofna lánardrottnagreiðslur með því að nota greiðslutillögu](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Nokkrir lands-/svæðisbundnir reitir og reitir opinbera geirans eru ekki enn tiltækir í sjálfvirkum greiðslutillögum lánardrottins.

Mælt er með því að lagt sé mat á hvort sjálfvirknin komi til með að gagnast fyrirtækinu þínu samkvæmt þínum kröfum.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Skoða niðurstöður sjálfvirkrar greiðslutillögu lánardrottins

Þegar röð sjálfvirkrar greiðslutillögu lánardrottins er búin til birtast tilfelli hverrar greiðslu í vikulegu yfirliti sjálfvirkniferlisins. Fyrir lánardrottnagreiðslur hefur vikulegu yfirliti sjálfvirkniferlisins verið bætt við bæði vinnusvæðið **Lánardrottnagreiðslur** og síðuna **Sjálfvirkni ferlis**.

[![Vikulegt yfirlit sjálfvirkniferlis á vinnusvæði lánardrottnagreiðslna.](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

Vikulegt yfirlit sjálfvirkniferlis á vinnusvæðinu **Lánardrottnagreiðslur** sýnir aðeins sjálfvirkar greiðslutillögur lánardrottins. Það sýnir öll greiðslutilfelli vikunnar, fyrir alla lögaðila sem innskráður notandi er með öryggisheimildir fyrir. Til dæmis, ef starfsmaður viðskiptaskulda ber ábyrgð á greiðslum í USMF og USSI fyrirtækjunum mun hann sjá tilfelli sjálfvirkrar greiðslutillögu lánardrottins fyrir þessi tvö fyrirtæki en engin önnur.

[![Vikulegt yfirlit sjálfvirkniferlis fyrir USMF og USSI fyrirtækin.](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Hvert tilfelli sýnir fyrirtækið sem greiðslubókin var eða verður stofnuð í. Ef greiðslur eru stofnaðar með miðstýrðum greiðslum er fyrirtækið sem sýnt er það fyrirtæki sem greiðslurnar verða stofnaðar í. Tilfellið sýnir ekki endilega hvaða reikningar fyrirtækisins verða greiddir.

Heiti hvers tilviks er einnig sýnt til að hjálpa til að auðkenna greiðslutillöguna.

Þar að auki er staða hvers tilviks sýnd. Eftirfarandi stöður eru notaðar:

- **Áætluð** – Greiðslutillaga er áætluð, en hún hefur ekki verið keyrð.
- **Villa** – Greiðslutillaga hefur verið keyrð en villa kom upp. Hægt er að skoða villurnar með því að velja hnappinn **Skoða niðurstöður**.
- **Lokið** – Greiðslutillaga hefur verið keyrð. Hægt er að skoða villurnar með því að velja tengilinn **Skoða niðurstöður**. Þessi tengill opnar greiðslubókina sem var stofnuð í tilvikinu.

Þegar búið er að stofna greiðslurnar er hægt að skoða greiðsluupphæðir í færslubókinni. Allar upphæðir eru sýndar í færslugjaldmiðli. Til dæmis, ef greiðslubókin inniheldur greiðslur í bandarískum og kanadískum dollurum eru heildargreiðslurnar fyrir hvorn gjaldmiðil sýndar. 

Hægt er að eyða greiðslubókinni eftir að hún hefur verið stofnuð í gegnum sjálfvirkniferlið. Ef greiðsla er eydd að fullu koma eftirfarandi tilvik upp:

- Staðan á sjálfvirkni ferlisins fyrir vikuna er áfram **Lokið**.
- Vinnslan fjarlægir greiðslusamtölur og tenglinum **Skoða greiðslur** er skipt út fyrir hnappinn **Skoða niðurstöður**.
- Þegar niðurstöðurnar eru skoðaðar birtast skilaboð sem segja að upprunalegri færslubók hafi verið eytt.

Eftir að greiðslu er eytt verða reikningarnir aftur opnir fyrir greiðslu. Svo er hægt að stofna nýtt tilvik til að greiða reikningana aftur.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Beryta sjálfvirkri greiðslutillögu lánardrottins

Með ramma sjálfvirkniferlisins er hægt að breyta greiðslunni, röðinni og tilfellunum sem eru stofnuð fyrir greiðslutillöguna. Hægt er að breyta röðinni annaðhvort á síðunni **Sjálfvirkniferli** eða í vikulegu yfirliti sjálfvirkniferlisins. Til dæmis, ef yfirmaður viðskiptaskulda ákveður að búa til allar ávísanir fyrir innlenda lánardrottna á miðvikudegi í stað mánudags, getur hann fundið tilfellið í vikuyfirlitinu og valið **Skoða/breyta - Röð**. Ef röð er breytt biður kerfið um að tilgreina hvort breytinguna eigi að gera á öllum fyrirliggjandi tilvikum eða aðeins nýjum tilvikum. Eldri tilvik sem eru komnar með stöðuna **Lokið**, eða þar sem kom upp staðan **Villa**, verður ekki breytt.

Einnig er hægt að bæta við nýju tilviki eða breyta fyrirliggjandi tilviki. Til dæmis er áætlað að keyra næsta tilvik greiðslutillögu miðvikudaginn 1. janúar, en þessi dagsetning er frídagur. Hægt er að breyta tilvikinu annaðhvort í vikulegu yfirliti sjálfvirkniferlisins eða á síðunni **Sjálfvirkniferli**. Síða opnast sem sýnir tímasetningar og skilyrði greiðslutillögu. Hér er hægt að breyta áætluðum tíma og dagsetningu. Einnig er hægt að breyta forsendum greiðslutillagna, ef breytingar eru nauðsynlegar. Til dæmis, ef áætlaðri dagsetningu greiðslutilviksins er breytt úr 1. janúar í 2. janúar, gætir þú einnig viljað breyta tengdum dagsetningum fyrir „til“ dagsetninguna.

Einnig er hægt að óvirkja tilvik eða röð tilvika. Til að gera tilvik óvirkt og fresta úrvinnslu þess skal velja það í vikulegu yfirliti sjálfvirkniferlisins og síðan velja **Gera óvirkt**. Hægt er að slökkva á röð á síðunni **Sjálfvirkniferli**.

## <a name="security-for-payment-proposal-automations"></a>Öryggi fyrir sjálfvirkar greiðslutillögur

Eftirtöldum skyldum og réttindum hefur verið bætt við fyrir sjálfvirkar greiðslutillögur lánardrottins. Þessar skyldur og réttindi eru sjálfgefnar öryggisstillingar en hægt er að breyta þeim eftir þörfum fyrirtækisins. Til dæmis, ef ekki aðeins yfirmaður viðskiptaskulda heldur líka starfsmaður viðskiptaskulda getur breytt og stofnað áætlað endurtekið tilvik, skal úthluta aðgangsheimildinni **Vinna með áætlunartilvik** á þann sem er í hlutverki starfsmanns viðskiptaskulda.

| Gjald                              | Hlutverk                                                                       | Réttindi |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Vinna með áætlunarraðir          | Viðskiptaskuldastjóri                                                   | Þessi aðgangsheimild veitir réttindi til að stofna og vinna með raðir sjálfvirkra greiðslutillaga og tilvika í gegnum eftirfarandi réttindi:<ul><li>Viðhalda áætlunartilvikum</li><li>Vinna með áætlunarraðir</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Skoða vikulegt yfirlit tilvika</li></ul> |
| Spyrjast fyrir um áætlunartilvik | Starfsmaður viðskiptaskulda, starfsmaður miðstýrðrar greiðslu viðskiptaskulda | Þessi aðgangsheimild veitir réttindi til að skoða tilvik sjálfvirkra greiðslutillaga og tilvika í gegnum eftirfarandi réttindi:<ul><li>Skoða áætlunartilvik</li><li>Skoða vikulegt yfirlit tilviks</li></ul> |
| Spyrjast fyrir um áætlunarraðir      | Engum                                                                       | Þessi aðgangsheimild veitir réttindi til að skoða stillingar raðanna og tilvika í gegnum eftirfarandi réttindi:<ul><li>Skoða áætlunartilvik</li><li>Skoða listasíðu tilvika</li><li>Skoða vikulegt yfirlit tilviks</li></ul>|
| Viðhalda áætlunartilvikum     | Engum                                                                       | Þessi aðgangsheimild veitir réttindi til að stofna og vinna með tilvik í gegnum eftirfarandi réttindi:<ul><li>Viðhalda áætlunartilvikum</li><li>Skoða vikulegt yfirlit tilviks</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]