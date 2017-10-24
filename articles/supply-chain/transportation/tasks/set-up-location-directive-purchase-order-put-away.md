--- 
title: "Setja upp leiðbeiningar um staðsetningu fyrir frágang innkaupapöntunar"
description: "Þessi verklýsing sýnir hvernig á að setja upp einfaldar staðsetningarleiðbeiningar."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45e1e54c807597d4d5ff7370748012cbf28c1c6b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Setja upp leiðbeiningar um staðsetningu fyrir frágang innkaupapöntunar

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp einfaldar staðsetningarleiðbeiningar. Dæmið sem er sýnt stofnar staðsetningarleiðbeiningar til að nota til að ákvarða hvar á að setja vörur sem hafa verið mótteknar fyrir innkaupapöntun. Hægt er að nota þessar verkefnaleiðbeiningar með nefndum gögnum með notkun sýnifyrirtækisins USMF. Frumskilyrði: Þú þarft að stofna ráðstöfunarkóða. Í þessu ferli notum við ráðstöfunarkóða sem kallast Endurmerkja. Ef þú ert að stofna staðsetningarleiðbeiningar í eigin gögnum þarftu að hafa sett upp ítarlegt vöruhúsakerfi fyrir vöruhúsið þitt og vörurnar.  Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.

1. Fara í vöruhúsakerfi  > Uppsetning  > Staðsetningarleiðbeiningar.
2. Í reitnum Verkbeiðni velurðu „Innkaupapantanir“.

## <a name="create-a-location-directive-header"></a>Stofna haus staðsetningarleiðbeininga
1. Smellið á „Nýtt“.
2. Í reitinn raðnúmer skal slá inn númer.
    * Þetta er röðin sem staðsetningarleiðbeiningar eru unnar fyrir valda vinnutegund. Einnig er hægt að breyta röð, ef þörf krefur.  
3. Í reitinn Heiti skal slá inn gildi.
    * Þetta er einkvæmt auðkenni fyrir þessar leiðbeiningar.  
4. Í reitnum Vinnutegund velurðu ‚Frágangur‘.
    * Veldu gerð vinnu sem á að framkvæma. Frágangur er aðeins stutt gildi fyrir fyrirmæli með vinnugerðinni Innkaupapöntun.  
5. Í reitinn Svæði skal slá inn gildi.
6. Í reitinn vöruhús skal slá inn gildi.
    * Hafðu leiðbeiningarkóðann auðan.  Leiðbeiningarkóðar eru notaðir til að tengja línu verkbeiðnar af gerðinni Frágangur við tilgreindar leiðbeiningar. Fyrir innkaupapantanir er staðsetning síðustu línu verkbeiðni af gerðinni Frágangur leyst áður en vinnusniðmátið er ákvarðað. Þess vegna er ekki hægt að tengja síðustu línuna í vinnusniðmáti við tilgreindar leiðbeiningar.   
7. Í reitnum Ráðstöfunarkóði skal slá inn gildi.
    * Ráðstöfunarkóði takmarkar notkun staðsetningarleiðbeiningar, þannig að staðsetningarleiðbeiningar eru aðeins notaðar ef starfsmaður í vöruhúsi færir inn þennan sérstakt gildi við skráningu með farsíma.  
8. Smellið á „Vista“.

## <a name="edit-the-query-for-directive"></a>Breyta fyrirspurn um fyrirmæli
1. Smellt er á Breyta fyrirspurn.
    * Notkun þessarar tilskipunari takmarkast við notkun vörur sem skráðar eru í vöruhúsinu sem er tilgreind, og með ráðstöfunarkóða sem er tilgreint. Hægt er að bæta fleiri skorðum við fyrirspurnina.  
2. Smellið á „Í lagi“.

## <a name="add-directive-lines"></a>Bæta við leiðbeiningarlínum.
1. Smellið á „Nýtt“.
    * Þetta er röðin sem línur staðsetningarleiðbeiningar eru unnar fyrir valda vinnutegund. Einnig er hægt að breyta röð, ef þörf krefur.  
2. Í reitnum Frá-magnið skal slá inn númer.
    * Þetta er lægsta magn sem þessi tilskipunarlína gildir fyrir.  
