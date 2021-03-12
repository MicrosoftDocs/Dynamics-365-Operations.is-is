---
title: Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.6. (nóvember 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: f253355b3de4f148c11b1d9d3f43b6756e6bd38c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983676"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Nýjungar eða breytingar í Dynamics 365 Supply Chain Management 10.0.6. (nóvember 2019)

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Supply Chain Management 10.0.6. Þessi útgáfa er með byggingarnúmer 10.0.234. Þótt almennur framboðsdagur sé í nóvember eru nýju eiginleikarnir tiltækir til snemmbærrar útgáfu í október. Frekari upplýsingar um útgáfu 10.0.6 er að finna í [Frekari upplýsingar](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>V2 gagnaeining afbrigðalíkana afurðar

Önnur útgáfa fyrir gagnaeininguna „vöruuppsetningarlíkön“ er gefin út (kallað „Vöruuppsetningarmódel V2“). Sjálfgefið sniðmát „418-vöruuppsetningarlíkön“ þarf einnig að vera þannig að það notar nýju „Vöruuppsetningarmódelin V2“ gagnaeininguna í innflutnings- / útflutningsramma sniðmátunum. Sniðmátið verður ekki uppfært sjálfvirkt þannig að þú verður að hlaða sniðmátið sjálfgefið. V2 einingin flytur út eina röð sem aðskild skrá í viðhengi í staðinn fyrir að vera í röð og leysa stærðartakmarkanir V1 einingarinnar. 
 
Hvað þarftu að gera til að gera þessa breytingu?
-    Þar sem V1 einingin hefur verið felld úr gildi ættir þú að byrja að flytja úr V1 til V2. Ef þú ert að nota sniðmátið „418 vörulíkan“ geturðu smellt á hnappinn „hlaðið sjálfgefið sniðmát“ og endurhlaðið sniðmátið „418 - módel vörustillinga“
-    Ef þú þarft að halda eindrægni við núverandi kerfi geturðu haldið áfram að nota það sniðmát og (úrelt) V1 eininguna þar til þú færir samþættingarnar í nýja sniðmátið. 

## <a name="feature-management-enhancements"></a>Eiginleikastjórnunarviðbætur
Eiginleikastjórnun gerir þér nú kleift að virkja alla nýja eiginleika sjálfgefið, krefjast staðfestingar til að virkja eiginleika og virkja alla eiginleika sem ekki hafa þegar verið gerðir virkir. 


## <a name="purchase-agreement-responsible-party"></a>Ábyrgðaraðili innkaupasamnings
Þú hefur nú getu til að skilgreina aðal- og framhaldsaðila á flokkunarformi innkaupasamnings og innkaupasamningum sem af því hljótast.  Þetta veitir notandanum aðgang að þeim sem hefur umsjón með samningunum.

## <a name="rfq-link-on-the-purchase-order-line"></a>RFQ-tengill í línu innkaupapöntunar
Þú getur bætt við tilvísunartengil frá innkaupapöntunarlínunum aftur í samsvarandi RFQ línur sem þeir eru upprunnar frá, þannig að notandinn getur auðveldlega fengið styðjandi skjal beiðni um tilboð.

## <a name="additional-resources"></a>Frekari upplýsingar

### <a name="bug-fixes"></a>Villuleiðréttingar
Til að fá upplýsingar um villuleiðréttingarnar sem fylgja sérhverri uppfærslu sem er hluti af 10.0.6, skráðu þig inn á Lifecycle Services (LCS) og skoðaðu [KB grein](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Update 30 fyrir verkvang
Microsoft Dynamics 365 Supply Chain Management 10.0.6 inniheldur verkvangsuppfærslu 30. Til að læra meira um verkvangsuppfærslu 30, sjá [Hvað er nýtt eða breytt í verkvangsuppfærslu 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 útgáfa bylgja 2 áætlun
Ertu að velta fyrir þér væntanlegum og nýlega útgefnum möguleikum í einhverjum af viðskiptaforritum eða verkvangi okkar?

Skoðaðu [Dynamics 365: 2019 útgáfu bylgju 2 áætlun](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/). Við höfum tekið saman öll smáatriðin í eitt skjal sem hægt er að nota við áætlanagerð.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Fjarlægðir og úreltir eiginleikar Supply Chain Management

Efnið [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) lýsir eiginleikum sem hafa verið eða á að fjarlægja eða úrelda fyrir Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Áður en einhver eiginleiki er fjarlægður úr vörunni verður tilkynning um afskriftir tilkynnt í efninu [Fjarlægðir eða úreltir eiginleikar í Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mánuðum fyrir fjarlægingu.

Til að brjóta breytingar sem hafa aðeins áhrif á samantektartíma, en eru tvöfaldar samhæfðir við sandkassa og framleiðsluumhverfi, verður afskriftartíminn innan við 12 mánuði. Venjulega eru þetta hagnýtar uppfærslur sem þarf að gera við þýðandann.
