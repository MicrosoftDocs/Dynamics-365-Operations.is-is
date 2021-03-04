---
title: Yfirlit tekjuskráningar
description: Í þessu efnisatriði er að finna upplýsingar um tekjuskráningareiginleikann. Þessi eiginleiki veitir sveigjanlega umgjörð sem gerir það kleift að skilgreina sérstakar reglur fyrir fyrirtækið um greiningu bæði verðlags og tekjuáætlunar fyrir pantanir með mörgum vörutegundum.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a7e37a0800ec7909f79e5a2354f59c7450995641
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995615"
---
# <a name="revenue-recognition-overview"></a>Yfirlit tekjuskráningar

[!include [banner](../includes/banner.md)]

Fyrirtæki í atvinnugrein þar sem margar vörutegundir eru seldar, svo sem vörur, þjónusta, áskriftir og svo framvegis, verða að geta sundurgreint pantanir með mörgum vörutegundum svo hægt sé að greina tekjur á grundvelli sérstakra viðmiðunarregla fyrir fyrirtækið og atvinnugreinina.

> [!NOTE]
> Ekki er hægt að kveikja á tekjuskráningareiginleikanum í gegnum eiginleikastjórnun. Nota verður skilgreiningarlykil til að kveikja á honum.

> Tekjuskráning, þ.á m. búntaðgerð, er ekki studd fyrir notkun í Commerce-rásum (rafrænum viðskiptum, sölustað, símaveri). Ekki skal bæta vörum, sem skilgreindar eru með tekjuskráningu, við pantanir eða færslur sem stofnaðar eru í Commerce-rásum.

Almennt séð má nota tekjuskráningarferlið til að framkvæma þessi verk:

* Úthluta tekjum til að tryggja að viðeigandi verðlag greinist á grundvelli virðist hluta í pöntunum með mörgum vörutegundum.
* Fresta tekjum í samræmi við tekjuáætlun sem endurspeglar samningsbundinn tímaramma og hlutfall fyrir greiningu á tekjum yfir tímann.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Myndbandið [Hvernig á að nota tekjuskráningu í Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (sýnt hér að ofan) er innifalið í [Finance and Operations spilunarlistanum](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) á YouTube.

Tekjuskráningareiginleikinn veitir sveigjanlega umgjörð sem gerir það kleift að skilgreina sérstakar reglur fyrir fyrirtækið um greiningu bæði verðlags og tekjuáætlunar.

Útgefnar afurðir eru notaðar til að styðja við tekjuskráningu í fylgiskjölum sölupantana. Útgefnar afurðir innihalda uppsetninguna sem krafist er til að ákvarða verðlag og tekjuáætlun. Sölupöntunin getur átt uppruna sinn í tíma- og efnisverki.

Fyrirtæki geta notað tekjuáætlunareiginleikann án þess að nota verðlagseiginleikann. Því verður verðið í sölupöntunarlínum notað sem ýmist tekjur eða frestaðar tekjur. Ef tekjuáætlun er til fyrir sölupöntunarlínu verður verðinu í sölupöntunarlínunni frestað. Ef tekjuáætlun er ekki til fyrir sölupöntunarlínu verður verðið í sölupöntunarlínunni bókað á tekjulykil við reikningsfærslu.

Verðið er reiknað annaðhvort þegar sölupöntun er staðfest eða þegar reikningurinn er bókaður. Til að forskoða verðið áður en reikningur er bókaður verður þú að staðfesta sölupöntunina.

Þegar sölupöntunin er staðfest er áætlun um væntanlegar tekjur einnig stofnuð ef einhver sölupöntunarlína hefur tekjuáætlun. Þegar sölupöntun er reikningsfærð er áætlun um væntanlegar tekjur eytt og áætlun um væntanlegar tekjur er skipt út fyrir raunverulega tekjuskráningaráætlun.

Unnið er með upplýsingar úr tekjuskráningaráætlun fyrir hverja sölupöntunarlínu. Þar af leiðandi getur stjórnandi tekjuskráningar skoðað upplýsingarnar og losað línur í tekjur þegar samningsbundnum skyldum lýkur. Við lok hvers tímabils getur stjórnandi tekjuskráningar búið til færslubók fyrir tekjur til að losa allar áætlunarlínur sem eru á skilum á eða fyrir dagsetningu sem viðkomandi ákveður. Þessi færslubók tekna er ekki bókuð strax. Þar af leiðandi getur stjórnandi tekjuskráningar staðfest að rétt upphæð hafi verið losuð úr frestuðum tekjum í rauntekjur.

Ef samningsbreytingar valda því að nýrri sölupöntunarlínu sé bætt við annaðhvort fyrirliggjandi sölupöntun eða nýja sölupöntun er hægt að keyra endurúthlutunarferli til að leiðrétta verðið á öllum línum sölupantana.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]