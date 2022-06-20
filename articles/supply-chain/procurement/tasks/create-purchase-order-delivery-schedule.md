---
title: Stofna innkaupapöntun með afhendingaráætlun
description: Þessi grein sýnir hvernig á að búa til afhendingaráætlun fyrir innkaupapöntun.
author: GalynaFedorova
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e13103f374be838a5ea0fb5e08c449b419905cab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875247"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Stofna innkaupapöntun með afhendingaráætlun

[!include [banner](../../includes/banner.md)]

Þessi grein sýnir hvernig á að búa til afhendingaráætlun fyrir innkaupapöntun. Afhendingaráætlun er notaður þegar magn í pöntun eða færslubók er beðið um að sé afhent í margar sendingar. Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins. Þetta ferli myndi yfirleitt gert af innkaupaaðila.

## <a name="create-a-delivery-schedule"></a>Stofna afhendingaráætlun
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Innkaupapantanir > Allar innkaupapantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svæðinu **Lánardrottnalykill** skal slá inn `US-101`.
4. Veljið **Í lagi**.
5. Í reitinn **Vörunúmer** slærðu inn `M0001`.
6. Í reitinn **Magn** skal slá inn `10`.
7. Velja **Innkaupapöntunarlínu**.
8. Veldu **Afhendingaráætlun**.
- Síðan **Afhendingaráætlun** leyfir þér að tilgreina fjölda sendinga þar sem heildarmagn pöntunarlínu verða afhentar frá lánardrottinn.  
- Að sjálfgefnu afritar kerfið heildarmagn og aðrar upplýsingar um afhendingu á upprunalegri innkaupalínu í fyrstu afhendingaráætlunarlínu. Í þessu dæmi stofnum við áætlun fyrir tvær sendingar og sendingardagsetning seinni sendingar er stillt viku eftir fyrstu sendinguna.  
9. Í retinum **Magn** breytirðu magninu í `4`.
10. Veljið **Nýtt**.
11. Í reitnum **Magn** skal slá inn `6` sem eftirstandandi magn.
- Í svæðinu dagsetning afhendingar velurðu dagsetningu sem er einni viku eftir dagsetningu í fyrstu afhendingarlínunni.  
- Þú getur fylgst með heildarmagn sem úthlutað er til í línur afhendingaráætlunar með því að líta á reitina **Samtölu** og **Eftirstandandi**. Þegar eftirstöðvar magns eru núll, allt magnið í upphaflegu línunni hefur verið úthlutað á áætlun.  
12. Útvíkkaðu hlutann **Umreikningur gjalda**.
- Valkostir hér gera þér kleift að stjórna því hvernig á að dreifa gjöldum yfir í línur afhendingaráætlunar. Ef valið er **Afrita brúttóupphæðir**, er gjaldupphæð á upprunaleg pöntunarlína afritað í hverja pöntunarlínu. Valkosturinn **Úthluta á afhendingarlínur** deilir upprunalegum línugjöldum samkvæmt magninu á hverri afhendingarlínu.  
13. Fella saman hlutann **Umreikningur gjalda**.
14. Veljið **Í lagi**.
- Afhendingaráætlunin hefur nú verið notuð í pöntunina.  
- Upprunalegri pöntunarlínunni, nú nefnt viðskiptalína, hefur verið breytt í pöntunarlínu með margar afhendingar. Þetta er merkt með sérstöku tákni og virkar sem haus fyrir afhendingarlínurnar.  
15. Veljið aðra pöntunarlínuna sem er sú fyrri af tveimur afhendingarlínum.
- Tvær nýjar línur sem vísað er til sem afhendingarlínur, mynda í sameiningu eina afhendingaráætlun. pöntunina verður unnin gegn þessum línum og ekki gagnvart upphaflegu línunni. Ef skjöl eins og staðfestingar, færslubók innhreyfingarskjals, eða reikninga eru prentaðar, eru eingöngu afhendingarlínur sýndar.  

## <a name="change-the-delivery-schedule"></a>Breyta Afhendingaráætlun
Hægt er að breyta magni í afhendingarlínum. Ef þetta er gert er viðskiptalínan uppfærð sjálfkrafa í heildarmagn í afhendingarlínunum.  
1. Í reitnum **Magn** í fyrstu afhendingarlínu, skal breyta magninu úr `4` í `5`.
2. Veljið fyrsta pöntunarlínu (viðskiptalínuna).  
- Magn á viðskiptalínunni hefur verið breytt í 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Vinna úr innhreyfingarskjal afurða með afhendingaráætlanir
Þarf að staðfesta innkaupapöntun áður en hægt er að vinna úr innhreyfingarskjali afurða. Í þessu tilfelli er móttakan yfirleitt skráðar beint á Innkaupapöntunina. Kvittunin gæti einnig hafa verið skráð þegar vörurnar komu í vöruhúsinu.  
1. Í aðgerðasvæðinu velurðu **Innkaup**.
2. Veldu **Staðfesta**.
3. Í aðgerðasvæðinu velurðu **Móttaka**.
4. Velja **Innhreyfingarskjal afurða**. Í reitinn **Móttaka afurða** skal slá inn gildi.
- Þetta svæði er notað til að færa inn tilvísun sem verður notað sem fylgiskjal fyrir færslubók innhreyfingarskjala afurða.  
- Í reitnum **Magn** skal velja **Pantað magn**. Þessi valkostur þýðir að kvittunin verður unnið fyrir magnið sem pöntunarlínur voru stofnaðar með.  
- Gangið úr skugga um að reiturinn **Prenta innhreyfingarskjal afurða** sé stilltur á **Nei**. Prentunar er ekki þörf í þessu dæmi.  
5. Stækka hlutann **Línur**.
- Athugið hvernig innhreyfingarskjal afurða er stofnað fyrir tvær afhendingarlínur en ekki upprunalegu pöntunarlínunni. Hafi kvittunin verið skráð í vöruhúsi, myndi það einnig hafa verið skráð á línur afhendingaráætlunar.  
6. Fella saman hlutann **Línur**.
7. Veldu **Í lagi** til að bóka kvittunina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]