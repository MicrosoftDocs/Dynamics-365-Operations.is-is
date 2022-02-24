---
title: Gakktu úr skugga um að tvískipt skrif sé stillt í forritum Finance and Operations og Dataverse
description: Þetta efni útskýrir hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685540"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í forritum Finance and Operations og Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse. Einkum útskýrir það hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í forriti Finance and Operations

Til að ákvarða hvort villa sem birtist þegar reynt er að vista línur til að uppfæra eru úr tvöfaldri skráningu skal fyrst staðfesta að tvöföld skráning sé stillt.

+ Ef þú hefur stjórnunarréttindi í forriti Finance and Operations, farðu til **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**. Ef upplýsingar um tengt umhverfi og lista yfir töflukort sem eru í keyrslu eru birtar er tvöföld skráning stillt.

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur stjórnunarréttindi](media/verify_fin_ops_1.png)

+ Ef þú ert ekki með stjórnandaréttindi muntu fá villuboð, *Ekki er hægt að skrifa gögn í eininguna \<entity name\>*. Í dæminu á eftirfarandi mynd er ekki hægt að stofna viðskiptamannslínu í Finance and Operations forritinu vegna þess að tvöföld skráning er grunnstillt en viðskiptavinaflokkur og tilvísunargögn greiðsluskilmála eru ekki til í Dataverse.

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur ekki stjórnunarréttindi](media/verify_fin_ops_2.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í forriti Finance and Operations, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í Dataverse

Þegar þú býrð til gögn, ef þú sérð reitinn **Fyrirtæki** á síðum í Dataverse, tvískipt skrif er stillt.

![Staðfestir Dataverse tenginguna](media/verify_cds.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í Dataverse, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

Fyrir upplýsingar um hvernig á að skoða villuupplýsingar ef þú lendir í villum meðan þú býrð til gögn í Dataverse, sjáðu [Kveiktu á og skoðaðu rekja innskráningu viðbótarinnar Dataverse til að skoða villuupplýsingar](dual-write-troubleshooting.md#enable-view-trace).
