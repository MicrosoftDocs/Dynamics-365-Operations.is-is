---
title: Fjöldi bóka í hverri færslubók
description: Í þessu efnisatriði er lýst venslum á milli færslubóka og eignabóka þegar eignakaup eða afskriftartillaga er stofnuð í gegnum runuvinnslu. Hægt er að skilgreina hámarksfjölda bóka sem eru innifaldar fyrir hver kaup og fyrir afskriftir.
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cfb9a9e1456a7d9067e3c4369a7eb7150326655d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988953"
---
# <a name="number-of-books-per-journal"></a>Fjöldi bóka í hverri færslubók

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst venslum á milli færslubóka og eignabóka þegar eignakaup eða afskriftartillaga er stofnuð í gegnum runuvinnslu. Hægt er að skilgreina hámarksfjölda bóka sem eru teknar með fyrir hver kaup og fyrir afskriftir með því að nota svæðin í hlutanum **Fjölda bóka á færslubók** á flipanum **Almennt** á síðunni **Eignafæribreytur** (**Eignir \> Uppsetning \> Eignafæribreytur**). Þessi svæði gera þér kleift að dreifa fjölda eignabóka á hverja kaupabók og afskriftarbók.

Fyrir kauptillögu er sjálfgefið gildi að minnsta kosti 10.000 bækur. Fyrir afskriftartillögu er sjálfgefið gildi að minnsta kosti 2.000 bækur.

Til dæmis ef það eru 4000 eignir og tvær bækur eru tengdar við hverja eign verður ein bók bókuð í núgildandi lag og hin bókin verður bókuð á skattalagið. Ef 4.000 eignir eru keyptar í gegnum runuvinnslu, mun runuvinnslan sem stofnar eina eignakaupbók innihalda 4.000 eignabækur.

> [!NOTE]
> Færslubókin sem er stofnuð verður áfram notuð þar til runuvinnslunni er lokið.
>
> Afleiddar bækur eru ekki teknar með í hámarksfjölda bóka fyrir hverja færslubók.

Hægt er að nota runuvinnslu til að keyra afskriftir fyrir sama safn af keyptum eignum. Til dæmis er stofnar runuvinnsla tvær afskriftarbækur, sem hvor samanstendur af 2000 eignabókum. Fyrsta færslubókin mun innihalda bækur sem eru tengdar við eignir sem eru númeraðar 1 til 2.000. Önnur færslubókin mun svo innihalda bækur sem eru tengdar við eignir sem eru númeraðar 2.001 til 4.000.

Runuvinnslu útilokar lokaðar bækur. Í runuvinnslu fyrir afskrift er t.d. 10 af fyrstu 2.000 bókunum lokað. Í þessu tilfelli mun fyrsta færslubókin innihalda bækur sem eru tengdar við eignir sem eru númeraðar 1 til 2011. Önnur færslubókin mun svo innihalda bækur sem eru tengdar við eignir sem eru númeraðar 2.012 til 4.000.

Mörkin á fjölda bóka eru notuð ef tvítekin eignaauðkenni eru ekki til í sömu færslubók. Hins vegar ef eignaauðkennið er það sama og auðkenni bókarinnar, er hægt að fara umfram fjölda bóka fyrir hverja færslubók til að halda eignaauðkenninu í sömu færslubók.

Til dæmis eru til 5001 eignaauðkenni, þrjár bækur eru tengdar við hvert auðkenni og hver eignabók er bókuð á sama bókunarlagið. Afskriftir eru keyrðar fyrir þrjá samfellda mánuði, án samantektar.  Afskriftarbókin verður stofnuð í gegnum runuvinnslu og kerfið býr til sjö færslubækur með 667 eignaauðkennum og þremur bókum fyrir hvert auðkenni. Útkoman verður 2.001 bækur. Eftir þrjá mánuði verða því 6003 færslubókarlínur til að viðhalda sömu auðkennum eignar í sömu færslubók. Kerfið stofnar einnig eina færslubók með 332 eignaauðkennum og þremur bókum fyrir hvert auðkenni. Eftir þrjá mánuði verða línurnar 2.988.

> [!Note] 
> Ef færibreytan **Sundurliða afskriftir** er virk þegar verið er að stofna afskriftartillögu, þá hefur gildið í **Fjöldi bóka í hverri færslubók - AfskriftartillAGA** engin áhrif. Í þessu máli ER fjöldi bóka í færslubók 6000, sem eru innri skilgreindu mörkin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]