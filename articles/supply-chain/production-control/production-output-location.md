---
title: Staðsetning framleiðsluúttaks
description: Þetta efnisatriði lýsir stigveldi sem notað er til að auðkenna staðsetningu framleiðsluúttaks.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e4002bf7dddb196edf306268ecc16e1bfa5d6d1e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211308"
---
# <a name="production-output-location"></a>Staðsetning framleiðsluúttaks

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir stigveldi sem notað er til að auðkenna staðsetningu framleiðsluúttaks.

Staðsetning frameiðsluúttaks er sú staðsetning þar sem fullunnin vara er fyrst geymd eftir að hún hefur verið framleidd. Yfirleitt, er þessi staðsetning nálægt framleiðsluferlinu sem framleiðir fullunna vöru. Staðsetning framleiðsluúttaks er notuð sem milligeymsla fyrir efni áður en það er fært á sendingarsvæði, geymslusvæði, staðsetningu framleiðsluinntaks fyrir framleiðsluferli forstreymis og o.s.frv. 

Sjálfgefin staðsetning framleiðsluúttaks er stillt þegar fullunnar vörur eru skráðar í framleiðslupöntun eða runupöntun. Eftirfarandi stigveldi er notað til að auðkenna þessa úttaksstaðsetningu:

1. Notaðu þá úttaksstaðsetningu sem er skilgreind í haus framleiðslupöntunar eða runupöntunar.
2. Ef engin staðsetning fyrirfinnst hér, skal nota úttaksstaðsetninguna sem skilgreind er í því tilfangi sem notað var af síðustu aðgerð sem er skilgreind í framleiðsluleið.
3. Ef engin staðsetning fyrirfinnst hér, skal nota úttaksstaðsetninguna sem skilgreind er í þeim tilfangahópi sem notaður var af tilfanginu fyrir síðustu aðgerð sem er skilgreind í framleiðsluleið.
4. Ef engin staðsetning finnst þar, skal nota þá úttaksstaðsetningu sem er skilgreind í því vöruhúsi sem er skilgreint fyrir framleiðslupöntunina.

Sjálfgefin staðsetning framleiðsluúttaks er aðeins skilgreind fyrir afurðir sem eru uppsettar með ítarlegum vöruhúsaferlum. Þegar þessi gerð vöru er skráð sem fullunnin er vöruhúsavinna af gerðinni **Frágangur á fullbúnum vörum** eða **Frágangur aukaafurða eða hliðarafurða** stofnuð. Þessi gerð vinnu notast við staðsetningu framleiðsluúttaks sem tiltektarstaðsetningu. Frágangsstaðsetningin ákvarðast af staðsetningarleiðbeiningum.
