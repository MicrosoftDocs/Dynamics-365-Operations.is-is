---
title: Samþykkja tillögur
description: Þetta efnisatriði lýsir samþykki áætlaðra pantana sem eru studdar í Fínstillingu skipulagningar.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430306"
---
# <a name="approve-planned-orders"></a>Samþykkja tillögur

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði eru veittar upplýsingar um hvernig uppfæra eigi stöðu áætlaðra pantana í Fínstillingu skipulagningar.

Athugið að samþykki á áætluðum pöntunum er valfrjálst skref, og er eitt skref í því að stofna staðfesta pöntun úr áætlaðri pöntun. Mælt er með því að samþykkja breyttar áætlaðar pantanir, annars verða breytingarnar hunsaðar og yfirskrifaðar af næstu áætlunarkeyrslu.

![Áætlað pöntunarflæði](media/approved-planned-orders-1.png)

Reiturinn **Staða** hjálpar til við að fylgjast með framvindu með eftirfarandi gildum:

- **Óunnið:** Þegar aðaláætlunargerð myndar áætlaðar pantanir, hafa áætlaðar pantanir stöðuna *Óunnið*. Áætluðum pöntunum með þessa stöðu verður eytt við næstu áætlunarkeyrslu.
- **Lokið:** Ef þú ákveður að staðfesta ekki áætlaða pöntun geturðu breytt stöðunni í *Lokið* til að gefa til kynna að þú hafir lokið við að meta þessa áætluðu pöntun. Athugið að stöðurnar *Ómeðhöndlað* og *Lokið* er meðhöndlaðar eins af kerfinu.
- **Samþykkt:** Ef þú vilt halda breytingum eða ætlar að staðfesta áætlaða pöntun skaltu breyta stöðunni í *Samþykkt*. Áætlaðar pantanir með stöðuna *Samþykkt* eru hugsaðar sem fastar og eru áætlaðar fyrir aðaláætlanagerð, þannig að þeim er ekki breytt eða þeim eytt í síðari aðaláætlunarkeyrslum. Til að ná þessu afritar áætlunargrunnurinn *Samþykktar* áætlaðar pantanir úr gömlu áætlunarútgáfunni yfir í nýju áætlunarútgáfuna við aðalskipulagningu. Athugið að *Samþykktar* áætlaðar pantanir eru aðeins hugsaðar sem framboð innan tiltekinnar aðaláætlunar.

Hægt er að stjórna áætluðum pöntunum úr vinnusvæðinu **Aðaláætlanagerð**, úr listanum **Áætluð pöntun** eða listunum **Áætlaðar framleiðslupantanir**, **Áætlaðar innkaupapantanir**, og **Flutningsáætlanir**.
