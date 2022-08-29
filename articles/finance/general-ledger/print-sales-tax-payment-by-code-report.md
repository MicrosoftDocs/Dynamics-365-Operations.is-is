---
title: Prenta VSK-greiðslu eftir kóðaskýrslu
description: Þessi grein veitir upplýsingar um stillingar og aðgerðir sem eru nauðsynlegar til að prenta skýrslu Vöruskattsgreiðslu eftir kóða í bókhalds- eða skattkóðagjaldmiðlinum.
author: AdamTrukawka
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.search.form: ''
ms.openlocfilehash: ea11826d21b66e6283abf24b3f7b0945e6eb9192
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272369"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Prenta VSK-greiðslu eftir kóðaskýrslu 

[!include [banner](../includes/banner.md)]

Til að prenta skýrsluna **VSK-greiðsla eftir kóða** ferðu í **Skattur** \> **Fyrirspurnir og skýrslur** \> **VSK-skýrslur** \> **VSK-greiðsla eftiri kóða**. Sjálfgefið er að skýrslufjárhæðir séu búnar til í bókhaldsgjaldmiðli lögaðila fyrir alla skýrslukóða sem settir eru upp á síðunni **Kóðar fyrir virðisaukaskattskýrslu**.

Þú getur einnig búið til þessa skýrslu þannig að hún sýni VSK-greiðslufjárhæðir í gjaldmiðlum VSK-kóða fyrir alla skýrslukóða sem er úthlutað á VSK-kóða á síðunni **VSK-kóðar**.

## <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

Á vinnusvæðinu **Eiginleikastjórnun** kveikirðu á eftirfarandi eiginleika: **Mynda VSK-greiðslu eftir kóðaskýrslu í gjaldmiðli VSK-kóða**.

## <a name="run-the-report"></a>Keyrðu skýrsluna

1. Farðu í **Skatt** \> **Fyrirspurnir og skýrslur** \> **VSK-skýrslur** \> **VSK-greiðsla eftir kóða**.
2. Í reitnum **Skýrslugjaldmiðill** velurðu eitt af eftirfarandi gildum:

    - **Bókhaldsgjaldmiðill** - Prentaðu skýrlslufjárhæðirnar í bókhaldsgjaldmiðli.
    - **Gjaldmiðill VSK-kóða** - Prentaðu skýrslufjárhæðirnar í gjaldmiðlum VSK-kóða.

    ![Svarglugginn VSK-greiðsla eftir kóða.](media/Sales-tax-payment-by-code.png)

Eftirfarandi skýringarmynd sýnir dæmi um skýrsluna sem er búin til. Skýrslan sýnir að skýrslukóðinn **101** er með gjaldmiðilinn **EUR** ef reiturinn **VSK-gjaldmiðill** er stilltur á **EUR** fyrir VSK-kóðann sem skýrslukóðanum er úthlutað á.

![Dæmi um VSK-greiðslu eftir kóðaskýrslu.](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
