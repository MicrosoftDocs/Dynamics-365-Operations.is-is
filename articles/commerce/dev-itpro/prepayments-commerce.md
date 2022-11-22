---
title: Fyrirframgreiðslur inn Dynamics 365 Commerce
description: Þessi grein veitir yfirlit yfir vinnslu fyrir fyrirframgreiðslufærslur í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780203"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Fyrirframgreiðslur inn Dynamics 365 Commerce

[!include[banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir vinnslu fyrir fyrirframgreiðslufærslur í Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce vinnur úr fyrirframgreiðslufærslum fyrir eftirfarandi greiðslutegundir sem eru notaðar í viðskiptakröfum eða viðskipta:

- **Innborgun viðskiptavinareiknings** – Viðskiptavinur greiðir innborgun á sölustað (POS). Viðskipti afgreiðir innborgunina sem fyrirframgreiðslufærslu. Þegar þú bókar færsluna er greiðslubók búin til og bókuð á **Dagbókarskírteini** síðu í höfuðstöðvum Commerce. The **Fyrirframgreiðslubókarskírteini** gátreitinn á **Greiðsla** flipinn er sjálfkrafa valinn fyrir greiðslubók. Fyrir frekari upplýsingar, þar á meðal fyrirframgreiðslu og skatta-sértækar upplýsingar sem skipta máli fyrir marksvæðið, sjá [Hnattvæðingarúrræði - Lands-/svæðissértækt hjálparefni](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Pöntun viðskiptavinar sem hefur innborgun** – Viðskiptavinur býr til viðskiptavinapöntun á POS. Viðskiptavinurinn getur greitt innborgun fyrir pöntunina, byggt á sjálfgefna innborgunarprósentunni sem er stillt á **Pantanir viðskiptavina** síða í höfuðstöðvum viðskipta (**Viðskiptabreytur \> Pantanir viðskiptavina**). Commerce afgreiðir innborgunina fyrir pöntun viðskiptavinarins sem fyrirframgreiðslufærslu. Þegar þú bókar færsluna er greiðslubók búin til og bókuð á **Dagbókarskírteini** síðu. The **Fyrirframgreiðslubókarskírteini** gátreitinn á **Greiðsla** flipinn er sjálfkrafa valinn fyrir greiðslubók. Greiðslan er gerð upp og reikningur viðskiptavinarins er sjálfkrafa gefinn út þegar pöntun er sótt eða afhent.
- **Sölupöntun símaver** - Þjónustufulltrúi símavers býr til sölupöntun fyrir hönd viðskiptavinar, og **fyrirframgreiðslu** eiginleiki er stilltur á **Já** við greiðsluupptöku.

Commerce sinnir eftirfarandi verkefnum til að vinna úr fyrirframgreiðslu:

- **Vinna við innborgun viðskiptavinareiknings** – Innborgunargreiðsla sem viðskiptavinur gerir er flutt til Commerce með því að nota þjónustu sem samstillir gögn. Viðskipti búa til smásölugreiðslu fyrir greiðsluna. Þegar smásölufærslan er bókuð er staðgreiðslubók eða greiðslubók viðskiptavinar bókuð. The **Fyrirframgreiðslubókarskírteini** gátreitinn á **Greiðsla** flipi á **Dagbókarskírteini** síða í höfuðstöðvum Commerce er sjálfkrafa valin fyrir greiðslubók. Ekki er hægt að vinna fyrirframgreiðslur ef greiðsluupphæðin er neikvæð.
- **Vinna úr pöntun viðskiptavinar eða sölupöntun sem hefur innborgun** – Viðskiptavinur greiðir nauðsynlega innborgun fyrir pöntun viðskiptavinar með því að nota Commerce Data Exchange : Rauntímaþjónusta. Viðskipti stofnar annað hvort greiðslubók viðskiptavinar eða staðgreiðslubók, allt eftir greiðslumáta sem viðskiptavinurinn notar. The **Fyrirframgreiðslubókarskírteini** gátreitinn á **Greiðsla** flipi á **Dagbókarskírteini** síða er sjálfkrafa valin fyrir dagbókina í höfuðstöðvum Commerce. Ef viðskiptavinur notar marga greiðslumáta til að gera hlutagreiðslur, vinnur Commerce hverja hlutagreiðslu, byggt á greiðslumáta sem notaður var.

Fyrir kreditkort, og fyrir stafræn veski sem hafa undirliggjandi kreditkortagreiðslumáta, sendir Commerce „fanga“ beiðni eftir að hafa fengið heimild. (Fjár eru teknir áður en sölupöntun er reikningsfærð.)

Ef þú afturkallar pöntun viðskiptavinar er fyrirframgreiðsluupphæðin endurgreidd og greiðslubók fyrir endurgreiðslu er bókuð fyrir innborgunarupphæðina. Endurgreiðsluupphæðin er reiknuð út og bókuð, byggt á greiðslumáta sem þú tilgreindir þegar þú bókaðir endurgreiðslugreiðsluna. Commerce gæti beitt afpöntunargjaldi, byggt á hlutfallinu sem þú stillir á **Viðskiptabreytur** síðu í höfuðstöðvum Commerce.

Ef þú skilar pöntun viðskiptavinar er skilapöntun og greiðslubók fyrir endurgreiðslu stofnuð. Þegar þú bókar skilapöntun, stofnar Commerce annað hvort greiðslubók viðskiptavinar eða staðgreiðslubók, allt eftir greiðslumáta sem viðskiptavinurinn notaði fyrir upphaflegu færsluna.
