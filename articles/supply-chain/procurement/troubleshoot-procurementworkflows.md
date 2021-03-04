---
title: Villuleita verkflæði innkaupa og aðfanga
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með verkflæði innkaupa og aðfanga.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430759"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Villuleita verkflæði innkaupa og aðfanga

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með verkflæði innkaupa og aðfanga.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Villa þegar innkaupapöntun er endursend í verkflæðið eftir breytingu: „Breytingar á innkaupapöntun X eru aðeins leyfðar í stöðunni Drög þegar breytingastjórnun er virkjuð“

Þetta vandamál á sér aðeins stað ef innkaupapöntunin var með stöðuna *Staðfest* áður en óskað var eftir breytingum. Ef beðið er um breytingar á meðan innkaupapöntunin er með stöðuna *Samþykkt*, er hægt að vinna úr verkflæðinu.

### <a name="error-description"></a>Villulýsing

Eftirfarandi villa kemur upp í verkflæðinu þegar innkaupapöntun er send aftur eftir breytingu:

> Stöðvað (villa): X++ undantekning: Breytingar á innkaupapöntun PO0000569 eru aðeins leyfðar í stöðunni „Drög“ þegar breytingastjórnun er virkjuð á<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.

Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Vandamálið verður lagað í [þessari grein Microsoft Knowledge](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Ein eða fleiri dreifingar á fjárhagsupphæð eru annaðhvort yfir- eða undirdreifðar.

Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.

Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Ef hætt er við eftirstöðvar afhendingar í innkaupapöntun þar sem kveikt er á breytingastjórnun, fer innkaupapöntunin í stöðuna Staðfest.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Fyrir innkaupapöntun sem heyrir undir breytingastjórnun, ef eina breytingin sem beðið er um er afturköllun á eftirstöðvum afhendingar á einni eða fleiri línum, fer innkaupapöntunin beint í stöðuna *Staðfest* þegar hún er samþykkt og engin færslubók verður stofnuð.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Afturköllun á eftirstöðvum afhendingar hefur ekki áhrif á innihald staðfestingarbókar. Nota ætti þessa virkni þegar búið er að taka á móti línunni að hluta til og hætta ætti við eftirstandandi magn í vinnsluskrefinu eftir að innkaupapöntunin hefur verið staðfest hjá lánardrottni.

Ef þetta á að koma fram á staðfestingu innkaupapöntunarinnar ætti að leiðrétta magnið í innkaupapöntunarlínunni svo staðfestingin verði nauðsynleg. Að öðrum kosti, ef ekkert hefur verið móttekið í línunni, er hægt að fjarlægja magnið. Í þessu tilfelli þarf að staðfesta aftur.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Afturkallaðar innkaupapantanir birtast í listanum yfir drög á undirbúningssvæði innkaupapöntunar.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar búið er að hætta við innkaupapantanir sem voru með stöðuna *Staðfest*, sjást afturkölluðu innkaupapantanir ennþá í listanum yfir drög að innkaupapöntunum á vinnusvæðinu **Undirbúningur innkaupapöntunar**.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þetta vandamál á sér aðeins stað fyrir innkaupapantanir sem heyra undir breytingastjórnun. Það á sér stað vegna þess að afturköllunin er talin breyta sem þarf að samþykkja. Hægt er að framkvæma samþykkið sjálfkrafa af kerfinu. Þess vegna gengur ferlið út á að senda afturkallaða innkaupapöntun til samþykktarverkflæðis þannig að hún geti fengið stöðuna *Samþykkt*. Á þessu stigi sést innkaupapöntunin ekki lengur í listanum yfir drög að innkaupapöntunum á vinnusvæðinu **Undirbúningur innkaupapöntunar**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]