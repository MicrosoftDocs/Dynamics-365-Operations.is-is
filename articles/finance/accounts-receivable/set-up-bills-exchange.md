---
title: Setja upp víxla
description: Í þessari grein er fjallað um uppsetningu víxla.
author: ShivamPandey-msft
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: kfend
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 91821b10afe7cdbabd0a58b61219ce29d686c5c9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874726"
---
# <a name="set-up-bills-of-exchange"></a>Setja upp víxla

[!include [banner](../includes/banner.md)]

Í þessari grein er fjallað um uppsetningu víxla.

Víxill er rituð eða rafræn pöntun frá viðskiptavini sem tilgreinir að annar aðili, vanalega banki, eigi að borga tiltekna upphæð til fyrirtækisins. Þegar víxill er notaður sem greiðsla fyrir sölupöntunarreikning eða textareikning, er lykill viðskiptavinar tekjufærður. Tekjufærslan er tryggð með víxlinum þar til viðskiptavinur greiðir víxilinn til bankans. Vanalega er reikningurinn jafnaður með víxlinum á gjalddaga. Þegar tilkynning kemur frá bankanum að víxillinn hafi verið greiddur er hægt að loka víxlinum. Hægt er að gefa út víxil gegnum bankann á eftirfarandi tímum:

-   Á gjalddaga. Þetta kallast að senda greiðslu í innheimtu.
-   Fyrir gjalddaga, vanalega á afsláttardagsetningu sem tilgreind er í greiðsluskilmálum sem settir eru upp fyrir viðskiptavininn. Þegar færslan er bókuð er afsláttarupphæðin bókuð á kostnaðarlykil. Eftirstöðvarnar eru skuld þar til bankinn fær greiðsluna frá viðskiptavininum. Þetta kallast afsláttargreiðsla.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Setja upp bókunarreglur fyrir víxla

Notið skjámyndina **Bókunarreglur viðskiptavina** til að setja upp bókunarreglur sem nota á með víxlum, afsögn víxla, greiðslum til innheimtu, og afsláttargreiðslum. Veljið safnlykil þar sem bóka á upphæðir víxilsins í svæðinu **Safnlykill**. Þessi reikningur er debet- eða kreditfærður á grundvelli gerðar færslu víxilsins:
-   Fyrir víxla er þessi reikningur skuldfærður þegar víxill er bókaður og tekjufærður þegar afsláttargreiðsla eða greiðsluinnheimta er bókuð.
-   Fyrir afsagða víxla er þessi reikningur skuldfærður þegar afsagður víxill er bókaður.
-   Fyrir greiðsluinnheimtur er þessi reikningur skuldfærður þegar greiðsluinnheimta er bókuð.
-   Fyrir greiðsluafslætti er þessi reikningur skuldfærður þegar greiðsluafsláttur er bókaður.

Veljið lausafjárlykilinn þar sem á að bóka upphæðir víxilsins í svæðinu **jöfnunarlykill**. Þessi lykill er tekjufærður þegar víxill er jafnaður. Í svæðinu **Fyrirframgreiðslur virðisaukaskatts** skal velja safnlykilinn þar sem bóka á VSK-upphæðir þegar víxlar eru notaðir í fyrirframgreiðslur. Í svæðinu **Skuldir fyrir afsláttarlykil** skal velja lykilinn sem á að bóka afsláttarupphæðina í fyrir afsláttargreiðslur. Þessi reikningur er tekjufærður þegar afsláttargreiðsla er bókuð.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Setjið upp færibreytur viðskiptavina fyrir víxla

Á síðunni **Færibreytur viðskiptakrafna** eru sjálfgefnar bókunarreglur fyrir víxla sleginar inn á flipanum **Fjárhagur og virðisaukaskattur**. Númeraraðir eru skilgreindar á flipanum **Númeraraðir**.

## <a name="set-up-journal-names-for-bills-of-exchange"></a>Setja upp færslubókarheiti fyrir víxla


