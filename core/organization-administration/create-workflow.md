---
title: "Stofna verkflæði"
description: "Þetta efnisatriði útskýrir hvernig á að stofna verkflæði."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 1255cf90498f1968568dd2fa5a1377d989f40182
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-workflow"></a>Stofna verkflæði

Þetta efnisatriði útskýrir hvernig á að stofna verkflæði.

<a name="open-the-workflow-editor"></a>Opnaðu ritstjóra verkflæðis
------------------------

Microsoft Dynamics 365 Aðgerðir einingar sem verið er að vinna í ákvarðar gerðir sem hægt er að stofna verkflæði. Fylgið eftirfarandi skrefum til að velja gerð verkflæðis til að stofna og til að opna verkflæðisritill.

1.  Fara í einingunni sem á að stofna nýtt verkflæði fyrir. Til dæmis til að stofna verkflæði fyrir innkaupabeiðnir, smellið á **innkaup og aðföng**.
2.  Smellið á **Uppsetningu**&gt;**\[heiti Einingarinnar\] verkflæði**.
3.  Á listasíðu sem birtist, á Aðgerðasvæðinu skal smellt á **Nýtt**.
4.  Á **Stofna verkflæði** síðunni, veljið þá tegund verkflæðis sem á að stofna og smellið svo á **Stofna verkflæði**. Verkflæðisritill birtist Þú getur nú notað eftirfarandi ferli til að hanna verkflæði.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Draga verkflæðisþætti yfir á striga
Svæði **verkflæðiseining** í verkflæðisritill inniheldur þætti sem þú getur bætt við verkflæði. Til að bæta einingar við verkflæðisins skal draga þær yfir í striga.

## <a name="connect-the-elements"></a>Tengja einingar
Til að tengja eina verkflæðiseiningu við aðra skal halda bendlinum yfir einingu þar til tengipunktar birtast. Smella skal á tengipunktinn og draga hann yfir í aðra einingu. Gætið þess að tengja saman allar einingarnar.

## <a name="configure-the-properties-of-the-workflow"></a>Skilgreina eiginleika verkflæðis
Fylgið eftirfarandi skrefum til að skilgreina eiginleika verkflæðis.

1.  Smellt er á striga til að tryggja að enginn verkflæðiseiningunni er valinn.
2.  Smellið á ** eiginleikar ** til að opna í **Eiginleika ** fyrir verkflæðið.
3.  Farið að ferlinu í efninu [stilla eiginleika fyrir Verkflæði](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Skilgreinið einingar verkflæðisins
Stilla hverja einingu sem er valinn og dreginn á striga. Nánari upplýsingar um hvernig á að skilgreina hverja verkflæðiseiningu er að finna í eftirfarandi efnisatriði.

-   [Skilgreina handvirkt verk](configure-manual-task-workflow.md)
-   [Skilgreina sjálfvirkt verk](configure-automated-task-workflow.md)
-   [Skilgreining samþykktarferlis](configure-approval-process-workflow.md)
-   [Skilgreining samþykktarskrefs](configure-approval-step-workflow.md)
-   [Skilgreina handvirka ákvörðun](configure-manual-decision-workflow.md)
-   [Skilgreina skilyrtri ákvörðun](configure-conditional-decision-workflow.md)
-   [Skilgreina Hliðstæður verkþáttur](configure-parallel-activity-workflow.md)
-   [Skilgreina Hliðstæður grein](configure-parallel-branch-workflow.md)
-   [Skilgreina Verkflæði línuatriðis](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Leysa allar villur eða viðvaranir
Svæðið **Villur og athugasemdir**, neðst á verkflæðisritill, birtir skilaboð sem hafa verið búnir til fyrir verkflæði. Til að finna einingu þar sem villa eða viðvörun kemur upp, skal tvísmella á villuna eða viðvörunina. Allar villur og viðvaranir verður að leysa áður en hægt er að gera verkflæði virka.

## <a name="save-and-activate-the-workflow"></a>Vista og virkja verkflæðið
Þegar þú ert tilbúinn til að vista og virkja verkflæði skaltu fylgja þessum skrefum.

1.  Smellið á **Vista og loka** til að loka verkflæðisritlinum og opna í **Vista verkflæði** skjámynd.
2.  Færðu inn athugasemdir um þær breytingar sem þú hefur gert á verkflæðinu og smelltu á **Í lagi**.
3.  Ef villur og viðvaranir hefur verið leyst, **Virkja verkflæði** birtist. Veldu einn af eftirfarandi valkostum:
    -   Smellið til að virkja þessa útgáfu verkflæðisins á **virkja nýja útgáfu**. Þegar verkflæði er virkt, notendur senda skjöl í hana í vinnslu.
    -   Eigi ekki að virkja þessa útgáfu, smellið á **Ekki virkja nýju útgáfuna**. Hægt er að virkja verkflæðið síðar.




