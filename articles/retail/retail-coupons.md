---
title: "Búa til afsláttarmiða fyrir smásölu"
description: "Þetta efnisatriði gefur yfirlit yfir smásöluafsláttarmiða og útskýrir hvernig á að setja þá upp."
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9b4e792cae66e38546b3bdfdfbd59a2e36d891c2
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="create-coupons-for-retail-sales"></a>Búa til afsláttarmiða fyrir smásölu

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Yfirlit yfir afsláttarmiða

Afsláttarmiðar eru kóðar og strikamerki sem eru notuð til að setja smásöluafslætti inn í færslur. Hver afsláttarmiði gefur haft marga kóða og hver kóði getur haft sinn gildistíma. 

Hver afsláttarmiði tengist einum smásöluafslætti. Verðflokkurinn sem tengist afslættinum skilgreinir viðskiptavinina sem geta notað afsláttarmiðann eða rásina þar sem afsláttarmiðinn er gildur. 

Í raun eru afsláttarmiðar viðbót við smásöluafslætti. Afsláttarmiðinn felur í sér nauðsynlega afsláttarmiðakóða og strikamerki, ásamt tímabilum fyrir þessa kóða. Afsláttarmiðinn gefur einnig valkvæm notkunartakmörk og nauðsynlega eiginleika viðskiptavina. Í afslættinum kemur fram fyrir hvaða afurðahóp afsláttarmiðinn gildir. Verðflokkarnir fyrir afsláttinn hafa að geyma safn viðskiptavina, rásir eða vörulista sem afsláttarmiðinn gildir fyrir.

Til að stofna afsláttarmiða stofnarðu afsláttinn og afsláttarmiðinn í sitthvoru lagi. Þú tengir þá svo saman með því að velja afsláttinn á afsláttarmiðasíðunni í Microsoft Dynamics 365 for Retail. 

> [!NOTE]
> Eftir að afsláttarmiði er tengdur við afslátt verða nokkrir reitir á afsláttarsíðunni í Microsoft Dynamics 365 for Retail skrifvarðir, þar sem þeim er stýrt af stillingum afsláttarmiðans. Þessir reitir innihalda reitina fyrir stöðu og stöðluð dagsetningabil.

### <a name="limited-use-coupons"></a>Afsláttarmiðar með takmarkaða notkun

Hægt er að skilgreina afsláttarmiða þannig að notkun þeirra sé takmörkuð. Notkunartakmörk er hægt að skilgreina á viðskiptavin eða rás, eða sem algild mörk. Þessum mörkum er beitt þegar kóði eða strikamerki er slegið inn eða skannað á sölustað eða við skráningu sölupöntunar.

Þessum mörkum er beitt fyrir hvern kóða á afsláttarmiða. Til dæmis er hægt að nota einnota afsláttarmiða sem hefur tvo kóða tvisvar sinnum, einu sinni fyrir hvorn afsláttarmiðakóða. Hægt er að stilla hvorn kóðann á afsláttarmiða sem virkan, óháð hvorum öðrum.

> [!NOTE]
> Þegar kóða afsláttarmiða hefur náð notkunartakmörkum breytir kerfið *ekki* sjálfkrafa stöðu kóða afsláttarmiðans í „Notaður“. Kerfið leyfir þó ekki frekari notkun á kóða afsláttarmiða sem hefur náð notkunartakmörkum sínum. Ef staða á kóða afsláttarmiða er handvirkt stillt á allt nema „Virkur“ þá er ekki hægt að nota þennan kóða afsláttarmiða í neinni rás.

## <a name="managing-coupons"></a>Stjórnun afsláttarmiða

Það verður að stofna afsláttinn og afsláttarmiðann í sitthvoru lagi. Síðan eru þeir tengdir með því að velja afsláttinn á afsláttarmiðasíðunni. Eftir að afsláttarmiði er tengdur við afslátt verða nokkrir reitir afsláttarins skrifvarðir, þar sem þeim er stýrt af stillingum afsláttarmiðans. Þessir reitir innihalda reitina fyrir stöðu og stöðluð dagsetningabil.  

