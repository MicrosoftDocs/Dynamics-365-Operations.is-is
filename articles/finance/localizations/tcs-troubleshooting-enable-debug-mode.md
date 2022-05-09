---
title: Virkja villuleitarstillingu í skattaútreikningsþjónustunni
description: Þetta efnisatriði útskýrir hvernig á að virkja villuleitarham í skattaútreikningsþjónustunni til að rannsaka mál.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 2f526a2341c7ef682209ed979fe686e31ad62a37
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648158"
---
# <a name="enable-debug-mode-in-the-tax-calculation-service"></a>Virkja villuleitarstillingu í skattaútreikningsþjónustunni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að virkja villuleitarhaminn í skattaútreikningsþjónustunni til að rannsaka mál.

1. Bæta við **&debug=vs%2 CconfirmExit&** á vefslóð Application Object Server (AOS), og endurnýjaðu síðan síðuna.
2. Þegar þú velur **Söluskattur** til að reikna út söluskattinn, textaskrá sem er nefnd **TaxServiceTroubleshootingLog.txt** er opnað. The **TaxServiceTroubleshootingLog.txt** skrá inniheldur **Skattskyld skjal** og reiknibreytu. Þessum niðurstöðum er skilað frá skattaþjónustu og undantekningarupplýsingum til úrræðaleitar.

## <a name="sample"></a>Dæmi

```json
===============================Tax service calculation input JSON:=====================================
{
    "TaxableDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Transaction Line ID": "5816,68719677391",
            ...
            }
        ],
        "Transaction Header ID": "2022,68719506302",
        ...
        }
    ]
    },
    "Parameter": {
    "ContinueOnErrors": true,
    ...
    },
    "Adjustment": {
    "Lines": {}
    }
}
===========================Tax service calculation result JSON:=================================
{
    "taxDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Tax Codes": {
                ...
            }
        ],
        "Measures": {
            "List Code": "EUTrade"
        },
        "Tax Registration ID": null,
        "Transaction Header ID": "2022,68719506302",
        "Errors": null
        }
    ]
    },
    "solutionId": "b51e0025-cbbe-4d37-bf0b-90d7be4f214d|1",
    "isPartialSuccess": false
}
=============================CorrelationId:==============================
"21f3a8a1-ee9a-477b-b44e-b8ec79e74d16"
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
