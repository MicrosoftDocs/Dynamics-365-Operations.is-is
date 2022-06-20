---
title: Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða
description: Þessi grein lýsir því hvernig á að setja upp a Microsoft Dynamics 365 Commerce Netverslunarsíða sem getur þjónað kraftmiklu efni, byggt á breytum vefslóða.
author: StuHarg
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: e2b13403ffb316059476a03857c849b4f9f8cb9c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884664"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein lýsir því hvernig á að setja upp a Microsoft Dynamics 365 Commerce Netverslunarsíða sem getur þjónað kraftmiklu efni, byggt á breytum vefslóða.

Hægt er að stilla síður rafrænna viðskipta til að þjóna mismunandi efni byggt á hluta vefslóðar. Þess vegna er síðan þekkt sem gagnvirk síða. Hlutinn er notaður sem færibreyta til að sækja efni síðunnar. Til dæmis síða sem er búin til í Site builder og nefnd **blogg\_ áhorfandi** er varpað á slóðina `https://fabrikam.com/blog`. Síðan er hægt að nota þessa síðu til að sýna mismunandi efni byggt á síðasta hlutanum vefslóðinni. Til dæmis er síðasti hlutinn í vefslóð `https://fabrikam.com/blog/article-1` **article-1**.

Þú getur líka hnekið færibreytum vefslóðahluta með síðugerðarsíðu. Til dæmis síða sem er búin til í Site builder og nefnd **blogg\_ samantekt** hægt að kortleggja á slóðina `https://fabrikam.com/blog/about-this-blog`. Þegar`https://fabrikam.com/blog` Slóð er beðin með`/about-this-blog` hluti á endanum, the **blogg\_ samantekt** innihald síðu er skilað í stað þess`/about-this-blog` hluti sem er túlkaður sem færibreyta til að nota af`https://fabrikam.com/blog` síðu. 

Þegar þú velur nöfn fyrir færibreyturnar sem á að senda á kviku síðuna, nafn kviku síðunnar eins og það birtist í vefslóðinni (`/blog` í dæminu hér að ofan) er ekki hægt að nota sem færibreytuheiti eða undirstreng færibreytuheiti. 

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

Þegar leiðin er skilgreind munu allar beiðnir til færibreytustilltu vefslóðarinnar skila síðunni sem tengist þeirri vefslóð. Ef einhver beiðni inniheldur viðbótarhluta verður tengdri síðu skilað og efni síðunnar verður sótt með því að nota hlutann sem færibreytu. Til dæmis,`https://fabrikam.com/blog/article-1` mun skila`https://fabrikam.com/blog` síða sem sýnir efnið sem það sótti með því að nota **/grein-1** breytu.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
