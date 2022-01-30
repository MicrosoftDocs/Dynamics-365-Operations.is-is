---
title: Virkja handvirka birtingu einkunna og umsagna hjá stjórnanda
description: Í þessu efnisatriði er lýst hvernig hægt er að virkja handvirka birtingu einkunna og umsagna stjórnenda í Microsoft Dynamics 365 Commerce og hvernig hægt er að birta einkunnir og umsagnir handvirkt.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 443ebaa13d7ac29df66ffe77a2ed938e44a0c488
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968204"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Virkja handvirka birtingu einkunna og umsagna hjá stjórnanda

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er lýst hvernig hægt er að virkja handvirka birtingu einkunna og umsagna stjórnenda í Microsoft Dynamics 365 Commerce og hvernig hægt er að birta einkunnir og umsagnir handvirkt.

Lausn einkunna og umsagna Dynamics 365 Commerce notar Azure Cognitive Services til að sjálfkrafa ritskoða blótsyrði í titlum og efni umsagna og til að birta einkunnir og umsagnir. Því þarf ekki að grípa til handvirkrar íhlutunar til að yfirfara og birta einkunnir og umsagnir á svæði rafrænna viðskipta.

Sum fyrirtæki gætu hins vegar viljað að ritstjórar yfirfari og samþykki umsagnir handvirkt áður en þær eru birtar. Til að virkja handvirka birtingu einkunna og umsagna af hendi ritstjóra verður að virkja eiginleikann **Krefjast ritstjóra fyrir einkunnir og umsagnir** í vefsmið Commerce.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Virkja eiginleikann Krefjast ritstjóra fyrir einkunnir og umsagnir í vefsmið Commerce

Til að virkja eiginleikann **Krefjast ritstjóra fyrir einkunnir og umsagnir** í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Heim \> Umsagnir \> Stillingar**.
1. Stilltu valkostinn **Fara fram á að ritstjóri gefi einkunnir og umsagnir** á **Virkt**.

> [!NOTE]
> Með því að virkja eiginleikann **Fara fram á að ritstjóri gefi einkunnir og umsagnir** stöðvar þú sjálfvirka birtingu einkunna og umsagna þannig að handvirk birting er nú áskilin. Azure Cognitive Services mun hinsvegar halda áfram að ritskoða blótsyrði í titlum og efni umsagna.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Birta einkunnir og umsagnir

Þegar þú virkjar eiginleikann **Fara fram á að ritstjóri gefi einkunnir og umsagnir** verður ritstjóri að handvirkt fara yfir og birta einkunnir og umsagnir þannig að þær birtist á svæði rafrænna viðskipta.

Til að fara yfir og birta einkunnir og umsagnir í vefsmið Commerce skal fylgja þessum skrefum.

1. Fara í **Umsagnir \> Breytingar**.
1. Í hnitanetinu, ef reiturinn **Staða** fyrir línu er stilltur á **Óbirt** hefur einkunn og umsögn í þeirri línu ekki enn verið birt. Til að skoða aðeins óbirtar einkunnir og umsagnir skal velja **Staða: Þarfnast yfirferðar** í stöðusíunni fyrir ofan hnitanetið.
1. Veldu eina eða fleiri einkunnir og umsagnir sem eru með stöðuna **Óbirt** og veldu síðan **Birta** á skipanastikunni. Völdum einkunnum og umsögnum er bætt við birtingaröðina og þær munu birtast á vefsvæði rafrænna viðskipta eftir að þær eru birtar.

> [!NOTE]
> - Eftir að einkunn og umsögn hafa verið birt breytist stöðugildið úr **Óbirt** í núllgildi (auðan reit).
> - Ef þú velur margar einkunnir og umsagnir sem eru með blandaðar stöður og velur síðan **Birta** verða einkunnir og umsagnir birtar sem hafa ekki enn verið birtar. Einkunnir og umsagnir sem hafa þegar verið birtar verða hins vegar ekki birtar aftur.

Eftirfarandi mynd sýnir dæmi þar sem þrjár óbirtar einkunnir og umsagnir eru valdar á síðunni **Breytingar** í vefsmið Commerce.

![Þrjár óbirtar einkunnir og umsagnir valdar á síðu breytinga í vefsmið Commerce.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Velja að nota einkunnir og umsagnir](opt-in-ratings-reviews.md)

[Stjórna einkunnum og umsögnum](manage-reviews.md)

[Skilgreina einkunnir og umsagnir](configure-ratings-reviews.md)

[Samstilla afurðaeinkunnagjöf](sync-product-ratings.md)

[Inn- og útflutnings einkunnir og umsagnir](import-export-reviews.md)

[Stilla þjónustu-til-þjónustu auðkenningu](service-to-service-auth.md)

[Algengar spurningar um einkunnir og umsagnir](ratings-reviews-faq.md)
