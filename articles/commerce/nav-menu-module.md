---
title: Eining yfirlitsvalmyndar
description: Þessi grein fjallar um leiðsagnarvalmyndareiningarnar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d58d3957749fa961b7be164a0a474ac90a23321f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281509"
---
# <a name="navigation-menu-module"></a>Eining yfirlitsvalmyndar

[!include [banner](includes/banner.md)]

Þessi grein fjallar um leiðsagnarvalmyndareiningarnar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Aðaltilgangurinn einingar yfirlitsvalmyndar er að leyfa notendum vefsvæða að skoða vörur og síður samkvæmt yfirlitsstigveldi rásar sem er skilgreint í Dynamics 365 Commerce höfuðstöðvum. Vörur sem eru skilgreindar í einingu yfirlitsvalmyndar birtast sem yfirlit síðuhauss. Einingar yfirlitsvalmyndar styðja einnig föst valmyndaratriði sem tengjast öðrum síðum á e-Commerce svæði.

Hægt er að bæta einingu yfirlitsvalmyndar í hauseiningu síðu. Í Fabrikam-þema sýnir yfirlitsvalmynd sjálfgefið tvö stig. Í Upphafsþema sýnir yfirlitsvalmynd sjálfgefið tvö stig. Til að breyta fjölda stiga er skoðunarviðbót nauðsynleg við þemað.

Eftirfarandi mynd sýnir dæmi um yfirlitsvalmynd fyrir Fabrikam-svæðið með tveimur stigum tegundastigveldis og nokkrum föstum valmyndaratriðum.
![Dæmi um einingu yfirlitsvalmyndar.](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Eiginleikar einingar yfirlitsvalmyndar

| Nafn eiginleika             | Virði                 | lýsing |
|---------------------------|-----------------------|-------------|
| Uppruni                  | **Retail**, **Handvirk höfundarvinna**, **Retail og handvirk höfundarvinna** | **Retail**-gildið leyfir birtingu yfirlitsstigveldi rásarinnar úr Commerce Headquarters í yfirlitsvalmyndinni. **Handvirk höfundarvinna**-gildi leyfir umsjón með föstum valmyndaratriðum. **Retail og handvirk höfundarvinna** leyfir blöndu af hvoru tveggja. |
| Sýna flokkamyndir | **Satt** eða **Ósatt**    | Þegar þetta er virkt birtir þessi eiginleiki flokkamyndir á yfirlitsvalmyndinni eins og skilgreint er í höfuðstöðvum Commerce fyrir hvern flokk. Bætt við í Commerce Release 10.0.14. |
| Sýna kynningarmyndir | **Satt** eða **Ósatt** | Þegar þessi eiginleiki er virkur er hægt að grunnstilla kynningartilboð með því að nota myndir, tengla og texta. Þessum eiginleika var bætt við í Commerce útgáfu 10.0.17. |
|Bæta við flokki kynningarefnis | Texti, mynd eða tengill | Þegar **Sýna kynningarmyndir** er virkur er hægt að bæta við texta, mynd eða tengli sem kynningarefni á yfirlitsvalmyndinni. |
| Virkja stigskipta yfirlitsvalmynd | **Satt** eða **Ósatt** | Þegar þessi eiginleiki er virkur getur yfirlitsvalmynd sýnt mörg stig yfirlitsstigveldis. Þessi eiginleiki er í boði í Commerce útgáfu 10.0.15. |
| Stigafjöldi | heiltala | Þessi eiginleiki skilgreinir fjölda stiga sem á að sýna ef **Virkja stigskipta yfirlitsvalmynd** eiginleikinn er stilltur á **Satt**. |
| Fast valmyndaratriði| Fylki gilda| Föst valmyndaratriði sem tengja heiti valmyndaratriðis við tengil á fasta síðu vefsvæða. Hægt er að búa til valmyndaratriði fyrir neðan önnur valmyndaratriði. Fastar valmyndir birtast sjálfkrafa á rótarstigi og þeim verður bætt við yfirlitsstigveldi rásar ef það er til staðar. |
| Sýna rótarvalmynd | **Satt** eða **Ósatt** | Þegar þessi eiginleiki er virkur er hægt að skilgreina yfirlitsvalmynd undir sérstilltri rót (til dæmis **Versla núna**). Þessi eiginleiki er fáanlegur í Dynamics 365 Commerce útgáfu 10.0.15. |
| Rótarvalmynd | strengur | Hægt er að nota þennan eiginleika til að skilgreina texta fyrir sérstillta rót ef **Sýna rótarvalmynd** eiginleikinn er stillt á **Satt**. |

Eftirfarandi mynd sýnir dæmi um tegund myndar sem birtist á yfirlitsvalmyndinni fyrir Fabrikam-svæðið.
![Dæmi um einingu yfirlitsvalmyndar með flokkamyndum.](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Bæta einingu yfirlitsvalmyndar við hauseiningu

Frekari upplýsingar um hvernig á að bæta við einingu yfirlitsvalmyndar í hauseiningu er að finna í [Hauseining](author-header-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Brauðmylsnueining](add-breadcrumb.md)

[Vefsíðuvalseining](site-selector.md)

[Kaupgluggaeining](add-buy-box.md)

[Reglufylgni köku](cookie-compliance.md)

[Eining síðuhauss](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
