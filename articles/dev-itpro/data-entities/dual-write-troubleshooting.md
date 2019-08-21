---
title: Leiðbeiningar úrræðaleitar gagnasamþættingar
description: Þetta efni veitir úrræðaleitarupplýsingar um samþættingu gagna á milli Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797276"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Leiðbeiningar úrræðaleitar gagnasamþættingar

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Kveiktu á viðbótarsporun í Common Data Service og athugaðu upplýsingar um villuleiðbeiningar við tvískipta viðbót

Ef þú ert í vandræðum eða villu með tvískiptri samstillingu, geturðu skoðað villurnar í rakningarkladdanum:

1. Áður en þú getur skoðað villurnar verður þú að virkja viðbótarsporun með því að nota leiðbeiningarnar í [Skráðu viðbót](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) til að virkja viðbótarsporunina. Nú geturðu skoðað villurnar.
2. Skrá inn á Dynamics 365 for Sales.
3. Smelltu á stillingartáknið (gír) og veldu **Ítarlegar stillingar**.
4. Í valmyndinni **Stillingar** velurðu **Sérstillingar > Rakningarkladdi viðbótarsporunar**.
5. Smelltu á tegundarheitið **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** til að birta villuupplýsingarnar.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Athugaðu tvískiptar samstillingarvillur í Finance and Operations

Þú getur athugað villurnar við prófun með því að fylgja þessum skrefum:

+ Skráðu þig inn í Lifecycle Services (LCS).
+ Opnaðu LCS-verkið sem þú valdir til að framkvæma tvískipt próf.
+ Farðu í Umhverfi í skýi.
+ Fjartengt skjáborð til Finance and Operations VM með staðbundnum lykli sem birtist í LCS.
+ Opnaðu tilvikayfirlit. 
+ Farðu í **Forrit og þjónustukladdar > Microsoft > Dynamics > AX -DualWriteSync > Virkt**. Villurnar og smáatriðin birtast.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Hvernig á að aftengja og tengja annað Common Data Service umhverfi frá Finance and Operations

Þú getur uppfært tengla með því að fylgja þessum skrefum:

+ Farðu í Finance and Operations umhverfið.
+ Opnaðu Gagnastýringu.
+ Smelltu á **Tengil við CDS fyrir forrit**.
+ Veldu allar keyrandi kortlagningar og smelltu á **Hætta**. 
+ Veldu allar kortlagningar og smelltu á **Eyða**.

    > [!NOTE]
    > Valkosturinn **Eyða** birtist ekki ef sniðmátið **ViðskiptavinurV3-lykill** er valið. Afturkallaðu það ef þörf er á. **ViðskiptavinurV3-lykill** er eldra útvegað sniðmát og vinnur með lausninni Prospect to Cash. Vegna þess að það er gefið út á heimsvísu birtist það undir öllum sniðmátum.

+ Smelltu á **Aftengja umhverfi**.
+ Smelltu á **Já** til staðfestingar.
+ Til að tengja nýja umhverfið skaltu fylgja skrefunum í [uppsetningarhandbók](https://aka.ms/dualwrite-docs).

