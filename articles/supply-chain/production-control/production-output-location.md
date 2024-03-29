---
title: Staðsetning framleiðsluúttaks
description: Þessi grein lýsir stigveldi sem er notað til að auðkenna staðsetningu framleiðsluúttaks.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 130db343c4d09f2b8d31bf8acad3dcceec2be32e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067942"
---
# <a name="production-output-location"></a>Staðsetning framleiðsluúttaks

[!include [banner](../includes/banner.md)]

Þessi grein lýsir stigveldi sem er notað til að auðkenna staðsetningu framleiðsluúttaks.

Staðsetning frameiðsluúttaks er sú staðsetning þar sem fullunnin vara er fyrst geymd eftir að hún hefur verið framleidd. Yfirleitt, er þessi staðsetning nálægt framleiðsluferlinu sem framleiðir fullunna vöru. Staðsetning framleiðsluúttaks er notuð sem milligeymsla fyrir efni áður en það er fært á sendingarsvæði, geymslusvæði, staðsetningu framleiðsluinntaks fyrir framleiðsluferli forstreymis og o.s.frv. 

Sjálfgefin staðsetning framleiðsluúttaks er stillt þegar fullunnar vörur eru skráðar í framleiðslupöntun eða runupöntun. Eftirfarandi stigveldi er notað til að auðkenna þessa úttaksstaðsetningu:

1. Notaðu þá úttaksstaðsetningu sem er skilgreind í haus framleiðslupöntunar eða runupöntunar.
2. Ef engin staðsetning fyrirfinnst hér, skal nota úttaksstaðsetninguna sem skilgreind er í því tilfangi sem notað var af síðustu aðgerð sem er skilgreind í framleiðsluleið.
3. Ef engin staðsetning fyrirfinnst hér, skal nota úttaksstaðsetninguna sem skilgreind er í þeim tilfangahópi sem notaður var af tilfanginu fyrir síðustu aðgerð sem er skilgreind í framleiðsluleið.
4. Ef engin staðsetning finnst þar, skal nota þá úttaksstaðsetningu sem er skilgreind í því vöruhúsi sem er skilgreint fyrir framleiðslupöntunina.

Sjálfgefin framleiðslustaða er aðeins sett upp fyrir vörur sem eru settar upp með því að nota vöruhúsakerfisferli (WMS). Þegar þessi gerð vöru er skráð sem fullunnin er vöruhúsavinna af gerðinni **Frágangur á fullbúnum vörum** eða **Frágangur aukaafurða eða hliðarafurða** stofnuð. Þessi gerð vinnu notast við staðsetningu framleiðsluúttaks sem tiltektarstaðsetningu. Frágangsstaðsetningin ákvarðast af staðsetningarleiðbeiningum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]