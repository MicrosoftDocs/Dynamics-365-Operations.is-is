---
title: Stofna og komast yfir eignir viðskiptaskuldir
description: Þetta ferli fer í gegnum stofnun og kaup eignar með innkaupaferlið.
author: moaamer
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4290ced6bcf4432583cffc9122a4bba86266a559
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713614"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Stofna og komast yfir eignir viðskiptaskuldir

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum stofnun og kaup eignar með innkaupaferlið.  Hann notar Bókari og starfsmaður viðskiptaskulda Og USMF sýnigögn fyrirtækisins.


## <a name="set-fixed-assets-parameters"></a>Stilla færibreytur eigna
1. Í **skoðunarrúðnni** ferðu í **Kerfseiningar > Fastafjármunir > Uppsetning > Eignafæribreytur**.
2. Útvíkkaðu flýtiflipann **Innkaupapantanir**.
3. Hakaðu við gátreitinn **Leyfa eignakaup úr Innkaupum**.
4. Merktu við gátreitinn **Stofna eign við bókun innhreyfingarskjals afurða eða reiknings**.

## <a name="create-a-new-vendor-invoice"></a>Nýtt reikningur lánardrottins búið til.
1. Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Viðskiptaskuldir > Vinnusvæði > Reikningsfærsla lánardrottins**.
2. Smelltu á **Nýr reikningur lánardrottins**.
3. Í reitnum **Reikningslykill** skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í reitinn **Númer** skal slá inn gildi.
6. Í reitinn **Bókunardagssetning** skal rita dagsetningu.
7. Smella á **Bæta við línu**.
8. Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina. Hægt er að nota annað hvort vörur ekki á lager eða innkaupaflokkar fyrir eignakaup.  
9. Í listanum skal smella á tengilinn í valinni línu.
10. Í reitnum **Magn** slærðu inn tölu. Einnar reikningslínu stofnar einungis eina eign, óháð magni. Svæðisgildi fyrir magns reiknings verða flutt í magn eignar.  
11. Í reitnum **Einingarverð** skal slá inn tölu.
12. Útvíkkaðu flýtiflipann **Upplýsingar um línur**.
13. Smelltu á flipann **Eignir**.
14. Hakaðu við gátreitinn **Stofna nýja eign**.
15. Í reitnum **Eignaflokkur** skal smella á fellilistahnappinn til að opna leitina.
16. Veljið eignaflokk til að nota á þegar ný eign er stofnuð, á listanum.
17. Í listanum skal smella á tengilinn í valinni línu.
18. Smelltu á **bóka.** Eign verður stofnuð og keypt þegar reikningur er bókaður.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
