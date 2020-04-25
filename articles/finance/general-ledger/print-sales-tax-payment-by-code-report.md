---
title: Prenta VSK-greiðslu eftir kóðaskýrslu
description: Þetta efni veitir upplýsingar um stillingar og aðgerðir sem þarf til að prenta VSK-greiðslu eftir kóðaskýrslu í bókhalds- eða skattkóðagjaldmiðli.
author: anasyash
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 3c3b251aadfa997f453e60b0842f89a6f09eb9cb
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260256"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Prenta VSK-greiðslu eftir kóðaskýrslu 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Til að prenta skýrsluna **VSK-greiðsla eftir kóða** ferðu í **Skattur** \> **Fyrirspurnir og skýrslur** \> **VSK-skýrslur** \> **VSK-greiðsla eftiri kóða**. Sjálfgefið er að skýrslufjárhæðir séu búnar til í bókhaldsgjaldmiðli lögaðila fyrir alla skýrslukóða sem settir eru upp á síðunni **Kóðar fyrir virðisaukaskattskýrslu**.

Þú getur einnig búið til þessa skýrslu þannig að hún sýni VSK-greiðslufjárhæðir í gjaldmiðlum VSK-kóða fyrir alla skýrslukóða sem er úthlutað á VSK-kóða á síðunni **VSK-kóðar**.

## <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

Á vinnusvæðinu **Eiginleikastjórnun** kveikirðu á eftirfarandi eiginleika: **Mynda VSK-greiðslu eftir kóðaskýrslu í gjaldmiðli VSK-kóða**.

## <a name="run-the-report"></a>Keyrðu skýrsluna

1. Farðu í **Skatt** \> **Fyrirspurnir og skýrslur** \> **VSK-skýrslur** \> **VSK-greiðsla eftir kóða**.
2. Í reitnum **Skýrslugjaldmiðill** velurðu eitt af eftirfarandi gildum:

    - **Bókhaldsgjaldmiðill** - Prentaðu skýrlslufjárhæðirnar í bókhaldsgjaldmiðli.
    - **Gjaldmiðill VSK-kóða** - Prentaðu skýrslufjárhæðirnar í gjaldmiðlum VSK-kóða.

    ![Svarglugginn VSK-greiðsla eftir kóða](media/Sales-tax-payment-by-code.png)

Eftirfarandi skýringarmynd sýnir dæmi um skýrsluna sem er búin til. Skýrslan sýnir að skýrslukóðinn **101** er með gjaldmiðilinn **EUR** ef reiturinn **VSK-gjaldmiðill** er stilltur á **EUR** fyrir VSK-kóðann sem skýrslukóðanum er úthlutað á.

![Dæmi um VSK-greiðslu eftir kóðaskýrslu](media/Sales-tax-payment-by-code-2.png)
