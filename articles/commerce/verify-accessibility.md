---
title: Staðfesta aðgengi að efni síðu
description: Þetta efni lýsir því hvernig hægt er að sannreyna aðgengi að síðuinnihaldi í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7690f3bb17a56b9a16b6e818b675064b1979948e
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097366"
---
# <a name="verify-page-content-accessibility"></a>Staðfesta aðgengi að efni síðu


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig hægt er að sannreyna aðgengi að síðuinnihaldi í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Þegar þú hefur lokið við að breyta síðu ættirðu að ganga úr skugga um að innihaldið sé aðgengilegt fyrir alla á vefnum. Í höfundatækjum Commerce geturðu auðveldlega sannreynt aðgengi síðuefnisins með því að nota samþættu þjónustuna [Microsoft Accessibility Insights](https://accessibilityinsights.io/). Þessi þjónusta sannreynir innihald síðunnar gagnvart nýjustu viðmiðunarreglunum [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility).

Kveikja verður á samþættingu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) á leigjanda- eða vefsvæðisstigi áður en hægt er að nota hana.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Kveiktu á Microsoft Accessibility Insights fyrir öll vefsvæði leigjandans

Til að kveikja á [Microsoft Accessibility Insights](https://accessibilityinsights.io/) fyrir öll svæði Commerce í leigjandanum skal fylgja þessum skrefum.

> [!NOTE]
> Til að fara í leigjandastillingar verður þú að vera skráð/ur inn í Commerce sem kerfisstjóri.

1. Skráðu þig inn í Commerce sem kerfisstjóri.
1. Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.
1. Undir **Leigjandastillingar** velurðu **Eiginleikar**.
1. Stilltu valkostinn **Aðgengisathugun** **Kveikt**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Kveiktu á Microsoft Accessibility Insights fyrir stakt vefsvæði

Til að kveikja á [Microsoft Accessibility Insights](https://accessibilityinsights.io/) fyrir stakt svæði Commerce skal fylgja þessum skrefum.

1. Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).
1. Í vinstri yfirlitsglugganum velurðu **Svæðisstillingar** til að stækka hann.
1. Undir **Svæðisstillingar** velurðu **Eiginleikar**.
1. Stilltu valkostinn **Aðgengisathugun** **Kveikt**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Staðfestu aðgengi efnisins á heimasíðunni

Til að nota samþætta þjónustu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) til að skanna og staðfesta innihald heimasíðunnar í Commerce skal fylgja þessum skrefum.

1. Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).
1. Í vinstri stýriglugganum velurðu **Síður**.
1. Finndu og veldu heimasíðuna til að opna hana í ritlinum.
1. Á skipanastikunni velurðu **Athuga aðgengi**. Síðan **Athuga aðgengi** birtist.
1. Eftir að skönnuninni er lokið skaltu skoða innihald skýrslunnar.
1. Ef einhverjar athuganir misfórust skaltu velja hvert misheppnað athugunaratriði til að stækka það svo hægt sé að skoða frekari upplýsingar.
1. Til að loka skýrslunni eftir að þú hefur lokið við að skoða hana skal fletta neðst á síðuna **Athuga aðgengi** og velja **Í lagi**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta síðu svæðis sem þegar er til](modify-existing-page.md)

[Bæta við nýrri síðu á svæði](add-new-page.md)

[Velja síðuútlit](select-page-layouts.md)

[Stjórna SEO-lýsigögnum](manage-seo-metadata.md)

[Vista, forskoða og birta síðu](save-preview-publish-page.md)

[Bæta vörusíðu](enrich-product-page.md)

[Bæta lendingarsíðu flokks](enrich-category-page.md)

[Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]