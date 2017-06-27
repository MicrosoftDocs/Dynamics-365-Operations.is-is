---
title: "Umbreyta bókhaldi eða skýrslugjaldmiðlum"
description: 
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 728af2fff6317c17e47d48ea07dbeb57068fbf3f
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="convert-accounting-or-reporting-currencies"></a>Umbreyta bókhaldi eða skýrslugjaldmiðlum

[!include[banner](../includes/banner.md)]




Fyrirtæki°sem verður að breyta bókhaldsgjaldmiðli eða skýrslugjaldmiðli sínum hefur tvo valkostir. Fyrsti valkostur er að stofna nýtt fyrirtæki og byrja upp á nýtt. Annar kostur er að keyra umbreytingarferli bókhalds- og skýrslugjaldmiðla. Þetta er mjög langt ferli sem breytir hverri færslu í kerfinu. Einnig er krafist einhverrar uppsetningar áður en hægt er að keyra ferlið.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Undirbúa lögaðila fyrir umreikning gjaldeyris
Áður en hægt er að umreikna gjaldmiðil lögaðilans, verður að bakfæra allar endurmatsupphæðir erlends gjaldmiðils fyrir lykla viðskiptavina og lánardrottna og loka fyrri reikningsárum. Einnig þarf að undirbúa gagnagrunninn fyrir umreikning, og gera nauðsynlegar breytingar á lögaðilalyklinum sem er að undirgangast umreikning á gjaldmiðli. Eftir að umreikningi á gjaldmiðli er lokið verður að ljúka ákveðnum viðbótaraðgerðum. Það þarf að afstemma sléttunarmun í umreiknuðum upphæðum, endurreikna viðskiptatalnagögn, skrá fjárhagsfærslur, takmarka aðgang að umreikningstæki og endurmeta upphæðir í erlendum gjaldmiðli fyrir lykla viðskiptavina og lánardrottna.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Setja upp°lykla fyrir sjálfvirkar færslur
Við umreikningsferli gjaldmiðils, eru hagnaður eða tap eða auramismunur, bókaðar á lykla sem eru skilgreindar á síðunni **Fjárhagslyklar fyrir sjálfvirkar færslur**. Aðallyklum þarf að úthluta til eftirfarandi færslugerða áður en umreikningur vinnslu er keyrður:

-   Hagnaður af umreikningi bókhaldsgjaldmiðils
-   Tap af umreikningi bókhaldsgjaldmiðils
-   Auramismunur í bókhaldsgjaldmiðli
-   Auramismunur í skýrslugjaldmiðli
-   Niðurstaða í árslok

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Bókun sléttunarmunar og endurútreiknings upphæða
Eftirfarandi upplýsingar útskýra hvar mismunur í sléttun getur komið upp:

-   Ef verði á vörum hefur verið breytt í 0 (núll) er skýrsla prentuð, sem birtir vörunúmer,aeiningartegund, verð fyrir umreikning og einingu.
-   Sléttunarmunur á milli virðisaukaskatts og fjárhags er bókaður í almenna færslubók.
-   Upphæðir fyrir endurmat á erlendum gjaldmiðli eru endurreiknaðar og upphæðir viðskiptavina og lánardrottna eru endurreiknaðar.
-   Uppgjörsskýrslur viðskiptavina og lánardrottna eru stofnaðar fyrir sléttunarmismun fyrir hverja viðskiptamanns- og lánardrottnafærslu.
-   Sléttunarmunur á milli viðskiptavina og lánardrottna er bókaður í almenna færslubók
-   Jafnaðar kostnaðarupphæðir og kostnaðarleiðréttingarupphæðir í lokuðum birgðafærslum eru endurreiknaðar.
-   Sléttunarmun í birgðastjórnun eru bókuð í almennu færslubókina.
-   Lagerbirgðir eru endurreiknaðar.
-   Samtala upphæða í færslubók fjárhags endurreiknaðar.
-   Lokunarskjöl fjárhags eru endurreiknuð.
-   Fjárhagsstöður eru endurreiknuðar.
-   Sléttunarmun í fjárhag eru bókuð í almennu færslubókina.
-   Opnar fjárhagsfærslur eru endurreiknaðar.
-   Endanleg upphæð í stöðum fjárhagur er reiknaður.

Ef verið er að umreikna í nýja fjárhagsbókhaldsgjaldmiðilinn og villa kom upp við endurútreikning á samtölu upphæða eða bókun á sléttunarmun, verður að loka síðunni **Gjaldmiðilsumreikningur fjárhagsbókhalds**. Heildarupphæð verða síðan endurreiknuð og sléttunarmunur verður bókaður.

## <a name="processing-the-currency-conversion"></a>Vinna úr gjaldmiðilsumreikningi
Þegar umreikningsferli gjaldmiðils er ræst verða allir notendur að skrá sig út úr kerfinu. Skilgreina°þarf nýjan fjárhag eða skýrslugjaldmiðil og gengi. Þegar smellt er á **Í lagi**, keyrir ferlið og uppfærir hverja færslu í kerfinu. Umreikningur á gjaldmiðli er mjög langt ferli. Þegar því er lokið, sést að bókhald eða skýrslugjaldmiðill er uppfært á síðunni **Fjárhagur**.

## <a name="completing-the-currency-conversion"></a>Ljúka gjaldmiðilsumreikningi.
Allar afstemmingarskýrslur þurfa að vera virkjaðar aftur eftir umreikning til að ganga úr skugga um að allar umreiknaðar upphæðir séu réttar.

-   Ef breyting á fjárhagsbókhaldsgjaldmiðli veldur sléttunarmun, er sá mismunur ekki bókaður með því fylgiskjali þar sem sléttunarmismunur varð. Í staðinn er mismunurinn bókaður með fylgiskjali sem fært var inn fyrir umreikningsbókun. Eftir umreikning munu allar skýrslur sem villuleita eftir fylgiskjali og dagsetningu innihalda sléttunarmuninn. Þetta er rétt og má hunsa.
-   Ef afstemmingarskýrslur viðskiptavinar og lánardrottins sýna sitthvora upphæð í samtalslínu og enginn munur var fyrir umreikninginn þarf að bóka upphæðamismuninn. Lykillinn er safnlykill fyrir viðskiptavini og lánardrottna. Mótlykillinn er fjárhagslykill fyrir tap í umreikningi eða gróða í umreikningi.

Þegar öllum fjárhagsfærslubókum hefur verið eytt, er hægt að skrá fjárhagsfærslur aftur. Smellt er á **Fjárhagur** &gt; **Tímabils** &gt; **bækur** &gt; **Færslubókaskráning**. Hægt er að endurmeta upphæðir í erlendum gjaldmiðli eftir gjaldmiðilsumreikning, ef þörf er á endurmati. Upphæðir eru endurmetnar í erlendum gjaldmiðli með því að velja **Staðlað** í svæðinu **Aðferð** fyrir endurmat.




