---
title: Seinkanir
description: Þessi grein gefur upplýsingar um frestaðar dagsetningar á aðaláætlanagerð. Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.
author: t-benebo
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bda8d9fcf42727a1ef530dee5f58dbaf18d5022
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882548"
---
# <a name="delays"></a>Seinkanir

[!include [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar um frestaðar dagsetningar á aðaláætlanagerð. Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.

Aðaláætlanagerð°getur reiknað út fyrstu mögulegu dagsetningu uppfyllingar fyrir færslu, byggða á afhendingartíma, efnisframboði, getu til ráðstöfunar og ýmsum færibreytum áætlanagerðar. 

Ef aðaláætlanagerð°reiknar pöntunardagsetningu sem kemur á undan núverandi dagsetningu er ekki hægt að uppfylla pöntunina á réttum tíma. Þess vegna seinkar pöntuninni. Í þessu tilfelli áætlar aðaláætlanagerðin pöntunina fram í tímann frá núverandi dagsetningu og hefur afhendingartíma innifaldan. Þessir afhendingartímar hefjast með allar vörur á neðri-stigs hluta. Pöntunin fær svo seinkaða dagsetningu. Frestuð dagsetning er°raunhæfur gjalddagi, samkvæmt gildandi gögnum. Aðaláætlanagerð reiknar°einnig dagafjölda seinkunar. 

Í sumum tilvikum, gætir þú valið að reikna ekki seinkun, eins og þegar notendur vita að þeir°geta hraðað afhendingartíma með því að velja annan afhendingarmáta. 

Hægt er að skilgreina hvernig seinkanir°eru reiknaðar fyrir þekjuflokk. Hægt er að tengja þekjuflokk°við vöru seinna. 

Á síðunni **Færibreytur aðaláætlanagerðar** er hægt að stilla upphafstíma fyrir útreikning á seinkunum. Ef pöntun er uppfyllt að loknum tímafrestinum er einum degi°bætt við seinkunardagsetningu pöntunarinnar. 

> [!NOTE]
> Í eldri útgáfum voru útreiknaðar seinkanir kallaðar *Framvirk boð*, seinkunardagsetning var kölluð *Framvirk dagsetning* og frestuð færsla kallaðist *Færsla sem var sett í framtíðinni*.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Takmarkaðar tafir á framleiðsluuppsetningunni með mörgum BOM-stigum
Þegar þú vinnur með tafir í framleiðsluuppsetningunni sem hefur mörg BOM stig, er mikilvægt að hafa í huga að aðeins vörurnar beint fyrir ofan vöruna (í BOM-skipulagingunni) sem valda seinkuninni, verða uppfærðar með töf sem hluti af keyrslu aðaláætlunar. Töfum verður ekki beitt á aðrar vörur í BOM-skipulaginu fyrr en í fyrstu keyrslu aðaláætlunar, þegar fyrirhuguð pöntun fyrir efsta stigið er samþykkt eða styrkt. 

Til að vinna í kringum þessa þekktu takmörkun er hægt að samþykkja (eða stýra) framleiðslupöntunum efst í BOM-skipulaginu með seinkunum áður en næsta aðaláætlunargerð er keyrð. Þannig verður seinkun frá seinkaðri fyrirhugaðri framleiðslupöntun haldið og allir undirliggjandi íhlutir uppfærðir til samræmis.
Aðgerðaskilaboð er einnig hægt að nota til að bera kennsl á fyrirhugaðar pantanir sem hægt er að færa á síðari dagsetningu, vegna annarra tafa á BOM-skipulagi.

## <a name="desired-date"></a>Æskileg dagsetning

Á síðunni **Áætluð pöntun**, undir flipanum **Seinkanir**, er **Æskileg dagsetning** fyrir áætlaða pöntun. Æskileg dagsetning fyrir áætlaða pöntun er grunndagsetning fyrir seinkanir sem er reiknuð dagsetning sem jafngildir **Umbeðinni dagsetningu** sem er reiknuð út frá **Nettóþörf**. Ef áætluð pöntun er uppskriftarlína, framleiðslulína eða kanban-lína, er æskileg dagsetning byggð á **Dagsetning þarfa** og æskileg dagsetning birtist ekki á síðunni **Áætluð pöntun**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Þekjustillingar](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]