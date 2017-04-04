---
title: "Öryggi gátt lánardrottins"
description: "Þessi skrá útskýrir hvernig á að setja upp öryggisbúnað fyrir utanaðkomandi lánardrottna sem nota Gátt Lánardrottins. Þær upplýsingar eiga aðeins við 2016 Febrúar &amp;Maí 2016 útgáfum Dynamics AX."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 3a5c6a256f8330ba238ea3c0c25f14b10a9a58e6
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-portal-user-security"></a>Öryggi gátt lánardrottins

Þessi skrá útskýrir hvernig á að setja upp öryggisbúnað fyrir utanaðkomandi lánardrottna sem nota Gátt Lánardrottins. Þær upplýsingar eiga aðeins við 2016 Febrúar &amp;Maí 2016 útgáfum Dynamics AX.

Virkni gátt Lánardrottins hefur verið skipt eftir aukin lánardrottins samvinnusvæði aðgerðum í Dynamics 365 Aðgerðir útgáfu 1611. Nánari upplýsingar um uppsetningu á öryggi fyrir samvinnusvæði lánardrottins í [Sett upp og viðhalda lánardrottins samvinnusvæði](set-up-maintain-vendor-collaboration.md). Gátt lánardrottins birtir takmarkað safn upplýsinga um innkaupapantanir (POs) til ytri lánardrottna. Mikilvægt er að þú setjir rétt upp heimildir notanda fyrir gátt lánardrottins í Microsoft Dynamics AX, svo að lánardrottnar hafi ekki óviljandi aðgang að viðbótarupplýsingum í uppsetningu á Dynamics AX. **Mikilvægt:** Ólíkt öðrum notendum ættu ytri lánardrottnar ekki að hafa hlutverkið **SystemUser**. Hlutverkið **SystemUser** veitir aðgang að safni réttinda sem ekki eru hæafar fyrir utanaðkomandi notendur.

## <a name="setting-up-a-vendor-portal-user"></a>Setja upp notanda gáttar lánardrottins
Áður en notendareikningur er stofnaður fyrir einhvern sem mun nota gátt lánardrottins, verður að setja upp lánardrottinn til að heimila samvinnu við gátt lánardrottins. Notaðu reitinn **Innkaupapöntun samvinnu** á flipanum **Almennt** á síðunni **Lánardrottnar**. Ytri lánardrottnar sem nota gátt lánardrottins verða að hafa eftirfarandi uppsetningu:

-   Notandareikningurinn Microsoft Azure Active Directory (AAD) verður að vera skráður fyrir lánardrottinn á síðunni **Notendur** í Dynamics AX.
-   Lánardrottinn verður að hafa öryggishlutverkið **Lánardrottinn (ytri)** en ekki hlutverkið **SystemUser **. **Ábending:** Hlutverkið **SystemUser** er veitt sjálfkrafa þegar þú stofnar nýjan lykil notanda í Dynamics AX. Þess vegna þarf að fjarlægja það hlutverk og staðfesta viðvörunarboðin sem berast.
-   Lánardrottinsnotandi ætti ekki að veita heimild til að bæta viðbótarreitum úr töflum innkaupapöntunar við skoðun þeirra á innkaupapöntun. Á flipanum **Sérsnið**, á flipanum **Notendur**, skal stilla valkostinn **Yfirlýst sérsnið leyfð** fyrir notandann á **Nei**.
-   Notandareikningurinn verður að vera tengdur skráðum tengilið. Á síðunni **Notendur** skal velja tengilið í reitnum **Heiti**. Sá sem er valinn ætti að hafa hlutverkið **Tengiliður** fyrir viðkomandi lánardrottin.

Ef sami einstaklingur krefst aðgangs að gátt lánardrottins fyrir marga lánardrottna (kannski fyrir mismunandi lögaðila) verður hver notendareikningur þess einstaklings að vera tengdur sama skráðum tengilið. Hlutverkið **Lánardrottinn (ytri)** inniheldur alla grunngetu sem þarf til að nota aðgerðirnar sem eru tiltækar í gátt lánardrottins. Þessi uppsetning hjálpar til við að tryggja að samræmt notendaviðmót sem ytri notandinn sér leggi aðeins áherslu á ætlaðar aðstæður.

<a name="see-also"></a>Sjá einnig
--------

[Vendor collaboration](collaborate-vendors-vendor-portal.md)


