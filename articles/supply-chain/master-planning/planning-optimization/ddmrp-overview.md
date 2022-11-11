---
title: Eftirspurnardrifið efnisþörf skipulagning (DDMRP) yfirlit
description: Þessi grein veitir upplýsingar um Demand Driven Material Requirements Planning (DDMRP), skipulagsaðferðafræði sem byggir á aftengingu framboðs og eftirspurnar.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: cf5ca3996a882111b840e3acb5e2a4f3f26ec4b7
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740851"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Eftirspurnardrifið efnisþörf skipulagning (DDMRP) yfirlit

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Fyrirtæki hafa árum saman notað efniskröfur (MRP) sem kerfi til að reikna út efni og íhluti sem þarf til að framleiða vöru. Hins vegar hafa aðfangakeðjur nú breyst. Varahlutir hafa lengri afgreiðslutíma vegna þess að þeir eru í auknum mæli fengnir erlendis frá. Þess vegna hafa mörg fyrirtæki greint frá því að hafa orðið fyrir lagerútreikningum eða offramboði, vegna þess að þau vita ekki hversu mikið af birgðum á að geyma. Það eru líka meiri sveiflur á markaði (stundum ónákvæmar spár) og viðskiptavinir krefjast vöru á stuttum afgreiðslutíma. Þess vegna er skortur á birgðakeðju um allan heim. Að auki gefa MRP verkfæri skipuleggjendum oft þúsundir aðgerða til að gera. Þess vegna er erfitt að vita hvað á að leggja áherslu á. Oft er lausnin á mörgum þessara mála að skipta yfir í Demand Driven Material Requirements Planning (DDMRP).

DDMRP er skipulagsaðferðafræði sem byggir á því að aftengja framboð og eftirspurn. Þessi aftenging er náð með því að setja upp aftengingarpunkta. Fyrir þá hluti er biðminni viðhaldið til að tryggja að rétt magn af lager sé haldið. Aftenging framboðs og eftirspurnar hjálpar til við að koma í veg fyrir „bullwhip áhrif“ vegna þess að breytileiki fer ekki í gegnum keðjuna. (The *bullwhip áhrif* vísar til þess hvernig litlar sveiflur í eftirspurn á smásölustigi geta valdið sífellt meiri sveiflum í eftirspurn hjá heildsölu-, dreifingaraðila, framleiðanda og hráefnisbirgðastigi.) Hverjum stuðpúða er ætlað að standa undir meðalnotkun hluta og einnig er hægt að aðlaga hana. til að mæta auknum eftirspurn.

Sýnt hefur verið fram á að DDMRP sé dýrmæt áætlanagerð fyrir breytilegt umhverfi þar sem þoltími viðskiptavina er styttri en uppsafnaður leiðtími.

## <a name="the-five-components-of-ddmrp"></a>Fimm þættir DDMRP

DDMRP hefur fimm raðhluta (þrep). Fyrstu þrír þættirnir skilgreina í meginatriðum upphafs- og þróunarstillingar á eftirspurnardrifnu efnisþörfáætlunarlíkani. Síðustu tveir þættirnir skilgreina daglegan rekstur aðferðafræðinnar.

1. **[Stefnumótandi birgðastaða](ddmrp-inventory-positioning.md)** – Þekkja aftengingarpunkta í aðfangakeðjunetinu. Aftengingarpunktar eru sérstakir punktar í aðfangakeðjunni þinni þar sem þú setur birgðapúða sem þú munt fylgjast með og fylla á.
2. **[Buffer snið og stig](ddmrp-buffer-profile-and-levels.md)** – Fyrir hvern aftengingarpunkt, auðkenndu biðminni (lágmarksmagn, hámarksmagn og endurpöntunarpunkt) og endurpöntunarmagn.
3. **[Dynamic biðminni stillingar](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** - Stilltu biðminni, byggt á mismunandi rekstrarbreytum eða fyrirhuguðum framtíðaratburðum.
4. **[Eftirspurnarstýrð áætlanagerð](ddmrp-planning.md)** – Búðu til birgðapantanir eins og þær eru nauðsynlegar. Þessar birgðapantanir innihalda framleiðslupantanir, innkaupapantanir og birgðaflutningspantanir
5. **[Mjög samvinnufús og sýnileg framkvæmd](ddmrp-visual-and-collaborative-execution.md)** - Keyrðu birgðapantanir með hjálp sjónrænnar.

DDMRP er venjulega notað af framleiðendum sem eru með fjölþrepa efnisskrá (BOM). Hins vegar er einnig hægt að nota það á dreifingar- og smásölunet.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP inn Dynamics 365 Supply Chain Management

DDMRP fylgir Microsoft Dynamics 365 Supply Chain Management og krefst ekki viðbótar leyfisgjalda. Í Supply Chain Management hefur DDMRP virkni verið bætt við núverandi **Aðalskipulag** mát. Hins vegar krefst þess að þú notir áætlanagerð fínstillingarviðbótina.

DDMRP er samþætt við núverandi skipulagsuppsetningar í Supply Chain Management og er notað ásamt þeim uppsetningum til að komast að réttri skipulagsuppsetningu fyrir fyrirtæki þitt. Það er stjórnað af nýjum þekjukóða sem er allt öðruvísi en tímabil, lágmark/hámark, kröfu og svo framvegis. Það er ekki ný eining og kemur ekki í stað núverandi skipulagsvirkni. Hins vegar gefur það þér meiri virkni til að nota.
