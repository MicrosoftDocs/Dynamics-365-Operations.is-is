---
title: Setja upp afsláttarmiða fyrir smásölu
description: Þetta efnisatriði gefur yfirlit yfir afsláttarmiða og útskýrir hvernig á að setja þá upp.
author: scott-tucker
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a4de42c23bf96591d1ac99ed32438fe34a485998
ms.sourcegitcommit: 05868764acd3d77970724a30c49c5ae5ffb6ca5b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5906650"
---
# <a name="set-up-coupons-for-retail-sales"></a>Setja upp afsláttarmiða fyrir smásölu

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Yfirlit yfir afsláttarmiða

Afsláttarmiðar eru kóðar og strikamerki sem eru notuð til að setja afslætti inn í færslur. Hver afsláttarmiði gefur haft marga kóða og hver kóði getur haft sinn gildistíma.

Hver afsláttarmiði tengist einum afslætti. Verðflokkurinn sem tengist afslættinum skilgreinir viðskiptavinina sem geta notað afsláttarmiðann eða rásina þar sem afsláttarmiðinn er gildur.

Í raun eru afsláttarmiðar viðbót við afslætti. Afsláttarmiðinn felur í sér nauðsynlega afsláttarmiðakóða og strikamerki, ásamt tímabilum fyrir þessa kóða. Afsláttarmiðinn gefur einnig valkvæm notkunartakmörk og nauðsynlega eiginleika viðskiptavina. Í afslættinum kemur fram fyrir hvaða afurðahóp afsláttarmiðinn gildir. Verðflokkarnir fyrir afsláttinn hafa að geyma safn viðskiptavina, rásir eða vörulista sem afsláttarmiðinn gildir fyrir.

Til að stofna afsláttarmiða stofnarðu afsláttinn og afsláttarmiðinn í sitthvoru lagi. Síðan tengirðu þá með því að velja afsláttinn á afsláttarsíðunni í Commerce.

> [!NOTE]
> Þegar afsláttarmiði er tengdur við afslátt verða nokkrir reitir á afsláttarsíðunni í Commerce skrifvarðir vegna þess að stillingar afsláttarmiða stjórna þeim. Þessir reitir innihalda reitina fyrir stöðu og stöðluð dagsetningabil.
> 
> Þegar afsláttarmiðinn er notaður í rás símavers þarf að velja hnappinn **Endurreikna** **(flipann Selja > Reikna > Endurreikna)** til að afslátturinn sem tengist afsláttarmiðanum sé notaður. Þetta viðbótarskref verður fjarlægt í útgáfum í framtíðinni.

### <a name="limited-use-coupons"></a>Afsláttarmiðar með takmarkaða notkun

Hægt er að skilgreina afsláttarmiða þannig að notkun þeirra sé takmörkuð. Notkunartakmörk er hægt að skilgreina á viðskiptavin eða rás, eða sem algild mörk. Þessum mörkum er beitt þegar kóði eða strikamerki er slegið inn eða skannað á sölustað eða við skráningu sölupöntunar.

Þessum mörkum er beitt fyrir hvern kóða á afsláttarmiða. Til dæmis er hægt að nota einnota afsláttarmiða sem hefur tvo kóða tvisvar sinnum, einu sinni fyrir hvorn afsláttarmiðakóða. Hægt er að stilla hvorn kóðann á afsláttarmiða sem virkan, óháð hvorum öðrum.

Afsláttarmiða er hægt að nota í öllum sölurásum en hinsvegar fyrir símaverspantanir geta afsláttarmiðar með takmarkaðir notkun verði notaðir fyrir þessar símaverspantanir eingöngu þar sem stillingin **Lok pöntunar** í símaverinu er virkjuð. Ef þetta er ekki virkjað er aðeins hægt að nota afsláttarmiða með ótakmarkaðri notkun í pöntunum í gegnum símaver.

> [!NOTE]
> Þegar kóða afsláttarmiða hefur náð notkunartakmörkum breytir kerfið *ekki* sjálfkrafa stöðu kóða afsláttarmiðans í „Notaður“. Hins vegar hefur þessi kóði afsláttarmiða náð notkunarmörkum og er ekki hægt að nota. Ef staða á kóða afsláttarmiða er handvirkt stillt á eitthvað annað en **Virkur** þá er ekki hægt að nota þennan afsláttarmiðakóða í neinni rás.  

## <a name="managing-coupons"></a>Stjórnun afsláttarmiða

Það verður að stofna afsláttinn og afsláttarmiðann í sitthvoru lagi. Síðan eru þeir tengdir með því að velja afsláttinn á afsláttarmiðasíðunni. Eftir að afsláttarmiði er tengdur við afslátt verða nokkrir reitir afsláttarins skrifvarðir, þar sem þeim er stýrt af stillingum afsláttarmiðans. Þessir reitir innihalda reitina fyrir stöðu og stöðluð dagsetningabil.

