---
title: Ekki er hægt að ákvarða skattkóða
description: Í þessari grein er útskýrt hvernig á að úrræðaleita villuna „Ekki er hægt að ákvarða skattkóða“ í skattaútreikningsþjónustunni.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877860"
---
# <a name="tax-code-cannot-be-determined"></a>Ekki er hægt að ákvarða skattkóða

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir skref úrræðaleitar sem hægt er að taka ef upp kemur villan „Ekki er hægt að ákvarða skattkóða“ í skattaútreikningsþjónustunni.

## <a name="symptom"></a>Einkenni

Eftirfarandi villuboð berast „Haus/línur - 1, ekki hægt að ákvarða skattkóða.“ Einnig er hægt að finna villuna í skrá úrræðaleitar eins og sýnt er í eftirfarandi dæmi. Frekari upplýsingar eru í [Virkja stillingu kembingar fyrir bilanaleit](tcs-troubleshooting-enable-debug-mode.md).

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

Vandamálið er líklega tilkomið vegna þess að skatthópurinn og skatthópur vörunnar skarast ekki.

## <a name="troubleshoot"></a>Úrræðaleit

Fylgdu þessum skrefum til að úrræðaleita vandamálið.

1. Í skrá úrræðaleitar skal staðfesta að skattflokkur og skattflokkur vöru hafi verið ákvarðaðir. Ef gildin **Skattflokkur** og **Skattflokkur vöru** eru auð er ekki búið að ákvarða skattflokkinn eða skattflokk vöru. Ef þeir hafa verið ákvarðaðir gætu niðurstöðurnar verið rangar.

    Hér er dæmi um skrá úrræðaleitar.

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

2. Staðfestu að valkosturinn **Hnekkja virðisaukaskatti** í flipanum **Uppsetning** í upplýsingalínu sölupöntunar sé virkur.

    - Ef hann er virkur eru skattkóðar ákvarðaðir af gildinum **Skattflokkur** og **Skattflokkur vörur** sem færð eru inn í færslulínuna. Staðfestið að þessi gildi séu rétt slegin inn.
    - Ef hann er ekki virkur skal staðfesta að rétt gildi hafi verið stillt fyrir reitina **Gildissvið skattflokks** og **Gildissvið skattflokks vörur**. Frekari upplýsingar er að finna í [Engin samsvarandi niðurstaða fannst](tcs-troubleshooting-no-matching-result.md).

3. Ef skattflokkurinn og skattflokkur vöru hafa verið ákvarðaðir á réttan hátt skal finna út hvort þeir skarist.

    1. Í RCS skal fara í **Skattaeiginleikar** \> **Skattkóðar og flokkar** \> **Skattflokkur**.

        | Flokkur Line.Tax | Skattkóðar |
        |----------------|-----------|
        | A-hópur        | A         |

    2. Farðu í **Skattaeiginleikar** \> **Skattkóðar og flokkar** \> **Skattflokkur vöru**.

        | Skattflokkur Line.Item | Skattkóðar |
        |---------------------|-----------|
        | Flokkur B             | V         |

    Ef engin skörun er á skattflokki og skattflokki vöru verður skattkóðinn ekki ákvarðaður.

## <a name="mitigation"></a>Mildun

1. Farðu í gegnum hvert skref í hlutanum [Úrræðaleit](#troubleshoot) í þessari grein og lagaðu uppsetninguna eftir þörfum. Ef skattflokkur og skattflokkur vöru hafa ekki verið ákvarðaðir á réttan hátt skal skoða [Engin samsvarandi niðurstaða fannst](tcs-troubleshooting-no-matching-result.md).
2. Ef engin skörun er á skattflokki og skattflokki vörur skal búa til nýja eiginleikaútgáfu í RCS og laga uppsetninguna.

    - Farðu í **Skattaeiginleikar** \> **Skattkóðar og flokkar** > **Skattflokkur vöru**.

        | Skattflokkur Line.Item | Skattkóðar |
        |---------------------|-----------|
        | Flokkur B             | A;B       |

    Skattkóðinn verður ákvarðaður sem **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
