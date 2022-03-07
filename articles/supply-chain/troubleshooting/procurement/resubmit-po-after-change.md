---
title: Villa við endursendingu innkaupapöntunar í verkflæði eftir breytingu
description: Villa við endursendingu innkaupapöntunar í verkflæði eftir breytingu
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476707"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Villa við endursendingu innkaupapöntunar í verkflæði eftir breytingu


## <a name="symptoms"></a>Einkenni

Eftirfarandi villa kemur upp í verkflæðinu þegar innkaupapöntun er send aftur eftir breytingu:

> Stöðvað (villa): X++ undantekning: Breytingar á innkaupapöntun PO0000569 eru aðeins leyfðar í stöðunni „Drög“ þegar breytingastjórnun er virkjuð á<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Þetta vandamál á sér aðeins stað ef innkaupapöntunin var með stöðuna *Staðfest* áður en óskað var eftir breytingum. Ef beðið er um breytingar á meðan innkaupapöntunin er með stöðuna *Samþykkt*, er hægt að vinna úr verkflæðinu.

## <a name="resolution"></a>Lausn

Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.

Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Vandamálið verður lagað í [þessari grein Microsoft Knowledge](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).
