---
title: Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða
description: Þetta efnisatriði lýsir því hvernig setja á upp Microsoft Dynamics 365 Commerce-síðu rafrænna viðskipta sem getur þjónað gagnvirku efni, byggt á færibreytum vefslóða.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e72b738133b396848848d167cace80fe23694334
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098631"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir því hvernig setja á upp Microsoft Dynamics 365 Commerce-síðu rafrænna viðskipta sem getur þjónað gagnvirku efni, byggt á færibreytum vefslóða.

Hægt er að stilla síður rafrænna viðskipta til að þjóna mismunandi efni byggt á hluta vefslóðar. Þess vegna er síðan þekkt sem gagnvirk síða. Hlutinn er notaður sem færibreyta til að sækja efni síðunnar. Til dæmis er síða sem heitir **blogg\_yfirlit** stofnuð og tengd við vefslóðina `https://fabrikam.com/blog`. Síðan er hægt að nota þessa síðu til að sýna mismunandi efni byggt á síðasta hlutanum vefslóðinni. Til dæmis er síðasti hlutinn í vefslóð `https://fabrikam.com/blog/article-1` **article-1**.

Aðskildar sérsniðnar síður sem hnekkja gagnvirku síðunni geta einnig verið tengdar við hluta í vefslóðinni. Til dæmis er síða sem heitir **blogg\_samantekt** stofnuð og tengd við vefslóðina `https://fabrikam.com/blog/about-this-blog`. Þegar beðið er um þessa vefslóð kemur upp síðan **blogg\_samantekt** sem tengist færibreytunni **/about-this-blog** í staðinn fyrir síðuna **blogg\_yfirlit**.

> [!NOTE]
> Virknin til að hýsa, sækja og sýna efni gagnvirkrar síðu er innleidd með því að nota sérsniðna einingu. Frekari upplýsingar er að finna í [Stækkunarhæfni rásar á netinu](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Setja upp gagnvirka síðu fyrir rafræn viðskipti

Til að setja upp gagnvirka síðu fyrir rafræn viðskipti þarf að búa til gagnvirku síðuna, búa til grunnvefslóðina og skilgreina leiðina á gagnvirku síðuna.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Búa til síðu sem þjónar gagnvirku efni

Til að búa til síðu sem mun þjóna gagnvirku efni skal fylgja þessum skrefum í [Bæta við nýrri síðu á svæði](add-new-page.md). Síðan sem stofnuð er þarf innleiðingu einingar sem notar síðasta hlutann í vefslóð til að sækja efni frá ytri gagnagjafa. Frekari upplýsingar um sérsniðna þróun einingar er að finna í [Stækkunarhæfni rásar á netinu](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Stofna grunnvefslóð fyrir gagnvirka síðu

Til að stofna grunnvefslóð fyrir gagnvirka síðu í Commerce-vefsmið skal fylgja þessum skrefum.

1. Farið í **Vefslóðir** og veljið **Ný \> Ný vefslóð**.
1. Í svarglugganum **Stofna nýja vefslóð** skal velja **Innri síða**. Undir **Vefslóð** skal færa inn vefslóðina sem mun þjóna hlutverki leiðar fyrir gagnvirku síðuna (í þessu dæmi **/blog**). Veljið síðan **Næst**.
1. Í svarglugganum **Velja síðu** skal velja síðuna sem var stofnuð til að þjóna hlutverki gagnvirku síðunnar og síðan velja **Vista**.
1. Velja **Birta**.

### <a name="configure-the-route-to-the-dynamic-page"></a>Skilgreina leiðina á gagnvirka síðu

Til að skilgreina leiðina á gagnvirka síðu í Commerce-vefsmið skal fylgja þessum skrefum.

1. Farið í **Svæðisstillingar \> Viðbætur**.
1. Undir **Færibreytustilltar vefslóðir** skal velja **Bæta við** og síðan færa inn vefslóðina sem slegin var inn þegar vefslóðin var búin til (í þessu dæmi **/blog**).
1. Veljið **Vista og birta**.

Þegar leiðin er skilgreind munu allar beiðnir til færibreytustilltu vefslóðarinnar skila síðunni sem tengist þeirri vefslóð. Ef einhver beiðni inniheldur viðbótarhluta verður tengdri síðu skilað og efni síðunnar verður sótt með því að nota hlutann sem færibreytu. Til dæmis mun `https://fabrikam.com/blog/article-1` skila síðunni **blogg\_samantekt** og efni síðunnar verður sótt með því að nota færibreytuna **/article-1**.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Hnekkja færibreytustilltri vefslóð með sérsniðinni síðu

Til að hnekkja færibreytustilltri vefslóð með sérsniðinni síðu í Commerce-vefsmið skal fylgja þessum skrefum.

1. Farið í **Vefslóðir** og veljið **Ný \> Ný vefslóð**.
1. Í svarglugganum **Stofna nýja vefslóð** skal velja **Innri síða**. Undir **Vefslóð** skal færa inn vefslóðin sem inniheldur hlutann sem á að hnekkja (í þessu dæmi **/blog/about-this-blog**). Veljið síðan **Næst**.
1. Í svarglugganum **Velja síðu** skal velja sérsniðnu síðuna og síðan velja **Vista**.
1. Velja **Birta**.
1. Ef sérsniðna síðan hefur ekki enn verið birt skal fara í **Síður**, velja sérsniðna síðu og síðan velja **Birta**.

Þegar sérsniðna síðan hefur verið birt verður hún gefin upp í staðinn fyrir gagnvirku síðuna sem er með færibreytustillt efni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta síðu svæðis sem þegar er til](modify-existing-page.md)

[Bæta við nýrri síðu á svæði](add-new-page.md)

[Velja síðuútlit](select-page-layouts.md)

[Stjórna SEO-lýsigögnum](manage-seo-metadata.md)

[Vista, forskoða og birta síðu](save-preview-publish-page.md)

[Bæta vörusíðu](enrich-product-page.md)

[Bæta lendingarsíðu flokks](enrich-category-page.md)

[Staðfesta aðgengi að efni síðu](verify-accessibility.md)

[Stækkunarhæfni netrásar](e-commerce-extensibility/overview.md)
