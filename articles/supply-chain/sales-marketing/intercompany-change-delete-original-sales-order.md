---
title: Breyta eða eyða upprunalegri sölupöntun innan samstæðu
description: Í þessu efnisatriði er útskýrt hvernig á að breyta og eyða virkni upprunalegrar sölupöntunar
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7bd6bdbf65499e9f18bf6bb5e160a5634bc37fba
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548329"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Breyta eða eyða upprunalegri sölupöntun innan samstæðu

[!include [banner](../../includes/banner.md)]

Þegar sölupöntun er breytt eru breytingarnar sjálfkrafa samstilltar með bæði viðeigandi samstæðuinnkaupapöntun og samstæðusölupöntun.

> [!NOTE]
> Innkaupapantanir fyrir utanaðkomandi lánardrottna verða ekki fyrir neinum áhrifum af þeim breytingum sem eru gerðar, ekki heldur upprunalegar sölulínur sem eru tengdar við línur innkaupapöntunar fyrir utanaðkomandi lánardrottna.

Í eftirfarandi töflu eru teknar saman breytingarnar sem þú getur gert og niðurstöðurnar sem búist er við.

| Aðgerð | Niðurstaða |
|---|---|
| Eyða&nbsp;upprunalegri&nbsp;&nbsp;sölupöntun&nbsp;. | Tengdum innkaupapöntunum samstæðu og sölupöntunum samstæðu er einnig eytt. Ef staða pöntunarinnar er **Tiltektarlisti** eða seinna í ferlinu er ekki hægt að eyða sölupöntuninni. |
| Eyða línu í upprunalegri sölupöntun. | Tengdri innkaupapöntunarlínu samstæðu og sölupöntunarlínu samstæðu er eytt. Ef staða pöntunarinnar er **Tiltektarlisti** eða seinna í ferlinu er ekki hægt að eyða sölupöntunarlínunni. |
| Bæta nýrri sölulínu við upprunalega sölupöntun. | Nýja sölulínan er bæði stofnuð í innkaupapöntun samstæðunnar og sölupöntun samstæðunnar. |
| Breyta magni í upprunalegri sölupöntunarínu. | Magnið er samstillt við bæði línuna í innkaupapöntun samstæðunnar og línuna í sölupöntun samstæðunnar. Heildarupphæðin er endurreiknuð í öllum pöntununum. |
| Gera beina afhendingu óvirka á upprunalegri sölupöntun. | Ekki er hægt að breyta reitnum **Bein afhending** í upprunalegri sölupöntun ef lína samstæðusölupöntunar hefur náð lágmarksstöðunni **Tiltektarlisti**, **Úttakspöntun** eða **Færslubók tiltektarlista**. Afhendingaraðsetrinu á innkaupapöntun samstæðunnar er breytt í venjulega afhendingaraðsetrið (venjulegt afhendingaraðsetur innkaupapöntunar). Línum samstæðuinnkaupapöntunar er einnig breytt í venjulegt afhendingaraðsetur fyrir línurnar. Hvort tveggja er samstillt við sölupöntun samstæðunnar og línurnar. Afhendingargerðinni á öllum línum í upphaflegu sölupöntuninni er breytt í **Engin** og svæðið er samstillt innkaupalínum samstæðunnar. Innkaupapantanir fyrir utanaðkomandi lánardrottna verða ekki fyrir áhrifum, ekki heldur upprunalegar sölulínur sem eru tengdar við línur innkaupapöntunar fyrir utanaðkomandi lánardrottna. Afhendingardagsetningin á innkaupapöntun og línum samstæðunnar og umbeðnar dagsetningar móttöku/sendingar á sölupöntun samstæðunnar eru uppfærðar. |
| Virkja beina afhendingu á upprunalegri sölupöntun. | Ef lína samstæðusölupöntunar hefur náð lágmarksstöðu **Tiltektarlista**, **Úttakspöntunar** eða **Færslubókar tiltektarlista** er ekki hægt að breyta reitnum **Bein afhending** í upprunalegri sölupöntun. Afhendingaraðsetrinu á innkaupapöntun samstæðunnar verður breytt í afhendingaraðsetrið á upprunalegu sölupöntuninni og samstillt við sölupöntun samstæðunnar. Gerð afhendingar í öllum línum upprunalegrar sölupöntunar er breytt í **Beina afhendingu** og reiturinn er samstilltur við línur innkaupapöntunar innan samstæðu. Afhendingaraðsetrið á öllum upprunalegum sölupantanalínum er samstillt bæði við línur innkaupapöntunar samstæðunnar og við línur sölupöntunar samstæðunnar. Afhendingardagsetningin á innkaupapöntun og línum samstæðunnar og umbeðnar dagsetningar móttöku/sendingar á sölupöntun samstæðunnar eru uppfærðar. |
| Bæta athugasemd við bæði haus upprunalegu sölupöntunarinnar og línurnar. | Athugasemdin verður ekki afrituð á innkaupapöntun samstæðunnar eða sölupöntun samstæðunnar. |
| Breyta eða eyða athugasemd. | Ef athugasemd er breytt eða eytt, er samsvarandi athugasemd í innkaupapöntun samstæðunnar og sölupöntun samstæðunnar breytt eða eytt á sama hátt. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