Á síðunni **Heiti færslubóka** skal stofna að minnsta kosti fimm færslubókarheiti til að nota fyrir víxla. Hér eru bókargerðirnar:
-   **Útgefinn víxil viðskiptavinar** - Stofna færslubókarheiti fyrir Útgáfu víxla.
-   **Útgefinn afsagnarvíxil viðskiptavinar** - Stofna færslubókarheiti fyrir Útgáfu afsagnarvíxla.
-   **Endurútgefinn víxil viðskiptavinar** - Stofna færslubókarheiti fyrir endurútgáfu víxla.
-   **Greiðslusending viðskiptavinar** – Stofna færslubókarheiti fyrir greiðslubók.
-   **Jafna víxil viðskiptavinar** - Stofna færslubókarheiti fyrir jöfnun víxla.

Á síðu færslubókarfylgiskjalsins fyrir hverja víxlabók skal færa inn upplýsingar um víxilinn á flipanum **Víxill**. Eftir að víxils færslubókarlínurnar eru bókaðar, er hægt að skoða þær á síðunni **Fyrirspurn um víxil** og **Talnagögn víxla**.

## <a name="set-up-methods-of-payment-for-bills-of-exchange"></a>Setja upp greiðslumáta fyrir víxla

Á síðunni **Greiðsluhættir** þarf að setja upp að minnsta kosti einn greiðsluhátt fyrir víxla. Ef átt er í viðskiptum við fleiri en einn banka, skal setja upp greiðsluhátt sem samsvarar víxilgreiðslusniði sem hver banki krefst fyrir víxla.

## <a name="set-up-payment-fees-for-bills-of-exchange"></a>Setja upp greiðsluþóknanir fyrir víxla

Greiðsluþóknun er gjald sem er tengt innheimtu greiðslna frá viðskiptavinum. Hægt er að tengja margar uppsetningarlínur greiðsluþóknunar við hverja greiðsluþóknun. Hægt er að nota uppsetningarlínur til að stjórna því hvernig sjálfgefnar upphæðir fyrir greiðslugjöld eru reiknaðar. Til dæmis er hægt að stofna uppsetningarlínur fyrir greiðslumáta, greiðsluskilgreiningar, gjaldmiðla og tímabil. Einnig er hægt að stofna uppsetningarlínur prósentu eða upphæð sem byggist á dagabilum. Til dæmis er hægt að stofna vaxtaprósentu sem byggist á þeirri tímalengd sem greiðslan fer framyfir gjalddaga. Ef að bankinn tekur mismunandi gjöld fyrir mismunandi greiðslugerðir, eins og **Innheimta** eða **Afsláttur**, setjið upp aðskildar greiðsluþóknunarlínur fyrir hverja greiðslugerð.

## <a name="set-up-remittance-fees-for-bank-remittance-files"></a>Setja upp greiðslugjöld fyrir bankagreiðsluskrár

Á síðunni **Bankareikningar** er hægt að setja upp greiðslugjöld sem banki tekur til greiðslu fyrir allar gjaldskrár sem eru myndaðar. Greiðslugjöldin eru bókuð þegar greiðslan hefur verið staðfest og raunupphæðir gjaldsins komnar í ljós. Greiðslugjöld eru frábrugðin greiðsluþóknunum sem eru innheimtar af viðskiptavinum og eru tengdar færslubókarlínum.

## <a name="set-up-document-layouts-for-bills-of-exchange"></a>Setja upp útlit skjals fyrir víxla

Á síðunni **Bankareikningar** er smellt á **Setja upp** og tilgreint útlit skjalsins sem er nauðsynlegt fyrir hvern bankareikning þar sem á að mynda skjöl fyrir prentaða víxla.

## <a name="set-up-customers-for-bills-of-exchange"></a>Setja upp viðskiptavini fyrir víxla

Á síðunni **Viðskiptamenn** er fyrir hvern viðskiptavin sem hefur samþykkt að greiða með því að nota víxil, hægt að setja upp sjálfgefinn greiðsluhátt fyrir víxla á flipanum **Vanskil greiðslu**.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
