---
title: Ábendingar fyrir sýnileika birgða
description: Þetta efni gefur nokkrar ábendingar sem þú ættir að hafa í huga þegar þú setur upp og notar birgðasýnileikaviðbótina.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1f6ade36ac184a3c8bf790fc0d899ea01d90c8d2
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952416"
---
# <a name="inventory-visibility-tips"></a>Ábendingar fyrir sýnileika birgða

[!include [banner](../includes/banner.md)]

Hér eru nokkur ráð sem þú ættir að hafa í huga þegar þú setur upp og notar birgðasýnileikaviðbótina:

- Eins og er styður Inventory Visibility Add-in aðeins Microsoft Dataverse umhverfi sem var búið til með því að nota Microsoft Dynamics Lífsferilsþjónusta (LCS). Ef þín Dataverse umhverfi var búið til á annan hátt (til dæmis með því að nota Power Apps admin center), og ef það er tengt við þinn Dynamics 365 Supply Chain Management umhverfi, verður þú fyrst að biðja vöruteymi birgðasýnileika að laga kortlagningarvandann. Hægt er að hafa samband við teymið á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Teymið mun láta þig vita þegar umhverfið þitt er tilbúið fyrir þig til að setja upp Birgðasýnileika.
- Ef þú ert með fleiri en eitt LCS umhverfi skaltu búa til annað Azure Active Directory (Azure AD) umsókn fyrir hvert umhverfi. Ef þú notar sama forritskennið og leigjandakennið til að setja upp innbót birgðasýnileika fyrir mismunandi umhverfi mun koma upp vandamál varðandi lykla fyrir eldri umhverfi. Aðeins síðasta tilvikið af Inventory Visibility Add-in sem var sett upp mun gilda.
- Birgðasýnileiki er ekki stutt fyrir umhverfi sem hýst er í skýi. Það er aðeins stutt fyrir Tier-2+ umhverfi.
- Forritunarviðmótið (API) styður sem stendur fyrirspurnir um allt að 100 einstök atriði eftir`ProductID` gildi. Margfeldi`SiteID` og`LocationID` Einnig er hægt að tilgreina gildi í hverri fyrirspurn. Hámarksmörk eru skilgreind sem `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Magn API getur skilað að hámarki 512 færslum fyrir hverja beiðni.
- The`fno` gagnauppspretta er frátekin fyrir Supply Chain Management. Ef birgðasýnileikaviðbótin þín er samþætt við Supply Chain Management umhverfi mælum við með að þú eyðir ekki stillingum sem tengjast`fno` í [gagnagjafa](inventory-visibility-configuration.md#data-source-configuration).
- Birgðasýnileiki getur ekki breytt neinum gögnum fyrir`fno` gagnagjafa. Gagnaflæðið er einstefnu, sem þýðir að allt magn breytist fyrir`fno` gagnagjafi verður að koma frá Supply Chain Management umhverfi þínu. Þess vegna geturðu ekki notað API til að senda breytinga- eða pöntunarbeiðnir fyrir hendi fyrir`fno` gagnagjafa.
- Ef þú bætir einni eða fleiri nýjum ráðstöfunum við aðfangakeðjustjórnun umhverfið þitt, ættirðu einnig að bæta þeim við í Birgðasýnileika. Hins vegar verða allar magnbreytingar fyrir nýjar ráðstafanir að koma frá Supply Chain Management umhverfi þínu.
- The [stillingar skiptingarinnar](inventory-visibility-configuration.md#partition-configuration) samanstendur nú af tveimur grunnvíddum (`SiteId` og`LocationId`) sem gefa til kynna hvernig gögnunum er dreift. Aðgerðir undir sama skipting geta skilað meiri afköstum með lægri kostnaði. Lausnin inniheldur þessa skiptingastillingu sjálfgefið. Þess vegna, *þú þarft ekki að skilgreina það sjálfur*. Ekki sérsníða sjálfgefna skiptinguna. Ef þú eyðir því eða breytir því er líklegt að þú valdi óvæntri villu.
- Grunnvíddir sem eru skilgreindar í skiptingarstillingunni ættu ekki að vera skilgreindar í [uppsetningu vöruvísitölu stigveldis](inventory-visibility-configuration.md#index-configuration).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
