---
title: Stofna líkanastigveldi fyrir B2B-fyrirtæki
description: Í þessu efnisatriði er lýst hvernig á að stofna líkanastigveldi fyrirtækis fyrir B2B-fyrirtæki.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 91cb01637faa69bd3c7fefefae69c60cb948510e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211226"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>Stofna líkanastigveldi fyrir B2B-fyrirtæki

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig á að stofna líkanastigveldi fyrirtækis fyrir B2B-fyrirtæki í Microsoft Dynamics 365 Commerce.

Í Commerce Headquarters koma einingar viðskiptavina og viðskiptavinastigveldis fram fyrir hönd fyrirtækja viðskiptafélaga. Fyrirtækið viðskiptafélaga og notendur þess koma fram sem viðskiptavinir og stigveldi viðskiptavina eru notuð til að tengja þessa viðskiptavini hvern við annan.

Þegar beiðni viðskiptafélagi um að tengjast B2B-svæði fyrir rafræn viðskipti er samþykkt eru eftirfarandi aðgerðir framkvæmdar:

- Tvær nýjar viðskiptavinafærslur eru stofnaðar í kerfinu: Viðskiptavinafærsla af **Gerð: Fyrirtæki** fyrir fyrirtæki viðskiptafélaga og viðskiptavinafærsla af **Gerð: Einstaklingur** fyrir beiðandann (þ.e. notandi viðskiptafélaga sem sendi inn beiðnina).
- Ný stigveldisfærsla viðskiptavinar er stofnuð undir **Viðskiptavinur \> Stigveldi viðskiptavinar**. Þessi færsla er með eftirfarandi eiginleika í haus:

    - **Stigveldisauðkenni viðskiptavinar** – Einkvæmt kenni fyrir stigveldi viðskiptavinar. Þetta kenni notar númeraröð sem er skilgreind í samnýttum viðskiptafæribreytum í Commerce Headquarters.
    - **Heiti** – Fyrirtækisheiti viðskiptafélagans eins og það er tilgreint í innleiðingarferlinu.
    - **Tilgangur** – Þessi eiginleiki er stilltur á fyrirframskilgreint gildi **B2B-fyrirtæki**.
    - **Fyrirtæki** – Viðskiptavinakenni viðskiptafélagans.

Hér eru upplýsingarnar um stigveldisfærslu viðskiptavinar:

- Viðskiptavinafærsla beiðandans tengist stigveldi viðskiptavinarins.
- Stjórnandahlutverkið tengist beiðandanum.

Þegar stjórnandinn bætir fleiri notendum við fyrirtæki viðskiptafélagans á B2B-svæðinu verður ný viðskiptavinafærsla stofnuð fyrir hvern notanda í Commerce Headquarters. Þessari viðskiptavinafærslu er einnig bætt við viðeigandi stigveldi viðskiptavinar fyrir viðskiptafélagann og er með hlutverk „notanda“.

> [!NOTE]
> Í flestum tilfellum ættu samsvarandi gildi eiginleika allra viðskiptavinafærslna í stigveldi að passa saman. Sem dæmi, þar sem allir notendur viðskiptafélaga eiga að fá svipuð verð fyrir afurðir, ætti verðflokkur þeirra og tengdar skilgreiningar að passa saman. Kerfið framfylgir samt sem áður ekki þessari samsvörun. Þess vegna eru tilheyrandi notendur Commerce Headquarters ábyrgir fyrir því að tryggja að gildi eiginleika og skilgreiningar passi saman fyrir alla viðskiptavini í tilgreindu stigveldi.

Notendur Commerce Headquarters geta skoðað gildi eiginleikanna fyrir allar færslu viðskiptavina í stigveldinu í tvískiptu yfirliti. Veljið viðeigandi eiginleika viðskiptavinafærslu með því að velja flipaheitin í fellivalmyndinni. Notendur geta skoðað og breytt eiginleikagildum í þessu yfirliti. Að öðrum kosti, ef á að nota öll gildin úr viðskiptavinafærslu stjórnanda í allar færslur viðskiptavina, skal velja **Hnekkja** í upplýsingum um stigveldi viðskiptavinar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2B-svæði fyrir rafræn viðskipti](set-up-b2b-site.md)

[Stjórna notendum viðskiptafélaga á B2B-svæði fyrir rafræn viðskipti](manage-b2b-users.md)

[Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti](payment-method.md)

[Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]