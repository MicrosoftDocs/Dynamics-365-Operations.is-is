---
title: Seinkanir
description: Þetta efnisatriði veitir upplýsingar um seinkanir á dagsetningum í aðaláætlanagerð. Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
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
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/20/2019
ms.locfileid: "878311"
---
# <a name="delays"></a>Seinkanir

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um seinkanir á dagsetningum í aðaláætlanagerð. Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.

Aðaláætlanagerð°getur reiknað út fyrstu mögulegu dagsetningu uppfyllingar fyrir færslu, byggða á afhendingartíma, efnisframboði, getu til ráðstöfunar og ýmsum færibreytum áætlanagerðar. 

Ef aðaláætlanagerð°reiknar pöntunardagsetningu sem kemur á undan núverandi dagsetningu er ekki hægt að uppfylla pöntunina á réttum tíma. Þess vegna seinkar pöntuninni. Í þessu tilfelli áætlar aðaláætlanagerðin pöntunina fram í tímann frá núverandi dagsetningu og hefur afhendingartíma innifaldan. Þessir afhendingartímar hefjast með allar vörur á neðri-stigs hluta. Pöntunin fær svo seinkaða dagsetningu. Frestuð dagsetning er°raunhæfur gjalddagi, samkvæmt gildandi gögnum. Aðaláætlanagerð reiknar°einnig dagafjölda seinkunar. 

Í sumum tilvikum, gætir þú valið að reikna ekki seinkun, eins og þegar notendur vita að þeir°geta hraðað afhendingartíma með því að velja annan afhendingarmáta. 

Hægt er að skilgreina hvernig seinkanir°eru reiknaðar fyrir þekjuflokk. Hægt er að tengja þekjuflokk°við vöru seinna. 

Á síðunni**Færibreytur aðaláætlanagerðar** er hægt að stilla upphafstíma fyrir útreikning°seinkana. Ef pöntun er uppfyllt að loknum tímafrestinum er einum degi°bætt við seinkunardagsetningu pöntunarinnar. 

> [!ÁBENDING} Í eldri útgáfum voru reiknaðar seinkanir kallaðar *Framvirk boð*, seinkunardagsetning var kölluð *Framvirk dagsetning* og frestuð færsla kallaðist *Færsla sem var sett í framtíðinni*.

## <a name="desired-date"></a>Æskileg dagsetning

Á síðunni **Áætluð pöntun**, undir flipanum **Seinkanir**, er **Æskileg dagsetning** fyrir áætlaða pöntun. Æskileg dagsetning fyrir áætlaða pöntun er grunndagsetning fyrir seinkanir sem er reiknuð dagsetning sem jafngildir **Umbeðinni dagsetningu** sem er reiknuð út frá **Nettóþörf**. Ef áætluð pöntun er uppskriftarlína, framleiðslulína eða kanban-lína, er æskileg dagsetning byggð á **Dagsetning þarfa** og æskileg dagsetning birtist ekki á síðunni **Áætluð pöntun**.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Þekjustillingar](coverage-settings.md)
