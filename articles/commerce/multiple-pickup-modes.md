---
title: Virkja marga afhendingamáta fyrir pantanir viðskiptavinar
description: Þetta efnisatriði útskýrir virkni í Microsoft Dynamics 365 Commerce sem gerir þér kleift að stofna viðskiptavinapantanir fyrir það sem er sótt í verslun.
author: hhainesms
manager: annbe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 768b20ecc8d15353258c9b3af69b897957d3de60
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594971"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Virkja marga afhendingamáta fyrir pantanir viðskiptavinar

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Í Microsoft Dynamics 365 Commerce útgáfu 10.0.16 og nýrri, geta fyrirtæki skilgreint marga afhendingarmáta sem kaupendur eða sölufulltrúar geta valið úr þegar þeir stofna pantanir sem verða sóttar í verslun. Á þennan hátt geta fyrirtæki veitt kaupendum marga tengimöguleika. Til dæmis bjóða margir smásalar kaupendum upp á að velja milli þess að sækja pantanir í verslun eða fyrir utan verslun. Commerce styður skilgreiningu á þessum mismunandi afhendingarmátum þegar er sótt. Notendur geta þá nýtt sér þá þegar þeir stofna viðskiptavinapantanir í hvaða studdu Commerce-rás sem er (rafræn viðskipti, símaver eða verslun).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Virkja og skilgreina afhendingarmáta

Til að nota þessa virkni þarf að kveikja á eiginleikanum **Stuðningur fyrir margar afhendingarstillingar** á vinnusvæðinu **Eiginleikastjórnun** í Commerce Headquarters. Þegar kveikt hefur verið á eiginleikanum eru frekari skilgreiningar nauðsynlegar.

Í Commerce Version 10.0.15 og eldri geta fyrirtæki aðeins skilgreint einn afhendingarmáta sem merktan afhendingarmáta. Þessi skilgreining er gerð á síðunni **Færibreytur Commerce**. Í útgáfu 10.0.16 og síðar, þegar kveikt er á eiginleikanum **Stuðningur fyrir margar afhendingarstillingar**, er afhendingarmátinn sem var áður skilgreindur sem afhendingarstillingin á síðunni **Færibreytur Commerce** sjálfkrafa afritaður í nýju skilgreininguna fyrir afhendingarstillingar.

![Afhendingarmátar á færibreytusíðu Commerce](media/multiplepickupparameter.png)

Eftir að kveikt er á eiginleikanum **Stuðningur fyrir margar afhendingarstillingar**, er hægt að skilgreina marga afhendingarmáta í hnitanetinu **Afhendingarmáti fyrir sótt** í flýtiflipanum **Afhendingarmátar** í flipanum **Pantanir viðskiptavinar** á síðunni **Færibreytur Commerce**.

Reitirnir **Afhendingarmáti fyrir sótt** og **Rafrænn afhendingarmáti** og valkosturinn **Sýna aðeins valmöguleika flutningsmáta fyrir sendingar pantana** hafa verið færðir yfir í þennan flýtiflipa.

Áður en hægt er að skilgreina fleiri afhendingarmáta fyrir sóttar pantanir Þarf að skilgreina afhendingarmátana. Á síðunni **Afhendingarmáti** í Commerce Headquarters skal bæta við afhendingarmátanum sem á að vera afhendingarmáti fyrir það sem er sótt. Gangið úr skugga um að skilgreiningunni sé lokið að fullu. Til dæmis skal ganga úr skugga um að afhendingarmáti sé tengdur við viðeigandi rásir og vörur. Þegar því er lokið skal keyra verkið **Vinna úr afhendingarmáta** til að stofna tengslin milli afhendingarmáta, rása og vara. Þegar verkinu er lokið skal opna síðuna **Dreifingaráætlun** í Commerce Headquarters og keyra dreifingarverkið **1120** til að tryggja að viðeigandi gagnagrunnar Commerce-rásar séu uppfærðir með nýrri skilgreiningu á afhendingarmáta.

![Dæmi um skilgreiningu afhendingarmáta fyrir sótta pöntun fyrir utan verslun](media/pickupmodes.png)

Þegar búið er að skilgreina fleiri afhendingarmáta skal bæta þeim við hnitanetið **Afhendingarmáti fyrir sótt** á síðunni **Færibreytur Commerce**. Keyrið síðan viðeigandi dreifingarvinnslur til að uppfæra viðeigandi gagnagrunna Commerce-rásar með breytingu á skilgreiningu.

> [!NOTE]
> Fyrir utan fyrirliggjandi afhendingarmáta sem er afritaður í hnitanetið **Afhendingarmáti fyrir sótt** þegar kveikt er á eiginleikanum **Stuðningur fyrir margar afhendingarstillingar**, fyrir hverja aukalega skilgreiningu á afhendingarmáta sem stofnaður er, ætti að skilgreina nýja afhendingarmáta. Þegar afhendingarmátum er bætt við hnitanetið **Afhendingarmáti fyrir sótt**, sannprófar Commerce hvort einhverjar opnar sölulínur séu nú þegar að nota hann. Villuboð birtast ef einhverjar opnar sölulínur finnast. Afhendingarmátar er ekki taldir afhendingarmátar fyrir sóttar pantanir fyrr en öllum opnum sölulínum sem nota þá hefur verið lokað (annaðhvort reikningsfærðar eða afturkallaðar).

