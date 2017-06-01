---
title: "Öryggi notanda í gátt lánardrottins"
description: "Þessi skrá útskýrir hvernig á að setja upp öryggisbúnað fyrir utanaðkomandi lánardrottna sem nota Gátt Lánardrottins. Upplýsingarnar gildir aðeins um 2016 Febrúar &amp; 2016 Maí útgáfum Dynamics AX."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 560e0760c33cab4186095ac2ae7e105d75cc16d0
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="vendor-portal-user-security"></a>Öryggi notanda í gátt lánardrottins

[!include[banner](../includes/banner.md)]


Þessi skrá útskýrir hvernig á að setja upp öryggisbúnað fyrir utanaðkomandi lánardrottna sem nota Gátt Lánardrottins. Upplýsingarnar gildir aðeins um 2016 Febrúar &amp; 2016 Maí útgáfum Dynamics AX.

Virknin gátt Lánardrottins hefur verið skipt út fyrir virknina aukið samstarf lánardrottna í Dynamics 365 for Operations útgáfa 1611. Nánari upplýsingar um uppsetningu öryggis fyrir samstarf lánardrottna sjá [ Uppsetning og viðhald samstarfs lánardrottna](set-up-maintain-vendor-collaboration.md). Gátt lánardrottins birtir takmarkað safn upplýsinga um innkaupapantanir (POs) til ytri lánardrottna. Mikilvægt er að þú setjir rétt upp heimildir notanda fyrir gátt lánardrottins í Microsoft Dynamics AX, svo að lánardrottnar hafi ekki óviljandi aðgang að viðbótarupplýsingum í uppsetningu á Dynamics AX. **Mikilvægt:** Ólíkt öðrum notendum ættu ytri lánardrottnar ekki að hafa hlutverkið **SystemUser**. Hlutverkið **SystemUser** veitir aðgang að safni réttinda sem ekki eru hæafar fyrir utanaðkomandi notendur.

## <a name="setting-up-a-vendor-portal-user"></a>Setja upp notanda gáttar lánardrottins
Áður en notendareikningur er stofnaður fyrir einhvern sem mun nota gátt lánardrottins, verður að setja upp lánardrottinn til að heimila samvinnu við gátt lánardrottins. Notaðu reitinn **Innkaupapöntun samvinnu** á flipanum **Almennt** á síðunni **Lánardrottnar**. Ytri lánardrottnar sem nota gátt lánardrottins verða að hafa eftirfarandi uppsetningu:

-   Notandareikningurinn Microsoft Azure Active Directory (AAD) verður að vera skráður fyrir lánardrottinn á síðunni **Notendur** í Dynamics AX.
-   Lánardrottinn verður að hafa öryggishlutverkið **Lánardrottinn (ytri)** en ekki hlutverkið **SystemUser**. **Ábending:** Hlutverkið **SystemUser** er veitt sjálfkrafa þegar þú stofnar nýjan lykil notanda í Dynamics AX. Þess vegna þarf að fjarlægja það hlutverk og staðfesta viðvörunarboðin sem berast.
-   Lánardrottinsnotandi ætti ekki að veita heimild til að bæta viðbótarreitum úr töflum innkaupapöntunar við skoðun þeirra á innkaupapöntun. Á flipanum **Sérsnið**, á flipanum **Notendur**, skal stilla valkostinn **Yfirlýst sérsnið leyfð** fyrir notandann á **Nei**.
-   Notandareikningurinn verður að vera tengdur skráðum tengilið. Á síðunni **Notendur** skal velja tengilið í reitnum **Heiti**. Sá sem er valinn ætti að hafa hlutverkið **Tengiliður** fyrir viðkomandi lánardrottin.

Ef sami einstaklingur krefst aðgangs að gátt lánardrottins fyrir marga lánardrottna (kannski fyrir mismunandi lögaðila) verður hver notendareikningur þess einstaklings að vera tengdur sama skráðum tengilið. Hlutverkið **Lánardrottinn (ytri)** inniheldur alla grunngetu sem þarf til að nota aðgerðirnar sem eru tiltækar í gátt lánardrottins. Þessi uppsetning hjálpar til við að tryggja að samræmt notendaviðmót sem ytri notandinn sér leggi aðeins áherslu á ætlaðar aðstæður.

<a name="see-also"></a>Sjá einnig
--------

[Samstarf lánardrottna](collaborate-vendors-vendor-portal.md)




