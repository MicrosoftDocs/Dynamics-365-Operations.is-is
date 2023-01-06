---
title: Engin samsvarandi niðurstaða fannst
description: Þessi grein útskýrir hvernig hægt er að leita að villunni „Engin samsvarandi niðurstaða fannst“ í skattaútreikningsþjónustunni.
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
ms.openlocfilehash: d3bbc76741fdd018d1b2987538b8de7f6d92ee53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845145"
---
# <a name="no-matching-result-could-be-found"></a>Engin samsvarandi niðurstaða fannst

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir villuleitarskrefin sem hægt er að gera ef „Engin samsvarandi niðurstaða fannst“ villa kemur fram í skattaútreikningsþjónustunni.

## <a name="symptom"></a>Einkenni

Eftirfarandi villuboð birtast „Haus/línur - 1, skattkóði, engar niðurstöður fundust.“

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
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
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

Vandamálið kemur upp þegar uppsetning eiginleikans í Regulatory Configuration Service (RCS) er röng.

## <a name="troubleshoot"></a>Úrræðaleit

1. Sækja skrá fyrir úrræðaleit Frekari upplýsingar eru í [Virkja stillingu kembingar fyrir bilanaleit](tcs-troubleshooting-enable-debug-mode.md).
2. Berðu innslátt skattaþjónustuútreikninga saman við uppsetningu eiginleikans til að laga vandamálið við uppsetninguna.

    Eftirfarandi dæmi sýnir innslátt skattþjónustuútreiknings.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    Í eftirfarandi töflu er listi yfir skattahópana í RCS.

    | Header.Viðskiptaferli | Línur.Fyrirtækiseining | Header.Senda úr póstnúmeri | Skattflokkur |
    |-------------------------|---------------------|---------------------------|-----------|
    | Færslubók                 |                     |                           | A-hópur   |
    | Sala                   |                     | 30160                     | Flokkur B   |

    Samkvæmt innslætti á skattþjónustu er **Viðskiptaferli** gildið á hausnum **Sala** og **Póstnúmer sendanda** gildi á hausnum **30159**. Þetta inntak er byggt á uppsetningu reglna um gildissvið í RCS. Villan kemur upp vegna þess að það er engin samsvarandi lína.

    > [!NOTE]
    > Ef gildið í gildisreglunni er autt gildir reglan um hvaða gildi sem er.

## <a name="mitigation"></a>Mildun

Fylgdu þessum skrefum til að lagfæra villuna.

1. Í RCS skal fara í **Altækir eiginleikar** \> **Skattaútreikningur**.
2. Búa til nýja útgáfu eiginleika.
3. Bætt er við línu fyrir samsvarandi upplýsingar.

    | Header.Viðskiptaferli | Línur.Fyrirtækiseining | Header.Senda úr póstnúmeri| Skattflokkur |
    |-------------------------|---------------------|--------------------------|-----------|
    | Færslubók                 |                     |                          | A-hópur   |
    | Sala                   |                     | 30160                    | Flokkur B   |
    | Sala                   |                     | 30159                    | Flokkur B   |

4. Birga uppsetningarútgáfu eiginleika
5. Í Microsoft Dynamics 365 Finance skal fara í **Skattur** \> **Uppsetning** \> **Skattaskilgreining** \> **Færibreytur skattaútreiknings** og velja nýju útgáfuna.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