> [!IMPORTANT]
> Þegar búið er að skilgreina fleiri en einn afhendingarmáta á síðunni **Færibreytur Commerce** verður eiginleikinn **Stuðningur fyrir margar afhendingarstillingar** áskilinn og ekki verður hægt að slökkva á honum. Ef þarf að slökkva á eiginleikanum skal fjarlægja alla nema einn afhendingarmáta fyrir sóttar pantanir úr hnitanetinu **Afhendingarmáti fyrir sótt**. Þegar aðeins einn afhendingarmáti er skilgreindur, er eiginleikinn ekki lengur áskilinn og því hægt að slökkva á honum.

### <a name="e-commerce-site-configurations"></a>Skilgreiningar á svæði fyrir rafræn viðskipti

Þegar kveikt er á eiginleikanum **Stuðningur fyrir margar afhendingarstillingar** sýna eftirfarandi einingar á síðum rafrænna viðskipta nýju afhendingarmátana fyrir sóttar pantanir sem skilgreindar:

- Kaupgluggi
- Val á verslun
- Karfa
- Afhendingarupplýsingar
- Staðfesting pöntunar
- Upplýsingar um pöntun

Engin frekari skref eru nauðsynleg á síðum rafrænna viðskipta til að gera afhendingarmáta fyrir sóttar pantanir tiltæka.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Vinna með marga afhendingamáta

Þegar margir afhendingarmátar eru í boði fyrir rás, er viðskiptavinum boðið upp á aukna upplifun þegar þeir versla vörur sem verða sóttar. 

- Í rafrænum viðskiptarásum geta kaupendur valið hvaða sóttan afhendingarmáta sem er í boði. Til dæmis skilgreinir smásali tvo afhendingarmáta (sótt í verslun eða fyrir utan verslun), báðir skilgreindir í hnitanetinu **Afhendingarmáti fyrir sótt** og báðir eru í gildi fyrir rás pöntunaruppfyllingar og vöruna sem kaupandinn er að kaupa á þessu augnabliki. Í þessu tilvikum getur kaupandi valið æskilega afhendingu. Valinn afhendingarmáti fyrir pöntun sem er sótt verður afhendingarmátinn sem er tengdur við sölupöntunarlínuna þegar pöntunin er stofnuð í Commerce Headquarters.

    ![Að velja í rafrænum viðskiptum hvernig á að sækja pöntun](media/pickupecommerce.png)

- Í verslunarrásum, ef viðskiptavinapöntun sem á að sækja er stofnuð í forriti sölustaðar, er sölufulltrúinn beðinn um að velja úr tiltækum afhendingarmátum fyrir pöntun sem á að sækja, ef einhverjir hafa verið skilgreindir. Ef aðeins einn gildur afhendingarmáti er tiltækur fyrir rásina og vöruna, er sölufulltrúinn ekki beðinn um að velja hann. Þess í stað er tiltækur afhendingarmáti sjálfkrafa notaður fyrir pöntunarlínurnar.

    ![Að velja í forriti sölustaðar hvernig á að sækja pöntun](media/pickuppos.png)

- Á rásum símavers, þegar notendur stofna pantanir sem verða sóttar, geta þeir valið handvirkt hvaða skilgreindan afhendingarmáta sem er sem tengist rás símaversins. Kerfið staðfestir síðan að hægt sé að nota valdan afhendingarmáta þegar varan sem tengd er við hann er pöntuð. Þegar valinn er í rásum símavers afhendingarmáti fyrir pöntun sem verður sótt, verða sölupöntunarlínurnar að vera tengdar við gilt vöruhús verslunar. Ef vöruhús án verslunar er skilgreint í sölulínu símavers verður ekki hægt að stilla á sóttan afhendingarmáta fyrir þá sölulínu.
- Sölufulltrúar geta notað aðgerðina **Afturköllun pöntunar** eða **Uppfylling pöntunar** í forriti sölustaðar til að sækja lista yfir pantanir eða pöntunarlínur fyrir sótta pöntun. Ef sölufulltrúi notar fyrirframskilgreinda leitarsíu til að sýna allar pantanir sem verða sóttar í núverandi verslun, er fyrirspurnunum breytt til að tryggja að leitarniðurstöðurnar innihaldi allar gjaldgengar pantanir sem nota einhvers konar afhendingarmáta fyrir sótta pöntun. Notendur sölustaðar geta einnig notað fyrirliggjandi síur til að þrengja listann yfir pantanir niður í tiltekinn afhendingarmáta sóttrar pöntunar. Til dæmis geta þeir sýnt aðeins pantanir fyrir sótt fyrir utan verslun.

    ![Sía fyrir afhendingarmáta sendingar notuð fyrir lista pantana sem eru afturkallaðar.](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Það sem skal hafa í huga varðandi dreifingarstjórnun pöntunar

Eiginleikar [dreifingarstjórnunar pöntunar (DOM)](https://docs.microsoft.com/dynamics365/commerce/dom) í Commerce hunsa allar sölulínur sem eru merktar að verði sóttar í verslun. Þessir eiginleikar hafa verið uppfærðir til að tryggja að sölulínur sem eru tengdar við skilgreinda afhendingarmáta fyrir sóttar pantanir líti framhjá DOM-reglunni og verði ekki endurúthlutaðar á nýtt vöruhús uppfyllingar.
