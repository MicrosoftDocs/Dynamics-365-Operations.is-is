---
title: Færibreytur samstæðu
description: Þetta efnisatriði útskýrir færibreytur innan samstæðu
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 78186d466d88f876629ceb81ec99b94c8818c560
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678604"
---
# <a name="intercompany-parameters"></a>Færibreytur samstæðu

[!include [banner](../../includes/banner.md)]

Í samstæðufyrirtæki er hægt að setja upp færibreytur sem skera úr um hvernig viðskipti eru stunduð milli mismunandi lögaðila. Þessar færibreytur ákvarðast af reitunum sem þú velur. Hægt er að velja mismunandi samsetningar til að endurspegla mismunandi viðskiptaaðstæður.

Eftirfarandi tvö dæmi lýsa aðstæðum fyrir fyrirtæki innan samstæðu, eitt með tveimur stigum og annað með þremur stigum.

## <a name="example-1-two-level-intercompany-chain"></a>Dæmi 1: tveggja stiga samstæðukeðja

Fyrirtæki innan samstæðu fela í sér eftirfarandi lögaðila:

- Lögaðili A – Selur til utanaðkomandi viðskiptavina, en á engar birgðir. Þessi lögaðili kaupir af Lögaðila B.
- Lögaðili B – Selur eingöngu til lögaðila A.

Báðir lögaðilarnir geta selt og keypt hvor af öðrum.

Í þessu dæmi, er verðið á upprunalegri sölupöntun, sem beint er til utanaðkomandi viðskiptavinar, ávallt grundvallað á söluverðinu. Verðlagningu samstæðusölupöntunar og samstæðuinnkaupapöntunar er stjórnað af innri sölu eða tilfærsluverðlagi í samstæðusölupöntun í lögaðila B.

Upplýsingar í haus pantana stjórnast af upprunalegri sölupöntun til ytri viðskiptavinar. Hverskonar breytingar á sölupöntuninni innan samstæðunnar eru ekki samhæfðar við upprunalegu sölupöntunina.

Í lögaðila A, á síðunni **Innan samstæðu** fyrir lánardrottna, skal velja **Innkaupapöntunarreglur**. Veldu eftirfarandi reiti í reitahópnum **Upprunaleg sölupöntun (bein afhending)**:

- **Prenta fylgiseðil sjálfvirkt**
- **Bóka reikning sjálfvirkt**
- **Prenta reikning sjálfvirkt**

Í reitahópnum **Innkaupapöntun innan samstæðu (bein afhending)** skal velja eftirfarandi reit:

- **Bóka reikning sjálfvirkt**

Í flokknum **Upphafleg sölupöntun <-> Samstæðuinnkaupapöntun** skal velja eftirfarandi reiti:

- **Upplýsingar um viðskiptavin**
- **RMA-númer**

Í reitahópnum **Samstæðuinnkaupapöntun <-> Samstæðusölupöntun** skal velja eftirfarandi reiti:

- **Upplýsingar um viðskiptavin**
- **RMA-númer**
- **Rununúmer**
- **Raðnúmer**

Í lögaðilanum á síðunni **Innan samstæðu** fyrir viðskiptavini skal velja **Sölupöntunarreglur**. Veldu eftirfarandi reiti í reitahópnum **Stofnun sölupöntunar innan samstæðu**:

- **Tölusetning sölupantana** : **Fyrirtæki + upphaflegt númer**
- **Leyfa safnuppfærslu skjala fyrir upprunalegan viðskiptavin**

Í reitahópnum **Samstæðusölupöntunarverð** skal velja eftirfarandi reiti:

- **Leit að verði og afslætti**
- **Leyfa breytingar á verði**
- **Leyfa breytingar á afslætti**

Í reitahópnum **Samstæðusölupöntun \> Samstæðuinnkaupapöntun** skal velja eftirfarandi reiti:

- **Rununúmer**
- **Raðnúmer**

## <a name="example-2-three-level-intercompany-chain"></a>Dæmi 2: þriggja stiga samstæðukeðja

Fyrirtæki innan samstæðu fela í sér eftirfarandi lögaðila:

- Lögaðili A – Lögaðili sölu sem selur til ytri viðskiptavina og kaupir frá lögaðila B.
- Lögaðili B – Lögaðili framleiðslu eða dreifingar sem getur ekki afhent afurðir og kaupir frá lögaðila C.
- Lögaðili C – Lögaðili framleiðslu eða dreifingar sem afhendir afurðir til lögaðila B.

Innri tilfærsluverðlagning milli lögaðila B og C er á kostnaðarverði frá lögaðila sölunnar við upphaf keðjunnar. Hún er einnig á kostnaðarverði til lögaðila A sem selur til ytri viðskiptavina. Hinsvegar eru verð á upprunalegri sölupöntun til ytri viðskiptavinar ávallt byggð á söluverði.