Í raun eru afsláttarmiðarni nú viðbót við smásöluafslætti. Afsláttarmiðinn felur í sér afsláttarmiðakóða og strikamerki, ásamt tímabilum, notkunartakmörkum og nauðsynlegum eiginleikum viðskiptavina. Í afslættinum kemur fram fyrir hvaða afurðahóp afsláttarmiðinn gildir. Verðflokkarnir fyrir afsláttinn hafa að geyma safn viðskiptavina, rásir eða vörulista sem afsláttarmiðinn gildir fyrir.

## <a name="system-setup-for-coupons"></a>Kerfisuppsetning fyrir afsláttarmiða 

Áður en hægt er að setja upp afsláttarmiða verður að setja upp strikamerki og tvær númeraraðir afsláttarmiða. 

1.  Á síðunni **Stafir sniðmáts** skal stofna nýjan staf sniðmáts fyrir afsláttarmiðakóðann. Þú getur valið hvaða ónotaða staf sem er.
2.  Á síðunni **Uppsetning sniðmáts fyrir strikamerki** skal stofna nýtt sniðmát fyrir strikamerki. Stilltu reitinn **Gerð** á **Afsláttarmiði**.
3.  Á síðunni **Uppsetning strikamerkis** skal stofna nýtt strikamerki sem notast við sniðmát strikamerkis sem þú varst að stofna.
4.  Á síðunni **Númeraraðir** skaltu stofna tvær nýjar númeraraðir. Ein númeraröð er fyrir kenni afsláttarmiðakóða og hin röðin er fyrir númer afsláttarmiðans. Kenni afsláttarmiðans er einkvæmt kenni fyrir hvern kóða á afsláttarmiða. Afsláttarmiðanúmerið er einkvæmt kenni fyrir afsláttarmiða. Hver afsláttarmiði getur haft marga kóða og strikamerki sem virkjar afsláttarmiðann.

    > [!NOTE]
    > Það verður að stilla reitinn **Gildissvið** á **Fyrirtæki** fyrir báðar númeraraðir. Í flestum tilvikum ættirðu að framkalla bæði raðnúmerin sjálfvirkt.

5.  Á síðunni **Færibreytur smásölu** í flipanum **Strikamerki** skal velja strikamerkið sem var stofnað áðan.
6.  Á síðunni **Samnýttar færibreytur smásölu** í flipanum **Númeraraðir** skal velja númeraröðina sem var stofnuð fyrir númer afsláttarmiða og auðkenniskóða afsláttarmiða.
7.  Nú getur þú opnað síðuna **Afsláttarmiðar** og stofnað nýja afsláttarmiða.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Áhrif hlutauppfærslna á afsláttarmiða

Margir aðgreindir eiginleikar í Dynamics 365 for Retail mynda virkni afsláttarmiða. Hægt er að uppfæra Microsoft Dynamics 365 for Retail headquarters (HQ) og rásina að hluta á milli eininga. Þess vegna er mikilvægt að skilja hvernig hlutauppfærslur hafa áhrif á virkni afsláttarmiða í heild sinni.

- **HQ er uppfært að hluta en smásöluþjónn og sölustaður eru ekki uppfærðir.** Í uppfærslu á HQ er afsláttarmiði og afsláttarsíða uppfærð og smásöluverðskerfið er einnig uppfært. Ef aðeins ein af þessum tveimur einingum er uppfærð passa sumar síður í Retail ekki við gögn fyrir verðútreikning. Þar af leiðandi gætu óvæntir útreikningar á afsláttum eða villur komið upp við útreikning á afsláttum.
- **HQ er uppfært en smásöluþjónn og sölustaður eru ekki uppfærðir (N-1).** Þar sem ekki er hægt að uppfæra allar smásöluverslanir samtímis mælum við með því að þú uppfærir HQ áður en smásöluverslanir eru uppfærðar. Í N-1 tilfellinu verður ný virkni sem tengist afsláttarmiðum ekki tiltæk í verslunum sem hafa ekki verið uppfærðar enn. Til dæmis innleiðir afsláttarmiðavirkni „útilokaðar“ línur. Ef þú útilokar línur í afslætti eru þær ekki notaðar í smásöluverslun sem notast við eldri útgáfu.
- **HQ er ekki uppfært en smásöluþjónn og sölustaður er uppfærður (N+1).** Þar sem uppfært verðkerfi í smásöluþjóni getur höndlað eldri afsláttarmiðakóða í verðútreikningi ætti uppfærslan ekki að hafa nein áhrif á virkni í þessu tilfelli.

