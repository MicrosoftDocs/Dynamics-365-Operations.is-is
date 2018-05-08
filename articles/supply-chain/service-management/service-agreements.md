---
title: "Þjónustusamningar"
description: "Með þjónustusamningum er hægt að skilgreina tilföngin sem eru notuð í dæmigerðri þjónustuheimsókn og hvernig þessi tilföng eru reikningsfærð á viðskiptavininn."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
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
ms.sourcegitcommit: bf9df2a31c758ba6b63ac7952e00065df04552dc
ms.openlocfilehash: aaff0c1d71fcf2656d5d6e76a2bf4b7b3a699281
ms.contentlocale: is-is
ms.lasthandoff: 02/19/2018

---

# <a name="service-agreements"></a>Þjónustusamningar

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

## <a name="related-topics"></a>Tengd efnisatriði

[Þjónustusamningar stofnaðir](create-service-agreements.md)