Verðlagningu á öllum samstæðusölupöntunum og samstæðuinnkaupapöntunum er stjórnað í samstæðusölupöntuninni. Henni er stjórnað við upphaf keðjunnar. Lögaðili C sem selur til lögaðila B stýrir þar af leiðandi verðinu. Verðlagning samstæðusölupöntunar byggir á innri sölu eða tilfærsluverðlagningu sem er sett upp í lögaðila C.

Upplýsingar í haus pantana stjórnast af upprunalegri sölupöntun til ytri viðskiptavinar. Hverskonar breytingar á samstæðu-pöntunum eru ekki samhæfð við upprunalega sölupöntun.

Velja skal eftirfarandi færibreytur:

Í lögaðila A, á síðunni **Innan samstæðu** fyrir lánardrottna, skal velja **Innkaupapöntunarreglur**. Veldu eftirfarandi reiti í reitahópnum **Upprunaleg sölupöntun (bein afhending)**:

- **Prenta fylgiseðil sjálfvirkt**
- **Bóka reikning sjálfvirkt**
- **Prenta reikning sjálfvirkt**

Í reitahópnum **Innkaupapöntun innan samstæðu (bein afhending)** skal velja eftirfarandi reit:

- **Bóka reikning sjálfvirkt**

Í reitahópnum **Upphafleg sölupöntun <-> Samstæðuinnkaupapöntun** skal velja eftirfarandi reiti:

- **Upplýsingar um viðskiptavin**
- **RMA-númer**

Í reitahópnum **Samstæðuinnkaupapöntun <-> Samstæðusölupöntun** skal velja eftirfarandi reiti:

- **Upplýsingar um viðskiptavin**
- **RMA-númer**
- **Rununúmer**
- **Raðnúmer**

Í lögaðilanum á síðunni **Innan samstæðu** fyrir viðskiptavini skal velja **Sölupöntunarreglur**. Veldu eftirfarandi reiti í reitahópnum **Stofnun sölupöntunar innan samstæðu**:

- **Tölusetning sölupantana** : **Fyrirtæki + upphaflegt númer**
- **Leyfa safnuppfærslu skjala fyrir upprunalegan viðskiptavin**

Í reitahópnum **Samstæðusölupöntun \> Samstæðuinnkaupapöntun** skal velja eftirfarandi reiti:

- **Rununúmer**
- **Raðnúmer**

Í reitahópnum **Bókun reiknings viðskiptavinar í samstæðu** skal velja eftirfarandi reiti:

- **Einingarverð jafnt og kostnaðarverð**
- **Byrja upphaflega bókun reiknings viðskiptavinar**

Í lögaðila B, á síðunni **Innan samstæðu** fyrir lánardrottna, skal velja **Innkaupapöntunarreglur**. Veldu eftirfarandi reiti í reitahópnum **Upprunaleg sölupöntun (bein afhending)**:

- **Prenta fylgiseðil sjálfvirkt**
- **Bóka reikning sjálfvirkt**
- **Prenta reikning sjálfvirkt**

Í reitahópnum **Innkaupapöntun innan samstæðu (bein afhending)** skal velja eftirfarandi reit:

- **Bóka reikning sjálfvirkt**

Í reitahópnum **Upphafleg sölupöntun <-> Samstæðuinnkaupapöntun** skal velja eftirfarandi reiti:

- **Upplýsingar um viðskiptavin**
- **RMA-númer**
- **Verð og afsláttur**

Í reitahópnum **Samstæðuinnkaupapöntun <-> Samstæðusölupöntun** skal velja eftirfarandi reiti:

- **Upplýsingar um viðskiptavin**
- **RMA-númer**
- **Rununúmer**
- **Raðnúmer**

Í lögaðila C á síðunni **Innan samstæðu** fyrir viðskiptavini skal velja **Sölupöntunarreglur**. Veldu eftirfarandi reiti í reitahópnum **Stofnun sölupöntunar innan samstæðu**:

- **Tölusetning sölupantana** : **Kóði númeraraðar**
- **Leyfa safnuppfærslu skjala fyrir upprunalegan viðskiptavin**

Í reitahópnum **Samstæðusölupöntunarverð** skal velja eftirfarandi reit:

- **Leit að verði og afslætti**

Í reitahópnum **Bókun reiknings viðskiptavinar í samstæðu** skal velja eftirfarandi reiti:

- **Einingarverð jafnt og kostnaðarverð**
- **Byrja upphaflega bókun reiknings viðskiptavinar**

Í reitahópnum **Samstæðusölupöntun <-> Samstæðuinnkaupapöntun** skal velja eftirfarandi reiti:

- **Rununúmer**
- **Raðnúmer**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
