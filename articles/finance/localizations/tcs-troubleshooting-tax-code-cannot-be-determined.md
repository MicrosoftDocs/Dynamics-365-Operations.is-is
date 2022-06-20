---
title: Ekki er hægt að ákvarða skattkóða
description: Þessi grein útskýrir hvernig á að leysa villuna "Ekki er hægt að ákvarða skattkóða" í skattaútreikningsþjónustunni.
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
ms.openlocfilehash: 6a74724de38cf362900277ab9addc8e6894f7689
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877860"
---
# <a name="tax-code-cannot-be-determined"></a>Ekki er hægt að ákvarða skattkóða

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir úrræðaleitarskref sem þú getur tekið ef þú færð villuna „Ekki er hægt að ákvarða skattkóða“ í skattaútreikningsþjónustunni.

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

2. Staðfestu að **Hneka söluskatti** valmöguleika á **Uppsetning** flipi upplýsingar um sölupöntunarlínu er virkur.

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

    Ef það eru engin gatnamót fyrir skattflokkinn og vöruskattflokkinn verður skattkóði ekki ákvarðaður.

## <a name="mitigation"></a>Mildun

1. Farðu í gegnum hvert skref í [Úrræðaleit](#troubleshoot) kafla þessarar greinar og lagfærðu uppsetninguna eftir þörfum. Ef skattflokkur og vöruskattflokkur hafa ekki verið ákvarðaðir rétt, sjá [Engin samsvarandi niðurstaða fannst](tcs-troubleshooting-no-matching-result.md).
2. Ef það eru engin gatnamót fyrir skattaflokkinn og vöruskattflokkinn, búðu til nýja eiginleikaútgáfu í RCS og lagfærðu uppsetninguna.

    - Fara til **Skattaeiginleikar** \> **Skattnúmer og hópar** > **Vöruskattflokkur**.

        | Line.Item Tax Group | Skattkóðar |
        |---------------------|-----------|
        | Flokkur B             | A;B       |

    Skattnúmerið verður ákvarðað sem **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
