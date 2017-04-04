---
title: "Setja upp víxla"
description: "Í þessu efnisatriði er fjallað um uppsetningu víxla."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Setja upp víxla

Í þessu efnisatriði er fjallað um uppsetningu víxla.

Víxill er rituð eða rafræn pöntun frá viðskiptavini sem tilgreinir að annar aðili, vanalega banki, eigi að borga tiltekna upphæð til fyrirtækisins. Þegar víxill er notaður sem greiðsla fyrir sölupöntunarreikning eða textareikning, er lykill viðskiptavinar tekjufærður. Tekjufærslan er tryggð með víxlinum þar til viðskiptavinur greiðir víxilinn til bankans. Yfirleitt er reikningurinn jafnaður með víxlinum á gjalddaga. Þegar tilkynning kemur frá bankanum að víxillinn hafi verið greiddur er hægt að loka víxlinum. Hægt er að gefa út víxil gegnum bankann á eftirfarandi tímum:

-   Á gjalddaga. Þessi aðferð er þekkt sem greiðsla vegna innheimtu.
-   Fyrir gjalddaga, vanalega á afsláttardagsetningu sem tilgreind er í greiðsluskilmálum sem settir eru upp fyrir viðskiptavininn. Þegar færslan er bókuð er afsláttarupphæðin bókuð á kostnaðarlykil. Eftirstöðvarnar eru skuld þar til bankinn fær greiðsluna frá viðskiptavininum. Þessi aðferð er þekkt sem greiðsla vegna afsláttar.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Setja upp bókunarreglur fyrir víxla
Nota skal **bókunarreglur Viðskiptavina** síðu til að setja upp bókunarreglur sem nota má með víxlum, afsögn víxla, greiðslum til innheimtu og afsláttargreiðslum. Í því **safnlykil** svæðinu, veljið safnlykilinn þar sem bóka á upphæðir víxilsins í. Lykillinn er debet eða kredit, eftir gerð víxil:
-   Fyrir víxla er þessi reikningur skuldfærður þegar víxill er bókuð og henni er tekjufærður þegar afsláttargreiðsla eða greiðsluinnheimta er bókuð.
-   Fyrir afsagða víxla er þessi reikningur skuldfærður þegar afsagður víxill er bókaður.
-   Fyrir greiðsluinnheimtur er þessi reikningur skuldfærður þegar greiðsluinnheimta er bókuð.
-   Fyrir greiðsluafslætti er þessi reikningur skuldfærður þegar greiðsluafsláttur er bókaður.

Í í **Jöfnunarlykill** skal velja lykilinn til að bóka upphæðir víxilsins í reiðufé. Þessi lykill er tekjufærður þegar víxill er jafnaður. Í í **fyrirframgreiðslur virðisauka** svæðinu, veljið safnlykilinn þar sem bóka á vsk-upphæðir þegar víxlar eru notaðir í fyrirframgreiðslur. Í því **Skuldir vegna afsláttarlykils** svæðinu, veljið reikninginn þar sem bóka á afsláttarupphæðina fyrir afsláttargreiðslur til. Þessi reikningur er tekjufærður þegar afsláttargreiðsla er bókuð.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Setja upp færibreytur viðskiptavina fyrir víxla
Á við **Færibreytur viðskiptakrafna** síðuna sjálfgefna bókunarreglur fyrir víxla sem eru færðar inn í á **Fjárhags og virðisaukaskatts** flipanum. Númeraraðir eru skilgreindar í á **Númeraraðir** flipa.
Setja upp færslubókarheiti fyrir víxla
------------------------------------------

Í því **nöfnum Færslubóka** síðunni, stofna að minnsta kosti fimm færslubókarheiti til að nota fyrir víxla. Hér eru færslubókargerðirnar:
-   **Útgefinn víxil viðskiptavinar** -að Stofna færslubókarheiti fyrir Útgáfu víxla.
-   **Mótmæla víxli viðskiptavinar** – Stofna færslubókarheiti fyrir afsagnarbók víxils.
-   **Endurútgáfu víxils viðskiptavinar** – Stofna færslubókarheiti fyrir Endurútgáfu víxils.
-   **Greiðslusending viðskiptavinar** – Stofna færslubókarheiti fyrir greiðslubók.
-   **Jafna víxil viðskiptavinar** – Stofna færslubókarheiti fyrir jöfnunarbók víxils.

Fylgiskjal síðan færslubók fyrir hverja víxilbók, sláið inn upplýsingar um víxilinn í **víxils** flipa. Eftir víxils færslubókarlínurnar eru bókaðar, er hægt að skoða þær á þá **fyrirspurn um víxil** síðu og **talnagögn víxla** síðu.
Setja upp greiðslumáta fyrir víxla
-----------------------------------------------

Á við **Greiðsluhættir** síðu er að setja upp að minnsta kosti einn greiðsluhátt fyrir víxla. Ef átt er í viðskiptum við fleiri en einn banka, setjið upp greiðsluhátt sem samsvarar greiðslusnið sem hver banki krefst fyrir víxla.
Setja upp greiðsluþóknanir fyrir víxla
-----------------------------------------

Greiðsluþóknun er gjald sem er tengt innheimtu greiðslna frá viðskiptavinum. Margar greiðsluþóknunaruppsetning línur getur verið tengt hver greiðsluþóknun. Hægt er að nota uppsetningarlínur til að stjórna því hvernig sjálfgefnar upphæðir fyrir greiðslugjöld eru reiknaðar. Til dæmis er hægt að stofna uppsetningarlínur fyrir greiðslumáta, greiðsluskilgreiningar, gjaldmiðla og tímabil. Einnig er hægt að stofna uppsetningarlínur fyrir prósentu eða upphæð sem er byggða á dagabilum. Til dæmis er hægt að setja upp vaxtaprósentu sem byggir á lengd þess tíma sem greiðslan fer framyfir gjalddaga. Ef að bankinn tekur mismunandi gjöld fyrir mismunandi greiðslugerðir, eins og **Innheimtubréf** eða **Afsláttur**, setja upp aðskildar greiðsluþóknunarlínur fyrir hverja greiðslugerð.
Setja upp greiðslugjöld fyrir bankagreiðsluskrár
------------------------------------------------

Á við **bankareikninga** síðu er hægt að setja upp greiðslugjöld sem banki innheimtir fyrir allar gjaldskrár sem eru mynduð. Greiðslugjöldin eru bókuð þegar greiðslan hefur verið staðfest og raunupphæðir gjaldsins komnar í ljós. Greiðslugjöld frábrugðnar greiðsluþóknanir sem eru safnað frá viðskiptavinum og eru tengdar færslubókarlínum.
Setja upp útlit skjals fyrir víxla
---------------------------------------------

Á við **bankareikninga** síðunni er smellt á **Setja upp**, og tilgreina það útlit skjals sem krafist er fyrir hvern bankareikning sem á að mynda prentaða víxla skjöl fyrir.
Setja upp viðskiptavini fyrir víxla
--------------------------------------

Á við **Viðskiptavini** síðunni, fyrir hvern viðskiptavin sem hefur samþykkt að greiða með því að nota víxil, er hægt að setja upp sjálfgefinn greiðsluhátt fyrir víxla á á **sjálfgildi Greiðslu** flipa.




