---
title: Ábendingar fyrir Inventory Visibility
description: 'Í þessari grein eru nokkrar ábendingar sem þú ættir að hafa í huga þegar þú setur upp og notar Inventory Visibility viðbótina:'
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306086"
---
# <a name="inventory-visibility-tips"></a>Ábendingar fyrir Inventory Visibility

[!include [banner](../includes/banner.md)]

Hér eru nokkrar ábendingar sem þú ættir að hafa í huga þegar þú setur upp og notar Inventory Visibility viðbótina:

- Eins og er styður innbót birgðasýnileika aðeins Microsoft Dataverse umhverfi sem voru búin til með því að nota Microsoft Dynamics Lifecycle Services (LCS). Ef Dataverse umhverfið þitt var búið til á einhvern annan hátt (til dæmis með því að nota Power Apps stjórnendamiðstöðina) og ef það er tengt við umhverfi Dynamics 365 Supply Chain Management verður þú fyrst að hafa samband við vöruteymi birgðasýnileika til að leysa úr vandamáli vörpunar. Þú getur haft samband við teymið á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Teymið lætur þig vita þegar umhverfi þitt er tilbúið til að setja upp sýnileika birgða.
- Ef þú ert með fleiri en eitt LCS-umhverfi skaltu búa til annað Azure Active Directory (Azure AD) forrit fyrir hvert umhverfi. Ef þú notar sama forritskennið og leigjandakennið til að setja upp innbót birgðasýnileika fyrir mismunandi umhverfi mun koma upp vandamál varðandi lykla fyrir eldri umhverfi. Aðeins síðasta tilvik innbótar birgðasýnileika sem var sett upp verður gilt.
- Sýnileiki birgða er ekki studdur fyrir umhverfi sem er hýst í skýi eins og er. Þetta er aðeins stutt fyrir Tier-2+ umhverfi.
- Forritunarviðmótið (API) styður að spyrjast fyrir um allt að 100 stakar vörur eftir `ProductID` gildi. Einnig er hægt að tilgreina mörg `SiteID` og `LocationID` gildi í hverri fyrirspurn. Hámarkið er skilgreint sem `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Fjölforritaskilin getur skilað að hámarki 512 skrám fyrir hverja beiðni.
- Gagnagjafinn `fno` er frátekinn fyrir Supply Chain Management. Ef innbót birgðasýnileika er samþætt við umhverfi Supply Chain Management er mælt með því að eyða ekki skilgreiningum sem tengjast `fno` í [gagnagjafanum](inventory-visibility-configuration.md#data-source-configuration).
- Birgðasýnileiki getur ekki breytt neinum gögnum fyrir `fno` gagnagjafann. Gagnaflæðið er einstefna sem þýðir að allar magnbreytingar fyrir gagnaveituna verða `fno` að koma úr Supply Chain Management umhverfi þínu. Þar af leiðandi getur þú ekki notað API til að senda lagerbreytingar eða bókunarbeiðnir fyrir `fno` gagnagjafann.
- Ef þú bætir einni eða fleiri nýjum ráðstöfunum við Supply Chain Management ættir þú einnig að bæta þeim við sýnileika birgða. Hins vegar verða allar magnbreytingar fyrir nýjar mælingar að koma frá þínu Supply Chain Management umhverfi.
- [Skilgreining skiptingar](inventory-visibility-configuration.md#partition-configuration) samanstendur af tveimur grunnvíddum (`SiteId` og `LocationId`) sem gefa til kynna hvernig gögnunum er dreift. Rekstur undir sama deiliskipulagi getur skilað meiri árangri með minni tilkostnaði. Lausnin inniheldur sjálfgefið þessa skilgreiningu skiptingar. Þú *þarft því ekki að skilgreina það sjálf(ur)*. Ekki sérsníða sjálfgefna deildaskiptingu. Ef þú eyðir henni eða breytir henni er líklegt að óvænt villa komi upp.
- Grunnvíddir sem eru skilgreindar í skilgreiningu skiptingar eiga ekki að vera skilgreindar í [skilgreiningu á stigveldi vöruskráningar](inventory-visibility-configuration.md#index-configuration).
- [Skilgreining á stigveldi vöruskráningar](inventory-visibility-configuration.md#index-configuration) verður að innihalda að minnsta kosti eina stigveldisskráningu (til dæmis sem inniheldur grunnvíddina `Empty`), annars munu fyrirspurnir mistakast með villunni „Ekkert stigveldi atriðaskráningar hefur verið stillt.“
- Gagnagjafinn `@iv` er fyrirfram skilgreindur gagnagjafi og efnislegar mælingar skilgreindar í `@iv` með forskeytinu `@` eru fyrirfram skilgreindar mælingar. Þessar mælingar eru fyrirfram skilgreindar stillingar fyrir úthlutunareiginleikann, því skal ekki breyta eða eyða þeim. Annars er líklegt að óvæntar villur komi upp þegar úthlutunareiginleikinn er notaður.
- Hægt er að bæta nýjum efnislegum mælingum við fyrirfram skilgreinda reiknaða mælingu `@iv.@available_to_allocate`, en ekki má breyta heiti hennar.
- Ef þú endurheimtir gagnagrunn Supply Chain Management þá gæti endurheimtur gagnagrunnur innihaldið gögn sem eru ekki lengur í samræmi við gögn sem voru áður samstillt af birgðasýnileika í Dataverse. Þetta ósamræmi gagna getur valdið kerfisvillum og öðrum vandamálum. Því er mikilvægt að þú hreinsir alltaf öll tengd gögn birgðasýnileika frá Dataverse áður en þú endurheimtir gagnagrunn Supply Chain Management. Frekari upplýsingar er að finna í [Hreinsa gögn birgðasýnileika úr Dataverse áður en gagnagrunnur Supply Chain Management er endurheimtur](inventory-visibility-setup.md#restore-environment-database).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
