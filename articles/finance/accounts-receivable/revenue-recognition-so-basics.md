---
title: Tekjuskráning í sölupöntunum
description: Þessi grein lýsir grunnvirkni við samþykki á tekjum í sölupöntunum og reikningum. Tekjuskráning er tiltæk í sölupöntuninni og á samsvarandi reikningi sem er búinn til út frá sölupöntuninni.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5df7341160940f5c5db0dd4c5d86e4d9698d22e2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899958"
---
# <a name="revenue-recognition-on-sales-orders"></a>Tekjuskráning í sölupöntunum

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Ekki er hægt að kveikja á tekjuskráningareiginleikanum í gegnum eiginleikastjórnun. Nota verður skilgreiningarlykil til að kveikja á honum.

Þessi grein lýsir grunnvirkni við samþykki á tekjum í sölupöntunum og reikningum. Tekjuskráning er tiltæk í sölupöntun og á samsvarandi reikningi sem er búinn til út frá sölupöntuninni. Einnig er hægt að stofna sölupöntunina í gegnum tíma- og efnisverk.

> [!NOTE]
> Á skýringarmyndum í þessari grein hafa dálkar verið faldir eða þeim bætt við hnitanet til að skýra hugtök betur. Þar af leiðandi gætu síður og gögn á skýringarmyndum verið frábrugðnar því sem sést í vörunni.

## <a name="enter-a-sales-order"></a>Færa inn sölupöntun

Eftirfarandi sölupöntun er færð inn og hún inniheldur þrjár vörur sem eru settar upp fyrir tekjuskráningu.

