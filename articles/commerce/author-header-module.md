---
title: Fyrirsagnareining
description: Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697276"
---
# <a name="header-module"></a>Fyrirsagnareining

[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]

Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Fyrirsagnareining er sérstakur gámur sem er notaður til að hýsa allar einingar sem verða sýndar í fyrirsögn síðu. Til dæmis getur hún falið í sér merki vefsvæðisins, tengla á leiðsögustigveldi, tengla á aðrar síður á vefnum og leitarstikuna.

Fyrirsagnareining er sjálfkrafa fínstillt fyrir tækið sem vefurinn er skoðaður á (það er skjáborðstæki eða fartæki). Til dæmis, í fartæki er leiðsagnarstikan smækkuð niður í hnappinn **Valmynd** (sem er stundum kallaður *hamborgaravalmynd*).

## <a name="properties-of-a-header"></a>Eiginleikar fyrirsagnar

Eins og almennir gámar, styður fyrirsagnareiningin eiginleikana **fyrirsögn** og **breidd**.

Fyrirsagnareining hefur mörg hólf. Til dæmis eru til hólf fyrir upplýsingaskilaboð, leiðsagnarvalmynd, lógó, leitarstiku, körfutákn, tákn óskalista og reikningsupplýsingar. Hvert hólf styður sérstakt mengi eininga.

## <a name="modules-that-are-available-in-a-header-module"></a>Einingar sem eru fáanlegar í fyrirsagnareiningunni

Eftirfarandi einingar er hægt að nota í fyrirsagnareiningu:

- **Leiðasagnarvalmynd** - Leiðsagnarvalmyndin táknar leiðsagnarstigveldi rásarinnar og fleiri fasta leiðsagnartengla. Hægt er að stilla leiðsagnarstigveldi rásar í Dynamics 365 Retail. Stilltir hlutir birtast síðan sem fyrirsagnarleiðsögn. Að auki er hægt að stilla fasta leiðsögutengla og hægt er að veita hlutfallslega tengla á aðrar síður á svæði fyrir rafræn viðskipti. Hægt er að stilla fyrirsögnina sjálfn til vinstri, hægri eða miðju.
- **Körfutákn** - Körfutáknið er sérstakt tákn sem stendur fyrir körfuna. Það er sýnt í fyrirsögninni og sýnir fjölda atriða í körfunni. Hlekkur á körfusíðuna ætti að fylgja körfutákninu, svo að hægt sé að vísa viðskiptavinum á körfusíðuna þegar þeir hafa samskipti við táknið.
- **Tákn óskalista** - Tákn óskalistans er sýnt í hausnum og sýnir fjölda atriða sem hefur verið bætt við óskalista viðskiptavinarins. Hlekkur á óskalistasíðuna ætti að fylgja þessu tákni, svo að hægt sé að framsenda viðskiptavini á óskalistasíðuna þegar þeir hafa samskipti við táknið.
- **Innskráningareining** - Eining innskráningar er sýnd í hausnum. Hún gerir viðskiptavinum kleift að annaðhvort skrá sig inn á reikninginn sinn eða skrá sig fyrir reikning. Ef viðskiptavinurinn er þegar skráður inn er hægt að stilla eininguna til að sýna tengla á reikningssíðuna, síðu pöntunarferilsins eða aðra síðu.
- **Merkiseining** - Þessi eining sýnir merkið sem stendur fyrir söluaðila og vörumerki. Það er mynd sem hefur tengil. Tengillinn er venjulega stilltur þannig að hann hefur tilvísun á heimasíðuna. Þess vegna geta viðskiptavinir fljótt farið aftur á heimasíðuna af hvaða síðu sem er á svæðinu.
- **Viðvörun** - Viðvörun birtist í hausnum og er notuð til að sýna innbyggð skilaboð sem eiga við um allar síður á svæðinu. Til dæmis gæti viðvörun sýnt skilaboð eins og „Árlegri útsölu lýkur eftir tvo daga.“
- **Leitarstika** - Leitarstikan gerir notendum kleift að slá inn leitarskilyrði svo að þeir geti leitað að vörum. Einingin verður að vera stillt með vefslóð á leitarniðurstöðusíðunni. Hægt er að stilla fyrirspurn strengjasniðsins (sjálfgefið gildi er **"q"**). Leitarstikan er með sjálfvirkt hólf þar sem bæta skal sjálfvirkri einingu við.
- **Sjálfvirkni** - Sjálfvirka einingin sýnir niðurstöður sem sjálfkrafa eru lagðar til. Þessar niðurstöður geta verið lykilorð, vörur eða flokkar þar sem leitarorð er að finna.

## <a name="create-a-header-module"></a>Búa til hauseiningu

Til að stofna fyrirsagnareiningu skal fylgja eftirfarandi skrefum.

1. Stofnaðu síðubrot sem inniheldur hausaeiningu.
1. Bættu einingum við hólfin í hausseiningunni.
1. Uppfærðu stillingar fyrir hverja einingu.
1. Vistaðu síðubrotið. 
1. Athuga á síðunni og birtu hana.

Til að tryggja að haus birtist á hverri síðu, fylgdu þessum skrefum á hverju síðusniðmáti sem er búið til fyrir svæðið.

1. Á sjálfgefnu síðunni bætirðu við síðubrotinu sem inniheldur hauseininguna á hausinn í aðalhólfinu.
1. Vistaðu sniðmátið. 
1. Skráðu brotið út í sniðmátinu og birtu það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Kaupkassaeining](add-buy-box.md)

[Körfueining](add-cart-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Pöntunarstaðfestingareining](order-confirmation-module.md)

[Fyrirsagnareining](author-header-module.md)

[Neðanmálseining](author-footer-module.md)
