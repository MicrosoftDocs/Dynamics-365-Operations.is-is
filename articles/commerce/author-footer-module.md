---
title: Neðanmálseining
description: Þetta efni fjallar um neðanmálseiningar og hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 03/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 81db5cf32f23b7ee1ca8325eeec2e6ceafda55e0
ms.sourcegitcommit: 90a553e271e7cd471fed2e4f006d753fdb67b47d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2022
ms.locfileid: "8374832"
---
# <a name="footer-module"></a>Neðanmálseining  

[!include [banner](includes/banner.md)]

Þetta efni fjallar um síðufótseiningar og lýsir hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.

Neðanmálseiningin er sérstakur gámur sem er notaður til að hýsa einingarnar sem birtast í síðufætinum. Til dæmis getur hún innihaldið tengla á ýmsar síður á vefsvæðinu, eins og síðurnar **Hafa samband** og **Stefna verslunar**.

Eftirfarandi mynd sýnir dæmi um neðanmálseiningu á síðu svæðis.

![Dæmi um neðanmálseiningu.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Eiginleikar neðanmálseiningar 

Eins og á við um flesta gáma, styður neðanmálseiningin eiginleika fyrir fyrirsögnina og breiddina. Hún styður einnig að bæta við mörgum einingum neðanmálsflokka. Hver eining neðanmálsflokks sem er bætt við er gerð sem dálkur í neðanmálseiningunni.

## <a name="modules-available-in-a-footer-module"></a>Einingar eru fáanlegar í neðanmálseiningunni

**Fótur atriði** – Fóthlutaeining getur innihaldið annað hvort fyrirsögn eða tengil. Fyrirsögnin er almennt notuð sem heiti fótahluta.  Hægt er að stilla hvern tengil í neðanmálinu þannig að hann hafi bara texta (til dæmis tenglana „Hafðu samband“ og „Persónuvernd“), eða þannig að hann hafi bæði texta og mynd (til dæmis tengla á samfélagsmiðlum). Ef bæði fyrirsögn og tengill eru gefin upp mun fyrirsagnareiginleikinn hafa forgang yfir tengilinn. 

**Efst á síðu** - Einingin Efst á síðu veitir tengil fyrir fljótlega flettingu efst á síðuna. Áfangastaðar er krafist. Sjálfgefið gildi áfangastaðar er \#, sem fer með notandann efst á síðuna.

## <a name="create-a-footer-module"></a>Búa til neðanmálseiningu

1. Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.
1. Í glugganum **Nýtt brot** skal velja eininguna **Hólf**, slá inn heiti fyrir brotið og síðan velja **Í lagi**.
1. Í hólfinu **Sjálfgefið hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Neðanmálsflokkur** og síðan velja **Í lagi**.
1. Í hólfinu **Neðanmálsflokkur** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Neðanmálsatriði** og síðan velja **Í lagi**.
1. Veldu hólfið **Neðanmálsatriði** og síðan, hægra megin á eiginleikasvæðinu, skal stilla fyrirsögnina, tengil og texta tengils og mynd eftir því sem þörf krefur.
1. Til að bæta við fleiri neðanmálsatriðum skal endurtaka skref 5 til 7.
1. Til að bæta tenglinum „efst á síðu“ í neðanmáli skal velja úrfellingarmerkið (**...**) í hólfinu **Neðanmálsflokkur** og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Efst á síðu** og síðan velja **Í lagi**.
1. Veldu hólfið **Efst á síðu** og síðan, hægra megin á eiginleikasvæðinu, skal stilla textann og aðrar eiginleikaeiningar eftir því sem þörf krefur.
1. Veldu **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.

Til að tryggja að haus birtist á hverri síðu, fylgdu þessum skrefum á hverju síðusniðmáti sem er búið til fyrir svæðið.

1. Í hólfinu **Neðanmál** í einingunni **Sjálfgefin síða** skal bæta við neðanmálsbrotinu sem var búið til.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.

Með því að bæta broti við síðusniðmát hjálpar þú til við að tryggja að fóturinn birtist á hverri síðu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Pöntunarstaðfestingareining](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