3. Í reitinn Til magn skal slá inn númer.
4. Í reitnum Eining skal slá inn gildi.
    * Einingin sem „Frá magn“ og „Til magn“ er gefin upp í. Ef þessi reitur er auður er birgðaeining vörunnar notuð.  
5. Veljið valkost í reitnum Finna magn.
    * Ekkert, eða magn á númeraplötu: Magn skráð á hverja númeraplötu. Einingamælt magn: allt magnið sem er skráð. Eftirstöðvar: Magnið sem enn á eftir að skrá úr innkaupapöntunarlínunni. Væntanlegt magn: Heildarmagn sem er tilgreint í innkaupapöntunarlínunni.  
6. Merkja eða afmerkja gátreitinn Takmarka eftir einingu.
    * Ef þessi valkostur er valinn, og tilgreinir eininguna á síðunni Takmarka eftir einingu, er aðeins hægt að setja vörur með þá mælieiningu inn í staðsetningu. Til dæmis, ef mælieiningin er bretti þá er aðeins hægt að setja vörur í brettum á tilteknum stað.  
7. Merkja eða afmerkja við gátreitinn Leyfa að skipta.
    * Gerir það kleift að skipta magni á mörgum stöðum.  
8. Smellið á „Vista“.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Takmarka leiðbeiningarlínu við tilgreinda einingu
1. Smellt er á Takmarka eftir einingu.
    * Þessi hnappur er aðeins tiltækur þegar smellt er á Vista eftir að gátreiturinn Takmarka eftir einingu hefur verið valinn.  
2. Í reitnum Eining skal slá inn gildi.
3. Lokið síðunni.

## <a name="add-a-location-directive-action-line"></a>Bæta við aðgerðalínu staðsetningarleiðbeininga
1. Smellið á „Nýtt“.
    * Þetta er röðin sem aðgerðalínur staðsetningarleiðbeiningar eru unnar fyrir valda vinnutegund. Einnig er hægt að breyta röð, ef þörf krefur.  
2. Í reitinn Heiti skal slá inn gildi.
    * Þetta er einkvæmt auðkenni fyrir þessar leiðbeiningargerð.  
3. Veljið valkost í svæðinu Notkun fastrar staðsetningar.
    * Fastar og ekki-fastar staðsetningar: Allar staðsetningar sem ekki eru fastar sem og eigin föst staðsetning vöru, innan sviðsins sem er tilgreint í fyrirspurninni.  Aðeins föst staðsetning fyrir vöruna: Fastar staðsetningar fyrir vöruna eru gildar, og öll vöruafbrigði deila sama setti fastra staðsetninga. Aðeins fastar staðsetningar fyrir afurðarafbrigðin: Aðeins fastar staðsetningar tilgreindar fyrir hvert afurðarafbrigði eru gildar.  
4. Í reitnum Stefna skal velja valkost.
    * Verkbeiðnir af gerðinni Innkaupapöntun styðja eftirfarandi áætlanir: Ekkert: varan er staðsett á fyrstu staðsetningunni sem finnst. Steypa saman: Varan er staðsett þar sem svipaðar vörur eru þegar tiltækar. Tóm staðsetning með engin verk á innleið: varan er staðsett á fyrstu tómu staðsetningu sem finnst. Staðsetning er talin vera tóm ef hún hefur engar efnislegar birgðir og enga væntanlega vinnu á innleið.  
5. Smellið á „Vista“.

## <a name="edit-the-query-for-directive-action-line"></a>Breyta fyrirspurn um línu leiðbeiningaraðgerða
1. Smellt er á Breyta fyrirspurn.
2. Smelltu á Bæta við.
3. Í svæðinu Svæði skal slá inn "Auðkenni forstillingar staðsetningar".
    * Í þessu dæmi takmörkum við hugsanlegar staðsetningar með kenni forstillingar staðsetningar.  
4. Í reitinn Skilyrði skal slá inn gildi.
5. Smellið á „Í lagi“.
    * Þú getur haldið áfram að bæta við leiðbeiningarlínum og leiðbeiningaraðgerðum þar til að þú hefur náð yfir allar mögulegar aðstæður í vöruhúsinu.  


