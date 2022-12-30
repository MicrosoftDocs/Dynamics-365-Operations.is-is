---
title: Uppfærsla staðalkostnaðar í umhverfi sem tengist ekki framleiðslu
description: Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði í framleiðslulausu umhverfi.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 548955f544842ea5f60fd2d800c8c11cb459ee4c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679080"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Uppfærsla staðalkostnaðar í umhverfi sem tengist ekki framleiðslu

[!include [banner](../includes/banner.md)]

Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði í framleiðslulausu umhverfi.

Eftirfarandi leiðbeiningar gera ráð fyrir að notuð sé tveggja útgáfu nálgunin til að uppfæra staðlaðan kostnað. Í þessari nálgun inniheldur ein kostnaðarútgáfa upphaflega skilgreindan staðlaðan kostnað fyrir fryst tímabil og seinni kostnaðarútgáfan inniheldur stigvaxandi uppfærslur. Hver uppfærsla er færð inn sem kostnaðarfærsla innan seinni kostnaðarútgáfunnar og að lokum gerð virk. Önnur lausn felst í einnar útgáfu nálgun með því að nota upphaflega skilgreindan staðlaðan kostnað. Tveggja útgáfu nálgunin krefst þess að skilgreind sé önnur kostnaðarútgáfa. Hér eru leiðbeiningar fyrir skilgreiningu þessarar kostnaðarútgáfu:

-   Notið kostnaðargerðina **Staðlaður kostnaður**.
-   Gefið kostnaðarútgáfunni lýsandi kenni sem skýrir innihaldið, til dæmis **2016-UPPFÆRSLUR**.
-   Tryggja þarf að kostnaðarfærslur séu teknar með.
-   Leyfið kostnaðarfærslur fyrir öll svæði. Ef svæði er sérstaklega tilgreint er aðeins hægt að færa kostnaðarfærslur fyrir það svæði.
-   Tilgreinið varaúrræði sem **Ekkert**. Varaúrræðisreglan á aðeins við kostnaðarútreikninga vegna framleiddra vara.

Þannig er farið að við að leiðrétta, aðlaga eða uppfæra staðlaðan kostnað nýrra vara:

1.  Notið skjámyndina **Kostnaðarútgáfa** **Uppsetning** til að leyfa skráningu á kostnaðarfærslum inn í seinni kostnaðarútgáfuna. Koma má í veg fyrir virkjun á kostnaði í bið, svo að virkjun verði leyfð eftir að kostnaður í bið hefur verið algerlega og nákvæmlega skilgreindur. Einnig er hægt að færa inn dagsetningu í svæðinu **Frá dagsetningu**. Gott er að nota dagsetninguna þegar á að virkja stigvaxandi uppfærslur. Sem annar valkostur, skiljið svæðið **Frá dagsetningu** eftir autt fyrir kostnaðarútgáfuna, og færið svo inn dagsetningu í svæðið **Frá dagsetningu** fyrir hverja kostnaðarfærslu.
2.  Nota skal síðuna **Vöruverð** til að færa inn uppfærslur sem kostnaðarfærslur vöru sem eru innan seinni kostnaðarútgáfunnar.
3.  Notið skýrsluna **Vöruverð** til að sannprófa heilleika og réttmæti vörukostnaðarfærslanna innan seinni kostnaðarútgáfunnar.
4.  Notið síðuna **Viðhald kostnaðarútgáfu** til að breyta lokunarflaggi til að heimila virkjun á biðkostnaðarfærslum í seinni kostnaðarútgáfunni.
5.  Notið síðuna **Virkja verð** (sem er opnuð úr síðunni **Viðhald Kostnaðarútgáfu**) til að virkja allar biðkostnaðarfærslur í seinni kostnaðarútgáfunni. Einnig er hægt að gera kostnaðarfærslur í bið fyrir stakar vörur virkar með því að smella á hnappinn **Virkja biðverð** á síðunni **Vöruverð**.
6.  Notið skjámyndina **Uppsetning kostnaðarútgáfu** til þess að breyta lokunarflöggum í síðari kostnaðarútgáfunni og koma í veg fyrir frekara gagnaviðhald. Lokunarreglurnar hindra færslu nýs kostnaðar í bið og virkjun kostnaðar í bið.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]