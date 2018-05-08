---
title: "Stofna framleiðslupantanir"
description: "Þegar framleiðslupöntun er stofnuð er send beiðni um að hefja framleiðslu vöru. Framleiðslupöntunin inniheldur upplýsingar um það hvað verður framleitt, hversu mikið magn og áætluðu lokadagsetninguna. Hann inniheldur einnig upplýsingar um hvaða efni á að nota og hvaða ferli skuli fylgja til að framleiða vöruna."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d962dbf5a5a4e3847252171d3631f78341640bc7
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="create-production-orders"></a>Stofna framleiðslupantanir

[!include [banner](../includes/banner.md)]

Þegar framleiðslupöntun er stofnuð er send beiðni um að hefja framleiðslu vöru. Framleiðslupöntunin inniheldur upplýsingar um það hvað verður framleitt, hversu mikið magn og áætluðu lokadagsetninguna. Hann inniheldur einnig upplýsingar um hvaða efni á að nota og hvaða ferli skuli fylgja til að framleiða vöruna.

Framleiðslupöntun gengur í gegnum stig framleiðsluferlisins. Þegar pöntun er stofnuð er henni úthlutað stöðunni°**Stofnuð**. Þegar pöntun er lokið er henni úthlutað stöðunni°**Lokið**. Færibreytustilling í hverju°stigi heimilar notandanum að skilgreina hvert°skref. Stillingin getur verið stillt fyrir°einn notanda°eða fyrir alla notendur.

Framleiðsluuppskrift og leið í framleiðslu eru aðal einingar framleiðslupöntunar. Þær eru afritaðar í framleiðslupöntunina byggt á völdu vörunni og magni sem á að framleiða. Áður en framleiðslupöntun er ræst, er hægt að breyta framleiðsluuppskrift og leið.

Hægt er að stofna framleiðslupöntun við eftirfarandi kringumstæður:

-   Stofnað með framkvæmd aðaláætlunar byggt á eftirspurn efnis.
-   Stofnuð beint úr sölupöntunarlínu eða þegar framleiðslupöntun á hærra stigi er stofnuð og metin (fest framboð).
-   Stofnaðar handvirkt.





