---
title: Seinkanir
description: Þessi grein gefur upplýsingar um frestaðar dagsetningar á aðaláætlanagerð. Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a87b19732f413aa2844101f76dea83535da86599
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "359613"
---
# <a name="delays"></a>Seinkanir

[!include [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar um frestaðar dagsetningar á aðaláætlanagerð. Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.

Aðaláætlanagerð°getur reiknað út fyrstu mögulegu dagsetningu uppfyllingar fyrir færslu, byggða á afhendingartíma, efnisframboði, getu til ráðstöfunar og ýmsum færibreytum áætlanagerðar. 

Ef aðaláætlanagerð°reiknar pöntunardagsetningu sem kemur á undan núverandi dagsetningu er ekki hægt að uppfylla pöntunina á réttum tíma. Þess vegna seinkar pöntuninni. Í þessu tilfelli áætlar aðaláætlanagerðin pöntunina fram í tímann frá núverandi dagsetningu og hefur afhendingartíma innifaldan. Þessir afhendingartímar hefjast með allar vörur á neðri-stigs hluta. Pöntunin fær svo seinkaða dagsetningu. Frestuð dagsetning er°raunhæfur gjalddagi, samkvæmt gildandi gögnum. Aðaláætlanagerð reiknar°einnig dagafjölda seinkunar. 

Í sumum tilvikum, gætir þú valið að reikna ekki seinkun, eins og þegar notendur vita að þeir°geta hraðað afhendingartíma með því að velja annan afhendingarmáta. 

Hægt er að skilgreina hvernig seinkanir°eru reiknaðar fyrir þekjuflokk. Hægt er að tengja þekjuflokk°við vöru seinna. 

Á síðunni**Færibreytur aðaláætlanagerðar** er hægt að stilla upphafstíma fyrir útreikning°seinkana. Ef pöntun er uppfyllt að loknum tímafrestinum er einum degi°bætt við seinkunardagsetningu pöntunarinnar. 

**Ábending:** Í eldri útgáfum voru reiknaðar seinkanir kallaðar *Framvirk boð*,°seinkunardagsetning var kölluð *Framvirk dagsetning*,°og°frestuð færsla kallaðist *Færsla sem var sett í framtíðinni*.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Þekjustillingar](coverage-settings.md)



