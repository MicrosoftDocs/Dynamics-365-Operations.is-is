---
title: Ekki er hægt að ákvarða skattanúmer
description: Þetta efnisatriði útskýrir hvernig á að leysa villuna „Ekki er hægt að ákvarða skattkóða“ í skattaútreikningsþjónustunni.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 3c0914f0013ad2de61cd5a59e3092fef149742e4
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648144"
---
# <a name="tax-code-cannot-be-determined"></a>Ekki er hægt að ákvarða skattanúmer

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir úrræðaleitarskref sem þú getur tekið ef þú færð villu "Ekki er hægt að ákvarða skattkóða" í skattaútreikningsþjónustunni.

## <a name="symptom"></a>Einkenni

Þú færð eftirfarandi villuboð: "Höfuð/línur - 1, ekki er hægt að ákvarða skattkóða." Að öðrum kosti finnur þú villuna í úrræðaleitarskránni, eins og sýnt er í eftirfarandi dæmi. Fyrir frekari upplýsingar, sjá [Virkja villuleitarstillingu fyrir bilanaleit](tcs-troubleshooting-enable-debug-mode.md).

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Orsök

Málið kemur líklega upp vegna þess að skattflokkurinn og vöruskattsflokkurinn skerast ekki.

## <a name="troubleshoot"></a>Úrræðaleit

Fylgdu þessum skrefum til að leysa vandamálið.

1. Í úrræðaleitarskránni skal staðfesta að skattflokkur og vöruskattflokkur hafi verið ákvarðaður. Ef gildin fyrir **Skattahópur** og **Hlutaskattshópur** eru auðir, hefur skattflokkur og vöruskattflokkur ekki verið ákvarðaður. Ef þær hafa verið ákvarðaðar gætu niðurstöðurnar verið rangar.

    Hér er dæmi um úrræðaleitarskrá.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
                            "Adjustment": null
                        }
                    ],
                    "Measures": {
                        ...
                    },
                    ...
                }
            ]
        },
        ...
    }
    ```

2. Staðfestu að **Hneka söluskatti** valmöguleika á **Uppsetning** flipinn í upplýsingum sölupöntunarlínunnar er virkur.

    - Ef það er virkt eru skattkóðar ákvarðaðir af **Skattahópur** og **Vöruskattflokkur** gildi sem þú slærð inn á færslulínuna. Staðfestu að þessi gildi séu rétt slegin inn.
    - Ef það er ekki virkt skaltu ganga úr skugga um að rétt gildi hafi verið stillt fyrir **Gildistími skattaflokka** og **Gildistími vöruskattsflokks** sviðum. Fyrir frekari upplýsingar, sjá [Engin samsvarandi niðurstaða fannst](tcs-troubleshooting-no-matching-result.md) til.

3. Ef skattflokkur og vöruskattflokkur hafa verið ákvörðuð á réttan hátt, ákvarða hvort það séu einhver gatnamót fyrir þá.

    1. Í RCS, farðu til **Skattaeiginleikar** \> **Skattnúmer og hópar** \> **Skattahópur**.

        | Line.Tax Group | Skattkóðar |
        |----------------|-----------|
        | A hópur        | A         |

    2. Fara til **Skattaeiginleikar** \> **Skattnúmer og hópar** \> **Vöruskattflokkur**.

        | Line.Item Tax Group | Skattkóðar |
        |---------------------|-----------|
        | Flokkur B             | V         |

    Ef það eru engin gatnamót fyrir skattaflokkinn og vöruskattflokkinn verður skattkóði ekki ákvarðaður.

## <a name="mitigation"></a>Mildun

1. Farðu í gegnum hvert skref í [Úrræðaleit](#troubleshoot) kafla þessa efnis, og lagfærðu uppsetninguna eftir þörfum. Ef skattflokkur og vöruskattflokkur hafa ekki verið ákvarðaðir rétt, sjá [Engin samsvarandi niðurstaða fannst](tcs-troubleshooting-no-matching-result.md).
2. Ef það eru engin gatnamót fyrir skattaflokkinn og vöruskattflokkinn, búðu til nýja eiginleikaútgáfu í RCS og lagfærðu uppsetninguna.

    - Fara til **Skattaeiginleikar** \> **Skattnúmer og hópar** > **Vöruskattflokkur**.

        | Line.Item Tax Group | Skattkóðar |
        |---------------------|-----------|
        | Flokkur B             | A;B       |

    Skattnúmerið verður ákvarðað sem **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
