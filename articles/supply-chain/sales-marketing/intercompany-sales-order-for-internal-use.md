---
title: Stofna samstæðusölupöntun til innri notkunar
description: Þessi grein útskýrir hvernig á að búa til sölupöntun innan samstæðu fyrir innri notkun
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a37b8ab1b3df10cdbd3bbb87410bc3dc70dc0ed0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873522"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Stofna samstæðusölupöntun til innri notkunar

[!include [banner](../../includes/banner.md)]

Samstæðusölupöntun er yfirleitt stofnuð sjálfvirkt út frá samstæðuinnkaupapöntun. Þú getur einnig stofnað samstæðusölupöntun handvirkt sem býr þá til samstæðuinnkaupapöntun í lögaðila samstæðuviðskiptavinar.

![Innra söluferli innan samstæðu](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Stofna samstæðusölupöntun handvirkt

Gerðu þessi skref í lögaðila B, eins og sýnt er í skýringarmynd.

1. Farðu í **Viðskiptakröfur \> Sölupantanir \> Allar sölupantanir**.
1. Á aðgerðasvæðinu skal velja **Sölupöntun** til að stofna sölupöntun.
1. Á síðunni **Stofna sölupöntun** skal velja viðskiptavinalykil. Í flýtiflipanum **Almennt** skal ganga úr skugga um að gátreiturinn **Innan samstæðu** sé valinn. Þetta gefur til kynna að viðskiptavinurinn sé samstæðuviðskiptavinur.
1. Færðu inn eða breyttu upplýsingunum og veldu **Í lagi** og fylltu svo út pöntunarlínurnar eins og venjulega.

    Reitargildið **Afhendingaraðsetur** er afritað úr haus samstæðusölupöntunar í haus samstæðuinnkaupapöntunar. Reitargildið **Vörunúmer**, þ.m.t. afurðarvíddir, og reitagildin **Afhendingardagsetning** og **Gjaldmiðilskóði** eru afrituð úr samstæðusölupöntunarlínum í samstæðuinnkaupapöntunarlínur.

1. Í pöntunarhausnum skal velja **Innan samstæðu** til að skoða viðkomandi samstæðuinnkaupapöntun.
1. Í pöntunarlínunum skal velja **Innan samstæðu** til að skoða upplýsingar um lagerbirgðir fyrir samstæðuviðskipti.

> [!TIP]
> Hægt er að skoða samstæðusölupantanir á síðunni **Pantanir innan samstæðu**.

> [!NOTE]
> Þegar þú vinnur með samstæðu er mælt með að hreinsa gátreitinn **Eyða pöntun eftir reikningsfærslu** á síðunni **Færibreytur viðskiptakrafa**. Annars verður viðkomandi innkaupapöntun eytt. Við mælum einnig með því að þú hreinsir gátreitinn **Eyða innkaupapöntun eftir reikningsfærslu** á síðunni **Færibreytur viðskiptaskulda**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
