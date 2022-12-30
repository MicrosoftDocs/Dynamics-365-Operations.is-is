---
title: Eftirspurnarstýrð efnisþarfaráætlun (DDMRP) yfirlit
description: Þessi grein veitir upplýsingar um eftirspurnarstýrða áætlanagerð efnisþarfa (DDMRP), aðferð áætlanagerðar sem byggir á aftengingu framboðs og eftirspurnar.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740851"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Eftirspurnarstýrð efnisþarfaráætlun (DDMRP) yfirlit

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Í mörg ár hafa fyrirtæki notað efnisþarfaáætlun (MRP) sem kerfi til að reikna út hvaða efni og hluti þarf til að framleiða vöru. Hins vegar hafa aðfangakeðjur nú breyst. Hlutir hafa lengri endingartíma vegna þess að þeir eru í auknum mæli sóttir til útlanda. Þar af leiðandi hafa mörg fyrirtæki upplifað efnisskort eða umframefni því þau vita ekki hversu miklar birgðir á að geyma á lager. Einnig er meira flökt á markaðnum (stundum spáð á ónákvæman hátt) og viðskiptavinir eru að krefjast afurða með stuttum fyrirvara. Því er aðfangakeðjuskortur alls staðar í heiminum. Að auki veita MRP verkfæri skipuleggjendum þúsundir aðgerða. Því er erfitt að vita hverju á að einbeita sér að. Oft er lausnin á mörgum þessara vandamála að skipta yfir í eftirspurnarstýrða áætlanagerð efnisþarfa (DDMRP).

DDMRP er áætlanagerðaraðferð sem byggir á aftengingu framboðs og eftirspurnar. Þessi aftenging næst með því að setja upp vörur aftengingarpunkta. Fyrir þessar vörur er öryggisbirgðum haldið við til að tryggja að rétt magn sé geymt á lager. Aftenging framboðs og eftirspurnar hjálpar til við að koma í veg fyrir „svipuáhrif“ vegna þess að breytileikinn fer ekki í gegnum keðjuna. (*Svipuáhrifin* vísa til þess hvernig litlar sveiflur í eftirspurn á smásölustigi geta valdið smám saman stærri sveiflum í eftirspurn á heildsölu-, dreifingar-, framleiðanda- og hráefnisbirgjastigi.) Hverjum mörkum er ætlað að fullnægja notkun hluta og er einnig hægt að stilla til að bregðast við aukningum.

Sannað hefur verið að DDMRP er verðmæt áætlanagerð fyrir breytilegt umhverfi þar sem þoltími viðskiptavina er styttri en uppsafnaður afhendingartími.

## <a name="the-five-components-of-ddmrp"></a>Fimm íhlutir DDMRP

DDMRP hefur fimm hluti í röð (skref). Fyrstu þrír hlutarnir skilgreina í meginatriðum upphaflegu og breytilegu skilgreininguna á líkani eftirspurnarstýrðrar áætlanagerðar efnisþarfa. Síðustu tveir hlutarnir skilgreina hversdagslegar aðgerðir aðferðarinnar.

1. **[Birgðastaðsetning samkvæmt áætlun](ddmrp-inventory-positioning.md)** – Berðu kennsl á aftengingarpunkta í aðfangakeðjunetinu. Tengipunktar eru sérstakir punktar í aðfangakeðju þar sem þú setur upp öryggisbirgðir sem þú munt fylgjast með og fylla á.
2. **[Forstillingar og stöður öryggisbirgða](ddmrp-buffer-profile-and-levels.md)** – Fyrir hvern aftengingarpunkt skal bera kennsl á stærðir öryggisbirgða (lágmarksmagn, hámarksmagn og endurpöntunarpunkt) og endurpöntunarmagnið.
3. **[Sveigjanlegar leiðréttingar á öryggisbirgðum](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** – Leiðréttu öryggisbirgðastöður, samkvæmt breytilegum færibreytum aðgerða eða áætluðum tilvikum í framtíðinni.
4. **[Eftirspurnarstýrð áætlanagerð](ddmrp-planning.md)** – Búðu til birgðapantanir eftir þörfum. Þessar birgðapantanir innihalda framleiðslupantanir, innkaupapantanir og birgðaflutningspantanir
5. **[Sýnileg framkvæmd með mikilli samvinnu](ddmrp-visual-and-collaborative-execution.md)** – Keyrðu birgðapantanirnar með hjálp myndrænnar framsetningar.

DDMRP er yfirleitt notað af framleiðendum sem eru með margs uppskriftir á mörgum stigum. Hins vegar er einnig hægt að nota það á dreifingar- og smásölunet.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP í Dynamics 365 Supply Chain Management

DDMRP fylgir með Microsoft Dynamics 365 Supply Chain Management og krefst engra viðbótarleyfisgjalda. Í Supply Chain Management hefur DDMRP-virkninni verið bætt við fyrirliggjandi eininguna **Aðaláætlanagerð**. Hins vegar er þess krafist að þú notir viðbótina fyrir fínstillingu skipulagningar.

DDMRP er samþætt við núverandi áætlanagerð í Supply Chain Management og er notað ásamt þeim uppsetningum til að koma á réttum áætlanagerðum fyrir fyrirtækið þitt. Henni er stjórnað af nýjum þekjukóða sem er allt öðruvísi en tímabil, hám/lágm, þörf og svo framvegis. Þetta er ekki ný eining og hún kemur ekki í stað núverandi skipulagningar. Hins vegar gefur það þér meiri virkni til að nota.
