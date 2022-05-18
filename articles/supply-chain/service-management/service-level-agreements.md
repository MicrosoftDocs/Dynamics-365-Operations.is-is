---
title: Yfirlit þjónustustigssamninga
description: Í þjónustustigssamningi samþykkir viðskiptavinurinn lágmarks svartíma sem byggir á því hvenær þjónustufyrirtækið skráir málið og hvenær málið er leyst.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1db12600aa47f537da6918c82ef3164c2123a8ac
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670805"
---
# <a name="service-level-agreements-overview"></a>Yfirlit þjónustustigssamninga       

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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]