---
title: Stofna og komast yfir eignir viðskiptaskuldir
description: Þessi leiðarvísi fyrir verk um stofnun og kaup eignar með innkaupaferlið.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6c36338cc67855c79ec97d88bb8b633417b85c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "316419"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Stofna og komast yfir eignir viðskiptaskuldir

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk um stofnun og kaup eignar með innkaupaferlið.  Það notar Bókari og starfsmaður viðskiptaskulda Og USMF sýnigögn fyrirtækisins.


## <a name="set-fixed-assets-parameters"></a>Stilla færibreytur eigna
1. Fara í Eignir > Uppsetning > Færibreytur eigna.
2. Útvíkka eða draga saman hlutanum innkaupapöntun.
3. Merkja við Innkaupagátreit Leyfa eignakaup úr .
4. Merktu við gátreið Stofna eign á meðan innhreyfingarskjal afurða eða bókun reiknings.

## <a name="create-a-new-vendor-invoice"></a>Nýtt reikningur lánardrottins búið til.
1. Fara í Viðskiptaskuldir > Vinnusvæði > Færsla fyrir reikning lánardrottins.
2. Smellt er á Nýtt reikning lánardrottins.
3. Í reitnum reikningslykill skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í reitnum Númer skal slá inn gildi.
6. Dagsetning er rituð í reitinn Bókunardagssetning.
7. Smellið á „Bæta við línu“.
8. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
    * Hægt er að nota annað hvort vörur ekki á lager eða innkaupaflokkar fyrir eignakaup.  
9. Í listanum skal smella á tengilinn í valinni línu.
10. Færið inn númer í reitnum „Magn“.
    * Einnar reikningslínu stofnar einungis eina eign, óháð magni.  Svæðisgildi fyrir magns reiknings verða flutt í magn eignar.  
11. Færið inn númer í reitnum „Einingarverð“.
12. Útvíkka eða draga saman hluta upplýsingar Línu.
13. Smellið á flipann eigna.
14. Merktu við gátreit Stofna nýja eign.
15. Í reitnum eignaflokkur skal smella á fellilistahnappinn til að opna leitina.
16. Veljið eignaflokk til að nota á þegar ný eign er stofnuð, á listanum.
17. Í listanum skal smella á tengilinn í valinni línu.
18. Smellið á „Bóka“.
    * Eign verður stofnuð og keypt þegar reikningur er bókaður.  

