---
title: Sjálfvirk uppfærsla á eignateljurum
description: Þetta efni lýsir sjálfvirkri uppfærslu á eignateljurum í eignastýringu.
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
ms.openlocfilehash: fcc46fad8d57b7d4d57edfa4f2ae06de923d1c14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430155"
---
# <a name="automatic-update-of-asset-counters"></a>Sjálfvirk uppfærsla á eignateljurum

[!include [banner](../../includes/banner.md)]

Nánari upplýsingar um handvirka skráningu á eignateljurum er að finna í [Handvirk uppfærsla á eignateljurum](../work-orders/manual-update-of-asset-counters.md). Sjá upplýsingar um hvernig á að setja upp eignateljara í [Teljarar](../setup-for-objects/counters.md).

Einnig er hægt að uppfæra teljaragildi sjálfkrafa úr framleiðsluskráningum, byggt á framleiðslutíma eða framleiðslumagni (það er að segja, því magni sem er framleitt). Þessi uppfærsla er gerð á síðunni **Uppfæra eignateljara**. Þú getur uppfært eina eða fleiri eignir með því að stilla eina færibreytu, **Frá dagsetningu**. Þessi færibreyta tilgreinir upphafsdagsetningu framleiðsluskráninga (framleiðslutíma eða framleiðslumagn). Með öðrum orðum tilgreinir hún dagsetninguna sem uppfæra skal teljaragildi frá.

Allar eignir sem tengjast tilföngum *og* hafa eignateljara, sem eru settar upp til uppfærslu miðað við framleiðslutíma eða framleiðslumagn, verða með í sjálfvirkri uppfærslu og ný teljaragildi verða til. Ný teljagildi verða til.

Fyrir teljara sem byggjast á framleiðslumagni samanstendur talan bæði af gallalausu magni og villumagni sem er skráð. Ef einingin sem er notuð fyrir skráningu á framleiðslumagni er frábrugðin einingunni sem notuð er í teljaranum er magninu breytt til að samsvara teljaraeiningunni.

Eins og getið er hér að ofan er hægt að uppfæra sjálfvirka teljara úr framleiðsluskráningum. Þess vegna verður eignin sem þú vilt uppfæra teljara sjálfkrafa fyrir að tengjast tilföngum (vél). Þegar framleitt magn eða framleiðslutími hefur verið skráður á tilföngin geturðu uppfært tengda eignateljara.

1. Veldu **Eignastýring** > **Reglubundið** > **Eignir** > **Uppfæra eignateljara**.

2. Í reitnum **Frá dagsetningu** velurðu upphafsdagsetningu sjálfvirku uppfærslunnar.

    >[!NOTE]
    >Dagsetningin í þessum reit er dagsetningin „verk í vinnslu“ frá og með **Leiðarfærslur** (reiturinn **Framleiðslustýring** > **Fyrirspurnir og skýrslur** > **Framleiðsla** > **Leiðarfærslur** > **Efnisleg dagsetning**).

3. Á flýtiflipanum **Færslur til að taka með** er hægt að velja tilteknar eignir, eignategundir eða tilföng fyrir sjálfvirka uppfærslu. Veldu **Sía** og gerðu viðeigandi val.

4. Á flýtiflipanum **Keyra í bakgrunni** geturðu sett upp sjálfvirka uppfærslu sem runuvinnslu, eftir þörfum.

    Myndin hér að neðan sýnir dæmi um gluggann **Uppfæra eignateljara**.

    ![Mynd 1](media/12-work-orders.png)

5. Veljið **Í lagi**. 

Eftir að sjálfvirkri uppfærslu á eignateljurum er lokið geturðu skoðað gagnaskráningar sem tengjast eigninni á síðunni **Eignateljarar**. Veldu **Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir**, veldu eignina og síðan á aðgerðarrúðunni, á flipanum **Eignir**, í hópnum **Fyrirbyggjandi**, velurðu **Teljarar**.

Á síðunni **Samanlagt verðmæti eigna** er hægt að fá yfirlit yfir nýjustu skráningu sem hafa verið gerðar á öllum teljaragerðum á öllum eignum. Veldu **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Uppsafnað gildi eigna**. Þessi síða líkist síðunni **Eignateljar** en þú getur ekki bætt við eða breytt skráningum. Hún er aðeins til yfirlits.

Myndin hér að neðan sýnir dæmi um síðuna **Samanlagt verðmæti eigna**.

![Mynd 2](media/13-work-orders.png)

Athugið eftirfarandi stig:

- Hægt er að búa til handvirkar teljaragildisskráningar fyrir teljaragerðir sem eru uppfærðar sjálfkrafa. Nánari upplýsingar er að finna í [Handvirkri uppfærslu á eignateljurum](../work-orders/manual-update-of-asset-counters.md).

- Þú getur sett upp teljara sem tengjast öðrum teljara. Í þessu tilfelli, þegar teljarinn er uppfærður, eru tengdir teljarar sjálfkrafa uppfærðir um leið. Nánari upplýsingar um hvernig setja skal upp tengda eignateljara er að finna í [Teljarar](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]