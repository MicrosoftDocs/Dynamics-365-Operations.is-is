---
title: Stöðvun í birgðum
description: Þessi grein veitir yfirlit yfir birgðalæsingu, sem er partur af gæðaskoðunarferli í Microsoft Dynamics 365 for Finance and Operations. Hægt er að nota birgðalæsingu til að koma í veg fyrir að vörur séu unnar eða notaðar.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6291e2f012f148b247b747f84155b96cf09677
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557477"
---
# <a name="inventory-blocking"></a>Stöðvun í birgðum

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirlit yfir birgðalæsingu, sem er partur af gæðaskoðunarferli í Microsoft Dynamics 365 for Finance and Operations. Hægt er að nota birgðalæsingu til að koma í veg fyrir að vörur séu unnar eða notaðar.

Hægt er að loka vörubirgðum á eftirfarandi vegu.
-   Handvirkt
-   Með því að stofna gæðapöntun
-   Með því að nota ferlið sem myndar gæðapöntun
-   Með því að nota Birgðastöðulokun

## <a name="blocking-items-manually"></a>Læsa vörum handvirkt
Hægt er að loka á magn af vöru með því að stofna færslu í síðunni **birgðalæsing**. Aðeins er hægt að læsa vörum handvirkt sem eru í boði sem lagerbirgðir. Fyrir handvirkt læst magn verður að hugleiða hvort áætlun verkþátta innihaldi viðbúnar uppskriftir sem væntanlegt magn á lager. Áætlaðar innhreyfingar eru læstar vörur sem von er á að sé tiltækt sem birgðir á lager eftir skoðun. Hægt er að viðhalda viðbúinni dagsetningu. Að sjálfgefnu **Áætlaðar innhreyfingar** valkostur er valinn fyrir vörur sem eru læstar gegnum gæðapöntun. Hægt er að afturkalla handvirka lokun á handvirkt læstu magni með því að eyða færslu á síðunni **birgðalæsing**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Læsa vörum með því að stofna gæðapöntun
Hægt er að tilgreina vörurnar sem verða skoðaðar með því að stofna gæðapöntun á í **gæðapantanir** síðu. Þegar gæðapöntun er stofnuð er magn vöru sem tilgreint er lokað. Þegar gæðapöntun er mynduð sjálfkrafa er úrtaksáætlun vörunnar sem er tengd við gæðapöntunina stjórnar aðeins magni vara sem verður að skoða, ekki magni sem eru læst. magn vöru sem er færð inn á gæðapöntunina er magnið sem er lokað Óháð því magni sem er sent til skoðunar, eins og tilgreint er af úrtaksáætlun

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Læsa vörum með ferli sem myndar gæðapöntun
Ef gæðaferli tilgreinir að vara verður að vera skoðuð, er magn af vörunni læst sjálfkrafa. Þessvegna, Þegar gæðapöntun er mynduð sjálfkrafa er úrtaksáætlun vörunnar sem er tengd við gæðapöntunina stjórnar bæði magni vara sem eru útilokaðar og magni vara sem verður að skoða. Ef valkosturinn **full læsing** í **vöruúrtak** síðu er valinn er lokað fyrir fullt magn af til dæmis innkaupapöntunarlína við skoðun, óháð magni vörusýnishorns.
### <a name="example"></a>Dæmi

Í eftirfarandi dæmi er gæðapöntun mynduð þegar fylgiseðill innkaupapöntunar er bókaður. Í á **gæðatengingar** síðunni, tilgreindirðu að bókun fylgiseðils innkaupapöntunar er ferlið sem virkjar gæðapöntun.

|Uppsetning                                                                     |Aðgerðir notanda                 |Niðurstaða             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Gæðatenging tilgreinir að við bókun fylgiseðils innkaupapöntunar þarf að mynda gæðapöntun. Uppsetning vörusýna gæðapöntunar tilgreinir að 10% af magn í innkaupapöntunarlínu verða að vera skoðaðar. Enn fremur, afþví **full læsing** valkosturinn er valinn sýnir sýnishorn vörunnar að allt magnið í innkaupapöntunarlínunni verður að vera læst við skoðun óháð því magni sem er sent til skoðunar. | Fylgiseðillinn er bókaður. | Gæðapöntun er mynduð. Tíu prósent af magni innkaupapöntunar af hlutnum er sendur til skoðunar. Heildarmagn á innkaupapöntunarlínunni er lokað. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Læsa vörum Með því að nota Birgðastöðulokun
Hægt er að tilgreina hvaða birgðastöður eru lokunarstöður með því að nota **birgðalæsingu** færibreytur á í **Birgða stöður** síðu. Þú getur ekki notað birgðastöðu sem lokunar stöður fyrir framleiðslupantanir, sölupantanir, flutningspantanir, færslur á útleið eða samþættingar verks. Notið vörur með stöðu tiltækar birgðir fyrir vinnu á útleið. Ef vörur með stöðuna **slitin** og aðaláætlanagerð er keyrð fyrir þessar vörur, er litið á þessar vörur þannig að þær vanti og birgðir eru endurnýjaðar sjálfkrafa.



<a name="additional-resources"></a>Frekari upplýsingar
--------

[Stofna og viðhalda á birgðalokun](tasks/create-maintain-inventory-blocking.md)

[Gæðastjórnunarferli](quality-management-processes.md)

[Skoða gæði vara (verkefnaleiðbeiningar)](tasks/inspect-quality-goods.md)
