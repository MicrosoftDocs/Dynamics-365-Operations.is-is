---
title: Neðanmálseining
description: Þetta efni fjallar um neðanmálseiningar og hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697314"
---
# <a name="footer-module"></a>Neðanmálseining  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um neðanmálseiningar og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Neðanmálseiningin er sérstakur gámur sem er notaður til að hýsa einingarnar sem birtast í síðufætinum. Til dæmis getur hún innihaldið tengla á ýmsar síður á vefsvæðinu, eins og síðurnar **Hafa samband** og **Stefna verslunar**.

## <a name="footer-module-properties"></a>Eiginleikar neðanmálseiningar 

Eins og flestir gámar, styður neðanmálseining eiginleika fyrir fyrirsögnina og breiddina. Hún styður einnig að bæta við mörgum einingum neðanmálsflokka. Hver eining neðanmálsflokks sem er bætt við er gerð sem dálkur í neðanmálseiningunni.

## <a name="modules-available-in-a-footer-module"></a>Einingar eru fáanlegar í neðanmálseiningunni

**Neðanmálsatriði** - Eining neðanmálsatriða getur innihaldið fyrirsögn, mynd og tengil. Hægt er að nota fyrirsögnina annaðhvort staka eða í samsetningu með mynd og tengli. Hægt er að stilla hvern tengil í neðanmálinu þannig að hann hafi bara texta (til dæmis tenglana „Hafðu samband“ og „Persónuvernd“), eða þannig að hann hafi bæði texta og mynd (til dæmis tengla á samfélagsmiðlum).

**Efst á síðu** - Einingin Efst á síðu veitir tengil fyrir fljótlega flettingu efst á síðuna. Áfangastaðar er krafist. Sjálfgefið áfangastaðargildi er # sem sendir notandann efst á síðuna.

## <a name="author-a-footer-module"></a>Stofna neðanmálseiningu

1. Í leiðsagnarglugganum velurðu **Brot** og velur síðan **Nýtt síðubrot**.
1. Í valmyndinni **Nýtt síðubrot** velurðu neðanmálseininguna, sláðu inn heiti fyrir síðubrotið og veldu síðan **Í lagi**.
1. Í útlínutrénu til vinstri velurðu úrfellingarhnappinn (**...**) fyrir neðanmálseininguna og velur síðan **Bæta við einingu**.
1. Í valmyndinni **Bæta við einingu** velurðu neðanmálsflokkseiningu og velur síðan **Í lagi**.
1. Í útlínutrénu velurðu úrfellingarhnappinn fyrir neðanmálsflokkseininguna og velur síðan **Bæta við einingu**.
1. Í valmyndinni **Bæta við einingu** velurðu neðanmálsliðareiningu og velur síðan **Í lagi**.
1. Í útlínutrénu velurðu neðanmálsliðareininguna. Síðan skaltu stilla fyrirsögnina, tengja og tengja texta og mynd eins og þú þarfnast í eiginleikaglugganum til hægri.
1. Til að bæta við fleiri neðanmálsliðum skaltu endurtaka skref 5 til og með 7.
1. Til að bæta við tenglinum „Efst á síðu“ velurðu úrfellingarhnappinn fyrir neðanmálsflokkseininguna og velur síðan **Bæta við einingu**.
1. Í valmyndinni **Bæta við einingu** velurðu eininguna Efst á síðu og velur síðan **Í lagi**.
1. Í útlínutrénu velurðu eininguna Efst á síðu. Síðan skaltu stilla eininguna Efst á síðu í eiginleikaglugganum til hægri eins og þú þarft.
1. Vistaðu síðusagnarbrotið, skráðu það inn og gefðu það út.

Fylgdu þessum skrefum á hvert síðusniðmát sem búið er til fyrir svæðið.

1. Í hólfinu **Aðal** á sjálfgefnu síðunni, í neðanmálseiningunni skaltu bæta við neðanmálsbrotinu sem þú bjóst til.
1. Vistaðu sniðmátið, athugaðu það og gefðu það út.

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