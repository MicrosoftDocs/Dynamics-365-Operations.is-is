---
title: Handvirk uppfærsla á eignateljurum
description: Þetta efni lýsir handvirkri uppfærslu á eignateljurum í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9d9cd755f5dec125676a8dbefe63a64e226366ed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204517"
---
# <a name="manual-update-of-asset-counters"></a>Handvirk uppfærsla á eignateljurum

[!include [banner](../../includes/banner.md)]



Teljarar eru notaðir til að búa til skráningar á eign, svo sem skráningar um fjölda klukkustunda sem eignin hefur verið starfrækt eða magnið sem hefur verið framleitt.

Teljarategundin sem er valin fyrir teljara gæti verið stillt á að erfa teljaragildi. Með öðrum orðum er valkosturinn **Erfð teljaragildi eigna** stilltur á **Já** á flýtiflipanum **Almennt** á síðunni **Teljarar** (**Eignastýring** > **Uppsetning** > **Eignagerðir** > **Teljarar**). Í þessu tilfelli, þegar þú býrð til nýja teljaralínu af þeirri gerð, er hver undireign sem notar sömu teljarategund uppfærð sjálfkrafa.

Á síðunni **Allar eignir** stofnarðu teljaraskráningarnar klukkustundir eða magn á eign, byggt á lestri þínum af eigninni.

1. Veldu **Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir**.

2. Veldu eignina og síðan, í aðgerðaglugganum, á flipanum **Eign**, í hópnum **Fyrirbyggjandi**, velurðu **Teljarar**. Síðan **Eignateljarar** sýnir lista yfir allar fyrri gagnaskráningar sem hafa verið gerðar á valinni eign.

3. Veldu **Nýr** til að stofna skráningu. Eignakennið er fært sjálfkrafa inn í reitinn **Eign**.

4. Í reitinn **Teljari** skaltu velja viðeigandi teljara. Aðeins teljarar sem tengjast eignategundinni sem valin er á eigninni eru tiltækir til vals. Tengda einingin er sjálfvirkt sett inn í reitinn **Eining**.

5. Í reitnum **Skráð** velurðu dagsetningu og tíma fyrir gagnaskráningu.

6. Í reitinn **Gildi** slærðu inn númerið frá síðustu gagnaskráningu. Að öðrum kosti, í reitinn **Uppsafnað gildi** slærðu inn heildarfjölda tölu.

Athugið eftirfarandi stig:

- Ef þú setur upp nýjan teljara á eign verður að skrá breytingu á eigninni á síðunni **Eignateljarar**. Næst verðurðu að búa til tvær skráningarlínur sem eru með eins tímastimpla. Fyrsta línan verður að vera fyrir teljarann sem þú ert að skipta um. Á línunni sem tengist nýja teljaranum velurðu gátreitinn **Endurstilling teljara**. Í reitnum **Samtals** er heildartala talningar summan af samanlagðri talningu allra skráðra gilda á þeirri teljaragerð.

- Ef gátreiturinn **Endurstilling teljara** er valinn á eign með viðhaldsáætlun sem hefur bilgerðina „Einu sinni frá...“ eða „Einu sinni náð...“ er teljarinn enn virkur á nýju teljaralínunni því þú býrð til aðskilda teljaralínu og byrjar upp á nýtt með nýjum teljara.

Myndin hér að neðan sýnir dæmi um síðuna **Eignateljarar**.

![Mynd 1](media/11-work-orders.png)

Á síðunni **Eignateljarar** (**Eignastýring** > **Fyrirspurnir** > **Eignir** > **Eignateljarar**) er hægt að gera gagnaskráningar á nokkrum eignum í einu, eftir þörfum.

>[!NOTE]
>Þú getur sett upp svið til að skilgreina frávik í handvirkum gagnaskráningum. Þú getur einnig tilgreint hvaða skilaboð birtast ef skráningar eru utan skilgreinds sviðs. Nánari upplýsingar um hvernig setja skal upp teljara er að finna í [Teljarar](../setup-for-objects/counters.md).

