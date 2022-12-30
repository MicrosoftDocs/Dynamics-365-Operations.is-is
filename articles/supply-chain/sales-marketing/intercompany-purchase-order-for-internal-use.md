---
title: Stofna og reikningsfæra samstæðuinnkaupapöntun fyrir innri notkun
description: Þessi grein útskýrir hvernig á að stofna og reikningsfæra samstæðuinnkaupapöntun fyrir innri notkun
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 2260128c276ab7b712f7c97945b188ea42099fb4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877538"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Stofna og reikningsfæra samstæðuinnkaupapöntun fyrir innri notkun

[!include [banner](../../includes/banner.md)]

Hægt er að stofna innkaupapöntun innan samstæðu fyrir lánardrottinn innan samstæðu. Þetta stofnar sjálfkrafa stofna sölupöntun innan samstæðu hjá samstæðulánardrottinn.

![Innra innkaupaferli innan samstæðu](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Stofna samstæðuinnkaupapöntun og samsvarandi samstæðusölupöntun

Gerðu þessi skref í AAA lögaðila, eins og sýnt er í skýringarmynd.

1. Veldu **Viðskiptaskuldir** \> **Innkaupapantanir** \> **Allar innkaupapantanir**.
1. Á listasíðunni **Allar innkaupapantanir** skal stofna innkaupapöntun fyrir samstæðulánardrottin. Reitagildin eru afrituð úr lánardrottnalyklinum í innkaupapöntunina.

    Þar sem þú ert að vinna með samstæðulánardrottni er samstæðusölupöntun stofnuð í lögaðilanum sem samsvarar lánardrottni. Númer samstæðusölupöntunarinnar getur verið það sama og númer samstæðuinnkaupapöntunarinnar og það getur innihaldið auðkenni lögaðilans. Númeraskipulagið sem er notað fer eftir valinu í reitnum **Tölusetning sölupantana** á síðunni **Innan samstæðu**. Ef þú stofnar til dæmis innkaupapöntun 00029\_064 í lögaðila AAA er sölupöntunarnúmerið í lögaðila BBB AAA00029\_64.

    Upplýsingaskilaboð í upplýsingakladda sem tilkynna að samstæðuinnkaupapöntun og samstæðusölupöntun hafi verið stofnaðar. Skilaboðin innihalda sölupöntunarnúmer innan samstæðu þér til upplýsingar.

1. Bæta línuvörur við innkaupapöntun. Samsvarandi línuatriðum er sjálfkrafa bætt við samstæðusölupöntunina. Ef vara er ekki til í öðrum lögaðila birtast skilaboð og þú getur ekki bætt vörunni við innkaupapöntunina. Til að laga þetta þarf að skipta yfir á annan lögaðila og losa afurð til þess lögaðila. Það verður hægt að bæta vörunni við sölupantanir í þeim lögaðila. Skipta aftur yfir í lögaðila innkaupapöntunar, og halda áfram að bæta við línuatriði.
1. Þegar skráningu upplýsinga fyrir innkaupapöntunina er lokið skal staðfesta hana.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Vinna úr samstæðu fylgiseðil og reikning viðskiptavinar

Gerðu þessi skref í lögaðila BBB, eins og sýnt er í skýringarmynd.

1. Farðu í **Viðskiptakröfur \> Sölupantanir \> Allar sölupantanir**.
1. Á listasíðunni **Allar sölupantanir** skal velja samstæðusölupantanir.
1. Á aðgerðasvæðinu skal velja flipann **Taka til og pakka** og síðan velja **Fylgiseðill**.
1. Veldu gátreitinn **Bókun**.
1. Veldu **Í lagi**. Fylgiseðillinn er bókaður í lögaðila BBB.
1. Á listasíðunni **Allar sölupantanir** skal velja samstæðusölupantanir.
1. Á aðgerðasvæðinu skal velja flipann **Reikningur** og síðan velja **Reikningur**.
1. Veldu gátreitinn **Bókun**.
1. Veldu **Í lagi**.

    Reikningur viðskiptavinar fyrir samstæðusölupöntunina er bókaður í lögaðila BBB.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Vinna úr samstæðuinnhreyfingarskjal afurðar og reikningi lánardrottins

Gerðu þessi skref í AAA lögaðila, eins og sýnt er í skýringarmynd.

1. Opnið **Viðskiptaskuldir \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Á listasíðunni **Allar innkaupapantanir** skal velja samstæðuinnkaupapöntun.
1. Á aðgerðasvæðinu skal velja **Taka á móti** og síðan velja **Innhreyfingarskjal afurðar**. Innhreyfingarskjal afurðar er búið til. Númer innhreyfingarskjals afurðar er það sama og fylgiseðilsnúmer innan samstæðu.
1. Veldu gátreitinn **Bókun**.
1. Veldu **Í lagi**.
1. Á listasíðunni **Allar innkaupapantanir** skal velja samstæðuinnkaupapöntun.
1. Á aðgerðasvæðinu skal velja **Reikningur** og síðan velja **Reikningur**. Reikningur lánardrottins er stofnaður. Reikningsnúmer lánardrottins er sú sama og reikningsnúmer samstæðureiknings viðskiptavinar.
1. Ljúktu við að færa inn reikning lánardrottins og bókaðu hann síðan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
