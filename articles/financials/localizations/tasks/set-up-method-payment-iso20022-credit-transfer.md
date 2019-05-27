---
title: Setja upp greiðslumáta fyrir ISO20022-kreditfærslu
description: Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt lánardrottins fyrir ISO20022 millifærsla fjármuna eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð til að mynda skrá.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c9209006074fb9da2c3c2ffaa2af4adecfcc1aa9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549024"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Setja upp greiðslumáta fyrir ISO20022-kreditfærslu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að setja upp greiðsluhátt lánardrottins fyrir ISO20022 millifærsla fjármuna eða hvers kyns aðra greiðslugerð sem notar rafræn skýrslugerð til að mynda skrá. 

Áður en lokið er við þetta verkefni verður að flytja út skilgreiningu útflutningssniðs og setja upp greiðslulykla.

Þetta verkefni var stofnuð með DEMF sýnigögn fyrirtækisins.

Þetta þriðja ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.

1. Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.
2. Nota flýtiafmörkun til að finna færslur Til dæmis síu á í Greiðsluaðferðarsvæðinu með gildið 'SEPA CT'.
3. Smella á Breyta.
4. Í svæðinu tímabil skal velja ‚samtala'.
5. Veljið 'Rafræna greiðslu' í svæðinu Greiðslu.
6. Útvíkka hlutann Skráarsnið.
7. Velja skal Já í Almennan rafræna skýrslugerð svæði.
8. Færa inn eða velja gildi í reitnum skilgreiningu útflutningssniðs.
    * Á listanum, veljið gildi ISO20022 kreditfærsla (DE). Ef listi er auður er skilgreining greiðsluútflutnings lánardrottins ekki innfluttu og virkt.  
9. Veljið 'Banki' í svæðinu gerð lykils.
10. Tilgreindu gildi 'DEMF OPER' í svæði greiðslulykils.
11. Smellið á „Vista“.

