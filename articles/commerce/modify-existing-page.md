---
title: Breyta síðu svæðis sem þegar er til
description: Þetta efni lýsir því hvernig á að breyta fyrirliggjandi svæði í Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c393fc143214c2c7c7ddad9a77e273e1e53e34ac
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003442"
---
# <a name="modify-an-existing-site-page"></a>Breyta síðu svæðis sem þegar er til


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að breyta fyrirliggjandi svæði í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Þegar þú verður að breyta síðu er fyrsta skrefið að opna hana í ritlinum. Farðu á svæðið sem inniheldur síðuna þína og finndu síðan síðuna sem þú vilt á lista með síðum. Ef þú finnur ekki síðuna geturðu notað ríka leitarmöguleika höfundartækisins. Annaðhvort slærðu nákvæmlega inn nafn síðunnar eða sláðu inn fyrstu stafina í því og síðan stjörnu (\*). Síaður listi yfir síður birtist. Þú getur notað þennan lista til að finna síðuna sem þú vilt. Þegar þú hefur fundið rétta síðu skaltu velja heiti síðunnar til að opna síðuna í ritlinum.

> [!TIP]
> Ef síðan þín er sýnileg í eftirlitsaðila síðu geturðu valið hana og skoðað hana áður en þú opnar hana í ritlinum. Á þennan hátt geturðu skoðað margar síður á sama tíma.

Eftir að síðan er opin í ritlinum verður þú að ganga úr skugga um að hún sé skráðu út til þín. Skipanastikan í höfundatólinu er kvik, samhengisnæm og tekur tillit til stöðu. Þess vegna sýnir hún aðeins aðgerðir sem þú getur framkvæmt á blaðsíðu. Til dæmis, ef síðan er ekki skráð út til þín birtast hnapparnir **Vista** og **Innskráning** ekki á skipanastikunni. Staða síðunnar er einnig sýnd hægra megin í glugganum.

Ef síðan er ekki þegar skráð út á þig skaltu velja **Skrá út** á skipanastikunni. Skipunarstikan breytist til að endurspegla nýja stöðu síðunnar. Þú færð einnig tilkynningu þar sem fram kemur að síðan hafi verið skráð út á þig.

Næsta skref er að gera raunverulegar breytingar. Oft notarðu útlínutré síðunnar til vinstri til að finna og velja eininguna sem þú vilt breyta og gera síðan breytingar í eiginleikaglugganum til hægri. 

Hins vegar gæti breyting þín stundum falið í sér viðbót eða fjarlægingu líkana eða brota. Til að bæta við broti eða einingunni skaltu nota útlitsgreinatréð til að finna raufina sem þú vilt bæta einingunni eða brotinu við og veldu síðan úrfellingarhnappinn (**...**) fyrir það hólf. Valmynd birtist sem inniheldur skipanir til að bæta við einingu eða broti. Til að fjarlægja einingu eða brot, finndu og veldu það í útlitsstré síðunnar, veldu úrfellingarhnappinn og veldu síðan skipunina til að eyða einingunni eða brotinu.

> [!TIP]
> Þú getur líka skoðað og breytt eiginleikum fyrir hverja einingu sem er sýnileg í „það sem þú sérð er það sem þú færð“ (WYSIWYG) með því að velja það beint.

Eftir að þú hefur lokið við að gera breytingar þínar og forskoða áhrif þeirra ættirðu að skrá þig inn á síðuna með því að velja **Innskráning** á skipanastikunni. 

Til að birta breytingarnar þínar strax velurðu **Birta** á skipanastikunni. Síðasta innskráða útgáfan af síðunni sem þú breyttir er birt og verður tiltæk utanaðkomandi notendum sem skoða síðuna þína. 

## <a name="example-change-the-video-on-the-home-page"></a>Dæmi: Breyttu myndskeiðinu á heimasíðunni

Eftirfarandi dæmi sýnir hvernig á að breyta heimasíðunni með því að breyta myndbandinu sem birtist í einingunni.

1. Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).
1. Í stýriglugganum vinstra megin velurðu **Síður**.
1. Finndu og veldu heimasíðuna til að opna hana í ritlinum.
1. Á skipanastikunni velurðu **Skrá út**.
1. Í síðuútlínu velurðu hólfið **Aðal**.
1. Undir hólfinu **Aðal** stækkarðu allar einingar vökvaílátsins.
1. Finndu og veldu vídeóspilarann.
1. Í eiginleikaglugganum til hægri velurðu eiginleikann **myndskeið**. Eignarval birtist.
1. Í eignavali velurðu myndskeiðseignina eða velur **Hlaða upp nýrri eign** til að hlaða upp nýrri myndskeiðseign.
1. Veljið **Í lagi**.
1. Veldu **Vista** og síðan **Skrá inn**.
1. Í reitnum **Athugasemdir** slærðu inn **Myndskeiði breytt** og velur síðan **Í lagi**.
1. Veldu **Forskoða** til að forskoða uppfærða síðu. Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.
1. Velja **Birta**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Bæta við nýrri síðu á svæði](add-new-page.md)

[Velja síðuútlit](select-page-layouts.md)

[Stjórna SEO-lýsigögnum](manage-seo-metadata.md)

[Vista, forskoða og birta síðu](save-preview-publish-page.md)

[Bæta vörusíðu](enrich-product-page.md)

[Bæta lendingarsíðu flokks](enrich-category-page.md)

[Staðfesta aðgengi síðuinnihalds](verify-accessibility.md)
