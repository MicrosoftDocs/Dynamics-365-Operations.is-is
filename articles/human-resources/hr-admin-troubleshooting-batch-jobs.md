---
title: Bæta frammistöðu með því að tímasetja runuvinnslur utan vinnutíma
description: Þetta efnisatriði útskýrir hvernig á að leysa úr vandamálum sem tengjast afköstum með Microsoft Dynamics 365 Human Resources með því að tímasetja langtímarunuvinnslu eftir vinnutíma.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 13482ab7b9ee6303138a7a5e82dce78138e0b8ed
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357314"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Bæta frammistöðu með því að tímasetja runuvinnslur utan vinnutíma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Úthreyfing

Vandamál með afköst geta komið upp hjá Microsoft Dynamics 365 Human Resources ef langtímarunuvinnsla er keyrð á vinnutíma.

## <a name="resolution"></a>Upplausn

Tímasetjið eftirfarandi runuvinnslur utan vinnutíma. Einnig er mælt með því að endurskoða tíðni runuvinnsla sem keyra oft. Dragið úr endurtekningum á runuvinnslunni ef mögulegt. Í mörgum tilfellum er sjálfgefin tíðni nægjanleg.

Eftirfarandi runuvinnslur ættu að keyra að næturlagi eða eftir vinnutíma. Gætið þess að athuga tímabeltið fyrir þessar endurteknar runuvinnslur. Sumar runuvinnslur nota hugsanlega PST staðaltíma.

| Runuvinnsla | Sjálfgefin endurtekning |
| --- | --- |
| Hreinsun runuvinnsluferils | 1 skipti á mánuði |
| Flytja út hreinsun sviðsetningar | 1 skipti á dag |
| Samstilling ósvaraðra beiðna Common Data Service-samþættingar | 1 skipti á dag |
| Kerfisvinnsla gagnasamþjöppunar sem þarf að keyra reglulega utan vinnutíma | 1 skipti á dag |
| Kerfisvinnsla endurbyggingar gagnagrunnsvísa sem þarf að keyra reglulega utan vinnutíma | 1 skipti á dag |

1. Veldu í Human Resources **Kerfisstjórnun**.

2. Í stikunni **Leita** skal leita að einni af ofangreindum runuvinnslum.

3. Veljið **Keyra í bakgrunni** og veljið síðan **Endurtekning**.

   ![Stilltu endurtekningu.](media/talent-batch-history-cleanup-recurrence.png)

4. Undir **Skilgreina endurtekningu** skal stilla **Upphafsdagsetningu** og **Upphafstíma** þannig að endurtekning gerist utan vinnutíma eða um helgar. Veljið **Engin lokadagsetning**. 

   ![Skilgreina upphafsdagsetningu og tíma endurtekningar.](media/talent-batch-history-cleanup-define-recurrence.png)

5. Veldu **Í lagi**.

6. Ef þörf krefur skal breyta öðrum færibreytum undir **Keyra í bakgrunni** og síðan velja **Í lagi**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Auka afköst með sjálfvirkum hreinsunarverkum](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]