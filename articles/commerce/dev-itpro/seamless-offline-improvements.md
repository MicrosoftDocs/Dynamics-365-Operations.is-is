---
title: Þægilegur rofi án nettengingar fyrir gjafakorta- og kreditreikningsaðgerðir
description: Þessi grein veitir yfirlit yfir endurbætur sem veita óaðfinnanlegur rofi án nettengingar fyrir sérstakar greiðslugerðir.
author: BrianShook
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: e0416a61bd5fd3b875b427ad8a6313d0e9936f0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869162"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Þægilegur rofi án nettengingar fyrir gjafakorta- og kreditreikningsaðgerðir

[!include [banner](../includes/banner.md)]

Ef sölustaður (POS) tæki missir tengingu sína við rásagagnagrunninn geta flestar POS aðgerðir og færslur sem voru í gangi haldið áfram eftir að gjaldkerinn fær viðvörunarskilaboð um tap tengingarinnar. Í sumum tilvikum hafa færslur þó þætti sem treysta á rauntímaþjónustuna og þeir þættir eru ekki studdir þegar POS er ekki tengt. Þessi grein lýsir nokkurri virkni sem hjálpar til við að draga úr áhrifum glataðrar tengingar í þessum aðstæðum.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Lokið við gjafakortafærslur án tengingar

Innri gjafakort eru háð rauntímaþjónustu þar sem nauðsynlegt er að viðhalda stöðunni fyrir gjafakortin í Microsoft Dynamics 365 Commerce höfuðstöðvum. Til að koma í veg fyrir svik eða önnur vandamál varðandi samstillingu er gjafakortum læst um leið og þeim er bætt við færslu. Lásaraðgerðin tryggir að ekki er hægt að nota gjafakort á mörgum útstöðvum á sama tíma. Þegar færslunni lýkur er gjafakortið uppfært og aflæst.

Hins vegar, ef POS tapar tengingu eftir að gjafakorti hefur verið bætt við færslu getur gjafakortið orðið ónothæft. Til að koma í veg fyrir þetta ástand er Dynamics 365 Commerce með færibreytu sem gerir kleift að ljúka færslum sem innihalda gjafakortslínu sem má ljúka meðan POS er ótengdur. Þegar kveikt er á þessari færibreytu verða gjafakortafærslur sem eru þvingaðar án nettengingar vistaðar ásamt færslum án nettengingar og þær verða samstilltar við Commerce Headquarters þegar færslur án nettengingar eru samstilltar. Samstillingin mun einnig opna gjafakortið þannig að hægt sé að nota það í annarri afgreiðslustöð.

Til að virkja virknina að ljúka gjafakortafærslum þegar skipt hefur verið í stillingu án nettengingar ferðu í flipann **Bókun** á síðunni **Færibreytur Commerce**. Á þeim flipa finnurðu flýtiflipann **Gjafakort** og stillir **Leyfa að vinna úr færslum á gjafakorti án tengingar** á **Já**.

![Gjafakortastilling án nettengingar.](../media/gift.png)

Færibreytur Commerce eru venjulega í skyndiminni. Þess vegna getur þetta tekið allt að sólarhring að taka gildi eftir að stilling þessa stika er uppfærð og dreifingaráætlunin er hafin til að samstilla breytinguna við rásina. Til að virkja breytinguna strax skaltu endurstilla Microsoft Internet Information Services (IIS).

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Lokið við kreditreikningsfærslur án tengingar

Eins og innri gjafakort er kreditreikningum miðlægt viðhaldið í Commerce Headquarters. Commerce er með færibreytu sem gerir kleift að ljúka kreditreikningsfærslum meðan POS er ótengdur. Þessi færibreyta virkar eins og gjafakortsbreytan sem nefnd var í fyrri hlutanum. Þegar kveikt er á færibreytunni verða kreditreikningsfærslur sem eru þvingaðar án nettengingar samstilltar aftur við gagnagrunn rásarinnar ásamt öðrum færslum sem gerðar voru meðan POS var ekki tengdur.

Til að virkja virknina að ljúka kreditreikningsfærslum þegar skipt hefur verið í stillingu án nettengingar ferðu í flipann **Bókun** á síðunni **Færibreytur Commerce**. Á þeim flipa finnurðu flýtiflipann **Kreditreikningur** og stillir **Leyfa að vinna úr kreditreikningsfærslum án tengingar** á **Já**.

![Kreditreikningsstillingar án nettengingar.](../media/creditmemo.png)

Færibreytur Commerce eru venjulega í skyndiminni. Þess vegna getur þetta tekið allt að sólarhring að taka gildi eftir að stilling þessa stika er uppfærð og dreifingaráætlunin er hafin til að samstilla breytinguna við rásina. Til að virkja breytinguna strax skaltu endurstilla IIS.

## <a name="related-articles"></a>Tengdar greinar

- [Virkni sölustaðar án nettengingar](../pos-offline-functionality.md)
- [Aðgerðir sölustaðar (POS) með og án nettengingar](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]