Í raun eru afsláttarmiðar núna viðbót við afslætti. Afsláttarmiðinn felur í sér afsláttarmiðakóða og strikamerki, ásamt tímabilum, notkunartakmörkum og nauðsynlegum eiginleikum viðskiptavina. Í afslættinum kemur fram fyrir hvaða afurðahóp afsláttarmiðinn gildir. Verðflokkarnir fyrir afsláttinn hafa að geyma safn viðskiptavina, rásir eða vörulista sem afsláttarmiðinn gildir fyrir.

## <a name="system-setup-for-coupons"></a>Kerfisuppsetning fyrir afsláttarmiða

Áður en hægt er að setja upp afsláttarmiða verður að setja upp strikamerki og tvær númeraraðir afsláttarmiða.

1. Á síðunni **Stafir sniðmáts** skal stofna nýjan staf sniðmáts fyrir afsláttarmiðakóðann. Þú getur valið hvaða ónotaða staf sem er.
2. Á síðunni **Uppsetning sniðmáts fyrir strikamerki** skal stofna nýtt sniðmát fyrir strikamerki. Stilltu reitinn **Gerð** á **Afsláttarmiði**.
3. Á síðunni **Uppsetning strikamerkis** skal stofna nýtt strikamerki sem notast við sniðmát strikamerkis sem þú varst að stofna.
4. Á síðunni **Númeraraðir** skaltu stofna tvær nýjar númeraraðir. Ein númeraröð er fyrir kenni afsláttarmiðakóða og hin röðin er fyrir númer afsláttarmiðans. Kenni afsláttarmiðans er einkvæmt kenni fyrir hvern kóða á afsláttarmiða. Afsláttarmiðanúmerið er einkvæmt kenni fyrir afsláttarmiða. Hver afsláttarmiði getur haft marga kóða og strikamerki sem virkjar afsláttarmiðann.

    > [!NOTE]
    > Það verður að stilla reitinn **Gildissvið** á **Fyrirtæki** fyrir báðar númeraraðir. Í flestum tilvikum ættirðu að framkalla bæði raðnúmerin sjálfvirkt.

5. Á síðunni **Færibreytur Commerce** í flipanum **Strikamerki** skal velja strikamerkið sem var stofnað áðan.
6. Á síðunni **Samnýttar færibreytur Commerce** í flipanum **Númeraraðir** skal velja númeraröðina sem var stofnuð fyrir númer afsláttarmiða og auðkenniskóða afsláttarmiða.
7. Nú getur þú opnað síðuna **Afsláttarmiðar** og stofnað nýja afsláttarmiða.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Áhrif hlutauppfærslna á afsláttarmiða

Virkni afsláttarmiða samanstendur af mörgum ólíkum eiginleikum. Commerce-höfuðstöðvar (HQ) og rásin er hægt að uppfæra að hluta til yfir þætti. Þess vegna er mikilvægt að skilja hvernig hlutauppfærslur hafa áhrif á virkni afsláttarmiða í heild sinni.

- **HQ er uppfært að hluta en Commerce Scale Unit og sölustaður eru ekki uppfærðir.** Í uppfærslu á HQ er afsláttarmiði og afsláttarsíða uppfærð og viðskiptaverðskerfið er einnig uppfært. Ef aðeins einn af þessum þáttum er uppfærður munu sumar síður í Commerce ekki passa við gögn um verðútreikninga. Þar af leiðandi gætu óvæntir útreikningar á afsláttum eða villur komið upp við útreikning á afsláttum.
- **HQ er uppfært en Commerce Scale Unit og sölustaður eru ekki uppfærðir (N-1).** Þar sem ekki er hægt að uppfæra allar verslanir samtímis mælum við með því að þú uppfærir HQ áður en verslanir eru uppfærðar. Í atburðarás N-1 verður ný virkni sem er tengd afsláttarmiðum ekki tiltæk í verslunum sem hafa ekki verið uppfærðar. Til dæmis kynnir virkni afsláttarmiða til sögunnar „útiloka“ línur. Ef þú útilokar línur í afslætti eru þær ekki notaðar í verslun sem notast við eldri útgáfu.
- **HQ er ekki uppfært en Commerce Scale Unit og sölustaður eru uppfærðir (N+1).** Þar sem uppfært verðkerfi í Commerce Scale Unit getur höndlað eldri afsláttarmiðakóða í verðútreikningi ætti uppfærslan ekki að hafa nein áhrif á virkni í þessu tilfelli.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
