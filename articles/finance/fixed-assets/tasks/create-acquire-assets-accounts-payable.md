---
title: Stofna og komast yfir eignir viðskiptaskuldir
description: Þessi leiðarvísir fer í gegnum stofnun og kaup eignar með innkaupaferlið.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025639e6e5bdc6b95e9c496f11f29ed8ec8d388c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178259"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Stofna og komast yfir eignir viðskiptaskuldir

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísir fer í gegnum stofnun og kaup eignar með innkaupaferlið.  Hann notar Bókari og starfsmaður viðskiptaskulda Og USMF sýnigögn fyrirtækisins.


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

