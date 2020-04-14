---
title: Stofna vinnsluverkþætti fyrir lean-framleiðslu
description: Stofna ferlisverkþátt fyrir lean-framleiðslu.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 767d63327da0c9d4666bd3ef869417e809c81779
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149214"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>Stofna vinnsluverkþætti fyrir lean-framleiðslu

[!include [banner](../../includes/banner.md)]

Stofna ferlisverkþátt fyrir lean-framleiðslu. 

Skilyrði: 

1. Stofna verður framleiðsluflæði og útgáfu sem er ekki virk.

2. Stofna verður vinnuflokk.


## <a name="find-the-production-flow-version"></a>Finndu útgáfu framleiðsluflæðis
1. Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.

## <a name="create-a-new-activity"></a>Stofnaðu nýja aðgerð
1. Smellt er á Verkþætti.
    * Tryggja skal að valið framleiðsluflæði hafi útgáfu í drögum og velja þá útgáfu.  
2. Smellt er á verkþáttinn Stofna nýja áætlun.
3. Smelltu á Næsta.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitinn Heiti skal slá inn gildi.
    * Athugið að heitið verður að vera einkvæmt fyrir gefið framleiðsluflæði fyrir allar útgáfur.  
6. Í reitinn Vinna magn skal slá inn númer.
    * Athugið að óháð því hvaða magn vinnslu verður keyrt er þetta lágmarksmagn á hverja vinnslu til að reikna út kostnað við vinnu. Ef vinnsla á magn víkja frá þessu magni, verða kostnaðarfrávik vinnu stofnuð.  
7. Smelltu á Næsta.

## <a name="select-the-work-cell"></a>Veldu vinnuflokk
1. Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.
2. Í listanum skal smella á tengilinn í valinni línu.

## <a name="define-the-inventory-updates"></a>Skilgreina uppfærslur birgða
1. Velja eða hreinsa gátreitinn Uppfærsla á innhreyfingu á lager.
    * Ef Uppfæra á lager = Nei, er hægt að skilgreina verkþátt til að taka við hálfkláraðri afurð (verkþátturinn nær ekki næsta stigi í Uppskrift).    Einnig er hægt að velja að nota hálfkláraðar afurðir.  

## <a name="define-the-picking-activities"></a>Skilgreina tiltektarverkþættina
1. Smelltu á Næsta.
2. Í listanum skal merkja valda línu.
    * Sjálfgefinn tiltektarverkþáttur er stofnaður fyrir ílagsstaðsetningu valins vinnuflokks.  
3. Smelltu á Bæta við.
    * Hægt er að stofna viðbótar tiltektarverkþætti fyrir tilteknar vörur sem eru ekki sett í ílagsverkþætti vinnuflokks.  
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í reitnum Vörunúmer skal slá inn gildi.
6. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
    * Með þessari skilgreiningu er allt notað efni í verkþættinum tekið úr sjálfgefnu ílagsvöruhúsi og staðsetningu nema vara sem skilgreind er í annarri tiltektaraðgerð. Þessi vara verður tekið úr öðru vöruhúsi og staðsetningu.  
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Veldu eða hreinsaðu gátreitinn Skrá úrkast.
10. Smelltu á Næsta.

## <a name="define-the-activity-times"></a>Skilgreina tíma verkþátta
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Skilgreiningar er krafist á Keyrslutíma. Keyrslutími er notaður til að reikna út kostnað og gegnumstreymistíma kanban-vinnslurnar. Keyrslur eru ekki notaðar til að reikna álag og notkun, það er reiknað út með tíma ferlis úr verkinu útgáfu framleiðsluflæðis framleiðslu.  
2. Í reitinn Tími skal slá inn númer.
3. Í reitnum Eining skal slá inn gildi.
4. Velja tímaeiningu.
5. Í reitinn Á magn skal slá inn númer.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Biðtímar eru valfrjálsir.  
7. Í reitinn Tími skal slá inn númer.
8. Í reitnum Eining skal slá inn gildi.
9. Velja tímaeiningu.
10. Í reitinn Á magn skal slá inn númer.
11. Smelltu á Næsta.
12. Smellt er á Ljúka.
13. Lokið síðunni.

