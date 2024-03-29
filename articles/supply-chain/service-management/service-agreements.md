---
title: Yfirlit yfir þróaða og innleidda þjónustusamninga
description: Með þjónustusamningum er hægt að skilgreina tilföngin sem eru notuð í dæmigerðri þjónustuheimsókn og hvernig þessi tilföng eru reikningsfærð á viðskiptavininn.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf28619e66fa5d3e86bdbb3838dc7f711916bcec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905603"
---
# <a name="develop-and-establish-service-agreements-overview"></a>Yfirlit yfir þróaða og innleidda þjónustusamninga

[!include [banner](../includes/banner.md)]

Með þjónustusamningum er hægt að skilgreina tilföngin sem eru notuð í dæmigerðri þjónustuheimsókn og hvernig þessi tilföng eru reikningsfærð á viðskiptavininn.

Allir þjónustusamningar eru tengdir við verk sem færslur eru bókaðar á og reikningsfærðar. Engu að síður er einnig hægt að reikningsfæra færslur þjónustupöntunar beint í gegnum verk án þess að þurfa fyrst að tengja þjónustupöntun við þjónustusamning. Þetta mætti til dæmis gera þegar þjónustupöntun hefur aðeins eina þjónustuheimsókn og mikilvægara er að vinna þjónustufærslur fljótt en að skrá nákvæmar upplýsingar um viðskiptavininn yfir langt tímabil fyrir þjónustusamninginn.

## <a name="service-agreement"></a>Þjónustusamningur

Tilgreina verður verk, kenni þjónustusamnings og flokk þjónustusamnings í öllum þjónustusamningum. Nota má flokk þjónustusamnings til að raða og skipuleggja þjónustusamninga.

Haus þjónustusamnings inniheldur stillingar sem eiga við allar tengdar þjónustusamningslínur:

-  Hvort þjónustusamningurinn sé ógildur. Ef þjónustusamningurinn er ógildur er ekki hægt að mynda þjónustupantanir úr þjónustusamningnum.
-  Lengd þjónustusamningsins.
-  Hvernig þjónustupantanalínur eru sameinaðar í þjónustupantanir.
-  Hvort þjónustusamningurinn sé sniðmát.

Allir þjónustuhlutir og þjónustuverk sem hægt er að nota með þjónustusamningnum eru einnig sett upp í haus þjónustusamningsins með því að færa inn þjónustuverk eða þjónustuhlut sem á að tengja við ýmsar línur samningsins.

Einnig er hægt að afrita línur þjónustusamnings eða þjónustusniðmáts úr haus þjónustusamnings í gildandi þjónustusamning.

Hægt er að fresta þjónustusamningum og stöðva einstakar þjónustusamningslínur.

Ef gátreiturinn **Frestað** er valinn fyrir þjónustusamning er ekki hægt að:

-    Stofna þjónustupantanir sjálfvirkt eða handvirkt út frá þjónustusamningnum.

Ef gátreiturinn **Stöðvað** er valinn fyrir þjónustusamningslínur er ekki hægt að:

-    Stofna þjónustupantanir sjálfvirkt eða handvirkt út frá þjónustusamningslínuna.
-    Afritið þjónustusamningslínuna í annan þjónustusamning eða þjónustupöntun.


> [!NOTE]
> Ef þjónustusamning er frestað eru allar tengdar línur stöðvaðar óháð einstakri stöðu þeirra.

## <a name="service-agreement-lines"></a>Þjónustusamningslínur

Línur þjónustusamninga lýsa nákvæmlega efni umbeðinnar þjónustuvinnu. Línurnar innihalda eftirfarandi stillingar:

-  Færslugerð og lýsing á færslugerð.
-  Starfsmanninn sem framkvæmir vinnuna.
-  Hluti sem þarf að þjónusta fyrir þjónustusamninginn.
-  Hve oft vinna er unnin og tengdar vöru-, kostnaðar- þóknanafærslur eru skráðar.
-  Tímagluggann sem sameina má þjónustupantanalínur í þjónustupöntun.
-  Þjónustuverkin sem eru notuð til að sameina margar samningslínur í verkefni og til að búa til samantekt fyrir tæknimenn og viðskiptavini um hvaða þjónustuverk eigi að veita.
-  Hvort lína hafi verið stöðvuð. Ef lína hefur verið stöðvuð er ekki hægt að stofna þjónustupantanir fyrir hana.
-  Verkstillingar á borð við tegund og línueiginleika.

## <a name="related-articles"></a>Tengdar greinar

[Þjónustusamningar stofnaðir](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]