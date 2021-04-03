---
title: Bæta vörusíðu
description: Þetta efnisatriði lýsir hvernig á að auðga vörusíðu í Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1d7899ac79805abeb55323bd21f83b3af38e09b4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238679"
---
# <a name="enrich-a-product-page"></a>Bæta vörusíðu


[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að auðga vörusíðu í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Sjálfgefið er að vefsíðan þín noti almenna síðu til að sýna vörugögn. Þessi síða inniheldur grunnupplýsingar um vöruna og stjórntæki sem þarf til að selja hana. Hins vegar geturðu bætt við upplýsingarnar sem koma frá Commerce Scale Unit með viðbótarmyndum eða texta fyrir tiltekna afurð. Þetta ferli er þekkt sem að auðga vörusíðuna.

Í mörgum tilvikum viltu nota sérstakt viðbótarefni fyrir vörur þínar. Þegar þú ferð til **Retail og Commerce** í höfundatólinu sérðu lista yfir afurðir af rásinni sem er úthlutað á svæðið. Í þessum lista gefur dálkurinn **Auðgað** til kynna hvort vörusíðan fyrir vöru hafi verið auðguð. Ef gátmerki birtist í dálknum er auðguð vörusíða til staðar fyrir vöruna. Ef ekkert hak birtist er sjálfgefna vörusíðan og innihald notað fyrir vöruna. Þú getur forskoðað bæði auðgaðar og óauðgaðar vörusíður með því að velja vöruheiti á listanum.

## <a name="enrich-a-product-page"></a>Bæta vörusíðu

Fylgdu þessum skrefum til að auðga vörusíðu.

1. Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).
1. Í stýriglugganum vinstra megin velurðu **Afurðir**.
1. Veldu allar vörur sem eru ekki með auðgaða vörusíðu.
1. Í aðgerðasvæðinu velurðu **Auðga afurðasíðu**.
1. Veldu **PDP-sniðmát** og síðan **Í lagi**.
1. Í útlínutré síðunnar til hægri stækkarðu hólfið **Aðal**.
1. Veldu úrfellingarhnappinn (**...**) fyrir hólfið **Aðal** og veldu síðan **Bæta við einingu**.
1. Veldu **Gámur 2** og síðan **Í lagi**.
1. Veldu úrfellingarhnappinn fyrir **Gámur 2** og veldu síðan **Bæta við einingu**.
1. Veldu **Eiginleiki** og síðan **Í lagi**.
1. Í eiginleikaglugganum til hægri, í reitnum **Sniðinn texti** slærðu inn uppfærða lýsingu vörunnar.
1. Í reitinn **Fyrirsögn** slærðu inn fyrirsagnartexta og velur síðan **Í lagi**.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Í reitnum **Athugasemdir** slærðu inn **Afurð auðguð** og velur síðan **Í lagi**.
1. Veldu **Forskoða** til að forskoða auðgaða afurðasíðu. Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.
1. Velja **Birta**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta síðu svæðis sem þegar er til](modify-existing-page.md)

[Bæta við nýrri síðu á svæði](add-new-page.md)

[Velja síðuútlit](select-page-layouts.md)

[Stjórna SEO-lýsigögnum](manage-seo-metadata.md)

[Vista, forskoða og birta síðu](save-preview-publish-page.md)

[Bæta lendingarsíðu flokks](enrich-category-page.md)

[Staðfesta aðgengi að efni síðu](verify-accessibility.md)

[Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]