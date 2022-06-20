---
title: Endurbætur á sölustað fyrir raðaðar afurðir
description: Þessi grein sýnir endurbætur sem gerðar hafa verið á raðnúmeruðum vörum til að hjálpa þér að spara tíma og vera afkastameiri.
author: ShalabhjainMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 58252279a625bbdaac7192d1e6e538b9b1fd89ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890296"
---
# <a name="point-of-sale-pos-improvements-for-serialized-products"></a>Endurbætur á sölustað fyrir raðaðar afurðir

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Yfirlit

Byggt á stillingum í Commerce Headquarters er hægt að flokka vörur sem annaðhvort raðaðar eða óraðaðar. Þegar vörur eru raðaðar er hægt að úthluta einkvæmu númeri á hverja vöru sem hjálpar til við að rekja ábyrgð, vörur og staðfesta eignarhald. Þó svo að hægt sé að veita raðnúmer fyrir raðaðar vörur í Modern/Cloud Point of Sale (POS) hafa nokkrar endurbætur verið gerðar til að hjálpa gjaldkerum að spara tíma og auka afköst.

## <a name="pos-improvements"></a>POS endurbætur

- **Ekki er krafist raðnúmera fyrr en við kaup** - Áður þurfti gjaldkeri að bæta raðnúmeri við viðskipti fyrir raðaðar vörur. Þetta var vandamál ef gjaldkerar og söluaðilar höfðu tækifæri til að selja viðbótarvörur. Fram að greiðslustigi voru vörur oft uppfærðar í körfu. Í hvert skipti sem gjaldkeri bætti við nýrri vöru spurði kerfið hann því um raðnúmerið. Svargluggi raðnúmera inniheldur hnappinn **Bæta við síðar**. Þess vegna geta söluaðilar bætt hlut við færslu og veitt raðnúmerið síðar. Söluaðilar geta á fljótlegan hátt bætt við og skipt út röðuðum vörum í körfunni og gefið svo upp raðnúmerið rétt fyrir útskráningu. Ef raðnúmer er ekki veitt fyrir hvaða röðuðu vöru sem er fær gjaldkeri sem reynir að ljúka við viðskiptin villuboð. Þessi skilaboð segja að gjaldkeri þurfi að gefa upp raðnúmer sem vantar áður en hann getur haldið áfram.

    Fyrir hverja röðuðu vöru þar sem raðnúmeri var sleppt birtist athugasemd undir færslulínunni. Þessi athugasemd segir að raðnúmer hafi ekki verið gefið upp fyrir vöruna. Því getur gjaldkeri fljótt fundið vörur án raðnúmers.

    **Bæta við raðnúmeri** aðgerðin veitir einnig raðnúmer fyrir vörur þar sem raðnúmer vantar. Eftir að raðnúmerið er veitt er ekki hægt að breyta því. Gjaldkerinn verður að ógilda línuna og bæta við vörunni aftur.
    
- **Raðnúmers er ekki krafist fyrir pantanir viðskiptavinar** - Viðskiptavinir geta pantað í einni verslun og sótt í aðra. Gjaldkeri sem pantar fyrir viðskiptavin þarf ekki að gefa upp raðnúmerið. Raðnúmerið verður veitt við tiltekt eða afhendingu. Hins vegar verður að gefa upp raðnúmer fyrir öll línuatriði þegar afhendingargerðin **Framkvæma** er valin. Annars er ekki hægt að ljúka færslunni.
- **Röðuðum vörum er ekki steypt saman á færsluskjánum** – **Steypa saman afurðum** stillingin í **Afgreiðslustöð** reitarhópnum á **Virkniregla** síðunni gerir þér kleift að steypa saman óröðuðum vörum á færsluskjánum. Þegar sömu vörur eru settar saman er auðveldara að sjá þær á færsluskjá. Þar sem raðnúmer eru yfirleitt einkvæmt, og söluaðilar Þurfa ekki að slá inn raðnúmer fyrir kaup gildir stillingin **Steypa saman afurðum** ekki um raðaðar vörur. Þessi vegna er röðuðum vörum ekki steypt saman á færsluskjánum ef **Steypa saman afurðum** stillingin er valin.
- **Geta til að leita í færslubókum út frá raðnúmeri** – Nú er hægt að leita aukalega í færslubókum út frá raðnúmerum. Til að gera það skaltu opna „Færslubækur“ aðgerðina og ýta á „Ítarleg leit“ hnappinn á forritastikunni. Með því að nota „Bæta við síu“ hnappinn er einnig hægt að nota síu til að leita að raðnúmerum.


[!INCLUDE[footer-include](../includes/footer-banner.md)]