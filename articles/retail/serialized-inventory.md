---
title: "POS endurbætur fyrir raðaðar vörur"
description: "Þetta efnisatriði sýnir endurbætur sem hafa verið gerðar á röðuðum vörum til að hjálpa þér að spara tíma og auka afköst."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 74a27761c065e475fa7c10c5812f0307df9f570e
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---

# <a name="pos-improvements-for-serialized-products"></a>POS endurbætur fyrir raðaðar vörur

[!INCLUDE [banner](includes/banner.md)]

## <a name="overview"></a>Yfirlit 
Byggt á stillingum í Retail Headquarters er hægt að flokka vörur sem annaðhvort raðaðar eða óraðaðar. Þegar vörur eru raðaðar er hægt að úthluta einkvæmu númeri  á hverja vöru sem hjálpar til við að rekja ábyrgð, vörur og staðfesta eignarhald. Þó svo að hægt sé að veita raðnúmer fyrir raðaðar vörur í Modern/Cloud Point of Sale (POS) hafa nokkrar endurbætur verið gerðar til að hjálpa gjaldkerum að spara tíma og auka afköst.  

## <a name="pos-improvements"></a>POS endurbætur

- **Ekki er krafist raðnúmera fyrr en við kaup** - Áður þurfti gjaldkeri að bæta raðnúmeri við viðskipti fyrir raðaðar vörur. Þetta var vandamál ef gjaldkerar og söluaðilar höfðu tækifæri til að selja viðbótarvörur. Fram að greiðslustigi voru vörur oft uppfærðar í körfu. Í hvert skipti sem gjaldkeri bætti við nýrri vöru spurði kerfið hann eða hana því um raðnúmerið. Svargluggi raðnúmera inniheldur hnappinn **Bæta við síðar**. Þess vegna geta söluaðilar bætt hlut við færslu og veitt raðnúmerið síðar. Söluaðilar geta á fljótlegan hátt bætt við og skipt út röðuðum vörum í körfunni og gefið svo upp raðnúmerið rétt fyrir útskráningu. Ef raðnúmer er ekki veitt fyrir hvaða röðuðu vöru sem er fær gjaldkeri sem reynir að ljúka við viðskiptin villuboð. Þessi skilaboð segja að gjaldkeri þurfi að gefa upp raðnúmer sem vantar áður en hann eða hún getur haldið áfram.

    Fyrir hverja röðuðu vöru þar sem raðnúmeri var sleppt birtist athugasemd undir færslulínunni. Þessi athugasemd segir að raðnúmer hafi ekki verið gefið upp fyrir vöruna. Því getur gjaldkeri fljótt fundið vörur án raðnúmers.

    **Bæta við raðnúmeri** aðgerðin veitir einnig raðnúmer fyrir vörur þar sem raðnúmer vantar. Eftir að raðnúmerið er veitt er ekki hægt að breyta því. Gjaldkerinn verður að ógilda línuna og bæta við vörunni aftur. 
    
- **Raðnúmers er ekki krafist fyrir pantanir viðskiptavinar** - Viðskiptavinir geta pantað í einni verslun og sótt í aðra. Gjaldkeri sem pantar fyrir viðskiptavin þarf ekki að gefa upp raðnúmerið. Raðnúmerið verður veitt við tiltekt eða afhendingu. Hins vegar verður að gefa upp raðnúmer fyrir öll línuatriði þegar afhendingargerðin **Framkvæma** er valin. Annars er ekki hægt að ljúka færslunni.    
- **Röðuðum vörum er ekki steypt saman á færsluskjánum** – **Steypa saman afurðum** stillingin í **Afgreiðslustöð** reitarhópnum á **Virkniregla** síðunni gerir þér kleift að steypa saman óröðuðum vörum á færsluskjánum. Þegar sömu vörur eru settar saman er auðveldara að sjá þær á færsluskjá. Þar sem raðnúmer eru yfirleitt einkvæmt, og söluaðilar Þurfa ekki að slá inn raðnúmer fyrir kaup gildir stillingin **Steypa saman afurðum** ekki um raðaðar vörur. Þessi vegna er röðuðum vörum ekki steypt saman á færsluskjánum ef **Steypa saman afurðum** stillingin er valin.
- **Geta til að leita í færslubókum út frá raðnúmeri** - Nú er hægt að leita aukalega í færslubókum út frá raðnúmerum. Til að gera það skaltu opna „Færslubækur“ aðgerðina og ýta á „Ítarleg leit“ hnappinn á forritastikunni. Með því að nota „Bæta við síu“ hnappinn er einnig hægt að nota síu til að leita að raðnúmerum.

