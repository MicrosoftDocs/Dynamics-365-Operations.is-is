---
title: Breyta síðu svæðis sem þegar er til
description: Þetta efnisatriði lýsir því hvernig á að breyta fyrirliggjandi svæðssíðu í Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803730"
---
# <a name="modify-an-existing-site-page"></a>Breyta síðu svæðis sem þegar er til

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að breyta fyrirliggjandi svæðssíðu í Microsoft Dynamics 365 Commerce.

Þegar þú verður að breyta síðu er fyrsta skrefið að opna hana í ritlinum. Farðu á svæðið sem inniheldur síðuna þína og finndu síðan síðuna sem þú vilt á lista með síðum. Ef þú finnur ekki síðuna geturðu notað ríka leitarmöguleika höfundartækisins. Annaðhvort slærðu nákvæmlega inn nafn síðunnar eða sláðu inn fyrstu stafina í því og síðan stjörnu (\*). Síaður listi yfir síður birtist. Þú getur notað þennan lista til að finna síðuna sem þú vilt. Þegar þú hefur fundið rétta síðu skaltu velja heiti síðunnar til að opna síðuna í ritlinum.

> [!TIP]
> Ef síðan þín er sýnileg í síðuskoðun geturðu valið **Breyta** og skoðað síðuna áður en þú opnar hana í síðuritlinum. Á þennan hátt geturðu skoðað margar síður á sama tíma.

Eftir að síðan er opin í ritlinum verður þú að ganga úr skugga um að hún sé skráðu út til þín. Skipanastikan í höfundatólinu er kvik, samhengisnæm og tekur tillit til stöðu. Þess vegna sýnir það aðeins aðgerðir sem þú getur framkvæmt á síðunni núna. Til dæmis, ef síðan er ekki merkt þér birtast hnapparnir **Vista** og **Ljúka við breytingar** ekki á skipanastikunni. Staða síðunnar er einnig sýnd hægra megin í glugganum.

Ef síðan er ekki merkt þér skaltu velja **Breyta** á skipanastikunni. Skipunarstikan breytist til að endurspegla nýja stöðu síðunnar. Þú færð einnig tilkynningu þar sem fram kemur að síðan hafi verið skráð út á þig.

Næsta skref er að gera raunverulegar breytingar. Oft notarðu útlínutré síðunnar til vinstri til að finna og velja eininguna sem þú vilt breyta og gera síðan breytingar í eiginleikaglugganum til hægri. 

Hins vegar gæti breyting þín stundum falið í sér viðbót eða fjarlægingu líkana eða brota. Til að bæta við broti eða einingunni skaltu nota útlitsgreinatréð til að finna raufina sem þú vilt bæta einingunni eða brotinu við og veldu síðan úrfellingarhnappinn (**...**) fyrir það hólf. Valmynd birtist sem inniheldur skipanir til að bæta við einingu eða broti. Til að fjarlægja einingu eða brot, finndu og veldu það í útlitsstré síðunnar, veldu úrfellingarhnappinn og veldu síðan skipunina til að eyða einingunni eða brotinu.

> [!TIP]
> Einnig er hægt að skoða og breyta eiginleikum fyrir einingu sem er sýnileg í forskoðun sýnilegs síðuhönnuðar með því að velja hana með beinum hætti.

Eftir að þú ert búinn að gera breytingar þínar og forskoða áhrif þeirra skaltu merkja við síðuna með því að velja **Ljúka við breytingar** á skipanastikunni. 

Til að birta breytingarnar þínar strax velurðu **Birta** á skipanastikunni. Síðasta innskráða útgáfan af síðunni sem þú breyttir er birt og verður tiltæk utanaðkomandi notendum sem skoða síðuna þína. 

## <a name="example-change-the-video-on-the-home-page"></a>Dæmi: Breyttu myndskeiðinu á heimasíðunni

Eftirfarandi dæmi sýnir hvernig á að breyta heimasíðunni með því að breyta myndbandinu sem birtist í einingunni.

1. Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).
1. Í stýriglugganum vinstra megin velurðu **Síður**.
1. Finndu og veldu heimasíðuna til að opna hana í ritlinum.
1. Á skipanastikunni velurðu **Breyta**.
1. Í síðuútlínu velurðu hólfið **Aðal**.
1. Undir hólfinu **Aðal** stækkarðu allar einingar vökvaílátsins.
1. Finndu og veldu vídeóspilarann.
1. Í eiginleikaglugganum til hægri velurðu eiginleikann **myndskeið**. Eignarval birtist.
1. Í eignavali velurðu myndskeiðseignina eða velur **Hlaða upp nýrri eign** til að hlaða upp nýrri myndskeiðseign.
1. Veljið **Í lagi**.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
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

[Staðfesta aðgengi að efni síðu](verify-accessibility.md)

[Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
