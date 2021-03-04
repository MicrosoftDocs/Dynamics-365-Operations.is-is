---
title: Runueigindir
description: Þetta efnisatriði gefur upplýsingar um runueigindir. Runueigindi eru einkenni hráefnis og fullunninna afurða sem birgðakeyrslur samanstanda af. Þetta efnisatriði útskýrir einnig hvernig á að úthluta runueigindum, og hvernig hægt er að leita í þeim þegar runur eru teknar frá.
author: ShylaThompson
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370893e415a79091404f1c4eb0404ba8fd5b9ff2
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430683"
---
# <a name="batch-attributes"></a>Runueigindir

[!include [banner](../includes/banner.md)]

Þetta efnisatriði gefur upplýsingar um runueigindir. Runueigindi eru einkenni hráefnis og fullunninna afurða sem birgðakeyrslur samanstanda af. Þetta efnisatriði útskýrir einnig hvernig á að úthluta runueigindum, og hvernig hægt er að leita í þeim þegar runur eru teknar frá.

Runueigindi eru einkenni hráefnis og fullunninna afurða sem birgðakeyrslur samanstanda af. Runueigindir geta verið mismunandi, eftir þáttum eins og umhverfisþáttum, gæðum hráefna sem eru notuð til að framleiða rununa eða niðurstöðu endanlegrar afurðar. Númer og gerðir runueiginda sem eru notaðar geta verið afar mismunandi frá einni atvinnugrein til annarrar. Hér eru tvö dæmi sem sýna hvernig á að nota runueigindir:

-   Á sviði ostagerðar getur mjólk, sem er eitt af þeim hráefnum sem eru notuð til að framleiða ost, haft eigindirnar eins og fituinnihald og prósentuþyngd. Ostur sem er framleiddur úr mjólk getur haft aðrar eiginleika, eins og rakastig og aldur.
-   Í stáliðnaðinum getur járn sem er framleitt gæti hafa eigindir eins og prósentur magnesíuminnihalds, silfurinnihalds og sinkinnihalds.

Til að stjórna númer og gerðir eiginda, er hægt að nota runueigindaflokkar. Á þennan hátt þarf ekki að bæta hverri eigind sérstaklega við.

## <a name="assign-batch-attributes"></a>Úthluta runueigindum
Hægt er að úthluta runueigindum á stakar afurðir sem eru í birgðarunum, eða hægt er að úthluta þeim á afurðir sem tengjast ákveðnum viðskiptavinum. Áður en hægt er að úthluta runueigind á stigi viðskiptavinar verður að úthluta henni á stigi afurðar. Afurðin verður að hafa runuvíddina stillta á **Virka** í rakningarvíddarflokknum. Til að úthluta runueigind á staka vöru skal nota afurðabundna síðu. Ef eigindin er bundin við afurð fyrir viðskiptavin skal nota síðu tiltekins viðskiptavinar. Þegar eigind er bætt við vöru þarf einnig að skilgreina aðrar færibreytur. Hér eru nokkur dæmi:

-   Færið inn lágmarksgildi á bilinu fyrir eigindagerðirnar **Heiltala** eða **Brot**.
-   Vikmarkaaðgerðir fyrir eigindagerðirnar **Heiltala** eða **Brot**. Ef gildi eigindarinnar er utan marka lágmarks- og hámarksbils getur aðgerðin verið annaðhvort viðvörun eða villuboð.
-   Markgildi fyrir eigindina. Þetta gildi er kjörgildi eigindarinnar og það á við um allar gerðir eiginda.

Hægt er að opna síður fyrir afurðir sem eru valdar á síðunni **Útgefnar afurðir** í afurðastjórnun upplýsingar. Eftir runueigindum er úthlutað á afurð er hægt að bæta tilteknu gildi við eigindir á síðunni **Birgðarunueigindir**.

## <a name="reserve-batches"></a>Taka frá runur
Hægt er að leita í runueigindum þegar gerðar eru runufrátekningar fyrir sölupöntun til að framfylgja pöntun viðskiptavinar, eða þegar runur eru tíndar og teknar frá fyrir framleiðslupöntun. Leitin hjálpar til við að staðsetja birgðarunu sem inniheldur afurðina sem hefur þá runueigind sem óskað er. Þegar búið er að finna runu eða runur er hægt að taka frá afurð fyrir upphaflega færslulínu birgða.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]