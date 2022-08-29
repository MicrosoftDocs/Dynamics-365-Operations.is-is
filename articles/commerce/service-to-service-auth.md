---
title: Stilla sannvottun milli þjónusta
description: Þessi grein lýsir því hvernig á að stilla þjónustu-til-þjónustu auðkenningu í Microsoft Dynamics 365 Commerce til að hringja á öruggan hátt í þjónustu API fyrir einkunnir og umsagnir.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: e3134d4ddb2e4f3d260e51d49e7399ff84e0d74a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279449"
---
# <a name="configure-service-to-service-authentication"></a>Stilla sannvottun milli þjónusta

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að stilla þjónustu-til-þjónustu (S2S) auðkenningu í Microsoft Dynamics 365 Commerce að hringja á öruggan hátt í þjónustuforritaviðmót (API) fyrir einkunnir og umsagnir.

Dynamics 365 Commerce tilboð [einkunnir og umsagnir](ratings-reviews-overview.md) sem alhliða lausn. Þessi lausn veitir aðgang að þjónustu API utan Commerce, þannig að hægt er að framkvæma ýmis verkefni. Þessi verkefni fela í sér innflutning á einkunnum og umsögnum úr ytra kerfinu þínu í Commerce og útflutning á einkunnum og umsögnum frá Commerce. Til að gera Commerce kleift að hringja á öruggan hátt í einkunnagjöf og umsagnarþjónustu API, verður þú fyrst að stilla S2S auðkenningu með því að klára ferlið í þessari grein.

## <a name="add-a-new-app-registration"></a>Bættu við nýrri app skráningu

Áður en þú bætir við nýrri appskráningu þarftu að búa til forrit með því að nota [Azure gátt](https://portal.azure.com). Til að skrá app í Azure Active Directory (Azure AD) og virkjaðu auðkenningu skaltu fylgja skrefunum í [Notaðu Azure Active Directory með sérsniðnu tengi í Power Automate](/connectors/custom-connectors/azure-active-directory-authentication).

Safnaðu eftirfarandi auðkennum frá Azure gáttinni. Þú þarft þessi auðkenni í skrefunum sem fylgja.

- Biðlaraforritskenni
- Auðkenni viðskiptavinaskrár (leiganda).

Fylgdu þessum skrefum til að bæta við nýrri app skráningu í Commerce site builder.

1. Farðu í **Heim \> Umsagnir \> Stillingar**.
1. Undir **Þjónustu-til-þjónustu (S2S) Auðkenning**, veldu **Stjórna**.

    ![Stjórna hnappur í þjónustu-til-þjónustu (S2S) Authentication hlutanum í Commerce site builder.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. Í **S2S app færslur** rúðu sem birtist hægra megin, veldu **Bættu við nýrri S2S app skráningu**.
1. Í **Bæta við S2S forritafærslu** valmynd, sláðu inn eftirfarandi nauðsynlegar upplýsingar. Notaðu gildin úr skráningu Azure forritsins.

    - **Nafn** – Sláðu inn heiti umsóknar þinnar (til dæmis, **Fabrikam app**).
    - **Auðkenni viðskiptavinarforrits** – Sláðu inn auðkenni forritsins (til dæmis **00000000-0000-0000-0000-000000000000**).
    - **Auðkenni skráa (leiganda).** – Sláðu inn auðkenni möppu (til dæmis, **00000000-0000-0000-0000-000000000000**).

    ![Bæta við S2S App Entry valmynd í Commerce site builder.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Veldu **Senda**. Nafn umsóknar þinnar ætti að birtast á listanum í **S2S app færslur** rúðu.
1. Lokaðu **S2S app færslur** rúðu.
1. Veldu **Vista**.

## <a name="edit-an-existing-app-registration"></a>Breyttu núverandi appskráningu

Fylgdu þessum skrefum til að breyta núverandi forritaskráningu í Commerce site builder.

1. Farðu í **Heim \> Umsagnir \> Stillingar**.
1. Undir **Þjónustu-til-þjónustu (S2S) Auðkenning**, veldu **Stjórna**.
1. Í **S2S app færslur** veldu blýantstáknið við hliðina á færslunni sem þú vilt breyta.
1. Uppfærðu gildi í **Nafn**, **viðskiptavinarforrits**, og **Auðkenni skráa (leiganda).** reiti eftir þörfum.
1. Veldu **Senda**.
1. Lokaðu **S2S app færslur** rúðu.
1. Veldu **Vista**.

## <a name="remove-an-existing-app-registration"></a>Fjarlægðu núverandi forritaskráningu

Fylgdu þessum skrefum til að fjarlægja núverandi forritaskráningu í Commerce site builder.

1. Farðu í **Heim \> Umsagnir \> Stillingar**.
1. Undir **Þjónustu-til-þjónustu (S2S) Auðkenning**, veldu **Stjórna**.
1. Í **S2S app færslur** veldu ruslafatatáknið við hliðina á færslunni sem þú vilt fjarlægja. Færslan er fjarlægð af listanum.
1. Lokaðu **S2S app færslur** rúðu.
1. Veldu **Vista**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Velja að nota einkunnir og umsagnir](opt-in-ratings-reviews.md)

[Stjórna einkunnum og umsögnum](manage-reviews.md)

[Skilgreina einkunnir og umsagnir](configure-ratings-reviews.md)

[Samstilla afurðaeinkunnagjöf](sync-product-ratings.md)

[Virkja handvirka birtingu einkunna og umsagna hjá stjórnanda](manual-publish-rating-reviews.md)

[Flytja einkunnir og umsagnir inn og út](import-export-reviews.md)

[Algengar spurningar um einkunnir og umsagnir](ratings-reviews-faq.md) 
