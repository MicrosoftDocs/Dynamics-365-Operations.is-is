---
title: Stofna flutningsverkþætti fyrir lean-framleiðslu
description: Stofna flutningsverkþátt fyrir lean-framleiðslu.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2411dc51dc1b85499edb30d9a580f396277a5bd9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828875"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Stofna flutningsverkþætti fyrir lean-framleiðslu

[!include [banner](../../includes/banner.md)]

Stofna flutningsverkþátt fyrir lean-framleiðslu. 

Skilyrði: 

1. Stofna verður framleiðsluflæði og útgáfu sem er ekki virk.

2. Stofna verður Úr og í vöruhús og staðsetningar. Einnig er hægt að stofna áfyllingu eða áfyllingarvinnuflokk.


## <a name="find-the-production-flow-version"></a>Finndu útgáfu framleiðsluflæðis
1. Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Athugið að framleiðsluflæði verður að hafa útgáfu stöðuna drög.  
3. Í listanum skal smella á tengilinn í valinni línu.

## <a name="create-a-new-activity"></a>Stofnaðu nýja aðgerð
1. Smellt er á Verkþætti.
    * Tryggja skal að valið framleiðsluflæði hafi útgáfu í drögum og velja þá útgáfu.  
2. Smellt er á verkþáttinn Stofna nýja áætlun.
3. Smelltu á Næsta.
4. Í reitinn Heiti skal slá inn gildi.
5. Í reitnum Gerð verkþáttar skal velja ‚Flytja‘.
6. Í reitinn Vinna magn skal slá inn númer.
7. Smelltu á Næsta.

## <a name="select-the-work-cells"></a>Velja vinnuflokkana
1. Í reitnum Áfylling skal smella á fellilistahnappinn til að opna leitina.
    * Til að nota frálagsstaðsetningar vinnuflokksins sem frá staðsetningu í flutningsverkþætti skal velja vinnuflokk. Hægt er að gera sama við áfylltan vinnuflokk, sem setur markstaðsetningu fyrir flutning verkþáttar.  
2. Í listanum skal smella á tengilinn í valinni línu.

## <a name="define-the-inventory-updates"></a>Skilgreina uppfærslur birgða
1. Í reitnum Gerð afurðar skal velja valkost.
    * Athugið að flutningur breytir ekki gerð afurðar. Hægt er að flytja hálfkláraðar vörur eða tilbúnar afurðir (flutning á milli tveggja verkþátta framleiðsluflæðis og mögulega kanban-flæði).     Þegar tilbúnar afurðir eru fluttar er hægt að velja hvort tiltekt eða móttaka skili af sér birgðafærslu.  

## <a name="define-the-transfer-locations"></a>Skilgreina flutningsstaðsetningar
1. Smelltu á Næsta.
2. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Í reitnum Frakt eftir reit skal velja valkost.
    * Meðal valkosta eru: Farmsendanda - fyrirtækið vöruhús til sendingar í gangi, Viðtakanda - fyrirtækið rekstrareiningar í móttöku vöruhúss, Farmflytjanda - lánardrottinn þriðja aðila. Ef fyrirtækið rekstrareiningar er lánardrottinn krefst flutningsverkþátturinn undirverktakasamnings.  
8. Smelltu á Næsta.

## <a name="define-the-activity-times"></a>Skilgreina tíma verkþátta
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Skilgreiningar er krafist á Keyrslutíma. Keyrslutími er notaður til að reikna út kostnað og gegnumstreymi tímum kanban-vinnslurnar. Keyrslutímar eru ekki notaðir til að reikna álag og notkun sem er reiknað með tíma ferlis úr verkinu útgáfu framleiðsluflæðis framleiðslu.  
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]