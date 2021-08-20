---
title: Setja upp leiðbeiningar um staðsetningu fyrir frágang innkaupapöntunar
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp einfaldar staðsetningarleiðbeiningar.
author: ShylaThompson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b11d99f026f4c06b1e2c8b88acc1d9926bbc493bf1ebb851ef1b7b78daff2a9c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722224"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Setja upp leiðbeiningar um staðsetningu fyrir frágang innkaupapöntunar

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp einfaldar staðsetningarleiðbeiningar. Dæmið sem er sýnt stofnar staðsetningarleiðbeiningar til að nota til að ákvarða hvar á að setja vörur sem hafa verið mótteknar fyrir innkaupapöntun. Hægt er að nota þessar verkefnaleiðbeiningar með nefndum gögnum með notkun sýnifyrirtækisins USMF. Frumskilyrði: Þú þarft að stofna ráðstöfunarkóða. Í þessu ferli notum við ráðstöfunarkóða sem kallast Endurmerkja. Ef þú ert að stofna staðsetningarleiðbeiningar í eigin gögnum þarftu að hafa sett upp ítarlegt vöruhúsakerfi fyrir vöruhúsið þitt og vörurnar. Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.

1. Í skoðunarrúðunni ferðu í **Kerfi > Vöruhúsakerfi > Uppsetning > Vöruhús > Staðsetningarleiðbeiningar**.
2. Í reitnum **Gerð verkbeiðni** velurðu **Innkaupapantanir**.

## <a name="create-a-location-directive-header"></a>Stofna haus staðsetningarleiðbeininga
1. Veljið **Nýtt**.
2. Í reitinn **Raðnúmer** skal slá inn númer. Þetta er röðin sem staðsetningarleiðbeiningar eru unnar fyrir valda vinnutegund. Einnig er hægt að breyta röð, ef þörf krefur.  
3. Í reitinn **Heiti** skal slá inn gildi. Þetta er einkvæmt auðkenni fyrir þessar leiðbeiningar.  
4. Í reitnum **Verkbeiðni** velurðu **Frágangur**. Veldu gerð vinnu sem á að framkvæma. **Frágangur** er aðeins stutt gildi fyrir fyrirmæli með verkbeiðninni Innkaupapöntun.  
5. Í reitinn **Svæði** skal slá inn gildi.
6. Í reitinn **Vöruhús** skal slá inn gildi. Hafðu leiðbeiningarkóðann auðan.  Leiðbeiningarkóðar eru notaðir til að tengja línu verkbeiðnar af gerðinni Frágangur við tilgreindar leiðbeiningar. Fyrir innkaupapantanir er staðsetning síðustu línu verkbeiðni af gerðinni Frágangur leyst áður en vinnusniðmátið er ákvarðað. Þess vegna er ekki hægt að tengja síðustu línuna í vinnusniðmáti við tilgreindar leiðbeiningar.   
7. Í reitnum **Ráðstöfunarkóði** skal slá inn gildi. Ráðstöfunarkóði takmarkar notkun staðsetningarleiðbeiningar, þannig að staðsetningarleiðbeiningar eru aðeins notaðar ef starfsmaður í vöruhúsi færir inn þennan sérstakt gildi við skráningu með farsíma.  
8. Veljið **Vista**.

## <a name="edit-the-query-for-directive"></a>Breyta fyrirspurn um fyrirmæli
1. Veldu **Breyta fyrirspurn**. Notkun þessarar tilskipunari takmarkast við notkun vörur sem skráðar eru í vöruhúsinu sem er tilgreind, og með ráðstöfunarkóða sem er tilgreint. Hægt er að bæta fleiri skorðum við fyrirspurnina.  
2. Veljið **Í lagi**.

