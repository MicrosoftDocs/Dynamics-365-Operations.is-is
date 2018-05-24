---
title: "Þjónustustigssamningar"
description: "Í þjónustustigssamningi samþykkir viðskiptavinurinn lágmarks svartíma sem byggir á því hvenær þjónustufyrirtækið skráir málið og hvenær málið er leyst."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a>Þjónustustigssamningar        

[!include [banner](../includes/banner.md)]


Þjónustustigssamningur (SLA) er samningur á milli þjónustufyrirtækis og þjónustuviðskiptavinar. Í SLA samþykkir viðskiptavinurinn lágmarks svartíma sem byggir á því hvenær þjónustufyrirtækið skráir málið og hvenær málið er leyst.

SLA framfylgir stöðluðu þjónustustigi sem er boðið viðskiptavinum og gerir það einnig gagnsætt fyrir þjónustufyrirtæki þegar þjónustuverkefni skal lokið.

Hægt er að jafn marga þjónustustigssamninga og þörf er á til þess að bjóða þjónustuviðskiptavinum mismunandi þjónustustig.

## <a name="create-a-service-level-agreement"></a>Stofna þjónustustigssamning

1.  Smellið á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustusamningar** \> **Þjónustustigssamningar**.

2.  Sláðu inn nafn fyrir þjónustustigssamninginn í reitinn **Þjónustustigssamningur**.

3.  Sláðu inn þann tíma sem þú vilt leyfa til að ljúka þjónustusímtölum sem fylgja með þjónustusamningnum. Veldu síðan dagatal ef þú vilt byggja þjónustusamninginn á tilteknu dagatali.

## <a name="apply-a-service-level-agreement"></a>Nota þjónustustigssamning

Þjónustustigssamningurinn er notaður í þjónustusamningi.

Þjónustupantanir sem þú stofnar handvirkt og tengir við þjónustusamning sem hefur SLA eru mældar gagnvart SLA.

Þjónustupantanir sem eru stofnaðar sjálfkrafa eru ekki tengdar við þjónustustigssamning.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Nota þjónustustigssamning í þjónustusamningi

1.  Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**. Veldu þjónustusamning sem þú vilt nota SLA í og smelltu síðan á **Breyta** á **Aðgerðasvæðinu**.

2.  Í reitnum **Þjónustustigssamningur** skal velja SLA sem á að úthluta.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Nota þjónustustigssamning í þjónustusamningsflokki

1.  Smellið á **Þjónustustjórnun** \> **Uppsetningu** \> **Þjónustusamningar** \> **Þjónustusamningsflokkar**.

2.  Í reitnum **Þjónustustigssamningur** skal velja SLA sem á að úthluta.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Rekja tíma á þjónustupöntun gegn SLA

Þegar þú stofnar nýja þjónustupöntun fyrir þjónustusamning sem SLA er úthlutað til, hefst tímabilið fyrir afhendingu þjónustunnar og kerfið byrjar að fylgjast með afhendingartímanum. Að auki getur þú stillt eftirfarandi valkosti:

  - Hægt er að ræsa og stöðva tímaskráningu í þjónustupöntun til þess að skrá heildartímann sem varið er í þjónustupantanir.

  - Þú getur fylgst með samræmi við tímabilið sem er stillt í þjónustustigssamningnum.

  - Þú getur skilgreint ástæðukóða sem þarf að stilla ef farið er fram úr tímabili þjónustustigssamnings.

## <a name="see-also"></a>Sjá einnig

[Skoða uppfyllingu á þjónustustigssamningum](view-compliance-with-service-level-agreements.md)

  



