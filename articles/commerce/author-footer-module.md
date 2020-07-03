---
title: Neðanmálseining
description: Þetta efni fjallar um neðanmálseiningar og hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 87ffc0204019f2f7122c40dc21bdb5de012929d6
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411206"
---
# <a name="footer-module"></a>Neðanmálseining  

[!include [banner](includes/banner.md)]

Þetta efni fjallar um neðanmálseiningar og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Neðanmálseiningin er sérstakur gámur sem er notaður til að hýsa einingarnar sem birtast í síðufætinum. Til dæmis getur hún innihaldið tengla á ýmsar síður á vefsvæðinu, eins og síðurnar **Hafa samband** og **Stefna verslunar**.

Eftirfarandi mynd sýnir dæmi um neðanmálseiningu á síðu svæðis.

![Dæmi um neðanmálseiningu](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Eiginleikar neðanmálseiningar 

Eins og á við um flesta gáma, styður neðanmálseiningin eiginleika fyrir fyrirsögnina og breiddina. Hún styður einnig að bæta við mörgum einingum neðanmálsflokka. Hver eining neðanmálsflokks sem er bætt við er gerð sem dálkur í neðanmálseiningunni.

## <a name="modules-available-in-a-footer-module"></a>Einingar eru fáanlegar í neðanmálseiningunni

**Neðanmálsatriði** - Eining neðanmálsatriða getur innihaldið fyrirsögn, mynd og tengil. Hægt er að nota fyrirsögnina annaðhvort staka eða í samsetningu með mynd og tengli. Hægt er að stilla hvern tengil í neðanmálinu þannig að hann hafi bara texta (til dæmis tenglana „Hafðu samband“ og „Persónuvernd“), eða þannig að hann hafi bæði texta og mynd (til dæmis tengla á samfélagsmiðlum).

**Efst á síðu** - Einingin Efst á síðu veitir tengil fyrir fljótlega flettingu efst á síðuna. Áfangastaðar er krafist. Sjálfgefið gildi áfangastaðar er \#, sem fer með notandann efst á síðuna.

## <a name="create-a-footer-module"></a>Búa til neðanmálseiningu

1. Farðu í **Síðubrot** og veldu **Nýtt** til að búa til nýtt síðubrot.
1. Í glugganum **Nýtt síðubrot** skal velja eininguna **Hólf**, slá inn heiti fyrir síðubrotið og síðan velja **Í lagi**.
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

Með því að bæta síðusniðinu við síðusniðmát tryggirðu að neðanmálið sé sett á hverja síðu.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupkassaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Pöntunarstaðfestingareining](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)