## <a name="add-directive-lines"></a>Bæta við leiðbeiningarlínum.
1. Veljið **Nýtt**. Þetta er röðin sem línur staðsetningarleiðbeiningar eru unnar fyrir valda vinnutegund. Einnig er hægt að breyta röð, ef þörf krefur.  
2. Í reitnum **Frá magni** skal slá inn tölu. Þetta er lægsta magn sem þessi tilskipunarlína gildir fyrir.  
3. Í reitinn **Til magns** skal slá inn númer.
4. Í reitnum **Eining** skal slá inn gildi. Einingin sem „Frá magn“ og „Til magn“ er gefin upp í. Ef þessi reitur er auður er birgðaeining vörunnar notuð.  
5. Í reitnum **Finna magn** skal velja valkost.
    - Ekkert, eða magn á númeraplötu: Magn skráð á hverja númeraplötu.  
    - Einingamælt magn: allt magnið sem er skráð.  
    - Eftirstöðvar: Magnið sem enn á eftir að skrá úr innkaupapöntunarlínunni.  
    - Væntanlegt magn: Heildarmagn sem er tilgreint í innkaupapöntunarlínunni.  
6. Merkja eða afmerkja gátreitinn **Takmarka eftir einingu**. Ef þessi valkostur er valinn, og tilgreind einingin á síðunni **Takmarka eftir einingu** er aðeins hægt að setja vörur með þá mælieiningu inn í staðsetningu. Til dæmis, ef mælieiningin er bretti þá er aðeins hægt að setja vörur í brettum á tilteknum stað.  
7. Merkja eða afmerkja við gátreitinn **Leyfa að skipta**. Gerir það kleift að skipta magni á mörgum stöðum.  
8. Veljið **Vista**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Takmarka leiðbeiningarlínu við tilgreinda einingu
1. Veldu **Takmarka eftir einingu**. Þessi hnappur er aðeins tiltækur þegar smellt er á **Vista** eftir að gátreiturinn **Takmarka eftir einingu** hefur verið valinn.  
2. Í reitnum **Eining** skal slá inn gildi.
3. Lokið síðunni.

## <a name="add-a-location-directive-action-line"></a>Bæta við aðgerðalínu staðsetningarleiðbeininga
1. Veljið **Nýtt**. Þetta er röðin sem aðgerðalínur staðsetningarleiðbeiningar eru unnar fyrir valda vinnutegund. Einnig er hægt að breyta röð, ef þörf krefur.  
2. Í reitinn **Heiti** skal slá inn gildi. Þetta er einkvæmt auðkenni fyrir þessar leiðbeiningargerð.  
3. Í reitnum **Notkun fastrar staðsetningar** skal velja valkost.
    - Fastar og ekki-fastar staðsetningar: Allar staðsetningar sem ekki eru fastar sem og eigin föst staðsetning vöru, innan sviðsins sem er tilgreint í fyrirspurninni.  
    - Aðeins föst staðsetning fyrir vöruna: Fastar staðsetningar fyrir vöruna eru gildar, og öll vöruafbrigði deila sama setti fastra staðsetninga.  
    - Aðeins fastar staðsetningar fyrir afurðarafbrigðin: Aðeins fastar staðsetningar tilgreindar fyrir hvert afurðarafbrigði eru gildar.  
4. Í reitnum **Stefna** skal velja valkost. Verkbeiðnir af gerðinni innkaupapöntun styðja eftirfarandi stefnur: 
    - Ekkert: varan er sett á fyrsta staðinn sem finnst.  
    - Steypa saman: Varan er staðsett þar sem svipaðar vörur eru þegar tiltækar.  
    - Tóm staðsetning með engin verk á innleið: varan er staðsett á fyrstu tómu staðsetningu sem finnst. Staðsetning er talin vera tóm ef hún hefur engar efnislegar birgðir og enga væntanlega vinnu á innleið.  
5. Veljið **Vista**.

## <a name="edit-the-query-for-directive-action-line"></a>Breyta fyrirspurn um línu leiðbeiningaraðgerða
1. Veldu **Breyta fyrirspurn**.
2. Veljið **Bæta við**.
3. Í reitinn **Reitur** skal slá inn `location profile ID`. Í þessu dæmi takmörkum við hugsanlegar staðsetningar með kenni forstillingar staðsetningar.  
4. Í reitnum **Skilyrði** skal slá inn gildi.
5. Veljið **Í lagi**. Þú getur haldið áfram að bæta við leiðbeiningarlínum og leiðbeiningaraðgerðum þar til að þú hefur náð yfir allar mögulegar aðstæður í vöruhúsinu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]