[![Færa inn sölupöntun.](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Tvö hugtök eru til um tekjuskráningu:

- **Ákvarða tekjuupphæðina.** Tekjuupphæðin er reiknuð út frá uppsetningu útgefinna afurða. Tekjuupphæðin birtist aldrei viðskiptavininum og er aðeins notuð fyrir bókhald sölupöntunarreikningsins. Sölupöntunarlínurnar og skjölin sem eru prentuð út sem hluti af sölunni halda áfram að sýna eininguna/listaverðin.
- **Ákvarðið hvenær tekjuskráning skal eiga sér stað.** Tekjuáætlun er notuð til að ákvarða hvenær tekjur eru skráðar.

    Í þessu dæmi er fyrsta atriðið, S0001, úthlutað á **1O** (eitt tilvik) tekjuáætlunar. Þessi lína táknar atburðarás sem markar tímamót, þar sem tekjurnar verða skráðar eftir að uppsetning á sér stað í framtíðinni. Því verður tekjum frestað þar til uppsetningu er lokið.

    Önnur varan, S0008, er þjónustuvara sem er sett upp sem vara með stuðning á samningstíma (PCS). Viðvarandi verkfræðiþjónusta er veitt viðskiptavininum á 12 mánaða tímabili. Þess vegna er vörunni sjálfkrafa úthlutað **12M** tekjuáætlun. Þar sem þetta er stykkjavara þarf að skilgreina upphafs-og lokadagsetningar samnings. Sjálfgefið er að upphafs-og lokadagsetningar samningsins birtist á flipanum Vöruupplýsingar – Uppsetning. Í tekjuáætluninni er uppsetningin fyrir **12M** skilgreind þannig að samningsskilmálarnir eru fylltir út sjálfkrafa eins og sýnt er á eftirfarandi mynd.

    [![Tekjuáætlanir.](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Þriðja varan, S0012, er vélbúnaður og engri tekjuáætlun er sjálfgefið úthlutað. Tekjur af vélbúnaðinum eru staðfestar um leið og varan er reikningsfærð.

## <a name="confirm-the-sales-order"></a>Staðfesta sölupöntunina

Til að skoða viðbótarupplýsingar um tekjuupphæðina og tekjuáætlunina skal nota hnappana í flokknum **Tekjuskráning** á flipanum **Stjórna** á aðgerðarsvæði sölupöntunarinnar. Þar sem sölupöntunin er ekki staðfest á þessum tímapunkti eru hnapparnir sem eru notaðir fyrir tekjuskráningu ekki tiltækir. Þessir hnappar verða tiltækir eða ekki tiltækir eftir stigi sölupöntunarinnar þar til hún hefur verið uppfyllt.

[![Sölupöntunarhaus.](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

Fyrstu þrír hnapparnir veita upplýsingar um tekjuupphæð vara í uppsetningu sölupöntunar fyrir tekjuskráningu.

- **Úthlutun tekjuupphæðar** – Þessi hnappur er tiltækur eftir að sölupöntunin er staðfest eða reikningurinn er bókaður. Bæði staðfesting sölupöntunar og bókun reikningsins reikna út tekjurnar til að skrá verðið sem verður skráð eða frestað í bókhaldsfærslunni. Háð uppsetningunni sem um ræðir, getur útreiknuð tekjuupphæð verið frábrugðin einingarverðinu sem viðskiptavinurinn sér.
- **Endurúthluta verði með nýjum pöntunarlínum** – Þessi hnappur er tiltækur þegar sölupöntunin hefur verið staðfest eða reikningurinn hefur verið bókaður. Endurúthlutunarferlið er notað til að endurreikna tekjurnar sem verður að skrá eftir að nýrri línu er annað hvort bætt við núverandi sölupöntun, eftir að hún hefur verið reikningsfærð eða bætt við nýja sölupöntun. Í báðum tilfellum veldur viðbót á nýrri vöru breytingu á samningnum. Þar af leiðandi verður að endurúthluta tekjuupphæðinni.
- **Uppfæra úthlutun tekjuupphæðar** – Þessi hnappur er tiltækur eftir að sölupöntunin hefur verið staðfest, en er ekki tiltækur eftir að sölupöntunin hefur verið reikningsfærð. Uppfærslan er notuð til að endurkeyra úthlutun tekjuupphæðarinnar án þess að þurfa að staðfesta sölupöntunina. Eftir að sölupöntunin hefur verið reikningsfærð er ekki hægt að endurreikna tekjuupphæðina.

Síðustu tveir hnapparnir gefa upplýsingar um tekjuáætlun þeirra vara á sölupöntuninni sem eru með tekjuáætlun.

- **Áætluð tekjuskráningaráætlun** – Þessi hnappur er eftir að sölupöntunin hefur verið staðfest, en er ekki tiltækur eftir að sölupöntunin hefur verið reikningsfærð. Síða sem sýnir áætlaða tekjuáætlun opnast. Endanleg áætlun gæti breyst vegna þess að áætluð áætlun notar umbeðna sendingardagsetningu, en endanleg áætlun notar raunverulega sendingardagsetningu.
- **Áætlun tekjuskráningar** – Þessi hnappur verður tiltækur þegar sölupöntunin hefur verið reikningsfærð. Endanleg tekjuskráningaráætlun er ekki stofnuð við staðfestingu eða þegar fylgiseðill er stofnaður. Hún er aðeins stofnuð þegar sölupöntunin er reikningsfærð.

Í eftirfarandi dæmi urðu breytingar á verðúthlutun þegar sölupöntunin var staðfest. Hafa skal í huga að þrátt fyrir að tekjuupphæðum verði úthlutað á annan hátt verður heildarupphæðin í reitnum **Tekjur til skráningar** að vera jöfn samtölu þeirra sölupöntunarlína sem eru reikningsfærðar á viðskiptavininn. Til dæmis er samtala sölupöntunarlína, án skatts, $1499. Þar af leiðandi verður samtala **Tekna til skráningar** einnig að vera $1499.

[![Úthlutun á tekjuupphæð.](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Áætluð tekjuskráningaráætlun er einnig búin til. Tekjuáætlunin notar gildið fyrir **Tekjur til skráningar** sem upphæðina sem á að fresta. Vara S0001 frestar $321,21 í stað $300, og vara S0008 frestar $160,61 í stað $100. Vara S0012 er ekki sýnd í væntanlegri áætlun því tekjunum er ekki frestað. Þegar bókun á sér stað bókar vara S0012 upphæðina $1.017,18 beint í tekjufjárhagslykilinn.

[![Áætluð tekjuskráningaráætlun.](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Stofnið fylgiseðilinn

Næst er hægt að stofna fylgiseðil fyrir sölupöntunina. Engar tekjur eru skráðar þegar fylgiseðillinn er bókaður. Ef sölupöntunin var ekki staðfest mun bókun fylgiseðilsins ekki virkja útreikningi tekjuupphæð. Slíkt virkjar ekki heldur stofnun áætlaðrar eða endanlegrar tekjuskráningaráætlunar. Ef vörulíkanaflokkur er settur upp til að fresta tekjum á fylgiseðli, heldur hann áfram að bóka með núverandi fjárhagslyklum fyrir bókunarreglu, en ekki með nýjum frestuðum tekjulyklum sem notaðir eru við bókun reikninga.

## <a name="create-the-invoice"></a>Búið til reikning

Lokaskrefið er að reikningsfæra sölupöntunina. Þegar þú skoðar fylgiskjöl reikningsins tekur þú eftir því að tekjunum fyrir vörur S0001 og S0008 var frestað ($321,21 + 160,61 = 481,82) og eftirstöðvarnar fyrir vöruna S0012 voru bókaðar á tekjur (1.017,18). Þessi gildi eru samanlagt að upphæð $1.499, sem samsvarar samtölu sölupöntunarlínanna.

[![Færslur fylgiskjals.](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Þegar búið er að stofna reikninginn, verða hnapparnir **Úthlutun á tekjuupphæð**, **Endurúthlutun verðs með nýjum pöntunarlínum**, og **Tekjuskráningaráætlun** tiltækir, en hnapparnir **Uppfæra úthlutun tekjuupphæðar** og **Áætluð tekjuskráningaráætlun** verða ekki tiltækir.

[![Framboð hnappsins fyrir Tiltæka tekjuskráningu.](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

Hnappurinn **Úthlutun á tekjuupphæð** er enn tiltækur til að hægt sé að skoða útreikninginn á tekjuupphæðinni. Ef ekkert breyttist í sölupöntuninni eftir að hún var staðfest mun bókun reikningsins ekki breyta reiknaðri upphæð í reitnum **Tekjur til skráningar**.

Áætluð tekjuskráningaráætlun er fjarlægð og hennar í stað kemur endanleg tekjuskráningaráætlun. Upplýsingum um tekjuáætlun er haldið við fyrir hverja sölupöntunarlínu og eru þær notaðar til að losa um frestaðar tekjur í rauntekjur þar sem samningsbundnar skuldbindingar eru uppfylltar.

[![Endanleg tekjuskráningaráætlun.](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
