---
title: Eining yfirlitsvalmyndar
description: Þetta efnisatriði fjallar um einingar yfirlitsvalmyndar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2020
ms.locfileid: "4413295"
---
# <a name="navigation-menu-module"></a>Eining yfirlitsvalmyndar

[!include [banner](includes/banner.md)]

Þetta efnisatriði fjallar um einingar yfirlitsvalmyndar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Aðaltilgangurinn einingar yfirlitsvalmyndar er að leyfa notendum vefsvæða að skoða vörur og síður samkvæmt yfirlitsstigveldi rásar sem er skilgreint í Dynamics 365 Commerce höfuðstöðvum. Vörur sem eru skilgreindar í einingu yfirlitsvalmyndar birtast sem yfirlit síðuhauss. Einingar yfirlitsvalmyndar styðja einnig föst valmyndaratriði sem tengjast öðrum síðum á e-Commerce svæði.

Hægt er að bæta einingu yfirlitsvalmyndar í hauseiningu síðu. Í Fabrikam-þema sýnir yfirlitsvalmynd sjálfgefið tvö stig. Í Upphafsþema sýnir yfirlitsvalmynd sjálfgefið tvö stig. Til að breyta fjölda stiga er skoðunarviðbót nauðsynleg við þemað.

Eftirfarandi mynd sýnir dæmi um yfirlitsvalmynd fyrir Fabrikam-svæðið með tveimur stigum tegundastigveldis og nokkrum föstum valmyndaratriðum.
![Dæmi um einingu yfirlitsvalmyndar](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Eiginleikar einingar yfirlitsvalmyndar

| Nafn eiginleika             | Virði                 | lýsing |
|---------------------------|-----------------------|-------------|
| Uppruni                  | **Retail**, **Handvirk höfundarvinna**, **Retail og handvirk höfundarvinna** | **Retail**-gildið leyfir birtingu yfirlitsstigveldi rásarinnar úr Commerce Headquarters í yfirlitsvalmyndinni. **Handvirk höfundarvinna**-gildi leyfir umsjón með föstum valmyndaratriðum. **Retail og handvirk höfundarvinna** leyfir blöndu af hvoru tveggja. |
| Sýna flokkamyndir | **Satt** eða **Ósatt**    | Þegar þetta er virkt birtir þessi eiginleiki flokkamyndir á yfirlitsvalmyndinni eins og skilgreint er í höfuðstöðvum Commerce fyrir hvern flokk. Bætt við í Commerce Release 10.0.14. |
| Virkja stigskipta yfirlitsvalmynd | **Satt** eða **Ósatt** | Þegar þessi eiginleiki er virkur getur yfirlitsvalmynd sýnt mörg stig yfirlitsstigveldis. Þessi eiginleiki er fáanlegur í Dynamics 365 Commerce útgáfu 10.0.15. |
| Stigafjöldi | heiltala | Þessi eiginleiki skilgreinir fjölda stiga sem á að sýna ef **Virkja stigskipta yfirlitsvalmynd** eiginleikinn er stilltur á **Satt**. |
| Fast valmyndaratriði| Fylki gilda| Föst valmyndaratriði sem tengja heiti valmyndaratriðis við tengil á fasta síðu vefsvæða. Hægt er að búa til valmyndaratriði fyrir neðan önnur valmyndaratriði. Fastar valmyndir birtast sjálfkrafa á rótarstigi og þeim verður bætt við yfirlitsstigveldi rásar ef það er til staðar. |
| Sýna rótarvalmynd | **Satt** eða **Ósatt** | Þegar þessi eiginleiki er virkur er hægt að skilgreina yfirlitsvalmynd undir sérstilltri rót (til dæmis **Versla núna**). Þessi eiginleiki er fáanlegur í Dynamics 365 Commerce útgáfu 10.0.15. |
| Rótarvalmynd | strengur | Hægt er að nota þennan eiginleika til að skilgreina texta fyrir sérstillta rót ef **Sýna rótarvalmynd** eiginleikinn er stillt á **Satt**. |

Eftirfarandi mynd sýnir dæmi um tegund myndar sem birtist á yfirlitsvalmyndinni fyrir Fabrikam-svæðið.
![Dæmi um einingu yfirlitsvalmyndar með flokkamyndum](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Bæta einingu yfirlitsvalmyndar við hauseiningu

Frekari upplýsingar um hvernig á að bæta við einingu yfirlitsvalmyndar í hauseiningu er að finna í [Hauseining](author-header-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Brauðmylsnueining](add-breadcrumb.md)

[Svæðisvalseining](site-selector.md)

[Kaupgluggaeining](add-buy-box.md)

[Reglufylgni köku](cookie-compliance.md)

[Eining síðuhauss](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]