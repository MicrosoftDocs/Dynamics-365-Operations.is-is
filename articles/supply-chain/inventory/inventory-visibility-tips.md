---
title: Ábendingar fyrir sýnileika birgða
description: Þessi grein veitir nokkur ráð sem þú ættir að hafa í huga þegar þú setur upp og notar birgðasýnileikaviðbótina.
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
ms.openlocfilehash: 3bdd161815a15d5c39b3c0afc176a288c8d9055a
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306086"
---
# <a name="inventory-visibility-tips"></a>Ábendingar fyrir sýnileika birgða

[!include [banner](../includes/banner.md)]

Hér eru nokkur ráð sem þú ættir að hafa í huga þegar þú setur upp og notar birgðasýnileikaviðbótina:

- Sem stendur styður Inventory Visibility Add-in aðeins Microsoft Dataverse umhverfi sem var búið til með því að nota Microsoft Dynamics Lífsferilsþjónusta (LCS). Ef þín Dataverse umhverfi var búið til á annan hátt (til dæmis með því að nota Power Apps admin center), og ef það er tengt við þinn Dynamics 365 Supply Chain Management umhverfi, verður þú fyrst að biðja vöruteymi birgðasýnileika um að laga kortlagningarvandann. Hægt er að hafa samband við teymið á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Teymið mun láta þig vita þegar umhverfið þitt er tilbúið fyrir þig til að setja upp Birgðasýnileika.
- Ef þú ert með fleiri en eitt LCS umhverfi skaltu búa til annað Azure Active Directory (Azure AD) umsókn fyrir hvert umhverfi. Ef þú notar sama forritskennið og leigjandakennið til að setja upp innbót birgðasýnileika fyrir mismunandi umhverfi mun koma upp vandamál varðandi lykla fyrir eldri umhverfi. Aðeins síðasta tilvik birgðasýnileikaviðbótarinnar sem var sett upp mun gilda.
- Birgðasýnileiki er ekki stutt fyrir umhverfi sem hýst er í skýi. Það er aðeins stutt fyrir Tier-2+ umhverfi.
- Forritunarviðmótið (API) styður sem stendur fyrirspurnir um allt að 100 einstök atriði eftir`ProductID` gildi. Margfeldi`SiteID` og`LocationID` Einnig er hægt að tilgreina gildi í hverri fyrirspurn. Hámarksmörk eru skilgreind sem `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Magn API getur skilað að hámarki 512 færslum fyrir hverja beiðni.
- The`fno` gagnagjafinn er frátekinn fyrir Supply Chain Management. Ef birgðasýnileikaviðbótin þín er samþætt við Supply Chain Management umhverfi mælum við með að þú eyðir ekki stillingum sem tengjast`fno` í [gagnagjafa](inventory-visibility-configuration.md#data-source-configuration).
- Birgðasýnileiki getur ekki breytt neinum gögnum fyrir`fno` gagnagjafa. Gagnaflæðið er einstefnu, sem þýðir að allt magn breytist fyrir`fno` gagnagjafi verður að koma frá Supply Chain Management umhverfi þínu. Þess vegna geturðu ekki notað API til að senda breytinga- eða pöntunarbeiðnir fyrir hendi fyrir`fno` gagnagjafa.
- Ef þú bætir einni eða fleiri nýjum ráðstöfunum við Supply Chain Management umhverfið þitt, ættir þú einnig að bæta þeim við í Birgðasýnileika. Hins vegar verða allar magnbreytingar fyrir nýjar ráðstafanir að koma frá Supply Chain Management umhverfi þínu.
- The [stillingar skiptingarinnar](inventory-visibility-configuration.md#partition-configuration) samanstendur nú af tveimur grunnvíddum (`SiteId` og`LocationId`) sem gefa til kynna hvernig gögnunum er dreift. Aðgerðir undir sama skipting geta skilað meiri afköstum með lægri kostnaði. Lausnin inniheldur þessa skiptingarstillingu sjálfgefið. Þess vegna, *þú þarft ekki að skilgreina það sjálfur*. Ekki sérsníða sjálfgefna skiptinguna. Ef þú eyðir því eða breytir því er líklegt að þú valdi óvæntri villu.
- Grunnvíddir sem eru skilgreindar í skiptingarstillingunni ættu ekki að vera skilgreindar í [uppsetningu vöruvísitölu stigveldis](inventory-visibility-configuration.md#index-configuration).
- Þinn [uppsetningu vöruvísitölu stigveldis](inventory-visibility-configuration.md#index-configuration) verður að innihalda að minnsta kosti eitt vísitölustigveldi (til dæmis sem inniheldur grunnvíddina`Empty`), annars mistakast fyrirspurnir með villunni "Ekkert vísitölustigveldi hefur verið stillt."
- Uppruni gagna`@iv` er fyrirfram skilgreindur gagnagjafi og líkamlegar mælingar skilgreindar í`@iv` með forskeyti`@` eru fyrirfram skilgreindar ráðstafanir. Þessar ráðstafanir eru fyrirfram skilgreindar stillingar fyrir úthlutunareiginleikann, svo ekki breyta eða eyða þeim eða þú ert líklegri til að lenda í óvæntum villum þegar þú notar úthlutunareiginleikann.
- Þú getur bætt nýjum líkamlegum mælingum við fyrirfram skilgreinda reiknaða mælingu`@iv.@available_to_allocate`, en þú mátt ekki breyta nafni þess.
- Ef þú endurheimtir Supply Chain Management gagnagrunn, þá gæti endurheimti gagnagrunnurinn þinn innihaldið gögn sem eru ekki lengur í samræmi við gögn sem áður voru samstillt af Birgðasýnileika við Dataverse. Þetta ósamræmi í gögnum getur valdið kerfisvillum og öðrum vandamálum. Þess vegna er mikilvægt að þú hreinsar alltaf öll tengd birgðasýnileikagögn úr Dataverse áður en þú endurheimtir Supply Chain Management gagnagrunn. Sjá nánar [Hreinsaðu birgðasýnileikagögn frá Dataverse áður en þú endurheimtir Supply Chain Management gagnagrunninn](inventory-visibility-setup.md#restore-environment-database).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
